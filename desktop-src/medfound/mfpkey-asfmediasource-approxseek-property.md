---
description: Gibt an, ob die ASF-Medienquelle die ungefähre Suche verwendet.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: MFPKEY_ASFMediaSource_ApproxSeek-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106349774"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a><span data-ttu-id="fb2af-103">Mfpkey \_ asfmediasource \_ approxseek (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fb2af-103">MFPKEY\_ASFMediaSource\_ApproxSeek property</span></span>

<span data-ttu-id="fb2af-104">Gibt an, ob die ASF-Medienquelle die ungefähre Suche verwendet.</span><span class="sxs-lookup"><span data-stu-id="fb2af-104">Specifies whether the ASF media source uses approximate seeking.</span></span>



<span data-ttu-id="fb2af-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fb2af-105">Data type</span></span>

<span data-ttu-id="fb2af-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="fb2af-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="fb2af-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="fb2af-107">PROPVARIANT member</span></span>

<span data-ttu-id="fb2af-108">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="fb2af-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="fb2af-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="fb2af-109">VT\_BOOL</span></span>

<span data-ttu-id="fb2af-110">**Boolesche Werte**</span><span class="sxs-lookup"><span data-stu-id="fb2af-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="fb2af-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb2af-111">Remarks</span></span>

<span data-ttu-id="fb2af-112">Anwendungen können diese Eigenschaft verwenden, um die ASF-Medienquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fb2af-112">Applications can use this property to configure the ASF media source.</span></span> <span data-ttu-id="fb2af-113">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="fb2af-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="fb2af-114">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="fb2af-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="fb2af-115">Die ASF-Medienquelle behandelt die Suche wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fb2af-115">The ASF media source handles seeking as follows:</span></span>

-   <span data-ttu-id="fb2af-116">Wenn der Wert dieser Eigenschaft **Variant \_ true** ist, verwendet die Medienquelle die ungefähre Suche, die weniger genau, aber schneller als die genaue Suche ist.</span><span class="sxs-lookup"><span data-stu-id="fb2af-116">If the value of this property is **VARIANT\_TRUE**, the media source uses approximate seeking, which is less accurate but faster than exact seeking.</span></span>
-   <span data-ttu-id="fb2af-117">Wenn der Wert **Variant \_ false** ist und die ASF-Datei über einen Index verfügt, verwendet die Medienquelle die genaue Suche.</span><span class="sxs-lookup"><span data-stu-id="fb2af-117">If the value is **VARIANT\_FALSE** and the ASF file has an index, the media source uses exact seeking.</span></span>
-   <span data-ttu-id="fb2af-118">Wenn die ASF-Datei keinen Index enthält, verwendet die Medienquelle die approxmate-Suche, es sei denn, die Eigenschaft " [mfpkey \_ asfmediasource \_ iterativeseekifnoindex](mfpkey-asfmediasource-iterativeseekifnoindex.md) " ist auf **Variant \_ true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb2af-118">If the ASF file does not contain an index, the media source uses approxmate seeking unless the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is set to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="fb2af-119">Wenn die ASF-Datei keinen Index enthält und die Eigenschaft [mfpkey \_ asfmediasource \_ iterativeseekifnoindex](mfpkey-asfmediasource-iterativeseekifnoindex.md) den Wert **Variant \_ true** hat, verwendet die Medienquelle iteratives suchen.</span><span class="sxs-lookup"><span data-stu-id="fb2af-119">If the ASF file does not contain an index and the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is **VARIANT\_TRUE**, the media source uses iterative seeking.</span></span> <span data-ttu-id="fb2af-120">Das iterative suchen ist präziser, aber langsamer als die ungefähre Suche (in der Regel weniger genau als bei der exakten Suche).</span><span class="sxs-lookup"><span data-stu-id="fb2af-120">Iterative seeking is more accurate but slower than approximate seeking (but generally less accurate than exact seeking).</span></span>
    > [!Note]  
    > <span data-ttu-id="fb2af-121">Erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb2af-121">Requires Windows 7.</span></span>

     

<span data-ttu-id="fb2af-122">Der Standardwert dieser Eigenschaft ist **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="fb2af-122">The default value of this property is **VARIANT\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb2af-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb2af-123">Requirements</span></span>



| <span data-ttu-id="fb2af-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb2af-124">Requirement</span></span> | <span data-ttu-id="fb2af-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fb2af-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2af-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb2af-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fb2af-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb2af-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fb2af-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb2af-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fb2af-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb2af-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fb2af-130">Header</span><span class="sxs-lookup"><span data-stu-id="fb2af-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb2af-131"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb2af-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb2af-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb2af-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb2af-133">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb2af-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




