---
description: Enthält den symbolischen Link für eine hardwarebasierte Media Foundation Transformation (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: MFT_ENUM_HARDWARE_URL_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215417"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a><span data-ttu-id="2b41d-103">Attribut Attribut für MFT-Aufzählungs \_ \_ Hardware- \_ URL \_</span><span class="sxs-lookup"><span data-stu-id="2b41d-103">MFT\_ENUM\_HARDWARE\_URL\_Attribute attribute</span></span>

<span data-ttu-id="2b41d-104">Enthält den symbolischen Link für eine hardwarebasierte Media Foundation Transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="2b41d-104">Contains the symbolic link for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="2b41d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2b41d-105">Data type</span></span>

<span data-ttu-id="2b41d-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="2b41d-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="2b41d-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="2b41d-107">Get/set</span></span>

<span data-ttu-id="2b41d-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="2b41d-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="2b41d-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2b41d-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="2b41d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b41d-110">Remarks</span></span>

<span data-ttu-id="2b41d-111">Dieses Attribut wird von hardwarebasierten MFTs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b41d-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="2b41d-112">Der Wert des-Attributs ist die symbolische Verknüpfung für den Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="2b41d-112">The value of the attribute is the symbolic link for the device driver.</span></span> <span data-ttu-id="2b41d-113">Dieses Attribut wird auch für die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festgelegt, die von der [**msumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zugewiesen werden, wenn diese Zeiger hardwarebasierte MFTs darstellen.</span><span class="sxs-lookup"><span data-stu-id="2b41d-113">This attribute is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="2b41d-114">Die symbolische Verknüpfung sollte als nicht transparente Zeichenfolge betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="2b41d-114">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="2b41d-115">Um den anzeigen Amen für ein Gerät zu erhalten, Fragen Sie das MFT-Attribut " [ \_ Friendly \_ Name](mft-friendly-name-attribute.md) " ab.</span><span class="sxs-lookup"><span data-stu-id="2b41d-115">To get the display name for a device, query the [MFT\_FRIENDLY\_NAME](mft-friendly-name-attribute.md) attribute.</span></span>

<span data-ttu-id="2b41d-116">Für Software-MFTs sollte dieses Attribut nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2b41d-116">Software MFTs should not have this attribute set.</span></span>

<span data-ttu-id="2b41d-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="2b41d-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b41d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b41d-118">Requirements</span></span>



| <span data-ttu-id="2b41d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b41d-119">Requirement</span></span> | <span data-ttu-id="2b41d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2b41d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b41d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b41d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b41d-122">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2b41d-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="2b41d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b41d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b41d-124">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2b41d-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2b41d-125">Header</span><span class="sxs-lookup"><span data-stu-id="2b41d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b41d-126"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="2b41d-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b41d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b41d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b41d-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="2b41d-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2b41d-129">Hardware-MFTs</span><span class="sxs-lookup"><span data-stu-id="2b41d-129">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="2b41d-130">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="2b41d-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




