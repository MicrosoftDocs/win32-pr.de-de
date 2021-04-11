---
title: Referenz zum Video Komprimierungs-Manager
description: Referenz zum Video Komprimierungs-Manager
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Video für Windows (Vfw), Video Komprimierungs-Manager (VCM)
- VFW (Video für Windows), Video Komprimierungs-Manager (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206451"
---
# <a name="video-compression-manager-reference"></a><span data-ttu-id="34a02-105">Referenz zum Video Komprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="34a02-105">Video Compression Manager Reference</span></span>

<span data-ttu-id="34a02-106">In diesem Abschnitt werden die Funktionen, Strukturen, Meldungen und Makros beschrieben, die mit VCM verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="34a02-106">This section describes the functions, structures, messages, and macros, associated with VCM.</span></span> <span data-ttu-id="34a02-107">Diese Elemente werden wie folgt gruppiert.</span><span class="sxs-lookup"><span data-stu-id="34a02-107">These elements are grouped as follows.</span></span>

## <a name="compressor-installation-and-removal"></a><span data-ttu-id="34a02-108">Installation und Entfernung von Kompressors</span><span class="sxs-lookup"><span data-stu-id="34a02-108">Compressor Installation and Removal</span></span>

-   [<span data-ttu-id="34a02-109">**Icinstall**</span><span class="sxs-lookup"><span data-stu-id="34a02-109">**ICInstall**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [<span data-ttu-id="34a02-110">**Iclocate**</span><span class="sxs-lookup"><span data-stu-id="34a02-110">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="34a02-111">**Icopen**</span><span class="sxs-lookup"><span data-stu-id="34a02-111">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="34a02-112">**Icclose**</span><span class="sxs-lookup"><span data-stu-id="34a02-112">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [<span data-ttu-id="34a02-113">**Ikremove**</span><span class="sxs-lookup"><span data-stu-id="34a02-113">**ICRemove**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [<span data-ttu-id="34a02-114">**Icopenfunction**</span><span class="sxs-lookup"><span data-stu-id="34a02-114">**ICOpenFunction**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a><span data-ttu-id="34a02-115">Suchen und Öffnen eines Kompressors</span><span class="sxs-lookup"><span data-stu-id="34a02-115">Locating and Opening a Compressor</span></span>

-   [<span data-ttu-id="34a02-116">**Iclocate**</span><span class="sxs-lookup"><span data-stu-id="34a02-116">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="34a02-117">**Icopen**</span><span class="sxs-lookup"><span data-stu-id="34a02-117">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="34a02-118">**Icdebug**</span><span class="sxs-lookup"><span data-stu-id="34a02-118">**ICDecompressOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [<span data-ttu-id="34a02-119">**Icdrawopen**</span><span class="sxs-lookup"><span data-stu-id="34a02-119">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="34a02-120">**Icinfo**</span><span class="sxs-lookup"><span data-stu-id="34a02-120">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="34a02-121">**Icclose**</span><span class="sxs-lookup"><span data-stu-id="34a02-121">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a><span data-ttu-id="34a02-122">Auswählen von Kompressoren</span><span class="sxs-lookup"><span data-stu-id="34a02-122">Selecting Compressors</span></span>

-   [<span data-ttu-id="34a02-123">**Iccompressorchoose**</span><span class="sxs-lookup"><span data-stu-id="34a02-123">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [<span data-ttu-id="34a02-124">**Iccompressorfree**</span><span class="sxs-lookup"><span data-stu-id="34a02-124">**ICCompressorFree**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [<span data-ttu-id="34a02-125">**Compvaren**</span><span class="sxs-lookup"><span data-stu-id="34a02-125">**COMPVARS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a><span data-ttu-id="34a02-126">Konfigurieren von Kompressoren</span><span class="sxs-lookup"><span data-stu-id="34a02-126">Configuring Compressors</span></span>

-   [<span data-ttu-id="34a02-127">**ICM- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="34a02-127">**ICM\_CONFIGURE**</span></span>](icm-configure.md)
-   [<span data-ttu-id="34a02-128">**ICM \_ GetState**</span><span class="sxs-lookup"><span data-stu-id="34a02-128">**ICM\_GETSTATE**</span></span>](icm-getstate.md)
-   [<span data-ttu-id="34a02-129">**ICM \_ SetState**</span><span class="sxs-lookup"><span data-stu-id="34a02-129">**ICM\_SETSTATE**</span></span>](icm-setstate.md)
-   [<span data-ttu-id="34a02-130">**Icsendmessage**</span><span class="sxs-lookup"><span data-stu-id="34a02-130">**ICSendMessage**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a><span data-ttu-id="34a02-131">Informationen zum Kompressor</span><span class="sxs-lookup"><span data-stu-id="34a02-131">Compressor Information</span></span>

-   [<span data-ttu-id="34a02-132">**Icgetinfo**</span><span class="sxs-lookup"><span data-stu-id="34a02-132">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="34a02-133">**Icinfo**</span><span class="sxs-lookup"><span data-stu-id="34a02-133">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="34a02-134">**ICM \_ getdefaultkeyframerate**</span><span class="sxs-lookup"><span data-stu-id="34a02-134">**ICM\_GETDEFAULTKEYFRAMERATE**</span></span>](icm-getdefaultkeyframerate.md)
-   [<span data-ttu-id="34a02-135">**Icgetdisplayformat**</span><span class="sxs-lookup"><span data-stu-id="34a02-135">**ICGetDisplayFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [<span data-ttu-id="34a02-136">**ICM \_ getdefaultquality**</span><span class="sxs-lookup"><span data-stu-id="34a02-136">**ICM\_GETDEFAULTQUALITY**</span></span>](icm-getdefaultquality.md)
-   [<span data-ttu-id="34a02-137">**ICM \_ Info**</span><span class="sxs-lookup"><span data-stu-id="34a02-137">**ICM\_ABOUT**</span></span>](icm-about.md)

## <a name="single-image-compression"></a><span data-ttu-id="34a02-138">Komprimierung mit einem Bild</span><span class="sxs-lookup"><span data-stu-id="34a02-138">Single Image Compression</span></span>

-   [<span data-ttu-id="34a02-139">**Icimagecompress**</span><span class="sxs-lookup"><span data-stu-id="34a02-139">**ICImageCompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a><span data-ttu-id="34a02-140">Sequenz Komprimierung</span><span class="sxs-lookup"><span data-stu-id="34a02-140">Sequence Compression</span></span>

-   [<span data-ttu-id="34a02-141">**Icabqcompressframe**</span><span class="sxs-lookup"><span data-stu-id="34a02-141">**ICSeqCompressFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [<span data-ttu-id="34a02-142">**Icabqcompressframestart**</span><span class="sxs-lookup"><span data-stu-id="34a02-142">**ICSeqCompressFrameStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [<span data-ttu-id="34a02-143">**Icabqcompressframeend**</span><span class="sxs-lookup"><span data-stu-id="34a02-143">**ICSeqCompressFrameEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a><span data-ttu-id="34a02-144">Compvaren</span><span class="sxs-lookup"><span data-stu-id="34a02-144">COMPVARS</span></span>

-   [<span data-ttu-id="34a02-145">**Iccompressorchoose**</span><span class="sxs-lookup"><span data-stu-id="34a02-145">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a><span data-ttu-id="34a02-146">Bild Datenkomprimierung</span><span class="sxs-lookup"><span data-stu-id="34a02-146">Image Data Compression</span></span>

-   [<span data-ttu-id="34a02-147">**Iccompress**</span><span class="sxs-lookup"><span data-stu-id="34a02-147">**ICCOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [<span data-ttu-id="34a02-148">**ICM \_ - \_ komprimierungsget- \_ Format**</span><span class="sxs-lookup"><span data-stu-id="34a02-148">**ICM\_COMPRESS\_GET\_FORMAT**</span></span>](icm-compress-get-format.md)
-   [<span data-ttu-id="34a02-149">**ICM- \_ Komprimierungs \_ Abfrage**</span><span class="sxs-lookup"><span data-stu-id="34a02-149">**ICM\_COMPRESS\_QUERY**</span></span>](icm-compress-query.md)
-   [<span data-ttu-id="34a02-150">**ICM- \_ Komprimierung \_ get \_ size**</span><span class="sxs-lookup"><span data-stu-id="34a02-150">**ICM\_COMPRESS\_GET\_SIZE**</span></span>](icm-compress-get-size.md)
-   [<span data-ttu-id="34a02-151">**ICM- \_ Komprimierung \_ starten**</span><span class="sxs-lookup"><span data-stu-id="34a02-151">**ICM\_COMPRESS\_BEGIN**</span></span>](icm-compress-begin.md)
-   [<span data-ttu-id="34a02-152">**ICM- \_ Komprimierung \_ Beenden**</span><span class="sxs-lookup"><span data-stu-id="34a02-152">**ICM\_COMPRESS\_END**</span></span>](icm-compress-end.md)

## <a name="compressor-monitoring"></a><span data-ttu-id="34a02-153">Überwachung des Kompressors</span><span class="sxs-lookup"><span data-stu-id="34a02-153">Compressor Monitoring</span></span>

-   [<span data-ttu-id="34a02-154">**Icsetstatusproc**</span><span class="sxs-lookup"><span data-stu-id="34a02-154">**ICSETSTATUSPROC**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a><span data-ttu-id="34a02-155">Komprimieren von einzelnen Bildern</span><span class="sxs-lookup"><span data-stu-id="34a02-155">Decompressing Single Images</span></span>

-   [<span data-ttu-id="34a02-156">**Icimagedebug**</span><span class="sxs-lookup"><span data-stu-id="34a02-156">**ICImageDecompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a><span data-ttu-id="34a02-157">Abbild Daten werden komprimiert.</span><span class="sxs-lookup"><span data-stu-id="34a02-157">Decompressing Image Data</span></span>

-   [<span data-ttu-id="34a02-158">**ICDE CompressEx**</span><span class="sxs-lookup"><span data-stu-id="34a02-158">**ICDECOMPRESSEX**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [<span data-ttu-id="34a02-159">**ICDE compressexbegin**</span><span class="sxs-lookup"><span data-stu-id="34a02-159">**ICDecompressExBegin**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [<span data-ttu-id="34a02-160">**ICM- \_ \_ decoderende**</span><span class="sxs-lookup"><span data-stu-id="34a02-160">**ICM\_DECOMPRESSEX\_END**</span></span>](icm-decompressex-end.md)
-   [<span data-ttu-id="34a02-161">**ICM \_ Decompress \_ get- \_ Format**</span><span class="sxs-lookup"><span data-stu-id="34a02-161">**ICM\_DECOMPRESS\_GET\_FORMAT**</span></span>](icm-decompress-get-format.md)
-   [<span data-ttu-id="34a02-162">**ICM- \_ aufgeschbe \_ get- \_ Palette**</span><span class="sxs-lookup"><span data-stu-id="34a02-162">**ICM\_DECOMPRESS\_GET\_PALETTE**</span></span>](icm-decompress-get-palette.md)
-   [<span data-ttu-id="34a02-163">**Icabcompressexquery**</span><span class="sxs-lookup"><span data-stu-id="34a02-163">**ICDecompressExQuery**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [<span data-ttu-id="34a02-164">**Icdebug**</span><span class="sxs-lookup"><span data-stu-id="34a02-164">**ICDECOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [<span data-ttu-id="34a02-165">**ICM-Start \_ \_ Anfang**</span><span class="sxs-lookup"><span data-stu-id="34a02-165">**ICM\_DECOMPRESS\_BEGIN**</span></span>](icm-decompress-begin.md)
-   [<span data-ttu-id="34a02-166">**ICM-Debug- \_ \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="34a02-166">**ICM\_DECOMPRESS\_END**</span></span>](icm-decompress-end.md)
-   [<span data-ttu-id="34a02-167">**ICM-Abfrage "Debug" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="34a02-167">**ICM\_DECOMPRESS\_QUERY**</span></span>](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a><span data-ttu-id="34a02-168">Verwenden von Hardware-Drawing Funktionen</span><span class="sxs-lookup"><span data-stu-id="34a02-168">Using Hardware-Drawing Capabilities</span></span>

-   [<span data-ttu-id="34a02-169">**Icgetinfo**</span><span class="sxs-lookup"><span data-stu-id="34a02-169">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="34a02-170">**Icdrawbegin**</span><span class="sxs-lookup"><span data-stu-id="34a02-170">**ICDRAWBEGIN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [<span data-ttu-id="34a02-171">**ICM- \_ Zeichnungs \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="34a02-171">**ICM\_DRAW\_END**</span></span>](icm-draw-end.md)
-   [<span data-ttu-id="34a02-172">**ICM-Zeichnungs Leerung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="34a02-172">**ICM\_DRAW\_FLUSH**</span></span>](icm-draw-flush.md)
-   [<span data-ttu-id="34a02-173">**ICM- \_ Draw- \_ Abfrage**</span><span class="sxs-lookup"><span data-stu-id="34a02-173">**ICM\_DRAW\_QUERY**</span></span>](icm-draw-query.md)
-   [<span data-ttu-id="34a02-174">**Icdrawvorschlags Format**</span><span class="sxs-lookup"><span data-stu-id="34a02-174">**ICDrawSuggestFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [<span data-ttu-id="34a02-175">**ICM- \_ Zeichnen \_ starten**</span><span class="sxs-lookup"><span data-stu-id="34a02-175">**ICM\_DRAW\_START**</span></span>](icm-draw-start.md)
-   [<span data-ttu-id="34a02-176">**ICM- \_ Zeichnungs \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="34a02-176">**ICM\_DRAW\_STOP**</span></span>](icm-draw-stop.md)
-   [<span data-ttu-id="34a02-177">**ICM \_ getbufferswanted**</span><span class="sxs-lookup"><span data-stu-id="34a02-177">**ICM\_GETBUFFERSWANTED**</span></span>](icm-getbufferswanted.md)
-   [<span data-ttu-id="34a02-178">**ICM- \_ Zeichnen \_**</span><span class="sxs-lookup"><span data-stu-id="34a02-178">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="34a02-179">**Icdrawopen**</span><span class="sxs-lookup"><span data-stu-id="34a02-179">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="34a02-180">**Icdraw**</span><span class="sxs-lookup"><span data-stu-id="34a02-180">**ICDRAW**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [<span data-ttu-id="34a02-181">**ICM \_ Zeichnen \_ GetTime**</span><span class="sxs-lookup"><span data-stu-id="34a02-181">**ICM\_DRAW\_GETTIME**</span></span>](icm-draw-gettime.md)
-   [<span data-ttu-id="34a02-182">**ICM \_ Draw \_ setTime**</span><span class="sxs-lookup"><span data-stu-id="34a02-182">**ICM\_DRAW\_SETTIME**</span></span>](icm-draw-settime.md)
-   [<span data-ttu-id="34a02-183">**ICM- \_ Zeichnungs \_ Fenster**</span><span class="sxs-lookup"><span data-stu-id="34a02-183">**ICM\_DRAW\_WINDOW**</span></span>](icm-draw-window.md)
-   [<span data-ttu-id="34a02-184">**ICM- \_ Zeichnen \_**</span><span class="sxs-lookup"><span data-stu-id="34a02-184">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="34a02-185">**ICM \_ Zeichnen von \_ changepalette**</span><span class="sxs-lookup"><span data-stu-id="34a02-185">**ICM\_DRAW\_CHANGEPALETTE**</span></span>](icm-draw-changepalette.md)
-   [<span data-ttu-id="34a02-186">**ICM \_ Draw \_ renderbuffer**</span><span class="sxs-lookup"><span data-stu-id="34a02-186">**ICM\_DRAW\_RENDERBUFFER**</span></span>](icm-draw-renderbuffer.md)

## <a name="related-topics"></a><span data-ttu-id="34a02-187">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34a02-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34a02-188">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="34a02-188">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 




