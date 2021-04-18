---
description: 'Die completeconnect-Methode schließt eine Verbindung mit einer Ausgabe-PIN ab. Diese Methode überschreibt die cbasepin:: completeconnect-Methode.'
ms.assetid: 32d95815-e018-4724-8cf3-8cd093ede517
title: Crendererinputpin. completeconnect-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e868693308d40fb786f201a9d7f056dd88326ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364473"
---
# <a name="crendererinputpincompleteconnect-method"></a><span data-ttu-id="151e8-104">Crendererinputpin. completeconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="151e8-104">CRendererInputPin.CompleteConnect method</span></span>

<span data-ttu-id="151e8-105">Die- `CompleteConnect` Methode schließt eine Verbindung mit einer-Ausgabepin ab.</span><span class="sxs-lookup"><span data-stu-id="151e8-105">The `CompleteConnect` method completes a connection to an output pin.</span></span> <span data-ttu-id="151e8-106">Diese Methode überschreibt die [**cbasepin:: completeconnect**](cbasepin-completeconnect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="151e8-106">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="151e8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="151e8-107">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="151e8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="151e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="151e8-109">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="151e8-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="151e8-110">Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Ausgabe-PIN</span><span class="sxs-lookup"><span data-stu-id="151e8-110">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="151e8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="151e8-111">Return value</span></span>

<span data-ttu-id="151e8-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="151e8-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="151e8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="151e8-113">Requirements</span></span>



| <span data-ttu-id="151e8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="151e8-114">Requirement</span></span> | <span data-ttu-id="151e8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="151e8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="151e8-116">Header</span><span class="sxs-lookup"><span data-stu-id="151e8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="151e8-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="151e8-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="151e8-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="151e8-118">Library</span></span><br/> | <dl> <span data-ttu-id="151e8-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="151e8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="151e8-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="151e8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="151e8-121">**Crendererinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="151e8-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




