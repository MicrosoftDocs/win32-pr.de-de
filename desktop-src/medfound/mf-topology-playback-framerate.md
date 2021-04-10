---
description: Gibt die Aktualisierungsrate des Monitors an.
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: MF_TOPOLOGY_PLAYBACK_FRAMERATE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215137"
---
# <a name="mf_topology_playback_framerate-attribute"></a><span data-ttu-id="09aef-103">MF- \_ \_ topologiewiedergabe \_ Framerate-Attribut</span><span class="sxs-lookup"><span data-stu-id="09aef-103">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE attribute</span></span>

<span data-ttu-id="09aef-104">Gibt die Aktualisierungsrate des Monitors an.</span><span class="sxs-lookup"><span data-stu-id="09aef-104">Specifies the monitor refresh rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="09aef-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="09aef-105">Data type</span></span>

<span data-ttu-id="09aef-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="09aef-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="09aef-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="09aef-107">Get/set</span></span>

<span data-ttu-id="09aef-108">Um dieses Attribut abzurufen, nennen Sie [**mfgetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="09aef-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="09aef-109">Um dieses Attribut festzulegen, nennen Sie [**mfsetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="09aef-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="applies-to"></a><span data-ttu-id="09aef-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="09aef-110">Applies to</span></span>

[<span data-ttu-id="09aef-111">**Imftopology**</span><span class="sxs-lookup"><span data-stu-id="09aef-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="09aef-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09aef-112">Remarks</span></span>

<span data-ttu-id="09aef-113">Das topologielader verwendet dieses Attribut, um die Pipeline vor dem Start der Wiedergabe zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="09aef-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="09aef-114">Wenn Sie dieses Attribut festlegen, legen Sie auch das Attribut für die [ \_ \_ statische \_ Wiedergabe \_ der MF-Topologie](mf-topology-static-playback-optimizations.md) auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="09aef-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="09aef-115">Die Framerate wird als Verhältnis ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="09aef-115">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="09aef-116">Die oberen 32 Bits des Attribut Werts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner.</span><span class="sxs-lookup"><span data-stu-id="09aef-116">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span>

<span data-ttu-id="09aef-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="09aef-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="09aef-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09aef-118">Requirements</span></span>



| <span data-ttu-id="09aef-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09aef-119">Requirement</span></span> | <span data-ttu-id="09aef-120">Wert</span><span class="sxs-lookup"><span data-stu-id="09aef-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09aef-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09aef-121">Minimum supported client</span></span><br/> | <span data-ttu-id="09aef-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09aef-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="09aef-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09aef-123">Minimum supported server</span></span><br/> | <span data-ttu-id="09aef-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09aef-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="09aef-125">Header</span><span class="sxs-lookup"><span data-stu-id="09aef-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="09aef-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09aef-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09aef-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09aef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09aef-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="09aef-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="09aef-129">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="09aef-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="09aef-130">Video Qualitäts Verwaltung</span><span class="sxs-lookup"><span data-stu-id="09aef-130">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




