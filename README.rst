scrapy-rotating-free-proxies
============================
Avoid being banned by webpages when you crawl them. This is an extension to the amazing scrapy-rotating-proxies_ library this with very minor changes. The main target of this library is to get proxies dynamically when the spider is running. This library automatically fetches freely available lists of proxies from free-proxy-list.net_.

.. _scrapy-rotating-proxies: https://pypi.python.org/pypi/scrapy-rotating-free-proxies
.. _free-proxy-list.net: https://free-proxy-list.net/


Installation
------------
::

    pip install scrapy-rotating-free-proxies

Usage
-----

After installing you need to do just add following two variables in settings.py of your Scrapy project ::


    ROTATING_PROXY_LIST_PATH = '/my/path/proxies.txt'

    DOWNLOADER_MIDDLEWARES = {
        'rotating_proxies.middlewares.RotatingProxyMiddleware': 610,
        'rotating_proxies.middlewares.BanDetectionMiddleware': 620,
    }



For further details on using this library, refer to the original readme_.

.. _readme: https://github.com/TeamHG-Memex/scrapy-rotating-proxies/blob/master/README.rst


Thank you!
