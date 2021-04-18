---
description: Konstruktormethode.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Camthread. camthread-Konstruktor (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372235"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="25305-103">Camthread. camthread-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="25305-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="25305-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="25305-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="25305-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="25305-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="25305-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25305-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25305-107">*PHR*</span><span class="sxs-lookup"><span data-stu-id="25305-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="25305-108">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="25305-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="25305-109">Wenn der Konstruktor ausfällt, empfängt dieser Parameter einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="25305-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="25305-110">Wenn dies auftritt, befindet sich das Objekt nicht in einem gültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="25305-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="25305-111">Aus Gründen der Abwärtskompatibilität mit früheren Versionen von "straumbase. lib" ist dieser Parameter standardmäßig **null**.</span><span class="sxs-lookup"><span data-stu-id="25305-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="25305-112">Die Übergabe eines Werts ungleich **null** wird jedoch bevorzugt, sodass der Aufrufer den Status des Objekts überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="25305-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25305-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25305-113">Remarks</span></span>

<span data-ttu-id="25305-114">Die Konstruktormethode erstellt nicht den Thread.</span><span class="sxs-lookup"><span data-stu-id="25305-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="25305-115">Um den Thread zu erstellen, rufen Sie die Methode " [**camthread:: Create**](camthread-create.md) " auf.</span><span class="sxs-lookup"><span data-stu-id="25305-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="25305-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25305-116">Requirements</span></span>



| <span data-ttu-id="25305-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25305-117">Requirement</span></span> | <span data-ttu-id="25305-118">Wert</span><span class="sxs-lookup"><span data-stu-id="25305-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25305-119">Header</span><span class="sxs-lookup"><span data-stu-id="25305-119">Header</span></span><br/>  | <dl> <span data-ttu-id="25305-120"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25305-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="25305-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25305-121">Library</span></span><br/> | <dl> <span data-ttu-id="25305-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="25305-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25305-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25305-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25305-124">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="25305-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




