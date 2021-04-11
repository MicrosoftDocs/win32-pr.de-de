---
description: In diesem Thema wird beschrieben, wie Sie die transcodieren-API verwenden, um eine Mediendatei zu codieren.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Verwenden der transcode-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb97dd61ef75e71a82b522b65b682f861022bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127888"
---
# <a name="using-the-transcode-api"></a><span data-ttu-id="0387b-103">Verwenden der transcode-API</span><span class="sxs-lookup"><span data-stu-id="0387b-103">Using the Transcode API</span></span>

<span data-ttu-id="0387b-104">In diesem Thema wird beschrieben, wie Sie die transcodieren-API verwenden, um eine Mediendatei zu codieren.</span><span class="sxs-lookup"><span data-stu-id="0387b-104">This topic described how to use the transcode API to encode a media file.</span></span>

-   [<span data-ttu-id="0387b-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="0387b-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="0387b-106">Erstellen einer Medienquelle</span><span class="sxs-lookup"><span data-stu-id="0387b-106">Creating a Media Source</span></span>](#creating-a-media-source)
-   [<span data-ttu-id="0387b-107">Erstellen eines transcode-Profils</span><span class="sxs-lookup"><span data-stu-id="0387b-107">Creating a Transcode Profile</span></span>](#creating-a-transcode-profile)
    -   [<span data-ttu-id="0387b-108">Audioattribute</span><span class="sxs-lookup"><span data-stu-id="0387b-108">Audio Attributes</span></span>](#audio-attributes)
    -   [<span data-ttu-id="0387b-109">Video Attribute</span><span class="sxs-lookup"><span data-stu-id="0387b-109">Video Attributes</span></span>](#video-attributes)
    -   [<span data-ttu-id="0387b-110">Container Attribute</span><span class="sxs-lookup"><span data-stu-id="0387b-110">Container Attributes</span></span>](#container-attributes)
-   [<span data-ttu-id="0387b-111">Erstellen einer transcode-Topologie</span><span class="sxs-lookup"><span data-stu-id="0387b-111">Creating a Transcode Topology</span></span>](#creating-a-transcode-topology)
-   [<span data-ttu-id="0387b-112">Ausführen der Codierungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="0387b-112">Running the Encoding Session</span></span>](#running-the-encoding-session)
-   [<span data-ttu-id="0387b-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0387b-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="0387b-114">Übersicht</span><span class="sxs-lookup"><span data-stu-id="0387b-114">Overview</span></span>

<span data-ttu-id="0387b-115">Vor der Verwendung der transcodieren-API muss die Anwendung über die folgenden Informationen verfügen:</span><span class="sxs-lookup"><span data-stu-id="0387b-115">Before using the transcode API, the application must have the following pieces of information:</span></span>

-   <span data-ttu-id="0387b-116">Der Pfad oder die URL zu einer vorhandenen Mediendatei, die erneut codiert wird.</span><span class="sxs-lookup"><span data-stu-id="0387b-116">The path or URL to an existing media file that will be re-encoded.</span></span>
-   <span data-ttu-id="0387b-117">Der Name der Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="0387b-117">The name of the output file.</span></span>
-   <span data-ttu-id="0387b-118">Der Containertyp für die Ausgabedatei, z. b. MP4 oder Advanced Streaming Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="0387b-118">The container type for the output file, such as MP4 or Advanced Streaming Format (ASF).</span></span>
-   <span data-ttu-id="0387b-119">Das Codierungsformat.</span><span class="sxs-lookup"><span data-stu-id="0387b-119">The encoding format.</span></span> <span data-ttu-id="0387b-120">Zu diesen Informationen gehören die Medientypen, die die codierten Audiodaten und Videostreams beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0387b-120">This information includes the media types that describe the encoded audio and video streams.</span></span>

<span data-ttu-id="0387b-121">Um die transcodieren-API zu verwenden, führt eine Anwendung die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="0387b-121">To use the transcode API, an application performs the following steps.</span></span>

1.  <span data-ttu-id="0387b-122">Erstellen Sie eine Medienquelle, um die Quelldatei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="0387b-122">Create a media source to read the source file.</span></span>
2.  <span data-ttu-id="0387b-123">Erstellen Sie ein transcodieren-Profil.</span><span class="sxs-lookup"><span data-stu-id="0387b-123">Create a transcode profile.</span></span> <span data-ttu-id="0387b-124">Fügen Sie Attribute hinzu, die den Audiostream, den Videostream und den Datei Container beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0387b-124">Add attributes that describe the audio stream, video stream, and file container.</span></span>
3.  <span data-ttu-id="0387b-125">Verwenden Sie das transcodieren-Profil, um eine Codierungs Topologie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0387b-125">Use the transcode profile to create an encoding topology.</span></span> <span data-ttu-id="0387b-126">(Weitere Informationen zu Topologien finden Sie unter Informationen [zu Topologien](about-topologies.md).)</span><span class="sxs-lookup"><span data-stu-id="0387b-126">(For more information about topologies, see [About Topologies](about-topologies.md).)</span></span>
4.  <span data-ttu-id="0387b-127">Legen Sie die Topologie für die [Medien Sitzung](media-session.md)fest.</span><span class="sxs-lookup"><span data-stu-id="0387b-127">Set the topology on the [Media Session](media-session.md).</span></span>
5.  <span data-ttu-id="0387b-128">Starten Sie die Medien Sitzung, und warten Sie auf das Ereignis [mesessionend](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="0387b-128">Start the Media Session and wait for the [MESessionEnded](mesessionended.md) event.</span></span>

<span data-ttu-id="0387b-129">Im restlichen Teil dieses Themas werden diese Schritte ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0387b-129">The remainder of this topic describes these steps in more detail.</span></span>

## <a name="creating-a-media-source"></a><span data-ttu-id="0387b-130">Erstellen einer Medienquelle</span><span class="sxs-lookup"><span data-stu-id="0387b-130">Creating a Media Source</span></span>

<span data-ttu-id="0387b-131">Eine Medienquelle ist ein Objekt, das die Quelldatei liest und analysiert.</span><span class="sxs-lookup"><span data-stu-id="0387b-131">A media source is an object that reads and parses the source file.</span></span> <span data-ttu-id="0387b-132">Verwenden Sie zum Erstellen einer Medienquelle den [quellresolver](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="0387b-132">To create a media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="0387b-133">Beispielcode finden Sie im Thema [Verwenden des Quell Resolvers](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="0387b-133">You can find example code in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>

## <a name="creating-a-transcode-profile"></a><span data-ttu-id="0387b-134">Erstellen eines transcode-Profils</span><span class="sxs-lookup"><span data-stu-id="0387b-134">Creating a Transcode Profile</span></span>

<span data-ttu-id="0387b-135">Ein *transcodieren-Profil* beschreibt das Format und die Einstellungen, die zum Codieren der Ausgabedatei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0387b-135">A *transcode profile* describes the format and settings that are used to encode the output file.</span></span> <span data-ttu-id="0387b-136">Das transcodieren-Profil enthält drei Sätze von Attributen:</span><span class="sxs-lookup"><span data-stu-id="0387b-136">The transcode profile contains three sets of attributes:</span></span>

-   <span data-ttu-id="0387b-137">Audioattribute: Beschreibt die Ziel Einstellungen für das Audioformat und den Audioencoder.</span><span class="sxs-lookup"><span data-stu-id="0387b-137">Audio attributes: Describe the target audio format and audio encoder settings.</span></span>
-   <span data-ttu-id="0387b-138">Video Attribute: beschreiben Sie die Ziel Videoformat-und Video Encoder-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="0387b-138">Video attributes: Describe the target video format and video encoder settings.</span></span>
-   <span data-ttu-id="0387b-139">Container Attribute: Hiermit werden der Typ des Datei Containers sowie einige globale Codierungs Einstellungen definiert.</span><span class="sxs-lookup"><span data-stu-id="0387b-139">Container attributes: Define the type of file container, as well as some global encoding settings.</span></span>

<span data-ttu-id="0387b-140">Um ein transcodieren-Profil zu erstellen, rufen Sie die Funktion " [**mfkreatetranscodeprofile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) " auf.</span><span class="sxs-lookup"><span data-stu-id="0387b-140">To create a transcode profile, call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function.</span></span> <span data-ttu-id="0387b-141">Diese Funktion gibt einen Zeiger auf die [**imftranscodeprofile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="0387b-141">This function returns a pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface.</span></span> <span data-ttu-id="0387b-142">Das anfängliche Profil Objekt ist leer. Sie enthält keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="0387b-142">The initial profile object is empty; it contains no attributes.</span></span> <span data-ttu-id="0387b-143">Der nächste Schritt besteht darin, die Attribute hinzuzufügen, die das Profil definieren.</span><span class="sxs-lookup"><span data-stu-id="0387b-143">The next step is to add the attributes that define the profile.</span></span>

### <a name="audio-attributes"></a><span data-ttu-id="0387b-144">Audioattribute</span><span class="sxs-lookup"><span data-stu-id="0387b-144">Audio Attributes</span></span>

<span data-ttu-id="0387b-145">Um dem Audiodatenstrom Attribute hinzuzufügen, müssen Sie [**imftranscodeprofile:: setaudioattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0387b-145">To add attributes for the audio stream, call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span> <span data-ttu-id="0387b-146">Diese Attribute geben an, wie der Audiostream codiert wird.</span><span class="sxs-lookup"><span data-stu-id="0387b-146">These attributes specify how the audio stream is encoded.</span></span> <span data-ttu-id="0387b-147">Wenn die Ausgabedatei keinen Audiostream enthält, lassen Sie diese Attribute aus.</span><span class="sxs-lookup"><span data-stu-id="0387b-147">If the output file will not contain an audio stream, omit these attributes.</span></span>

<span data-ttu-id="0387b-148">Audioattribute werden in zwei Kategorien unterteilt:</span><span class="sxs-lookup"><span data-stu-id="0387b-148">Audio attributes fall into two categories:</span></span>

-   <span data-ttu-id="0387b-149">Attribute, die das Format des codierten Streams angeben</span><span class="sxs-lookup"><span data-stu-id="0387b-149">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="0387b-150">Attribute, die andere Codierungs Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="0387b-150">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="0387b-151">Format Attribute sind einfache Medientyp Attribute, wie im Abschnitt [audiomedientypen](audio-media-types.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0387b-151">Format attributes are simply media-type attributes, as described in the section [Audio Media Types](audio-media-types.md).</span></span> <span data-ttu-id="0387b-152">Der genaue Satz von Format Attributen hängt vom Encoder ab.</span><span class="sxs-lookup"><span data-stu-id="0387b-152">The exact set of format attributes depends on the encoder.</span></span> <span data-ttu-id="0387b-153">(Informationen hierzu finden Sie [unter Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md).) Im folgenden finden Sie eine Liste mit typischen audioformatattributen:</span><span class="sxs-lookup"><span data-stu-id="0387b-153">(See [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).) Here is a list of typical audio format attributes:</span></span>



| <span data-ttu-id="0387b-154">Format-Attribut</span><span class="sxs-lookup"><span data-stu-id="0387b-154">Format Attribute</span></span>                                                                         | <span data-ttu-id="0387b-155">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0387b-155">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="0387b-156">MF- \_ MT- \_ Untertyp</span><span class="sxs-lookup"><span data-stu-id="0387b-156">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="0387b-157">Der Untertyp.</span><span class="sxs-lookup"><span data-stu-id="0387b-157">The subtype.</span></span> <span data-ttu-id="0387b-158">Siehe [audiountertyp-GUIDs](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="0387b-158">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> |
| [<span data-ttu-id="0387b-159">MF \_ \_ -MT- \_ audionum- \_ Kanäle</span><span class="sxs-lookup"><span data-stu-id="0387b-159">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="0387b-160">Die Anzahl der audiochannels.</span><span class="sxs-lookup"><span data-stu-id="0387b-160">The number of audio channels.</span></span>                                    |
| [<span data-ttu-id="0387b-161">MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde</span><span class="sxs-lookup"><span data-stu-id="0387b-161">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="0387b-162">Die Anzahl von Audiobeispielen pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="0387b-162">The number of audio samples per second.</span></span>                          |
| [<span data-ttu-id="0387b-163">MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="0387b-163">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="0387b-164">Die Block Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="0387b-164">The block alignment.</span></span>                                             |
| [<span data-ttu-id="0387b-165">MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde</span><span class="sxs-lookup"><span data-stu-id="0387b-165">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="0387b-166">Die durchschnittliche Anzahl von Bytes pro Sekunde (die codierte Bitrate).</span><span class="sxs-lookup"><span data-stu-id="0387b-166">The average number of bytes per second (the encoded bit rate).</span></span>   |



 

<span data-ttu-id="0387b-167">Die folgenden Codierungs Parameter sind definiert.</span><span class="sxs-lookup"><span data-stu-id="0387b-167">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="0387b-168">Codierungs Parameter</span><span class="sxs-lookup"><span data-stu-id="0387b-168">Encoding Parameter</span></span>                                                             | <span data-ttu-id="0387b-169">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0387b-169">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="0387b-170">MF- \_ transcode- \_ \_ Anfüge- \_ Encoder</span><span class="sxs-lookup"><span data-stu-id="0387b-170">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="0387b-171">Verhindert, dass die transcodieren-API einen Encoder für den Audiodatenstrom einfügt.</span><span class="sxs-lookup"><span data-stu-id="0387b-171">Prevents the transcode API from inserting an encoder for the audio stream.</span></span> |
| [<span data-ttu-id="0387b-172">MF- \_ transcode- \_ Codierungs Profil</span><span class="sxs-lookup"><span data-stu-id="0387b-172">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="0387b-173">Gibt die Konformitäts Vorlage für Geräte an.</span><span class="sxs-lookup"><span data-stu-id="0387b-173">Specifies the device conformance template.</span></span> <span data-ttu-id="0387b-174">(Gilt nur für ASF-Dateien.)</span><span class="sxs-lookup"><span data-stu-id="0387b-174">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="0387b-175">MF- \_ transcode \_ qualityvsspeed</span><span class="sxs-lookup"><span data-stu-id="0387b-175">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="0387b-176">Gibt den Kompromiss zwischen Codierungsqualität und Geschwindigkeit an.</span><span class="sxs-lookup"><span data-stu-id="0387b-176">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="0387b-177">Sie müssen die Format Attribute festlegen.</span><span class="sxs-lookup"><span data-stu-id="0387b-177">You must set the format attributes.</span></span> <span data-ttu-id="0387b-178">Die Codierungs Parameter sind optional.</span><span class="sxs-lookup"><span data-stu-id="0387b-178">The encoding parameters are optional.</span></span>

<span data-ttu-id="0387b-179">Eine Möglichkeit, ein Format zu finden, das mit dem Encoder kompatibel ist, besteht darin, die Funktion [**mftranscodegetaudiooutputavailabletypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0387b-179">One way to find a format that is compatible with the encoder is to call the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="0387b-180">Der gewünschte Encoder wird durch den Untertyp angegeben.</span><span class="sxs-lookup"><span data-stu-id="0387b-180">The desired encoder is specified by subtype.</span></span> <span data-ttu-id="0387b-181">Die-Funktion gibt eine Auflistung von Medientypen für diesen Encoder zurück.</span><span class="sxs-lookup"><span data-stu-id="0387b-181">The function returns a collection of media types for that encoder.</span></span> <span data-ttu-id="0387b-182">Sie können einen Typ aus der Liste auswählen und die Attribute in das Profil kopieren.</span><span class="sxs-lookup"><span data-stu-id="0387b-182">You can select a type from the list and copy the attributes to the profile.</span></span> <span data-ttu-id="0387b-183">Beispielsweise Code, in dem dieser Ansatz verwendet wird, finden Sie unter [Tutorial: Codieren einer WMA-Datei](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span><span class="sxs-lookup"><span data-stu-id="0387b-183">For example code that uses this approach, see [Tutorial: Encoding a WMA File](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span></span>

### <a name="video-attributes"></a><span data-ttu-id="0387b-184">Video Attribute</span><span class="sxs-lookup"><span data-stu-id="0387b-184">Video Attributes</span></span>

<span data-ttu-id="0387b-185">Um Attribute für den Videostream hinzuzufügen, müssen Sie [**imftranscodeprofile:: setvideoattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0387b-185">To add attributes for the video stream, call [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span> <span data-ttu-id="0387b-186">Diese Attribute geben an, wie der Videostream codiert wird.</span><span class="sxs-lookup"><span data-stu-id="0387b-186">These attributes specify how the video stream is encoded.</span></span> <span data-ttu-id="0387b-187">Wenn die Ausgabedatei keinen Videostream enthält, lassen Sie diese Attribute aus.</span><span class="sxs-lookup"><span data-stu-id="0387b-187">If the output file will not contain a video stream, omit these attributes.</span></span>

<span data-ttu-id="0387b-188">Wie bei audioattributen werden die Video Attribute in zwei Kategorien unterteilt:</span><span class="sxs-lookup"><span data-stu-id="0387b-188">As with audio attributes, the video attributes fall into two categories:</span></span>

-   <span data-ttu-id="0387b-189">Attribute, die das Format des codierten Streams angeben</span><span class="sxs-lookup"><span data-stu-id="0387b-189">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="0387b-190">Attribute, die andere Codierungs Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="0387b-190">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="0387b-191">Format Attribute sind Medientyp Attribute, wie im Abschnitt [Video Medientypen](video-media-types.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0387b-191">Format attributes are media-type attributes, as described in the section [Video Media Types](video-media-types.md).</span></span> <span data-ttu-id="0387b-192">Im folgenden finden Sie eine Liste mit typischen Videoformat Attributen:</span><span class="sxs-lookup"><span data-stu-id="0387b-192">Here is a list of typical video format attributes:</span></span>



| <span data-ttu-id="0387b-193">Format-Attribut</span><span class="sxs-lookup"><span data-stu-id="0387b-193">Format Attribute</span></span>                                                       | <span data-ttu-id="0387b-194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0387b-194">Description</span></span>                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="0387b-195">MF- \_ MT- \_ Untertyp</span><span class="sxs-lookup"><span data-stu-id="0387b-195">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                         | <span data-ttu-id="0387b-196">Der Untertyp.</span><span class="sxs-lookup"><span data-stu-id="0387b-196">The subtype.</span></span> <span data-ttu-id="0387b-197">Siehe [Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="0387b-197">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span> |
| [<span data-ttu-id="0387b-198">MF- \_ MT- \_ Frame \_ Rate</span><span class="sxs-lookup"><span data-stu-id="0387b-198">MF\_MT\_FRAME\_RATE</span></span>](mf-mt-frame-rate-attribute.md)                  | <span data-ttu-id="0387b-199">Die Framerate.</span><span class="sxs-lookup"><span data-stu-id="0387b-199">The frame rate.</span></span>                                                  |
| [<span data-ttu-id="0387b-200">MF- \_ MT- \_ Frame \_ Größe</span><span class="sxs-lookup"><span data-stu-id="0387b-200">MF\_MT\_FRAME\_SIZE</span></span>](mf-mt-frame-size-attribute.md)                  | <span data-ttu-id="0387b-201">Die Frame Größe.</span><span class="sxs-lookup"><span data-stu-id="0387b-201">The frame size.</span></span>                                                  |
| [<span data-ttu-id="0387b-202">**MF-mittlere mittlere \_ \_ \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="0387b-202">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)            | <span data-ttu-id="0387b-203">Die durchschnittliche Bitrate.</span><span class="sxs-lookup"><span data-stu-id="0387b-203">The average bit rate.</span></span>                                            |
| [<span data-ttu-id="0387b-204">Verhältnis der MF- \_ MT- \_ Pixel \_ Seite \_</span><span class="sxs-lookup"><span data-stu-id="0387b-204">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>](mf-mt-pixel-aspect-ratio-attribute.md) | <span data-ttu-id="0387b-205">Das Pixel Seitenverhältnis.</span><span class="sxs-lookup"><span data-stu-id="0387b-205">The pixel aspect ratio.</span></span>                                          |



 

<span data-ttu-id="0387b-206">Die folgenden Codierungs Parameter sind definiert.</span><span class="sxs-lookup"><span data-stu-id="0387b-206">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="0387b-207">Codierungs Parameter</span><span class="sxs-lookup"><span data-stu-id="0387b-207">Encoding Parameter</span></span>                                                             | <span data-ttu-id="0387b-208">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0387b-208">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="0387b-209">MF- \_ transcode- \_ \_ Anfüge- \_ Encoder</span><span class="sxs-lookup"><span data-stu-id="0387b-209">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="0387b-210">Verhindert, dass die transcodieren-API einen Encoder für den Videostream einfügt.</span><span class="sxs-lookup"><span data-stu-id="0387b-210">Prevents the transcode API from inserting an encoder for the video stream.</span></span> |
| [<span data-ttu-id="0387b-211">MF- \_ transcode- \_ Codierungs Profil</span><span class="sxs-lookup"><span data-stu-id="0387b-211">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="0387b-212">Gibt die Konformitäts Vorlage für Geräte an.</span><span class="sxs-lookup"><span data-stu-id="0387b-212">Specifies the device conformance template.</span></span> <span data-ttu-id="0387b-213">(Gilt nur für ASF-Dateien.)</span><span class="sxs-lookup"><span data-stu-id="0387b-213">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="0387b-214">MF- \_ transcode \_ qualityvsspeed</span><span class="sxs-lookup"><span data-stu-id="0387b-214">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="0387b-215">Gibt den Kompromiss zwischen Codierungsqualität und Geschwindigkeit an.</span><span class="sxs-lookup"><span data-stu-id="0387b-215">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="0387b-216">Sie müssen die Format Attribute festlegen.</span><span class="sxs-lookup"><span data-stu-id="0387b-216">You must set the format attributes.</span></span> <span data-ttu-id="0387b-217">Die Codierungs Parameter sind optional.</span><span class="sxs-lookup"><span data-stu-id="0387b-217">The encoding parameters are optional.</span></span>

### <a name="container-attributes"></a><span data-ttu-id="0387b-218">Container Attribute</span><span class="sxs-lookup"><span data-stu-id="0387b-218">Container Attributes</span></span>

<span data-ttu-id="0387b-219">Container Attribute definieren Eigenschaften auf Dateiebene der Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="0387b-219">Container attributes define file-level characteristics of the output file.</span></span> <span data-ttu-id="0387b-220">Um Container Attribute festzulegen, müssen Sie [**imftranscodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0387b-220">To set container attributes, call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span> <span data-ttu-id="0387b-221">Die folgenden Attribute sind definiert.</span><span class="sxs-lookup"><span data-stu-id="0387b-221">The following attributes are defined.</span></span>



| <span data-ttu-id="0387b-222">Attribut</span><span class="sxs-lookup"><span data-stu-id="0387b-222">Attribute</span></span>                                                                          | <span data-ttu-id="0387b-223">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0387b-223">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0387b-224">\_transcode- \_ Anpassungs \_ Profil für MF</span><span class="sxs-lookup"><span data-stu-id="0387b-224">MF\_TRANSCODE\_ADJUST\_PROFILE</span></span>](mf-transcode-adjust-profile.md)                  | <span data-ttu-id="0387b-225">Definiert die Datenstrom Einstellungen, die für die transcodieren-Topologie verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0387b-225">Defines the stream settings to use for the transcode topology.</span></span> <span data-ttu-id="0387b-226">Sie können die Flags so festlegen, dass die Eingabe Quell Einstellungen verwendet oder benutzerdefinierte streamattribute verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0387b-226">You can set the flags to use the input source settings or use custom stream attributes.</span></span> |
| [<span data-ttu-id="0387b-227">MF- \_ transcode- \_ ContainerType</span><span class="sxs-lookup"><span data-stu-id="0387b-227">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                     | <span data-ttu-id="0387b-228">Gibt das Dateiformat der Ausgabedatei an, z. b. MP4 oder ASF.</span><span class="sxs-lookup"><span data-stu-id="0387b-228">Specifies the file format of the output file, such as MP4 or ASF.</span></span> <span data-ttu-id="0387b-229">Basierend auf diesem Wert wird der Topologie die entsprechende Medien Senke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0387b-229">Based on this value, the appropriate media sink is added to the topology.</span></span>            |
| [<span data-ttu-id="0387b-230">MF- \_ transcode \_ Skip- \_ \_ metadatenübertragung</span><span class="sxs-lookup"><span data-stu-id="0387b-230">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER</span></span>](mf-transcode-skip-metadata-transfer.md) | <span data-ttu-id="0387b-231">Gibt an, ob Metadaten aus der Quelle in die Ausgabedatei kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="0387b-231">Specifies whether metadata from the source is copied to the output file.</span></span>                                                                               |
| [<span data-ttu-id="0387b-232">MF- \_ transcode- \_ topologymode</span><span class="sxs-lookup"><span data-stu-id="0387b-232">MF\_TRANSCODE\_TOPOLOGYMODE</span></span>](mf-transcode-topologymode.md)                       | <span data-ttu-id="0387b-233">Gibt an, ob während der Transcodierung hardwarebasierte Codecs verwendet werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="0387b-233">Specifies whether hardware-based codecs may be used during transcoding.</span></span>                                                                                |
| [<span data-ttu-id="0387b-234">MFT \_ fieldofuse \_ Unlock- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="0387b-234">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)          | <span data-ttu-id="0387b-235">Entsperrt einen Codec mit Einschränkungen für das Feld.</span><span class="sxs-lookup"><span data-stu-id="0387b-235">Unlocks a codec that has field-of-use restrictions.</span></span> <span data-ttu-id="0387b-236">Weitere Informationen finden Sie unter [Einschränkungen](field-of-use-restrictions.md)für das Feld "Verwendung".</span><span class="sxs-lookup"><span data-stu-id="0387b-236">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>              |



 

<span data-ttu-id="0387b-237">Das MF-Attribut " [ \_ \_ ContainerType](mf-transcode-containertype.md) " ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0387b-237">The [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute is required.</span></span> <span data-ttu-id="0387b-238">Die anderen Container Attribute sind optional.</span><span class="sxs-lookup"><span data-stu-id="0387b-238">The other container attributes are optional.</span></span>

## <a name="creating-a-transcode-topology"></a><span data-ttu-id="0387b-239">Erstellen einer transcode-Topologie</span><span class="sxs-lookup"><span data-stu-id="0387b-239">Creating a Transcode Topology</span></span>

<span data-ttu-id="0387b-240">Die transcodieren-Topologie ist eine partielle Topologie, die die Medienquelle, die entsprechenden Codecs und die Medien Senke enthält.</span><span class="sxs-lookup"><span data-stu-id="0387b-240">The transcode topology is a partial topology that contains the media source, the appropriate codecs, and the media sink.</span></span> <span data-ttu-id="0387b-241">Um die transcodieren-Topologie zu erstellen, rufen Sie die [**mfkreatetranscodetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="0387b-241">To create the transcode topology, call to the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function.</span></span> <span data-ttu-id="0387b-242">Diese Funktion übernimmt die folgenden Parameter als Eingabe:</span><span class="sxs-lookup"><span data-stu-id="0387b-242">This function takes the following parameters as input:</span></span>

-   <span data-ttu-id="0387b-243">Ein Zeiger auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="0387b-243">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="0387b-244">Der Name der Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="0387b-244">The name of the output file.</span></span>
-   <span data-ttu-id="0387b-245">Ein Zeiger auf die [**imftranscodeprofile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) -Schnittstelle des transcodieren-Profils.</span><span class="sxs-lookup"><span data-stu-id="0387b-245">A pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface of the transcode profile.</span></span>

<span data-ttu-id="0387b-246">Die-Funktion gibt einen Zeiger auf die [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="0387b-246">The function returns a pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

## <a name="running-the-encoding-session"></a><span data-ttu-id="0387b-247">Ausführen der Codierungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="0387b-247">Running the Encoding Session</span></span>

<span data-ttu-id="0387b-248">Nachdem Sie die Topologie erstellt haben, können Sie die Datei codieren.</span><span class="sxs-lookup"><span data-stu-id="0387b-248">After you create the topology, you are ready to encode the file.</span></span> <span data-ttu-id="0387b-249">Sie können das Profil zu diesem Zeitpunkt verwerfen.</span><span class="sxs-lookup"><span data-stu-id="0387b-249">You can discard the profile at this point.</span></span>

1.  <span data-ttu-id="0387b-250">Rufen Sie [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um die Medien Sitzung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0387b-250">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session.</span></span>
2.  <span data-ttu-id="0387b-251">Wenden Sie [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) an, um die Topologie für die Medien Sitzung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0387b-251">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
3.  <span data-ttu-id="0387b-252">Zum Starten der Codierungs Sitzung wird [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0387b-252">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start the encoding session.</span></span>
4.  <span data-ttu-id="0387b-253">Warten Sie auf das Ereignis [mesessionend](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="0387b-253">Wait for the [MESessionEnded](mesessionended.md) event.</span></span>
5.  <span data-ttu-id="0387b-254">[**Imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) wird aufgerufen, um die Medien Sitzung zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0387b-254">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
6.  <span data-ttu-id="0387b-255">Warten Sie auf das Ereignis [mesessionclosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="0387b-255">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span>
7.  <span data-ttu-id="0387b-256">Nennen Sie [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="0387b-256">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
8.  <span data-ttu-id="0387b-257">Rückrufe [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="0387b-257">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="0387b-258">Der meiste Zeitaufwand für die Codierung erfolgt zwischen den Schritten 3 und 4.</span><span class="sxs-lookup"><span data-stu-id="0387b-258">Most of the time spent encoding occurs between steps 3 and 4.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0387b-259">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0387b-259">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0387b-260">Transcode-API</span><span class="sxs-lookup"><span data-stu-id="0387b-260">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="0387b-261">Informationen zur Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="0387b-261">About the Media Session</span></span>](about-the-media-session.md)
</dt> </dl>

 

 



