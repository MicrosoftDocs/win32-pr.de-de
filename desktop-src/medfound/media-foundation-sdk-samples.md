---
description: In diesem Abschnitt werden Beispielanwendungen beschrieben, die veranschaulichen, wie Media Foundation.Encoding SamplesPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated or Obsolete SamplesRelated topics
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Media Foundation-SDK-Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5482fabe5e4bfdfe5d451fd8ccb9c0ba0504a5ff
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482716"
---
# <a name="media-foundation-sdk-samples"></a>Media Foundation-SDK-Beispiele

In diesem Abschnitt werden Beispielanwendungen beschrieben, die die Verwendung von Media Foundation veranschaulichen.

-   [Codierungsbeispiele](#encoding-samples)
-   [Wiedergabebeispiele](#playback-samples)
-   [Plug-Ins](#plug-ins)
-   [Quelllesebeispiele](#source-reader-samples)
-   [Videoaufnahme](#video-capture)
-   [Verschiedene Beispiele](#miscellaneous-samples)
-   [Veraltete oder veraltete Beispiele](#deprecated-or-obsolete-samples)
-   [Zugehörige Themen](#related-topics)

## <a name="encoding-samples"></a>Codierungsbeispiele



| Beispiel                            | BESCHREIBUNG                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [Transcode](transcode-sample.md) | Zeigt, wie eine Mediendatei in Windows Medienformat neu codiert wird. |



 

## <a name="playback-samples"></a>Wiedergabebeispiele



| Beispiel                                            | BESCHREIBUNG                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BasicPlayback](/previous-versions//bb970475(v=vs.85))          | Gibt Audio- und Videodateien mithilfe der [Mediensitzung](media-session.md)wieder. In diesem Beispiel wird veranschaulicht, wie Wiedergabetopologien erstellt, die Mediensitzung gesteuert und Sitzungsereignisse während der Wiedergabe empfangen werden. |
| [MFPlayer](/previous-versions//bb970516(v=vs.85))                    | Veranschaulicht einige Wiedergabefunktionen, die nicht im [BasicPlayback-Beispiel](/previous-versions//bb970475(v=vs.85)) enthalten sind.                                                                                              |
| [ProtectedPlayback](protectedplayback-sample.md) | Gibt geschützte Audio- und Videodateien wieder. In diesem Beispiel wird gezeigt, wie die PMP-Sitzung (Protected Media Path) und Content Enabler-Objekte verwendet werden.                                                              |



 

## <a name="plug-ins"></a>Plug-Ins



| Beispiel                                       | Sub-Area                         | BESCHREIBUNG                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [Decoder](decoder-sample.md)                | Media Foundation Transformieren (MFT) | Videodecoder.                                                                                         |
| [EVRPresenter](evrpresenter-sample.md)      | Sonstiges                    | Benutzerdefinierte Präsentation für den [erweiterten Videorenderer](enhanced-video-renderer.md) (ENHANCED VIDEO Renderer, EVR).                 |
| [MFT \_ AudioDelay](mft-audiodelay-sample.md) | MFT                              | Audioeffekttransformation. Zeigt, wie Sie einen grundlegenden MFT für die Audioverarbeitung schreiben.                           |
| [MFT \_ Grayscale](mft-grayscale-sample.md)   | MFT                              | Graustufenvideoeffekt. Zeigt, wie Sie einen grundlegenden MFT für die Videoverarbeitung schreiben.                           |
| [MPEG1Source](mpeg1source-sample.md)        | Medienquelle                     | Analysiert MPEG-1-Systemebenenstreams. Zeigt, wie eine benutzerdefinierte Medienquelle und ein Bytestreamhandler geschrieben werden. |
| [WavSink](wavsink-sample.md)                | Mediensenke                       | Eine Archivsenke, die WAV-Dateien schreibt. Zeigt, wie eine benutzerdefinierte Mediensenke geschrieben wird.                        |
| [WavSource](wavsource-sample.md)            | Medienquelle                     | Analysiert WAV-Dateien. Zeigt, wie eine benutzerdefinierte Medienquelle und ein Bytestreamhandler geschrieben werden.                   |



 

## <a name="source-reader-samples"></a>Quelllesebeispiele



| Beispiel                                      | BESCHREIBUNG                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [Audioclip](audio-clip-sample.md)         | Verwendet den [Quellleser,](source-reader.md) um Audiodaten aus einer Mediendatei zu decodieren.      |
| [VideoThumbnail](videothumbnail-sample.md) | Verwendet den [Quellleser,](source-reader.md) um einzelne Frames aus einer Videodatei abzurufen. |



 

## <a name="video-capture"></a>Videoaufnahme



| Beispiel                                        | BESCHREIBUNG                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [MFCaptureD3D](mfcaptured3d-sample.md)       | Zeigt, wie Sie eine Vorschau des Videos von einem Videoaufnahmegerät anzeigen, indem Sie Direct3D zum Rendern des Videos verwenden. |
| [MFCaptureToFile](mfcapturetofile-sample.md) | Zeigt, wie Videos von einer Videokamera in einer Datei erfasst werden.                                   |



 

## <a name="miscellaneous-samples"></a>Verschiedene Beispiele



| Beispiel                                         | BESCHREIBUNG                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ASFParser](asfparser-sample.md)              | Zeigt, wie Daten aus einer ASF-Datei (Advanced Systems Format) analysiert werden.                                                                                   |
| [DXVA-HD](dxva-hd-sample.md)                  | Zeigt die Verwendung von Microsoft DirectX Video Acceleration High Definition (DXVA-HD).                                                                      |
| [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) | Verwendet DirectX Video Acceleration (DXVA) 2.0, um einen Stream von 4:2:2 YUV-Videos zu erstellen. In diesem Beispiel wird die Verwendung der Videoverarbeitungsfunktionen von DXVA veranschaulicht. |



 

## <a name="deprecated-or-obsolete-samples"></a>Veraltete oder veraltete Beispiele




| Beispiel | BESCHREIBUNG | 
|--------|-------------|
| <a href="mfplayer2-sample.md">MFPlayer2</a> | Veranschaulicht einige erweiterte Wiedergabefunktionen der <a href="using-mfplay-for-audio-video-playback.md">MFPlay-API.</a> | 
| <a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a> | Wendet einen Graustufeneffekt auf Video an. Zeigt, wie MFTs in eine Wiedergabetopologie eingefügt werden.<br /><blockquote>[!Note]<br />Dieses Beispiel ist nicht mehr im SDK enthalten.</blockquote><br /> | 
| <a href="playlist-sample.md">Wiedergabeliste</a> | Gibt eine Sequenz von Audiodateien mithilfe der Sequencerquelle wieder.<br /><blockquote>[!Note]<br />Dieses Beispiel ist nicht mehr im SDK enthalten.</blockquote><br /> | 
| <a href="simplecapture-sample.md">SimpleCapture</a> | Zeigt, wie Sie mithilfe der MFPlay-API eine Vorschau des Videos von einem Videoaufnahmegerät anzeigen. | 
| <a href="simpleplay-sample.md">SimplePlay</a> | Zeigt, wie eine Mediendatei mithilfe der MFPlay-API wiedergegeben wird. | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
