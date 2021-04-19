---
description: Die IsIdle-Methode bestimmt, ob das Objekt auf Daten wartet.
ms.assetid: be1b5633-f9e9-497e-8b6f-5634eae91273
title: Coutputqueue. IsIdle-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsIdle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bf8b42189e356659e74398eaa3eefeb5f771a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355994"
---
# <a name="coutputqueueisidle-method"></a><span data-ttu-id="5bd64-103">Coutputqueue. IsIdle-Methode</span><span class="sxs-lookup"><span data-stu-id="5bd64-103">COutputQueue.IsIdle method</span></span>

<span data-ttu-id="5bd64-104">Die- `IsIdle` Methode bestimmt, ob das Objekt auf Daten wartet.</span><span class="sxs-lookup"><span data-stu-id="5bd64-104">The `IsIdle` method determines whether the object is waiting for data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd64-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bd64-105">Syntax</span></span>


```C++
BOOL IsIdle();
```



## <a name="parameters"></a><span data-ttu-id="5bd64-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bd64-106">Parameters</span></span>

<span data-ttu-id="5bd64-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5bd64-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5bd64-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5bd64-108">Return value</span></span>

<span data-ttu-id="5bd64-109">Gibt " **true** " zurück, wenn der Thread wartet und das Beispiel Array leer ist.</span><span class="sxs-lookup"><span data-stu-id="5bd64-109">Returns **TRUE** if the thread is waiting and the sample array is empty.</span></span> <span data-ttu-id="5bd64-110">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5bd64-110">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bd64-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bd64-111">Requirements</span></span>



| <span data-ttu-id="5bd64-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bd64-112">Requirement</span></span> | <span data-ttu-id="5bd64-113">Wert</span><span class="sxs-lookup"><span data-stu-id="5bd64-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd64-114">Header</span><span class="sxs-lookup"><span data-stu-id="5bd64-114">Header</span></span><br/>  | <dl> <span data-ttu-id="5bd64-115"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bd64-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5bd64-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5bd64-116">Library</span></span><br/> | <dl> <span data-ttu-id="5bd64-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5bd64-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bd64-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bd64-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd64-119">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5bd64-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




