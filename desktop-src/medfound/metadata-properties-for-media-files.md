---
description: In diesem Thema werden die gängigsten Metadateneigenschaften für Mediendateien aufgelistet.
ms.assetid: 35187720-413a-45a0-8558-918f7c3161e1
title: Metadateneigenschaften für Mediendateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cab541a480b03d7ef6bfb9a1a2036226b767774
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354902"
---
# <a name="metadata-properties-for-media-files"></a>Metadateneigenschaften für Mediendateien

In diesem Thema werden die gängigsten Metadateneigenschaften für Mediendateien aufgelistet.

-   [Allgemeine Medien Eigenschaften](#common-media-properties)
-   [Medien Freigabe Eigenschaften](#media-sharing-properties)
-   [SDK-Zuordnungen im Windows Media-Format](#windows-media-format-sdk-mappings)
-   [Zugehörige Themen](#related-topics)

## <a name="common-media-properties"></a>Allgemeine Medien Eigenschaften

Das shelleigenschaftssystem definiert einen Satz allgemeiner Metadateneigenschaften für alle Arten von shellobjekten. Eine Teilmenge ist für Mediendateien anwendbar. In der folgenden Tabelle sind die gängigsten Shelleigenschaften für Medien aufgeführt. Mediendateien unterstützen möglicherweise weitere Eigenschaften, die hier nicht aufgeführt sind. Außerdem unterstützt nicht jedes Dateiformat alle aufgelisteten Eigenschaften. Eine umfassende Liste der Shelleigenschaften finden Sie unter [Shelleigenschaften](/previous-versions//ff521730(v=vs.85)).



| PROPERTYKEY                                                              | Shellname                                                                                    | BESCHREIBUNG                                                                                                                                                                                               | Datentyp    |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [\_ \_ DLNA- \_ Profil- \_ ID für mfpkey-Inhalt](mfpkey-content-dlna-profile-id.md) | Keine                                                                                          | Der DLNA-Profil Bezeichner (Digital Living Network Alliance).                                                                                                                                                | VT \_ LPWSTR   |
| **Pkey \_ - \_ audiochannelanzahl**                                            | [System. Audio. ChannelCount](../properties/props-system-audio-channelcount.md)                       | Anzahl der Audiokanäle.                                                                                                                                                                                 | VT \_ UI4      |
| **Pkey \_ - \_ audioencodingbitrate**                                         | [System. Audio. encodingbitrate](../properties/props-system-audio-encodingbitrate.md)                 | Die durchschnittliche Audiobitrate in Bits pro Sekunde.                                                                                                                                                               | VT \_ UI4      |
| **Pkey \_ - \_ Audioformat**                                                  | [System. Audio. Format](../properties/props-system-audio-format.md)                                   | Audiountertyp ([**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)), ausgedrückt als Zeichenfolge.                                                                                                                 | VT \_ LPWSTR   |
| **Pkey \_ -Audiodatei " \_ isvariablebitrate"**                                       | [System. Audio. isvariablebitrate](../properties/props-system-audio-isvariablebitrate.md)             | Gibt an, ob der Audiostream Variablen-Bitrate-Codierung verwendet.                                                                                                                                       | VT \_ bool     |
| **Pkey \_ - \_ audiodatenwert**                                               | [System. Audio. Peer Value](../properties/props-system-audio-peakvalue.md)                             | Maximale Volumeebene von Audioinhalten.                                                                                                                                                                       | VT \_ UI4      |
| **Pkey \_ -Audiodatei ( \_ Samplerate)**                                              | [System. Audio. Samplerate](../properties/props-system-audio-samplerate.md)                           | Audiobeispielrate in Samplings pro Sekunde. Entspricht dem Attribut " [**MF \_ MT \_ - \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md) " im Medientyp.                           | VT \_ UI4      |
| **Pkey \_ - \_ audiosamplesize**                                              | [System. Audiodatei. samplesize](../properties/props-system-audio-samplesize.md)                           | Anzahl von Bits pro audiostich Probe. Entspricht dem [**MF \_ MT \_ - \_ audiobits \_ pro \_ Sample-**](mf-mt-audio-bits-per-sample-attribute.md) Attribut im Medientyp.                                         | VT \_ UI4      |
| **Pkey \_ - \_ audiostreamnummer**                                            | [System. Audiodatei. streamnumber](../properties/props-system-audio-streamnumber.md)                       | Der Bezeichner des Audiodatenstroms.                                                                                                                                                                           | VT \_ UI4      |
| **Pkey- \_ Autor**                                                         | [System.Author](../properties/props-system-author.md)                                               | Schrift.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **Pkey- \_ Kommentar**                                                        | [System. Comment](../properties/props-system-comment.md)                                             | Ein an eine Datei angefügter Kommentar, der normalerweise von einem Benutzer hinzugefügt wird.                                                                                                                                                  | VT \_ LPWSTR   |
| **Pkey- \_ Copyright**                                                      | [System. Copyright](../properties/props-system-copyright.md)                                         | Copyright Informationen                                                                                                                                                                                    | VT \_ LPWSTR   |
| **Pkey \_ DRM \_ isprotehiert**                                               | [System. DRM. IsProtected](../properties/props-system-drm-isprotected.md)                             | Gibt an, ob der Inhalt durch Digital Rights Management (DRM) geschützt ist.                                                                                                                         | VT \_ bool     |
| **Pkey- \_ Schlüsselwörter**                                                       | [System.Keywords](../properties/props-system-keywords.md)                                           | Keywords.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **Pkey- \_ Sprache**                                                       | [System. Language](../properties/props-system-language.md)                                           | Sprache:                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **Pkey \_ Media \_ authorurl**                                               | [System. Media. authorurl](../properties/props-system-media-authorurl.md)                             | URL der Website des Autors.                                                                                                                                                                              | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ averagelevel**                                            | [System. Media. averagelevel](../properties/props-system-media-averagelevel.md)                       | Durchschnittliche Volumeebene für Audioinhalte.                                                                                                                                                                    | VT \_ UI4      |
| **Pkey- \_ Medien \_ classprimaryid**                                          | [System. Media. classprimaryid](../properties/props-system-media-classprimaryid.md)                   | Die Zeichen folgen Darstellung einer GUID, die die primäre Klasse von Medien angibt. Gültige Werte finden Sie in der Dokumentation zum [**WM/mediaclassprimaryid-**](../wmformat/wm-mediaprimaryid.md) Attribut.       | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ classsecondaryid**                                        | [System. Media. classsecondaryid](../properties/props-system-media-classsecondaryid.md)               | Die Zeichen folgen Darstellung einer GUID, die die sekundäre Klasse von Medien angibt. Gültige Werte finden Sie in der Dokumentation für das [**WM/MediaClassSecondaryID-**](../wmformat/wm-mediasecondaryid.md) Attribut. | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ collectiongroupid**                                       | [System. Media. collectiongroupid](../properties/props-system-media-collectiongroupid.md)             | Die Zeichen folgen Darstellung einer GUID, die die Sammlungs Gruppe identifiziert.                                                                                                                                 | VT \_ LPWSTR   |
| **Pkey \_ Medien \_ CollectionId**                                            | [System. Media. CollectionId](../properties/props-system-media-collectionid.md)                       | Die Zeichen folgen Darstellung einer GUID, die die Auflistung identifiziert.                                                                                                                                       | VT \_ LPWSTR   |
| **Pkey \_ Media- \_ Inhalts Verteiler**                                      | [System. Media. contentdistributor](../properties/props-system-media-contentdistributor.md)           | Der Verteiler des Inhalts.                                                                                                                                                                               | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ contentid**                                               | [System. Media. contentid](../properties/props-system-media-contentid.md)                             | Die Zeichen folgen Darstellung einer GUID, die die Auflistung identifiziert.                                                                                                                                       | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ datecodiert**                                             | [System. Media. datecodiert](../properties/props-system-media-dateencoded.md)                         | Zeitpunkt, zu dem der Inhalt codiert wurde.                                                                                                                                                                        | VT \_ FILETIME |
| **Pkey \_ Media \_ datereleasing**                                            | [System. Media. datereleasing](../properties/props-system-media-datereleased.md)                       | Ursprüngliches Veröffentlichungsdatum.                                                                                                                                                                                    | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ Dauer**                                                | [System. Media. Duration](../properties/props-system-media-duration.md)                               | Dauer in 100-Nanosecond-Einheiten. Äquivalent zum " [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) "-Attribut im Präsentations Deskriptor.                                                       | VT \_ UI8      |
| **Pkey- \_ Medien \_ dvdid**                                                   | [System. Media. dvdid](../properties/props-system-media-dvdid.md)                                     | Digital Video Disk Identifier (dvdid).                                                                                                                                                                    | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ encodby**                                               | [System. Media. encodecodby](../properties/props-system-media-encodedby.md)                             | Der Name der Person oder Gruppe, die den Inhalt codiert hat.                                                                                                                                                     | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ Codierungs Einstellungen**                                        | [System. Media. encodingsettings](../properties/props-system-media-encodingsettings.md)               | Beschreibung der Einstellungen, die zum Codieren des Inhalts verwendet werden.                                                                                                                                                   | VT \_ LPWSTR   |
| **Pkey \_ Media- \_ MCDI**                                                    | [System. Media. MCDI](../properties/props-system-media-mcdi.md)                                       | Musik-CD-Bezeichner. Dieser Wert wird verwendet, um eine CD zu identifizieren.                                                                                                                                                 | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ MetadataContentProvider**                                 | [System. Media. MetadataContentProvider](../properties/props-system-media-metadatacontentprovider.md) | Der Name des metadateninhaltsanbieters. (Beispielsweise können Metadaten von einem kommerziellen Dienst bereitgestellt werden.)                                                                                                 | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ Producer**                                                | [System. Media. Producer](../properties/props-system-media-producer.md)                               | Der Name des Herstellers des Inhalts.                                                                                                                                                                      | VT \_ LPWSTR   |
| **Pkey- \_ Media \_ promotionurl**                                            | [System. Media. promotionurl](../properties/props-system-media-promotionurl.md)                       | Die URL einer Website, die eine herauf Stufung im Zusammenhang mit dem Inhalt bietet.                                                                                                                                             | VT \_ LPWSTR   |
| **Pkey \_ Media \_ providerrating**                                          | [System. Media. providerrating](../properties/props-system-media-providerrating.md)                   | Die Bewertung des Inhalts, wie vom metadateninhaltsanbieter zugewiesen.                                                                                                                                       | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ providerstyle**                                           | [System. Media. providerstyle](../properties/props-system-media-providerstyle.md)                     | Der Stil oder das Genre des Inhalts, wie vom metadateninhaltsanbieter zugewiesen.                                                                                                                               | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ Herausgeber**                                               | [System. Media. Publisher](../properties/props-system-media-publisher.md)                             | Gebers.                                                                                                                                                                                                | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ Untertitel**                                                | [System. Media. Untertitel](../properties/props-system-media-subtitle.md)                               | Untertitel.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ UniqueFileIdentifier**                                    | [System. Media. UniqueFileIdentifier](../properties/props-system-media-uniquefileidentifier.md)       | Eine generische Zeichenfolge, die sein kann, um die Datei zu identifizieren.                                                                                                                                                        | VT \_ LPWSTR   |
| **Pkey \_ Media \_ Writer**                                                  | [System. Media. Writer](../properties/props-system-media-writer.md)                                   | Maschine.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **Pkey- \_ Medien \_ Jahr**                                                    | [System. Media. Year](../properties/props-system-media-year.md)                                       | Jahr, an dem der Inhalt veröffentlicht wurde.                                                                                                                                                                           | VT \_ UI4      |
| **Pkey \_ Musik- \_ albumartist**                                             | [System. Music. albumartist](../properties/props-system-music-albumartist.md)                         | Primärer Maler für das Album. Dieses Attribut kann verwendet werden, um den primären Künstler eines Albums von einem Künstler zu unterscheiden, der an einer bestimmten Spur zusammengearbeitet hat.                                            | VT \_ LPWSTR   |
| **Pkey \_ Music- \_ albumtitle**                                              | [System. Music. albumtitle](../properties/props-system-music-albumtitle.md)                           | Titel des Albums.                                                                                                                                                                                              | VT \_ LPWSTR   |
| **Pkey \_ Musik \_ Künstlerin**                                                  | [System. Music. Artist](../properties/props-system-music-artist.md)                                   | Interpret.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **Pkey \_ Music- \_ beatsperminute**                                          | [System. Music. beatsperminute](../properties/props-system-music-beatsperminute.md)                   | Beats pro Minute.                                                                                                                                                                                         | VT \_ LPWSTR   |
| **Pkey \_ Music \_ Composer**                                                | [System. Music. Composer](../properties/props-system-music-composer.md)                               | Ersteller.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **Pkey- \_ Musik \_ Leiter**                                               | [System. Music. Conductor](../properties/props-system-music-conductor.md)                             | Dirigentin.                                                                                                                                                                                                | VT \_ LPWSTR   |
| **Pkey \_ Music \_ contentgroupdescription**                                 | [System. Music. contentgroupdescription](../properties/props-system-music-contentgroupdescription.md) | Beschreibung der Inhalts Gruppe (z. b. ein-oder-Reihe).                                                                                                                                      | VT \_ LPWSTR   |
| **Pkey- \_ Musik \_ Genre**                                                   | [System. Music. Genre](../properties/props-system-music-genre.md)                                     | Richtungen.                                                                                                                                                                                                    | VT \_ LPWSTR   |
| **Pkey- \_ Musik \_ initialkey**                                              | [System.Music.Initialkey](../properties/props-system-music-initialkey.md)                           | Der erste Schlüssel der Musik.                                                                                                                                                                             | VT \_ LPWSTR   |
| **Pkey- \_ Musik- \_ iscompilation**                                           | [System. Music. iscompilation](../properties/props-system-music-iscompilation.md)                     | Gibt an, ob die Musikdatei Teil einer Kompilierung ist.                                                                                                                                                | VT \_ bool     |
| **Pkey- \_ Musik- \_ Texte**                                                  | [System. Music. Lyrics](../properties/props-system-music-lyrics.md)                                   | Texte.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **Pkey \_ Musik \_ Stimmung**                                                    | [System. Music. Mood](../properties/props-system-music-mood.md)                                       | Mood.                                                                                                                                                                                                     | VT \_ LPWSTR   |
| **Pkey- \_ Musik- \_ Teilmenge**                                               | [System. Music. Parser](../properties/props-system-music-partofset.md)                             | Die Teilenummer und die Gesamtanzahl der Teile in der Menge, zu der die Datei gehört, getrennt durch einen Schrägstrich.                                                                                                 | VT \_ LPWSTR   |
| **Pkey- \_ Musik \_ Zeitraum**                                                  | [System. Music. period](../properties/props-system-music-period.md)                                   | Dauer.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **Pkey \_ Musik \_ tracknumber**                                             | [System. Music. tracknumber](../properties/props-system-music-tracknumber.md)                         | Nachverfolgen der Nummer.                                                                                                                                                                                             | VT \_ UI4      |
| **Pkey-Parameter \_ Bewertung**                                                 | [System. Parser-Bewertung](../properties/props-system-parentalrating.md)                               | Eltern Bewertung.                                                                                                                                                                                          | VT \_ LPWSTR   |
| **Pkey- \_ parametrialratingreason**                                           | [System. parametrialratingreason](../properties/props-system-parentalratingreason.md)                   | Gründe für die zugewiesene Eltern Bewertung.                                                                                                                                                                 | VT \_ LPWSTR   |
| **Pkey- \_ Bewertung**                                                         | [System. Rating](../properties/props-system-rating.md)                                               | Benutzer Bewertung.                                                                                                                                                                                              | VT \_ UI4      |
| **Pkey- \_ thumbnailstream**                                                | [System. thumbnailstream](../properties/props-system-thumbnailstream.md)                             | Miniaturbild.                                                                                                                                                                                          | VT- \_ Stream   |
| **Pkey- \_ Titel**                                                          | [System.Title](../properties/props-system-title.md)                                                 | Titel.                                                                                                                                                                                                    | VT \_ LPWSTR   |
| **Pkey- \_ Video \_ Komprimierung**                                             | [System. Video. Compression](../properties/props-system-video-compression.md)                         | Der Video Untertyp ([**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)) wird als Zeichenfolge ausgedrückt.                                                                                                                 | VT \_ LPWSTR   |
| **Pkey- \_ Video \_ Director**                                                | [System. Video. Director](../properties/props-system-video-director.md)                               | Direktors.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **Pkey \_ Video \_ encodingbitrate**                                         | [System. Video. encodingbitrate](../properties/props-system-video-encodingbitrate.md)                 | Die durchschnittliche Video Bitrate in Bits pro Sekunde.                                                                                                                                                               | VT \_ UI4      |
| **Pkey- \_ Video \_ FourCC**                                                  | [System. Video. FourCC](../properties/props-system-video-fourcc.md)                                   | Die **FourCC** des Video Codierungs Formats. Gilt nur, wenn der Video Untertyp als **FourCC** -Wert ausgedrückt werden kann.                                                                                    | VT \_ UI4      |
| **Pkey \_ - \_ videoframeheight**                                             | [System. Video. frameheight](../properties/props-system-video-frameheight.md)                         | Video Rahmenhöhe.                                                                                                                                                                                       | VT \_ UI4      |
| **Pkey- \_ Video \_ Framerate**                                               | [System. Video. Framerate](../properties/props-system-video-framerate.md)                             | Video Frame Rate, ausgedrückt als Frames pro Sekunde × 1000.                                                                                                                                                  | VT \_ UI4      |
| **Pkey- \_ Video \_ framewidth**                                              | [System. Video. framewidth](../properties/props-system-video-framewidth.md)                           | Video Rahmenbreite.                                                                                                                                                                                        | VT \_ UI4      |
| **Pkey- \_ Video \_ horizontalaspectratio**                                   | [System. Video. horizontalaspectratio](../properties/props-system-video-horizontalaspectratio.md)     | Die horizontale Komponente des Pixel Seitenverhältnisses. (Äquivalent zum Zähler des MF-Attribut für das [**\_ Pixel-Pixel- \_ \_ Seiten \_ Verhältnis**](mf-mt-pixel-aspect-ratio-attribute.md) im Medientyp.)          | VT \_ UI4      |
| **Pkey- \_ Video \_ isstereo**                                                | [System. Video. isstereo](/previous-versions//mt744507(v=vs.85))                                     | Gibt an, ob der Videostream Stereo Videoinhalte enthält.                                                                                                                                         | VT \_ bool     |
| **Pkey- \_ Video \_ streamnumber**                                            | [System. Video. streamnumber](../properties/props-system-video-streamnumber.md)                       | Der Bezeichner des Videodaten Stroms.                                                                                                                                                                           | VT \_ UI4      |
| **Pkey- \_ Video- \_ totalbitrate**                                            | [System. Video. totalbitrate](../properties/props-system-video-totalbitrate.md)                       | Die Gesamt Datenmenge für alle Video-und Audiodatenströme (in Bits pro Sekunde). (Gilt nur für Dateien, die mindestens einen Videostream haben.)                                                                              | VT \_ UI4      |
| **Pkey- \_ Video \_ verticalaspectratio**                                     | [System. Video. verticalaspectratio](../properties/props-system-video-verticalaspectratio.md)         | Die vertikale Komponente des Pixel Seitenverhältnisses. (Entspricht dem Nenner des MF- [**\_ MT- \_ Pixel-Pixel- \_ Seiten \_ Verhältnis**](mf-mt-pixel-aspect-ratio-attribute.md) Attributs im Medientyp.)          | VT \_ UI4      |



 

## <a name="media-sharing-properties"></a>Medien Freigabe Eigenschaften

Damit eine Mediendatei mit dem Medien Freigabe Feature kompatibel ist, sollte der Eigenschaften Handler die folgenden Metadateneigenschaften verfügbar machen. Diese Eigenschaften ermöglichen es dem Medien Freigabe Dienst, die richtigen Optionen zum transcodieren des Inhalts in verschiedene Formate oder Bitraten bereitzustellen.

-   [\_ \_ DLNA- \_ Profil- \_ ID für mfpkey-Inhalt](mfpkey-content-dlna-profile-id.md)
-   **Pkey \_ - \_ audiochannelanzahl**
-   **Pkey \_ - \_ audioencodingbitrate**
-   **Pkey \_ - \_ Audioformat**
-   **Pkey \_ \_Audiosamplerate** (optional)
-   **Pkey \_ \_Audiosamplesize** (optional)
-   **Pkey \_ DRM \_ IsProtected** (erforderlich für DRM-Inhalt)
-   **Pkey- \_ Medien \_ Dauer**
-   **Pkey- \_ Video \_ Komprimierung**
-   **Pkey \_ Video \_ encodingbitrate**
-   **Pkey- \_ Video \_ FourCC**
-   **Pkey \_ - \_ videoframeheight**
-   **Pkey \_ Video \_ Framerate** (optional)
-   **Pkey- \_ Video \_ framewidth**
-   **Pkey- \_ Video- \_ totalbitrate**

Die **pkey \_ DRM-Eigenschaft \_ IsProtected** ist erforderlich, wenn der Inhalt mithilfe von DRM geschützt wird. Andernfalls ist diese Eigenschaft optional.

Die Eigenschaften **pkey \_ - \_ Audiosamplerate**, **pkey \_ - \_ audiosamplesize** und **pkey- \_ \_ Videoframerate** sind optional. Der Medien Freigabe Dienst macht Sie verfügbar, wenn Sie verfügbar sind.

Eigenschaften in der **pkey \_ - \_ \* *Gruppe "audio_" gelten nur für Dateien mit einem Audiodatenstrom, und Eigenschaften in der* \_ \_ \* Videogruppe "_ pkey** " gelten nur für Dateien mit einem Videostream.

## <a name="windows-media-format-sdk-mappings"></a>SDK-Zuordnungen im Windows Media-Format

Die ASF-Medienquelle ordnet den ASF-Header Attributen die folgenden Eigenschafts Schlüssel zu. In einigen Fällen unterscheiden sich die Datentypen zwischen der shelleigenschaft und dem Format-SDK-Attribut.



| PROPERTYKEY                              | Format-SDK-Attribut                                                  |
|------------------------------------------|-----------------------------------------------------------------------|
| **Pkey \_ -Audiodatei " \_ isvariablebitrate"**       | [**Isvbr**](../wmformat/isvbr.md)                                           |
| **Pkey \_ - \_ audiodatenwert**               | [**Peer Value**](../wmformat/peakvalue.md)                                   |
| **Pkey- \_ Autor**                         | [**Autor**](../wmformat/author.md)                                         |
| **Pkey- \_ Kommentar**                        | [**Beschreibung**](../wmformat/description.md)                               |
| **Pkey- \_ Copyright**                      | [**Copyright**](../wmformat/copyright.md)                                   |
| **Pkey \_ DRM \_ isprotehiert**               | [**Ist \_ geschützt**](../wmformat/is-protected.md)                            |
| **Pkey- \_ Schlüsselwörter**                       | [**WM/Kategorie**](../wmformat/wm-category.md)                               |
| **Pkey- \_ Sprache**                       | [**WM/Sprache**](../wmformat/wm-language.md)                               |
| **Pkey \_ Media \_ authorurl**               | [**WM/authorurl**](../wmformat/wm-authorurl.md)                             |
| **Pkey- \_ Medien \_ averagelevel**            | [**Averagelevel**](../wmformat/averagelevel.md)                             |
| **Pkey- \_ Medien \_ classprimaryid**          | [**WM/mediaclassprimaryid**](../wmformat/wm-mediaprimaryid.md)              |
| **Pkey- \_ Medien \_ classsecondaryid**        | [**WM/MediaClassSecondaryID**](../wmformat/wm-mediasecondaryid.md)          |
| **Pkey- \_ Medien \_ collectiongroupid**       | [**WM/wmcollectiongroupid**](../wmformat/wm-wmcollectiongroupid.md)         |
| **Pkey \_ Medien \_ CollectionId**            | [**WM/wmcollectionid**](../wmformat/wm-wmcollectionid.md)                   |
| **Pkey \_ Media- \_ Inhalts Verteiler**      | [**WM/contentdistributor**](../wmformat/wm-contentdistributor.md)           |
| **Pkey- \_ Medien \_ contentid**               | [**WM/wmcontentid**](../wmformat/wm-wmcontentid.md)                         |
| **Pkey- \_ Medien \_ datecodiert**             | [**WM/encodingtime**](../wmformat/wm-encodingtime.md)                       |
| **Pkey \_ Media \_ datereleasing**            | [**WM/originalreleasetime**](../wmformat/wm-originalreleasetime.md)         |
| **Pkey- \_ Medien \_ dvdid**                   | [**WM/dvdid**](../wmformat/wm-dvdid.md)                                     |
| **Pkey- \_ Medien \_ encodby**               | [**WM/encodby**](../wmformat/wm-encodedby.md)                             |
| **Pkey- \_ Medien \_ Codierungs Einstellungen**        | [**WM/encodingsettings**](../wmformat/wm-encodingsettings.md)               |
| **Pkey \_ Media- \_ MCDI**                    | [**WM/MCDI**](../wmformat/wm-mcdi.md)                                       |
| **Pkey- \_ Medien \_ MetadataContentProvider** | [**WM/Anbieter**](../wmformat/wm-provider.md)                               |
| **Pkey- \_ Medien \_ Producer**                | [**WM/Producer**](../wmformat/wm-producer.md)                               |
| **Pkey- \_ Media \_ promotionurl**            | [**WM/promotionurl**](../wmformat/wm-promotionurl.md)                       |
| **Pkey \_ Media \_ providerrating**          | [**WM/providerrating**](../wmformat/wm-providerrating.md)                   |
| **Pkey- \_ Medien \_ providerstyle**           | [**WM/providerstyle**](../wmformat/wm-providerstyle.md)                     |
| **Pkey- \_ Medien \_ Herausgeber**               | [**WM/Verleger**](../wmformat/wm-publisher.md)                             |
| **Pkey- \_ Medien \_ Untertitel**                | [**WM/subtitledescription**](../wmformat/wm-subtitledescription.md)         |
| **Pkey- \_ Medien \_ UniqueFileIdentifier**    | [**WM/UniqueFileIdentifier**](../wmformat/wm-uniquefileidentifier.md)       |
| **Pkey \_ Media \_ Writer**                  | [**WM/Writer**](../wmformat/wm-writer.md)                                   |
| **Pkey- \_ Medien \_ Jahr**                    | [**WM/Jahr**](../wmformat/wm-year.md)                                       |
| **Pkey \_ Musik- \_ albumartist**             | [**WM/albumartist**](../wmformat/wm-albumartist.md)                         |
| **Pkey \_ Music- \_ albumtitle**              | [**WM/albumtitle**](../wmformat/wm-albumtitle.md)                           |
| **Pkey \_ Musik \_ Künstlerin**                  | [**Autor**](../wmformat/author.md)                                         |
| **Pkey \_ Music- \_ beatsperminute**          | [**WM/beatsperminütlich**](../wmformat/wm-beatsperminute.md)                   |
| **Pkey \_ Music \_ Composer**                | [**WM/Composer**](../wmformat/wm-composer.md)                               |
| **Pkey- \_ Musik \_ Leiter**               | [**WM/Dirigent**](../wmformat/wm-conductor.md)                             |
| **Pkey \_ Music \_ contentgroupdescription** | [**WM/contentgroupdescription**](../wmformat/wm-contentgroupdescription.md) |
| **Pkey- \_ Musik \_ Genre**                   | [**WM/Genre**](../wmformat/wm-genre.md)                                     |
| **Pkey- \_ Musik \_ initialkey**              | [**WM/initialkey**](../wmformat/wm-initialkey.md)                           |
| **Pkey- \_ Musik- \_ iscompilation**           | **WM/iskompilierung**                                                  |
| **Pkey- \_ Musik- \_ Texte**                  | [**WM/Liedtexte**](../wmformat/wm-lyrics.md)                                   |
| **Pkey \_ Musik \_ Stimmung**                    | [**WM/Stimmung**](../wmformat/wm-mood.md)                                       |
| **Pkey- \_ Musik- \_ Teilmenge**               | [**WM/Element Satz**](../wmformat/wm-partofset.md)                             |
| **Pkey- \_ Musik \_ Zeitraum**                  | [**WM/Zeitraum**](../wmformat/wm-period.md)                                   |
| **Pkey \_ Musik \_ tracknumber**             | [**WM/tracknumber**](../wmformat/wm-tracknumber.md)                         |
| **Pkey-Parameter \_ Bewertung**                 | [**WM/parametrialbewertung**](../wmformat/wm-parentalrating.md)                   |
| **Pkey- \_ parametrialratingreason**           | [**WM/parametrialratingreason**](../wmformat/wm-parentalratingreason.md)       |
| **Pkey- \_ Bewertung**                         | [**WM/shareduserrating**](../wmformat/wm-shareduserrating.md)               |
| **Pkey- \_ thumbnailstream**                | [**WM/Bild**](../wmformat/wmpicture.md)                       |
| **Pkey- \_ Titel**                          | [**Titel**](../wmformat/title.md)                                           |
| **Pkey- \_ Video \_ Director**                | [**WM/Director**](../wmformat/wm-director.md)                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Metadaten](media-metadata.md)
</dt> <dt>

[Shellmetadatenanbieter](shell-metadata-providers.md)
</dt> </dl>

 

 
