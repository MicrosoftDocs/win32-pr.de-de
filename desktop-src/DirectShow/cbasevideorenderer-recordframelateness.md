---
description: Mit der recordframellichkeit-Methode wird die Zeit für das Rendering aufgezeichnet und Statistiken für die Eigenschaften Seite gesammelt.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Cbasevideorenderer. recordframel-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359253"
---
# <a name="cbasevideorendererrecordframelateness-method"></a><span data-ttu-id="7d6e1-103">Cbasevideorenderer. recordframel-Methode</span><span class="sxs-lookup"><span data-stu-id="7d6e1-103">CBaseVideoRenderer.RecordFrameLateness method</span></span>

<span data-ttu-id="7d6e1-104">Die `RecordFrameLateness` -Methode zeichnet die Zeit, zu der das Rendering aufgetreten ist, und sammelt Statistiken für die Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="7d6e1-104">The `RecordFrameLateness` method records how timely the rendering occurred and gathers statistics for the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d6e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d6e1-105">Syntax</span></span>


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="7d6e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d6e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d6e1-107">*trlate*</span><span class="sxs-lookup"><span data-stu-id="7d6e1-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6e1-108">Der Wert, der angibt, wie spät das Beispiel in Bezugszeit Einheiten über die Fälligkeits Zeit hinausging.</span><span class="sxs-lookup"><span data-stu-id="7d6e1-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="7d6e1-109">*trframe*</span><span class="sxs-lookup"><span data-stu-id="7d6e1-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6e1-110">Interframe-Zeit in Bezugszeit Einheiten.</span><span class="sxs-lookup"><span data-stu-id="7d6e1-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d6e1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d6e1-111">Return value</span></span>

<span data-ttu-id="7d6e1-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7d6e1-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d6e1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d6e1-113">Requirements</span></span>



| <span data-ttu-id="7d6e1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d6e1-114">Requirement</span></span> | <span data-ttu-id="7d6e1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7d6e1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6e1-116">Header</span><span class="sxs-lookup"><span data-stu-id="7d6e1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7d6e1-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d6e1-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7d6e1-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7d6e1-118">Library</span></span><br/> | <dl> <span data-ttu-id="7d6e1-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7d6e1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d6e1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d6e1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d6e1-121">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7d6e1-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




