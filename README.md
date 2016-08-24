suds-passworddigest
===================

adds Web Services Security PasswordDigest authentication to SUDS

Installation
----------------

installation is simple

    pip install git+https://github.com/miuhaki/suds-passworddigest-py3.git


Usage
-------------------

    from suds.client import Client
    from suds.wsse import Security

    from suds_passworddigest.token import UsernameDigestToken

    client = Client()
    security = Security()
    token = UsernameDigestToken('my_username', 'my_pass')
    security.tokens.append(token)
    client.set_options(wsse=security)
