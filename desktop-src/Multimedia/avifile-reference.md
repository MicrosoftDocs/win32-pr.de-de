---
title: Avifile-Referenz
description: Avifile-Referenz
ms.assetid: 73532d83-89c2-4911-8558-ce110e9f0f95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0291d0ac5864a9b370e79a98fa061770d05bca03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037515"
---
# <a name="avifile-reference"></a><span data-ttu-id="1e09f-103">Avifile-Referenz</span><span class="sxs-lookup"><span data-stu-id="1e09f-103">AVIFile Reference</span></span>

<span data-ttu-id="1e09f-104">In diesem Abschnitt werden die Funktionen, Strukturen und Makros für Anwendungen beschrieben, die die avifile-Dienste verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e09f-104">This section describes the functions, structures, and macros for applications using the AVIFile services.</span></span> <span data-ttu-id="1e09f-105">Diese Elemente werden wie folgt gruppiert:</span><span class="sxs-lookup"><span data-stu-id="1e09f-105">These elements are grouped as follows:</span></span>

## <a name="avifile-library-operations"></a><span data-ttu-id="1e09f-106">Vorgänge der avifile-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e09f-106">AVIFile Library Operations</span></span>

-   [<span data-ttu-id="1e09f-107">**Avifileingeit**</span><span class="sxs-lookup"><span data-stu-id="1e09f-107">**AVIFileInit**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileinit)
-   [<span data-ttu-id="1e09f-108">**Avifileexit**</span><span class="sxs-lookup"><span data-stu-id="1e09f-108">**AVIFileExit**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileexit)

## <a name="opening-and-closing-avi-files"></a><span data-ttu-id="1e09f-109">Öffnen und Schließen von AVI-Dateien</span><span class="sxs-lookup"><span data-stu-id="1e09f-109">Opening and Closing AVI Files</span></span>

-   [<span data-ttu-id="1e09f-110">**AVIFileOpen**</span><span class="sxs-lookup"><span data-stu-id="1e09f-110">**AVIFileOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileopen)
-   [<span data-ttu-id="1e09f-111">**Avifileadressf**</span><span class="sxs-lookup"><span data-stu-id="1e09f-111">**AVIFileAddRef**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileaddref)
-   [<span data-ttu-id="1e09f-112">**Avifilerelease**</span><span class="sxs-lookup"><span data-stu-id="1e09f-112">**AVIFileRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)
-   [<span data-ttu-id="1e09f-113">**Getopendatamepreview**</span><span class="sxs-lookup"><span data-stu-id="1e09f-113">**GetOpenFileNamePreview**</span></span>](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

## <a name="reading-from-a-file"></a><span data-ttu-id="1e09f-114">Lesen aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="1e09f-114">Reading from a File</span></span>

-   [<span data-ttu-id="1e09f-115">**Avifileingefo**</span><span class="sxs-lookup"><span data-stu-id="1e09f-115">**AVIFileInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileinfo)
-   [<span data-ttu-id="1e09f-116">**Avifileingefo**</span><span class="sxs-lookup"><span data-stu-id="1e09f-116">**AVIFILEINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa)
-   [<span data-ttu-id="1e09f-117">**Avifilereaddata**</span><span class="sxs-lookup"><span data-stu-id="1e09f-117">**AVIFileReadData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata)

## <a name="writing-to-a-file"></a><span data-ttu-id="1e09f-118">Schreiben in eine Datei</span><span class="sxs-lookup"><span data-stu-id="1e09f-118">Writing to a File</span></span>

-   [<span data-ttu-id="1e09f-119">**Avifileschreitedata**</span><span class="sxs-lookup"><span data-stu-id="1e09f-119">**AVIFileWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)

## <a name="using-the-clipboard"></a><span data-ttu-id="1e09f-120">Verwenden der Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="1e09f-120">Using the Clipboard</span></span>

-   [<span data-ttu-id="1e09f-121">**Aviputfleonclipboard**</span><span class="sxs-lookup"><span data-stu-id="1e09f-121">**AVIPutFileOnClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard)
-   [<span data-ttu-id="1e09f-122">**Avigetfromclipboard**</span><span class="sxs-lookup"><span data-stu-id="1e09f-122">**AVIGetFromClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)
-   [<span data-ttu-id="1e09f-123">**Aviclearclipboard**</span><span class="sxs-lookup"><span data-stu-id="1e09f-123">**AVIClearClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard)

## <a name="opening-and-closing-streams"></a><span data-ttu-id="1e09f-124">Öffnen und Schließen von Streams</span><span class="sxs-lookup"><span data-stu-id="1e09f-124">Opening and Closing Streams</span></span>

-   [<span data-ttu-id="1e09f-125">**AVIFileGetStream**</span><span class="sxs-lookup"><span data-stu-id="1e09f-125">**AVIFileGetStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)
-   [<span data-ttu-id="1e09f-126">**Avistreamopenfromfile**</span><span class="sxs-lookup"><span data-stu-id="1e09f-126">**AVIStreamOpenFromFile**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea)
-   [<span data-ttu-id="1e09f-127">**Avistreamadressf**</span><span class="sxs-lookup"><span data-stu-id="1e09f-127">**AVIStreamAddRef**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref)
-   [<span data-ttu-id="1e09f-128">**Avistreamrelease**</span><span class="sxs-lookup"><span data-stu-id="1e09f-128">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="reading-stream-information"></a><span data-ttu-id="1e09f-129">Lesen von streaminformationen</span><span class="sxs-lookup"><span data-stu-id="1e09f-129">Reading Stream Information</span></span>

-   [<span data-ttu-id="1e09f-130">**AVISTREAMINFO**</span><span class="sxs-lookup"><span data-stu-id="1e09f-130">**AVISTREAMINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)
-   [<span data-ttu-id="1e09f-131">**Avistreamlesdata**</span><span class="sxs-lookup"><span data-stu-id="1e09f-131">**AVIStreamReadData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata)
-   [<span data-ttu-id="1e09f-132">**Avistreamdatasize**</span><span class="sxs-lookup"><span data-stu-id="1e09f-132">**AVIStreamDataSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)
-   [<span data-ttu-id="1e09f-133">**Avistreamlesformat**</span><span class="sxs-lookup"><span data-stu-id="1e09f-133">**AVIStreamReadFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat)
-   [<span data-ttu-id="1e09f-134">**Avistreamformatsize**</span><span class="sxs-lookup"><span data-stu-id="1e09f-134">**AVIStreamFormatSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)
-   [<span data-ttu-id="1e09f-135">**Avistreamread**</span><span class="sxs-lookup"><span data-stu-id="1e09f-135">**AVIStreamRead**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamread)
-   [<span data-ttu-id="1e09f-136">**Avistreamsamplesize**</span><span class="sxs-lookup"><span data-stu-id="1e09f-136">**AVIStreamSampleSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)
-   [<span data-ttu-id="1e09f-137">**Avistreambeginstreaming**</span><span class="sxs-lookup"><span data-stu-id="1e09f-137">**AVIStreamBeginStreaming**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming)
-   [<span data-ttu-id="1e09f-138">**Avistreamendstreaming**</span><span class="sxs-lookup"><span data-stu-id="1e09f-138">**AVIStreamEndStreaming**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming)

## <a name="decompressing-video-data-in-a-stream"></a><span data-ttu-id="1e09f-139">Dekomprimieren von Video Daten in einem Stream</span><span class="sxs-lookup"><span data-stu-id="1e09f-139">Decompressing Video Data in a Stream</span></span>

-   [<span data-ttu-id="1e09f-140">**AVIStreamGetFrameOpen**</span><span class="sxs-lookup"><span data-stu-id="1e09f-140">**AVIStreamGetFrameOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen)
-   [<span data-ttu-id="1e09f-141">**AVIStreamGetFrame**</span><span class="sxs-lookup"><span data-stu-id="1e09f-141">**AVIStreamGetFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe)
-   [<span data-ttu-id="1e09f-142">**Avistreamgetframeclose**</span><span class="sxs-lookup"><span data-stu-id="1e09f-142">**AVIStreamGetFrameClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

## <a name="creating-a-file-from-existing-streams"></a><span data-ttu-id="1e09f-143">Erstellen einer Datei aus vorhandenen Streams</span><span class="sxs-lookup"><span data-stu-id="1e09f-143">Creating a File from Existing Streams</span></span>

-   [<span data-ttu-id="1e09f-144">**Avisave**</span><span class="sxs-lookup"><span data-stu-id="1e09f-144">**AVISave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisavea)
-   [<span data-ttu-id="1e09f-145">**Avisavev**</span><span class="sxs-lookup"><span data-stu-id="1e09f-145">**AVISaveV**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisaveva)
-   [<span data-ttu-id="1e09f-146">**Avisaveoptions**</span><span class="sxs-lookup"><span data-stu-id="1e09f-146">**AVISaveOptions**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions)
-   [<span data-ttu-id="1e09f-147">**Getsavefile Name Preview**</span><span class="sxs-lookup"><span data-stu-id="1e09f-147">**GetSaveFileNamePreview**</span></span>](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa)
-   [<span data-ttu-id="1e09f-148">**Avimakefilefromstreams**</span><span class="sxs-lookup"><span data-stu-id="1e09f-148">**AVIMakeFileFromStreams**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams)

## <a name="writing-individual-streams"></a><span data-ttu-id="1e09f-149">Schreiben einzelner Streams</span><span class="sxs-lookup"><span data-stu-id="1e09f-149">Writing Individual Streams</span></span>

-   [<span data-ttu-id="1e09f-150">**Avifilekreatestream**</span><span class="sxs-lookup"><span data-stu-id="1e09f-150">**AVIFileCreateStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)
-   [<span data-ttu-id="1e09f-151">**Avistreamsetformat**</span><span class="sxs-lookup"><span data-stu-id="1e09f-151">**AVIStreamSetFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)
-   [<span data-ttu-id="1e09f-152">**AVIStreamWrite**</span><span class="sxs-lookup"><span data-stu-id="1e09f-152">**AVIStreamWrite**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite)
-   [<span data-ttu-id="1e09f-153">**Avifileschreitedata**</span><span class="sxs-lookup"><span data-stu-id="1e09f-153">**AVIFileWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)
-   [<span data-ttu-id="1e09f-154">**Avistreamschreitedata**</span><span class="sxs-lookup"><span data-stu-id="1e09f-154">**AVIStreamWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)
-   [<span data-ttu-id="1e09f-155">**Avistreamrelease**</span><span class="sxs-lookup"><span data-stu-id="1e09f-155">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="finding-the-starting-position-in-a-stream"></a><span data-ttu-id="1e09f-156">Ermitteln der Anfangs Position in einem Stream</span><span class="sxs-lookup"><span data-stu-id="1e09f-156">Finding the Starting Position in a Stream</span></span>

-   [<span data-ttu-id="1e09f-157">**AVIStreamStart**</span><span class="sxs-lookup"><span data-stu-id="1e09f-157">**AVIStreamStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamstart)
-   [<span data-ttu-id="1e09f-158">**Avistreamstarttime**</span><span class="sxs-lookup"><span data-stu-id="1e09f-158">**AVIStreamStartTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)
-   [<span data-ttu-id="1e09f-159">**Avistreamlength**</span><span class="sxs-lookup"><span data-stu-id="1e09f-159">**AVIStreamLength**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamlength)
-   [<span data-ttu-id="1e09f-160">**Avistreamverlängert-Zeit**</span><span class="sxs-lookup"><span data-stu-id="1e09f-160">**AVIStreamLengthTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)
-   [<span data-ttu-id="1e09f-161">**Avistreamfindsample**</span><span class="sxs-lookup"><span data-stu-id="1e09f-161">**AVIStreamFindSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [<span data-ttu-id="1e09f-162">**Avistreamend**</span><span class="sxs-lookup"><span data-stu-id="1e09f-162">**AVIStreamEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamend)
-   [<span data-ttu-id="1e09f-163">**Avistreamendzeit**</span><span class="sxs-lookup"><span data-stu-id="1e09f-163">**AVIStreamEndTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

## <a name="finding-sample-and-key-frames"></a><span data-ttu-id="1e09f-164">Suchen von Beispiel-und Keyframes</span><span class="sxs-lookup"><span data-stu-id="1e09f-164">Finding Sample and Key Frames</span></span>

-   [<span data-ttu-id="1e09f-165">**Avistreamfindsample**</span><span class="sxs-lookup"><span data-stu-id="1e09f-165">**AVIStreamFindSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [<span data-ttu-id="1e09f-166">**Avistreamiskeyframe**</span><span class="sxs-lookup"><span data-stu-id="1e09f-166">**AVIStreamIsKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)
-   [<span data-ttu-id="1e09f-167">**Avistreamnearestkeyframe**</span><span class="sxs-lookup"><span data-stu-id="1e09f-167">**AVIStreamNearestKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)
-   [<span data-ttu-id="1e09f-168">**Avistreamnearestkeyframetime**</span><span class="sxs-lookup"><span data-stu-id="1e09f-168">**AVIStreamNearestKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime)
-   [<span data-ttu-id="1e09f-169">**Avistreamnearestsample**</span><span class="sxs-lookup"><span data-stu-id="1e09f-169">**AVIStreamNearestSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)
-   [<span data-ttu-id="1e09f-170">**Avistreamnearestsampletime**</span><span class="sxs-lookup"><span data-stu-id="1e09f-170">**AVIStreamNearestSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)
-   [<span data-ttu-id="1e09f-171">**Avistreamnextkeyframe**</span><span class="sxs-lookup"><span data-stu-id="1e09f-171">**AVIStreamNextKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)
-   [<span data-ttu-id="1e09f-172">**Avistreamnextkeyframetime**</span><span class="sxs-lookup"><span data-stu-id="1e09f-172">**AVIStreamNextKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)
-   [<span data-ttu-id="1e09f-173">**Avistreamnextsample**</span><span class="sxs-lookup"><span data-stu-id="1e09f-173">**AVIStreamNextSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)
-   [<span data-ttu-id="1e09f-174">**Avistreamnextsampletime**</span><span class="sxs-lookup"><span data-stu-id="1e09f-174">**AVIStreamNextSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)
-   [<span data-ttu-id="1e09f-175">**Avistreamprevkeyframe**</span><span class="sxs-lookup"><span data-stu-id="1e09f-175">**AVIStreamPrevKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)
-   [<span data-ttu-id="1e09f-176">**Avistreamprevkeyframetime**</span><span class="sxs-lookup"><span data-stu-id="1e09f-176">**AVIStreamPrevKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)
-   [<span data-ttu-id="1e09f-177">**Avistreamprevsample**</span><span class="sxs-lookup"><span data-stu-id="1e09f-177">**AVIStreamPrevSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)
-   [<span data-ttu-id="1e09f-178">**Avistreamprevsampletime**</span><span class="sxs-lookup"><span data-stu-id="1e09f-178">**AVIStreamPrevSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)
-   [<span data-ttu-id="1e09f-179">**Avistreamsampleprosample**</span><span class="sxs-lookup"><span data-stu-id="1e09f-179">**AVIStreamSampleToSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)

## <a name="switching-between-samples-and-time"></a><span data-ttu-id="1e09f-180">Wechseln zwischen Beispielen und Zeit</span><span class="sxs-lookup"><span data-stu-id="1e09f-180">Switching Between Samples and Time</span></span>

-   [<span data-ttu-id="1e09f-181">**Avistreamsamplecomtime**</span><span class="sxs-lookup"><span data-stu-id="1e09f-181">**AVIStreamSampleToTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime)
-   [<span data-ttu-id="1e09f-182">**Avistreamtimeto Sample**</span><span class="sxs-lookup"><span data-stu-id="1e09f-182">**AVIStreamTimeToSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample)

## <a name="creating-temporary-streams"></a><span data-ttu-id="1e09f-183">Erstellen temporärer Streams</span><span class="sxs-lookup"><span data-stu-id="1e09f-183">Creating Temporary Streams</span></span>

-   [<span data-ttu-id="1e09f-184">**Avistreamcreate**</span><span class="sxs-lookup"><span data-stu-id="1e09f-184">**AVIStreamCreate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate)
-   [<span data-ttu-id="1e09f-185">**Avimakecompressedstream**</span><span class="sxs-lookup"><span data-stu-id="1e09f-185">**AVIMakeCompressedStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream)
-   [<span data-ttu-id="1e09f-186">**Avistreamrelease**</span><span class="sxs-lookup"><span data-stu-id="1e09f-186">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="editing-avi-streams"></a><span data-ttu-id="1e09f-187">Bearbeiten von AVI-Streams</span><span class="sxs-lookup"><span data-stu-id="1e09f-187">Editing AVI Streams</span></span>

-   [<span data-ttu-id="1e09f-188">**"Kreateeditablestream"**</span><span class="sxs-lookup"><span data-stu-id="1e09f-188">**CreateEditableStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-createeditablestream)
-   [<span data-ttu-id="1e09f-189">**Editstreamcut**</span><span class="sxs-lookup"><span data-stu-id="1e09f-189">**EditStreamCut**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)
-   [<span data-ttu-id="1e09f-190">**Editstreamcopy**</span><span class="sxs-lookup"><span data-stu-id="1e09f-190">**EditStreamCopy**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)
-   [<span data-ttu-id="1e09f-191">**Editstreampaste**</span><span class="sxs-lookup"><span data-stu-id="1e09f-191">**EditStreamPaste**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreampaste)
-   [<span data-ttu-id="1e09f-192">**Editstreamclone**</span><span class="sxs-lookup"><span data-stu-id="1e09f-192">**EditStreamClone**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamclone)
-   [<span data-ttu-id="1e09f-193">**Editstreamabtinfo**</span><span class="sxs-lookup"><span data-stu-id="1e09f-193">**EditStreamSetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa)
-   [<span data-ttu-id="1e09f-194">**Editstreamsetname**</span><span class="sxs-lookup"><span data-stu-id="1e09f-194">**EditStreamSetName**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea)

## <a name="related-topics"></a><span data-ttu-id="1e09f-195">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e09f-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e09f-196">Avifile-Funktionen und-Makros</span><span class="sxs-lookup"><span data-stu-id="1e09f-196">AVIFile Functions and Macros</span></span>](avifile-functions-and-macros.md)
</dt> </dl>

 

 




