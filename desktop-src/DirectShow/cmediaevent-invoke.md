---
description: Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: Cmediaevent. aufrufen-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22482cffe11f62d50361bc950409858a2436d8a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358742"
---
# <a name="cmediaeventinvoke-method"></a><span data-ttu-id="92592-103">Cmediaevent. aufrufen-Methode</span><span class="sxs-lookup"><span data-stu-id="92592-103">CMediaEvent.Invoke method</span></span>

<span data-ttu-id="92592-104">Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.</span><span class="sxs-lookup"><span data-stu-id="92592-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="92592-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="92592-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="92592-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="92592-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92592-107">*dispidmember*</span><span class="sxs-lookup"><span data-stu-id="92592-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="92592-108">Der Bezeichner des Members.</span><span class="sxs-lookup"><span data-stu-id="92592-108">Identifier of the member.</span></span> <span data-ttu-id="92592-109">Verwenden Sie [**cmediaevent:: GetIDsOfNames**](cmediaevent-getidsofnames.md) oder die Dokumentation des Objekts, um den Dispatchbezeichner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="92592-109">Use [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="92592-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="92592-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="92592-111">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="92592-111">Reserved for future use.</span></span> <span data-ttu-id="92592-112">Muss IID \_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="92592-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="92592-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="92592-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="92592-114">Der Gebiets Schema Kontext, in dem Argumente interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="92592-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="92592-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="92592-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="92592-116">Flags, die den Kontext des `CMediaEvent::Invoke` Aufrufes beschreiben.</span><span class="sxs-lookup"><span data-stu-id="92592-116">Flags describing the context of the `CMediaEvent::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="92592-117">*pdispparameams*</span><span class="sxs-lookup"><span data-stu-id="92592-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="92592-118">Ein Zeiger auf eine-Struktur, die ein Array von Argumenten, ein Array von Argument dispatchids für benannte Argumente und Zähler für die Anzahl der Elemente in den Arrays enthält.</span><span class="sxs-lookup"><span data-stu-id="92592-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for the number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="92592-119">*pVarResult*</span><span class="sxs-lookup"><span data-stu-id="92592-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="92592-120">Ein Zeiger auf den Speicherort, an dem das Ergebnis gespeichert werden soll, oder **null** , wenn der Aufrufer kein Ergebnis erwartet.</span><span class="sxs-lookup"><span data-stu-id="92592-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="92592-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="92592-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="92592-122">Zeiger auf eine-Struktur, die Ausnahme Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="92592-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="92592-123">*gibt puArgErr*</span><span class="sxs-lookup"><span data-stu-id="92592-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="92592-124">Zeiger auf den Index des ersten Arguments innerhalb des **rgvarg** -Arrays der **DISPPARAMS** -Struktur, das einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="92592-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="92592-125">Weitere Informationen zu **disppara** Metern finden Sie unter Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="92592-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92592-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92592-126">Return value</span></span>

<span data-ttu-id="92592-127">Gibt DISP \_ E \_ unknowninterface zurück, wenn *riid* nicht IID \_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="92592-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="92592-128">Gibt einen der Fehlercodes aus [**cmediaevent:: GetTypeInfo**](cmediaevent-gettypeinfo.md) zurück, wenn der-Rückruf fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="92592-128">Returns one of the error codes from [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="92592-129">Andernfalls wird das **HRESULT** aus dem Aufruf von **IDispatch::** Aufruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="92592-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92592-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92592-130">Requirements</span></span>



| <span data-ttu-id="92592-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92592-131">Requirement</span></span> | <span data-ttu-id="92592-132">Wert</span><span class="sxs-lookup"><span data-stu-id="92592-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92592-133">Header</span><span class="sxs-lookup"><span data-stu-id="92592-133">Header</span></span><br/>  | <dl> <span data-ttu-id="92592-134"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92592-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="92592-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="92592-135">Library</span></span><br/> | <dl> <span data-ttu-id="92592-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="92592-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92592-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92592-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92592-138">**Cmediaevent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="92592-138">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




