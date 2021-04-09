---
description: Enthält die Kategorie-GUID für eine Media Foundation Transformation (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: MFPKEY_CATEGORY-Eigenschaft (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865576"
---
# <a name="mfpkey_category-property"></a><span data-ttu-id="21002-103">Eigenschaft "mfpkey \_ Category"</span><span class="sxs-lookup"><span data-stu-id="21002-103">MFPKEY\_CATEGORY property</span></span>

<span data-ttu-id="21002-104">Enthält die Kategorie-GUID für eine Media Foundation Transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="21002-104">Contains the category GUID for a Media Foundation transform (MFT).</span></span>



<span data-ttu-id="21002-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="21002-105">Data type</span></span>

<span data-ttu-id="21002-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="21002-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="21002-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="21002-107">PROPVARIANT member</span></span>

<span data-ttu-id="21002-108">**GUID** (**CLSID** \* )</span><span class="sxs-lookup"><span data-stu-id="21002-108">**GUID** (**CLSID**\*)</span></span>

<span data-ttu-id="21002-109">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="21002-109">VT\_CLSID</span></span>

<span data-ttu-id="21002-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="21002-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="21002-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21002-111">Remarks</span></span>

<span data-ttu-id="21002-112">Der Wert dieser Eigenschaft ist eine GUID, die die MFT-Kategorie bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="21002-112">The value of this property is a GUID that identifies the MFT category.</span></span> <span data-ttu-id="21002-113">Eine Liste der Kategorien finden Sie unter [**MFT \_ Category**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="21002-113">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

<span data-ttu-id="21002-114">Diese Eigenschaft ist optional und dient nur zu Informationszwecken.</span><span class="sxs-lookup"><span data-stu-id="21002-114">This property is optional and is informational only.</span></span> <span data-ttu-id="21002-115">Eine MFT kann diese Eigenschaft verwenden, um die Kategorie zu melden, in der Sie registriert ist.</span><span class="sxs-lookup"><span data-stu-id="21002-115">An MFT can use this property to report the category under which it is registered.</span></span> <span data-ttu-id="21002-116">Um diese Eigenschaft zu erhalten, Fragen Sie die MFT für die **IPropertyStore** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="21002-116">To get this property, query the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="21002-117">Um eine MFT-Kategorie aufzulisten, müssen Sie die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="21002-117">To enumerate an MFT category, call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function.</span></span> <span data-ttu-id="21002-118">Es gibt keine direkte Verknüpfung zwischen der **MF** -Funktion und dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="21002-118">There is no direct link between the **MFTEnum** function and this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="21002-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21002-119">Requirements</span></span>



| <span data-ttu-id="21002-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21002-120">Requirement</span></span> | <span data-ttu-id="21002-121">Wert</span><span class="sxs-lookup"><span data-stu-id="21002-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21002-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21002-122">Minimum supported client</span></span><br/> | <span data-ttu-id="21002-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21002-123">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="21002-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21002-124">Minimum supported server</span></span><br/> | <span data-ttu-id="21002-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21002-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="21002-126">Header</span><span class="sxs-lookup"><span data-stu-id="21002-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="21002-127"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="21002-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21002-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21002-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21002-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="21002-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="21002-130">Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="21002-130">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




