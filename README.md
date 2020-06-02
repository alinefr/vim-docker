# vim-docker

This is a docker container with [bash](https://www.gnu.org/software/bash/) & [vim](https://www.vim.org/).
It's built from alpine, in order to be as minimal as possible.

## Why?

I really like named docker volumes. When I want to edit something in one of those volumes, I use to do like this. Suppose my volume is named `myvolume`:

```
docker run -v myvolume:/mnt/myvolume -ti debian /bin/bash
```

But, before this, I have to:

```
apt update && apt -y install vim
```

Now, I just do:

```
docker run -v myvolume:/mnt/myvolume -ti alinefr/vim /bin/bash
```

So this container makes things more convenient. I did it to myself, to help me be more productive. If you find this useful, just use it!
