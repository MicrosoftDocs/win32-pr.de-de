---
description: Ruft ein CMSG-Objekt in der Warteschlange ab, das eine Anforderung enthält.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Cmsgthread. getthreadmsg-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365472"
---
# <a name="cmsgthreadgetthreadmsg-method"></a><span data-ttu-id="382cb-103">Cmsgthread. getthreadmsg-Methode</span><span class="sxs-lookup"><span data-stu-id="382cb-103">CMsgThread.GetThreadMsg method</span></span>

<span data-ttu-id="382cb-104">Ruft ein [**CMSG**](cmsg.md) -Objekt in der Warteschlange ab, das eine Anforderung enthält.</span><span class="sxs-lookup"><span data-stu-id="382cb-104">Retrieves a queued [**CMsg**](cmsg.md) object containing a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="382cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="382cb-105">Syntax</span></span>


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a><span data-ttu-id="382cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="382cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="382cb-107">*msg*</span><span class="sxs-lookup"><span data-stu-id="382cb-107">*msg*</span></span> 
</dt> <dd>

<span data-ttu-id="382cb-108">Zeiger auf ein zugeordneter [**CMSG**](cmsg.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="382cb-108">Pointer to an allocated [**CMsg**](cmsg.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="382cb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="382cb-109">Return value</span></span>

<span data-ttu-id="382cb-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="382cb-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="382cb-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="382cb-111">Remarks</span></span>

<span data-ttu-id="382cb-112">Diese Member-Funktion wird von der privaten [**ThreadProc**](camthread-threadproc.md) -Funktion des Arbeitsthreads aufgerufen, um die nächste Member-Funktion abzurufen.</span><span class="sxs-lookup"><span data-stu-id="382cb-112">This member function is called from the worker thread's private [**ThreadProc**](camthread-threadproc.md) function to retrieve the next member function.</span></span> <span data-ttu-id="382cb-113">Der *msg* -Parameter sollte auf ein zugeordneter [**CMSG**](cmsg.md) -Objekt zeigen, das mit den Parametern der nächsten Anforderung in der Warteschlange aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="382cb-113">The *msg* parameter should point to an allocated [**CMsg**](cmsg.md) object that will be filled with the parameters to the next request in the queue.</span></span> <span data-ttu-id="382cb-114">Wenn keine Anforderungen in der Warteschlange vorliegen, wird diese Element Funktion blockiert, bis die nächste Anforderung in die Warteschlange eingereiht wird (durch einen aufrufenden Befehl der [**cmsgthread::P utthreadmsg**](cmsgthread-putthreadmsg.md) -Member-Funktion).</span><span class="sxs-lookup"><span data-stu-id="382cb-114">If there are no queued requests, this member function blocks until the next request is queued (by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function).</span></span>

## <a name="requirements"></a><span data-ttu-id="382cb-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="382cb-115">Requirements</span></span>



| <span data-ttu-id="382cb-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="382cb-116">Requirement</span></span> | <span data-ttu-id="382cb-117">Wert</span><span class="sxs-lookup"><span data-stu-id="382cb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="382cb-118">Header</span><span class="sxs-lookup"><span data-stu-id="382cb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="382cb-119"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="382cb-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="382cb-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="382cb-120">Library</span></span><br/> | <dl> <span data-ttu-id="382cb-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="382cb-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="382cb-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="382cb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="382cb-123">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="382cb-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




