---
description: Erzwingt, dass der erweiterte Videorenderer (EVR) Bob Deinterlacing verwendet.
ms.assetid: 56f808b3-c2eb-46e4-84a1-c478a5db78e7
title: EVRConfig_ForceBob-Attribut (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afeeb1e7fb57f956d378e71ac4452ea2e4f168be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343020"
---
# <a name="evrconfig_forcebob-attribute"></a><span data-ttu-id="5479d-103">Evrconfig \_ forcebob-Attribut</span><span class="sxs-lookup"><span data-stu-id="5479d-103">EVRConfig\_ForceBob attribute</span></span>

<span data-ttu-id="5479d-104">Erzwingt, dass der erweiterte Videorenderer (EVR) Bob Deinterlacing verwendet.</span><span class="sxs-lookup"><span data-stu-id="5479d-104">Forces the Enhanced Video Renderer (EVR) to use bob deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="5479d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5479d-105">Data type</span></span>

<span data-ttu-id="5479d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5479d-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5479d-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="5479d-107">Get/set</span></span>

<span data-ttu-id="5479d-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5479d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5479d-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="5479d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="5479d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5479d-110">Remarks</span></span>

<span data-ttu-id="5479d-111">Dieses Attribut kann in der EVR-Medien Senke festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5479d-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="5479d-112">Zum Festlegen des-Attributs verwenden Sie **QueryInterface** , um die EVR-Medien Senke für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle abzufragen.</span><span class="sxs-lookup"><span data-stu-id="5479d-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="5479d-113">Das Festlegen dieses Attributs hat denselben Effekt wie das Festlegen des **MF videomixprefs \_ forcebob** -Flags für den EVR.</span><span class="sxs-lookup"><span data-stu-id="5479d-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_ForceBob** flag on the EVR.</span></span> <span data-ttu-id="5479d-114">Eine Beschreibung dieses Flags finden Sie unter [**MF videomixprefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .</span><span class="sxs-lookup"><span data-stu-id="5479d-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="5479d-115">Die GUID-Konstante für dieses Attribut wird aus "straumiids. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="5479d-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5479d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5479d-116">Requirements</span></span>



| <span data-ttu-id="5479d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5479d-117">Requirement</span></span> | <span data-ttu-id="5479d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5479d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5479d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5479d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5479d-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5479d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5479d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5479d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5479d-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5479d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5479d-123">Header</span><span class="sxs-lookup"><span data-stu-id="5479d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5479d-124"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5479d-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5479d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5479d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5479d-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5479d-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5479d-127">EVR-Attribute</span><span class="sxs-lookup"><span data-stu-id="5479d-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="5479d-128">Video Qualitäts Verwaltung</span><span class="sxs-lookup"><span data-stu-id="5479d-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




