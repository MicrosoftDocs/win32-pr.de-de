---
description: Die checkConnect-Methode bestimmt, ob eine PIN-Verbindung geeignet ist.
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Ctransforminputpin. checkConnect-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e10c174a4e295576cfa9ce902faeac889f5a6a9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368454"
---
# <a name="ctransforminputpincheckconnect-method"></a><span data-ttu-id="24075-103">Ctransforminputpin. checkConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="24075-103">CTransformInputPin.CheckConnect method</span></span>

<span data-ttu-id="24075-104">Die- `CheckConnect` Methode bestimmt, ob eine PIN-Verbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="24075-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="24075-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="24075-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="24075-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="24075-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24075-107">*ppin*</span><span class="sxs-lookup"><span data-stu-id="24075-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="24075-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="24075-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24075-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24075-109">Return value</span></span>

<span data-ttu-id="24075-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="24075-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="24075-111">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="24075-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="24075-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="24075-112">Return code</span></span>                                                                                               | <span data-ttu-id="24075-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24075-113">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="24075-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="24075-114"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="24075-115">Erfolg</span><span class="sxs-lookup"><span data-stu-id="24075-115">Success</span></span><br/>             |
| <dl> <span data-ttu-id="24075-116"><dt>**VFW \_ E \_ ungültige \_ Richtung**</dt></span><span class="sxs-lookup"><span data-stu-id="24075-116"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="24075-117">Falsche PIN-Richtung</span><span class="sxs-lookup"><span data-stu-id="24075-117">Wrong pin direction</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="24075-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24075-118">Remarks</span></span>

<span data-ttu-id="24075-119">Diese Methode überschreibt die [**cbasepin:: checkConnect**](cbasepin-checkconnect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="24075-119">This method overrides the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method.</span></span> <span data-ttu-id="24075-120">Er ruft die [**ctransformfilter:: checkConnect**](ctransformfilter-checkconnect.md) -Methode des Filters auf, die \_ in der Basisklasse den Wert s OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="24075-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="24075-121">Die abgeleitete Klasse kann die **ctransformfilter:: checkConnect** -Methode überschreiben, um zusätzliche Überprüfungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="24075-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="24075-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24075-122">Requirements</span></span>



| <span data-ttu-id="24075-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24075-123">Requirement</span></span> | <span data-ttu-id="24075-124">Wert</span><span class="sxs-lookup"><span data-stu-id="24075-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24075-125">Header</span><span class="sxs-lookup"><span data-stu-id="24075-125">Header</span></span><br/>  | <dl> <span data-ttu-id="24075-126"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24075-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="24075-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="24075-127">Library</span></span><br/> | <dl> <span data-ttu-id="24075-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="24075-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




