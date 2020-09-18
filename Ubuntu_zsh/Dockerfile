# ubuntu install
FROM ubuntu
MAINTAINER 9r00t
RUN apt-get -y update && \
    apt-get install -y git\
    wget

# zsh install & change shell
RUN apt-get -y install zsh
RUN chsh -s /usr/bin/zsh

# oh-my-zsh install
RUN sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# powerline install
RUN apt-get -y install fonts-powerline

# hack font install
COPY ttf /ttf
ENV TERM xterm-256color

# bullet-train theme install
RUN git clone https://github.com/caiogondim/bullet-train.zsh.git ~/.oh-my-zsh/custom/theme/bullet-train
ENV ZSH_THEME bullet-train/bullet-train
COPY .zshrc /root/.zshrc
CMD ["zsh"]
#FROM zshusers/zsh

