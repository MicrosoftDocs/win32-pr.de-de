---
description: 'Der Bezeichner des Threads, der zuletzt die IPinFlowControl:: Block-Methode für diese Pin aufgerufen hat. Diese Element Variable ist nur gültig, wenn die PIN blockiert ist.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Cdynamicoutputpin:: m_dwBlockCallerThreadID Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372751"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a><span data-ttu-id="d1ee9-104">Cdynamicoutputpin:: m \_ dwblockcallerthreadid-Member</span><span class="sxs-lookup"><span data-stu-id="d1ee9-104">CDynamicOutputPin::m\_dwBlockCallerThreadID member</span></span>

<span data-ttu-id="d1ee9-105">Der Bezeichner des Threads, der zuletzt die [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) -Methode für diese Pin aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="d1ee9-105">The identifier of the thread that last called the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method on this pin.</span></span> <span data-ttu-id="d1ee9-106">Diese Element Variable ist nur gültig, wenn die PIN blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1ee9-106">This member variable is only valid while the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1ee9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1ee9-107">Syntax</span></span>


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a><span data-ttu-id="d1ee9-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1ee9-108">Remarks</span></span>

<span data-ttu-id="d1ee9-109">Bevor Sie auf diese Variable zugreifen, halten Sie den kritischen Abschnitt [**cdynamicoutputpin:: m \_ blockstatus eLOCK**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="d1ee9-109">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1ee9-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1ee9-110">Requirements</span></span>



| <span data-ttu-id="d1ee9-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1ee9-111">Requirement</span></span> | <span data-ttu-id="d1ee9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d1ee9-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ee9-113">Header</span><span class="sxs-lookup"><span data-stu-id="d1ee9-113">Header</span></span><br/>  | <dl> <span data-ttu-id="d1ee9-114"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1ee9-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d1ee9-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d1ee9-115">Library</span></span><br/> | <dl> <span data-ttu-id="d1ee9-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d1ee9-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1ee9-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1ee9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1ee9-118">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d1ee9-118">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




