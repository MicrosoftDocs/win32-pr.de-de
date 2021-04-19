---
description: 'Die findpin-Methode ruft die PIN mit dem angegebenen Bezeichner ab. Diese Methode implementiert die ibasefilter:: findpin-Methode.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: CSource. findpin-Methode (Quelle. h)
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
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355892"
---
# <a name="csourcefindpin-method"></a><span data-ttu-id="86f46-104">CSource. findpin-Methode</span><span class="sxs-lookup"><span data-stu-id="86f46-104">CSource.FindPin method</span></span>

<span data-ttu-id="86f46-105">Die- `FindPin` Methode ruft die PIN mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="86f46-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="86f46-106">Diese Methode implementiert die [**ibasefilter:: findpin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) -Methode.</span><span class="sxs-lookup"><span data-stu-id="86f46-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86f46-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="86f46-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="86f46-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="86f46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86f46-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="86f46-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="86f46-110">Zeiger auf eine mit NULL endenden Zeichenfolge, die die PIN identifiziert.</span><span class="sxs-lookup"><span data-stu-id="86f46-110">Pointer to a null-terminated string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="86f46-111">*pppin*</span><span class="sxs-lookup"><span data-stu-id="86f46-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="86f46-112">Empfängt einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN.</span><span class="sxs-lookup"><span data-stu-id="86f46-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="86f46-113">Wenn die Methode fehlschlägt, \* wird *pppin* auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="86f46-113">If the method fails, \**ppPin* is set to **NULL**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86f46-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86f46-114">Return value</span></span>

<span data-ttu-id="86f46-115">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="86f46-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="86f46-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="86f46-116">Return code</span></span>                                                                                       | <span data-ttu-id="86f46-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86f46-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="86f46-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86f46-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="86f46-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="86f46-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="86f46-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="86f46-120"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="86f46-121">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="86f46-121">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="86f46-122"><dt>**VFW \_ E \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="86f46-122"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="86f46-123">Es wurde keine PIN mit diesem Bezeichner gefunden.</span><span class="sxs-lookup"><span data-stu-id="86f46-123">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86f46-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86f46-124">Remarks</span></span>

<span data-ttu-id="86f46-125">Die erste Pin hat immer den Namen "1". die zweite Pin hat den Namen "2". und so weiter.</span><span class="sxs-lookup"><span data-stu-id="86f46-125">The first pin is always named "1"; the second pin is named "2"; and so forth.</span></span> <span data-ttu-id="86f46-126">Weitere Informationen finden Sie unter [**csourcestream:: QueryId**](csourcestream-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="86f46-126">For more information, see [**CSourceStream::QueryId**](csourcestream-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86f46-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86f46-127">Requirements</span></span>



| <span data-ttu-id="86f46-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86f46-128">Requirement</span></span> | <span data-ttu-id="86f46-129">Wert</span><span class="sxs-lookup"><span data-stu-id="86f46-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86f46-130">Header</span><span class="sxs-lookup"><span data-stu-id="86f46-130">Header</span></span><br/>  | <dl> <span data-ttu-id="86f46-131"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86f46-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="86f46-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="86f46-132">Library</span></span><br/> | <dl> <span data-ttu-id="86f46-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="86f46-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86f46-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86f46-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f46-135">**CSource-Klasse**</span><span class="sxs-lookup"><span data-stu-id="86f46-135">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




