---
description: 'CBaseFilter.FindPin-Methode: Die FindPin-Methode ruft den Pin mit dem angegebenen Bezeichner ab. Diese Methode implementiert die IBaseFilter::FindPin-Methode.'
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: CBaseFilter.FindPin-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2bbef9b051a42597b2585a432f544eead4e2e0a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099818"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="02a26-104">CBaseFilter.FindPin-Methode</span><span class="sxs-lookup"><span data-stu-id="02a26-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="02a26-105">Die `FindPin` -Methode ruft den Pin mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="02a26-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="02a26-106">Diese Methode implementiert die [**IBaseFilter::FindPin-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)</span><span class="sxs-lookup"><span data-stu-id="02a26-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a26-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="02a26-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="02a26-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="02a26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02a26-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="02a26-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="02a26-110">Zeiger auf eine konstante, mit NULL endende Unicode-Zeichenfolge, die den Pin identifiziert.</span><span class="sxs-lookup"><span data-stu-id="02a26-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="02a26-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="02a26-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="02a26-112">Adresse einer Variablen, die einen Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Pins empfängt.</span><span class="sxs-lookup"><span data-stu-id="02a26-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02a26-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02a26-113">Return value</span></span>

<span data-ttu-id="02a26-114">Gibt einen der folgenden **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="02a26-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="02a26-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="02a26-115">Return code</span></span>                                                                                       | <span data-ttu-id="02a26-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02a26-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="02a26-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02a26-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="02a26-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="02a26-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="02a26-119"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="02a26-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="02a26-120">**NULL-Zeigerargument.**</span><span class="sxs-lookup"><span data-stu-id="02a26-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="02a26-121"><dt>**VFW \_ E \_ NICHT \_ GEFUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="02a26-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="02a26-122">Ein übereinstimmender Pin wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="02a26-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="02a26-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02a26-123">Remarks</span></span>

<span data-ttu-id="02a26-124">Diese Methode ruft die [**CBasePin::Name-Methode**](cbasepin-name.md) auf, um den Namen jedes Pins mit der zeichenfolge zu vergleichen, die durch den *Id-Parameter* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="02a26-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="02a26-125">Wenn die Methode erfolgreich ist, verfügt die **IPin-Schnittstelle** über einen ausstehenden Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="02a26-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="02a26-126">Stellen Sie sicher, dass Sie es freigeben, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="02a26-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a26-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02a26-127">Requirements</span></span>



| <span data-ttu-id="02a26-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02a26-128">Requirement</span></span> | <span data-ttu-id="02a26-129">Wert</span><span class="sxs-lookup"><span data-stu-id="02a26-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02a26-130">Header</span><span class="sxs-lookup"><span data-stu-id="02a26-130">Header</span></span><br/>  | <dl> <span data-ttu-id="02a26-131"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="02a26-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="02a26-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02a26-132">Library</span></span><br/> | <dl> <span data-ttu-id="02a26-133"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="02a26-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02a26-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="02a26-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a26-135">**CBaseFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="02a26-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




