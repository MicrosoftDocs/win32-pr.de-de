---
description: Kritischer Abschnitt, der den Blockierungs Zustand schützt.
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: 'Cdynamicoutputpin:: m_BlockStateLock Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d9175342218e8b82698fe9b89d15937d6913e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364704"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a><span data-ttu-id="5a965-103">Cdynamicoutputpin:: m \_ blockstatus-Member</span><span class="sxs-lookup"><span data-stu-id="5a965-103">CDynamicOutputPin::m\_BlockStateLock member</span></span>

<span data-ttu-id="5a965-104">Kritischer Abschnitt, der den Blockierungs Zustand schützt.</span><span class="sxs-lookup"><span data-stu-id="5a965-104">Critical section that protects the blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a965-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a965-105">Syntax</span></span>


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a><span data-ttu-id="5a965-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a965-106">Remarks</span></span>

<span data-ttu-id="5a965-107">Halten Sie diesen kritischen Abschnitt vor, bevor Sie eine der folgenden Element Variablen verwenden:</span><span class="sxs-lookup"><span data-stu-id="5a965-107">Hold this critical section before using any of the following member variables:</span></span>

-   [<span data-ttu-id="5a965-108">**Cdynamicoutputpin:: m \_ blockstate**</span><span class="sxs-lookup"><span data-stu-id="5a965-108">**CDynamicOutputPin::m\_BlockState**</span></span>](cdynamicoutputpin-m-blockstate.md)
-   [<span data-ttu-id="5a965-109">**Cdynamicoutputpin:: m \_ dwblockcallerthreadid**</span><span class="sxs-lookup"><span data-stu-id="5a965-109">**CDynamicOutputPin::m\_dwBlockCallerThreadID**</span></span>](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [<span data-ttu-id="5a965-110">**Cdynamicoutputpin:: m \_ dwnumoutstandingoutputpinusers**</span><span class="sxs-lookup"><span data-stu-id="5a965-110">**CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers**</span></span>](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [<span data-ttu-id="5a965-111">**Cdynamicoutputpin:: m \_ hnotifycallerpinblockedevent**</span><span class="sxs-lookup"><span data-stu-id="5a965-111">**CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent**</span></span>](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a><span data-ttu-id="5a965-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a965-112">Requirements</span></span>



| <span data-ttu-id="5a965-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a965-113">Requirement</span></span> | <span data-ttu-id="5a965-114">Wert</span><span class="sxs-lookup"><span data-stu-id="5a965-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a965-115">Header</span><span class="sxs-lookup"><span data-stu-id="5a965-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5a965-116"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a965-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5a965-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5a965-117">Library</span></span><br/> | <dl> <span data-ttu-id="5a965-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5a965-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a965-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a965-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a965-120">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5a965-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




