django-axis-order
=================

In geo applications `coordinate tuples <https://wiki.osgeo.org/wiki/Axis_Order_Confusion>`_ can be ordered either (x,y) or (y,x) or (x,y) but meant as (y,x). 
Based on this problem and on some geo spatial standards which requires to retreive the correct axis order from the `epsg registry <https://epsg.org/API_UsersGuide.html>`_, we developed this simple django app to cache the spatial reference objects.




Quick-Start
-----------

Install it as any other django app to your project:

.. code-block:: bash

    $ pip install django-axis-order

Add `axis_order_cache` to `INSTALLED_APSS`:

.. code-block:: python

    INSTALLED_APSS = [
        # other apps
        "axis_order_cache"
    ]


.. note::
    As pre requirement you will need to install the `gdal and geos binaries <https://docs.djangoproject.com/en/4.2/ref/contrib/gis/install/geolibs/>`_ on your system first.