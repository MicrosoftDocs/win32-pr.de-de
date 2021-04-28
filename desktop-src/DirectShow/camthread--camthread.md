---
description: CABThread.~CABThread-Destruktor – Destruktormethode.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: CABThread.~HIDThread-Destruktor (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 84a40205fc93677f20256676ad09a18357d46acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096438"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="e9d70-103">CABThread.~CABThread-Destruktor</span><span class="sxs-lookup"><span data-stu-id="e9d70-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="e9d70-104">Destruktormethode.</span><span class="sxs-lookup"><span data-stu-id="e9d70-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d70-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9d70-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="e9d70-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9d70-106">Remarks</span></span>

<span data-ttu-id="e9d70-107">Der Destruktor ruft die [**METHODE CABThread::Close**](camthread-close.md) auf, die darauf wartet, dass der Thread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9d70-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d70-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9d70-108">Requirements</span></span>



| <span data-ttu-id="e9d70-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9d70-109">Requirement</span></span> | <span data-ttu-id="e9d70-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e9d70-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d70-111">Header</span><span class="sxs-lookup"><span data-stu-id="e9d70-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e9d70-112"><dt>Wxutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9d70-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e9d70-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e9d70-113">Library</span></span><br/> | <dl> <span data-ttu-id="e9d70-114"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e9d70-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9d70-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9d70-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9d70-116">**WEBCAMThread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e9d70-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




