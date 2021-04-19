---
description: Dekonstruktormethode.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: Camthread. ~ camthread-debugtor (wxutil. h)
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
ms.openlocfilehash: b0b0a4dde858811a75347105b9fccd2f499c4faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361545"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="9c185-103">Camthread. ~ camthread-Dekonstruktor</span><span class="sxs-lookup"><span data-stu-id="9c185-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="9c185-104">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="9c185-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c185-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c185-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="9c185-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c185-106">Remarks</span></span>

<span data-ttu-id="9c185-107">Der Dekonstruktor Ruft die Methode " [**camthread:: Close**](camthread-close.md) " auf, die darauf wartet, dass der Thread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c185-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c185-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c185-108">Requirements</span></span>



| <span data-ttu-id="9c185-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c185-109">Requirement</span></span> | <span data-ttu-id="9c185-110">Wert</span><span class="sxs-lookup"><span data-stu-id="9c185-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c185-111">Header</span><span class="sxs-lookup"><span data-stu-id="9c185-111">Header</span></span><br/>  | <dl> <span data-ttu-id="9c185-112"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c185-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9c185-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9c185-113">Library</span></span><br/> | <dl> <span data-ttu-id="9c185-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9c185-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c185-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c185-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c185-116">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9c185-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




