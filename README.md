Simple ftp server based on vsftpd.

Minimalistic clone of [fauria/vsftpd](https://hub.docker.com/r/fauria/vsftpd/)\
Based on [bogem/ftp](https://github.com/bogem/dockerfiles/tree/master/ftp)

The ip connection limit is disabled 

# Usage
	$ docker run -d -v <host folder>:/home/vsftpd \
					-p 20:20 -p 21:21 -p 47400-47470:47400-47470 \
					-e FTP_USER=<username> \
					-e FTP_PASS=<password> \
					-e PASV_ADDRESS=<ip address of your server> \
					--name ftp \
					--restart=always ninjawulf98/vsftpd
