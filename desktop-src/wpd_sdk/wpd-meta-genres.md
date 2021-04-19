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
# <a name="wpd_meta_genres-enumeration"></a><span data-ttu-id="2d20a-103">WPD \_ Meta \_ Genres-Enumeration</span><span class="sxs-lookup"><span data-stu-id="2d20a-103">WPD\_META\_GENRES enumeration</span></span>

<span data-ttu-id="2d20a-104">Der Enumerationstyp **WPD \_ Meta \_ Genres** beschreibt einen umfangreichen Genre-Typ einer Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="2d20a-104">The **WPD\_META\_GENRES** enumeration type describes a broad genre type of a media file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d20a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d20a-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="2d20a-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="2d20a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2d20a-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**WPD- \_ Meta- \_ Genre nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2d20a-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**WPD\_META\_GENRE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-108">Das Genre wurde nicht festgelegt oder ist nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="2d20a-108">The genre has not been set, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**WPD \_ Meta \_ Genre \_ generic \_ Music \_ - \_ Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="2d20a-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-110">Dabei handelt es sich um eine generische Musikdatei (nur Audiodaten).</span><span class="sxs-lookup"><span data-stu-id="2d20a-110">This is a generic music file (audio only).</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_generische WPD \_ -Meta Genre \_ \_ \_ \_ - \_ Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="2d20a-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-112">Dabei handelt es sich um eine generische nicht-Musik-Audiodatei, z. b. eine Sprache oder ein Audiobuch.</span><span class="sxs-lookup"><span data-stu-id="2d20a-112">This is a generic non-music audio file, for example, a speech or audio book.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_ \_ \_ sprach \_ \_ \_ Audiobuch \_ Dateien im WPD-Meta-Genre**</span><span class="sxs-lookup"><span data-stu-id="2d20a-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_AUDIO\_BOOK\_FILES**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-114">Dies ist eine audiobuchdatei.</span><span class="sxs-lookup"><span data-stu-id="2d20a-114">This is an audio book file.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**\_ \_ \_ \_ \_ \_ nicht \_ \_ Audiobuch "gesprochene Word-Dateien für WPD"**</span><span class="sxs-lookup"><span data-stu-id="2d20a-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_FILES\_NON\_AUDIO\_BOOK**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-116">Dies ist eine Audiodatei mit Sprech Wörtern, bei der es sich nicht um ein Audiobuch handelt, z. b. ein Interview oder eine Sprache.</span><span class="sxs-lookup"><span data-stu-id="2d20a-116">This is a spoken-word audio file that is not an audio book, for example, an interview or speech.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD \_ Meta \_ Genre \_ gesprochene \_ Word- \_ Neuigkeiten**</span><span class="sxs-lookup"><span data-stu-id="2d20a-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_NEWS**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-118">Dies ist eine nachrichtenaudiodatei oder Videodatei.</span><span class="sxs-lookup"><span data-stu-id="2d20a-118">This is a news audio or video file.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD \_ Meta \_ Genre \_ gesprochene \_ Word \_ Talk- \_ Sendungen**</span><span class="sxs-lookup"><span data-stu-id="2d20a-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_TALK\_SHOWS**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-120">Dies ist eine Audioaufzeichnung einer Gesprächs Anzeige.</span><span class="sxs-lookup"><span data-stu-id="2d20a-120">This is an audio recording of a talk show.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**generische WPD- \_ \_ Metagenre- \_ \_ Video \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="2d20a-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**WPD\_META\_GENRE\_GENERIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-122">Dies ist eine generische Videodatei.</span><span class="sxs-lookup"><span data-stu-id="2d20a-122">This is a generic video file.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**WPD- \_ Meta \_ Genre News- \_ \_ Video \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="2d20a-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**WPD\_META\_GENRE\_NEWS\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-124">Dies ist eine News-Videodatei.</span><span class="sxs-lookup"><span data-stu-id="2d20a-124">This is a news video file.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**WPD \_ Meta \_ Genre \_ Music- \_ Video \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="2d20a-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**WPD\_META\_GENRE\_MUSIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-126">Dies ist eine Musikvideo Datei.</span><span class="sxs-lookup"><span data-stu-id="2d20a-126">This is a music video file.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**WPD \_ Meta \_ Genre \_ Home- \_ Video \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="2d20a-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**WPD\_META\_GENRE\_HOME\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-128">Dies ist eine Home-Videodatei.</span><span class="sxs-lookup"><span data-stu-id="2d20a-128">This is a home video file.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**WPD \_ Meta \_ Genre \_ Feature \_ Film- \_ Video \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="2d20a-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**WPD\_META\_GENRE\_FEATURE\_FILM\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-130">Dies ist eine Videodatei mit einem FeatureFilm.</span><span class="sxs-lookup"><span data-stu-id="2d20a-130">This is a feature film video file.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**WPD \_ Meta \_ Genre \_ TV- \_ Video \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="2d20a-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**WPD\_META\_GENRE\_TELEVISION\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-132">Dies ist eine Videodatei des Fernsehprogramms.</span><span class="sxs-lookup"><span data-stu-id="2d20a-132">This is a television program video file.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**\_ \_ \_ Schulungs \_ \_ \_ Videodatei für das WPD-Meta Genre**</span><span class="sxs-lookup"><span data-stu-id="2d20a-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**WPD\_META\_GENRE\_TRAINING\_EDUCATIONAL\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-134">Dies ist eine Schulungs Videodatei.</span><span class="sxs-lookup"><span data-stu-id="2d20a-134">This is an educational video file.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**Video Datei für WPD \_ Meta \_ Genre \_ Photo \_ Montage \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d20a-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**WPD\_META\_GENRE\_PHOTO\_MONTAGE\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-136">Dies ist eine Videodatei mit einer Foto-Montage.</span><span class="sxs-lookup"><span data-stu-id="2d20a-136">This is a video file featuring a photo montage.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**Das WPD \_ \_ -Meta Genre \_ generic \_ Non \_ \_ audionon- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="2d20a-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_AUDIO\_NON\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-138">Dabei handelt es sich um eine Datei ohne Audiodaten oder Videos.</span><span class="sxs-lookup"><span data-stu-id="2d20a-138">This is a file without audio or video.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**WPD \_ \_ -Meta \_ Genre \_ Audiopodcast**</span><span class="sxs-lookup"><span data-stu-id="2d20a-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**WPD\_META\_GENRE\_AUDIO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-140">Dabei handelt es sich um einen Audiopodcast.</span><span class="sxs-lookup"><span data-stu-id="2d20a-140">This is an audio podcast.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**WPD- \_ Meta \_ Genre-Video- \_ \_ Podcast**</span><span class="sxs-lookup"><span data-stu-id="2d20a-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**WPD\_META\_GENRE\_VIDEO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-142">Dies ist ein Video-Podcast.</span><span class="sxs-lookup"><span data-stu-id="2d20a-142">This is a video podcast.</span></span>

</dd> <dt>

<span data-ttu-id="2d20a-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**WPD- \_ Meta \_ Genre \_ gemischter \_ Podcast**</span><span class="sxs-lookup"><span data-stu-id="2d20a-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**WPD\_META\_GENRE\_MIXED\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="2d20a-144">Dies ist ein Podcast, das sowohl Audiodaten als auch Videos enthält.</span><span class="sxs-lookup"><span data-stu-id="2d20a-144">This is a podcast containing both audio and video.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d20a-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d20a-145">Remarks</span></span>

<span data-ttu-id="2d20a-146">Diese Enumeration wird von der [WPD \_ Media \_ Meta \_ Genre](media-properties.md) -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d20a-146">This enumeration is used by the [WPD\_MEDIA\_META\_GENRE](media-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d20a-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d20a-147">Requirements</span></span>



| <span data-ttu-id="2d20a-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d20a-148">Requirement</span></span> | <span data-ttu-id="2d20a-149">Wert</span><span class="sxs-lookup"><span data-stu-id="2d20a-149">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d20a-150">Header</span><span class="sxs-lookup"><span data-stu-id="2d20a-150">Header</span></span><br/> | <dl> <span data-ttu-id="2d20a-151"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d20a-151"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d20a-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d20a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d20a-153">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="2d20a-153">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




