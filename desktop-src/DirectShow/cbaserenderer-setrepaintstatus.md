---
description: Die Methode "Methode" aktiviert oder deaktiviert Repaint-Ereignisse.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Cbasererererer. abtrepaintstatus-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364465"
---
# <a name="cbaserenderersetrepaintstatus-method"></a><span data-ttu-id="30b02-103">Cbasererererer. abtrepaintstatus-Methode</span><span class="sxs-lookup"><span data-stu-id="30b02-103">CBaseRenderer.SetRepaintStatus method</span></span>

<span data-ttu-id="30b02-104">Die- `SetRepaintStatus` Methode aktiviert oder deaktiviert Repaint-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="30b02-104">The `SetRepaintStatus` method enables or disables repaint events.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30b02-105">Syntax</span></span>


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a><span data-ttu-id="30b02-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30b02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30b02-107">*brepaint*</span><span class="sxs-lookup"><span data-stu-id="30b02-107">*bRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="30b02-108">Boolescher Wert, der angibt, ob Repaint-Ereignisse aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="30b02-108">Boolean value indicating whether repaint events are enabled.</span></span> <span data-ttu-id="30b02-109">**True** gibt an, dass der Filter [**EC \_ Repaint**](ec-repaint.md) -Ereignisse an den Filter Graph-Manager sendet.</span><span class="sxs-lookup"><span data-stu-id="30b02-109">If **TRUE**, the filter will sent [**EC\_REPAINT**](ec-repaint.md) events to the filter graph manager.</span></span> <span data-ttu-id="30b02-110">Andernfalls werden keine EC- \_ Repaint-Ereignisse gesendet.</span><span class="sxs-lookup"><span data-stu-id="30b02-110">Otherwise, it will not send EC\_REPAINT events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30b02-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30b02-111">Return value</span></span>

<span data-ttu-id="30b02-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="30b02-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30b02-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30b02-113">Remarks</span></span>

<span data-ttu-id="30b02-114">Diese Methode stellt sicher, dass der Filter Graph-Manager nicht mit redundanten EC Repaint-Ereignissen überflutet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="30b02-114">This method ensures that the filter graph manager is not flooded with redundant EC\_REPAINT events.</span></span> <span data-ttu-id="30b02-115">Nachdem der Filter ein [**EC \_ Repaint**](ec-repaint.md) -Ereignis gesendet hat, wird diese Methode mit dem Wert " **true**" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="30b02-115">After the filter sends an [**EC\_REPAINT**](ec-repaint.md) event, it calls this method with the value **TRUE**.</span></span> <span data-ttu-id="30b02-116">Der Filter sendet keine weiteren EC \_ Repaint-Ereignisse, bis mehr Daten empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="30b02-116">The filter does not send more EC\_REPAINT events until it receives more data.</span></span>

## <a name="requirements"></a><span data-ttu-id="30b02-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30b02-117">Requirements</span></span>



| <span data-ttu-id="30b02-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30b02-118">Requirement</span></span> | <span data-ttu-id="30b02-119">Wert</span><span class="sxs-lookup"><span data-stu-id="30b02-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b02-120">Header</span><span class="sxs-lookup"><span data-stu-id="30b02-120">Header</span></span><br/>  | <dl> <span data-ttu-id="30b02-121"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30b02-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30b02-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30b02-122">Library</span></span><br/> | <dl> <span data-ttu-id="30b02-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="30b02-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b02-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30b02-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b02-125">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="30b02-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




