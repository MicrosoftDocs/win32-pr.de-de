---
description: Die onthreadcreate-Methode wird aufgerufen, wenn der streamingindthread initialisiert wird.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Csourcestream. onthreadcreate-Methode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370208"
---
# <a name="csourcestreamonthreadcreate-method"></a><span data-ttu-id="6dba1-103">Csourcestream. onthreadcreate-Methode</span><span class="sxs-lookup"><span data-stu-id="6dba1-103">CSourceStream.OnThreadCreate method</span></span>

<span data-ttu-id="6dba1-104">Die- `OnThreadCreate` Methode wird aufgerufen, wenn der streamingthread initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6dba1-104">The `OnThreadCreate` method is called when the streaming thread is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dba1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dba1-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a><span data-ttu-id="6dba1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dba1-106">Parameters</span></span>

<span data-ttu-id="6dba1-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6dba1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6dba1-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6dba1-108">Return value</span></span>

<span data-ttu-id="6dba1-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="6dba1-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dba1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dba1-110">Remarks</span></span>

<span data-ttu-id="6dba1-111">Die Thread Prozedur [**csourcestream:: ThreadProc**](csourcestream-threadproc.md)ruft diese Methode auf, wenn Sie zum ersten Mal eine [**csourcestream:: init**](csourcestream-init.md) -Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="6dba1-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method when it first receives a [**CSourceStream::Init**](csourcestream-init.md) request.</span></span> <span data-ttu-id="6dba1-112">Die-Methode führt in der-Basisklasse keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="6dba1-112">The method does nothing in the base class.</span></span> <span data-ttu-id="6dba1-113">Die abgeleitete Klasse kann diese Methode überschreiben, um Thread Initialisierungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6dba1-113">The derived class can override this method to perform thread initializations.</span></span> <span data-ttu-id="6dba1-114">Wenn die abgeleitete Klasse einen Fehlercode zurückgibt, wird der Thread mit einem Fehler beendet.</span><span class="sxs-lookup"><span data-stu-id="6dba1-114">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dba1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dba1-115">Requirements</span></span>



| <span data-ttu-id="6dba1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6dba1-116">Requirement</span></span> | <span data-ttu-id="6dba1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6dba1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dba1-118">Header</span><span class="sxs-lookup"><span data-stu-id="6dba1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6dba1-119"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6dba1-119"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6dba1-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6dba1-120">Library</span></span><br/> | <dl> <span data-ttu-id="6dba1-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6dba1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dba1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dba1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dba1-123">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6dba1-123">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




