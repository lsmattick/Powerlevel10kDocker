FROM ubuntu

# set termainal color properties
ENV TERM xterm-256color

# update ubuntu
RUN apt update

# Install zsh, git, and curl
RUN apt install zsh -y && \
    apt install git -y && \
    apt install curl -y

# set default to zsh
RUN chsh -s $(which zsh)

# download oh-my-zsh
RUN sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# clone powerlevel10k repo to /root/.oh-my-zsh/themes/
# and generate .zshrc
RUN git clone --depth=1 https://github.com/romkatv/powerlevel10k.git /root/.oh-my-zsh/themes/powerlevel10k

# add preset p10k configs so ther is no set up required
COPY config_files/.p10k.zsh /root/.p10k.zsh
COPY config_files/.zshrc /root/.zshrc

WORKDIR /root

# start terminal on launch
CMD ["/bin/zsh"]
