---
description: Die EndRun-Methode wechselt zum beendeten oder angehaltenen Modus.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Ccmdqueue. EndRun-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367ef026402ff191ceb04657c21d6f3bd11ebe73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356312"
---
# <a name="ccmdqueueendrun-method"></a><span data-ttu-id="de27b-103">Ccmdqueue. EndRun-Methode</span><span class="sxs-lookup"><span data-stu-id="de27b-103">CCmdQueue.EndRun method</span></span>

<span data-ttu-id="de27b-104">Die `EndRun` Methode wechselt zum beendeten oder angehaltenen Modus.</span><span class="sxs-lookup"><span data-stu-id="de27b-104">The `EndRun` method switches to the stopped or paused mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="de27b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de27b-105">Syntax</span></span>


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a><span data-ttu-id="de27b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="de27b-106">Parameters</span></span>

<span data-ttu-id="de27b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="de27b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de27b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de27b-108">Return value</span></span>

<span data-ttu-id="de27b-109">Gibt einen **HRESULT** -Wert zurück, der von der-Implementierung abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="de27b-109">Returns an **HRESULT** value that depends on the implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="de27b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de27b-110">Remarks</span></span>

<span data-ttu-id="de27b-111">Die Zeit Zuordnung zwischen der streamzeit und der Präsentationszeit ist nicht bekannt, nachdem diese Element Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="de27b-111">Time mapping between stream time and presentation time is not known after this member function has been called.</span></span> <span data-ttu-id="de27b-112">Verwenden Sie die Funktion [**ccmdqueue:: Run**](ccmdqueue-run.md) Member, um diese Zuordnung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="de27b-112">Call the [**CCmdQueue::Run**](ccmdqueue-run.md) member function to carry out this mapping.</span></span>

## <a name="requirements"></a><span data-ttu-id="de27b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de27b-113">Requirements</span></span>



| <span data-ttu-id="de27b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de27b-114">Requirement</span></span> | <span data-ttu-id="de27b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="de27b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de27b-116">Header</span><span class="sxs-lookup"><span data-stu-id="de27b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="de27b-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de27b-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de27b-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de27b-118">Library</span></span><br/> | <dl> <span data-ttu-id="de27b-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="de27b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de27b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de27b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de27b-121">**Ccmdqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="de27b-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




