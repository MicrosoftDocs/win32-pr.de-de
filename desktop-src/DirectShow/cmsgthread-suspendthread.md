---
description: Verwendet die Microsoft Win32 SuspendThread-Funktion, um den Betrieb eines laufenden Threads anzuhalten.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Cmsgthread. SuspendThread-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358793"
---
# <a name="cmsgthreadsuspendthread-method"></a><span data-ttu-id="a8e16-103">Cmsgthread. SuspendThread-Methode</span><span class="sxs-lookup"><span data-stu-id="a8e16-103">CMsgThread.SuspendThread method</span></span>

<span data-ttu-id="a8e16-104">Verwendet die Microsoft Win32 **SuspendThread** -Funktion, um den Betrieb eines laufenden Threads anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="a8e16-104">Uses the Microsoft Win32 **SuspendThread** function to suspend the operation of a running thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8e16-105">Syntax</span></span>


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a><span data-ttu-id="a8e16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8e16-106">Parameters</span></span>

<span data-ttu-id="a8e16-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a8e16-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8e16-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8e16-108">Return value</span></span>

<span data-ttu-id="a8e16-109">Wenn die Member-Funktion erfolgreich ist, ist der Rückgabewert die vorherige anhalteanzahl des Threads.</span><span class="sxs-lookup"><span data-stu-id="a8e16-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="a8e16-110">Wenn die Member-Funktion fehlschlägt, ist der Rückgabewert 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a8e16-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="a8e16-111">Um erweiterte Fehlerinformationen abzurufen, rufen Sie die Microsoft Win32 **GetLastError** -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="a8e16-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8e16-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8e16-112">Remarks</span></span>

<span data-ttu-id="a8e16-113">Der Client Thread ruft diese Member-Funktion auf, um den Betrieb des Arbeitsthreads anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="a8e16-113">The client thread calls this member function to suspend the operation of the worker thread.</span></span> <span data-ttu-id="a8e16-114">Der Arbeits Thread bleibt angehalten und wird erst ausgeführt, wenn ein zusätzlicher Befehl an die [**cmsgthread:: ResumeThread**](cmsgthread-resumethread.md) -Member-Funktion erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a8e16-114">The worker thread remains suspended and will not execute until an additional call to the [**CMsgThread::ResumeThread**](cmsgthread-resumethread.md) member function is made.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8e16-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8e16-115">Requirements</span></span>



| <span data-ttu-id="a8e16-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8e16-116">Requirement</span></span> | <span data-ttu-id="a8e16-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a8e16-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e16-118">Header</span><span class="sxs-lookup"><span data-stu-id="a8e16-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a8e16-119"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8e16-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a8e16-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8e16-120">Library</span></span><br/> | <dl> <span data-ttu-id="a8e16-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a8e16-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8e16-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8e16-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e16-123">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a8e16-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




