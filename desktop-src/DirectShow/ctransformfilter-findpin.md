---
description: 'Die findpin-Methode ruft die PIN mit dem angegebenen Bezeichner ab. Diese Methode implementiert die ibasefilter:: findpin-Methode.'
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: Ctransformfilter. findpin-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364721"
---
# <a name="ctransformfilterfindpin-method"></a><span data-ttu-id="04639-104">Ctransformfilter. findpin-Methode</span><span class="sxs-lookup"><span data-stu-id="04639-104">CTransformFilter.FindPin method</span></span>

<span data-ttu-id="04639-105">Die **findpin** -Methode ruft die PIN mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="04639-105">The **FindPin** method gets the pin with the specified identifier.</span></span> <span data-ttu-id="04639-106">Diese Methode implementiert die [**ibasefilter:: findpin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) -Methode.</span><span class="sxs-lookup"><span data-stu-id="04639-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="04639-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="04639-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="04639-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="04639-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04639-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="04639-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="04639-110">Breit Zeichen-Zeichenfolge, die den PIN-Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="04639-110">Wide-character string that contains the pin identifier.</span></span>

</dd> <dt>

<span data-ttu-id="04639-111">*pppin*</span><span class="sxs-lookup"><span data-stu-id="04639-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="04639-112">Empfängt einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN.</span><span class="sxs-lookup"><span data-stu-id="04639-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="04639-113">Wenn die Methode fehlschlägt, `*ppPin` wird auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04639-113">If the method fails, `*ppPin` is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04639-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04639-114">Return value</span></span>

<span data-ttu-id="04639-115">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="04639-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="04639-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="04639-116">Return code</span></span>                                                                                       | <span data-ttu-id="04639-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04639-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="04639-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04639-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="04639-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="04639-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="04639-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="04639-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="04639-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="04639-121">Insufficient memory.</span></span><br/>                       |
| <dl> <span data-ttu-id="04639-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="04639-122"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="04639-123">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="04639-123">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="04639-124"><dt>**VFW \_ E \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="04639-124"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="04639-125">Es wurde keine PIN mit diesem Bezeichner gefunden.</span><span class="sxs-lookup"><span data-stu-id="04639-125">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="04639-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04639-126">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04639-127">Bei der Implementierung dieser Methode wird [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) nicht so aufgerufen, dass Sie dem PIN-Bezeichner entspricht.</span><span class="sxs-lookup"><span data-stu-id="04639-127">The implementation of this method does not call [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) to match the pin identifier.</span></span> <span data-ttu-id="04639-128">Stattdessen geht die Methode davon aus, dass die Eingabe-PIN "in" und die Ausgabe-PIN als "out" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="04639-128">Instead, the method assumes that the input pin is named "In", and the output pin is named "Out".</span></span> <span data-ttu-id="04639-129">Wenn Sie einen anderen Satz von PIN-Bezeichner verwenden, überschreiben Sie diese Methode.</span><span class="sxs-lookup"><span data-stu-id="04639-129">If you use a different set of pin identifiers, override this method.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04639-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04639-130">Requirements</span></span>



| <span data-ttu-id="04639-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04639-131">Requirement</span></span> | <span data-ttu-id="04639-132">Wert</span><span class="sxs-lookup"><span data-stu-id="04639-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04639-133">Header</span><span class="sxs-lookup"><span data-stu-id="04639-133">Header</span></span><br/>  | <dl> <span data-ttu-id="04639-134"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04639-134"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="04639-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="04639-135">Library</span></span><br/> | <dl> <span data-ttu-id="04639-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="04639-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04639-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04639-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04639-138">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="04639-138">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




