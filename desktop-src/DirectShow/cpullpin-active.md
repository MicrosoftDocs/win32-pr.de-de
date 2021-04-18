---
description: Die aktive Methode erstellt einen Arbeits Thread, der Daten aus der Ausgabe-PIN abruft. Diese Methode führt auch einen Commit für die Zuweisung aus.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Cpullpin. Active-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354842"
---
# <a name="cpullpinactive-method"></a><span data-ttu-id="bae6d-104">Cpullpin. Active-Methode</span><span class="sxs-lookup"><span data-stu-id="bae6d-104">CPullPin.Active method</span></span>

<span data-ttu-id="bae6d-105">Die **aktive** Methode erstellt einen Arbeits Thread, der Daten aus der Ausgabe-PIN abruft.</span><span class="sxs-lookup"><span data-stu-id="bae6d-105">The **Active** method creates a worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="bae6d-106">Diese Methode führt auch einen Commit für die Zuweisung aus.</span><span class="sxs-lookup"><span data-stu-id="bae6d-106">This method also commits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="bae6d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bae6d-107">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="bae6d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bae6d-108">Parameters</span></span>

<span data-ttu-id="bae6d-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bae6d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bae6d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bae6d-110">Return value</span></span>

<span data-ttu-id="bae6d-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bae6d-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bae6d-112">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="bae6d-112">Possible values include the following.</span></span>



| <span data-ttu-id="bae6d-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bae6d-113">Return code</span></span>                                                                                  | <span data-ttu-id="bae6d-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bae6d-114">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="bae6d-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bae6d-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="bae6d-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="bae6d-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="bae6d-117"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="bae6d-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="bae6d-118">Die PIN-Verbindung wurde nicht ordnungsgemäß eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="bae6d-118">The pin connection was not established correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="bae6d-119"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="bae6d-119"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="bae6d-120">Der Thread konnte nicht erstellt werden, oder der Thread ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bae6d-120">Could not create the thread, or the thread already exists.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bae6d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bae6d-121">Remarks</span></span>

<span data-ttu-id="bae6d-122">Ruft diese Methode auf, wenn der besitzende Filter aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="bae6d-122">Call this method when the owning filter becomes active.</span></span> <span data-ttu-id="bae6d-123">(Wenn Ihre Eingabe-PIN von [**cbasepin**](cbasepin.md)abgeleitet ist, überschreiben Sie die [**cbasepin:: Active**](cbasepin-active.md) -Methode.)</span><span class="sxs-lookup"><span data-stu-id="bae6d-123">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Active**](cbasepin-active.md) method.)</span></span>

<span data-ttu-id="bae6d-124">Rufen Sie vor dem Aufrufen dieser Methode die [**cpullpin:: Connect**](cpullpin-connect.md) -Methode auf, um die Verbindung mit der Ausgabepin herzustellen.</span><span class="sxs-lookup"><span data-stu-id="bae6d-124">Before calling this method, call the [**CPullPin::Connect**](cpullpin-connect.md) method to establish the connection with the output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="bae6d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bae6d-125">Requirements</span></span>



| <span data-ttu-id="bae6d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bae6d-126">Requirement</span></span> | <span data-ttu-id="bae6d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bae6d-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bae6d-128">Header</span><span class="sxs-lookup"><span data-stu-id="bae6d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bae6d-129"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="bae6d-129"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="bae6d-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bae6d-130">Library</span></span><br/> | <dl> <span data-ttu-id="bae6d-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bae6d-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bae6d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bae6d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae6d-133">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bae6d-133">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




