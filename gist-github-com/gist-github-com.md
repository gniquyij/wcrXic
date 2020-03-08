If you visit gist.github.com in China, you might find:

![(gist-unreachable](./gist-unreachable.png)

## What happened?

`dig +trace gist.github.com`, found the A record of gist.github.com was returned by a generic top level domain name (gTLD) server, which was not [the expected](https://vjyq.github.io/wcrXic/).

![gist-unreachable-reason](./gist-unreachable-reason.png)

## Make it reachable

Open your terminal, `sudo vi /etc/hosts`, add the following line, then save:

```
192.30.253.119  gist.github.com
```

Here you go:

![(gist-reachable](./gist-reachable.png)
