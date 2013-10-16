:title: Images Command
:description: List images
:keywords: images, docker, container, documentation

=========================
``images`` -- List images
=========================

::

    Usage: docker images [OPTIONS] [NAME]

    List images

      -a=false: show all images. Only 'Head' or endpoint images are listed by default.
      -notrunc=false: Don't truncate output
      -q=false: only show numeric IDs
      -viz=false: output in graphviz format

The following example lists an untagged image, and the docker and ubuntu images pulled from the docker image registry.

The resultant list shows the short ID of the image - if you need the long ID, add -notrunc

::

    # docker images
    REPOSITORY              TAG                 ID                  CREATED             SIZE
    docker                  latest              b3bb541ba6ef        6 hours ago         20.08 MB (virtual 1.078 GB)
    <none>                  <none>              362600dd69de        12 hours ago        148.6 MB (virtual 280.3 MB)
    ubuntu                  12.04               8dbd9e392a96        6 months ago        131.5 MB (virtual 131.5 MB)
    ubuntu                  latest              8dbd9e392a96        6 months ago        131.5 MB (virtual 131.5 MB)
    ubuntu                  precise             8dbd9e392a96        6 months ago        131.5 MB (virtual 131.5 MB)
    ubuntu                  12.10               b750fe79269d        6 months ago        24.65 kB (virtual 180.1 MB)
    ubuntu                  quantal             b750fe79269d        6 months ago        24.65 kB (virtual 180.1 MB)


Displaying images visually
--------------------------

::

    sudo docker images -viz | dot -Tpng -o docker.png

.. image:: https://docs.docker.io/en/latest/_static/docker_images.gif
