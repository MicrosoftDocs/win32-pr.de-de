---
description: Die getrealstate-Methode ruft den Filter Zustand ab.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Cbaserderderer. getrealstate-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356375"
---
# <a name="cbaserenderergetrealstate-method"></a><span data-ttu-id="5b466-103">Cbaserderderer. getrealstate-Methode</span><span class="sxs-lookup"><span data-stu-id="5b466-103">CBaseRenderer.GetRealState method</span></span>

<span data-ttu-id="5b466-104">Die- `GetRealState` Methode ruft den Filter Zustand ab.</span><span class="sxs-lookup"><span data-stu-id="5b466-104">The `GetRealState` method retrieves the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b466-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b466-105">Syntax</span></span>


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a><span data-ttu-id="5b466-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b466-106">Parameters</span></span>

<span data-ttu-id="5b466-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5b466-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b466-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b466-108">Return value</span></span>

<span data-ttu-id="5b466-109">Gibt den Wert des [**cbasefilter:: m- \_ Zustands**](cbasefilter-m-state.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="5b466-109">Returns the value of [**CBaseFilter::m\_State**](cbasefilter-m-state.md).</span></span> <span data-ttu-id="5b466-110">Der Wert ist ein Member des Enumerationstyps [**Filter \_ Status**](/windows/win32/api/strmif/ne-strmif-filter_state) .</span><span class="sxs-lookup"><span data-stu-id="5b466-110">The value is a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b466-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b466-111">Remarks</span></span>

<span data-ttu-id="5b466-112">Diese Methode stellt eine einfachere Alternative zur [**cbaserdenderer:: GetState**](cbaserenderer-getstate.md) -Methode zur internen Verwendung bereit.</span><span class="sxs-lookup"><span data-stu-id="5b466-112">This method provides a simpler alternative to the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method, for internal use.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b466-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b466-113">Requirements</span></span>



| <span data-ttu-id="5b466-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b466-114">Requirement</span></span> | <span data-ttu-id="5b466-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5b466-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b466-116">Header</span><span class="sxs-lookup"><span data-stu-id="5b466-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5b466-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b466-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b466-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5b466-118">Library</span></span><br/> | <dl> <span data-ttu-id="5b466-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5b466-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b466-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b466-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b466-121">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5b466-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




