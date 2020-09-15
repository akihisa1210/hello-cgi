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
docker-compose up
```

## Access

Open `localhost:8080/cgi-bin/first.pl`
