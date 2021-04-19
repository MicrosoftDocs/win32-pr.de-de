---
description: Die addadvisepacket-Methode fügt der Liste der ausstehenden Anforderungen eine Benachrichtigungs Anforderung hinzu.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Camschedule. addadvisepacket-Methode (dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368602"
---
# <a name="camscheduleaddadvisepacket-method"></a><span data-ttu-id="fa5fd-103">Camschedule. addadvisepacket-Methode</span><span class="sxs-lookup"><span data-stu-id="fa5fd-103">CAMSchedule.AddAdvisePacket method</span></span>

<span data-ttu-id="fa5fd-104">Die- `AddAdvisePacket` Methode fügt der Liste der ausstehenden Anforderungen eine anforderungsanforderung hinzu.</span><span class="sxs-lookup"><span data-stu-id="fa5fd-104">The `AddAdvisePacket` method adds an advise request to the list of pending requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa5fd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa5fd-105">Syntax</span></span>


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a><span data-ttu-id="fa5fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa5fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa5fd-107">*zeitpunkt1 zeitlich* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="fa5fd-107">*time1* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="fa5fd-108">Angeforderte Zeit für die Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="fa5fd-108">Requested time for the advise.</span></span>

</dd> <dt>

<span data-ttu-id="fa5fd-109">*zeitpunkt2?* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="fa5fd-109">*time2* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="fa5fd-110">Für regelmäßige Anforderungs Anforderungen die Zeit zwischen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="fa5fd-110">For periodic advise requests, the time between notifications.</span></span> <span data-ttu-id="fa5fd-111">Dieser Parameter wird ignoriert, wenn *bperiodisch* den Wert **false** hat.</span><span class="sxs-lookup"><span data-stu-id="fa5fd-111">This parameter is ignored if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fa5fd-112">*hnotify*</span><span class="sxs-lookup"><span data-stu-id="fa5fd-112">*hNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="fa5fd-113">Handle für eine Semaphor, wenn *bperiodisch* **true** ist, oder Handle für ein Ereignis, wenn *bperiodisch* den Wert **false** hat.</span><span class="sxs-lookup"><span data-stu-id="fa5fd-113">Handle to a semaphore if *bPeriodic* is **TRUE**, or handle to an event if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fa5fd-114">*bperiodisch*</span><span class="sxs-lookup"><span data-stu-id="fa5fd-114">*bPeriodic*</span></span> 
</dt> <dd>

<span data-ttu-id="fa5fd-115">Boolescher Wert, der angibt, ob eine regelmäßige Benachrichtigung oder eine One-Shot-Benachrichtigung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa5fd-115">Boolean value that specifies whether to add a periodic notification or a one-shot notification.</span></span> <span data-ttu-id="fa5fd-116">**True** gibt an, dass die Benachrichtigung regelmäßig erfolgt. der *zeitpunkt2?* -Parameter gibt die Zeit zwischen Benachrichtigungen an.</span><span class="sxs-lookup"><span data-stu-id="fa5fd-116">If **TRUE**, the notification is periodic; the *time2* parameter specifies the time between notifications.</span></span> <span data-ttu-id="fa5fd-117">Der Wert **false** gibt an, dass die Benachrichtigung nur einmal auftritt.</span><span class="sxs-lookup"><span data-stu-id="fa5fd-117">If **FALSE**, the notification occurs only once.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa5fd-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa5fd-118">Return value</span></span>

<span data-ttu-id="fa5fd-119">Gibt einen Bezeichner für die Benachrichtigungs Anforderung zurück (das "Cookie").</span><span class="sxs-lookup"><span data-stu-id="fa5fd-119">Returns an identifier for the advise request (the "cookie").</span></span> <span data-ttu-id="fa5fd-120">Wenn die Methode fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fa5fd-120">If the method fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa5fd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa5fd-121">Requirements</span></span>



| <span data-ttu-id="fa5fd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa5fd-122">Requirement</span></span> | <span data-ttu-id="fa5fd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fa5fd-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa5fd-124">Header</span><span class="sxs-lookup"><span data-stu-id="fa5fd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fa5fd-125"><dt>Dsschedule. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa5fd-125"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="fa5fd-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa5fd-126">Library</span></span><br/> | <dl> <span data-ttu-id="fa5fd-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fa5fd-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa5fd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa5fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa5fd-129">**Camschedule-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fa5fd-129">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




