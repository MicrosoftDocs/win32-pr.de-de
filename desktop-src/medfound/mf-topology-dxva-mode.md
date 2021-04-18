---
description: Gibt an, ob der topologielader die Microsoft DirectX Video Acceleration (DXVA) in der Topologie aktiviert.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: MF_TOPOLOGY_DXVA_MODE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad75b37a2ca2e971077b05d1bbeb92748530614
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347156"
---
# <a name="mf_topology_dxva_mode-attribute"></a><span data-ttu-id="ad5d1-103">\_ \_ DXVA-Modusattribut der MF-Topologie \_</span><span class="sxs-lookup"><span data-stu-id="ad5d1-103">MF\_TOPOLOGY\_DXVA\_MODE attribute</span></span>

<span data-ttu-id="ad5d1-104">Gibt an, ob der topologielader die Microsoft DirectX Video Acceleration (DXVA) in der Topologie aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ad5d1-104">Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad5d1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ad5d1-105">Data type</span></span>

<span data-ttu-id="ad5d1-106">**[**Mftopology \_ \_**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** Als **UInt32** gespeicherter DXVA-Modus</span><span class="sxs-lookup"><span data-stu-id="ad5d1-106">**[**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ad5d1-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="ad5d1-107">Get/set</span></span>

<span data-ttu-id="ad5d1-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ad5d1-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ad5d1-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ad5d1-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ad5d1-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="ad5d1-110">Applies to</span></span>

[<span data-ttu-id="ad5d1-111">**Imftopology**</span><span class="sxs-lookup"><span data-stu-id="ad5d1-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="ad5d1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad5d1-112">Remarks</span></span>

<span data-ttu-id="ad5d1-113">Der Wert dieses Attributs ist eine Enumerationskonstante für den [**mftopology- \_ DXVA- \_ Modus**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) .</span><span class="sxs-lookup"><span data-stu-id="ad5d1-113">The value of this attribute is an [**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) enumeration constant.</span></span> <span data-ttu-id="ad5d1-114">Der Standardwert ist **mftopology \_ DXVA \_ default**.</span><span class="sxs-lookup"><span data-stu-id="ad5d1-114">The default value is **MFTOPOLOGY\_DXVA\_DEFAULT**.</span></span>

<span data-ttu-id="ad5d1-115">Dieses Attribut steuert, welche MFTs einen Zeiger auf den Direct3D-Geräte-Manager erhalten.</span><span class="sxs-lookup"><span data-stu-id="ad5d1-115">This attribute controls which MFTs receive a pointer to the Direct3D device manager.</span></span> <span data-ttu-id="ad5d1-116">Um die vollständige Videobeschleunigung zu aktivieren, legen Sie den Wert auf **mftopology \_ DXVA \_ Full** fest.</span><span class="sxs-lookup"><span data-stu-id="ad5d1-116">To enable full video acceleration, set the value to **MFTOPOLOGY\_DXVA\_FULL**.</span></span> <span data-ttu-id="ad5d1-117">Der Wert **mftopology \_ DXVA \_ default** ist aus Gründen der Abwärtskompatibilität definiert und entspricht dem Verhalten aller früheren Versionen von Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ad5d1-117">The value **MFTOPOLOGY\_DXVA\_DEFAULT** is defined for backward compatibility; it matches the behavior of all earlier versions of Microsoft Media Foundation.</span></span>

<span data-ttu-id="ad5d1-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ad5d1-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad5d1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad5d1-119">Requirements</span></span>



| <span data-ttu-id="ad5d1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad5d1-120">Requirement</span></span> | <span data-ttu-id="ad5d1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ad5d1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad5d1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad5d1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ad5d1-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad5d1-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ad5d1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad5d1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ad5d1-125">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad5d1-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ad5d1-126">Header</span><span class="sxs-lookup"><span data-stu-id="ad5d1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad5d1-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad5d1-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad5d1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad5d1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad5d1-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ad5d1-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad5d1-130">Direct3D Device Manager</span><span class="sxs-lookup"><span data-stu-id="ad5d1-130">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="ad5d1-131">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="ad5d1-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




