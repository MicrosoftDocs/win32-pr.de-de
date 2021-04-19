---
description: Verwendet die Microsoft Win32-Funktion SetThreadPriority, um die Priorität des Threads auf einen neuen Wert festzulegen.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: Cmsgthread. SetThreadPriority-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370923"
---
# <a name="cmsgthreadsetthreadpriority-method"></a><span data-ttu-id="d1205-103">Cmsgthread. SetThreadPriority-Methode</span><span class="sxs-lookup"><span data-stu-id="d1205-103">CMsgThread.SetThreadPriority method</span></span>

<span data-ttu-id="d1205-104">Verwendet die Microsoft Win32-Funktion **SetThreadPriority** , um die Priorität des Threads auf einen neuen Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d1205-104">Uses the Microsoft Win32 **SetThreadPriority** function to set the priority of the thread to a new value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1205-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1205-105">Syntax</span></span>


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a><span data-ttu-id="d1205-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1205-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1205-107">*npriorität*</span><span class="sxs-lookup"><span data-stu-id="d1205-107">*nPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="d1205-108">Priorität des Threads.</span><span class="sxs-lookup"><span data-stu-id="d1205-108">Priority of the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1205-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1205-109">Return value</span></span>

<span data-ttu-id="d1205-110">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="d1205-110">Returns one of the following values.</span></span>



| <span data-ttu-id="d1205-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d1205-111">Return code</span></span>                                                                              | <span data-ttu-id="d1205-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1205-112">Description</span></span>                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d1205-113"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d1205-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="d1205-114">Die Priorität wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d1205-114">Priority was successfully set.</span></span><br/> |
| <dl> <span data-ttu-id="d1205-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d1205-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="d1205-116">Es wurde keine Priorität festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d1205-116">Priority was not set.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="d1205-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1205-117">Remarks</span></span>

<span data-ttu-id="d1205-118">Der Client und der Arbeits Thread können diese Member-Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="d1205-118">The client and the worker thread can call this member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1205-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1205-119">Requirements</span></span>



| <span data-ttu-id="d1205-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1205-120">Requirement</span></span> | <span data-ttu-id="d1205-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d1205-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1205-122">Header</span><span class="sxs-lookup"><span data-stu-id="d1205-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d1205-123"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1205-123"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d1205-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d1205-124">Library</span></span><br/> | <dl> <span data-ttu-id="d1205-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d1205-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1205-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1205-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1205-127">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d1205-127">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




