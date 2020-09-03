# hello-cgi

CGI Getting Started. Ref. https://httpd.apache.org/docs/2.4/en/howto/cgi.html


## Apache Configure

### cgid_module

Before
```
	# LoadModule cgid_module modules/mod_cgid.so
```

After
```
  LoadModule cgid_module modules/mod_cgid.so
```


## Start Service
```
docker run -it --rm \
  -v $(pwd):/workspace \
  -v $(pwd)/cgi-bin:/usr/local/apache2/cgi-bin \
  -v $(pwd)/httpd.conf:/usr/local/apache2/conf/httpd.conf \
  -p 8080:80 \
  httpd:2.4.46

# On Git Bash
docker run -it --rm \
  -v /$(pwd):/workspace \
  -v /$(pwd)/cgi-bin:/usr/local/apache2/cgi-bin \
  -v /$(pwd)/httpd.conf:/usr/local/apache2/conf/httpd.conf \
  -p 8080:80 \
  httpd:2.4.46
```

## Access

Open `localhost:8080/cgi-bin/first.pl`
