### BASE ###
FROM alpine:3.9 as base
ARG ARCH
RUN apk --no-cache add \
    $([ "$ARCH" == "amd64" ] && echo "open-vm-tools grub-bios") \
    bash \
    bash-completion \
    blkid \
    busybox-initscripts \
    ca-certificates \
    connman \
    conntrack-tools \
    coreutils \
    curl \
    dbus \
    dosfstools \
    e2fsprogs \
    e2fsprogs-extra \
    findutils \
    grub-efi \
    haveged \
    htop \
    iproute2 \
    iptables \
    jq \
    kbd-bkeymaps \
    logrotate \
    mdadm \
    mdadm-misc \
    ncurses \
    nfs-utils \
    open-iscsi \
    openrc \
    openssh-client \
    openssh-server \
    parted \
    procps \
    qemu-guest-agent \
    rng-tools \
    rsync \
    strace \
    sudo \
    tar \
    util-linux \
    vim \
    xz \
 && mv -vf /etc/conf.d/qemu-guest-agent /etc/conf.d/qemu-guest-agent.orig \
 && mv -vf /etc/conf.d/rngd             /etc/conf.d/rngd.orig \
 && true
RUN apk --no-cache add \
    --repository 'http://dl-cdn.alpinelinux.org/alpine/edge/community' \
    --repository 'http://dl-cdn.alpinelinux.org/alpine/edge/testing' \
    efibootmgr
