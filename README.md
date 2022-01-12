# FileBot
For saving naming configs used in FileBot for Plex media

All formats are setup for use with a Windows share containing the Plex media mapped to the Z: drive.

## Movies
Uses the movie name `{n.colon(' - ')}` plus the year `{y}` to create the folder. File name is composed of the built-in Plex format plus video format `$vf`, video codec `$vc`, audio codec `$ac`, followed by the ID number from themoviedb.org `{tmdb-$id}`. It then checks for the strings forced or SDH to preserve multiple subtitle versions in the same language.

## TV
Uses the built-in Plex naming format to generate the show folder `{plex[1]}` followed by the season folder `{plex[2]}`. File name is composed of the built-in Plex format plus video format `$vf`, video codec `$vc`, audio codec `$ac`, followed by the ID number from thetvdb.com `{$id}`. It then checks for the strings forced or SDH to preserve multiple subtitle versions in the same language.

## HDR
The HDR variants are the same as their corresponding preset with the addition of the HDR type `$hdr` after the audio codec. If FileBot can detect the HDR type, the file name will show up correctly. If it can't detect it, only the built-in Plex format will be displayed. If this happens, re-match using the normal mode.
