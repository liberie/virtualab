all: configure install

configure: 
	#configura as variáveis de sistema
	#./scripts/configure_variables

install: configure
	mkdir -p /etc/xensh
	#users.conf nao utilizado
	#cp shell/users.conf /etc/xensh
	cp shell/vars.config /etc/xensh
	cp shell/xensh /bin/xensh
	cp shell/xenprog /usr/local/sbin
	cp shell/xenprogd /usr/local/sbin
	#cp shell/cron.d/xensh /etc/cron.d/xensh
	echo /bin/xensh >> /etc/shells
	#Adicionando usuário demo
	#adduser --shell /bin/xensh demo
	./scripts/create_first_user
	# OOOOOOOOO  KK   KK
	# OO     OO  KK  KK 
	# OO     OO  KK KK
	# OO     OO  KKK
	# OO     OO  KK KK
	# OO     OO  KK  KK
	# OOOOOOOOO  KK   KK
	echo Sistema instalado

uninstall: clean
	rm -f /etc/xensh/vars.config
	rm -f /bin/xensh
	rm -f /usr/local/sbin/xenprog
	rm -f /usr/local/sbin/xenprogd
	#rm -f /etc/cron.d/xensh 

clean:
	userdel -rf demo


