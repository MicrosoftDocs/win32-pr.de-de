---
description: Die MPEG-4-Dateisenke erstellt MP4-Dateien.
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: MPEG-4-Dateisenke
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e0175a5c21cc9f7c0186f70b37a5f94f5bf12151e606a2a441b4c75919d7e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102110"
---
# <a name="mpeg-4-file-sink"></a>MPEG-4-Dateisenke

Die MPEG-4-Dateisenke erstellt MP4-Dateien. Weitere Informationen zum MP4-Dateiformat finden Sie in den folgenden Standarddokumenten:

-   ISO/IEC 14496-12: *Information technology -- Coding of audio-visual objects -- Part 12: ISO Base Media File Format (ISO-Basismediendateiformat)*
-   ISO/IEC 14496-14: *Information technology -- Coding of audio-visual objects -- Part 14: MP4 File Format*

> [!Note]  
> (Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)

 

Die MPEG-4-Dateisenke kapselt keine Codierungsfunktionen.

Rufen Sie zum Erstellen der MPEG-4-Dateisenke die [**MFCreateMPEG4MediaSink-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) auf. Die MPEG-4-Dateisenke macht die folgenden Schnittstellen über **QueryInterface verfügbar:**

-   [**DEADClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**VEREERBUNGFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**GEGETService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**VERERBUNGMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**VERERBUNGMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a>Beispielbeschreibungsfeld

MP4 ist ein erweiterbares Containerformat. Die MP4-Spezifikation definiert keine feste Struktur zum Beschreiben von Medientypen in einem MP4-Container. Stattdessen wird eine Objekthierarchie definiert, mit der benutzerdefinierte Strukturen für jedes Format definiert werden können. Die Formatbeschreibung wird im Feld für die Beispielbeschreibung ("stsd") für jeden Stream gespeichert. Das Beispielbeschreibungsfeld enthält eine Liste von Beispieleinträgen. Für jeden Beispieleintrag definiert ein 4-Byte-Code, der einem FOURCC ähnelt, die Formatstruktur.

Die MPEG-4-Dateisenke kann das Beispielbeschreibungsfeld für die folgenden Formate generieren:

-   H.264/AVC-Video
-   AAC-Audio
-   MP3-Audio

Bei anderen Formaten muss das Beispielbeschreibungsfeld im Medientyp für jeden Stream angegeben werden. Um das Beispielbeschreibungsfeld anzugeben, legen Sie die folgenden Attribute für den Medientyp fest:



| attribute                                                                     | Beschreibung                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BESCHREIBUNG DES MF \_ MT \_ \_ MPEG4-BEISPIELS \_](mf-mt-mpeg4-sample-description.md)      | Enthält das Beispielbeschreibungsfeld als binäres Blob.                                                                                                         |
| [MF \_ MT \_ MPEG4 – AKTUELLER \_ \_ \_ BEISPIELEINTRAG](mf-mt-mpeg4-current-sample-entry.md) | Gibt an, welche der Beispieleinträge im Beispielbeschreibungsfeld derzeit aktiv sind. (Optional.)<br/> Derzeit muss der Wert 0 (null) sein.<br/> |



 

In einigen Fällen ist es nicht möglich, ein Beispielbeschreibungsfeld zu generieren, bis alle Daten codiert wurden. Beispielsweise sind Informationen wie die durchschnittliche Bitrate möglicherweise nicht im Voraus bekannt. In diesem Fall können Sie den Medientyp aktualisieren, indem Sie die [**BENUTZEROBERFLÄCHEMediaTypeHandler-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) in der MPEG-4-Dateisenke verwenden. Dies muss vor dem Abschluss der Mediensenke erfolgen.

In der Regel wird der Medientyp von einem Upstreamencoder erstellt. Der Encoder kann während des Streamings einen neuen Medientyp durch eine dynamische Formatänderung generieren. Weitere Informationen finden Sie unter [Dynamische Formatänderungen.](basic-mft-processing-model.md)

## <a name="h264avc-video"></a>H.264/AVC-Video

Die MPEG-4-Dateisenke unterstützt die Version des AVC-Streams, der über einen elementaren Videostream verfügt. Sequenzparametersatz (SPS) und PICTURE Parameter Set (PPS) NALUs sind im Beispielbeschreibungsfeld enthalten, wie in ISO/IEC 14496 Teil 15 Abschnitt 5.1 definiert. Die Dateisenke unterstützt nicht die alternative Methode zum Speichern von SPS/PPS-NALUs als separater elementarer Parametersatzdatenstrom.

Die MPEG-4-Dateisenke kann das Beispielbeschreibungsfeld generieren, muss jedoch mit den SPS- und PPS-NALUs bereitgestellt werden. Geben Sie diese Informationen im Medientyp an, indem Sie das [**MF \_ MT MPEG \_ SEQUENCE \_ \_ HEADER-Attribut**](mf-mt-mpeg-sequence-header-attribute.md) festlegen. Der Wert des Attributs ist der H.264-Sequenzheader. Der Sequenzheader muss aus den SPS- und PPS-NALUs bestehen, die entweder durch 3-Byte- oder 4-Byte-Startcodes getrennt sind.

Optional können Sie beim Konfigurieren der Dateisenke das [**MF \_ MT MPEG \_ SEQUENCE \_ \_ HEADER-Attribut**](mf-mt-mpeg-sequence-header-attribute.md) aus dem anfänglichen Medientyp weglassen. In diesem Fall müssen Sie den Medientyp später aktualisieren, damit er den Sequenzheader enthält.

Für die MPEG-4-Dateisenke gelten die folgenden Anforderungen für AVC-Bitstreams:

-   Der Bitstream muss der Formatspezifikation für H.264 Anhang B entsprechen. Insbesondere müssen NALUs durch 3-Byte- oder 4-Byte-Startcodes getrennt werden.
-   Medienbeispiele müssen alle Slice- und Daten-NALUs enthalten, die einer einzelnen Präsentationszeit entsprechen.
-   Beim Schreiben von B-Frames in eine MP4-Datei müssen Sie sowohl den Präsentationszeitstempel als auch den Decodierungszeitstempel festlegen. Wenn der Stream über einen B-Frame verfügt und der Decodierungszeitstempel nicht festgelegt ist, sieht der MP4-Writer, dass die Framezeit rückwärts geht, und der Frame wird verdrungen. 

## <a name="aac-audio"></a>AAC Audio

Für AAC-Audio kann die MPEG-4-Dateisenke das Beispielbeschreibungsfeld für die folgenden Untertypen generieren:

-   **MFAudioFormat \_ AAC**
-   **MEDIASUBTYPE \_ RAW \_ AAC1**

Weitere Informationen zu diesen Untertypen finden Sie unter [AAC-Medientypen.](aac-media-types.md)

Für den **\_ AAC-Untertyp MFAudioFormat** enthält der Medientyp optional das [**MF \_ MT USER \_ \_ DATA-Attribut.**](mf-mt-user-data-attribute.md) Falls vorhanden, wird mit diesem Attribut der Teil der [**HEAACWAVEINFO-Struktur**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) angegeben, der nach der **WAVEFORMATEX-Struktur** (d. h. nach dem **wfx-Element) angezeigt** wird. Darauf folgen die AudioSpecificConfig()-Daten gemäß ISO/IEC 14496-3. Wenn das **MF \_ MT USER \_ \_ DATA-Attribut** nicht vorhanden ist, wird angenommen, dass der Stream ein LC-Profil (AAC Low Complexity) ist, und die MPEG-4-Dateisenke generiert ein geeignetes Beispielbeschreibungsfeld.

Für den **MEDIASUBTYPE \_ RAW \_ AAC1-Untertyp** muss die Mediensenke das [**MF \_ MT USER \_ \_ DATA-Attribut**](mf-mt-user-data-attribute.md) enthalten, und das Attribut muss die AudioSpecificConfig()-Daten enthalten.

Die MPEG-4-Dateisenke erstellt die MPEG-4-Variante des AAC-Beispielbeschreibungsfelds unter Verwendung eines Mp4a-Beispieleintrags mit objectTypeIndication = 0x40. Es werden keine MPEG-2-Objekttypen verwendet.

## <a name="mp3-audio"></a>MP3-Audio

Für MP3-Audio kann die MPEG-4-Dateisenke das Beispielbeschreibungsfeld aus einem Standard-Audiomedientyp generieren. (Siehe [Audiomedientypen](audio-media-types.md).)

Die MPEG-4-Dateisenke erstellt die MPEG-4-Variante des MP3-Beispielbeschreibungsfelds unter Verwendung eines Mp4a-Beispieleintrags mit objectTypeIndication = 0x6b für MPEG-1-Audio.

## <a name="limitations"></a>Einschränkungen

-   Die maximale Größe der erstellungsdatei beträgt 4 GB. In Windows 8 werden Dateien unterstützt, die größer als 4 GB sind.
-   Die MPEG-4-Dateisenke unterstützt keine Bearbeitungslisten ("edts" und "elst").

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Windows 8 der MPEG-4-Quelle und -Senke

-   Unterstützung für Lese- und Schreibrotation in Windows 8 MPEG-4-Quelle und -Senke hinzugefügt. Dies wird in der Windows 7 MPEG-4-Quelle und -Senke nicht unterstützt.

    Die MPEG-4-Quelle liest den Drehwinkel für eine aktive Videospur als Summe des Drehwinkels von "mvhd" und von "tkhd".

    Die Microsoft MPEG-4-Senke schreibt den Drehwinkel in "tkhd", schreibt jedoch eine 0-Grad-Matrix (Identität) in "mvhd". Beachten Sie, dass die Microsoft MPEG-4-Senke nur eine einzelne Videospur unterstützt.

    IPropertyStore liest den Drehwinkel nur für die erste Videospur als Summe des Drehwinkels von "mvhd" und von "tkhd".

    IPropertyStore schreibt den Drehwinkel nur für die erste Videospur in "tkhd", nachdem der Drehwinkel entsprechend dem Drehwinkel in "mvhd" angepasst wurde, sofern vorhanden.

-   Filmfragmente ("moof") werden in der MPEG-4 Windows 8 quelle und -Senke unterstützt, "mfra" jedoch nicht.
-   H.263 wird in Windows 8 MPEG-4-Quelle unterstützt.

    Die MPEG-4-Quelle ordnet nun zwei Fourccs von "h263" und "s263" im MPEG-4-Dateiformat dem Medientyp **von MFVideoFormat \_ H263 zu.**

-   Weitere Fourcc-Unterstützung für MJPEG in Windows 8 MPEG-4-Quelle hinzugefügt.

    Die MPEG-4-Quelle ordnet foucc von "dmb1" dem Medientyp **von MFVideoFormat \_ MJPG zu.**

-   In der MPEG-4-Quelle Windows 8 Die Metadatenunterstützung von Ragigana wurde hinzugefügt.

    Mpeg-4-Quelle liest Die Metadaten von "soal", "soar", "soaa", "sonm" und "soco". IPropertyStore liest Die Metadaten von Ragignana durch den Satz der entsprechenden PKEYs.

    Die folgende Tabelle zeigt die Zuordnung zwischen dem kanonischen Shellnamen, dem Eigenschaftsschlüssel und der Feld-/Tag-ID im MPEG-4-Dateiformat.

    

    | Feld                                | Eigenschaftsschlüssel                         | Tag-/Feld-ID |
    |--------------------------------------|--------------------------------------|------------|
    | System. Musik. AlbumTitleSortOverride  | PKEY \_ Musik \_ AlbumTitleSortOverride  | soal       |
    | System. Musik. InterpretsortOverride      | PKEY \_ Musik \_ InterpretSortOverride      | Steigen       |
    | System. Musik. AlbumArtistSortOverride | PKEY \_ Musik \_ AlbumArtistSortOverride | soaa       |
    | System.TitleSortOverride             | PKEY \_ TitleSortOverride             | sonm       |
    | System. Musik. ComposerSortOverride    | PKEY \_ Musik \_ ComposerSortOverride    | Soco       |

    

     

-   Unterstützung für Stereo-3D-Atome in Windows 8 MPEG-4-Quelle hinzugefügt.

-   AC3- und DD+-Unterstützung wurde in Windows 8 MPEG-4-Quelle und -Senke hinzugefügt.
-   Dateien, die größer als 4 GB sind, werden in Windows 8 MPEG-4-Senke für nicht fragmentiertes MP4 unterstützt.
-   Die Bereinigung wurde in der MPEG-4-Windows 8 optimiert.

    Um die Latenz zu reduzieren, werden Informationen für die zwei nächstgelegenen Keyframes für eine bestimmte Suchposition über [**DIETTSeekInfo::GetGrammrestKeyFrames verfügbar gemacht.**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes) Da der Keyframe keine abhängigen Frames hat, stellt er den Frame nach der Decodierung nur eines Frames vor. Verwenden Sie ZUM Abrufen dieser Schnittstelle über die Medienquelle, Pipeline oder Anwendung [**DEN BERGetService::GetService.**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)

    Legen Sie die Rate in der MPEG-4-Quelle auf 0 fest. Wenn sich die Pipeline im Bereinigungsmodus befindet, ist die Rate 0 (null).

-   SPS und PPS können in Beispieldaten in der MPEG-4-Senke gespeichert werden.

    [MF \_ Das MPEG4SINK \_ SPSPPS \_ PASSTHROUGH-Attribut](mf-mpeg4sink-spspps-passthrough.md) in der MPEG-4-Senke ist so definiert, dass SPS- und PPS-Dateien zusammen mit Eingabebeispielen (H.264-Videodaten) gespeichert werden können. Die erzeugten MP4-Clips können von Windows 7 MPEG-4-Quelle und anderen abspielt werden.

-   SPS und PPS können aus Eingabebeispielen in der MPEG-4-Senke extrahiert werden.

    Wenn SPS und PPS nicht über [MF \_ MT MPEG SEQUENCE \_ \_ \_ HEADER](mf-mt-mpeg-sequence-header-attribute.md) auf dem Eingabemedientyp der MPEG-4-Senke festgelegt sind, versucht die MPEG-4-Senke, SPS und PPS aus Eingabebeispielen zu extrahieren. Die MPEG-4-Senke ignoriert alle Eingabebeispiele, bis sie den ersten SPS und PPS findet, da alle Eingabebeispiele ohne SPS und PPS nicht decodiert werden können.

-   3D-Informationen im AVC-Konfigurationsdatensatz werden für nicht fragmentiertes MP4 unterstützt.
-   Die NOPTIM-Länge wird für komprimierte H.264-Beispiele verfügbar gemacht, um die H.264 VLD DXVA-Decodierung zu optimieren.

    Mpeg-4-Quelle legt [MF \_ NMEDIUM \_ LENGTH \_ SET](mf-nalu-length-set.md) für den **Ausgabemedientyp von MFVideoFormat \_ H264** oder **MFVideoFormat \_ h264 fest.** Es legt das Blob [von \_ MF-NLECK \_ LENGTH \_ INFORMATION](mf-nalu-length-information.md) für jede Ausgabestichprobe mit einer N WIE-Länge von 4 Byte für verschiedene N WIES-Dateien in einer komprimierten Stichprobe fest.

-   Unterstützung für MPEG2 ADTS-Audio in MP4-Quelle hinzugefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Medienquellen und -senken](media-sources-and-sinks.md)
</dt> <dt>

[Mediensenken](media-sinks.md)
</dt> <dt>

[MPEG-4-Unterstützung in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
