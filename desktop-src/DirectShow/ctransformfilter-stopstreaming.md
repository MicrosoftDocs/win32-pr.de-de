---
description: Die stopstreaming-Methode wird aufgerufen, wenn der Filter in den Zustand "beendet" wechselt.
ms.assetid: cfebfed2-4105-4dea-8d47-60d6160ee337
title: Ctransformfilter. stopstreaming-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4990b55ad87a4eb754af7101e762ce227a090993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365668"
---
# <a name="ctransformfilterstopstreaming-method"></a><span data-ttu-id="8e136-103">Ctransformfilter. stopstreaming-Methode</span><span class="sxs-lookup"><span data-stu-id="8e136-103">CTransformFilter.StopStreaming method</span></span>

<span data-ttu-id="8e136-104">Die- `StopStreaming` Methode wird aufgerufen, wenn der Filter in den Zustand "beendet" wechselt.</span><span class="sxs-lookup"><span data-stu-id="8e136-104">The `StopStreaming` method is called when the filter switches to the stopped state.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e136-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e136-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="8e136-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e136-106">Parameters</span></span>

<span data-ttu-id="8e136-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8e136-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e136-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e136-108">Return value</span></span>

<span data-ttu-id="8e136-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8e136-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e136-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e136-110">Remarks</span></span>

<span data-ttu-id="8e136-111">Diese Methode führt keine Aktion in der Basisklasse durch, aber die abgeleitete Klasse kann Sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="8e136-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e136-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e136-112">Requirements</span></span>



| <span data-ttu-id="8e136-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e136-113">Requirement</span></span> | <span data-ttu-id="8e136-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8e136-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e136-115">Header</span><span class="sxs-lookup"><span data-stu-id="8e136-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8e136-116"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e136-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8e136-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8e136-117">Library</span></span><br/> | <dl> <span data-ttu-id="8e136-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8e136-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e136-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e136-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e136-120">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8e136-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




