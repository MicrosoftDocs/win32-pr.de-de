---
description: Gibt die Anzahl der Threads an, die vom Encoder verwendet werden.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: MFPKEY_NUMTHREADS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528664"
---
# <a name="mfpkey_numthreads-property"></a><span data-ttu-id="c6512-103">Mfpkey- \_ numThreads (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c6512-103">MFPKEY\_NUMTHREADS Property</span></span>

<span data-ttu-id="c6512-104">Gibt die Anzahl der Threads an, die vom Encoder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6512-104">Specifies the number of threads that the encoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c6512-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c6512-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c6512-106">g \_ wszwmvcnumthreads</span><span class="sxs-lookup"><span data-stu-id="c6512-106">g\_wszWMVCNumThreads</span></span>

## <a name="data-type"></a><span data-ttu-id="c6512-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c6512-107">Data Type</span></span>

<span data-ttu-id="c6512-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c6512-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="c6512-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="c6512-109">Default Value</span></span>

<span data-ttu-id="c6512-110">1</span><span class="sxs-lookup"><span data-stu-id="c6512-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="c6512-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6512-111">Remarks</span></span>

<span data-ttu-id="c6512-112">Dieser Wert soll die Codierung in mehrere Threads aufteilen, um die Vorteile von Computern mit mehreren Prozessoren zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="c6512-112">This value is intended to divide encoding into multiple threads to take advantage of computers with multiple processors.</span></span> <span data-ttu-id="c6512-113">Wenn Codierungs Aufgaben in mehrere Threads aufgeteilt werden, kann dies zu einer geringfügigen Abnahme der Qualität im Vergleich zu einem einzelnen Thread führen.</span><span class="sxs-lookup"><span data-stu-id="c6512-113">Splitting encoding tasks into multiple threads can cause a slight decrease in quality as compared to a single thread.</span></span>

<span data-ttu-id="c6512-114">Für den Video Encoder (wmvencod.dll), der mit Windows XP und Windows Vista veröffentlicht wurde, sollte diese Eigenschaft auf 1, 2 oder 4 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c6512-114">For the video encoder (wmvencod.dll) released with Windows XP and Windows Vista, this property should be set to 1, 2, or 4.</span></span> <span data-ttu-id="c6512-115">Andere Werte werden abgerundet.</span><span class="sxs-lookup"><span data-stu-id="c6512-115">Other values will be rounded down.</span></span>

<span data-ttu-id="c6512-116">Für den Video Encoder (wmvencod.dll), der mit Windows 7 veröffentlicht wurde, sollte diese Eigenschaft auf 1, 2, 4 oder 8 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c6512-116">For the video encoder (wmvencod.dll) released with Windows 7, this property should be set to 1, 2, 4, or 8.</span></span> <span data-ttu-id="c6512-117">Andere Werte werden abgerundet.</span><span class="sxs-lookup"><span data-stu-id="c6512-117">Other values will be rounded down.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6512-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6512-118">Requirements</span></span>



| <span data-ttu-id="c6512-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6512-119">Requirement</span></span> | <span data-ttu-id="c6512-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c6512-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6512-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6512-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c6512-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6512-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c6512-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6512-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c6512-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6512-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6512-125">Header</span><span class="sxs-lookup"><span data-stu-id="c6512-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6512-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6512-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6512-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6512-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6512-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6512-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




