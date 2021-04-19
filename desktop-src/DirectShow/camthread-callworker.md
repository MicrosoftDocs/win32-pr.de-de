---
description: Die callworker-Methode signalisiert dem Thread eine Anforderung.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Camthread. callworker-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372668"
---
# <a name="camthreadcallworker-method"></a><span data-ttu-id="d0b24-103">Camthread. callworker-Methode</span><span class="sxs-lookup"><span data-stu-id="d0b24-103">CAMThread.CallWorker method</span></span>

<span data-ttu-id="d0b24-104">Die- `CallWorker` Methode signalisiert dem Thread eine-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d0b24-104">The `CallWorker` method signals the thread with a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b24-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0b24-105">Syntax</span></span>


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a><span data-ttu-id="d0b24-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0b24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0b24-107">*dwparam*</span><span class="sxs-lookup"><span data-stu-id="d0b24-107">*dwParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0b24-108">Anforderungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="d0b24-108">Request parameter.</span></span> <span data-ttu-id="d0b24-109">Die abgeleitete Klasse definiert die Bedeutung des Parameters.</span><span class="sxs-lookup"><span data-stu-id="d0b24-109">The derived class defines the meaning of the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0b24-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0b24-110">Return value</span></span>

<span data-ttu-id="d0b24-111">Gibt einen Wert zurück, der von der abgeleiteten Klasse definiert wird.</span><span class="sxs-lookup"><span data-stu-id="d0b24-111">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0b24-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0b24-112">Remarks</span></span>

<span data-ttu-id="d0b24-113">Die Methoden " [**camthread:: GetRequest**](camthread-getrequest.md) " und " [**camthread:: CheckRequest**](camthread-checkrequest.md) " rufen den Wert des Parameters " *dwparam* " ab.</span><span class="sxs-lookup"><span data-stu-id="d0b24-113">The [**CAMThread::GetRequest**](camthread-getrequest.md) and [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods retrieve the value of the *dwParam* parameter.</span></span> <span data-ttu-id="d0b24-114">Die GetRequest-Methode blockiert, bis `CallWorker` aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d0b24-114">The GetRequest method blocks until `CallWorker` is called.</span></span>

<span data-ttu-id="d0b24-115">Diese Methode wird blockiert, bis die Methode " [**camthread:: Reply**](camthread-reply.md) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d0b24-115">This method blocks until the [**CAMThread::Reply**](camthread-reply.md) method is called.</span></span> <span data-ttu-id="d0b24-116">Der Rückgabewert ist der Parameter, der für die Antwort angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d0b24-116">The return value is the parameter given to Reply.</span></span>

<span data-ttu-id="d0b24-117">Diese Methode enthält die " [**camthread:: m \_ accesslock**](camthread-m-accesslock.md) "-Sperre zum Serialisieren von Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="d0b24-117">This method holds the [**CAMThread::m\_AccessLock**](camthread-m-accesslock.md) lock to serialize requests.</span></span> <span data-ttu-id="d0b24-118">Daher müssen Sie diese Methode aus dem Thread selbst oder aus einer beliebigen Member-Funktion, die im Kontext des Threads ausgeführt wird, abrufen.</span><span class="sxs-lookup"><span data-stu-id="d0b24-118">Therefore, do call this method from the thread itself or from any member function that executes in the context of the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b24-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0b24-119">Requirements</span></span>



| <span data-ttu-id="d0b24-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0b24-120">Requirement</span></span> | <span data-ttu-id="d0b24-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d0b24-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b24-122">Header</span><span class="sxs-lookup"><span data-stu-id="d0b24-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d0b24-123"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0b24-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d0b24-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d0b24-124">Library</span></span><br/> | <dl> <span data-ttu-id="d0b24-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d0b24-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0b24-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0b24-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0b24-127">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d0b24-127">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




