---
description: Die MPEG-4-Datei Quelle analysiert MP4-und 3GPP-Dateien.
ms.assetid: e64c1554-9702-4cc0-98ad-8a33e04ed09d
title: MPEG-4-Datei Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90df56d58df19a53c37436bd631a1cc68dd8114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215032"
---
# <a name="mpeg-4-file-source"></a>MPEG-4-Datei Quelle

Die MPEG-4-Datei Quelle analysiert MP4-und 3GPP-Dateien. Weitere Informationen zum MP4-Dateiformat finden Sie in den folgenden Standarddokumenten:

-   ISO/IEC 14496-12: *Informationstechnologie-Codierung von audiovisuellen Objekten--Teil 12: ISO-Basis Mediendatei Format*
-   ISO/IEC 14496-14: *Informationstechnologie--Codierung von audiovisuellen Objekten--Teil 14: MP4-Datei Format*

> [!Note]  
> (Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)

 

Die MPEG-4-Datei Quelle decodiert die Audiodaten/Videodaten in der Datei nicht.

Dieses Thema enthält folgende Abschnitte:

## <a name="file-extensions-and-mime-types"></a>Dateierweiterungen und MIME-Typen

Die MPEG-4-Datei Quelle ist die Standard Medienquelle für die folgenden Dateinamen Erweiterungen.



| Dateierweiterung | BESCHREIBUNG           |
|----------------|-----------------------|
| 3G2           | 3GPP2                 |
| 3GP           | 3GPP                  |
| 3GP2          | 3GPP2                 |
| 3GPP          | 3GPP                  |
| .m4a           | MPEG-4-Audiodatei          |
| .m4v           | MPEG-4-Video          |
| .mov           | Apple QuickTime Movie |
| .mp4           | MPEG-4-Audiodaten oder-Video |
| MP4V          | MPEG-4-Video          |



 

Es ist auch die Standard Medienquelle für die folgenden MIME-Typen.



| MIME-Typ (MIME type)   | BESCHREIBUNG  |
|-------------|--------------|
| Audiodaten/3GPP  | 3GPP-Audiodaten   |
| Audiodaten/3GPP2 | 3GPP2-Audiodatei  |
| Audiodatei/MP4   | MPEG-4-Audiodatei |
| Video/3GPP  | 3GPP-Video   |
| Video/3GPP2 | 3GPP2-Video  |
| Video/MP4   | MPEG-4-Video |



 

## <a name="media-types"></a>Medientypen

MP4 ist ein erweiterbares Containerformat. Die MP4-Spezifikation definiert keine festgelegte Struktur zum Beschreiben von Medientypen in einem MP4-Container. Stattdessen wird eine Objekthierarchie definiert, mit der benutzerdefinierte Strukturen für jedes Format definiert werden können. Die Formatbeschreibung wird im Feld Beispiel Beschreibung ("STSD") für diesen Stream gespeichert. Das Feld für die Beispiel Beschreibung enthält eine Liste von Beispieleinträgen. Ein 4-Byte-Code, der einem FourCC ähnelt, definiert für jeden Beispiel Eintrag die Format Struktur.

Diese Erweiterbarkeit bedeutet, dass die MPEG-4-Datei Quelle nicht jede mögliche Formatbeschreibung erkennen kann. Stattdessen wird bei der Erstellung von Medientypen für die Streams ein Ansatz mit zwei Stufen benötigt. Jeder Medientyp enthält mindestens die folgenden Attribute.



| Attribut                                                                     | BESCHREIBUNG                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md)                     | Gleich **mfmediatype \_ -Audiodatei** oder **mfmediatype- \_ Video**.     |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)                            | Gibt den Untertyp des Streams an.                                  |
| [\_ \_ \_ Beispiel Beschreibung für MF MT MPEG4 \_](mf-mt-mpeg4-sample-description.md)      | Enthält das komplette Beispiel Beschreibungsfeld als binäres Blob. |
| [\_Beispiel Eintrag für MF MT \_ MPEG4 \_ aktuell \_ \_](mf-mt-mpeg4-current-sample-entry.md) | Gibt den aktuellen Eintrag im Feld für die Beispiel Beschreibung an.     |



 

Die MPEG-4-Datei Quelle erkennt einige Beispiel Eintrags Typen. Für diese Einträge kann die Format Struktur analysiert und ein kompletter Medientyp mit zusätzlichen Attributen erstellt werden, die die Format Details beschreiben. Siehe [Medientyp Attribute](media-type-attributes.md).

Die MPEG-4-Datei Quelle kann die folgenden Beispiel Einträge analysieren.



| Beispielcode für den Eintrag | Haupttyp | Subtype                                                               | BESCHREIBUNG                                         | Notizen                                                                                                                                                                                            |
|-------------------|------------|-----------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALaw            | Audio      | **Alarm im Wave- \_ Format \_**                                                | Codieren von Gesetzen                                        |                                                                                                                                                                                                  |
| Speichern            | Video      | **MF-Format ( \_ mjpg)**                                               | Photo-JPEG-Stream                                   | Das QuickTime-Container-Format unterstützt auch Motion JPEG-Streams mit mjpa-oder mjpb-Einträgen, aber die MPEG-4-Datei Quelle stellt keinen kompletten Medientyp für diese Typen bereit.               |
| 'avc1'            | Video      | **MF-Format \_ H264**                                               | H. 264-Video                                         |                                                                                                                                                                                                  |
| 'mp4a'            | Audio      | **MF Audioformat- \_ AAC**<br/> **MF Audioformat \_ MP3**<br/>   | AAC oder MP3                                          | Der Eintrag "mp4a" kann andere MPEG-Audioformate beschreiben, aber die MPEG-4-Datei Quelle analysiert die Format Struktur nicht.                                                                          |
| MP4V            | Video      | **MF-Format \_ M4S2**<br/> **MF-Format \_ MP4V**<br/> | MPEG-4, Teil 2                                       | **MF-Format \_ M4S2** wird für das einfache Profil MPEG-4 Part 2 verwendet.<br/> **MF-Format \_ MP4V** wird für alle anderen MPEG-4 Part 2-Profile verwendet, einschließlich des erweiterten einfachen Profils.<br/> |
| Stoffes            | Audio      | **MF Audioformat \_ PCM**                                                | 8-Bit-PCM-Audiodaten                                     |                                                                                                                                                                                                  |
| "sowt"            | Audio      | **MF Audioformat \_ PCM**                                                | Little-Endian PCM-Audiodaten (16 Bit)                      |                                                                                                                                                                                                  |
| Ergänzungs            | Audio      | **MF Audioformat \_ PCM**                                                | 16-Bit-Big-Endian PCM-Audiodaten                         | Die MPEG-4-Datei Quelle konvertiert die Audiodaten in das Little-Endian-Format.                                                                                                                          |
| uLaw            | Audio      | **Mulaw im Wave- \_ Format \_**                                               | Codierungs Gesetze                                        |                                                                                                                                                                                                  |
| "VC-1"            | Video      | **MF-Format \_ WVC1**                                               | VC-1-Video                                          |                                                                                                                                                                                                  |
| Gar            | Audio      | **MF Audioformat \_ PCM**                                                | 8-Bit-oder 16-Bit-Big-Endian PCM-Audiodaten                | Die MPEG-4-Datei Quelle konvertiert die Audiodaten in das Little-Endian-Format.                                                                                                                          |
| 0x00000000        | Audio      | **MF Audioformat \_ PCM**                                                | 8-Bit-oder 16-Bit-Big-Endian PCM-Audiodaten                | Die MPEG-4-Datei Quelle konvertiert die Audiodaten in das Little-Endian-Format.                                                                                                                          |
| 0x6d730002        | Audio      | **ADPCM im Wave- \_ Format \_**                                               | Adaptive Differential Pulse Code-Modulation (ADPCM) |                                                                                                                                                                                                  |
| 0x6d730011        | Audio      | **Wave- \_ Format \_ IMA \_ ADPCM**                                          | ADPCM                                               |                                                                                                                                                                                                  |



 

Bei anderen Codes, die nicht in der vorherigen Tabelle angezeigt werden, legt die MPEG-4-Datei Quelle den Untertyp wie folgt fest:

1.  *Untertyp* = MFMPEG4Format- \_ Basis
2.  *Untertyp*. Data1 = Beispielcode für den Eintrag

Bei Codes, die nicht in der Tabelle angezeigt werden, muss ein Decoder das Beispiel Description-Attribut " [MF \_ MT \_ MPEG4 \_ \_ ](mf-mt-mpeg4-sample-description.md) " verwenden, um das Beispiel Beschreibungsfeld zu analysieren.

Eine Liste der Beispielcode und Links zu relevanten Spezifikationen finden Sie auf der Website für die [MP4-Registrierungs](https://mp4ra.org) Stelle.

## <a name="limitations"></a>Einschränkungen

Die MPEG-4-Datei Quelle bietet keine Unterstützung für die folgenden Features von MP4-Dateien:

-   Externe Spuren.
-   Film Fragmente ("muof"-oder "mfra"-Felder). "muof" wird in Windows 8 unterstützt.
-   Streamen von Präsentationen. Die MPEG-4-Datei Quelle ignoriert die Hinweis Spuren im Hintergrund.
-   Suchen nach SMPTE-Zeit Code.
-   Komprimierte Atome ("cmov").

Nur Video-und Audiodatenströme werden unterstützt. Alle Spuren, die andere Streamtypen enthalten, werden automatisch ignoriert. Mediendaten müssen in ' mdat '-Atome abgelegt werden.

Wenn die Ergänzung zum Platt Form Update für Windows Vista installiert ist, ist die MPEG-4-Datei Quelle unter Windows Vista verfügbar. der Zugriff auf Windows Vista ist jedoch nur mithilfe des [Quell Readers](source-reader.md)möglich.

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Windows 8-Updates für MPEG-4-Quelle und-Senke

-   Unterstützung für Lese-und Schreibvorgänge in Windows 8 in MPEG-4-Quelle und-Senke hinzugefügt Dies wird in der Windows 7 MPEG-4-Quelle und-Senke nicht unterstützt.

    MPEG-4-Quelle liest den Drehwinkel für eine aktive Videospur als Summe des Drehwinkels von "mvhd" und von "tkhd".

    Microsoft MPEG-4 Sink schreibt den Drehwinkel in "tkhd", schreibt jedoch eine 0-Grad-Matrix (Identity) in "mvhd". Beachten Sie, dass Microsoft MPEG-4 Sink nur eine einzelne Video Spur unterstützt.

    IPropertyStore liest den Drehwinkel nur für die erste Video Spur als Summe aus dem Drehwinkel von "mvhd" und von "tkhd".

    IPropertyStore schreibt den Drehwinkel nur für die erste Video Spur in "tkhd", nachdem der Drehungs Winkel entsprechend dem Drehwinkel in "mvhd" angepasst wurde, sofern vorhanden.

-   Film Fragmente ("muof") werden in der Windows 8 MPEG-4-Quelle und-Senke unterstützt, aber "mfra" ist nicht.
-   H. 263 wird in der Windows 8 MPEG-4-Quelle unterstützt.

    Die MPEG-4-Quelle ordnet nun zwei FourCC-Zeichen von "H263" und "263" im MPEG-4-Dateiformat dem Medientyp " **mfvideoformat \_ H263**" zu.

-   Weitere FourCC-Unterstützung für MJPEG in Windows 8 MPEG-4-Quelle hinzugefügt.

    Die MPEG-4-Quelle ordnet den Medientyp "dmb1" dem Medientyp von **mfvideoformat \_ mjpg** zu.

-   Unterstützung von Furigana-Metadaten wurde in Windows 8 MPEG-4-Quelle hinzugefügt.

    MPEG-4-Quelle liest Furigana-Metadaten aus "Soal", "Soar", "soaa", "sonm" und "SOCO". IPropertyStore liest die "furignana"-Metadaten über den Satz entsprechender pkeys.

    In der folgenden Tabelle wird die Zuordnung zwischen dem kanonischen Namen der Shell, dem Eigenschafts Schlüssel und der Box/Tag-ID im MPEG-4-Dateiformat angezeigt.

    

    | Feld                                | Eigenschafts Schlüssel                         | Tag/Feld-ID |
    |--------------------------------------|--------------------------------------|------------|
    | System. Music. albumtitlesorbuverride  | Pkey \_ Musik \_ albumtitlesortoverride  | Soal       |
    | System. Music. artistsorbuverride      | Pkey \_ Musik \_ artistsortoverride      | soar       |
    | System. Music. albumartistsorbuverride | Pkey \_ Musik \_ albumartistsortoverride | soaa       |
    | System. titlesorbuverride             | Pkey- \_ titlesortoverride             | sonm       |
    | System. Music. composersorbuverride    | Pkey \_ Music \_ composersortoverride    | SOCO       |

    

     

-   Unterstützung für Stereo-3D-Atom in Windows 8 MPEG-4-Quelle hinzugefügt.

-   Unterstützung für Unterstützung von AC3 und DD + in Windows 8 MPEG-4-Quelle und-Senke.
-   Dateien, die größer als 4 Gigabyte (GB) sind, werden in der Windows 8 MPEG-4-Senke für nicht fragmentäre MP4-Dateien unterstützt.
-   Das Scrubbing wurde in der MPEG-4-Quelle von Windows 8 optimiert.

    Um die Latenz zu verringern, werden Informationen für die beiden nächsten Keyframes für eine bestimmte Suchposition durch [**imfseekinfo:: getnearestkeyframes**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes)verfügbar gemacht. Da der Keyframe keine abhängigen Frames hat, wird der Frame nach dem Decodieren von nur einem Frame dargestellt. Verwenden Sie [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , um diese Schnittstelle über die Medienquelle, die Pipeline oder die Anwendung abzurufen.

    Legen Sie in MPEG-4-Quelle die Rate auf NULL fest. Wenn sich die Pipeline im Bereinigungs-Modus befindet, ist die Rate 0 (null).

-   SPS und PPS können in Beispiel Daten in der MPEG-4-Senke gespeichert werden.

    [MF \_ Das MPEG4SINK \_ spspps \_ Passthrough](mf-mpeg4sink-spspps-passthrough.md) -Attribut für die MPEG-4-Senke ist so definiert, dass SPS-und-PPS mit Eingabe Beispielen (H. 264-Videodaten) gespeichert werden können. Die erzeugten MP4-Clips können von Windows 7 MPEG-4 Source und anderen wiedergegeben werden.

-   SPS und PPS können aus Eingabe Beispielen in MPEG-4-Senke extrahiert werden.

    Wenn SPS und PPS nicht über einen MF-k- [ \_ MPEG- \_ \_ Sequenz \_ Header](mf-mt-mpeg-sequence-header-attribute.md) auf dem Eingabe Medientyp der MPEG-4-Senke festgelegt sind, versucht die MPEG-4-Senke, SPS und PPS aus den Eingabe Beispielen zu extrahieren. MPEG-4 Sink ignoriert alle Eingabe Beispiele, bis die ersten SPS und PPS gefunden werden, da alle Eingabe Beispiele ohne SPS und PPS nicht decodiert werden können.

-   3D-Informationen im AVC-Konfigurationsdaten Satz werden für nicht fragmentäre MP4-Dateien unterstützt.
-   Die Nalu-Länge wird für h. 264-komprimierte Beispiele zur Optimierung der h. 264 VLD DXVA-Decodierung verfügbar gemacht.

    MPEG-4-Quelle legt die [Länge von MF Nalu fest, die für den Ausgabe Medientyp von MF-Format H264 oder MF-Format H264 \_ \_ \_ festgelegt](mf-nalu-length-set.md) ist. **\_** **\_** Sie legt das BLOB von [MF- \_ Nalu- \_ Längen \_ Informationen](mf-nalu-length-information.md) für jedes Ausgabe Beispiel fest, mit einer Länge von 4 Byte Nalu für verschiedene Nalu in einem komprimierten Beispiel.

-   Unterstützung für "MPEG2-ADTs-Audiodatei" in MP4-Quelle

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienquellen und senken](media-sources-and-sinks.md)
</dt> <dt>

[MPEG-4-Unterstützung in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




