============
pytracremote
============

Python wrapper over shell script that manages trac copying and .htpasswd
management on remote server that serves mu;tiple trac instances in different
folders


Requirements
============

1. Software on local host: ssh, apg
2. Software on host with trac: htpasswd

Example usage
=============

.. code-block:: python

	>>> import pytracremote
	>>> t_r = pytracremote.TracRemote(ssh_host="trac.example.com", ssh_user="tracmanager", tracs_dir='/var/lib/trac/projects', htpasswd_path='/var/lib/trac/projects/.htpasswd', chgrp='apache2')
	>>> t_r.get_trac_users()
	['user1', 'user2']