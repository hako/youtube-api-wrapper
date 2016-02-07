===========
Basic usage
===========

Videos
------

The VideoAPI class gives access to the `Videos API endpoint. <https://developers.google.com/youtube/v3/docs/videos>`_ .

.. automodule:: youtube_api.client
   :members:

Examples:

.. code-block:: python

    from youtube_api.client import VideoAPI

    client = VideoAPI('API_KEY')

    video = client.get_video_by_id('Video Id')


Channels
------

The ChannelsAPI class gives access to the `Channels API endpoint. <https://developers.google.com/youtube/v3/docs/channels>`_ .

.. automodule:: youtube_api.client
   :members:

Examples:

.. code-block:: python

    from youtube_api.client import ChannelsAPI

    client = ChannelsAPI('API_KEY')

    data = client.get_channel_for_username('Username')



By default only snippet part is retrieved. `Querying for more parts. <https://developers.google.com/youtube/v3/getting-started#part>`_
results in an higher quota consumption. It's possible to check the quota used before submitting the query by calling:

.. code-block:: python

    client.calculate_quota(('snippet', 'contentDetails'))
    >>> 4

