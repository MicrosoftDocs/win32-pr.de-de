---
description: Ermöglicht dem erweiterten Videorenderer (EVR), seine Ausgabe auf die GPU-Bandbreite zu begrenzen.
ms.assetid: d591af2e-d47d-4220-a4f6-968f2ac45284
title: EVRConfig_AllowDropToThrottle-Attribut (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97cbab6fae6644b3c0187d09edb59ab2538012e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041548"
---
# <a name="evrconfig_allowdroptothrottle-attribute"></a><span data-ttu-id="b2470-103">Evrconfig \_ allowdropto Throttle-Attribut</span><span class="sxs-lookup"><span data-stu-id="b2470-103">EVRConfig\_AllowDropToThrottle attribute</span></span>

<span data-ttu-id="b2470-104">Ermöglicht dem erweiterten Videorenderer (EVR), seine Ausgabe auf die GPU-Bandbreite zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="b2470-104">Allows the Enhanced Video Renderer (EVR) to limit its output to match GPU bandwidth.</span></span>

## <a name="data-type"></a><span data-ttu-id="b2470-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b2470-105">Data type</span></span>

<span data-ttu-id="b2470-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b2470-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b2470-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="b2470-107">Get/set</span></span>

<span data-ttu-id="b2470-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b2470-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b2470-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b2470-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2470-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2470-110">Remarks</span></span>

<span data-ttu-id="b2470-111">Dieses Attribut kann in der EVR-Medien Senke festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b2470-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="b2470-112">Zum Festlegen des-Attributs verwenden Sie **QueryInterface** , um die EVR-Medien Senke für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle abzufragen.</span><span class="sxs-lookup"><span data-stu-id="b2470-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="b2470-113">Das Festlegen dieses Attributs hat dieselbe Auswirkung wie das Festlegen des Attributs " **MF videorenderprefs \_ allowoutputthrottelt** " für den EVR.</span><span class="sxs-lookup"><span data-stu-id="b2470-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_AllowOutputThrottling** flag on the EVR.</span></span> <span data-ttu-id="b2470-114">Eine Beschreibung dieses Flags finden Sie unter [**MF videorenderprefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .</span><span class="sxs-lookup"><span data-stu-id="b2470-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="b2470-115">Die GUID-Konstante für dieses Attribut wird aus "straumiids. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="b2470-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2470-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2470-116">Requirements</span></span>



| <span data-ttu-id="b2470-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2470-117">Requirement</span></span> | <span data-ttu-id="b2470-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b2470-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2470-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2470-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2470-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2470-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b2470-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2470-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2470-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2470-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b2470-123">Header</span><span class="sxs-lookup"><span data-stu-id="b2470-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2470-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2470-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2470-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2470-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2470-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b2470-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2470-127">EVR-Attribute</span><span class="sxs-lookup"><span data-stu-id="b2470-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2470-128">Video Qualitäts Verwaltung</span><span class="sxs-lookup"><span data-stu-id="b2470-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




