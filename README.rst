pms
===
.. image:: http://badge.fury.io/py/Poor-Mans-Spotify.png
    :target: https://pypi.python.org/pypi/Poor-Mans-Spotify
.. image:: https://pypip.in/d/Poor-Mans-Spotify/badge.png
    :target: https://pypi.python.org/pypi/Poor-Mans-Spotify

Features
--------
- Search and stream music
- Create playlists
- Download music
- Works with Python 2.7 and 3.x
- Works with Windows, Linux and Mac OSX 10.9
- No Python dependencies
- Requires mplayer

Installation
------------

Using pip::
    
    sudo pip install Poor-Mans-Spotify

Using git::

    git clone https://github.com/np1/pms.git
    
Manually::

Download `zip file <https://github.com/np1/pms/archive/master.zip>`_ or `tar.gz file <https://github.com/np1/pms/archive/master.tar.gz >`_ and extract.

https://github.com/np1/pms/archive/master.zip
https://github.com/np1/pms/archive/master.tar.gz

### Mac OSX installation notes:
    
Download mplayer

    https://www.macupdate.com/app/mac/18580/mplayer

Make a link for mplayer

    ln -s /Applications/MPlayer OSX.app/Contents/Resources/External_Binaries/mplayer.app/Contents/MacOS/mplayer /usr/local/bin/mplayer

Install X11

    http://xquartz.macosforge.org/landing/
    
if using MplayerX: 

    ln -s /Applications/MPlayerX.app/Contents/Resources/binaries/x86_64/mplayer /usr/local/bin/mplayer

# Upgrading

It is recommended you update to the latest version

### Upgrade pip installation:

    sudo pip install Poor-Mans-Spotify --upgrade

### Upgrade git clone:

from within the pms directory;

    git pull


# Usage

    pms is run on the command line using the command:
    
    pms
    
    or ./pms on Linux/MacOS if you are in the same directory


Searching
---------

You can enter an artist/song name to search whenever the program is expecting text
input. Searches must be prefixed with a . character.

When a list of songs is displayed, you can use the following commands:

Downloading
-----------
Enter ```d 3``` to download song 3

Selecting
---------

```all``` to play all

```1,2,3``` to play songs 1 2 and 3

```2-4, 6, 6-3``` to play songs 2, 3, 4, 6, 6, 5, 4, 3

Note: The commands ```shuffle``` and ```repeat``` can be inserted at the start or end of 
any of the above to enable those modes: eg, ```shuffle 1,2,3``` and ```repeat 2-4, 1```


Manipulating
------------
```rm 1,3``` to remove songs 1 and 3.  Also use rm 1,2,5-7 to remove a range

```rm all``` to remove all songs

```sw 1,3``` to swap the position of songs 1 and 3

```mv 1,3``` to move song 1 to postion 3


Playlist commands
-----------------

```add 1,2,3``` to add songs 1,2 and 3 to the temporary playlist.  To add a range,
 ```add 1,2,5-7```  can be entered
    
```add 1,2,3 playlist_name``` to add songs 1,2,3 to a saved playlist.  A new playlist will be created if it doesn't already exist.

```ls``` to list your saved playlists

```open <playlist_name>``` to open a saved playlist as the current playlist

```vp``` to view the working playlist (then use rm, mv and sw to modify it)

```save <playlist_name>``` to save the currently displayed songs as a stored
    playlist on disk

```rm <playlist_name>``` to delete a playlist from disk

You can load a playlist when invoking pms using the following command:

    ```pms open <playlistname>```

```q``` to quit

```h``` for help


# Screenshot
![pms running in terminal](http://i.imgur.com/Oqyz5vk.png "pms running in terminal")

# Usage Example:

    $ > ./pms

    Enter artist/song name or \h for help or \q to quit: wagner

    Searching for 'wagner'

    Item   Size    Artist                Track                  Length   Bitrate 
    1      2.1 Mb  Wilhelm Richard Wagn  Die Hochzeit (Сон в л  03:09    96      
    2      7.2 Mb  Wilhelm Richard Wagn  Ein Sommernachtstraum  03:09    320     
    3      9.2 Mb  Richard Wagner        Ride Of The Valkyries  10:07    128     
    4      5.6 Mb  Wilhelm Richard Wagn  Der Weg In Walghal     04:05    192     
    5      3.2 Mb  Wilhelm Richard Wagn  Die Hochze             02:20    192     
    6      4.8 Mb  Richard Wagner        Carmina Burana         05:19    128     
    7      4.8 Mb  Wagner                O Fortuna (Excalibur   05:18    128     
    8      3.5 Mb  Wilhelm Richard Wagn  Das Leben (Жизнь)      03:55    128     
    9      10. Mb  Johann Sebastian Bac  Concerto in D minor a  04:47    320     
    10     9.2 Mb  Richard Wagner        Die Walküre (Der Ring  10:07    128     
    11     3.4 Mb  Wilhelm Richard Wagn  Spring waltz           01:31    320     
    12     2.1 Mb  Wilhelm Richard Wagn  Die Hochzeit (Der Tra  03:09    96      
    13     9.8 Mb  Richard Wagner (Виль  The Mastersinger of N  10:42    128     
    14     3.2 Mb  Wilhelm Richard Wagn  Die Hochzeit           02:20    192     
    15     10. Mb  Richard Wagner        Tristan and Isolde     11:45    128     
    16     3.5 Mb  Wagner Riñhard        Вальс I. Жизнь         03:55    128     
    17     3.1 Mb  Wilhelm Richard Wagn  Tear                   03:27    128     
    18     5.6 Mb  Wilhelm Richard Wagn  Requem for a dream     04:05    192     
    19     3.8 Mb  Richard Wagner Lisa   Now we are free        04:14    128     
    20     8.8 Mb  Wilhelm Richard Wagn  Der Weg in Walghal     06:28    192     

