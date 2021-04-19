---
description: Der \_ \_ Enumerationstyp WPD Meta Genres beschreibt einen umfangreichen Genre-Typ einer Mediendatei.
ms.assetid: a69cab70-5a45-4e75-abbd-230396c2b5ec
title: WPD_META_GENRES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_META_GENRES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f6ff4875474776df1e2436e0209e6d863f5b3e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369443"
---
# <a name="wpd_meta_genres-enumeration"></a>WPD \_ Meta \_ Genres-Enumeration

Der Enumerationstyp **WPD \_ Meta \_ Genres** beschreibt einen umfangreichen Genre-Typ einer Mediendatei.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_META_GENRES { 
  WPD_META_GENRE_UNUSED                            = 0x0,
  WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE          = 0x1,
  WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE      = 0x11,
  WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES      = 0x12,
  WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK  = 0x13,
  WPD_META_GENRE_SPOKEN_WORD_NEWS                  = 0x14,
  WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS            = 0x15,
  WPD_META_GENRE_GENERIC_VIDEO_FILE                = 0x21,
  WPD_META_GENRE_NEWS_VIDEO_FILE                   = 0x22,
  WPD_META_GENRE_MUSIC_VIDEO_FILE                  = 0x23,
  WPD_META_GENRE_HOME_VIDEO_FILE                   = 0x24,
  WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE           = 0x25,
  WPD_META_GENRE_TELEVISION_VIDEO_FILE             = 0x26,
  WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE   = 0x27,
  WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE          = 0x28,
  WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO       = 0x30,
  WPD_META_GENRE_AUDIO_PODCAST                     = 0x40,
  WPD_META_GENRE_VIDEO_PODCAST                     = 0x41,
  WPD_META_GENRE_MIXED_PODCAST                     = 0x42
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**WPD- \_ Meta- \_ Genre nicht \_ verwendet**
</dt> <dd>

Das Genre wurde nicht festgelegt oder ist nicht anwendbar.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**WPD \_ Meta \_ Genre \_ generic \_ Music \_ - \_ Audiodatei**
</dt> <dd>

Dabei handelt es sich um eine generische Musikdatei (nur Audiodaten).

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_generische WPD \_ -Meta Genre \_ \_ \_ \_ - \_ Audiodatei**
</dt> <dd>

Dabei handelt es sich um eine generische nicht-Musik-Audiodatei, z. b. eine Sprache oder ein Audiobuch.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_ \_ \_ sprach \_ \_ \_ Audiobuch \_ Dateien im WPD-Meta-Genre**
</dt> <dd>

Dies ist eine audiobuchdatei.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**\_ \_ \_ \_ \_ \_ nicht \_ \_ Audiobuch "gesprochene Word-Dateien für WPD"**
</dt> <dd>

Dies ist eine Audiodatei mit Sprech Wörtern, bei der es sich nicht um ein Audiobuch handelt, z. b. ein Interview oder eine Sprache.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD \_ Meta \_ Genre \_ gesprochene \_ Word- \_ Neuigkeiten**
</dt> <dd>

Dies ist eine nachrichtenaudiodatei oder Videodatei.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD \_ Meta \_ Genre \_ gesprochene \_ Word \_ Talk- \_ Sendungen**
</dt> <dd>

Dies ist eine Audioaufzeichnung einer Gesprächs Anzeige.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**generische WPD- \_ \_ Metagenre- \_ \_ Video \_ Datei**
</dt> <dd>

Dies ist eine generische Videodatei.

</dd> <dt>

<span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**WPD- \_ Meta \_ Genre News- \_ \_ Video \_ Datei**
</dt> <dd>

Dies ist eine News-Videodatei.

</dd> <dt>

<span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**WPD \_ Meta \_ Genre \_ Music- \_ Video \_ Datei**
</dt> <dd>

Dies ist eine Musikvideo Datei.

</dd> <dt>

<span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**WPD \_ Meta \_ Genre \_ Home- \_ Video \_ Datei**
</dt> <dd>

Dies ist eine Home-Videodatei.

</dd> <dt>

<span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**WPD \_ Meta \_ Genre \_ Feature \_ Film- \_ Video \_ Datei**
</dt> <dd>

Dies ist eine Videodatei mit einem FeatureFilm.

</dd> <dt>

<span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**WPD \_ Meta \_ Genre \_ TV- \_ Video \_ Datei**
</dt> <dd>

Dies ist eine Videodatei des Fernsehprogramms.

</dd> <dt>

<span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**\_ \_ \_ Schulungs \_ \_ \_ Videodatei für das WPD-Meta Genre**
</dt> <dd>

Dies ist eine Schulungs Videodatei.

</dd> <dt>

<span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**Video Datei für WPD \_ Meta \_ Genre \_ Photo \_ Montage \_ \_**
</dt> <dd>

Dies ist eine Videodatei mit einer Foto-Montage.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**Das WPD \_ \_ -Meta Genre \_ generic \_ Non \_ \_ audionon- \_ Video**
</dt> <dd>

Dabei handelt es sich um eine Datei ohne Audiodaten oder Videos.

</dd> <dt>

<span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**WPD \_ \_ -Meta \_ Genre \_ Audiopodcast**
</dt> <dd>

Dabei handelt es sich um einen Audiopodcast.

</dd> <dt>

<span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**WPD- \_ Meta \_ Genre-Video- \_ \_ Podcast**
</dt> <dd>

Dies ist ein Video-Podcast.

</dd> <dt>

<span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**WPD- \_ Meta \_ Genre \_ gemischter \_ Podcast**
</dt> <dd>

Dies ist ein Podcast, das sowohl Audiodaten als auch Videos enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der [WPD \_ Media \_ Meta \_ Genre](media-properties.md) -Eigenschaft verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




