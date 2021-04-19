---
description: Legt die maximale Anzahl von Such Iterationen fest, die von der ASF-Medienquelle beim Ausführen iterativer Suchvorgänge verwendet werden.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: MFPKEY_ASFMediaSource_IterativeSeek_Max_Count-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354279"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a><span data-ttu-id="dd1b0-103">Mfpkey \_ asfmediasource \_ iterativeseek \_ Max \_ count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dd1b0-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count property</span></span>

<span data-ttu-id="dd1b0-104">Legt die maximale Anzahl von Such Iterationen fest, die von der ASF-Medienquelle beim Ausführen iterativer Suchvorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-104">Sets the maximum number of search iterations the ASF media source will use when it performs iterative seeking.</span></span>



<span data-ttu-id="dd1b0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="dd1b0-105">Data type</span></span>

<span data-ttu-id="dd1b0-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="dd1b0-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="dd1b0-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="dd1b0-107">PROPVARIANT member</span></span>

<span data-ttu-id="dd1b0-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="dd1b0-108">**ULONG**</span></span>

<span data-ttu-id="dd1b0-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="dd1b0-109">VT\_UI4</span></span>

<span data-ttu-id="dd1b0-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="dd1b0-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="dd1b0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd1b0-111">Remarks</span></span>

<span data-ttu-id="dd1b0-112">Verwenden Sie diese Eigenschaft, um die ASF-Medienquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="dd1b0-113">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="dd1b0-114">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="dd1b0-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="dd1b0-115">Diese Eigenschaft gilt nur, wenn iteratives suchen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="dd1b0-116">Weitere Informationen finden Sie unter [mfpkey \_ asfmediasource \_ iterativeseekifnoindex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="dd1b0-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="dd1b0-117">Der gültige Bereich dieser Eigenschaft ist \[ 1-10 ( \] einschließlich).</span><span class="sxs-lookup"><span data-stu-id="dd1b0-117">The valid range of this property is \[1-10\], inclusive.</span></span> <span data-ttu-id="dd1b0-118">Bei einer höheren Zahl ist das iterative suchen tendenziell genauer, dauert jedoch länger.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-118">With a higher number, iterative seeking tends to be more accurate but takes longer.</span></span>

<span data-ttu-id="dd1b0-119">Der Standardwert ist 5.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-119">The default value is 5.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd1b0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd1b0-120">Requirements</span></span>



| <span data-ttu-id="dd1b0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd1b0-121">Requirement</span></span> | <span data-ttu-id="dd1b0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="dd1b0-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1b0-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd1b0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dd1b0-124">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="dd1b0-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="dd1b0-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd1b0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dd1b0-126">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="dd1b0-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="dd1b0-127">Header</span><span class="sxs-lookup"><span data-stu-id="dd1b0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd1b0-128"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd1b0-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd1b0-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd1b0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd1b0-130">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dd1b0-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




