---
description: 'Die QueryId-Methode ruft den PIN-Bezeichner ab. Diese Methode überschreibt die cbasepin:: QueryId-Methode.'
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: Crendererinputpin. QueryId-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b56ae2a846b4d89da4c6a9d4c8f88bd3094c5cff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362143"
---
# <a name="crendererinputpinqueryid-method"></a><span data-ttu-id="bde94-104">Crendererinputpin. QueryId-Methode</span><span class="sxs-lookup"><span data-stu-id="bde94-104">CRendererInputPin.QueryId method</span></span>

<span data-ttu-id="bde94-105">Die- `QueryId` Methode ruft den PIN-Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="bde94-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="bde94-106">Diese Methode überschreibt die [**cbasepin:: QueryId**](cbasepin-queryid.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bde94-106">This method overrides the [**CBasePin::QueryId**](cbasepin-queryid.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bde94-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bde94-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="bde94-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bde94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bde94-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="bde94-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="bde94-110">Empfängt eine Zeichenfolge mit dem PIN-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="bde94-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bde94-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bde94-111">Return value</span></span>

<span data-ttu-id="bde94-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bde94-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="bde94-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bde94-113">Return code</span></span>                                                                                   | <span data-ttu-id="bde94-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bde94-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="bde94-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bde94-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bde94-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="bde94-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="bde94-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="bde94-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bde94-118">Nicht genügend Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="bde94-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="bde94-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="bde94-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bde94-120">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="bde94-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bde94-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bde94-121">Remarks</span></span>

<span data-ttu-id="bde94-122">Diese Methode ordnet die breit Zeichen-Zeichenfolge "in" zu und weist Sie dem *ID* -Parameter zu.</span><span class="sxs-lookup"><span data-stu-id="bde94-122">This method allocates the wide-character string "In" and assigns it to the *Id* parameter.</span></span> <span data-ttu-id="bde94-123">Der Aufrufer muss den zugewiesenen Speicher mithilfe der **CoTaskMemFree** -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="bde94-123">The caller must free the allocated memory, using the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bde94-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bde94-124">Requirements</span></span>



| <span data-ttu-id="bde94-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bde94-125">Requirement</span></span> | <span data-ttu-id="bde94-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bde94-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bde94-127">Header</span><span class="sxs-lookup"><span data-stu-id="bde94-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bde94-128"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bde94-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bde94-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bde94-129">Library</span></span><br/> | <dl> <span data-ttu-id="bde94-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bde94-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bde94-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bde94-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde94-132">**Crendererinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bde94-132">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




