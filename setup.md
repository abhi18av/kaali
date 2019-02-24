# abhi18av

## Customizing a published Vagrant Box

https://scotch.io/tutorials/how-to-create-a-vagrant-base-box-from-an-existing-one


## Base box

https://app.vagrantup.com/offensive-security/boxes/kali-linux


## For customizing the startup and network behaviour
https://www.kali.org/news/announcing-kali-for-vagrant/



## Updated the root password

- Enter the elevated user shell

```
sudo -i
```


- Change the root password 

```
passwd
```


## Setup the System Utils and Packages


```
apt install pkg-config

apt install libsqlite3-dev

apt install libpcre3-dev 


```




## Setup the Nix package manager

- While staying in the root shell

```
mkdir /etc/nix

touch /etc/nix/nix.conf

echo "build-users-group =" > /etc/nix/nix.conf

curl https://nixos.org/nix/install | sh

. /root/.nix-profile/etc/profile.d/nix.sh

nix-channel --add https://nixos.org/channels/nixpkgs-unstable

nix-channel --update

```


# Setup the NeoVim

```
nix-env -iA nixpkgs.neovim


```


# Setup the Julia language 

```
nix-env -iA nixpkgs.julia
```



## Setup OCaml



```

nix-env -iA nixpkgs.opam
opam init --disable-sandboxing

opam install utop
opam install core containers 
opam install ctypes ctypes-foreign
opam install yojson
opam install cohttp lwt
opam install sqlite3
opam install qcheck
opam install alcotest
opam install shcaml
opam install genspio


```


