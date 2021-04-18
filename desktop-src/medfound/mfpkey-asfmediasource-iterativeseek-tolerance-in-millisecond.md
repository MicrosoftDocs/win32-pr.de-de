---
description: Legt die Toleranz (in Millisekunden) fest, die verwendet wird, wenn die ASF-Medienquelle iterative Suchvorgänge ausführt.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106351846"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a><span data-ttu-id="1e967-103">Mfpkey \_ asfmediasource \_ iterativeseek \_ Tolerance \_ in \_ millisecond (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1e967-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond property</span></span>

<span data-ttu-id="1e967-104">Legt die Toleranz (in Millisekunden) fest, die verwendet wird, wenn die ASF-Medienquelle iterative Suchvorgänge ausführt.</span><span class="sxs-lookup"><span data-stu-id="1e967-104">Sets the tolerance, in milliseconds, that is used when the ASF media source performs iterative seeking.</span></span>



<span data-ttu-id="1e967-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1e967-105">Data type</span></span>

<span data-ttu-id="1e967-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="1e967-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1e967-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="1e967-107">PROPVARIANT member</span></span>

<span data-ttu-id="1e967-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="1e967-108">**ULONG**</span></span>

<span data-ttu-id="1e967-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="1e967-109">VT\_UI4</span></span>

<span data-ttu-id="1e967-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="1e967-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1e967-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e967-111">Remarks</span></span>

<span data-ttu-id="1e967-112">Verwenden Sie diese Eigenschaft, um die ASF-Medienquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1e967-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="1e967-113">Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="1e967-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="1e967-114">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="1e967-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="1e967-115">Diese Eigenschaft gilt nur, wenn iteratives suchen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1e967-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="1e967-116">Weitere Informationen finden Sie unter [mfpkey \_ asfmediasource \_ iterativeseekifnoindex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="1e967-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="1e967-117">Der iterative Suchalgorithmus stoppt, wenn er ein Paket findet, dessen Abstand von der Suchzeit innerhalb der angegebenen Toleranz liegt.</span><span class="sxs-lookup"><span data-stu-id="1e967-117">The iterative seeking algorithm halts if it finds a packet whose distance from the seek time is within the specified tolerance.</span></span> <span data-ttu-id="1e967-118">Der Standardwert ist 8000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="1e967-118">The default value is 8000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e967-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e967-119">Requirements</span></span>



| <span data-ttu-id="1e967-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e967-120">Requirement</span></span> | <span data-ttu-id="1e967-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1e967-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e967-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e967-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1e967-123">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1e967-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1e967-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e967-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1e967-125">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1e967-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1e967-126">Header</span><span class="sxs-lookup"><span data-stu-id="1e967-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e967-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e967-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e967-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e967-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e967-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e967-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




