---
description: 'Ordnet eine einzelne Element Funktion und einen optionalen Satz von Parametern einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern zu, der bei nachfolgenden Aufrufen der cmediaevent:: aufrufen-Member-Funktion verwendet werden kann.'
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: Cmediaevent. GetIDsOfNames-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 191fa85264e4e7e22aa67f409db20cebd68f4319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361015"
---
# <a name="cmediaeventgetidsofnames-method"></a><span data-ttu-id="88061-103">Cmediaevent. GetIDsOfNames-Methode</span><span class="sxs-lookup"><span data-stu-id="88061-103">CMediaEvent.GetIDsOfNames method</span></span>

<span data-ttu-id="88061-104">Ordnet eine einzelne Element Funktion und einen optionalen Satz von Parametern einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern zu, der bei nachfolgenden Aufrufen der [**cmediaevent:: Aufrufen**](cmediaevent-invoke.md) -Member-Funktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="88061-104">Maps a single member function and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used upon subsequent calls to the [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="88061-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88061-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="88061-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="88061-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88061-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="88061-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="88061-108">Verweis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="88061-108">Reference identifier.</span></span> <span data-ttu-id="88061-109">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="88061-109">Reserved for future use.</span></span> <span data-ttu-id="88061-110">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="88061-110">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="88061-111">*rgsznames*</span><span class="sxs-lookup"><span data-stu-id="88061-111">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="88061-112">Adresse eines Zeigers auf ein zugeordnetes Array von Namen, die zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="88061-112">Address of a pointer to a passed-in array of names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="88061-113">*CNAMES*</span><span class="sxs-lookup"><span data-stu-id="88061-113">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="88061-114">Die Anzahl der zuzuordnenden Namen.</span><span class="sxs-lookup"><span data-stu-id="88061-114">Count of the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="88061-115">*lcid*</span><span class="sxs-lookup"><span data-stu-id="88061-115">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="88061-116">Der Gebiets Schema Kontext, in dem die Namen interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="88061-116">Locale context in which to interpret the names.</span></span>

</dd> <dt>

<span data-ttu-id="88061-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="88061-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="88061-118">Zeiger auf ein Array, das vom Aufrufer zugeordnet wird. jedes Element von enthält eine ID, die einem der Namen entspricht, die im *rgsznames* -Array übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="88061-118">Pointer to a caller-allocated array, each element of which contains an ID corresponding to one of the names passed in the *rgszNames* array.</span></span> <span data-ttu-id="88061-119">Das erste Element stellt den Elementnamen dar. die nachfolgenden Elemente stellen jeden der Parameter des Members dar.</span><span class="sxs-lookup"><span data-stu-id="88061-119">The first element represents the member name; the subsequent elements represent each of the member's parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88061-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88061-120">Return value</span></span>

<span data-ttu-id="88061-121">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="88061-121">Returns one of the following values.</span></span>



| <span data-ttu-id="88061-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="88061-122">Return code</span></span>                                                                                            | <span data-ttu-id="88061-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88061-123">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="88061-124"><dt>**DISP \_ E \_ unbekannte \_ CLSID**</dt></span><span class="sxs-lookup"><span data-stu-id="88061-124"><dt>**DISP\_E\_UNKNOWN\_CLSID**</dt></span></span> </dl> | <span data-ttu-id="88061-125">Die CLSID wurde nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="88061-125">The CLSID was not recognized.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="88061-126"><dt>**DISP \_ E \_ unknownname**</dt></span><span class="sxs-lookup"><span data-stu-id="88061-126"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl>    | <span data-ttu-id="88061-127">Mindestens ein Name ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="88061-127">One or more of the names were not known.</span></span> <span data-ttu-id="88061-128">Die zurückgegebenen DispIds enthalten \_ für jeden Eintrag, der einem unbekannten Namen entspricht, die DISPID unbekannt.</span><span class="sxs-lookup"><span data-stu-id="88061-128">The returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span><br/> |
| <dl> <span data-ttu-id="88061-129"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="88061-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="88061-130">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="88061-130">Out of memory.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="88061-131"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="88061-131"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="88061-132">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="88061-132">Success.</span></span><br/>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="88061-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88061-133">Requirements</span></span>



| <span data-ttu-id="88061-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88061-134">Requirement</span></span> | <span data-ttu-id="88061-135">Wert</span><span class="sxs-lookup"><span data-stu-id="88061-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88061-136">Header</span><span class="sxs-lookup"><span data-stu-id="88061-136">Header</span></span><br/>  | <dl> <span data-ttu-id="88061-137"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88061-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88061-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="88061-138">Library</span></span><br/> | <dl> <span data-ttu-id="88061-139">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="88061-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88061-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88061-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88061-141">**Cmediaevent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="88061-141">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




