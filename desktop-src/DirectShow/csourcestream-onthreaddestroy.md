---
description: Die onthreaddestroy-Methode wird aufgerufen, wenn der streamingthread gerade beendet wird.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Csourcestream. onthreaddestroy-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358637"
---
# <a name="csourcestreamonthreaddestroy-method"></a><span data-ttu-id="0f54c-103">Csourcestream. onthreaddestroy-Methode</span><span class="sxs-lookup"><span data-stu-id="0f54c-103">CSourceStream.OnThreadDestroy method</span></span>

<span data-ttu-id="0f54c-104">Die- `OnThreadDestroy` Methode wird aufgerufen, wenn der streamingthread gerade beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0f54c-104">The `OnThreadDestroy` method is called when the streaming thread is about to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f54c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f54c-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a><span data-ttu-id="0f54c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f54c-106">Parameters</span></span>

<span data-ttu-id="0f54c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0f54c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f54c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f54c-108">Return value</span></span>

<span data-ttu-id="0f54c-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="0f54c-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f54c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f54c-110">Remarks</span></span>

<span data-ttu-id="0f54c-111">Die Thread Prozedur [**csourcestream:: ThreadProc**](csourcestream-threadproc.md)ruft diese Methode auf, bevor Sie beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0f54c-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method before it exits.</span></span> <span data-ttu-id="0f54c-112">Die-Methode führt in der Basisklasse keine Aktion aus. Sie kann von der abgeleiteten Klasse außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="0f54c-112">The method does nothing in the base class; it is available for the derived class to override.</span></span> <span data-ttu-id="0f54c-113">Wenn die abgeleitete Klasse einen Fehlercode zurückgibt, wird der Thread mit einem Fehler beendet.</span><span class="sxs-lookup"><span data-stu-id="0f54c-113">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f54c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f54c-114">Requirements</span></span>



| <span data-ttu-id="0f54c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f54c-115">Requirement</span></span> | <span data-ttu-id="0f54c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0f54c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f54c-117">Header</span><span class="sxs-lookup"><span data-stu-id="0f54c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0f54c-118"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f54c-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0f54c-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0f54c-119">Library</span></span><br/> | <dl> <span data-ttu-id="0f54c-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0f54c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f54c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f54c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f54c-122">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0f54c-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




