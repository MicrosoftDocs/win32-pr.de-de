---
description: Die completeconnect-Methode schließt eine Verbindung mit einer anderen Pin ab.
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: Ctransformoutputpin. completeconnect-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d0c9c9fc7096191d7cdedffa21e2639fa0750ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362150"
---
# <a name="ctransformoutputpincompleteconnect-method"></a><span data-ttu-id="33819-103">Ctransformoutputpin. completeconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="33819-103">CTransformOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="33819-104">Die- `CompleteConnect` Methode schließt eine Verbindung mit einer anderen Pin ab.</span><span class="sxs-lookup"><span data-stu-id="33819-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="33819-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33819-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="33819-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33819-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33819-107">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="33819-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="33819-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen Pin.</span><span class="sxs-lookup"><span data-stu-id="33819-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33819-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33819-109">Return value</span></span>

<span data-ttu-id="33819-110">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="33819-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33819-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33819-111">Remarks</span></span>

<span data-ttu-id="33819-112">Diese Methode überschreibt die [**cbaseoutputpin:: completeconnect**](cbaseoutputpin-completeconnect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="33819-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="33819-113">Er ruft die [**ctransformfilter:: completeconnect**](ctransformfilter-completeconnect.md) -Methode des Filters auf, die \_ in der Basisklasse "s OK" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="33819-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="33819-114">Die abgeleitete Klasse kann die **ctransformfilter:: completeconnect** -Methode überschreiben, um zusätzliche Überprüfungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="33819-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="33819-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33819-115">Requirements</span></span>



| <span data-ttu-id="33819-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33819-116">Requirement</span></span> | <span data-ttu-id="33819-117">Wert</span><span class="sxs-lookup"><span data-stu-id="33819-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33819-118">Header</span><span class="sxs-lookup"><span data-stu-id="33819-118">Header</span></span><br/>  | <dl> <span data-ttu-id="33819-119"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33819-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="33819-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33819-120">Library</span></span><br/> | <dl> <span data-ttu-id="33819-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="33819-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




