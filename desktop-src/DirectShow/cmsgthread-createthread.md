---
description: Erstellt einen Thread.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Cmsgthread. kreatethread-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8951995de18158fe4d1e5f84b1d98da701067ab6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368562"
---
# <a name="cmsgthreadcreatethread-method"></a><span data-ttu-id="46031-103">Cmsgthread. kreatethread-Methode</span><span class="sxs-lookup"><span data-stu-id="46031-103">CMsgThread.CreateThread method</span></span>

<span data-ttu-id="46031-104">Erstellt einen Thread.</span><span class="sxs-lookup"><span data-stu-id="46031-104">Creates a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="46031-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46031-105">Syntax</span></span>


```C++
BOOL CreateThread();
```



## <a name="parameters"></a><span data-ttu-id="46031-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46031-106">Parameters</span></span>

<span data-ttu-id="46031-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="46031-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46031-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46031-108">Return value</span></span>

<span data-ttu-id="46031-109">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="46031-109">Returns one of the following values.</span></span>



| <span data-ttu-id="46031-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="46031-110">Return code</span></span>                                                                              | <span data-ttu-id="46031-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46031-111">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="46031-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="46031-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="46031-113">Der Thread wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="46031-113">Thread was successfully created.</span></span><br/>     |
| <dl> <span data-ttu-id="46031-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="46031-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="46031-115">Der Thread wurde nicht erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="46031-115">Thread was not successfully created.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="46031-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46031-116">Remarks</span></span>

<span data-ttu-id="46031-117">Der Thread führt eine Schleife aus, blockiert Sie, bis eine Anforderung in die Warteschlange eingereiht wird (über die Member-Funktion [**cmsgthread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) und ruft dann die [**cmsgthread:: threadmessageproc**](cmsgthread-threadmessageproc.md) -Member-Funktion für jede Nachricht auf.</span><span class="sxs-lookup"><span data-stu-id="46031-117">The thread will loop, blocking until a request is queued (through the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then calling the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function with each message.</span></span>

## <a name="requirements"></a><span data-ttu-id="46031-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46031-118">Requirements</span></span>



| <span data-ttu-id="46031-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46031-119">Requirement</span></span> | <span data-ttu-id="46031-120">Wert</span><span class="sxs-lookup"><span data-stu-id="46031-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46031-121">Header</span><span class="sxs-lookup"><span data-stu-id="46031-121">Header</span></span><br/>  | <dl> <span data-ttu-id="46031-122"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46031-122"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46031-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="46031-123">Library</span></span><br/> | <dl> <span data-ttu-id="46031-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="46031-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46031-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46031-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46031-126">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="46031-126">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




