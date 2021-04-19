---
description: Zeiger auf ein kritisches Abschnitts Objekt.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'Csourceseeking:: m_pLock Member (ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373827"
---
# <a name="csourceseekingm_plock-member"></a><span data-ttu-id="0e921-103">Csourceseeking:: m \_ Plock-Member</span><span class="sxs-lookup"><span data-stu-id="0e921-103">CSourceSeeking::m\_pLock member</span></span>

<span data-ttu-id="0e921-104">Zeiger auf ein kritisches Abschnitts Objekt.</span><span class="sxs-lookup"><span data-stu-id="0e921-104">Pointer to a critical section object.</span></span> <span data-ttu-id="0e921-105">Die- `CSourceSeeking` Klasse verwendet diesen kritischen Abschnitt, um den Zugriff auf die Start-und Endzeit-, Dauer-und Raten Variablen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="0e921-105">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and rate variables.</span></span> <span data-ttu-id="0e921-106">Diese Variable wird in der Konstruktormethode initialisiert. siehe [**csourceseeking:: csourceseeking**](csourceseeking-csourceseeking.md).</span><span class="sxs-lookup"><span data-stu-id="0e921-106">This variable is initialized in the constructor method; see [**CSourceSeeking::CSourceSeeking**](csourceseeking-csourceseeking.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e921-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e921-107">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="0e921-108">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0e921-108">Requirements</span></span>



| <span data-ttu-id="0e921-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e921-109">Requirement</span></span> | <span data-ttu-id="0e921-110">Wert</span><span class="sxs-lookup"><span data-stu-id="0e921-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e921-111">Header</span><span class="sxs-lookup"><span data-stu-id="0e921-111">Header</span></span><br/>  | <dl> <span data-ttu-id="0e921-112"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e921-112"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0e921-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e921-113">Library</span></span><br/> | <dl> <span data-ttu-id="0e921-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0e921-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e921-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e921-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e921-116">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0e921-116">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




