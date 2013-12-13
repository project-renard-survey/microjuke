# MicroJuke - Minimal audio player for Linux
By: Joe Gillotti <joe@u13.net> released under the GPL

NOTE: This is *extremely* beta. I've been listening to it a lot lately, but it 
really lacks polish in its current state. (-feb 1, 2012)

### Start Here 
1. Install dependencies (as below.
2. Run `perl gather.pl PathToMusicFolder`
3. Run `perl microjuke.pl`

At this beta release, the song parser is not yet incorporated
into the main gui layout.

For last.fm:
1. go to File -> Plugins. Tick the Last.FM box
2. restart microjuke
3. go to Last.FM > Authenticate as different user
4. It will open your web browser to last.fm's app auth page
5. Log in / click allow access. 

### Features 
- Automatically recursively parse and construct your song library
- Quickly find and play the thousands of tracks in your library
- Scrobble plays to last.fm

### Dependencies 

Necessary dependencies and perl modules are:
- Gstreamer
- Glib
- Gtk2
- Gtk2::SimpleMenu
- Gtk2::SimpleList
- MP3::Info
- LWP

The following are optional. On systems that do not provide packages for them, install
vorbis-tools and flac, for potentially slightly slower performance when parsing
- Ogg::Vorbis::Header
- Audio::FLAC::Header
- MP4::Info
- Audio::WMA

### How to install dependencies 

Ubuntu/Debian:
`apt-get install libgstreamer-perl libgstreamer-interfaces-perl  libgtk2-perl libmp3-info-perl libogg-vorbis-header-perl libaudio-flac-header-perl gstreamer0.10-plugins-bad gstreamer0.10-plugins-base gstreamer0.10-plugins-good gstreamer0.10-plugins-ugly libgtk2-notify-perl xdg-utils libxml-simple-perl libmp4-info-perl libaudio-wma-perl`

Fedora (you may need to enable RPMForge):
`yum install perl-Gtk2 perl-MP3-Info perl-GStreamer perl-libwww-perl.noarch vorbis-tools flac perl-Gtk2-Notify xdg-utils perl-XML-Simple`

FreeBSD - install these ports/packages:
`p5-Gtk2 p5-Glib2 p5-GStreamer gstreamer-plugins-bad gstreamer-plugins-good gstreamer-plugins-ugly p5-MP3-Info p5-audio-flac-header p5-Ogg-Vorbis-Header`
