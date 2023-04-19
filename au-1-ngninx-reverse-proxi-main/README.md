# AU-1-ngninx-reverse-proxi

## Setup

1. Add `a.test` and `b.test` host mapping to your localhost

```sh
sudo bash -c '
  echo >> /etc/hosts
  echo "# The following lines are for nginx reverse proxy test" >> /etc/hosts
  echo "127.0.0.1       a.test" >> /etc/hosts
  echo "127.0.0.1       b.test" >> /etc/hosts
'
```

2. Run

```sh
docker-compose up
```

3. Test

```sh
curl a.test
curl b.test
```

You should receive HTML page

Open in your browser:

1. a.test/a.png
2. b.test/b.jpg

You should receive 403 Forbiden error
