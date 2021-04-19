---
description: Ruft den Bezeichner des Threads ab.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: Cmsgthread. getthreadid-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0819810b9b7589fc5272c0e79f87fc2f34325f5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372424"
---
# <a name="cmsgthreadgetthreadid-method"></a><span data-ttu-id="04f48-103">Cmsgthread. getthreadid-Methode</span><span class="sxs-lookup"><span data-stu-id="04f48-103">CMsgThread.GetThreadID method</span></span>

<span data-ttu-id="04f48-104">Ruft den Bezeichner des Threads ab.</span><span class="sxs-lookup"><span data-stu-id="04f48-104">Retrieves the thread's identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="04f48-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04f48-105">Syntax</span></span>


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a><span data-ttu-id="04f48-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04f48-106">Parameters</span></span>

<span data-ttu-id="04f48-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="04f48-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="04f48-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04f48-108">Return value</span></span>

<span data-ttu-id="04f48-109">Gibt den privaten Datenmember der **m \_ ThreadId** zurück.</span><span class="sxs-lookup"><span data-stu-id="04f48-109">Returns the **m\_ThreadId** private data member.</span></span>

## <a name="remarks"></a><span data-ttu-id="04f48-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04f48-110">Remarks</span></span>

<span data-ttu-id="04f48-111">Diese Funktion gibt den Microsoft Win32-Bezeichner für den Arbeits Thread zurück.</span><span class="sxs-lookup"><span data-stu-id="04f48-111">This function returns the Microsoft Win32 identifier for the worker thread.</span></span> <span data-ttu-id="04f48-112">Sie können diese Member-Funktion entweder für den Arbeits Thread oder einen Client Thread aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="04f48-112">You can call this member function on either the worker thread or a client thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="04f48-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04f48-113">Requirements</span></span>



| <span data-ttu-id="04f48-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04f48-114">Requirement</span></span> | <span data-ttu-id="04f48-115">Wert</span><span class="sxs-lookup"><span data-stu-id="04f48-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04f48-116">Header</span><span class="sxs-lookup"><span data-stu-id="04f48-116">Header</span></span><br/>  | <dl> <span data-ttu-id="04f48-117"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04f48-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="04f48-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="04f48-118">Library</span></span><br/> | <dl> <span data-ttu-id="04f48-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="04f48-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04f48-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04f48-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f48-121">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="04f48-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




