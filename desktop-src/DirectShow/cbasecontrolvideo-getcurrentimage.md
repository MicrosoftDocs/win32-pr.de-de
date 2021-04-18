---
description: Die getaccesstimage-Methode ruft eine Kopie des aktuellen Bilds beim Renderer ab.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Cbasecontrolvideo. getaccesstimage-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d44e6930d0d7e179162939c13a54f2953c5ab965
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365434"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a><span data-ttu-id="543b1-103">Cbasecontrolvideo. gethapptimage-Methode</span><span class="sxs-lookup"><span data-stu-id="543b1-103">CBaseControlVideo.GetCurrentImage method</span></span>

<span data-ttu-id="543b1-104">Die- `GetCurrentImage` Methode ruft eine Kopie des aktuellen Bilds beim Renderer ab.</span><span class="sxs-lookup"><span data-stu-id="543b1-104">The `GetCurrentImage` method retrieves a copy of the current image at the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="543b1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="543b1-105">Syntax</span></span>


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a><span data-ttu-id="543b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="543b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="543b1-107">*pbuffersize*</span><span class="sxs-lookup"><span data-stu-id="543b1-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="543b1-108">Ein Zeiger auf die Größe des Ausgabepuffers.</span><span class="sxs-lookup"><span data-stu-id="543b1-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="543b1-109">*pvideoimage*</span><span class="sxs-lookup"><span data-stu-id="543b1-109">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="543b1-110">Zeiger auf den Ausgabepuffer für das Bild.</span><span class="sxs-lookup"><span data-stu-id="543b1-110">Pointer to the output buffer for the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="543b1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="543b1-111">Return value</span></span>

<span data-ttu-id="543b1-112">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="543b1-112">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="543b1-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="543b1-113">Return code</span></span>                                                                                        | <span data-ttu-id="543b1-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="543b1-114">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="543b1-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="543b1-115"><dt>**E\_FAIL**</dt></span></span> </dl>             | <span data-ttu-id="543b1-116">Fehler.</span><span class="sxs-lookup"><span data-stu-id="543b1-116">Failure.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="543b1-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="543b1-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>       | <span data-ttu-id="543b1-118">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="543b1-118">Invalid argument.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="543b1-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="543b1-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>      | <span data-ttu-id="543b1-120">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="543b1-120">Out of memory.</span></span> <span data-ttu-id="543b1-121">Wird zurückgegeben, wenn der *pvideoinfo* -Parameter **null** ist.</span><span class="sxs-lookup"><span data-stu-id="543b1-121">Returned when the *pVideoInfo* parameter is **NULL**.</span></span><br/>   |
| <dl> <span data-ttu-id="543b1-122"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="543b1-122"><dt>**NOERROR**</dt></span></span> </dl>             | <span data-ttu-id="543b1-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="543b1-123">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="543b1-124"><dt>**VFW \_ E \_ nicht \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="543b1-124"><dt>**VFW\_E\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="543b1-125">Der Vorgang konnte nicht ausgeführt werden, da der Filter nicht angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="543b1-125">The operation could not be performed because the filter is not paused.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="543b1-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="543b1-126">Remarks</span></span>

<span data-ttu-id="543b1-127">Diese Member-Funktion Ruft das Bild aus dem Beispiel ab und kopiert es in den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="543b1-127">This member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="543b1-128">Der Abschnitt des Videos, das in den Ausgabepuffer kopiert wurde, reflektiert das Quell Rechteck, das über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle festgelegt</span><span class="sxs-lookup"><span data-stu-id="543b1-128">The section of video copied into the output buffer reflects the source rectangle set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="543b1-129">Das Ziel Rechteck wird nicht wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="543b1-129">It does not reflect the destination rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="543b1-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="543b1-130">Requirements</span></span>



| <span data-ttu-id="543b1-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="543b1-131">Requirement</span></span> | <span data-ttu-id="543b1-132">Wert</span><span class="sxs-lookup"><span data-stu-id="543b1-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="543b1-133">Header</span><span class="sxs-lookup"><span data-stu-id="543b1-133">Header</span></span><br/>  | <dl> <span data-ttu-id="543b1-134"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="543b1-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="543b1-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="543b1-135">Library</span></span><br/> | <dl> <span data-ttu-id="543b1-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="543b1-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="543b1-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="543b1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="543b1-138">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="543b1-138">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




