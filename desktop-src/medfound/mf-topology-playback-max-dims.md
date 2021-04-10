---
description: Gibt die Größe des Zielfensters für die Videowiedergabe an.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: MF_TOPOLOGY_PLAYBACK_MAX_DIMS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1fc6a57c5e031bc6f35f36e688bd44986f541b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215136"
---
# <a name="mf_topology_playback_max_dims-attribute"></a><span data-ttu-id="228d0-103">Maximal zulässige Anzahl von \_ \_ \_ \_ DiMS-Attributen</span><span class="sxs-lookup"><span data-stu-id="228d0-103">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS attribute</span></span>

<span data-ttu-id="228d0-104">Gibt die Größe des Zielfensters für die Videowiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="228d0-104">Specifies the size of the destination window for video playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="228d0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="228d0-105">Data type</span></span>

<span data-ttu-id="228d0-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="228d0-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="228d0-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="228d0-107">Get/set</span></span>

<span data-ttu-id="228d0-108">Um dieses Attribut abzurufen, nennen Sie [**mfgetattributesize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span><span class="sxs-lookup"><span data-stu-id="228d0-108">To get this attribute, call [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span></span>

<span data-ttu-id="228d0-109">Um dieses Attribut festzulegen, muss [**mfsetattributesize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="228d0-109">To set this attribute, call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span></span>

## <a name="applies-to"></a><span data-ttu-id="228d0-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="228d0-110">Applies to</span></span>

[<span data-ttu-id="228d0-111">**Imftopology**</span><span class="sxs-lookup"><span data-stu-id="228d0-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="228d0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="228d0-112">Remarks</span></span>

<span data-ttu-id="228d0-113">Das topologielader verwendet dieses Attribut, um die Pipeline vor dem Start der Wiedergabe zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="228d0-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="228d0-114">Wenn Sie dieses Attribut festlegen, legen Sie auch das Attribut für die [ \_ \_ statische \_ Wiedergabe \_ der MF-Topologie](mf-topology-static-playback-optimizations.md) auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="228d0-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="228d0-115">Die oberen 32 Bits des Attribut Werts enthalten die Breite, und die unteren 32 Bits enthalten die Höhe, beide in Pixel.</span><span class="sxs-lookup"><span data-stu-id="228d0-115">The upper 32 bits of the attribute value contain the width and the lower 32 bits contain the height, both in pixels.</span></span>

<span data-ttu-id="228d0-116">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="228d0-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="228d0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="228d0-117">Requirements</span></span>



| <span data-ttu-id="228d0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="228d0-118">Requirement</span></span> | <span data-ttu-id="228d0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="228d0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="228d0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="228d0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="228d0-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="228d0-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="228d0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="228d0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="228d0-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="228d0-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="228d0-124">Header</span><span class="sxs-lookup"><span data-stu-id="228d0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="228d0-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="228d0-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="228d0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="228d0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="228d0-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="228d0-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="228d0-128">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="228d0-128">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="228d0-129">Video Qualitäts Verwaltung</span><span class="sxs-lookup"><span data-stu-id="228d0-129">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




