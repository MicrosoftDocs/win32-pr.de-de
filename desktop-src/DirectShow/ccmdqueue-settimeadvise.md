---
description: Die settimereference-Methode richtet ein Zeit Geber Ereignis mit der Referenzuhr ein.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Ccmdqueue. settimeempfehlung-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364408"
---
# <a name="ccmdqueuesettimeadvise-method"></a><span data-ttu-id="6dda9-103">Ccmdqueue. settimeempfehlung-Methode</span><span class="sxs-lookup"><span data-stu-id="6dda9-103">CCmdQueue.SetTimeAdvise method</span></span>

<span data-ttu-id="6dda9-104">Die- `SetTimeAdvise` Methode richtet ein Timer-Ereignis mit der Referenzuhr ein.</span><span class="sxs-lookup"><span data-stu-id="6dda9-104">The `SetTimeAdvise` method sets up a timer event with the reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dda9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dda9-105">Syntax</span></span>


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a><span data-ttu-id="6dda9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dda9-106">Parameters</span></span>

<span data-ttu-id="6dda9-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6dda9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6dda9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6dda9-108">Return value</span></span>

<span data-ttu-id="6dda9-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6dda9-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dda9-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dda9-110">Remarks</span></span>

<span data-ttu-id="6dda9-111">Diese Member-Funktion Ruft die [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) -Methode auf, um eine Benachrichtigung für den frühesten Zeitraum einzurichten, der in der Warteschlange erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6dda9-111">This member function calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method to set up a notification for the earliest time required in the queue.</span></span> <span data-ttu-id="6dda9-112">Zurück gestellte Präsentationszeit Befehle sind immer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6dda9-112">Presentation-time commands that are deferred are always checked.</span></span> <span data-ttu-id="6dda9-113">Wenn sich das Filter Diagramm im laufenden Modus befindet, werden auch verzögerte Befehle mit streamzeit geprüft.</span><span class="sxs-lookup"><span data-stu-id="6dda9-113">If the filter graph is in running mode, deferred commands using stream time are also checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dda9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dda9-114">Requirements</span></span>



| <span data-ttu-id="6dda9-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6dda9-115">Requirement</span></span> | <span data-ttu-id="6dda9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6dda9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dda9-117">Header</span><span class="sxs-lookup"><span data-stu-id="6dda9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6dda9-118"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6dda9-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6dda9-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6dda9-119">Library</span></span><br/> | <dl> <span data-ttu-id="6dda9-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6dda9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dda9-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dda9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dda9-122">**Ccmdqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6dda9-122">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




