---
description: Die completeconnect-Methode schließt eine Verbindung mit einer anderen Pin ab.
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: Ctransforminputpin. completeconnect-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 455517968481b9333fbeba590aca644b34b2f5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366715"
---
# <a name="ctransforminputpincompleteconnect-method"></a><span data-ttu-id="3f88d-103">Ctransforminputpin. completeconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="3f88d-103">CTransformInputPin.CompleteConnect method</span></span>

<span data-ttu-id="3f88d-104">Die- `CompleteConnect` Methode schließt eine Verbindung mit einer anderen Pin ab.</span><span class="sxs-lookup"><span data-stu-id="3f88d-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f88d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f88d-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="3f88d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f88d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f88d-107">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="3f88d-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="3f88d-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen Pin.</span><span class="sxs-lookup"><span data-stu-id="3f88d-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f88d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f88d-109">Return value</span></span>

<span data-ttu-id="3f88d-110">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3f88d-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f88d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f88d-111">Remarks</span></span>

<span data-ttu-id="3f88d-112">Diese Methode überschreibt die [**cbasepin:: completeconnect**](cbasepin-completeconnect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3f88d-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="3f88d-113">Er ruft die [**ctransformfilter:: completeconnect**](ctransformfilter-completeconnect.md) -Methode des Filters auf, die \_ in der Basisklasse "s OK" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3f88d-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="3f88d-114">Die abgeleitete Klasse kann die **ctransformfilter:: completeconnect** -Methode überschreiben, um zusätzliche Überprüfungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3f88d-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f88d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f88d-115">Requirements</span></span>



| <span data-ttu-id="3f88d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f88d-116">Requirement</span></span> | <span data-ttu-id="3f88d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3f88d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f88d-118">Header</span><span class="sxs-lookup"><span data-stu-id="3f88d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3f88d-119"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f88d-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3f88d-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f88d-120">Library</span></span><br/> | <dl> <span data-ttu-id="3f88d-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3f88d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




