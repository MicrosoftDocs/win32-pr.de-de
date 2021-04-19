---
description: Die coinitializehelper-Methode ruft die CoInitializeEx-Funktion am Anfang des Threads auf.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Camthread. coinitializehelper-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356422"
---
# <a name="camthreadcoinitializehelper-method"></a><span data-ttu-id="be052-103">Camthread. coinitializehelper-Methode</span><span class="sxs-lookup"><span data-stu-id="be052-103">CAMThread.CoInitializeHelper method</span></span>

<span data-ttu-id="be052-104">Die- `CoInitializeHelper` Methode ruft die CoInitializeEx-Funktion am Anfang des Threads auf.</span><span class="sxs-lookup"><span data-stu-id="be052-104">The `CoInitializeHelper` method calls the CoInitializeEx function at the start of the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="be052-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be052-105">Syntax</span></span>


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a><span data-ttu-id="be052-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be052-106">Parameters</span></span>

<span data-ttu-id="be052-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="be052-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be052-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be052-108">Return value</span></span>

<span data-ttu-id="be052-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="be052-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="be052-110">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="be052-110">The following are possible values.</span></span>



| <span data-ttu-id="be052-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="be052-111">Return code</span></span>                                                                             | <span data-ttu-id="be052-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be052-112">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="be052-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="be052-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="be052-114">Die CoInitializeEx-Funktion ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be052-114">The CoInitializeEx function is not available.</span></span><br/> |
| <dl> <span data-ttu-id="be052-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="be052-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="be052-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="be052-116">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="be052-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="be052-117"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="be052-118">Fehler.</span><span class="sxs-lookup"><span data-stu-id="be052-118">Failure.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="be052-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be052-119">Remarks</span></span>

<span data-ttu-id="be052-120">Die Methode " [**camthread:: initialthread proc**](camthread-initialthreadproc.md) " ruft diese Hilfsmethode auf, die die Funktion "CoInitializeEx" aufruft.</span><span class="sxs-lookup"><span data-stu-id="be052-120">The [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method calls this helper method, which calls the CoInitializeEx function.</span></span> <span data-ttu-id="be052-121">Er verwendet das coinit- \_ Flag "deaktivierte \_ OLE1DDE", um dynamischer Datenaustausch (DDE) zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="be052-121">It uses the COINIT\_DISABLE\_OLE1DDE flag, to disable Dynamic Data Exchange (DDE).</span></span> <span data-ttu-id="be052-122">Weitere Informationen finden Sie unter Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="be052-122">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="be052-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be052-123">Requirements</span></span>



| <span data-ttu-id="be052-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be052-124">Requirement</span></span> | <span data-ttu-id="be052-125">Wert</span><span class="sxs-lookup"><span data-stu-id="be052-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be052-126">Header</span><span class="sxs-lookup"><span data-stu-id="be052-126">Header</span></span><br/>  | <dl> <span data-ttu-id="be052-127"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be052-127"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="be052-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="be052-128">Library</span></span><br/> | <dl> <span data-ttu-id="be052-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="be052-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be052-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be052-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be052-131">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="be052-131">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




