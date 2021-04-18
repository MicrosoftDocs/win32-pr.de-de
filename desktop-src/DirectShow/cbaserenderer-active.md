---
description: Die aktive Methode wird aufgerufen, wenn der Zustand zum Anhalten oder ausführen gewechselt wird.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: Cbaserderderer. Active-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11593ffb25a953f4269d84ee2b9c9d884a23e5fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371605"
---
# <a name="cbaserendereractive-method"></a><span data-ttu-id="9a814-103">Cbaserderderer. Active-Methode</span><span class="sxs-lookup"><span data-stu-id="9a814-103">CBaseRenderer.Active method</span></span>

<span data-ttu-id="9a814-104">Die- `Active` Methode wird aufgerufen, wenn der Zustand zum Anhalten oder ausführen gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="9a814-104">The `Active` method is called when the state is switched to paused or running.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a814-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a814-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="9a814-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a814-106">Parameters</span></span>

<span data-ttu-id="9a814-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9a814-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a814-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a814-108">Return value</span></span>

<span data-ttu-id="9a814-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="9a814-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a814-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a814-110">Remarks</span></span>

<span data-ttu-id="9a814-111">Die Eingabe-PIN ruft diese Methode von ihrer eigenen [**crendererinputpin:: Active**](crendererinputpin-active.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="9a814-111">The input pin calls this method from its own [**CRendererInputPin::Active**](crendererinputpin-active.md) method.</span></span> <span data-ttu-id="9a814-112">Diese Methode führt in der Basisklasse keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="9a814-112">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a814-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a814-113">Requirements</span></span>



| <span data-ttu-id="9a814-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a814-114">Requirement</span></span> | <span data-ttu-id="9a814-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9a814-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a814-116">Header</span><span class="sxs-lookup"><span data-stu-id="9a814-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9a814-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a814-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a814-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a814-118">Library</span></span><br/> | <dl> <span data-ttu-id="9a814-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9a814-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a814-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a814-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a814-121">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9a814-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




