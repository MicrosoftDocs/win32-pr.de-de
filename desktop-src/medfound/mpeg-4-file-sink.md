---
description: Mit der MPEG-4-Datei Senke werden MP4-Dateien erstellt.
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: MPEG-4-Datei-Senke
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c27517463bca7dfa88fdbc09d77f7a6512c896d
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "106371796"
---
# <a name="mpeg-4-file-sink"></a>MPEG-4-Datei-Senke

Mit der MPEG-4-Datei Senke werden MP4-Dateien erstellt. Weitere Informationen zum MP4-Dateiformat finden Sie in den folgenden Standarddokumenten:

-   ISO/IEC 14496-12: *Informationstechnologie-Codierung von audiovisuellen Objekten--Teil 12: ISO-Basis Mediendatei Format*
-   ISO/IEC 14496-14: *Informationstechnologie--Codierung von audiovisuellen Objekten--Teil 14: MP4-Datei Format*

> [!Note]  
> (Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)

 

In der MPEG-4-Datei-Senke werden die Codierungs Funktionen nicht eingeschlossen.

Rufen Sie zum Erstellen der MPEG-4-Datei Senke die [**MFCreateMPEG4MediaSink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) -Funktion auf. Die MPEG-4-Datei Senke macht die folgenden Schnittstellen über **QueryInterface** verfügbar:

-   [**IMF-staatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**Imffinalizablemediasink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMF Media Event Generator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**Imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a>Beispiel Feld für die Beschreibung

MP4 ist ein erweiterbares Containerformat. Die MP4-Spezifikation definiert keine festgelegte Struktur zum Beschreiben von Medientypen in einem MP4-Container. Stattdessen wird eine Objekthierarchie definiert, mit der benutzerdefinierte Strukturen für jedes Format definiert werden können. Die Formatbeschreibung wird für jeden Stream im Feld für die Beispiel Beschreibung ("STSD") gespeichert. Das Feld für die Beispiel Beschreibung enthält eine Liste von Beispieleinträgen. Ein 4-Byte-Code, der einem FourCC ähnelt, definiert für jeden Beispiel Eintrag die Format Struktur.

Die MPEG-4-Datei Senke kann das Beispiel Beschreibungsfeld für die folgenden Formate generieren:

-   H. 264/AVC-Video
-   AAC-Audiodatei
-   MP3-Audio

Bei anderen Formaten muss das Feld für die Beispiel Beschreibung im Medientyp für jeden Stream angegeben werden. Um das Feld für die Beispiel Beschreibung anzugeben, legen Sie die folgenden Attribute für den Medientyp fest:



| Attribut                                                                     | BESCHREIBUNG                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ \_ \_ Beispiel Beschreibung für MF MT MPEG4 \_](mf-mt-mpeg4-sample-description.md)      | Enthält das Beispiel Beschreibungsfeld als binäres Blob.                                                                                                         |
| [\_Beispiel Eintrag für MF MT \_ MPEG4 \_ aktuell \_ \_](mf-mt-mpeg4-current-sample-entry.md) | Gibt an, welche der Beispiel Einträge im Feld für die Beispiel Beschreibung derzeit aktiv ist. (Optional.)<br/> Derzeit muss der Wert 0 (null) sein.<br/> |



 

In einigen Fällen ist es nicht möglich, ein Beispiel Beschreibungsfeld zu generieren, bis alle Daten codiert wurden. Beispielsweise werden Informationen wie die durchschnittliche Bitrate möglicherweise nicht im Voraus bekannt sein. In diesem Fall können Sie den Medientyp aktualisieren, indem Sie die [**imfmediatypeer Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) -Schnittstelle in der MPEG-4-Datei-Senke verwenden. Dies muss erfolgen, bevor die Medien Senke fertiggestellt wird.

In der Regel wird der Medientyp von einem upstreamencoder erstellt. Der Encoder kann beim Streaming einen neuen Medientyp durch eine dynamische Formatänderung generieren. Weitere Informationen finden Sie unter [dynamische Format Änderungen](basic-mft-processing-model.md).

## <a name="h264avc-video"></a>H. 264/AVC-Video

Die MPEG-4-Datei-Senke unterstützt die Version des AVC-Streams mit einem elementaren Videostream, wobei Sequence-Parametersatz (SPS) und der Bildparameter Satz (PPS) nalus im Feld für die Beispiel Beschreibung enthalten sind, wie in ISO/IEC 14496 Part 15 section 5,1 definiert. Die File-Senke unterstützt die alternative Methode zum Speichern von SPS/PPS nalus nicht als separaten Legenden Stream für Parametersätze.

Die MPEG-4-Datei Senke kann das Beispiel Beschreibungsfeld generieren, muss jedoch mit den SPS und PPS nalus bereitgestellt werden. Geben Sie diese Informationen im Medientyp an, indem Sie das [**MF \_ MT-MPEG- \_ \_ Sequenz \_ Header**](mf-mt-mpeg-sequence-header-attribute.md) Attribut festlegen. Der Wert des-Attributs ist der H. 264-Sequenz Header. Der Sequence-Header muss aus den SPS-und PPS-nalus bestehen, die entweder durch 3-Byte-oder 4-Byte-Start Codes getrennt sind.

Wenn Sie die Datei Senke konfigurieren, können Sie optional das [**MF MT- \_ \_ MPEG- \_ Sequenz \_ Header**](mf-mt-mpeg-sequence-header-attribute.md) Attribut aus dem ersten Medientyp weglassen. In diesem Fall müssen Sie den Medientyp später aktualisieren, um den Sequence-Header einzuschließen.

Für die MPEG-4-Datei-Senke gelten die folgenden Anforderungen für AVC-Bitstreams:

-   Der Bitstrom muss der Format Spezifikation H. 264 Anhang B entsprechen. Insbesondere muss nalus entweder durch 3-Byte-oder 4-Byte-Start Codes getrennt werden.
-   Medien Beispiele müssen alle Slice-und Daten-nalus enthalten, die einer einzelnen Präsentationszeit entsprechen.
-   Beim Schreiben von B-Frames in eine MP4-Datei müssen Sie sowohl den Präsentationszeit Stempel als auch den Zeitstempel für die Decodierung festlegen. Wenn der Stream einen B-Frame hat und der decodiertimestamp nicht festgelegt ist, wird dem MP4-Writer angezeigt, dass die Frame-Zeit rückwärts geht und den Frame löscht. 

## <a name="aac-audio"></a>AAC Audio

Bei AAC-Audiodaten kann die MPEG-4-Datei-Senke das Beispiel Beschreibungsfeld für die folgenden Untertypen generieren:

-   **MF Audioformat- \_ AAC**
-   **Mediasubtype \_ RAW \_ AAC1**

Weitere Informationen zu diesen unter Stilen finden Sie unter [AAC-Medientypen](aac-media-types.md).

Für den **MF Audioformat- \_ AAC** -Untertyp enthält der Medientyp optional das [**MF MT- \_ \_ Benutzer \_ Daten**](mf-mt-user-data-attribute.md) Attribut. Wenn dieses Attribut vorhanden ist, ist dies der Teil der [**heaacwaveinfo**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) -Struktur, der nach der **WaveFormatEx** -Struktur angezeigt wird (d. h. nach dem **wfx** -Member). Danach folgen die audiospecificconfig ()-Daten gemäß ISO/IEC 14496-3. Wenn das **MF \_ MT- \_ Benutzer \_ Daten** Attribut nicht vorhanden ist, wird davon ausgegangen, dass es sich um ein LC-Profil (AAC Low Komplexität) handelt, und die MPEG-4-Datei Senke generiert eine passende Beispiel Beschreibungs Box.

Für den Untertyp " **mediasubtype \_ RAW \_ AAC1** " muss die Medien Senke das [**MF \_ MT- \_ Benutzer \_ Daten**](mf-mt-user-data-attribute.md) Attribut enthalten, und das-Attribut muss die audiospecificconfig ()-Daten enthalten.

Die MPEG-4-Datei Senke erstellt mithilfe eines "mp4a"-Beispiel Eintrags mit objecttypeindikation = 0x40 die MPEG-4-Variante des Felds "Beschreibung" der AAC-Beispieldatei. MPEG-2-Objekttypen werden nicht verwendet.

## <a name="mp3-audio"></a>MP3-Audiodatei

Für MP3-Audiodaten kann die MPEG-4-Datei-Senke das Beispiel Beschreibungsfeld aus einem standardaudiomedientyp generieren. (Siehe [audiomedientyp](audio-media-types.md).)

Die MPEG-4-Datei Senke erstellt die MPEG-4-Variante des Beispiels Felds "MP3 Sample Description" unter Verwendung eines "mp4a"-Beispiel Eintrags mit objecttypeindikation = 0x6b für MPEG-1-Audiodaten.

## <a name="limitations"></a>Einschränkungen

-   Die maximale Größe der erstellten Datei beträgt 4 GB. In Windows 8 werden Dateien, die größer als 4 gbgb sind, unterstützt.
-   Die MPEG-4-Datei Senke unterstützt keine Bearbeitungs Listen ("Edts" und "Elst"-Felder).

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
-   Dateien, die größer als 4 GB sind, werden in der Windows 8 MPEG-4-Senke für nicht fragmentionales MP4 unterstützt.
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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Medienquellen und senken](media-sources-and-sinks.md)
</dt> <dt>

[Medien senken](media-sinks.md)
</dt> <dt>

[MPEG-4-Unterstützung in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
