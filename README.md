# blog

A *markdown* based minimal blog written in Flask. 

## Running It

```bash
$ pip install -r requirements.txt && ./blog
```

Open [Login](http://localhost:5000/login/) page.

The password is `Password` by default.

## Modifications

The original can be found at: [Peewee](https://github.com/coleifer/peewee)

It is customized for adding File upload, Password hashing, Better error handling and Custom CSS/Branding.

It also allows you to change the Bind Host and Port.

## Technical

It is meant to be a single tenant software. The user running it is responsible for their data.

It persists data to `~/.${USER}-blog.db` and uploads files to `~/.${USER}-blog-uploads/`

Authenticate via `~/.${USER}-blog.pass` file or `${PASSWORD_HASH}` variable. Passwords are obtained by:

```bash
$ echo -n Password | openssl dgst -binary -sha256 | base64
```

## Questions?

Reach out to Karthik Kumar Viswanathan *karthikkumar at gmail dot com* if you have anything to say about it.
