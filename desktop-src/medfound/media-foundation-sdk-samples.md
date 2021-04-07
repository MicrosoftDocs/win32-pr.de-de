---
description: In diesem Abschnitt werden Beispielanwendungen beschrieben, die veranschaulichen, wie Media Foundation. Encoding samplesplayback SamplesPlug-InsSource Reader samplesvideo capturesonstige samplesdeprecated oder veraltete, samplesrelated-Themen verwendet werden.
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Media Foundation-SDK-Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f335b5ba744b098efdb7570aa861ad36fc9216cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761418"
---
# <a name="media-foundation-sdk-samples"></a>Media Foundation-SDK-Beispiele

In diesem Abschnitt werden Beispielanwendungen beschrieben, die die Verwendung von Media Foundation veranschaulichen.

-   [Codierungs Beispiele](#encoding-samples)
-   [Wiedergabe Beispiele](#playback-samples)
-   [Plug-ins](#plug-ins)
-   [Beispiele für Quell Leser](#source-reader-samples)
-   [Video Erfassung](#video-capture)
-   [Verschiedene Beispiele](#miscellaneous-samples)
-   [Veraltete oder veraltete Beispiele](#deprecated-or-obsolete-samples)
-   [Zugehörige Themen](#related-topics)

## <a name="encoding-samples"></a>Codierungs Beispiele



| Beispiel                            | BESCHREIBUNG                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [Transcodieren](transcode-sample.md) | Zeigt, wie Sie eine Mediendatei in das Windows Media-Format umcodieren. |



 

## <a name="playback-samples"></a>Wiedergabe Beispiele



| Beispiel                                            | BESCHREIBUNG                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Basicplayback](/previous-versions//bb970475(v=vs.85))          | Gibt Audiodateien und Videodateien mithilfe der [Medien Sitzung](media-session.md)wieder. Dieses Beispiel veranschaulicht das Erstellen von Wiedergabe Topologien, das Steuern der Medien Sitzung und das Empfangen von Sitzungs Ereignissen während der Wiedergabe. |
| [MF Player](/previous-versions//bb970516(v=vs.85))                    | Veranschaulicht einige Wiedergabe Funktionen, die nicht im [basicplayback](/previous-versions//bb970475(v=vs.85)) -Beispiel enthalten sind.                                                                                              |
| [Protectedplayback](protectedplayback-sample.md) | Gibt geschützte Audiodateien und Videodateien wieder. In diesem Beispiel wird gezeigt, wie die PMP-Sitzung (Protected Media Path) und die Verwendung von Content Wegbereiter-Objekten verwendet werden.                                                              |



 

## <a name="plug-ins"></a>Plug-Ins



| Beispiel                                       | Sub-Area                         | BESCHREIBUNG                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [Decoder](decoder-sample.md)                | Media Foundation Transformation (MFT) | Video Decoder.                                                                                         |
| [Evrpresenter](evrpresenter-sample.md)      | Verschiedenes                    | Benutzerdefinierter Presenter für den [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR).                 |
| [MFT \_ Audiodelay](mft-audiodelay-sample.md) | MFT                              | Audioeffekt-Transformation. Zeigt, wie ein einfaches MFT für die Audioverarbeitung geschrieben wird.                           |
| [MFT- \_ Graustufen](mft-grayscale-sample.md)   | MFT                              | Graustufen Videoeffekt. Zeigt, wie ein einfaches MFT für die Videoverarbeitung geschrieben wird.                           |
| [MPEG1Source](mpeg1source-sample.md)        | Medienquelle                     | Analysiert MPEG-1-Datenströme auf Systemebene. Zeigt, wie Sie eine benutzerdefinierte Medienquelle und einen Byte Datenstrom Handler schreiben. |
| [Wavsink](wavsink-sample.md)                | Medien Senke                       | Eine Archivierungs Senke, die WAV-Dateien schreibt. Zeigt, wie eine benutzerdefinierte Medien Senke geschrieben wird.                        |
| [Wavsource](wavsource-sample.md)            | Medienquelle                     | Analysiert WAV-Dateien. Zeigt, wie Sie eine benutzerdefinierte Medienquelle und einen Byte Datenstrom Handler schreiben.                   |



 

## <a name="source-reader-samples"></a>Beispiele für Quell Leser



| Beispiel                                      | BESCHREIBUNG                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [Audioclip](audio-clip-sample.md)         | Verwendet den [Quell Reader](source-reader.md) , um Audiodaten aus einer Mediendatei zu decodieren.      |
| [Videominiatur](videothumbnail-sample.md) | Verwendet den [Quell Reader](source-reader.md) , um einzelne Frames aus einer Videodatei zu erhalten. |



 

## <a name="video-capture"></a>Video Erfassung



| Beispiel                                        | BESCHREIBUNG                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [MFCaptureD3D](mfcaptured3d-sample.md)       | Zeigt, wie Sie eine Vorschau des Videos von einem Video Erfassungsgerät mithilfe von Direct3D zum Rendering des Videos anzeigen. |
| [MF-Datei](mfcapturetofile-sample.md) | Zeigt, wie Videos von einer Videokamera in einer Datei aufgezeichnet werden.                                   |



 

## <a name="miscellaneous-samples"></a>Verschiedene Beispiele



| Beispiel                                         | BESCHREIBUNG                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Asfparser](asfparser-sample.md)              | Zeigt, wie Daten aus einer ASF-Datei (Advanced Systems Format) analysiert werden.                                                                                   |
| [DXVA-HD](dxva-hd-sample.md)                  | Zeigt, wie Microsoft DirectX Video Acceleration High Definition (DXVA-HD) verwendet wird.                                                                      |
| [DXVA2 \_ videoproc](dxva2-videoproc-sample.md) | Verwendet die DirectX-Videobeschleunigung (DXVA) 2,0, um einen Stream von 4:2:2 YUV Video zu erstellen. In diesem Beispiel wird gezeigt, wie die Videoverarbeitungs Funktionen von DXVA verwendet werden. |



 

## <a name="deprecated-or-obsolete-samples"></a>Veraltete oder veraltete Beispiele



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Beispiel</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfplayer2-sample.md">MFPlayer2</a></td>
<td>Veranschaulicht einige erweiterte Wiedergabe Funktionen der <a href="using-mfplay-for-audio-video-playback.md">MF Play</a> -API.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions//bb970336(v=vs.85)">Playbackfx</a></td>
<td>Wendet einen Graustufen Effekt auf Video an. Zeigt, wie MFTs in eine Wiedergabe Topologie eingefügt werden.<br/>
<blockquote>
[!Note]<br />
Dieses Beispiel ist nicht mehr im SDK enthalten.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="playlist-sample.md">Abspielen</a></td>
<td>Gibt eine Sequenz von Audiodateien mithilfe der Sequencer-Quelle wieder.<br/>
<blockquote>
[!Note]<br />
Dieses Beispiel ist nicht mehr im SDK enthalten.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="simplecapture-sample.md">Simplecapture</a></td>
<td>Zeigt, wie Sie mithilfe der mfplay-API ein Video von einem Video Erfassungsgerät in der Vorschau anzeigen.</td>
</tr>
<tr class="odd">
<td><a href="simpleplay-sample.md">Simpleplay</a></td>
<td>Zeigt, wie Sie eine Mediendatei mit der mfplay-API abspielen können.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
