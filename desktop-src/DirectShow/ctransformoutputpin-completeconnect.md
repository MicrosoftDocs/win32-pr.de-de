---
description: 'CTransformOutputPin.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Verbindung mit einem anderen Pin ab.'
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: CTransformOutputPin.CompleteConnect-Methode (Transfrm.h)
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
ms.openlocfilehash: 7ab3d7e56473094b31c0d97d0e15c083ff61a21d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094918"
---
# <a name="ctransformoutputpincompleteconnect-method"></a><span data-ttu-id="66ac3-103">CTransformOutputPin.CompleteConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="66ac3-103">CTransformOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="66ac3-104">Die `CompleteConnect` -Methode schließt eine Verbindung mit einem anderen Pin ab.</span><span class="sxs-lookup"><span data-stu-id="66ac3-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ac3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="66ac3-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="66ac3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="66ac3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ac3-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="66ac3-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="66ac3-108">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins.</span><span class="sxs-lookup"><span data-stu-id="66ac3-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ac3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66ac3-109">Return value</span></span>

<span data-ttu-id="66ac3-110">Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="66ac3-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66ac3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66ac3-111">Remarks</span></span>

<span data-ttu-id="66ac3-112">Diese Methode überschreibt die [**CBaseOutputPin::CompleteConnect-Methode.**](cbaseoutputpin-completeconnect.md)</span><span class="sxs-lookup"><span data-stu-id="66ac3-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="66ac3-113">Sie ruft die [**CTransformFilter::CompleteConnect-Methode**](ctransformfilter-completeconnect.md) des Filters auf, die S \_ OK in der Basisklasse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="66ac3-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="66ac3-114">Die abgeleitete Klasse kann die **CTransformFilter::CompleteConnect-Methode** überschreiben, um zusätzliche Überprüfungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="66ac3-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ac3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66ac3-115">Requirements</span></span>



| <span data-ttu-id="66ac3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66ac3-116">Requirement</span></span> | <span data-ttu-id="66ac3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="66ac3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66ac3-118">Header</span><span class="sxs-lookup"><span data-stu-id="66ac3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="66ac3-119"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="66ac3-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66ac3-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="66ac3-120">Library</span></span><br/> | <dl> <span data-ttu-id="66ac3-121"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="66ac3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




