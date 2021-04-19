---
description: Die GetRequest-Methode wartet auf die nächste Thread Anforderung.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Csourcestream. GetRequest-Methode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366774"
---
# <a name="csourcestreamgetrequest-method"></a><span data-ttu-id="d169b-103">Csourcestream. GetRequest-Methode</span><span class="sxs-lookup"><span data-stu-id="d169b-103">CSourceStream.GetRequest method</span></span>

<span data-ttu-id="d169b-104">Die- `GetRequest` Methode wartet auf die nächste Thread Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d169b-104">The `GetRequest` method waits for the next thread request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d169b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d169b-105">Syntax</span></span>


```C++
Command GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="d169b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d169b-106">Parameters</span></span>

<span data-ttu-id="d169b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d169b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d169b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d169b-108">Return value</span></span>

<span data-ttu-id="d169b-109">Gibt die nächste Thread Anforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="d169b-109">Returns the next thread request.</span></span>

## <a name="remarks"></a><span data-ttu-id="d169b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d169b-110">Remarks</span></span>

<span data-ttu-id="d169b-111">Diese Methode überschreibt die Methode " [**camthread:: GetRequest**](camthread-getrequest.md) ".</span><span class="sxs-lookup"><span data-stu-id="d169b-111">This method overrides the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="d169b-112">Der Rückgabewert wird in den folgenden enumerierten Typ umgewandelt:</span><span class="sxs-lookup"><span data-stu-id="d169b-112">The return value is cast to the following enumerated type:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="d169b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d169b-113">Requirements</span></span>



| <span data-ttu-id="d169b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d169b-114">Requirement</span></span> | <span data-ttu-id="d169b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d169b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d169b-116">Header</span><span class="sxs-lookup"><span data-stu-id="d169b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d169b-117"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d169b-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d169b-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d169b-118">Library</span></span><br/> | <dl> <span data-ttu-id="d169b-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d169b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d169b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d169b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d169b-121">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d169b-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




