# website-devilbox

More information at: http://devilbox.org/

rename `metadiablo-devilbox.env` to `.env` then place into a clean `git clone` of devilbox.

after that simply run `docker-compose up`

You can then move the entire website directory into `\data\www`

create symlink `ln -s website/public/ htdocs`

use `tree -L 1` to verify 2 directories.

```
devilbox@php-x.x.x in /shared/httpd/website $ tree -L 1
.
├── website
└── htdocs -> website/public

2 directories, 0 files
```

set up your hosts file to add your DNS record
```
    Open Notepad with administrator privileges
    Browse to C:\Windows\System32\drivers\etc\hosts (Or paste this into the address bar)
    Open the file
    Make your changes
```

for windows add: `127.0.0.1 website.loc`

then browse on to https://website.loc and you're good to go!

(you may need to update your certificate authorities, with firefox you can import the certificate form the devilbox\ca directory)

more instructions found here: https://support.mozilla.org/en-US/kb/setting-certificate-authorities-firefox

For windows 10: https://docs.microsoft.com/en-us/skype-sdk/sdn/articles/installing-the-trusted-root-certificate