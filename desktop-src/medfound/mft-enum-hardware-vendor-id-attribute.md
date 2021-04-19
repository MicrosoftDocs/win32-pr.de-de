---
description: Gibt die Hersteller-ID für ein Hardware basiertes Microsoft Media Foundation an.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: MFT_ENUM_HARDWARE_VENDOR_ID_Attribute-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4d92585936e52cbb0b9b65201a5de0d3a02b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353174"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a><span data-ttu-id="97315-103">Attribut Attribut-ID des MFT-Aufzählungs \_ \_ Hardware \_ Herstellers \_ \_</span><span class="sxs-lookup"><span data-stu-id="97315-103">MFT\_ENUM\_HARDWARE\_VENDOR\_ID\_Attribute attribute</span></span>

<span data-ttu-id="97315-104">Gibt die Anbieter-ID für eine hardwarebasierte Microsoft Media Foundation Transformation (MFT) an.</span><span class="sxs-lookup"><span data-stu-id="97315-104">Specifies the vendor ID for a hardware-based Microsoft Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="97315-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="97315-105">Data type</span></span>

<span data-ttu-id="97315-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="97315-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="97315-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="97315-107">Get/set</span></span>

<span data-ttu-id="97315-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="97315-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="97315-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="97315-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="97315-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97315-110">Remarks</span></span>

<span data-ttu-id="97315-111">Dieses Attribut ist informativ und optional.</span><span class="sxs-lookup"><span data-stu-id="97315-111">This attribute is informational and optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="97315-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97315-112">Requirements</span></span>



| <span data-ttu-id="97315-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97315-113">Requirement</span></span> | <span data-ttu-id="97315-114">Wert</span><span class="sxs-lookup"><span data-stu-id="97315-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="97315-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97315-115">Minimum supported client</span></span><br/> | <span data-ttu-id="97315-116">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="97315-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="97315-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97315-117">Minimum supported server</span></span><br/> | <span data-ttu-id="97315-118">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="97315-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="97315-119">Header</span><span class="sxs-lookup"><span data-stu-id="97315-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="97315-120"><dt>"MF Transform. idl"</dt></span><span class="sxs-lookup"><span data-stu-id="97315-120"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97315-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97315-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97315-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="97315-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="97315-123">Hardware-MFTs</span><span class="sxs-lookup"><span data-stu-id="97315-123">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="97315-124">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="97315-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




