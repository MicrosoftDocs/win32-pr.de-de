---
description: 'CBaseOutputPin.CheckConnect-Methode: Die CheckConnect-Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.'
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: CBaseOutputPin.CheckConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ea5ad32de18046f3d23145d82e971391c3e304c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096188"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="4e0a5-103">CBaseOutputPin.CheckConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="4e0a5-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="4e0a5-104">Die `CheckConnect` -Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e0a5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e0a5-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="4e0a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e0a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e0a5-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="4e0a5-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="4e0a5-108">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e0a5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e0a5-109">Return value</span></span>

<span data-ttu-id="4e0a5-110">Gibt einen der folgenden **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="4e0a5-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4e0a5-111">Return code</span></span>                                                                                               | <span data-ttu-id="4e0a5-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e0a5-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4e0a5-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4e0a5-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="4e0a5-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="4e0a5-115"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="4e0a5-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="4e0a5-116">Der Eingabepin unterstützt [**IMemInputPin nicht.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)</span><span class="sxs-lookup"><span data-stu-id="4e0a5-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="4e0a5-117"><dt>**VFW \_ E \_ UNGÜLTIGE \_ RICHTUNG**</dt></span><span class="sxs-lookup"><span data-stu-id="4e0a5-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="4e0a5-118">Pin-Anweisungen sind nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="4e0a5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e0a5-119">Remarks</span></span>

<span data-ttu-id="4e0a5-120">Diese Methode ruft die [**CBasePin::CheckConnect-Methode**](cbasepin-checkconnect.md) der Basisklasse auf und fragt dann den Eingabepin für seine [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ab.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e0a5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e0a5-121">Requirements</span></span>



| <span data-ttu-id="4e0a5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e0a5-122">Requirement</span></span> | <span data-ttu-id="4e0a5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4e0a5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0a5-124">Header</span><span class="sxs-lookup"><span data-stu-id="4e0a5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4e0a5-125"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="4e0a5-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e0a5-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e0a5-126">Library</span></span><br/> | <dl> <span data-ttu-id="4e0a5-127"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4e0a5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e0a5-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4e0a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e0a5-129">**CBaseOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4e0a5-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




