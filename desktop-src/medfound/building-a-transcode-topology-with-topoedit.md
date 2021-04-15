---
description: In diesem Thema wird beschrieben, wie eine Transcodierung-Topologie in topoedit erstellt wird.
ms.assetid: 9a7b57f9-f606-4874-9fd3-aa37215f6f20
title: Aufbauen einer transcode-Topologie mit topoedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ef750b4dd54ef05ab7733cc861d7a09dd5d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524648"
---
# <a name="building-a-transcode-topology-with-topoedit"></a>Aufbauen einer transcode-Topologie mit topoedit

In diesem Thema wird beschrieben, wie eine Transcodierung-Topologie in topoedit erstellt wird.

> [!Note]  
> Diese Funktion erfordert Windows 7

 

## <a name="to-build-a-transcoding-topology"></a>So erstellen Sie eine Transcodierungs Topologie

1.  Klicken Sie im Menü **Datei** auf **transcode Rendering**.

2.  Wählen Sie im Dialogfeld **Medienquelle auswählen** die Quelldatei für die Transcodierung aus.
3.  Klicken Sie auf **Öffnen**.
4.  Wählen Sie im Dialogfeld **transcode-Profil auswählen** eines der Codierungs Profile aus der Dropdown Liste aus.
    > [!Note]  
    > Die Profile werden aus dem Datei TranscodeProfiles.xml geladen.

     

5.  Wählen Sie im Dialogfeld **Zieldatei auswählen** den Namen der Ausgabedatei aus.
6.  Topoedit erstellt die transcodieren-Topologie und zeigt die topologieknoten im Hauptanwendungsfenster an.
7.  Klicken Sie **auf der Symbol** Leiste auf die Schaltfläche wiedergeben, um die Medien Sitzung auszuführen. Warten Sie, bis die Codierung beendet ist.

## <a name="transcodeprofilesxml"></a>TranscodeProfiles.xml

Topoedit lädt die Codierungs Profile aus der Datei TranscodeProfiles.xml. Diese Datei befindet sich im Verzeichnis bin des Windows SDK.

Die Datei beginnt mit einem **tedtranscodeprofiles** -Element. Jedes Profil beginnt mit einem **tedtranscodeprofile** -Element. Jedes Profil besteht aus einem Satz von Werten im Format `<VALUE_NAME Value="VALUE"/>` . Die folgenden Werte sind definiert:



| Wert                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AudioAvgBytesPerSecond"></span><span id="audioavgbytespersecond"></span><span id="AUDIOAVGBYTESPERSECOND"></span>**Audioavgbytespersecond**<br/>                                         | Die durchschnittlichen Bytes pro Sekunde für den Audiodatenstrom. Entspricht dem Attribut " [**MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) ".<br/>                                                |
| <span id="AudioBitsPerSample"></span><span id="audiobitspersample"></span><span id="AUDIOBITSPERSAMPLE"></span>**AudioBitsPerSample**<br/>                                                         | Die Anzahl der Bits pro Sample für den Audiodatenstrom. Entspricht dem [**MF \_ MT \_ - \_ audiobits \_ pro \_ Sample-**](mf-mt-audio-bits-per-sample-attribute.md) Attribut.<br/>                                                          |
| <span id="AudioBlockAlignment"></span><span id="audioblockalignment"></span><span id="AUDIOBLOCKALIGNMENT"></span>**Audioblockalignment**<br/>                                                     | Die Block Ausrichtung für den Audiodatenstrom. Entspricht dem [**MF \_ MT \_ - \_ Audioblock- \_ Ausrichtungs**](mf-mt-audio-block-alignment-attribute.md) Attribut.<br/>                                                                     |
| <span id="AudioEncodingProfile"></span><span id="audioencodingprofile"></span><span id="AUDIOENCODINGPROFILE"></span>**Audioencodingprofile**<br/>                                                 | Ein Codec-spezifischer Wert, der das Audioprofil definiert. Entspricht dem [MF- \_ transcode- \_ encodingprofile](mf-transcode-encodingprofile.md) -Attribut. <br/>                                                                     |
| <span id="AudioFormat"></span><span id="audioformat"></span><span id="AUDIOFORMAT"></span>**Audioformat**<br/>                                                                                     | Der codierte audiountertyp. Entspricht dem [**MF \_ MT- \_ SubType**](mf-mt-subtype-attribute.md) -Attribut.<br/>                                                                                                                  |
| <span id="AudioNumChannels"></span><span id="audionumchannels"></span><span id="AUDIONUMCHANNELS"></span>**Audionum Channels**<br/>                                                                 | Die Anzahl der Kanäle im Audiostream. Entspricht dem [**MF-Attribut "MF \_ MT \_ \_ audionum \_ Channels**](mf-mt-audio-num-channels-attribute.md) ".<br/>                                                                         |
| <span id="AudioSamplesPerSecond"></span><span id="audiosamplespersecond"></span><span id="AUDIOSAMPLESPERSECOND"></span>**Audiosamplespersecond**<br/>                                             | Die Samplingrate des Audiodatenstroms (in Stichproben pro Sekunde). Entspricht dem-Attribut " [**MF \_ MT \_ - \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md) ".<br/>                                            |
| <span id="ContainerType"></span><span id="containertype"></span><span id="CONTAINERTYPE"></span>**CONTAINERTYPE**<br/>                                                                             | Der Datei Containertyp. Entspricht dem [MF- \_ transcode- \_ ContainerType](mf-transcode-containertype.md) -Attribut. <br/>                                                                                                       |
| <span id="ProfileName"></span><span id="profilename"></span><span id="PROFILENAME"></span>**Profile Name**<br/>                                                                                     | Der Anzeige Name des Profils.<br/>                                                                                                                                                                                            |
| <span id="SkipMetadataTransfer"></span><span id="skipmetadatatransfer"></span><span id="SKIPMETADATATRANSFER"></span>**SkipMetadataTransfer**<br/>                                                 | Geben Sie 1 an, wenn Metadaten nicht in die Ausgabedatei übertragen werden sollen, oder 0, wenn Metadaten übertragen werden sollen. Entspricht dem [MF- \_ transcode \_ Skip \_ - \_ metadatenübertragungs](mf-transcode-skip-metadata-transfer.md) -Attribut.<br/> |
| <span id="VideoBitrate"></span><span id="videobitrate"></span><span id="VIDEOBITRATE"></span>**Videobitrate**<br/>                                                                                 | Die durchschnittliche Video Bitrate. Entspricht dem [**MF \_ MT \_ AVG- \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) -Attribut. <br/>                                                                                                        |
| <span id="VideoEncodeComplexity"></span><span id="videoencodecomplexity"></span><span id="VIDEOENCODECOMPLEXITY"></span>**Videoencodebug**<br/>                                             | Ein Codec-spezifischer Wert, der die Codierqualität definiert. Entspricht dem [MF- \_ transcode \_ qualityvsspeed](mf-transcode-qualityvsspeed.md) -Attribut. <br/>                                                                      |
| <span id="VideoEncodingProfile"></span><span id="videoencodingprofile"></span><span id="VIDEOENCODINGPROFILE"></span>**Videoencodingprofile**<br/>                                                 | Ein Codec-spezifischer Wert, der das Video Profil definiert. Entspricht dem [MF- \_ transcode- \_ encodingprofile](mf-transcode-encodingprofile.md) -Attribut. <br/>                                                                     |
| <span id="VideoFormat"></span><span id="videoformat"></span><span id="VIDEOFORMAT"></span>**Videoformat**<br/>                                                                                     | Der codierte Video Untertyp. Entspricht dem [**MF \_ MT- \_ SubType**](mf-mt-subtype-attribute.md) -Attribut.<br/>                                                                                                                  |
| <span id="VideoFrameHeight"></span><span id="videoframeheight"></span><span id="VIDEOFRAMEHEIGHT"></span>**Videoframeheight**<br/>                                                                 | Die Höhe des Ausgabevideos. Entspricht dem [**MF \_ MT- \_ Frame \_ Größen**](mf-mt-frame-size-attribute.md) Attribut.<br/>                                                                                                      |
| <span id="VideoFrameRateDenominator"></span><span id="videoframeratedenominator"></span><span id="VIDEOFRAMERATEDENOMINATOR"></span>**Videoframeratenenner**<br/>                             | Der Nenner der Framerate des Ausgabevideos. Entspricht dem [**MF \_ MT- \_ Frame \_ Raten**](mf-mt-frame-rate-attribute.md) Attribut.<br/>                                                                               |
| <span id="VideoFrameRateNumerator"></span><span id="videoframeratenumerator"></span><span id="VIDEOFRAMERATENUMERATOR"></span>**Videoframeratenumschlag**<br/>                                     | Der Zähler der Framerate des Ausgabevideos. Entspricht dem [**MF \_ MT- \_ Frame \_ Raten**](mf-mt-frame-rate-attribute.md) Attribut.<br/>                                                                                 |
| <span id="VideoFrameWidth"></span><span id="videoframewidth"></span><span id="VIDEOFRAMEWIDTH"></span>**Videoframewidth**<br/>                                                                     | Die Breite des Ausgabevideos. Entspricht dem [**MF \_ MT- \_ Frame \_ Größen**](mf-mt-frame-size-attribute.md) Attribut.<br/>                                                                                                       |
| <span id="VideoPixelAspectRatioDenominator"></span><span id="videopixelaspectratiodenominator"></span><span id="VIDEOPIXELASPECTRATIODENOMINATOR"></span>**Videopixelaspectrationenner**<br/> | Der Nenner des Pixel Seitenverhältnisses (par) des Ausgabevideos. Entspricht dem Attribut " [**MF \_ MT Pixel Page \_ \_ \_ Ratio**](mf-mt-pixel-aspect-ratio-attribute.md) ". <br/>                                               |
| <span id="VideoPixelAspectRatioNumerator"></span><span id="videopixelaspectrationumerator"></span><span id="VIDEOPIXELASPECTRATIONUMERATOR"></span>**Videopixelaspectrationumschlag**<br/>         | Der Zähler des Werts des Ausgabevideos. Entspricht dem Attribut " [**MF \_ MT Pixel Page \_ \_ \_ Ratio**](mf-mt-pixel-aspect-ratio-attribute.md) ". <br/>                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Topoedit](topoedit.md)
</dt> </dl>

 

 




