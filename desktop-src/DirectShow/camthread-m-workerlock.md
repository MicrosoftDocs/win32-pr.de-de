---
description: Kritischer Abschnitt, der die von Threads gemeinsam genutzten Daten sperrt.
ms.assetid: 87966d7d-6677-462f-93bc-fedda7f0bdcf
title: 'Camthread:: m_WorkerLock Member (wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_WorkerLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fce6c2ff2a7857f6cb69ce3bb92fe2b6f24bcbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373851"
---
# <a name="camthreadm_workerlock-member"></a><span data-ttu-id="5ffc5-103">Camthread:: m \_ workerlock-Member</span><span class="sxs-lookup"><span data-stu-id="5ffc5-103">CAMThread::m\_WorkerLock member</span></span>

<span data-ttu-id="5ffc5-104">Kritischer Abschnitt, der die von Threads gemeinsam genutzten Daten sperrt.</span><span class="sxs-lookup"><span data-stu-id="5ffc5-104">Critical section that locks data shared among threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ffc5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ffc5-105">Syntax</span></span>


```C++
CCritSec m_WorkerLock;
```



## <a name="requirements"></a><span data-ttu-id="5ffc5-106">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5ffc5-106">Requirements</span></span>



| <span data-ttu-id="5ffc5-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ffc5-107">Requirement</span></span> | <span data-ttu-id="5ffc5-108">Wert</span><span class="sxs-lookup"><span data-stu-id="5ffc5-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ffc5-109">Header</span><span class="sxs-lookup"><span data-stu-id="5ffc5-109">Header</span></span><br/>  | <dl> <span data-ttu-id="5ffc5-110"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ffc5-110"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5ffc5-111">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5ffc5-111">Library</span></span><br/> | <dl> <span data-ttu-id="5ffc5-112">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5ffc5-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ffc5-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ffc5-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ffc5-114">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5ffc5-114">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




