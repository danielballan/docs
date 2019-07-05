***********************
Using GitHub at NSLS-II
***********************

Two-factor authentication
-------------------------

We strongly recommend `securing your account with two-factor authentication <https://help.github.com/en/articles/securing-your-account-with-two-factor-authentication-2fa>`_.

For normal use from the campus network, the most convenient way to access
GitHub is using SSH. See `GitHub's SSH guide <https://help.github.com/en/articles/connecting-to-github-with-ssh>`_.
Your remotes will look like:

.. code-block:: bash


   $ git remote -v
   danielballan   git@github.com:danielballan/bluesky (fetch)
   danielballan   git@github.com:danielballan/bluesky (push)
   origin         git@github.com:bluesky/bluesky (fetch)
   origin         git@github.com:bluesky/bluesky (push)

Note ``git@github.com:`` in place of where you might have
``https://github.com/``. You can update a remote using

.. code-block:: bash

   $ git remote set-url <NAME> <NEW_URL>

For use inside the ring, connecting via SSH does not work. (Consult ITC to ask
why.) Your best option is to a personal access token, which you can do at
`github.com/settings/tokens <https://github.com/settings/tokens>`_ or by
following `GitHub's token guide <https://help.github.com/en/articles/creating-a-personal-access-token-for-the-command-line>`_.
You can then paste the token into a file in your home directory. Make sure
to restrict the permissions with ``chmod 600 path/to/file_with_token`` or any
user will be able to read it and log into GitHub as you!

To *use* the token, set the remote urls in the HTTPS style
(not ``git@github.com:``). When you try to push you will be prompted to enter
your username. Paste the token it instead. GitHub will recognize your username
automatically from the token.
