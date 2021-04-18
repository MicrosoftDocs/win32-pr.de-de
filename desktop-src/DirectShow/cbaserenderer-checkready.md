---
description: Die checkready-Methode fragt ab, ob ein Zustandsübergang abgeschlossen ist.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Cbaserderderer. checkready-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371196"
---
# <a name="cbaserenderercheckready-method"></a><span data-ttu-id="19c5a-103">Cbaserderderer. checkready-Methode</span><span class="sxs-lookup"><span data-stu-id="19c5a-103">CBaseRenderer.CheckReady method</span></span>

<span data-ttu-id="19c5a-104">Die- `CheckReady` Methode fragt ab, ob ein Zustandsübergang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="19c5a-104">The `CheckReady` method queries whether a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c5a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19c5a-105">Syntax</span></span>


```C++
BOOL CheckReady();
```



## <a name="parameters"></a><span data-ttu-id="19c5a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19c5a-106">Parameters</span></span>

<span data-ttu-id="19c5a-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="19c5a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="19c5a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19c5a-108">Return value</span></span>

<span data-ttu-id="19c5a-109">Gibt " **true** " zurück, wenn der Zustandsübergang beendet ist, oder " **false** ", wenn der Filter weiterhin in einen neuen Zustand übergeht.</span><span class="sxs-lookup"><span data-stu-id="19c5a-109">Returns **TRUE** if the state transition is complete, or **FALSE** if the filter is still transitioning to a new state.</span></span>

## <a name="requirements"></a><span data-ttu-id="19c5a-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19c5a-110">Requirements</span></span>



| <span data-ttu-id="19c5a-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19c5a-111">Requirement</span></span> | <span data-ttu-id="19c5a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="19c5a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19c5a-113">Header</span><span class="sxs-lookup"><span data-stu-id="19c5a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="19c5a-114"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19c5a-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="19c5a-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19c5a-115">Library</span></span><br/> | <dl> <span data-ttu-id="19c5a-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="19c5a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19c5a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19c5a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c5a-118">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="19c5a-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="19c5a-119">**Cbaserderderer:: notready**</span><span class="sxs-lookup"><span data-stu-id="19c5a-119">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> <dt>

[<span data-ttu-id="19c5a-120">**Cbasererderer:: Ready**</span><span class="sxs-lookup"><span data-stu-id="19c5a-120">**CBaseRenderer::Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




