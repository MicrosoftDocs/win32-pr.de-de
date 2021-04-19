---
description: Die setabortsignal-Methode legt ein Flag fest, das angibt, ob das Rendering beendet und weitere Beispiele abgelehnt werden sollen.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Cbaserderderer. * tabortsignal-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369123"
---
# <a name="cbaserenderersetabortsignal-method"></a><span data-ttu-id="29295-103">Cbaserderderer. \* tabortsignal-Methode</span><span class="sxs-lookup"><span data-stu-id="29295-103">CBaseRenderer.SetAbortSignal method</span></span>

<span data-ttu-id="29295-104">Die- `SetAbortSignal` Methode legt ein Flag fest, das angibt, ob das Rendering beendet und weitere Beispiele abgelehnt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="29295-104">The `SetAbortSignal` method sets a flag which indicates whether to stop rendering and reject further samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="29295-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29295-105">Syntax</span></span>


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a><span data-ttu-id="29295-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="29295-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29295-107">*babort*</span><span class="sxs-lookup"><span data-stu-id="29295-107">*bAbort*</span></span> 
</dt> <dd>

<span data-ttu-id="29295-108">Boolescher Wert, der angibt, ob das Rendering beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29295-108">Boolean value indicating whether to stop rendering.</span></span> <span data-ttu-id="29295-109">Wenn der Wert **true** ist, werden keine weiteren Beispiele für den Filter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29295-109">If **TRUE**, the filter will not render any more samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29295-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29295-110">Return value</span></span>

<span data-ttu-id="29295-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="29295-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29295-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29295-112">Remarks</span></span>

<span data-ttu-id="29295-113">Diese Methode legt das Flag [**cbaserdenderer:: m \_ babort**](cbaserenderer-m-babort.md) fest.</span><span class="sxs-lookup"><span data-stu-id="29295-113">This method sets the [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="29295-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29295-114">Requirements</span></span>



| <span data-ttu-id="29295-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29295-115">Requirement</span></span> | <span data-ttu-id="29295-116">Wert</span><span class="sxs-lookup"><span data-stu-id="29295-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29295-117">Header</span><span class="sxs-lookup"><span data-stu-id="29295-117">Header</span></span><br/>  | <dl> <span data-ttu-id="29295-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29295-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="29295-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="29295-119">Library</span></span><br/> | <dl> <span data-ttu-id="29295-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="29295-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29295-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29295-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29295-122">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="29295-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




