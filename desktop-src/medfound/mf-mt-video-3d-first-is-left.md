---
description: Gibt für ein 3D-Videoformat an, welche Ansicht die linke Ansicht ist.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: MF_MT_VIDEO_3D_FIRST_IS_LEFT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393789"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a><span data-ttu-id="b3895-103">MF \_ MT \_ \_ -Video 3D \_ erste \_ ist Left- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="b3895-103">MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute</span></span>

<span data-ttu-id="b3895-104">Gibt für ein 3D-Videoformat an, welche Ansicht die linke Ansicht ist.</span><span class="sxs-lookup"><span data-stu-id="b3895-104">For a 3D video format, specifies which view is the left view.</span></span>

## <a name="data-type"></a><span data-ttu-id="b3895-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b3895-105">Data type</span></span>

<span data-ttu-id="b3895-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3895-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b3895-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3895-107">Remarks</span></span>

<span data-ttu-id="b3895-108">Bei 3D-Videos enthält jedes Video Beispiel zwei Ansichten, die als *erste Ansicht* und *zweite Ansicht* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3895-108">For 3D video, each video sample contains two views, which are designated *first view* and *second view*.</span></span> <span data-ttu-id="b3895-109">Das genaue Layout der Ansichten im Arbeitsspeicher wird durch das Format Attribut des " [MF \_ MT \_ \_ -Video 3D \_ ](mf-mt-video-3d-format.md) " angegeben.</span><span class="sxs-lookup"><span data-stu-id="b3895-109">The exact layout of the views in memory is indicated by the [MF\_MT\_VIDEO\_3D\_FORMAT](mf-mt-video-3d-format.md) attribute.</span></span>



| <span data-ttu-id="b3895-110">Format</span><span class="sxs-lookup"><span data-stu-id="b3895-110">Format</span></span>               | <span data-ttu-id="b3895-111">Erste Ansicht</span><span class="sxs-lookup"><span data-stu-id="b3895-111">First View</span></span>              | <span data-ttu-id="b3895-112">Zweite Ansicht</span><span class="sxs-lookup"><span data-stu-id="b3895-112">Second View</span></span>               |
|----------------------|-------------------------|---------------------------|
| <span data-ttu-id="b3895-113">Seite-an-Seite gepackt</span><span class="sxs-lookup"><span data-stu-id="b3895-113">Packed side-by-side</span></span>  | <span data-ttu-id="b3895-114">Linke Hälfte des Puffers</span><span class="sxs-lookup"><span data-stu-id="b3895-114">Left half of the buffer</span></span> | <span data-ttu-id="b3895-115">Rechte Hälfte des Puffers</span><span class="sxs-lookup"><span data-stu-id="b3895-115">Right half of the buffer</span></span>  |
| <span data-ttu-id="b3895-116">Von oben nach unten gepackt</span><span class="sxs-lookup"><span data-stu-id="b3895-116">Packed top-to-bottom</span></span> | <span data-ttu-id="b3895-117">Obere Hälfte des Puffers</span><span class="sxs-lookup"><span data-stu-id="b3895-117">Top half of the buffer</span></span>  | <span data-ttu-id="b3895-118">Untere Hälfte des Puffers</span><span class="sxs-lookup"><span data-stu-id="b3895-118">Bottom half of the buffer</span></span> |
| <span data-ttu-id="b3895-119">MultiView</span><span class="sxs-lookup"><span data-stu-id="b3895-119">Multiview</span></span>            | <span data-ttu-id="b3895-120">Puffer Index 0</span><span class="sxs-lookup"><span data-stu-id="b3895-120">Buffer index 0</span></span>          | <span data-ttu-id="b3895-121">Puffer Index 1</span><span class="sxs-lookup"><span data-stu-id="b3895-121">Buffer index 1</span></span>            |
| <span data-ttu-id="b3895-122">Basis Ansicht</span><span class="sxs-lookup"><span data-stu-id="b3895-122">Base view</span></span>            | <span data-ttu-id="b3895-123">Ganzer Frame</span><span class="sxs-lookup"><span data-stu-id="b3895-123">Entire frame</span></span>            | <span data-ttu-id="b3895-124">Nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="b3895-124">Not present</span></span>               |



 

<span data-ttu-id="b3895-125">Standardmäßig ist die erste Ansicht die linke Ansicht, die zweite Ansicht ist die Rechte Ansicht.</span><span class="sxs-lookup"><span data-stu-id="b3895-125">By default, the first view is the left view, and the second view is the right view.</span></span> <span data-ttu-id="b3895-126">Wenn die linke und die Rechte Ansicht ausgetauscht werden, legen Sie für das MF \_ MT \_ \_ -Video 3D- \_ \_ Attribut erste ist Left- \_ Attribut im Medientyp auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="b3895-126">If the left and right views are swapped, set the MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute to **FALSE** in the media type.</span></span>

> [!Note]  
> <span data-ttu-id="b3895-127">Im Format der *Basis Ansicht* (**MFVideo3DSampleFormat \_ baseview**) wird nur die Basis Ansicht beibehalten, sodass dieses Attribut nicht angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3895-127">In *base view* format (**MFVideo3DSampleFormat\_BaseView**), only the base view is retained, so this attribute does not apply.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b3895-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3895-128">Requirements</span></span>



| <span data-ttu-id="b3895-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3895-129">Requirement</span></span> | <span data-ttu-id="b3895-130">Wert</span><span class="sxs-lookup"><span data-stu-id="b3895-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3895-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3895-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b3895-132">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b3895-132">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b3895-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3895-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b3895-134">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b3895-134">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b3895-135">Header</span><span class="sxs-lookup"><span data-stu-id="b3895-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3895-136"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3895-136"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3895-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3895-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3895-138">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b3895-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




