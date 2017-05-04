Purpose
========
This repository is to demonstrate the issue at https://www.drupal.org/node/2872239 under the simplest setup possible.

Requirements
------------

You must have vagrant installed on your system beforte following the steps below.

Setup
-----
Clone repository:

```
git clone https://github.com/BrianGilbert/2872239.git
```

CD to directory:
```
cd 2872239
```

Run VM:
```
vagrant up
```

Run drupal installation and import config:
http://drupal-8-2-8.local/core/install.php

Back at terminal:
```
drush use @drupal-8-2-8.local
drush cim -y
```

Creat a standard page, Add a new moderation state update to it and set time in the future, save page as draft.

Goto http://drupal-8-2-8.local/admin/reports/status and run c ron manually after the moderation state time has elapsed.

View recent log messages and see error with Message like the following:
'Drupal\Core\Database\DatabaseExceptionWrapper: SQLSTATE…'

