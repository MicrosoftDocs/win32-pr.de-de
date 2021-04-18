---
description: Enthält den anzeigen Amen für eine hardwarebasierte Media Foundation Transformation (MFT).
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: MFT_FRIENDLY_NAME_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33417fd30f4d856ce7306fbbbd492fa29575f7ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343809"
---
# <a name="mft_friendly_name_attribute-attribute"></a><span data-ttu-id="8c7ee-103">Attribut Attribut für MFT-Anzeige \_ \_ Name \_</span><span class="sxs-lookup"><span data-stu-id="8c7ee-103">MFT\_FRIENDLY\_NAME\_Attribute attribute</span></span>

<span data-ttu-id="8c7ee-104">Enthält den anzeigen Amen für eine hardwarebasierte Media Foundation Transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="8c7ee-104">Contains the display name for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="8c7ee-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8c7ee-105">Data type</span></span>

<span data-ttu-id="8c7ee-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="8c7ee-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="8c7ee-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="8c7ee-107">Get/set</span></span>

<span data-ttu-id="8c7ee-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="8c7ee-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="8c7ee-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8c7ee-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="8c7ee-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c7ee-110">Remarks</span></span>

<span data-ttu-id="8c7ee-111">Dieses Attribut wird von hardwarebasierten MFTs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8c7ee-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="8c7ee-112">Sie wird auch für die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festgelegt, die von der [**msumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zugewiesen werden, wenn diese Zeiger hardwarebasierte MFTs darstellen.</span><span class="sxs-lookup"><span data-stu-id="8c7ee-112">It is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="8c7ee-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="8c7ee-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c7ee-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c7ee-114">Requirements</span></span>



| <span data-ttu-id="8c7ee-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c7ee-115">Requirement</span></span> | <span data-ttu-id="8c7ee-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8c7ee-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c7ee-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c7ee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c7ee-118">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8c7ee-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="8c7ee-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c7ee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c7ee-120">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8c7ee-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8c7ee-121">Header</span><span class="sxs-lookup"><span data-stu-id="8c7ee-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c7ee-122"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="8c7ee-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c7ee-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c7ee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c7ee-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="8c7ee-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8c7ee-125">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="8c7ee-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




