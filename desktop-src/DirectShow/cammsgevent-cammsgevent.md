---
description: 'OEMMsgEvent.OEMMsgEvent-Konstruktor : Konstruktormethode.'
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: OEMMsgEvent.OEMMsgEvent-Konstruktor (Wxutil.h)
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
ms.openlocfilehash: dac72ecb97a1ea1fd2594af9c11b8a03078cf2cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096534"
---
# <a name="cammsgeventcammsgevent-constructor"></a><span data-ttu-id="ca2a9-103">OEMMsgEvent.OEMMsgEvent-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="ca2a9-103">CAMMsgEvent.CAMMsgEvent constructor</span></span>

<span data-ttu-id="ca2a9-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ca2a9-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca2a9-105">Syntax</span></span>


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="ca2a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca2a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca2a9-107">*Phr*</span><span class="sxs-lookup"><span data-stu-id="ca2a9-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ca2a9-108">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="ca2a9-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="ca2a9-109">Wenn der Konstruktor fehlschlägt, empfängt dieser Parameter einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ca2a9-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="ca2a9-110">In diesem Fall befindet sich das Objekt nicht in einem gültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="ca2a9-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="ca2a9-111">Aus Gründen der Abwärtskompatibilität mit früheren Versionen von strmbase.lib wird dieser Parameter standardmäßig auf **NULL festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="ca2a9-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="ca2a9-112">Die Übergabe eines Werts, der nicht **NULL** ist, wird jedoch bevorzugt, damit der Aufrufer den Status des Objekts überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="ca2a9-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca2a9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca2a9-113">Requirements</span></span>



| <span data-ttu-id="ca2a9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca2a9-114">Requirement</span></span> | <span data-ttu-id="ca2a9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ca2a9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2a9-116">Header</span><span class="sxs-lookup"><span data-stu-id="ca2a9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ca2a9-117"><dt>Wxutil.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="ca2a9-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ca2a9-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca2a9-118">Library</span></span><br/> | <dl> <span data-ttu-id="ca2a9-119"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ca2a9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca2a9-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ca2a9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca2a9-121">**CAMMsgEvent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ca2a9-121">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




