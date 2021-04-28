---
description: 'CABThread.WEBCAMThread-Konstruktor : Konstruktormethode.'
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: CABThread.MSIThread-Konstruktor (Wxutil.h)
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
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096408"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="789b2-103">CABThread.CABThread-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="789b2-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="789b2-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="789b2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="789b2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="789b2-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="789b2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="789b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="789b2-107">*Phr*</span><span class="sxs-lookup"><span data-stu-id="789b2-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="789b2-108">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="789b2-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="789b2-109">Wenn der Konstruktor fehlschlägt, empfängt dieser Parameter einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="789b2-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="789b2-110">In diesem Fall befindet sich das Objekt nicht in einem gültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="789b2-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="789b2-111">Aus Gründen der Abwärtskompatibilität mit früheren Versionen von strmbase.lib wird dieser Parameter standardmäßig auf **NULL** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="789b2-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="789b2-112">Die Übergabe eines Werts ungleich **NULL** wird jedoch bevorzugt, damit der Aufrufer den Status des Objekts überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="789b2-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="789b2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="789b2-113">Remarks</span></span>

<span data-ttu-id="789b2-114">Die Konstruktormethode erstellt den Thread nicht.</span><span class="sxs-lookup"><span data-stu-id="789b2-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="789b2-115">Um den Thread zu erstellen, rufen Sie die [**METHODE TARThread::Create**](camthread-create.md) auf.</span><span class="sxs-lookup"><span data-stu-id="789b2-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="789b2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="789b2-116">Requirements</span></span>



| <span data-ttu-id="789b2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="789b2-117">Requirement</span></span> | <span data-ttu-id="789b2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="789b2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="789b2-119">Header</span><span class="sxs-lookup"><span data-stu-id="789b2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="789b2-120"><dt>Wxutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="789b2-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="789b2-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="789b2-121">Library</span></span><br/> | <dl> <span data-ttu-id="789b2-122"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="789b2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="789b2-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="789b2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="789b2-124">**WEBCAMThread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="789b2-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




