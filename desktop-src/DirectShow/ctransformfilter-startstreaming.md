---
description: Die startstreaming-Methode wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt.
ms.assetid: 1e3bbca7-b5b1-41fd-8f70-b7ef39c9491b
title: Ctransformfilter. startstreaming-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50df2db2aada7f96744af5e553f474818594d399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361401"
---
# <a name="ctransformfilterstartstreaming-method"></a><span data-ttu-id="ab511-103">Ctransformfilter. startstreaming-Methode</span><span class="sxs-lookup"><span data-stu-id="ab511-103">CTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="ab511-104">Die- `StartStreaming` Methode wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="ab511-104">The `StartStreaming` method is called when the filter switches to the paused state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab511-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab511-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="ab511-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab511-106">Parameters</span></span>

<span data-ttu-id="ab511-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ab511-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab511-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab511-108">Return value</span></span>

<span data-ttu-id="ab511-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ab511-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab511-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab511-110">Remarks</span></span>

<span data-ttu-id="ab511-111">Diese Methode führt keine Aktion in der Basisklasse durch, aber die abgeleitete Klasse kann Sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="ab511-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab511-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab511-112">Requirements</span></span>



| <span data-ttu-id="ab511-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab511-113">Requirement</span></span> | <span data-ttu-id="ab511-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ab511-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab511-115">Header</span><span class="sxs-lookup"><span data-stu-id="ab511-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ab511-116"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab511-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ab511-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab511-117">Library</span></span><br/> | <dl> <span data-ttu-id="ab511-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ab511-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab511-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab511-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab511-120">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ab511-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




