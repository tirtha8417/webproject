# webproject
apt update
apt -y upgrade
apt -y install git ruby ruby-dev make clang autoconf curl wget ncurses-utils libsqlite-dev postgresql postgresql-dev libpcap-dev libffi-dev libxslt-dev pkg-config
git clone -b termux https://github.com/timwr/metasploit-framework.git
cd metasploit-framework
gem install bundler
gem install nokogiri -- --using-system-libraries
bundle install --gemfile Gemfile.local
./msfconsole
