---
description: Die preparerender-Methode wird aufgerufen, bevor der Filter ein Beispiel rendert.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Cbaserderderer. preparerender-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374013"
---
# <a name="cbaserendererpreparerender-method"></a><span data-ttu-id="de75c-103">Cbaserderderer. preparerender-Methode</span><span class="sxs-lookup"><span data-stu-id="de75c-103">CBaseRenderer.PrepareRender method</span></span>

<span data-ttu-id="de75c-104">Die- `PrepareRender` Methode wird aufgerufen, bevor der Filter eine Stichprobe rendert.</span><span class="sxs-lookup"><span data-stu-id="de75c-104">The `PrepareRender` method is called before the filter renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="de75c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de75c-105">Syntax</span></span>


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a><span data-ttu-id="de75c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="de75c-106">Parameters</span></span>

<span data-ttu-id="de75c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="de75c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de75c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de75c-108">Return value</span></span>

<span data-ttu-id="de75c-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="de75c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de75c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de75c-110">Remarks</span></span>

<span data-ttu-id="de75c-111">Der Filter ruft diese Methode auf, bevor die [**cbaserdenderer:: onreceivefirstsample**](cbaserenderer-onreceivefirstsample.md) -Methode oder die [**cbaserdenderer:: Rendering**](cbaserenderer-render.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="de75c-111">The filter calls this method before it calls the [**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) method or the [**CBaseRenderer::Render**](cbaserenderer-render.md) method.</span></span> <span data-ttu-id="de75c-112">`PrepareRender` führt in der Basisklasse keine Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="de75c-112">`PrepareRender` does not do anything in the base class.</span></span> <span data-ttu-id="de75c-113">Die abgeleitete Klasse kann Sie außer Kraft setzen, um vor dem Rendering erforderliche Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="de75c-113">The derived class can override it to perform any actions required before rendering.</span></span> <span data-ttu-id="de75c-114">Ein Videorenderer kann diese Methode z. b. überschreiben, um die Palette zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="de75c-114">For example, a video renderer can override this method to realize its palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="de75c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de75c-115">Requirements</span></span>



| <span data-ttu-id="de75c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de75c-116">Requirement</span></span> | <span data-ttu-id="de75c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="de75c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de75c-118">Header</span><span class="sxs-lookup"><span data-stu-id="de75c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="de75c-119"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de75c-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de75c-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de75c-120">Library</span></span><br/> | <dl> <span data-ttu-id="de75c-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="de75c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de75c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de75c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de75c-123">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="de75c-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




