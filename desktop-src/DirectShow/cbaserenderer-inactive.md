---
description: Die inaktive Methode wird aufgerufen, wenn der Status in "beendet" versetzt wird.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Cbaserderderer. inaktive-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364873"
---
# <a name="cbaserendererinactive-method"></a><span data-ttu-id="43d21-103">Cbaserderderer. inaktive-Methode</span><span class="sxs-lookup"><span data-stu-id="43d21-103">CBaseRenderer.Inactive method</span></span>

<span data-ttu-id="43d21-104">Die- `Inactive` Methode wird aufgerufen, wenn der Zustand in "beendet" versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="43d21-104">The `Inactive` method is called when the state is switched to stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d21-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43d21-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="43d21-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43d21-106">Parameters</span></span>

<span data-ttu-id="43d21-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="43d21-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43d21-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43d21-108">Return value</span></span>

<span data-ttu-id="43d21-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="43d21-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="43d21-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43d21-110">Remarks</span></span>

<span data-ttu-id="43d21-111">Die Eingabe-PIN ruft diese Methode von ihrer eigenen [**crendererinputpin:: inaktiven**](crendererinputpin-inactive.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="43d21-111">The input pin calls this method from its own [**CRendererInputPin::Inactive**](crendererinputpin-inactive.md) method.</span></span> <span data-ttu-id="43d21-112">Der Filter Ruft die [**cbaserdenderer:: clearpdingsample**](cbaserenderer-clearpendingsample.md) -Methode auf, um das aktuelle Beispiel freizugeben.</span><span class="sxs-lookup"><span data-stu-id="43d21-112">The filter calls the [**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md) method to release the most recent sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="43d21-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43d21-113">Requirements</span></span>



| <span data-ttu-id="43d21-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43d21-114">Requirement</span></span> | <span data-ttu-id="43d21-115">Wert</span><span class="sxs-lookup"><span data-stu-id="43d21-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d21-116">Header</span><span class="sxs-lookup"><span data-stu-id="43d21-116">Header</span></span><br/>  | <dl> <span data-ttu-id="43d21-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43d21-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43d21-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43d21-118">Library</span></span><br/> | <dl> <span data-ttu-id="43d21-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="43d21-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43d21-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43d21-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d21-121">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="43d21-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




