---
description: 'Verwendet die Microsoft Win32 ResumeThread-Funktion, um den Vorgang des Arbeitsthreads nach einem vorherigen aufrufsvorgang der cmsgthread:: SuspendThread-Member-Funktion fortzusetzen.'
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: Cmsgthread. ResumeThread-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370836"
---
# <a name="cmsgthreadresumethread-method"></a><span data-ttu-id="1493f-103">Cmsgthread. ResumeThread-Methode</span><span class="sxs-lookup"><span data-stu-id="1493f-103">CMsgThread.ResumeThread method</span></span>

<span data-ttu-id="1493f-104">Verwendet die Microsoft Win32 **ResumeThread** -Funktion, um den Vorgang des Arbeitsthreads nach einem vorherigen aufrufsvorgang der [**cmsgthread:: SuspendThread**](cmsgthread-suspendthread.md) -Member-Funktion fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="1493f-104">Uses the Microsoft Win32 **ResumeThread** function to continue the operation of the worker thread after a previous call to the [**CMsgThread::SuspendThread**](cmsgthread-suspendthread.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1493f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1493f-105">Syntax</span></span>


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a><span data-ttu-id="1493f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1493f-106">Parameters</span></span>

<span data-ttu-id="1493f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1493f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1493f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1493f-108">Return value</span></span>

<span data-ttu-id="1493f-109">Wenn die Member-Funktion erfolgreich ist, ist der Rückgabewert die vorherige anhalteanzahl des Threads.</span><span class="sxs-lookup"><span data-stu-id="1493f-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="1493f-110">Wenn die Member-Funktion fehlschlägt, ist der Rückgabewert 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1493f-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="1493f-111">Um erweiterte Fehlerinformationen abzurufen, rufen Sie die Microsoft Win32 **GetLastError** -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="1493f-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1493f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1493f-112">Requirements</span></span>



| <span data-ttu-id="1493f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1493f-113">Requirement</span></span> | <span data-ttu-id="1493f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1493f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1493f-115">Header</span><span class="sxs-lookup"><span data-stu-id="1493f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1493f-116"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1493f-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1493f-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1493f-117">Library</span></span><br/> | <dl> <span data-ttu-id="1493f-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1493f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1493f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1493f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1493f-120">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1493f-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




