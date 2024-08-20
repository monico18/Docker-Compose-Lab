FROM sharelatex/sharelatex:latest

# Download and run TeX Live upgrade script
RUN wget http://mirror.ctan.org/systems/texlive/tlnet/update-tlmgr-latest.sh && \
    chmod +x update-tlmgr-latest.sh && \
    ./update-tlmgr-latest.sh -- --upgrade && \
    tlmgr update --self

RUN tlmgr install scheme-full && \
    tlmgr path add

RUN rm update-tlmgr-latest.sh
