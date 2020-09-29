```sh
bazel build @getdns//:binaries
rm -f stubby stubby.yml libunbound.so.8
find -L bazel-out -type f -path "**/copy_*/**" -and \( -name "stubby" -or -name "stubby.yml" -or -name "libunbound.so.8" \) -exec cp {} . \;
chmod a+w stubby
patchelf --set-rpath . stubby
sudo setcap 'cap_net_bind_service=+ep' stubby
```

```sh
./stubby -C stubby.yml
```
