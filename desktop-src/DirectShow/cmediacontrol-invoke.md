---
description: Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: Cmediacontrol. aufrufen-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b9a29d163180ffc609ca44f2bbbfb2870c5faef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372083"
---
# <a name="cmediacontrolinvoke-method"></a><span data-ttu-id="b40e0-103">Cmediacontrol. aufrufen-Methode</span><span class="sxs-lookup"><span data-stu-id="b40e0-103">CMediaControl.Invoke method</span></span>

<span data-ttu-id="b40e0-104">Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.</span><span class="sxs-lookup"><span data-stu-id="b40e0-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b40e0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b40e0-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b40e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b40e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b40e0-107">*dispidmember*</span><span class="sxs-lookup"><span data-stu-id="b40e0-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="b40e0-108">Der Bezeichner des Members.</span><span class="sxs-lookup"><span data-stu-id="b40e0-108">Identifier of the member.</span></span> <span data-ttu-id="b40e0-109">Verwenden Sie [**cmediacontrol:: GetIDsOfNames**](cmediacontrol-getidsofnames.md) oder die Dokumentation des Objekts, um den Dispatchbezeichner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b40e0-109">Use [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b40e0-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="b40e0-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="b40e0-111">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b40e0-111">Reserved for future use.</span></span> <span data-ttu-id="b40e0-112">Muss IID \_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b40e0-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="b40e0-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="b40e0-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="b40e0-114">Der Gebiets Schema Kontext, in dem Argumente interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b40e0-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="b40e0-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="b40e0-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b40e0-116">Flags, die den Kontext des `CMediaControl::Invoke` Aufrufes beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b40e0-116">Flags describing the context of the `CMediaControl::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="b40e0-117">*pdispparameams*</span><span class="sxs-lookup"><span data-stu-id="b40e0-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="b40e0-118">Ein Zeiger auf eine-Struktur, die ein Array von Argumenten, ein Array von Argument dispatchids für benannte Argumente und Zähler für die Anzahl der Elemente in den Arrays enthält.</span><span class="sxs-lookup"><span data-stu-id="b40e0-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="b40e0-119">*pVarResult*</span><span class="sxs-lookup"><span data-stu-id="b40e0-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="b40e0-120">Ein Zeiger auf den Speicherort, an dem das Ergebnis gespeichert werden soll, oder **null** , wenn der Aufrufer kein Ergebnis erwartet.</span><span class="sxs-lookup"><span data-stu-id="b40e0-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="b40e0-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="b40e0-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b40e0-122">Zeiger auf eine-Struktur, die Ausnahme Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="b40e0-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="b40e0-123">*gibt puArgErr*</span><span class="sxs-lookup"><span data-stu-id="b40e0-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="b40e0-124">Zeiger auf den Index des ersten Arguments innerhalb des **rgvarg** -Arrays der **DISPPARAMS** -Struktur, das einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="b40e0-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="b40e0-125">Weitere Informationen zu **disppara** Metern finden Sie unter Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="b40e0-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b40e0-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b40e0-126">Return value</span></span>

<span data-ttu-id="b40e0-127">Gibt DISP \_ E \_ unknowninterface zurück, wenn *riid* nicht IID \_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="b40e0-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="b40e0-128">Gibt einen der Fehlercodes aus [**cmediacontrol:: GetTypeInfo**](cmediacontrol-gettypeinfo.md) zurück, wenn der-Rückruf fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="b40e0-128">Returns one of the error codes from [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="b40e0-129">Andernfalls wird das **HRESULT** aus dem Aufruf von **IDispatch::** Aufruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b40e0-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b40e0-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b40e0-130">Requirements</span></span>



| <span data-ttu-id="b40e0-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b40e0-131">Requirement</span></span> | <span data-ttu-id="b40e0-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b40e0-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b40e0-133">Header</span><span class="sxs-lookup"><span data-stu-id="b40e0-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b40e0-134"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b40e0-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b40e0-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b40e0-135">Library</span></span><br/> | <dl> <span data-ttu-id="b40e0-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b40e0-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b40e0-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b40e0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b40e0-138">**Cmediacontrol-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b40e0-138">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




