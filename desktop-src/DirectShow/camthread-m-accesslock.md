---
description: Kritischer Abschnitt, der den Zugriff auf den Thread durch andere Threads sperrt.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Camthread:: m_AccessLock Member (wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365548"
---
# <a name="camthreadm_accesslock-member"></a><span data-ttu-id="204b2-103">Camthread:: m \_ accesslock-Member</span><span class="sxs-lookup"><span data-stu-id="204b2-103">CAMThread::m\_AccessLock member</span></span>

<span data-ttu-id="204b2-104">Kritischer Abschnitt, der den Zugriff auf den Thread durch andere Threads sperrt.</span><span class="sxs-lookup"><span data-stu-id="204b2-104">Critical section that locks the thread from being accessed by other threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="204b2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="204b2-105">Syntax</span></span>


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a><span data-ttu-id="204b2-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="204b2-106">Remarks</span></span>

<span data-ttu-id="204b2-107">Die Methoden " [**camthread:: Create**](camthread-create.md) " und " [**camthread:: callworker**](camthread-callworker.md) " enthalten diese Sperre, um Vorgänge für den Thread zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="204b2-107">The [**CAMThread::Create**](camthread-create.md) and [**CAMThread::CallWorker**](camthread-callworker.md) methods hold this lock, to serialize operations on the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="204b2-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="204b2-108">Requirements</span></span>



| <span data-ttu-id="204b2-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="204b2-109">Requirement</span></span> | <span data-ttu-id="204b2-110">Wert</span><span class="sxs-lookup"><span data-stu-id="204b2-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="204b2-111">Header</span><span class="sxs-lookup"><span data-stu-id="204b2-111">Header</span></span><br/>  | <dl> <span data-ttu-id="204b2-112"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="204b2-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="204b2-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="204b2-113">Library</span></span><br/> | <dl> <span data-ttu-id="204b2-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="204b2-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="204b2-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="204b2-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="204b2-116">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="204b2-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




