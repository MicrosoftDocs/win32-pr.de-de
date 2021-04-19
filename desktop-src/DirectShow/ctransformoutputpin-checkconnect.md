---
description: Die checkConnect-Methode bestimmt, ob eine PIN-Verbindung geeignet ist.
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Ctransformoutputpin. checkConnect-Methode (Transfrm. h)
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
ms.openlocfilehash: b9a20eb8d3e20679cb8805d3a1cd8e167ef0bfd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356030"
---
# <a name="ctransformoutputpincheckconnect-method"></a><span data-ttu-id="f52dc-103">Ctransformoutputpin. checkConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="f52dc-103">CTransformOutputPin.CheckConnect method</span></span>

<span data-ttu-id="f52dc-104">Die- `CheckConnect` Methode bestimmt, ob eine PIN-Verbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f52dc-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f52dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f52dc-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="f52dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f52dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f52dc-107">*ppin*</span><span class="sxs-lookup"><span data-stu-id="f52dc-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="f52dc-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="f52dc-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f52dc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f52dc-109">Return value</span></span>

<span data-ttu-id="f52dc-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f52dc-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f52dc-111">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="f52dc-111">Possible values include the following.</span></span>



| <span data-ttu-id="f52dc-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f52dc-112">Return code</span></span>                                                                                  | <span data-ttu-id="f52dc-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f52dc-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="f52dc-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f52dc-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f52dc-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f52dc-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="f52dc-116"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="f52dc-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="f52dc-117">Die Eingabe-PIN des Filters ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="f52dc-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f52dc-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f52dc-118">Remarks</span></span>

<span data-ttu-id="f52dc-119">Diese Methode überschreibt die [**cbaseoutputpin:: checkConnect**](cbaseoutputpin-checkconnect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f52dc-119">This method overrides the [**CBaseOutputPin::CheckConnect**](cbaseoutputpin-checkconnect.md) method.</span></span> <span data-ttu-id="f52dc-120">Er ruft die [**ctransformfilter:: checkConnect**](ctransformfilter-checkconnect.md) -Methode des Filters auf, die \_ in der Basisklasse den Wert s OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f52dc-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="f52dc-121">Die abgeleitete Klasse kann die **ctransformfilter:: checkConnect** -Methode überschreiben, um zusätzliche Überprüfungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f52dc-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="f52dc-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f52dc-122">Requirements</span></span>



| <span data-ttu-id="f52dc-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f52dc-123">Requirement</span></span> | <span data-ttu-id="f52dc-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f52dc-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f52dc-125">Header</span><span class="sxs-lookup"><span data-stu-id="f52dc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f52dc-126"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f52dc-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f52dc-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f52dc-127">Library</span></span><br/> | <dl> <span data-ttu-id="f52dc-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f52dc-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




