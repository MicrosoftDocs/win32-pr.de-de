---
description: 'CTransformInputPin.CheckConnect-Methode: Die CheckConnect-Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.'
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: CTransformInputPin.CheckConnect-Methode (Transfrm.h)
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
ms.openlocfilehash: 3e981254677c2e0a361a0a21f125f734ff1403db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095088"
---
# <a name="ctransforminputpincheckconnect-method"></a><span data-ttu-id="fd5f5-103">CTransformInputPin.CheckConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="fd5f5-103">CTransformInputPin.CheckConnect method</span></span>

<span data-ttu-id="fd5f5-104">Die `CheckConnect` -Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd5f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd5f5-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="fd5f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd5f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd5f5-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="fd5f5-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="fd5f5-108">Zeiger auf die IPin-Schnittstelle des [**Ausgabepins.**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="fd5f5-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd5f5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd5f5-109">Return value</span></span>

<span data-ttu-id="fd5f5-110">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fd5f5-111">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="fd5f5-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fd5f5-112">Return code</span></span>                                                                                               | <span data-ttu-id="fd5f5-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd5f5-113">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="fd5f5-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fd5f5-114"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="fd5f5-115">Erfolg</span><span class="sxs-lookup"><span data-stu-id="fd5f5-115">Success</span></span><br/>             |
| <dl> <span data-ttu-id="fd5f5-116"><dt>**VFW \_ E \_ UNGÜLTIGE \_ RICHTUNG**</dt></span><span class="sxs-lookup"><span data-stu-id="fd5f5-116"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="fd5f5-117">Falsche Stecknadelrichtung</span><span class="sxs-lookup"><span data-stu-id="fd5f5-117">Wrong pin direction</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd5f5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd5f5-118">Remarks</span></span>

<span data-ttu-id="fd5f5-119">Diese Methode überschreibt die [**CBasePin::CheckConnect-Methode.**](cbasepin-checkconnect.md)</span><span class="sxs-lookup"><span data-stu-id="fd5f5-119">This method overrides the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method.</span></span> <span data-ttu-id="fd5f5-120">Sie ruft die [**CTransformFilter::CheckConnect-Methode**](ctransformfilter-checkconnect.md) des Filters auf, die S \_ OK in der Basisklasse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="fd5f5-121">Die abgeleitete Klasse kann die **CTransformFilter::CheckConnect-Methode** überschreiben, um zusätzliche Überprüfungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd5f5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd5f5-122">Requirements</span></span>



| <span data-ttu-id="fd5f5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd5f5-123">Requirement</span></span> | <span data-ttu-id="fd5f5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fd5f5-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5f5-125">Header</span><span class="sxs-lookup"><span data-stu-id="fd5f5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fd5f5-126"><dt>Transfrm.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="fd5f5-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fd5f5-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fd5f5-127">Library</span></span><br/> | <dl> <span data-ttu-id="fd5f5-128"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fd5f5-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




