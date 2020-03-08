# deser-ruby

Deser-ruby is a script to automatically generate serialized payloads on Ruby/Rails and other Ruby driven applications, which deserialize data from user input using `Marshal.load` or `YAML.load`.

The generated payloads use the **Universal RCE for Ruby 2.x** to gain RCE capabilities over the target application.

## Usage

Using deser-ruby is very straightforward::

```
$ ruby deser-ruby.rb --help
Usage: serializer.rb [options]
    -s, --save=FILE                  File to store payload (default=payload)
    -y, --yaml                       Generate YAML payload (default is False)
    -t, --test                       Attempt payload deserialization
    -c, --command=COMMAND            Command to execute
    -e, --encode=ENCODE              Encode payload (base64|hex)
    -h, --help                       Prints this help
```

**Attention:** Using `-t`, the serialized payload will be executed on your system!

#### References

* [Universal RCE for Ruby 2.x](https://www.elttam.com/blog/ruby-deserialization/)
* [Universal RCE for Ruby2.x - YAML](https://staaldraad.github.io/post/2019-03-02-universal-rce-ruby-yaml-load/)