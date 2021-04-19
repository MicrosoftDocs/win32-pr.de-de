---
description: Die \_ Member-Variable m busingimagezuweisung gibt an, ob die Zuweisung für die PIN-Verbindung ein cimagezuordcator-Objekt ist. Wenn der Wert true ist, ist die Zuweisung ein cimagezuordcator-Objekt (oder wird von dieser Klasse abgeleitet).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Cdrawimage:: m_bUsingImageAllocator Member (winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e08d1e8217f42c6855759cefeef40e56949156fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372633"
---
# <a name="cdrawimagem_busingimageallocator-member"></a><span data-ttu-id="d3f5e-104">Cdrawimage:: m \_ busingimagezuordcator-Member</span><span class="sxs-lookup"><span data-stu-id="d3f5e-104">CDrawImage::m\_bUsingImageAllocator member</span></span>

<span data-ttu-id="d3f5e-105">Die `m_bUsingImageAllocator` Member-Variable gibt an, ob die Zuweisung der Pin-Verbindung ein **cimagezuordcator** -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="d3f5e-105">The `m_bUsingImageAllocator` member variable indicates whether the allocator for the pin connection is a **CImageAllocator** object.</span></span> <span data-ttu-id="d3f5e-106">Wenn der Wert **true** ist, ist die Zuweisung ein **cimagezuordcator** -Objekt (oder wird von dieser Klasse abgeleitet).</span><span class="sxs-lookup"><span data-stu-id="d3f5e-106">If the value is **TRUE**, the allocator is a **CImageAllocator** object (or is derived from that class).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f5e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3f5e-107">Syntax</span></span>


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a><span data-ttu-id="d3f5e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3f5e-108">Remarks</span></span>

<span data-ttu-id="d3f5e-109">Wenn der Wert **true** ist, kann das **cdrawimage** -Objekt die GDI **-BitBLT** -Funktion und die **StretchBlt** -Funktion verwenden, um das Bild zu Rendering, anstatt die langsamsten Funktionen **SetDIBitsToDevice** und **StretchDIBits** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3f5e-109">When the value is **TRUE**, the **CDrawImage** object can use the GDI **BitBlt** and **StretchBlt** functions to render the image, rather than the slower **SetDIBitsToDevice** and **StretchDIBits** functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f5e-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3f5e-110">Requirements</span></span>



| <span data-ttu-id="d3f5e-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3f5e-111">Requirement</span></span> | <span data-ttu-id="d3f5e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d3f5e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f5e-113">Header</span><span class="sxs-lookup"><span data-stu-id="d3f5e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="d3f5e-114"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3f5e-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3f5e-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d3f5e-115">Library</span></span><br/> | <dl> <span data-ttu-id="d3f5e-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d3f5e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f5e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3f5e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f5e-118">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d3f5e-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="d3f5e-119">**Cdrawimage:: notifyzucator**</span><span class="sxs-lookup"><span data-stu-id="d3f5e-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> <dt>

[<span data-ttu-id="d3f5e-120">**Cdrawimage:: usingimagezuordcator**</span><span class="sxs-lookup"><span data-stu-id="d3f5e-120">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




