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
# <a name="media-foundation-sdk-samples"></a><span data-ttu-id="c6edb-103">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6edb-103">Media Foundation SDK Samples</span></span>

<span data-ttu-id="c6edb-104">In diesem Abschnitt werden Beispielanwendungen beschrieben, die die Verwendung von Media Foundation veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="c6edb-104">This section describes sample applications that demonstrate how to use Media Foundation.</span></span>

-   [<span data-ttu-id="c6edb-105">Codierungs Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6edb-105">Encoding Samples</span></span>](#encoding-samples)
-   [<span data-ttu-id="c6edb-106">Wiedergabe Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6edb-106">Playback Samples</span></span>](#playback-samples)
-   [<span data-ttu-id="c6edb-107">Plug-ins</span><span class="sxs-lookup"><span data-stu-id="c6edb-107">Plug-Ins</span></span>](#plug-ins)
-   [<span data-ttu-id="c6edb-108">Beispiele für Quell Leser</span><span class="sxs-lookup"><span data-stu-id="c6edb-108">Source Reader Samples</span></span>](#source-reader-samples)
-   [<span data-ttu-id="c6edb-109">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="c6edb-109">Video Capture</span></span>](#video-capture)
-   [<span data-ttu-id="c6edb-110">Verschiedene Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6edb-110">Miscellaneous Samples</span></span>](#miscellaneous-samples)
-   [<span data-ttu-id="c6edb-111">Veraltete oder veraltete Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6edb-111">Deprecated or Obsolete Samples</span></span>](#deprecated-or-obsolete-samples)
-   [<span data-ttu-id="c6edb-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6edb-112">Related topics</span></span>](#related-topics)

## <a name="encoding-samples"></a><span data-ttu-id="c6edb-113">Codierungs Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6edb-113">Encoding Samples</span></span>



| <span data-ttu-id="c6edb-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c6edb-114">Sample</span></span>                            | <span data-ttu-id="c6edb-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6edb-115">Description</span></span>                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="c6edb-116">Transcodieren</span><span class="sxs-lookup"><span data-stu-id="c6edb-116">Transcode</span></span>](transcode-sample.md) | <span data-ttu-id="c6edb-117">Zeigt, wie Sie eine Mediendatei in das Windows Media-Format umcodieren.</span><span class="sxs-lookup"><span data-stu-id="c6edb-117">Shows how to reencode a media file to Windows Media format.</span></span> |



 

## <a name="playback-samples"></a><span data-ttu-id="c6edb-118">Wiedergabe Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6edb-118">Playback Samples</span></span>



| <span data-ttu-id="c6edb-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c6edb-119">Sample</span></span>                                            | <span data-ttu-id="c6edb-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6edb-120">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6edb-121">[Basicplayback](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6edb-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span></span>          | <span data-ttu-id="c6edb-122">Gibt Audiodateien und Videodateien mithilfe der [Medien Sitzung](media-session.md)wieder.</span><span class="sxs-lookup"><span data-stu-id="c6edb-122">Plays audio and video files by using the [Media Session](media-session.md).</span></span> <span data-ttu-id="c6edb-123">Dieses Beispiel veranschaulicht das Erstellen von Wiedergabe Topologien, das Steuern der Medien Sitzung und das Empfangen von Sitzungs Ereignissen während der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="c6edb-123">This sample demonstrates how to create playback topologies, control the Media Session, and receive session events during playback.</span></span> |
| <span data-ttu-id="c6edb-124">[MF Player](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6edb-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span></span>                    | <span data-ttu-id="c6edb-125">Veranschaulicht einige Wiedergabe Funktionen, die nicht im [basicplayback](/previous-versions//bb970475(v=vs.85)) -Beispiel enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c6edb-125">Demonstrates some playback functions that are not included in the [BasicPlayback](/previous-versions//bb970475(v=vs.85)) sample.</span></span>                                                                                              |
| [<span data-ttu-id="c6edb-126">Protectedplayback</span><span class="sxs-lookup"><span data-stu-id="c6edb-126">ProtectedPlayback</span></span>](protectedplayback-sample.md) | <span data-ttu-id="c6edb-127">Gibt geschützte Audiodateien und Videodateien wieder.</span><span class="sxs-lookup"><span data-stu-id="c6edb-127">Plays protected audio and video files.</span></span> <span data-ttu-id="c6edb-128">In diesem Beispiel wird gezeigt, wie die PMP-Sitzung (Protected Media Path) und die Verwendung von Content Wegbereiter-Objekten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6edb-128">This sample shows how to use the protected media path (PMP) session and how to use content enabler objects.</span></span>                                                              |



 

## <a name="plug-ins"></a><span data-ttu-id="c6edb-129">Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="c6edb-129">Plug-Ins</span></span>



| <span data-ttu-id="c6edb-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c6edb-130">Sample</span></span>                                       | <span data-ttu-id="c6edb-131">Sub-Area</span><span class="sxs-lookup"><span data-stu-id="c6edb-131">Sub-Area</span></span>                         | <span data-ttu-id="c6edb-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6edb-132">Description</span></span>                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6edb-133">Decoder</span><span class="sxs-lookup"><span data-stu-id="c6edb-133">Decoder</span></span>](decoder-sample.md)                | <span data-ttu-id="c6edb-134">Media Foundation Transformation (MFT)</span><span class="sxs-lookup"><span data-stu-id="c6edb-134">Media Foundation transform (MFT)</span></span> | <span data-ttu-id="c6edb-135">Video Decoder.</span><span class="sxs-lookup"><span data-stu-id="c6edb-135">Video decoder.</span></span>                                                                                         |
| [<span data-ttu-id="c6edb-136">Evrpresenter</span><span class="sxs-lookup"><span data-stu-id="c6edb-136">EVRPresenter</span></span>](evrpresenter-sample.md)      | <span data-ttu-id="c6edb-137">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="c6edb-137">Miscellaneous</span></span>                    | <span data-ttu-id="c6edb-138">Benutzerdefinierter Presenter für den [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="c6edb-138">Custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span>                 |
| [<span data-ttu-id="c6edb-139">MFT \_ Audiodelay</span><span class="sxs-lookup"><span data-stu-id="c6edb-139">MFT\_AudioDelay</span></span>](mft-audiodelay-sample.md) | <span data-ttu-id="c6edb-140">MFT</span><span class="sxs-lookup"><span data-stu-id="c6edb-140">MFT</span></span>                              | <span data-ttu-id="c6edb-141">Audioeffekt-Transformation.</span><span class="sxs-lookup"><span data-stu-id="c6edb-141">Audio effect transform.</span></span> <span data-ttu-id="c6edb-142">Zeigt, wie ein einfaches MFT für die Audioverarbeitung geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c6edb-142">Shows how to write a basic MFT for audio processing.</span></span>                           |
| [<span data-ttu-id="c6edb-143">MFT- \_ Graustufen</span><span class="sxs-lookup"><span data-stu-id="c6edb-143">MFT\_Grayscale</span></span>](mft-grayscale-sample.md)   | <span data-ttu-id="c6edb-144">MFT</span><span class="sxs-lookup"><span data-stu-id="c6edb-144">MFT</span></span>                              | <span data-ttu-id="c6edb-145">Graustufen Videoeffekt.</span><span class="sxs-lookup"><span data-stu-id="c6edb-145">Grayscale video effect.</span></span> <span data-ttu-id="c6edb-146">Zeigt, wie ein einfaches MFT für die Videoverarbeitung geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c6edb-146">Shows how to write a basic MFT for video processing.</span></span>                           |
| [<span data-ttu-id="c6edb-147">MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="c6edb-147">MPEG1Source</span></span>](mpeg1source-sample.md)        | <span data-ttu-id="c6edb-148">Medienquelle</span><span class="sxs-lookup"><span data-stu-id="c6edb-148">Media source</span></span>                     | <span data-ttu-id="c6edb-149">Analysiert MPEG-1-Datenströme auf Systemebene.</span><span class="sxs-lookup"><span data-stu-id="c6edb-149">Parses MPEG-1 systems-layer streams.</span></span> <span data-ttu-id="c6edb-150">Zeigt, wie Sie eine benutzerdefinierte Medienquelle und einen Byte Datenstrom Handler schreiben.</span><span class="sxs-lookup"><span data-stu-id="c6edb-150">Shows how to write a custom media source and byte-stream handler.</span></span> |
| [<span data-ttu-id="c6edb-151">Wavsink</span><span class="sxs-lookup"><span data-stu-id="c6edb-151">WavSink</span></span>](wavsink-sample.md)                | <span data-ttu-id="c6edb-152">Medien Senke</span><span class="sxs-lookup"><span data-stu-id="c6edb-152">Media sink</span></span>                       | <span data-ttu-id="c6edb-153">Eine Archivierungs Senke, die WAV-Dateien schreibt.</span><span class="sxs-lookup"><span data-stu-id="c6edb-153">An archive sink that writes .wav files.</span></span> <span data-ttu-id="c6edb-154">Zeigt, wie eine benutzerdefinierte Medien Senke geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c6edb-154">Shows how to write a custom media sink.</span></span>                        |
| [<span data-ttu-id="c6edb-155">Wavsource</span><span class="sxs-lookup"><span data-stu-id="c6edb-155">WavSource</span></span>](wavsource-sample.md)            | <span data-ttu-id="c6edb-156">Medienquelle</span><span class="sxs-lookup"><span data-stu-id="c6edb-156">Media source</span></span>                     | <span data-ttu-id="c6edb-157">Analysiert WAV-Dateien.</span><span class="sxs-lookup"><span data-stu-id="c6edb-157">Parses .wav files.</span></span> <span data-ttu-id="c6edb-158">Zeigt, wie Sie eine benutzerdefinierte Medienquelle und einen Byte Datenstrom Handler schreiben.</span><span class="sxs-lookup"><span data-stu-id="c6edb-158">Shows how to write a custom media source and byte-stream handler.</span></span>                   |



 

## <a name="source-reader-samples"></a><span data-ttu-id="c6edb-159">Beispiele für Quell Leser</span><span class="sxs-lookup"><span data-stu-id="c6edb-159">Source Reader Samples</span></span>



| <span data-ttu-id="c6edb-160">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c6edb-160">Sample</span></span>                                      | <span data-ttu-id="c6edb-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6edb-161">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6edb-162">Audioclip</span><span class="sxs-lookup"><span data-stu-id="c6edb-162">Audio Clip</span></span>](audio-clip-sample.md)         | <span data-ttu-id="c6edb-163">Verwendet den [Quell Reader](source-reader.md) , um Audiodaten aus einer Mediendatei zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="c6edb-163">Uses the [Source Reader](source-reader.md) to decode audio from a media file.</span></span>      |
| [<span data-ttu-id="c6edb-164">Videominiatur</span><span class="sxs-lookup"><span data-stu-id="c6edb-164">VideoThumbnail</span></span>](videothumbnail-sample.md) | <span data-ttu-id="c6edb-165">Verwendet den [Quell Reader](source-reader.md) , um einzelne Frames aus einer Videodatei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c6edb-165">Uses the [Source Reader](source-reader.md) to get single frames from a video file.</span></span> |



 

## <a name="video-capture"></a><span data-ttu-id="c6edb-166">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="c6edb-166">Video Capture</span></span>



| <span data-ttu-id="c6edb-167">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c6edb-167">Sample</span></span>                                        | <span data-ttu-id="c6edb-168">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6edb-168">Description</span></span>                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6edb-169">MFCaptureD3D</span><span class="sxs-lookup"><span data-stu-id="c6edb-169">MFCaptureD3D</span></span>](mfcaptured3d-sample.md)       | <span data-ttu-id="c6edb-170">Zeigt, wie Sie eine Vorschau des Videos von einem Video Erfassungsgerät mithilfe von Direct3D zum Rendering des Videos anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c6edb-170">Shows how to preview video from a video capture device, using Direct3D to render the video.</span></span> |
| [<span data-ttu-id="c6edb-171">MF-Datei</span><span class="sxs-lookup"><span data-stu-id="c6edb-171">MFCaptureToFile</span></span>](mfcapturetofile-sample.md) | <span data-ttu-id="c6edb-172">Zeigt, wie Videos von einer Videokamera in einer Datei aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="c6edb-172">Shows how to capture video from a video camera to a file.</span></span>                                   |



 

## <a name="miscellaneous-samples"></a><span data-ttu-id="c6edb-173">Verschiedene Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6edb-173">Miscellaneous Samples</span></span>



| <span data-ttu-id="c6edb-174">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c6edb-174">Sample</span></span>                                         | <span data-ttu-id="c6edb-175">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6edb-175">Description</span></span>                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6edb-176">Asfparser</span><span class="sxs-lookup"><span data-stu-id="c6edb-176">ASFParser</span></span>](asfparser-sample.md)              | <span data-ttu-id="c6edb-177">Zeigt, wie Daten aus einer ASF-Datei (Advanced Systems Format) analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="c6edb-177">Shows how to parse data from an Advanced Systems Format (ASF) file.</span></span>                                                                                   |
| [<span data-ttu-id="c6edb-178">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="c6edb-178">DXVA-HD</span></span>](dxva-hd-sample.md)                  | <span data-ttu-id="c6edb-179">Zeigt, wie Microsoft DirectX Video Acceleration High Definition (DXVA-HD) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6edb-179">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>                                                                      |
| [<span data-ttu-id="c6edb-180">DXVA2 \_ videoproc</span><span class="sxs-lookup"><span data-stu-id="c6edb-180">DXVA2\_VideoProc</span></span>](dxva2-videoproc-sample.md) | <span data-ttu-id="c6edb-181">Verwendet die DirectX-Videobeschleunigung (DXVA) 2,0, um einen Stream von 4:2:2 YUV Video zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6edb-181">Uses DirectX Video Acceleration (DXVA) 2.0 to create a stream of 4:2:2 YUV video.</span></span> <span data-ttu-id="c6edb-182">In diesem Beispiel wird gezeigt, wie die Videoverarbeitungs Funktionen von DXVA verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6edb-182">This sample shows how to use the video processing features of DXVA.</span></span> |



 

## <a name="deprecated-or-obsolete-samples"></a><span data-ttu-id="c6edb-183">Veraltete oder veraltete Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6edb-183">Deprecated or Obsolete Samples</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c6edb-184">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c6edb-184">Sample</span></span></th>
<th><span data-ttu-id="c6edb-185">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6edb-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6edb-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span><span class="sxs-lookup"><span data-stu-id="c6edb-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span></span></td>
<td><span data-ttu-id="c6edb-187">Veranschaulicht einige erweiterte Wiedergabe Funktionen der <a href="using-mfplay-for-audio-video-playback.md">MF Play</a> -API.</span><span class="sxs-lookup"><span data-stu-id="c6edb-187">Demonstrates some advanced playback features of the <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> API.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6edb-188"><a href="/previous-versions//bb970336(v=vs.85)">Playbackfx</a></span><span class="sxs-lookup"><span data-stu-id="c6edb-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span></span></td>
<td><span data-ttu-id="c6edb-189">Wendet einen Graustufen Effekt auf Video an.</span><span class="sxs-lookup"><span data-stu-id="c6edb-189">Applies a grayscale effect to video.</span></span> <span data-ttu-id="c6edb-190">Zeigt, wie MFTs in eine Wiedergabe Topologie eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c6edb-190">Shows how to insert MFTs into a playback topology.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c6edb-191">Dieses Beispiel ist nicht mehr im SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="c6edb-191">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6edb-192"><a href="playlist-sample.md">Abspielen</a></span><span class="sxs-lookup"><span data-stu-id="c6edb-192"><a href="playlist-sample.md">Playlist</a></span></span></td>
<td><span data-ttu-id="c6edb-193">Gibt eine Sequenz von Audiodateien mithilfe der Sequencer-Quelle wieder.</span><span class="sxs-lookup"><span data-stu-id="c6edb-193">Plays a sequence of audio files using the sequencer source.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c6edb-194">Dieses Beispiel ist nicht mehr im SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="c6edb-194">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6edb-195"><a href="simplecapture-sample.md">Simplecapture</a></span><span class="sxs-lookup"><span data-stu-id="c6edb-195"><a href="simplecapture-sample.md">SimpleCapture</a></span></span></td>
<td><span data-ttu-id="c6edb-196">Zeigt, wie Sie mithilfe der mfplay-API ein Video von einem Video Erfassungsgerät in der Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c6edb-196">Shows how to preview video from a video capture device, using the MFPlay API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6edb-197"><a href="simpleplay-sample.md">Simpleplay</a></span><span class="sxs-lookup"><span data-stu-id="c6edb-197"><a href="simpleplay-sample.md">SimplePlay</a></span></span></td>
<td><span data-ttu-id="c6edb-198">Zeigt, wie Sie eine Mediendatei mit der mfplay-API abspielen können.</span><span class="sxs-lookup"><span data-stu-id="c6edb-198">Shows how to play a media file using the MFPlay API.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c6edb-199">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6edb-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6edb-200">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6edb-200">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="c6edb-201">Info über Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6edb-201">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
