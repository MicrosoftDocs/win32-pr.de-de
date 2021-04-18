---
description: Die checkConnect-Methode bestimmt, ob eine PIN-Verbindung geeignet ist.
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Cbaseoutputpin. checkConnect-Methode (amfilter. h)
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
ms.openlocfilehash: f3274e47e9a77d86f350c17aaca04ec0cdb95ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368600"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="3136a-103">Cbaseoutputpin. checkConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="3136a-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="3136a-104">Die- `CheckConnect` Methode bestimmt, ob eine PIN-Verbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="3136a-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="3136a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3136a-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="3136a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3136a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3136a-107">*ppin*</span><span class="sxs-lookup"><span data-stu-id="3136a-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="3136a-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="3136a-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3136a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3136a-109">Return value</span></span>

<span data-ttu-id="3136a-110">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3136a-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="3136a-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3136a-111">Return code</span></span>                                                                                               | <span data-ttu-id="3136a-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3136a-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3136a-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3136a-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="3136a-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3136a-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="3136a-115"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="3136a-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="3136a-116">Die eingabepin unterstützt [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)nicht.</span><span class="sxs-lookup"><span data-stu-id="3136a-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="3136a-117"><dt>**VFW \_ E \_ ungültige \_ Richtung**</dt></span><span class="sxs-lookup"><span data-stu-id="3136a-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="3136a-118">PIN-Anweisungen sind nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="3136a-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="3136a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3136a-119">Remarks</span></span>

<span data-ttu-id="3136a-120">Diese Methode ruft die [**cbasepin:: checkConnect**](cbasepin-checkconnect.md) -Methode der Basisklasse auf und fragt dann die Eingabe-PIN für Ihre [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="3136a-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3136a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3136a-121">Requirements</span></span>



| <span data-ttu-id="3136a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3136a-122">Requirement</span></span> | <span data-ttu-id="3136a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3136a-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3136a-124">Header</span><span class="sxs-lookup"><span data-stu-id="3136a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3136a-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3136a-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3136a-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3136a-126">Library</span></span><br/> | <dl> <span data-ttu-id="3136a-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3136a-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3136a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3136a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3136a-129">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3136a-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




