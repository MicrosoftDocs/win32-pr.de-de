---
description: Konstruktormethode.
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Cammsgevent. cammsgevent-Konstruktor (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d207afae53a715728d8307656b0c2427ce9574c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358763"
---
# <a name="cammsgeventcammsgevent-constructor"></a><span data-ttu-id="7ec71-103">Cammsgevent. cammsgevent-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="7ec71-103">CAMMsgEvent.CAMMsgEvent constructor</span></span>

<span data-ttu-id="7ec71-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="7ec71-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec71-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ec71-105">Syntax</span></span>


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="7ec71-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ec71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec71-107">*PHR*</span><span class="sxs-lookup"><span data-stu-id="7ec71-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="7ec71-108">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="7ec71-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="7ec71-109">Wenn der Konstruktor ausfällt, empfängt dieser Parameter einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7ec71-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="7ec71-110">Wenn dies auftritt, befindet sich das Objekt nicht in einem gültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="7ec71-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="7ec71-111">Aus Gründen der Abwärtskompatibilität mit früheren Versionen von "straumbase. lib" ist dieser Parameter standardmäßig **null**.</span><span class="sxs-lookup"><span data-stu-id="7ec71-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="7ec71-112">Die Übergabe eines Werts ungleich **null** wird jedoch bevorzugt, sodass der Aufrufer den Status des Objekts überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="7ec71-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ec71-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ec71-113">Requirements</span></span>



| <span data-ttu-id="7ec71-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ec71-114">Requirement</span></span> | <span data-ttu-id="7ec71-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7ec71-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec71-116">Header</span><span class="sxs-lookup"><span data-stu-id="7ec71-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7ec71-117"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ec71-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7ec71-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7ec71-118">Library</span></span><br/> | <dl> <span data-ttu-id="7ec71-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7ec71-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ec71-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ec71-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec71-121">**Cammsgevent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7ec71-121">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




