
default:	build

clean:
	rm -rf Makefile objs

build:
	$(MAKE) -f objs/Makefile

install:
	$(MAKE) -f objs/Makefile install

modules:
	$(MAKE) -f objs/Makefile modules

upgrade:
	/usr/local/cac/sbin/nginx -t

	kill -USR2 `cat /usr/local/cac/logs/nginx.pid`
	sleep 1
	test -f /usr/local/cac/logs/nginx.pid.oldbin

	kill -QUIT `cat /usr/local/cac/logs/nginx.pid.oldbin`
