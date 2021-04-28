---
description: 'CMediaEvent.Invoke-Methode: Ermöglicht den Zugriff auf Eigenschaften und Methoden, die von einem -Objekt verfügbar gemacht werden.'
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: CMediaEvent.Invoke-Methode (Ctlutil.h)
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
ms.openlocfilehash: ea812d0c7629b98d90f3f7e535d229c707452b23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095538"
---
# <a name="cmediaeventinvoke-method"></a><span data-ttu-id="4fa55-103">CMediaEvent.Invoke-Methode</span><span class="sxs-lookup"><span data-stu-id="4fa55-103">CMediaEvent.Invoke method</span></span>

<span data-ttu-id="4fa55-104">Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.</span><span class="sxs-lookup"><span data-stu-id="4fa55-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fa55-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4fa55-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fa55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fa55-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="4fa55-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa55-108">Bezeichner des Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="4fa55-108">Identifier of the member.</span></span> <span data-ttu-id="4fa55-109">Verwenden [**Sie CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) oder die Dokumentation des Objekts, um den Dispatchbezeichner zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fa55-109">Use [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4fa55-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="4fa55-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa55-111">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4fa55-111">Reserved for future use.</span></span> <span data-ttu-id="4fa55-112">Muss IID NULL \_ sein.</span><span class="sxs-lookup"><span data-stu-id="4fa55-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="4fa55-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="4fa55-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa55-114">Der Locale-Kontext, in dem Argumente interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fa55-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="4fa55-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="4fa55-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa55-116">Flags, die den Kontext des Aufrufs `CMediaEvent::Invoke` beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4fa55-116">Flags describing the context of the `CMediaEvent::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="4fa55-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="4fa55-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa55-118">Zeiger auf eine -Struktur, die ein Array von Argumenten, ein Array von Argument-Dispatch-IDs für benannte Argumente und die Anzahl der Elemente in den Arrays enthält.</span><span class="sxs-lookup"><span data-stu-id="4fa55-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for the number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="4fa55-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="4fa55-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa55-120">Zeiger auf den Ort, an dem das Ergebnis gespeichert werden soll, oder **NULL,** wenn der Aufrufer kein Ergebnis erwartet.</span><span class="sxs-lookup"><span data-stu-id="4fa55-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="4fa55-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="4fa55-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa55-122">Zeiger auf eine -Struktur, die Ausnahmeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="4fa55-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="4fa55-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="4fa55-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa55-124">Zeiger auf den Index des ersten Arguments innerhalb des **rgvarg-Arrays** der **DISPPARAMS-Struktur** mit einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="4fa55-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="4fa55-125">Weitere Informationen zu **DISPPARAMS finden** Sie im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="4fa55-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fa55-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fa55-126">Return value</span></span>

<span data-ttu-id="4fa55-127">Gibt DISP \_ E \_ UNKNOWNINTERFACE zurück, *wenn riid* nicht IID \_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="4fa55-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="4fa55-128">Gibt einen der Fehlercodes von [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) zurück, wenn der Aufruf fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="4fa55-128">Returns one of the error codes from [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="4fa55-129">Andernfalls gibt das **HRESULT** aus dem Aufruf von **IDispatch::Invoke** zurück.</span><span class="sxs-lookup"><span data-stu-id="4fa55-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa55-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fa55-130">Requirements</span></span>



| <span data-ttu-id="4fa55-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fa55-131">Requirement</span></span> | <span data-ttu-id="4fa55-132">Wert</span><span class="sxs-lookup"><span data-stu-id="4fa55-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa55-133">Header</span><span class="sxs-lookup"><span data-stu-id="4fa55-133">Header</span></span><br/>  | <dl> <span data-ttu-id="4fa55-134"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa55-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4fa55-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4fa55-135">Library</span></span><br/> | <dl> <span data-ttu-id="4fa55-136"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa55-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fa55-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4fa55-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa55-138">**CMediaEvent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4fa55-138">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




