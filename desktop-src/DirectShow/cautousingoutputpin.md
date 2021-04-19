---
description: Die cautousingoutputpin-Klasse erhält Zugriff auf ein cdynamicoutputpin-Objekt und gibt Sie frei.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: Cautousingoutputpin-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371716"
---
# <a name="cautousingoutputpin-class"></a><span data-ttu-id="f9550-103">Cautousingoutputpin-Klasse</span><span class="sxs-lookup"><span data-stu-id="f9550-103">CAutoUsingOutputPin class</span></span>

<span data-ttu-id="f9550-104">Die **cautousingoutputpin** -Klasse erhält Zugriff auf ein [**cdynamicoutputpin**](cdynamicoutputpin.md) -Objekt und gibt Sie frei.</span><span class="sxs-lookup"><span data-stu-id="f9550-104">The **CAutoUsingOutputPin** class obtains and releases access to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

<span data-ttu-id="f9550-105">**Cautousingoutputpin** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f9550-105">**CAutoUsingOutputPin** has these types of members:</span></span>



| <span data-ttu-id="f9550-106">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="f9550-106">Public Methods</span></span>                                                           | <span data-ttu-id="f9550-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9550-107">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="f9550-108">**Cautousingoutputpin**</span><span class="sxs-lookup"><span data-stu-id="f9550-108">**CAutoUsingOutputPin**</span></span>](cautousingoutputpin-cautousingoutputpin.md)   | <span data-ttu-id="f9550-109">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f9550-109">Constructor method.</span></span> <span data-ttu-id="f9550-110">Erhält Zugriff auf die angegebene PIN.</span><span class="sxs-lookup"><span data-stu-id="f9550-110">Obtains access to the specified pin.</span></span> |
| [<span data-ttu-id="f9550-111">**~ Cautousingoutputpin**</span><span class="sxs-lookup"><span data-stu-id="f9550-111">**~CAutoUsingOutputPin**</span></span>](cautousingoutputpin--cautousingoutputpin.md) | <span data-ttu-id="f9550-112">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f9550-112">Destructor method.</span></span> <span data-ttu-id="f9550-113">Erhält Zugriff auf die angegebene PIN.</span><span class="sxs-lookup"><span data-stu-id="f9550-113">Obtains access to the specified pin.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="f9550-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9550-114">Remarks</span></span>

<span data-ttu-id="f9550-115">Wenn bestimmte Methoden für [**cdynamicoutputpin**](cdynamicoutputpin.md)aufgerufen werden, muss der Aufrufer Zugriff auf die PIN erhalten und diesen Zugriff freigeben.</span><span class="sxs-lookup"><span data-stu-id="f9550-115">When certain methods are called on [**CDynamicOutputPin**](cdynamicoutputpin.md), the caller must obtain access to the pin and then release that access.</span></span> <span data-ttu-id="f9550-116">Der Aufrufer verwendet die [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode, um Zugriff zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f9550-116">To obtain access, the caller uses the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method.</span></span> <span data-ttu-id="f9550-117">Zum Freigeben des Zugriffs wird die [**cdynamicoutputpin:: stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f9550-117">To release access, it calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method.</span></span> <span data-ttu-id="f9550-118">Bei der **cautousingoutputpin** -Klasse handelt es sich um eine Hilfsklasse, die diese Aufgaben in den Konstruktor-und dekonstruktormethoden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f9550-118">The **CAutoUsingOutputPin** class is a helper class that handles these tasks in its constructor and destructor methods.</span></span> <span data-ttu-id="f9550-119">Im folgenden Codebeispiel wird gezeigt, wie diese Klasse verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="f9550-119">The following code example shows how to use this class:</span></span>


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a><span data-ttu-id="f9550-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9550-120">Requirements</span></span>



| <span data-ttu-id="f9550-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9550-121">Requirement</span></span> | <span data-ttu-id="f9550-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f9550-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9550-123">Header</span><span class="sxs-lookup"><span data-stu-id="f9550-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f9550-124"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9550-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f9550-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9550-125">Library</span></span><br/> | <dl> <span data-ttu-id="f9550-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f9550-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9550-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9550-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9550-128">Basisklassen Referenz</span><span class="sxs-lookup"><span data-stu-id="f9550-128">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

 




