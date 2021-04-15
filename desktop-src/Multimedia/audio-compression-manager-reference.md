---
title: Referenz zum Audiokomprimierungs-Manager
description: Referenz zum Audiokomprimierungs-Manager
ms.assetid: a4e234c7-4dd3-4269-90a5-5de2c8837c0f
keywords:
- Windows-Multimedia, ACM-Referenz
- Multimedia, ACM-Referenz
- Multimedia-Audiodatei, ACM-Referenz
- Audiodatei, ACM-Referenz)
- Audiokomprimierungs-Manager (ACM), Referenz
- ACM (Audiokomprimierungs-Manager), Referenz
- ACM-Referenz, Informationen zu
- Referenz für ACM, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d365b0a69ecd94a07811b24762aa4bffdc8c9f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516721"
---
# <a name="audio-compression-manager-reference"></a><span data-ttu-id="649d4-111">Referenz zum Audiokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="649d4-111">Audio Compression Manager Reference</span></span>

<span data-ttu-id="649d4-112">In diesem Abschnitt werden die Funktionen, Strukturen und Meldungen beschrieben, die dem ACM zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="649d4-112">This section describes the functions, structures, and messages associated with the ACM.</span></span> <span data-ttu-id="649d4-113">Diese Elemente werden wie folgt gruppiert.</span><span class="sxs-lookup"><span data-stu-id="649d4-113">These elements are grouped as follows.</span></span>

## <a name="drivers"></a><span data-ttu-id="649d4-114">Treiber</span><span class="sxs-lookup"><span data-stu-id="649d4-114">Drivers</span></span>

-   [<span data-ttu-id="649d4-115">**acmdriveradd**</span><span class="sxs-lookup"><span data-stu-id="649d4-115">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="649d4-116">**acmdriverclose**</span><span class="sxs-lookup"><span data-stu-id="649d4-116">**acmDriverClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverclose)
-   [<span data-ttu-id="649d4-117">**Acmdriverdetails**</span><span class="sxs-lookup"><span data-stu-id="649d4-117">**ACMDRIVERDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmdriverdetails)
-   [<span data-ttu-id="649d4-118">**acmdriverenum**</span><span class="sxs-lookup"><span data-stu-id="649d4-118">**acmDriverEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum)
-   [<span data-ttu-id="649d4-119">**acmdriverenumcallback**</span><span class="sxs-lookup"><span data-stu-id="649d4-119">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="649d4-120">**acmdriverid**</span><span class="sxs-lookup"><span data-stu-id="649d4-120">**acmDriverID**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverid)
-   [<span data-ttu-id="649d4-121">**acmdrivermessage**</span><span class="sxs-lookup"><span data-stu-id="649d4-121">**acmDriverMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdrivermessage)
-   [<span data-ttu-id="649d4-122">**acmdriveropen**</span><span class="sxs-lookup"><span data-stu-id="649d4-122">**acmDriverOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveropen)
-   [<span data-ttu-id="649d4-123">**acmdriverpriority**</span><span class="sxs-lookup"><span data-stu-id="649d4-123">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="649d4-124">**acmdriverproc**</span><span class="sxs-lookup"><span data-stu-id="649d4-124">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)
-   [<span data-ttu-id="649d4-125">**acmdriverremove**</span><span class="sxs-lookup"><span data-stu-id="649d4-125">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

## <a name="filters"></a><span data-ttu-id="649d4-126">Filter</span><span class="sxs-lookup"><span data-stu-id="649d4-126">Filters</span></span>

-   [<span data-ttu-id="649d4-127">**Acmfilterchoose**</span><span class="sxs-lookup"><span data-stu-id="649d4-127">**ACMFILTERCHOOSE**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfilterchoose)
-   [<span data-ttu-id="649d4-128">**acmfilterchooabhuokproc**</span><span class="sxs-lookup"><span data-stu-id="649d4-128">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="649d4-129">**Acmfilterdetails**</span><span class="sxs-lookup"><span data-stu-id="649d4-129">**ACMFILTERDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfilterdetails)
-   [<span data-ttu-id="649d4-130">**acmfilteraufzählung**</span><span class="sxs-lookup"><span data-stu-id="649d4-130">**acmFilterEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfilterenum)
-   [<span data-ttu-id="649d4-131">**acmfilterenumcallback**</span><span class="sxs-lookup"><span data-stu-id="649d4-131">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="649d4-132">**Acmfiltertagdetails**</span><span class="sxs-lookup"><span data-stu-id="649d4-132">**ACMFILTERTAGDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfiltertagdetails)
-   [<span data-ttu-id="649d4-133">**acmfiltertagenum**</span><span class="sxs-lookup"><span data-stu-id="649d4-133">**acmFilterTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagenum)
-   [<span data-ttu-id="649d4-134">**acmfiltertagenumschlag**</span><span class="sxs-lookup"><span data-stu-id="649d4-134">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)

## <a name="formats"></a><span data-ttu-id="649d4-135">Formate</span><span class="sxs-lookup"><span data-stu-id="649d4-135">Formats</span></span>

-   [<span data-ttu-id="649d4-136">**Acmformatchoose**</span><span class="sxs-lookup"><span data-stu-id="649d4-136">**ACMFORMATCHOOSE**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformatchoose)
-   [<span data-ttu-id="649d4-137">**acmformatchooabhuokproc**</span><span class="sxs-lookup"><span data-stu-id="649d4-137">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)
-   [<span data-ttu-id="649d4-138">**Acmformatdetails**</span><span class="sxs-lookup"><span data-stu-id="649d4-138">**ACMFORMATDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformatdetails)
-   [<span data-ttu-id="649d4-139">**acmformaterum**</span><span class="sxs-lookup"><span data-stu-id="649d4-139">**acmFormatEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatenum)
-   [<span data-ttu-id="649d4-140">**acmformatenumcallback**</span><span class="sxs-lookup"><span data-stu-id="649d4-140">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="649d4-141">**acmformatvorschlagen**</span><span class="sxs-lookup"><span data-stu-id="649d4-141">**acmFormatSuggest**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest)
-   [<span data-ttu-id="649d4-142">**Acmformattagdetails**</span><span class="sxs-lookup"><span data-stu-id="649d4-142">**ACMFORMATTAGDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformattagdetails)
-   [<span data-ttu-id="649d4-143">**acmformattagenum**</span><span class="sxs-lookup"><span data-stu-id="649d4-143">**acmFormatTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformattagenum)
-   [<span data-ttu-id="649d4-144">**acmformattagenumschlag**</span><span class="sxs-lookup"><span data-stu-id="649d4-144">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)

## <a name="messages"></a><span data-ttu-id="649d4-145">Meldungen</span><span class="sxs-lookup"><span data-stu-id="649d4-145">Messages</span></span>

-   [<span data-ttu-id="649d4-146">**MM \_ ACM \_ filterchoose**</span><span class="sxs-lookup"><span data-stu-id="649d4-146">**MM\_ACM\_FILTERCHOOSE**</span></span>](mm-acm-filterchoose.md)
-   [<span data-ttu-id="649d4-147">**MM \_ ACM \_ formatchoose**</span><span class="sxs-lookup"><span data-stu-id="649d4-147">**MM\_ACM\_FORMATCHOOSE**</span></span>](mm-acm-formatchoose.md)

## <a name="streams"></a><span data-ttu-id="649d4-148">Datenströme</span><span class="sxs-lookup"><span data-stu-id="649d4-148">Streams</span></span>

-   [<span data-ttu-id="649d4-149">**acmstreamclose**</span><span class="sxs-lookup"><span data-stu-id="649d4-149">**acmStreamClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)
-   [<span data-ttu-id="649d4-150">**acmStreamConvert**</span><span class="sxs-lookup"><span data-stu-id="649d4-150">**acmStreamConvert**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)
-   <span data-ttu-id="649d4-151">[**acmstreamconvertcallback**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="649d4-151">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>
-   [<span data-ttu-id="649d4-152">**ACMSTREAMHEADER**</span><span class="sxs-lookup"><span data-stu-id="649d4-152">**ACMSTREAMHEADER**</span></span>](/windows/win32/api/msacm/ns-msacm-acmstreamheader)
-   [<span data-ttu-id="649d4-153">**acmstreammessage**</span><span class="sxs-lookup"><span data-stu-id="649d4-153">**acmStreamMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreammessage)
-   [<span data-ttu-id="649d4-154">**acmstreamopen**</span><span class="sxs-lookup"><span data-stu-id="649d4-154">**acmStreamOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)
-   [<span data-ttu-id="649d4-155">**acmStreamPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="649d4-155">**acmStreamPrepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)
-   [<span data-ttu-id="649d4-156">**acmstreamreset**</span><span class="sxs-lookup"><span data-stu-id="649d4-156">**acmStreamReset**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamreset)
-   [<span data-ttu-id="649d4-157">**acmstreamsize**</span><span class="sxs-lookup"><span data-stu-id="649d4-157">**acmStreamSize**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)
-   [<span data-ttu-id="649d4-158">**acmstreamunprepareheader**</span><span class="sxs-lookup"><span data-stu-id="649d4-158">**acmStreamUnprepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)

## <a name="miscellaneous"></a><span data-ttu-id="649d4-159">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="649d4-159">Miscellaneous</span></span>

-   [<span data-ttu-id="649d4-160">**acmgetversion**</span><span class="sxs-lookup"><span data-stu-id="649d4-160">**acmGetVersion**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmgetversion)
-   [<span data-ttu-id="649d4-161">**acmmetrics**</span><span class="sxs-lookup"><span data-stu-id="649d4-161">**acmMetrics**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmmetrics)

## <a name="related-topics"></a><span data-ttu-id="649d4-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="649d4-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="649d4-163">Audiokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="649d4-163">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> </dl>

 

 