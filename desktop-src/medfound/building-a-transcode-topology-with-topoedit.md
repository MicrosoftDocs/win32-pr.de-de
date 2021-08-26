---
description: In diesem Thema wird beschrieben, wie Sie eine Transcodierungstopologie in TopoEdit erstellen.
ms.assetid: 9a7b57f9-f606-4874-9fd3-aa37215f6f20
title: Erstellen einer Transcodierungstopologie mit TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5386af09b04f155295b807523cdb1c5519c946b45228df51d767e9d2a3aabe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959460"
---
# <a name="building-a-transcode-topology-with-topoedit"></a>Erstellen einer Transcodierungstopologie mit TopoEdit

In diesem Thema wird beschrieben, wie Sie eine Transcodierungstopologie in TopoEdit erstellen.

> [!Note]  
> Für dieses Feature ist Windows 7 erforderlich.

 

## <a name="to-build-a-transcoding-topology"></a>So erstellen Sie eine Transcodierungstopologie

1.  Klicken Sie im Menü **Datei** auf **Transcodierung rendern.**

2.  Wählen Sie im Dialogfeld **Medienquelle auswählen** die Quelldatei für die Transcodierung aus.
3.  Klicken Sie auf **Öffnen**.
4.  Wählen Sie im Dialogfeld **Transcodierungsprofil** auswählen eines der Codierungsprofile aus der Dropdownliste aus.
    > [!Note]  
    > Die Profile werden aus der Datei TranscodeProfiles.xml geladen.

     

5.  Wählen Sie im Dialogfeld **Zieldatei** auswählen den Namen der Ausgabedatei aus.
6.  TopoEdit erstellt die Transcodierungstopologie und zeigt die Topologieknoten im Hauptanwendungsfenster an.
7.  Klicken Sie auf der Symbolleiste auf die Schaltfläche **Wiedergeben,** um die Mediensitzung auszuführen. Warten Sie, bis die Codierung abgeschlossen ist.

## <a name="transcodeprofilesxml"></a>TranscodeProfiles.xml

TopoEdit lädt die Codierungsprofile aus der Datei TranscodeProfiles.xml. Diese Datei befindet sich im Verzeichnis Bin des Windows SDK.

Die Datei beginnt mit einem **TedTranscodeProfiles-Element.** Jedes Profil beginnt mit einem **TedTranscodeProfile-Element.** Jedes Profil besteht aus einem Satz von Werten im Format `<VALUE_NAME Value="VALUE"/>` . Die folgenden Werte werden definiert:



| Wert                                                                                                                                                                                                    | Beschreibung                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AudioAvgBytesPerSecond"></span><span id="audioavgbytespersecond"></span><span id="AUDIOAVGBYTESPERSECOND"></span>**AudioAvgBytesPerSecond**<br/>                                         | Die durchschnittlichen Bytes pro Sekunde für den Audiostream. Entspricht dem [**MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND-Attribut.**](mf-mt-audio-avg-bytes-per-second-attribute.md)<br/>                                                |
| <span id="AudioBitsPerSample"></span><span id="audiobitspersample"></span><span id="AUDIOBITSPERSAMPLE"></span>**AudioBitsPerSample**<br/>                                                         | Die Anzahl der Bits pro Beispiel für den Audiostream. Entspricht dem [**MF \_ MT AUDIO \_ \_ BITS PER \_ \_ SAMPLE-Attribut.**](mf-mt-audio-bits-per-sample-attribute.md)<br/>                                                          |
| <span id="AudioBlockAlignment"></span><span id="audioblockalignment"></span><span id="AUDIOBLOCKALIGNMENT"></span>**AudioBlockAlignment**<br/>                                                     | Die Blockausrichtung für den Audiostream. Entspricht dem [**MF MT AUDIO BLOCK \_ \_ \_ \_ ALIGNMENT-Attribut.**](mf-mt-audio-block-alignment-attribute.md)<br/>                                                                     |
| <span id="AudioEncodingProfile"></span><span id="audioencodingprofile"></span><span id="AUDIOENCODINGPROFILE"></span>**AudioEncodingProfile**<br/>                                                 | Ein codecspezifischer Wert, der das Audioprofil definiert. Entspricht dem [MF \_ TRANSCODE \_ ENCODINGPROFILE-Attribut.](mf-transcode-encodingprofile.md) <br/>                                                                     |
| <span id="AudioFormat"></span><span id="audioformat"></span><span id="AUDIOFORMAT"></span>**AudioFormat**<br/>                                                                                     | Der codierte Audiountertyp. Entspricht dem [**MF \_ MT \_ SUBTYPE-Attribut.**](mf-mt-subtype-attribute.md)<br/>                                                                                                                  |
| <span id="AudioNumChannels"></span><span id="audionumchannels"></span><span id="AUDIONUMCHANNELS"></span>**AudioNumChannels**<br/>                                                                 | Die Anzahl der Kanäle im Audiostream. Entspricht dem [**MF MT AUDIO NUM \_ \_ \_ \_ CHANNELS-Attribut.**](mf-mt-audio-num-channels-attribute.md)<br/>                                                                         |
| <span id="AudioSamplesPerSecond"></span><span id="audiosamplespersecond"></span><span id="AUDIOSAMPLESPERSECOND"></span>**AudioSamplesPerSecond**<br/>                                             | Die Abtastrate des Audiodatenstroms in Stichproben pro Sekunde. Entspricht dem [**MF MT AUDIO SAMPLES PER \_ \_ \_ \_ \_ SECOND-Attribut.**](mf-mt-audio-samples-per-second-attribute.md)<br/>                                            |
| <span id="ContainerType"></span><span id="containertype"></span><span id="CONTAINERTYPE"></span>**ContainerType**<br/>                                                                             | Der Dateicontainertyp. Entspricht dem [MF \_ TRANSCODE \_ CONTAINERTYPE-Attribut.](mf-transcode-containertype.md) <br/>                                                                                                       |
| <span id="ProfileName"></span><span id="profilename"></span><span id="PROFILENAME"></span>**Profilename**<br/>                                                                                     | Der Anzeigename des Profils.<br/>                                                                                                                                                                                            |
| <span id="SkipMetadataTransfer"></span><span id="skipmetadatatransfer"></span><span id="SKIPMETADATATRANSFER"></span>**SkipMetadataTransfer**<br/>                                                 | Geben Sie 1 an, wenn Metadaten nicht in die Ausgabedatei übertragen werden sollen, oder 0, wenn Metadaten übertragen werden sollen. Entspricht dem [MF \_ TRANSCODE \_ SKIP METADATA \_ \_ TRANSFER-Attribut.](mf-transcode-skip-metadata-transfer.md)<br/> |
| <span id="VideoBitrate"></span><span id="videobitrate"></span><span id="VIDEOBITRATE"></span>**VideoBitrate**<br/>                                                                                 | Die durchschnittliche Videobitrate. Entspricht dem [**MF \_ MT \_ AVG \_ BITRATE-Attribut.**](mf-mt-avg-bitrate-attribute.md) <br/>                                                                                                        |
| <span id="VideoEncodeComplexity"></span><span id="videoencodecomplexity"></span><span id="VIDEOENCODECOMPLEXITY"></span>**VideoEncodeComplexity**<br/>                                             | Ein codecspezifischer Wert, der die Codierungsqualität definiert. Entspricht dem [MF \_ TRANSCODE \_ QUALITYVSSPEED-Attribut.](mf-transcode-qualityvsspeed.md) <br/>                                                                      |
| <span id="VideoEncodingProfile"></span><span id="videoencodingprofile"></span><span id="VIDEOENCODINGPROFILE"></span>**VideoEncodingProfile**<br/>                                                 | Ein codecspezifischer Wert, der das Videoprofil definiert. Entspricht dem [MF \_ TRANSCODE \_ ENCODINGPROFILE-Attribut.](mf-transcode-encodingprofile.md) <br/>                                                                     |
| <span id="VideoFormat"></span><span id="videoformat"></span><span id="VIDEOFORMAT"></span>**VideoFormat**<br/>                                                                                     | Der codierte Videountertyp. Entspricht dem [**MF \_ MT \_ SUBTYPE-Attribut.**](mf-mt-subtype-attribute.md)<br/>                                                                                                                  |
| <span id="VideoFrameHeight"></span><span id="videoframeheight"></span><span id="VIDEOFRAMEHEIGHT"></span>**VideoFrameHeight**<br/>                                                                 | Die Höhe des Ausgabevideos. Entspricht dem [**MF \_ MT FRAME \_ \_ SIZE-Attribut.**](mf-mt-frame-size-attribute.md)<br/>                                                                                                      |
| <span id="VideoFrameRateDenominator"></span><span id="videoframeratedenominator"></span><span id="VIDEOFRAMERATEDENOMINATOR"></span>**VideoFrameRateDenominator**<br/>                             | Der Nenner der Bildfrequenz des Ausgabevideos. Entspricht dem [**MF \_ MT FRAME \_ \_ RATE-Attribut.**](mf-mt-frame-rate-attribute.md)<br/>                                                                               |
| <span id="VideoFrameRateNumerator"></span><span id="videoframeratenumerator"></span><span id="VIDEOFRAMERATENUMERATOR"></span>**VideoFrameRateNumerator**<br/>                                     | Der Zähler der Bildfrequenz des Ausgabevideos. Entspricht dem [**MF \_ MT FRAME \_ \_ RATE-Attribut.**](mf-mt-frame-rate-attribute.md)<br/>                                                                                 |
| <span id="VideoFrameWidth"></span><span id="videoframewidth"></span><span id="VIDEOFRAMEWIDTH"></span>**VideoFrameWidth**<br/>                                                                     | Die Breite des Ausgabevideos. Entspricht dem [**MF \_ MT FRAME \_ \_ SIZE-Attribut.**](mf-mt-frame-size-attribute.md)<br/>                                                                                                       |
| <span id="VideoPixelAspectRatioDenominator"></span><span id="videopixelaspectratiodenominator"></span><span id="VIDEOPIXELASPECTRATIODENOMINATOR"></span>**VideoPixelAspectRatioDenominator**<br/> | Der Nenner des Pixel-Seitenverhältnisses (PAR) des Ausgabevideos. Entspricht dem [**MF MT PIXEL ASPECT \_ \_ \_ \_ RATIO-Attribut.**](mf-mt-pixel-aspect-ratio-attribute.md) <br/>                                               |
| <span id="VideoPixelAspectRatioNumerator"></span><span id="videopixelaspectrationumerator"></span><span id="VIDEOPIXELASPECTRATIONUMERATOR"></span>**VideoPixelAspectRatioNumerator**<br/>         | Der Zähler des PAR des Ausgabevideos. Entspricht dem [**MF MT PIXEL ASPECT \_ \_ \_ \_ RATIO-Attribut.**](mf-mt-pixel-aspect-ratio-attribute.md) <br/>                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




