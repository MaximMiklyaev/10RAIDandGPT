///////////////////RAID10 GPT

****Добавить в Vagrantfile еще дисков / в данном примере 5 дисков

*****************************************
:disks => {
	  :sata1 => {
	     :dfile => './sata1.vdi',
	     :size => 250,
	     :port => 1
		    },
	  :sata2 => {
            :dfile => './sata2.vdi',
            :size => 250, # Megabytes
	     :port => 2
		    },
          :sata3 => {
            :dfile => './sata3.vdi',
            :size => 250,
            :port => 3
                    },
          :sata4 => {
            :dfile => './sata4.vdi',
            :size => 250, # Megabytes
            :port => 4
                    },
          :sata5 => {
            :dfile => './sata5.vdi',
            :size => 250, # Megabytes
            :port => 5
                    }
**********************************************

***скачиваем Vagrantfile

git clone https://github.com/MaximMiklyaev/10RAIDandGPT.git

***переходим в директорию 

cd /raid

***запускаем образ / авторежиме соберётся RAID10 и создастся раздел GPT на RAID

vagrant up

