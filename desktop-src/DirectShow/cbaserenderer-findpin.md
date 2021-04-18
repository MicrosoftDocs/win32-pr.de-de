---
description: Die findpin-Methode ruft die PIN mit dem angegebenen Bezeichner ab.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Cbaserderderer. findpin-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364761"
---
# <a name="cbaserendererfindpin-method"></a><span data-ttu-id="a11fc-103">Cbaserderderer. findpin-Methode</span><span class="sxs-lookup"><span data-stu-id="a11fc-103">CBaseRenderer.FindPin method</span></span>

<span data-ttu-id="a11fc-104">Die- `FindPin` Methode ruft die PIN mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="a11fc-104">The `FindPin` method retrieves the pin with the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="a11fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a11fc-105">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="a11fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a11fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a11fc-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="a11fc-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="a11fc-108">Ein Zeiger auf eine Konstante, mit NULL endender breit Zeichen Zeichenfolge, die die PIN identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a11fc-108">Pointer to a constant, null-terminated wide-character string that identifies the pin.</span></span> <span data-ttu-id="a11fc-109">Muss L "in" lauten.</span><span class="sxs-lookup"><span data-stu-id="a11fc-109">Must be L"In".</span></span>

</dd> <dt>

<span data-ttu-id="a11fc-110">*pppin*</span><span class="sxs-lookup"><span data-stu-id="a11fc-110">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a11fc-111">Adresse einer Variablen, die einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN empfängt.</span><span class="sxs-lookup"><span data-stu-id="a11fc-111">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="a11fc-112">Wenn die Methode fehlschlägt, wird *\* pppin* auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a11fc-112">If the method fails, *\*ppPin* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a11fc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a11fc-113">Return value</span></span>

<span data-ttu-id="a11fc-114">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a11fc-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a11fc-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a11fc-115">Return code</span></span>                                                                                       | <span data-ttu-id="a11fc-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a11fc-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a11fc-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a11fc-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="a11fc-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a11fc-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="a11fc-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a11fc-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="a11fc-120">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="a11fc-120">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="a11fc-121"><dt>**VFW \_ E \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="a11fc-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="a11fc-122">Nicht gefunden:</span><span class="sxs-lookup"><span data-stu-id="a11fc-122">Not found.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="a11fc-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a11fc-123">Remarks</span></span>

<span data-ttu-id="a11fc-124">Diese Methode überschreibt die [**cbasefilter:: findpin**](cbasefilter-findpin.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a11fc-124">This method overrides the [**CBaseFilter::FindPin**](cbasefilter-findpin.md) method.</span></span> <span data-ttu-id="a11fc-125">Die einzige PIN des Filters (die Eingabe-PIN) heißt "in".</span><span class="sxs-lookup"><span data-stu-id="a11fc-125">The filter's only pin (the input pin) is named "In".</span></span>

## <a name="requirements"></a><span data-ttu-id="a11fc-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a11fc-126">Requirements</span></span>



| <span data-ttu-id="a11fc-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a11fc-127">Requirement</span></span> | <span data-ttu-id="a11fc-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a11fc-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a11fc-129">Header</span><span class="sxs-lookup"><span data-stu-id="a11fc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a11fc-130"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a11fc-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a11fc-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a11fc-131">Library</span></span><br/> | <dl> <span data-ttu-id="a11fc-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a11fc-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a11fc-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a11fc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a11fc-134">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a11fc-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




