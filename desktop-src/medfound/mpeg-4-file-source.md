---
description: Die MPEG-4-Dateiquelle analysiert MP4- und 3GPP-Dateien.
ms.assetid: e64c1554-9702-4cc0-98ad-8a33e04ed09d
title: MPEG-4-Dateiquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece07ec0f2a2d94b477335e885f11c0d36769bffd11002ba464cec1d9c6ffb21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848050"
---
# <a name="mpeg-4-file-source"></a>MPEG-4-Dateiquelle

Die MPEG-4-Dateiquelle analysiert MP4- und 3GPP-Dateien. Weitere Informationen zum MP4-Dateiformat finden Sie in den folgenden Standarddokumenten:

-   ISO/IEC 14496-12: *Information technology -- Coding of audio-visual objects -- Part 12: ISO Base Media File Format (ISO-Basismediendateiformat)*
-   ISO/IEC 14496-14: *Information technology -- Coding of audio-visual objects -- Part 14: MP4 File Format*

> [!Note]  
> (Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)

 

Die MPEG-4-Dateiquelle decodiert die Audio-/Videodaten in der Datei nicht.

Dieses Thema enthält folgende Abschnitte:

## <a name="file-extensions-and-mime-types"></a>Dateierweiterungen und MIME-Typen

Die MPEG-4-Dateiquelle ist die Standardmedienquelle für die folgenden Dateierweiterungen.



| Dateierweiterung | BESCHREIBUNG           |
|----------------|-----------------------|
| 3G2           | 3GPP2                 |
| 3GP           | 3GPP                  |
| 3GP2          | 3GPP2                 |
| 3GPP          | 3GPP                  |
| .m4a           | MPEG-4-Audio          |
| .m4v           | MPEG-4-Video          |
| .mov           | Apple QuickTime Movie |
| .mp4           | MPEG-4-Audio oder -Video |
| MP4V          | MPEG-4-Video          |



 

Es ist auch die Standardmedienquelle für die folgenden MIME-Typen.



| MIME-Typ (MIME type)   | Beschreibung  |
|-------------|--------------|
| audio/3gpp  | 3GPP-Audio   |
| audio/3gpp2 | 3GPP2-Audio  |
| audio/mp4   | MPEG-4-Audio |
| video/3gpp  | 3GPP-Video   |
| video/3gpp2 | 3GPP2-Video  |
| video/mp4   | MPEG-4-Video |



 

## <a name="media-types"></a>Medientypen

MP4 ist ein erweiterbares Containerformat. Die MP4-Spezifikation definiert keine feste Struktur zum Beschreiben von Medientypen in einem MP4-Container. Stattdessen wird eine Objekthierarchie definiert, mit der benutzerdefinierte Strukturen für jedes Format definiert werden können. Die Formatbeschreibung wird im Feld für die Beispielbeschreibung ("stsd") für diesen Stream gespeichert. Das Beispielbeschreibungsfeld enthält eine Liste von Beispieleinträgen. Für jeden Beispieleintrag definiert ein 4-Byte-Code, der einem FOURCC ähnelt, die Formatstruktur.

Diese Erweiterbarkeit bedeutet, dass die MPEG-4-Dateiquelle nicht jede mögliche Formatbeschreibung erkennen kann. Stattdessen wird beim Erstellen von Medientypen für die Streams ein zweistufiger Ansatz verwendet. Jeder Medientyp enthält mindestens die folgenden Attribute.



| attribute                                                                     | Beschreibung                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|
| [**MF \_ \_ MT-HAUPTTYP \_**](mf-mt-major-type-attribute.md)                     | Entspricht **MFMediaType \_ Audio oder** **MFMediaType \_ Video**.     |
| [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)                            | Gibt den Streamuntertyp an.                                  |
| [BESCHREIBUNG DES MF \_ MT \_ \_ MPEG4-BEISPIELS \_](mf-mt-mpeg4-sample-description.md)      | Enthält das vollständige Beispielbeschreibungsfeld als binäres Blob. |
| [MF \_ MT \_ MPEG4 – AKTUELLER \_ \_ \_ BEISPIELEINTRAG](mf-mt-mpeg4-current-sample-entry.md) | Gibt den aktuellen Eintrag im Beispielbeschreibungsfeld an.     |



 

Die MPEG-4-Dateiquelle erkennt einige Beispieleintragstypen. Für diese Einträge kann die Formatstruktur analysiert und ein vollständiger Medientyp mit zusätzlichen Attributen erstellt werden, die die Formatdetails beschreiben. Weitere Informationen [finden Sie unter Medientypattribute.](media-type-attributes.md)

Die MPEG-4-Dateiquelle kann die folgenden Beispieleinträge analysieren.



| Beispieleintragscode | Haupttyp | Subtype                                                               | Beschreibung                                         | Hinweise                                                                                                                                                                                            |
|-------------------|------------|-----------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "alaw"            | Audio      | **WAVE \_ FORMAT \_ ALAW**                                                | A-Law-Codierung                                        |                                                                                                                                                                                                  |
| "jpeg"            | Video      | **MFVideoFormat \_ MJPG**                                               | Foto-JPEG-Stream                                   | Das QuickTime-Containerformat unterstützt auch JPEG-Bewegungsstreams mit Einträgen vom Typ "mjpa" oder "mjpb", die MPEG-4-Dateiquelle stellt jedoch keinen vollständigen Medientyp für diese Typen zur Verfügung.               |
| 'avc1'            | Video      | **MFVideoFormat \_ H264**                                               | H.264-Video                                         |                                                                                                                                                                                                  |
| 'mp4a'            | Audio      | **MFAudioFormat \_ AAC**<br/> **MFAudioFormat \_ MP3**<br/>   | AAC oder MP3                                          | Der Eintrag "mp4a" kann andere MPEG-Audioformate beschreiben, aber die MPEG-4-Dateiquelle analysiert die Formatstruktur nicht.                                                                          |
| 'mp4v'            | Video      | **MFVideoFormat \_ M4S2**<br/> **MFVideoFormat \_ MP4V**<br/> | MPEG-4 Teil 2                                       | **MFVideoFormat \_ M4S2** wird für MPEG-4 Part 2 Simple Profile verwendet.<br/> **MFVideoFormat \_ MP4V** wird für alle anderen MPEG-4 Part 2-Profile verwendet, einschließlich Erweitertes einfaches Profil.<br/> |
| "raw"            | Audio      | **MFAudioFormat \_ PCM**                                                | 8-Bit-PCM-Audio                                     |                                                                                                                                                                                                  |
| "sowt"            | Audio      | **MFAudioFormat \_ PCM**                                                | 16-Bit-Little-Endian-PCM-Audio                      |                                                                                                                                                                                                  |
| "twos"            | Audio      | **MFAudioFormat \_ PCM**                                                | 16-Bit-Big-Endian-PCM-Audio                         | Die MPEG-4-Dateiquelle konvertiert die Audiodaten in das Little-Endian-Format.                                                                                                                          |
| "ulaw"            | Audio      | **WELLENFORMAT \_ \_ MULAW**                                               | μ-Law-Codierung                                        |                                                                                                                                                                                                  |
| "vc-1"            | Video      | **MFVideoFormat \_ WVC1**                                               | VC-1-Video                                          |                                                                                                                                                                                                  |
| "NONE"            | Audio      | **MFAudioFormat \_ PCM**                                                | 8-Bit- oder 16-Bit-Big-Endian-PCM-Audio                | Die MPEG-4-Dateiquelle konvertiert die Audiodaten in das Little-Endian-Format.                                                                                                                          |
| 0x00000000        | Audio      | **MFAudioFormat \_ PCM**                                                | 8-Bit- oder 16-Bit-Big-Endian-PCM-Audio                | Die MPEG-4-Dateiquelle konvertiert die Audiodaten in das Little-Endian-Format.                                                                                                                          |
| 0x6d730002        | Audio      | **WAVE \_ FORMAT \_ ADPCM**                                               | Adaptive Differential Pulse Code Pulses (ADPCM) |                                                                                                                                                                                                  |
| 0x6d730011        | Audio      | **WELLENFORMAT \_ \_ IMA \_ ADPCM**                                          | Adpcm                                               |                                                                                                                                                                                                  |



 

Für alle anderen Codes, die in der vorherigen Tabelle nicht angezeigt werden, legt die MPEG-4-Dateiquelle den Untertyp wie folgt fest:

1.  *subtype* = MFMPEG4Format \_ Base
2.  *Untertyp*. Data1 = Beispieleintragscode

Für Codes, die nicht in der Tabelle angezeigt werden, muss ein Decoder das [MF \_ MT \_ MPEG4 SAMPLE \_ \_ DESCRIPTION-Attribut](mf-mt-mpeg4-sample-description.md) verwenden, um das Beispielbeschreibungsfeld zu analysieren.

Eine Liste der Beispieleintragscodes und Links zu relevanten Spezifikationen finden Sie auf der Website der [MP4-Registrierungsstelle.](https://mp4ra.org)

## <a name="limitations"></a>Einschränkungen

Die MPEG-4-Dateiquelle unterstützt die folgenden Funktionen von MP4-Dateien nicht:

-   Externe Spuren.
-   Filmfragmente (Felder "moof" oder "mfra"). "moof" wird in Windows 8 unterstützt.
-   Gestreamte Präsentationen. Die MPEG-4-Dateiquelle ignoriert Hinweisspuren im Hintergrund.
-   Suchen nach SMPTE-Zeitcode.
-   Komprimierte Atome ("cmov").

Es werden nur Video- und Audiostreams unterstützt. Alle Spuren, die andere Streamtypen enthalten, werden im Hintergrund ignoriert. Mediendaten müssen in "mdat"-Atomen platziert werden.

Wenn die Plattformupdateergänzung für Windows Vista installiert ist, ist die MPEG-4-Dateiquelle auf Windows Vista verfügbar, aber auf Windows Vista kann nur über den [Quellleser](source-reader.md)zugegriffen werden.

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Windows 8 Updates für QUELLE und Senke von MPEG-4

-   Rotationslese- und Schreibunterstützung in Windows 8 QUELLE und Senke MPEG-4 hinzugefügt. Dies wird in der Quelle und Senke des Windows 7 MPEG-4 nicht unterstützt.

    Mpeg-4-Quelle liest den Drehwinkel für eine aktive Videospur als Summe des Drehwinkels von "mvhd" und von "tkhd".

    Die Microsoft MPEG-4-Senke schreibt den Drehwinkel in "tkhd", schreibt jedoch eine 0-Grad-Matrix (Identität) in "mvhd". Beachten Sie, dass die Microsoft MPEG-4-Senke nur eine einzelne Videospur unterstützt.

    IPropertyStore liest den Drehwinkel nur für die erste Videospur als Summe des Drehwinkels von "mvhd" und von "tkhd".

    IPropertyStore schreibt den Drehwinkel nur für die erste Videospur in "tkhd", nachdem der Drehwinkel entsprechend dem Drehwinkel in "mvhd" angepasst wurde(sofern vorhanden).

-   Filmfragmente ("moof") werden in Windows 8 MPEG-4-Quelle und -Senke unterstützt, "mfra" jedoch nicht.
-   H.263 wird in Windows 8 MPEG-4-Quelle unterstützt.

    Die Quelle MPEG-4 ordnet nun zwei Fourccs von "h263" und "s263" im MPEG-4-Dateiformat dem Medientyp **MFVideoFormat \_ H263** zu.

-   Weitere Fourcc-Unterstützung für MJPEG in Windows 8 MPEG-4-Quelle hinzugefügt.

    MPEG-4 source ordnet foucc von 'dmb1' dem Medientyp von **MFVideoFormat \_ MJPG** zu.

-   In Windows 8 MPEG-4-Quelle hinzugefügte Unterstützung für Diessana-Metadaten.

    Die MPEG-4-Quelle liest die Metadaten von "soal", "soar", "soaa", "sonm" und "soco". IPropertyStore liest Signaturmetadaten über den Satz der entsprechenden PKEYs.

    Die folgende Tabelle zeigt die Zuordnung zwischen dem kanonischen Shellnamen, dem Eigenschaftsschlüssel und der Feld-/Tag-ID im MPEG-4-Dateiformat.

    

    | Feld                                | Eigenschaftenschlüssel                         | Tag-/Feld-ID |
    |--------------------------------------|--------------------------------------|------------|
    | System. Musik. AlbumTitleSortOverride  | PKEY \_ Musik \_ AlbumTitleSortOverride  | soal       |
    | System. Musik. InterpretSortOverride      | PKEY \_ Musik \_ ArtistSortOverride      | Steigen       |
    | System. Musik. AlbumArtistSortOverride | PKEY \_ Musik \_ AlbumArtistSortOverride | soaa       |
    | System.TitleSortOverride             | PKEY \_ TitleSortOverride             | sonm       |
    | System. Musik. ComposerSortOverride    | PKEY \_ Musik \_ ComposerSortOverride    | Soco       |

    

     

-   Unterstützung von Stereo-3D-Atomen in Windows 8 MPEG-4-Quelle hinzugefügt.

-   AC3- und DD+-Unterstützung wurde in Windows 8 MPEG-4-Quelle und -Senke hinzugefügt.
-   Dateien, die größer als 4 Gigabyte (GB) sind, werden in Windows 8 MPEG-4-Senke für nicht fragmentales MP4 unterstützt.
-   Die Bereinigung wurde in Windows 8 MPEG-4-Quelle optimiert.

    Um die Latenz zu reduzieren, werden Informationen für die beiden nächstgelegenen Keyframes für eine bestimmte Suchposition über [**DEN SUCHBEGRIFFINFO::GetRestrestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes)verfügbar gemacht. Da der Keyframe keine abhängigen Frames enthält, wird der Frame nach dem Decodieren nur eines Frames dargestellt. Verwenden Sie [**DIE USEGETService::GetService-Schnittstelle,**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) um diese Schnittstelle über die Medienquelle, Pipeline oder Anwendung abzurufen.

    Legen Sie rate in mpeg-4 source auf 0 (null) fest. Wenn sich die Pipeline im Bereinigungsmodus befindet, ist die Rate 0 (null).

-   SPS und PPS können in Beispieldaten in der MPEG-4-Senke gespeichert werden.

    [MF \_ Das MPEG4SINK \_ SPSPPS \_ PASSTHROUGH-Attribut](mf-mpeg4sink-spspps-passthrough.md) in der MPEG-4-Senke ist so definiert, dass SPS und PPS zusammen mit Eingabebeispielen (H.264-Videodaten) gespeichert werden können. Die erzeugten MP4-Clips können von Windows 7 MPEG-4-Quelle und anderen wiedergegeben werden.

-   SPS und PPS können aus Eingabebeispielen in der MPEG-4-Senke extrahiert werden.

    Wenn SPS und PPS nicht über [MF MT MPEG SEQUENCE \_ \_ \_ \_ HEADER](mf-mt-mpeg-sequence-header-attribute.md) auf dem Eingabemedientyp der MPEG-4-Senke festgelegt werden, versucht die MPEG-4-Senke, SPS und PPS aus Eingabebeispielen zu extrahieren. Die MPEG-4-Senke ignoriert alle Eingabebeispiele, bis sie den ersten SPS und PPS findet, da alle Eingabebeispiele ohne SPS und PPS nicht decodiert werden können.

-   3D-Informationen im AVC-Konfigurationsdatensatz werden für nicht fragmentale MP4-Dateien unterstützt.
-   Die NALU-Länge wird für komprimierte H.264-Stichproben verfügbar gemacht, um die H.264 VLD DXVA-Decodierung zu optimieren.

    MPEG-4 source sets [MF \_ NALU \_ LENGTH \_ SET](mf-nalu-length-set.md) on the output media type of **MFVideoFormat \_ H264** or **MFVideoFormat \_ h264**. Es legt das Blob der [MF \_ NALU \_ LENGTH \_ INFORMATION](mf-nalu-length-information.md) für jedes Ausgabebeispiel mit einer NALU-Länge von vier Byte für verschiedene NALU-Objekte in einem komprimierten Beispiel fest.

-   Unterstützung für MPEG2 ADTS-Audio in MP4-Quelle hinzugefügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienquellen und -senken](media-sources-and-sinks.md)
</dt> <dt>

[MPEG-4-Unterstützung in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




