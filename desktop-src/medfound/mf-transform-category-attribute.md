---
description: Gibt die Kategorie für eine Media Foundation Transformation (MFT) an.
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: MF_TRANSFORM_CATEGORY_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214877"
---
# <a name="mf_transform_category_attribute-attribute"></a><span data-ttu-id="be205-103">\_ \_ Kategorie \_ Attribut Attribut der MF-Transformation</span><span class="sxs-lookup"><span data-stu-id="be205-103">MF\_TRANSFORM\_CATEGORY\_Attribute attribute</span></span>

<span data-ttu-id="be205-104">Gibt die Kategorie für eine Media Foundation Transformation (MFT) an.</span><span class="sxs-lookup"><span data-stu-id="be205-104">Specifies the category for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="be205-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="be205-105">Data type</span></span>

<span data-ttu-id="be205-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="be205-106">**GUID**</span></span>

<span data-ttu-id="be205-107">Eine Liste möglicher Werte finden Sie unter [**MFT \_ Category**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="be205-107">For a list of possible values, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

## <a name="getset"></a><span data-ttu-id="be205-108">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="be205-108">Get/set</span></span>

<span data-ttu-id="be205-109">Um dieses Attribut abzurufen, wenden Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)an.</span><span class="sxs-lookup"><span data-stu-id="be205-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="be205-110">Um dieses Attribut festzulegen, wenden Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)an.</span><span class="sxs-lookup"><span data-stu-id="be205-110">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="be205-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be205-111">Remarks</span></span>

<span data-ttu-id="be205-112">Dieses Attribut wird für die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festgelegt, die von der [**motenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="be205-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="be205-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be205-113">Requirements</span></span>



| <span data-ttu-id="be205-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be205-114">Requirement</span></span> | <span data-ttu-id="be205-115">Wert</span><span class="sxs-lookup"><span data-stu-id="be205-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="be205-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be205-116">Minimum supported client</span></span><br/> | <span data-ttu-id="be205-117">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="be205-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="be205-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be205-118">Minimum supported server</span></span><br/> | <span data-ttu-id="be205-119">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="be205-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="be205-120">Header</span><span class="sxs-lookup"><span data-stu-id="be205-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="be205-121"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="be205-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be205-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be205-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be205-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="be205-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="be205-124">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="be205-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




