---
description: Die IsQueued-Methode bestimmt, ob das Objekt einen Arbeits Thread zum Übermitteln von Beispielen verwendet.
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: Coutputqueue. IsQueued-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 47093acedb3a28d633ea2c8b0bbdbba3c1493de7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369439"
---
# <a name="coutputqueueisqueued-method"></a><span data-ttu-id="0ca4b-103">Coutputqueue. IsQueued-Methode</span><span class="sxs-lookup"><span data-stu-id="0ca4b-103">COutputQueue.IsQueued method</span></span>

<span data-ttu-id="0ca4b-104">Die- `IsQueued` Methode bestimmt, ob das Objekt einen Arbeits Thread zum Übermitteln von Beispielen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ca4b-104">The `IsQueued` method determines whether the object is using a worker thread to deliver samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca4b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ca4b-105">Syntax</span></span>


```C++
BOOL IsQueued();
```



## <a name="parameters"></a><span data-ttu-id="0ca4b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ca4b-106">Parameters</span></span>

<span data-ttu-id="0ca4b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0ca4b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ca4b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ca4b-108">Return value</span></span>

<span data-ttu-id="0ca4b-109">Gibt " **true** " zurück, wenn das Objekt einen Arbeits Thread verwendet, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="0ca4b-109">Returns **TRUE** if the object is using a worker thread, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca4b-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ca4b-110">Requirements</span></span>



| <span data-ttu-id="0ca4b-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ca4b-111">Requirement</span></span> | <span data-ttu-id="0ca4b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="0ca4b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca4b-113">Header</span><span class="sxs-lookup"><span data-stu-id="0ca4b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="0ca4b-114"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ca4b-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ca4b-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ca4b-115">Library</span></span><br/> | <dl> <span data-ttu-id="0ca4b-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0ca4b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ca4b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ca4b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca4b-118">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0ca4b-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




