---
description: Die Aufruf Methode ermöglicht den Zugriff auf Eigenschaften und Methoden, die vom-Objekt verfügbar gemacht werden.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: Cmediaposition. aufrufen-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366880"
---
# <a name="cmediapositioninvoke-method"></a><span data-ttu-id="dfbf5-103">Cmediaposition. aufrufen-Methode</span><span class="sxs-lookup"><span data-stu-id="dfbf5-103">CMediaPosition.Invoke method</span></span>

<span data-ttu-id="dfbf5-104">Die- `Invoke` Methode ermöglicht den Zugriff auf Eigenschaften und Methoden, die vom-Objekt verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-104">The `Invoke` method provides access to properties and methods exposed by the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfbf5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfbf5-105">Syntax</span></span>


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a><span data-ttu-id="dfbf5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfbf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfbf5-107">*dispidmember*</span><span class="sxs-lookup"><span data-stu-id="dfbf5-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbf5-108">Der Bezeichner des Members.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-108">Identifier of the member.</span></span> <span data-ttu-id="dfbf5-109">Verwenden Sie [**cmediaposition:: GetIDsOfNames**](cmediaposition-getidsofnames.md) , um den Dispatchbezeichner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-109">Use [**CMediaPosition::GetIDsOfNames**](cmediaposition-getidsofnames.md) to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dfbf5-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="dfbf5-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbf5-111">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-111">Reserved for future use.</span></span> <span data-ttu-id="dfbf5-112">Muss IID \_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="dfbf5-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="dfbf5-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbf5-114">Der Gebiets Schema Kontext, in dem Argumente interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="dfbf5-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="dfbf5-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbf5-116">Flags, die den Kontext des Aufrufs beschreiben.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-116">Flags describing the context of the call.</span></span>

</dd> <dt>

<span data-ttu-id="dfbf5-117">*pdispparameams*</span><span class="sxs-lookup"><span data-stu-id="dfbf5-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbf5-118">Zeiger auf eine **dipparams** -Struktur, die die Argumente enthält.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-118">Pointer to a **DIPPARAMS** structure that contains the arguments.</span></span>

</dd> <dt>

<span data-ttu-id="dfbf5-119">*pVarResult*</span><span class="sxs-lookup"><span data-stu-id="dfbf5-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbf5-120">Zeiger auf eine **Variante** , die das Ergebnis empfängt, oder **null** , wenn der Aufrufer kein Ergebnis erwartet.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-120">Pointer to a **VARIANT** that receives the result, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="dfbf5-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="dfbf5-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbf5-122">Ein Zeiger auf eine-Struktur, die Ausnahme Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-122">Pointer to a structure that receives exception information.</span></span>

</dd> <dt>

<span data-ttu-id="dfbf5-123">*gibt puArgErr*</span><span class="sxs-lookup"><span data-stu-id="dfbf5-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbf5-124">Ein Zeiger auf eine Variable, die den Index des ersten Arguments empfängt, das einen Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-124">Pointer to a variable that receives the index of the first argument that causes an error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfbf5-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfbf5-125">Return value</span></span>

<span data-ttu-id="dfbf5-126">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-126">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dfbf5-127">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-127">Possible values include the following.</span></span>



| <span data-ttu-id="dfbf5-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dfbf5-128">Return code</span></span>                                                                                              | <span data-ttu-id="dfbf5-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfbf5-129">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="dfbf5-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf5-130"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="dfbf5-131">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-131">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="dfbf5-132"><dt>**DISP \_ E \_ unknowninterface**</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf5-132"><dt>**DISP\_E\_UNKNOWNINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="dfbf5-133">Der *riid* -Parameter ist nicht IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="dfbf5-133">The *riid* parameter is not IID\_NULL</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dfbf5-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfbf5-134">Requirements</span></span>



| <span data-ttu-id="dfbf5-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfbf5-135">Requirement</span></span> | <span data-ttu-id="dfbf5-136">Wert</span><span class="sxs-lookup"><span data-stu-id="dfbf5-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfbf5-137">Header</span><span class="sxs-lookup"><span data-stu-id="dfbf5-137">Header</span></span><br/>  | <dl> <span data-ttu-id="dfbf5-138"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf5-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dfbf5-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dfbf5-139">Library</span></span><br/> | <dl> <span data-ttu-id="dfbf5-140">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf5-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfbf5-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfbf5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfbf5-142">**Cmediaposition-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dfbf5-142">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




