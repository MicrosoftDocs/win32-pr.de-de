---
description: 'CSource.FindPin-Methode: Die FindPin-Methode ruft den Pin mit dem angegebenen Bezeichner ab. Diese Methode implementiert die IBaseFilter::FindPin-Methode.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: CSource.FindPin-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daa1e2404e7c6fbf1d879d71374298103bdc621f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098858"
---
# <a name="csourcefindpin-method"></a><span data-ttu-id="39da7-104">CSource.FindPin-Methode</span><span class="sxs-lookup"><span data-stu-id="39da7-104">CSource.FindPin method</span></span>

<span data-ttu-id="39da7-105">Die `FindPin` -Methode ruft den Pin mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="39da7-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="39da7-106">Diese Methode implementiert die [**IBaseFilter::FindPin-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)</span><span class="sxs-lookup"><span data-stu-id="39da7-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="39da7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="39da7-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="39da7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="39da7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39da7-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="39da7-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="39da7-110">Zeiger auf eine auf NULL beendete Zeichenfolge, die den Pin identifiziert.</span><span class="sxs-lookup"><span data-stu-id="39da7-110">Pointer to a null-terminated string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="39da7-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="39da7-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="39da7-112">Empfängt einen Zeiger auf die [**IPin-Schnittstelle des Pins.**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="39da7-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="39da7-113">Wenn die Methode fehlschlägt, \* *wird ppPin* auf NULL **festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="39da7-113">If the method fails, \**ppPin* is set to **NULL**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39da7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39da7-114">Return value</span></span>

<span data-ttu-id="39da7-115">Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="39da7-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="39da7-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="39da7-116">Return code</span></span>                                                                                       | <span data-ttu-id="39da7-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39da7-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="39da7-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="39da7-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="39da7-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="39da7-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="39da7-120"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="39da7-120"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="39da7-121"> NULL-Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="39da7-121">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="39da7-122"><dt>**VFW \_ E \_ NICHT \_ GEFUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="39da7-122"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="39da7-123">Eine Stecknadel mit diesem Bezeichner wurde nicht finden.</span><span class="sxs-lookup"><span data-stu-id="39da7-123">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="39da7-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39da7-124">Remarks</span></span>

<span data-ttu-id="39da7-125">Der erste Pin hat immer den Namen "1". der zweite Pin heißt "2"; usw.</span><span class="sxs-lookup"><span data-stu-id="39da7-125">The first pin is always named "1"; the second pin is named "2"; and so forth.</span></span> <span data-ttu-id="39da7-126">Weitere Informationen finden Sie unter [**CSourceStream::QueryId**](csourcestream-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="39da7-126">For more information, see [**CSourceStream::QueryId**](csourcestream-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39da7-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39da7-127">Requirements</span></span>



| <span data-ttu-id="39da7-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39da7-128">Requirement</span></span> | <span data-ttu-id="39da7-129">Wert</span><span class="sxs-lookup"><span data-stu-id="39da7-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39da7-130">Header</span><span class="sxs-lookup"><span data-stu-id="39da7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="39da7-131"><dt>Source.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="39da7-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="39da7-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="39da7-132">Library</span></span><br/> | <dl> <span data-ttu-id="39da7-133"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="39da7-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39da7-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="39da7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39da7-135">**CSource-Klasse**</span><span class="sxs-lookup"><span data-stu-id="39da7-135">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




