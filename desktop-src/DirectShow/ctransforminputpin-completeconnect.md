---
description: 'CTransformInputPin.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Verbindung mit einem anderen Pin ab.'
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: CTransformInputPin.CompleteConnect-Methode (Transfrm.h)
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
ms.openlocfilehash: 20f378479209b2614116ba25f51950923358f1b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085008"
---
# <a name="ctransforminputpincompleteconnect-method"></a><span data-ttu-id="c7c4f-103">CTransformInputPin.CompleteConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="c7c4f-103">CTransformInputPin.CompleteConnect method</span></span>

<span data-ttu-id="c7c4f-104">Die `CompleteConnect` -Methode schließt eine Verbindung mit einem anderen Pin ab.</span><span class="sxs-lookup"><span data-stu-id="c7c4f-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c4f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7c4f-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="c7c4f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7c4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c4f-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="c7c4f-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="c7c4f-108">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins.</span><span class="sxs-lookup"><span data-stu-id="c7c4f-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c4f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7c4f-109">Return value</span></span>

<span data-ttu-id="c7c4f-110">Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="c7c4f-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c4f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7c4f-111">Remarks</span></span>

<span data-ttu-id="c7c4f-112">Diese Methode überschreibt die [**CBasePin::CompleteConnect-Methode.**](cbasepin-completeconnect.md)</span><span class="sxs-lookup"><span data-stu-id="c7c4f-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="c7c4f-113">Sie ruft die [**CTransformFilter::CompleteConnect-Methode**](ctransformfilter-completeconnect.md) des Filters auf, die S \_ OK in der Basisklasse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c7c4f-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="c7c4f-114">Die abgeleitete Klasse kann die **CTransformFilter::CompleteConnect-Methode** überschreiben, um zusätzliche Überprüfungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c7c4f-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c4f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7c4f-115">Requirements</span></span>



| <span data-ttu-id="c7c4f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7c4f-116">Requirement</span></span> | <span data-ttu-id="c7c4f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c7c4f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c4f-118">Header</span><span class="sxs-lookup"><span data-stu-id="c7c4f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c7c4f-119"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7c4f-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c7c4f-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c7c4f-120">Library</span></span><br/> | <dl> <span data-ttu-id="c7c4f-121"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c7c4f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




