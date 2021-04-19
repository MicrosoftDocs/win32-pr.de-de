---
description: Der Verweis \_ Zeit-Datentyp definiert die Einheiten für Verweis Zeiten in DirectShow. Jede Einheit der Verweis Zeit beträgt 100 Nanosekunden.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME ("strinmif. h")
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373960"
---
# <a name="reference_time"></a><span data-ttu-id="2f58f-104">Verweis \_ Zeit</span><span class="sxs-lookup"><span data-stu-id="2f58f-104">REFERENCE\_TIME</span></span>

<span data-ttu-id="2f58f-105">Der **Verweis \_ Zeit** -Datentyp definiert die Einheiten für Verweis Zeiten in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2f58f-105">The **REFERENCE\_TIME** data type defines the units for reference times in DirectShow.</span></span> <span data-ttu-id="2f58f-106">Jede Einheit der Verweis Zeit beträgt 100 Nanosekunden.</span><span class="sxs-lookup"><span data-stu-id="2f58f-106">Each unit of reference time is 100 nanoseconds.</span></span>


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a><span data-ttu-id="2f58f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f58f-107">Remarks</span></span>

<span data-ttu-id="2f58f-108">Der **Verweis \_ Zeit** -Datentyp ist eine ganze Zahl mit 64 Bit.</span><span class="sxs-lookup"><span data-stu-id="2f58f-108">The **REFERENCE\_TIME** data type is a 64-bit integer.</span></span>

<span data-ttu-id="2f58f-109">Verweis Zeiten werden normalerweise von einer der folgenden Baselines gemessen:</span><span class="sxs-lookup"><span data-stu-id="2f58f-109">Reference times are usually measured from one of the following baselines:</span></span>

-   <span data-ttu-id="2f58f-110">Eine absolute Uhrzeitangabe.</span><span class="sxs-lookup"><span data-stu-id="2f58f-110">An absolute clock time.</span></span> <span data-ttu-id="2f58f-111">In diesem Fall hängt die Baseline von der Implementierung der Uhr ab.</span><span class="sxs-lookup"><span data-stu-id="2f58f-111">In this case, the baseline will depend on the implementation of the clock.</span></span> <span data-ttu-id="2f58f-112">Weitere Informationen finden Sie unter [Referenzuhren](reference-clocks.md).</span><span class="sxs-lookup"><span data-stu-id="2f58f-112">For more information, see [Reference Clocks](reference-clocks.md).</span></span>
-   <span data-ttu-id="2f58f-113">Relativ zum Anfang der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="2f58f-113">Relative to the start of playback.</span></span>

<span data-ttu-id="2f58f-114">Weitere Informationen zu Referenz Zeiten finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="2f58f-114">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f58f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f58f-115">Requirements</span></span>



| <span data-ttu-id="2f58f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f58f-116">Requirement</span></span> | <span data-ttu-id="2f58f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2f58f-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f58f-118">Header</span><span class="sxs-lookup"><span data-stu-id="2f58f-118">Header</span></span><br/> | <dl> <span data-ttu-id="2f58f-119"><dt>"Strinmif. h" (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f58f-119"><dt>Strmif.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f58f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f58f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f58f-121">DirectShow-Datentypen</span><span class="sxs-lookup"><span data-stu-id="2f58f-121">DirectShow Data Types</span></span>](directshow-data-types.md)
</dt> </dl>

 

 




