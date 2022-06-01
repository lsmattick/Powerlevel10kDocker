# Powerlevel10kDocker
A minimal example docker image using ubuntu with the romkatv/powerlevel10k zsh theme.

This git repo contains a minimal dockerfile to use the powerlevel10k theme in a docker container. For more information on the powerlevel10k zsh theme: https://github.com/romkatv/powerlevel10k#readme

I highly recommend downloading the recommended fonts that go with the powerlevel10k theme. Download fonts the in the following link to the machine you will be using terminal on: https://github.com/romkatv/powerlevel10k#fonts

For a minimal image, refer to the minimal_image directory. If you want to use preset configs, load in the .p10k.zsh and .zshrc files to your docker image. An example of this is given in the image_wigh_configs directory.

To generate the .p10k.zsh and .zshrc files, get a docker container running using the minimal_image docker file. Go throug the set up process. Make any final customizations by editing the .p10k.zsh file. Save the resulting .p10k.zsh and .zshrc.
