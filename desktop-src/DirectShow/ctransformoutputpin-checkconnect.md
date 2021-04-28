---
description: 'CTransformOutputPin.CheckConnect-Methode: Die CheckConnect-Methode bestimmt, ob eine Pinverbindung geeignet ist.'
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: CTransformOutputPin.CheckConnect-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 190acd2fbab5206b114b57719d350e3ad5eac0c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094948"
---
# <a name="ctransformoutputpincheckconnect-method"></a><span data-ttu-id="e0c20-103">CTransformOutputPin.CheckConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="e0c20-103">CTransformOutputPin.CheckConnect method</span></span>

<span data-ttu-id="e0c20-104">Die `CheckConnect` -Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="e0c20-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c20-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0c20-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="e0c20-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0c20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0c20-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="e0c20-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c20-108">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Ausgabepins.</span><span class="sxs-lookup"><span data-stu-id="e0c20-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0c20-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0c20-109">Return value</span></span>

<span data-ttu-id="e0c20-110">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="e0c20-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e0c20-111">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="e0c20-111">Possible values include the following.</span></span>



| <span data-ttu-id="e0c20-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e0c20-112">Return code</span></span>                                                                                  | <span data-ttu-id="e0c20-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0c20-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="e0c20-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e0c20-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e0c20-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e0c20-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="e0c20-116"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="e0c20-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="e0c20-117">Der Eingabepin des Filters ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="e0c20-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e0c20-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0c20-118">Remarks</span></span>

<span data-ttu-id="e0c20-119">Diese Methode überschreibt die [**CBaseOutputPin::CheckConnect-Methode.**](cbaseoutputpin-checkconnect.md)</span><span class="sxs-lookup"><span data-stu-id="e0c20-119">This method overrides the [**CBaseOutputPin::CheckConnect**](cbaseoutputpin-checkconnect.md) method.</span></span> <span data-ttu-id="e0c20-120">Sie ruft die [**CTransformFilter::CheckConnect-Methode**](ctransformfilter-checkconnect.md) des Filters auf, die \_ S OK in der Basisklasse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e0c20-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="e0c20-121">Die abgeleitete Klasse kann die **CTransformFilter::CheckConnect-Methode** überschreiben, um zusätzliche Überprüfungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="e0c20-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c20-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0c20-122">Requirements</span></span>



| <span data-ttu-id="e0c20-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0c20-123">Requirement</span></span> | <span data-ttu-id="e0c20-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e0c20-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c20-125">Header</span><span class="sxs-lookup"><span data-stu-id="e0c20-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e0c20-126"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0c20-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e0c20-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0c20-127">Library</span></span><br/> | <dl> <span data-ttu-id="e0c20-128"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e0c20-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




