---
title: Audiokomprimierungs Funktionen
description: Audiokomprimierungs Funktionen
ms.assetid: da207a50-9c67-4cf3-920b-5878637060db
keywords:
- Multimedia-Audiofunktionen, ACM-Funktionen
- Audiofunktionen, ACM-Funktionen
- Audiokomprimierungs-Manager (ACM), Funktionen
- ACM (Audiokomprimierungs-Manager), Funktionen
- ACM-Referenz, Funktionen
- Referenz für ACM, Funktionen
- ACM-Funktionen
- Audiokomprimierung, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a495e52e404d04955a2c330729ef82cccb726554
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314756"
---
# <a name="audio-compression-functions"></a><span data-ttu-id="e585b-111">Audiokomprimierungs Funktionen</span><span class="sxs-lookup"><span data-stu-id="e585b-111">Audio Compression Functions</span></span>

<span data-ttu-id="e585b-112">Die folgenden Funktionen werden bei der Audiokomprimierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e585b-112">The following functions are used with audio compression.</span></span>

-   [<span data-ttu-id="e585b-113">**acmdriveradd**</span><span class="sxs-lookup"><span data-stu-id="e585b-113">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="e585b-114">**acmdriverclose**</span><span class="sxs-lookup"><span data-stu-id="e585b-114">**acmDriverClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverclose)
-   [<span data-ttu-id="e585b-115">**acmdriverdetails**</span><span class="sxs-lookup"><span data-stu-id="e585b-115">**acmDriverDetails**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverdetails)
-   [<span data-ttu-id="e585b-116">**acmdriverenum**</span><span class="sxs-lookup"><span data-stu-id="e585b-116">**acmDriverEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum)
-   [<span data-ttu-id="e585b-117">**acmdriverenumcallback**</span><span class="sxs-lookup"><span data-stu-id="e585b-117">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="e585b-118">**acmdriverid**</span><span class="sxs-lookup"><span data-stu-id="e585b-118">**acmDriverID**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverid)
-   [<span data-ttu-id="e585b-119">**acmdrivermessage**</span><span class="sxs-lookup"><span data-stu-id="e585b-119">**acmDriverMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdrivermessage)
-   [<span data-ttu-id="e585b-120">**acmdriveropen**</span><span class="sxs-lookup"><span data-stu-id="e585b-120">**acmDriverOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveropen)
-   [<span data-ttu-id="e585b-121">**acmdriverpriority**</span><span class="sxs-lookup"><span data-stu-id="e585b-121">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="e585b-122">**acmdriverproc**</span><span class="sxs-lookup"><span data-stu-id="e585b-122">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)
-   [<span data-ttu-id="e585b-123">**acmdriverremove**</span><span class="sxs-lookup"><span data-stu-id="e585b-123">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)
-   [<span data-ttu-id="e585b-124">**acmfilterchoose**</span><span class="sxs-lookup"><span data-stu-id="e585b-124">**acmFilterChoose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose)
-   [<span data-ttu-id="e585b-125">**acmfilterchooabhuokproc**</span><span class="sxs-lookup"><span data-stu-id="e585b-125">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="e585b-126">**acmfilterdetails**</span><span class="sxs-lookup"><span data-stu-id="e585b-126">**acmFilterDetails**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfilterdetails)
-   [<span data-ttu-id="e585b-127">**acmfilteraufzählung**</span><span class="sxs-lookup"><span data-stu-id="e585b-127">**acmFilterEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfilterenum)
-   [<span data-ttu-id="e585b-128">**acmfilterenumcallback**</span><span class="sxs-lookup"><span data-stu-id="e585b-128">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="e585b-129">**acmfiltertagdetails**</span><span class="sxs-lookup"><span data-stu-id="e585b-129">**acmFilterTagDetails**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagdetails)
-   [<span data-ttu-id="e585b-130">**acmfiltertagenum**</span><span class="sxs-lookup"><span data-stu-id="e585b-130">**acmFilterTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagenum)
-   [<span data-ttu-id="e585b-131">**acmfiltertagenumschlag**</span><span class="sxs-lookup"><span data-stu-id="e585b-131">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [<span data-ttu-id="e585b-132">**acmformatchoose**</span><span class="sxs-lookup"><span data-stu-id="e585b-132">**acmFormatChoose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose)
-   [<span data-ttu-id="e585b-133">**acmformatchooabhuokproc**</span><span class="sxs-lookup"><span data-stu-id="e585b-133">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)
-   [<span data-ttu-id="e585b-134">**acmformatdetails**</span><span class="sxs-lookup"><span data-stu-id="e585b-134">**acmFormatDetails**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatdetails)
-   [<span data-ttu-id="e585b-135">**acmformaterum**</span><span class="sxs-lookup"><span data-stu-id="e585b-135">**acmFormatEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatenum)
-   [<span data-ttu-id="e585b-136">**acmformatenumcallback**</span><span class="sxs-lookup"><span data-stu-id="e585b-136">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="e585b-137">**acmformatvorschlagen**</span><span class="sxs-lookup"><span data-stu-id="e585b-137">**acmFormatSuggest**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest)
-   [<span data-ttu-id="e585b-138">**acmformattagdetails**</span><span class="sxs-lookup"><span data-stu-id="e585b-138">**acmFormatTagDetails**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformattagdetails)
-   [<span data-ttu-id="e585b-139">**acmformattagenum**</span><span class="sxs-lookup"><span data-stu-id="e585b-139">**acmFormatTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformattagenum)
-   [<span data-ttu-id="e585b-140">**acmformattagenumschlag**</span><span class="sxs-lookup"><span data-stu-id="e585b-140">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   [<span data-ttu-id="e585b-141">**acmgetversion**</span><span class="sxs-lookup"><span data-stu-id="e585b-141">**acmGetVersion**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmgetversion)
-   [<span data-ttu-id="e585b-142">**acmmetrics**</span><span class="sxs-lookup"><span data-stu-id="e585b-142">**acmMetrics**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmmetrics)
-   [<span data-ttu-id="e585b-143">**acmstreamclose**</span><span class="sxs-lookup"><span data-stu-id="e585b-143">**acmStreamClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)
-   [<span data-ttu-id="e585b-144">**acmStreamConvert**</span><span class="sxs-lookup"><span data-stu-id="e585b-144">**acmStreamConvert**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)
-   <span data-ttu-id="e585b-145">[**acmstreamconvertcallback**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e585b-145">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>
-   [<span data-ttu-id="e585b-146">**acmstreammessage**</span><span class="sxs-lookup"><span data-stu-id="e585b-146">**acmStreamMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreammessage)
-   [<span data-ttu-id="e585b-147">**acmstreamopen**</span><span class="sxs-lookup"><span data-stu-id="e585b-147">**acmStreamOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)
-   [<span data-ttu-id="e585b-148">**acmStreamPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="e585b-148">**acmStreamPrepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)
-   [<span data-ttu-id="e585b-149">**acmstreamreset**</span><span class="sxs-lookup"><span data-stu-id="e585b-149">**acmStreamReset**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamreset)
-   [<span data-ttu-id="e585b-150">**acmstreamsize**</span><span class="sxs-lookup"><span data-stu-id="e585b-150">**acmStreamSize**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)
-   [<span data-ttu-id="e585b-151">**acmstreamunprepareheader**</span><span class="sxs-lookup"><span data-stu-id="e585b-151">**acmStreamUnprepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)

## <a name="related-topics"></a><span data-ttu-id="e585b-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e585b-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e585b-153">Referenz zum Audiokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="e585b-153">Audio Compression Manager Reference</span></span>](audio-compression-manager-reference.md)
</dt> </dl>

 

 