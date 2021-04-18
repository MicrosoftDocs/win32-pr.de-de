---
description: Die getimagesize-Methode ruft Informationen zur Video Bild Größe ab.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Cbasecontrolvideo. getimagesize-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364502"
---
# <a name="cbasecontrolvideogetimagesize-method"></a><span data-ttu-id="a712e-103">Cbasecontrolvideo. getimagesize-Methode</span><span class="sxs-lookup"><span data-stu-id="a712e-103">CBaseControlVideo.GetImageSize method</span></span>

<span data-ttu-id="a712e-104">Die- `GetImageSize` Methode ruft Informationen zur Video Bild Größe ab.</span><span class="sxs-lookup"><span data-stu-id="a712e-104">The `GetImageSize` method retrieves video image size information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a712e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a712e-105">Syntax</span></span>


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="a712e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a712e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a712e-107">*pvideoinfo*</span><span class="sxs-lookup"><span data-stu-id="a712e-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="a712e-108">Zeiger auf eine [**videinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur, die ausgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a712e-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to be filled in.</span></span>

</dd> <dt>

<span data-ttu-id="a712e-109">*pbuffersize*</span><span class="sxs-lookup"><span data-stu-id="a712e-109">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a712e-110">Ein Zeiger auf die Größe des Video Puffers.</span><span class="sxs-lookup"><span data-stu-id="a712e-110">Pointer to the size of the video buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a712e-111">*psourcerect*</span><span class="sxs-lookup"><span data-stu-id="a712e-111">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="a712e-112">Zeiger auf die Rechteck Abmessungen des Quellvideos.</span><span class="sxs-lookup"><span data-stu-id="a712e-112">Pointer to the rectangle dimensions of the source video.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a712e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a712e-113">Return value</span></span>

<span data-ttu-id="a712e-114">Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a712e-114">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="a712e-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a712e-115">Return code</span></span>                                                                                  | <span data-ttu-id="a712e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a712e-116">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a712e-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="a712e-117"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="a712e-118">Fehler.</span><span class="sxs-lookup"><span data-stu-id="a712e-118">Failure.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="a712e-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="a712e-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a712e-120">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="a712e-120">Invalid argument.</span></span> <span data-ttu-id="a712e-121">Das Datenformat ist nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a712e-121">The data format is not compatible.</span></span><br/>           |
| <dl> <span data-ttu-id="a712e-122"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="a712e-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="a712e-123">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a712e-123">Unexpected error occurred.</span></span> <span data-ttu-id="a712e-124">Mindestens ein Argument ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a712e-124">One or more arguments are **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="a712e-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="a712e-125"><dt>**NOERROR**</dt></span></span> </dl>       | <span data-ttu-id="a712e-126">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a712e-126">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="a712e-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a712e-127">Remarks</span></span>

<span data-ttu-id="a712e-128">Diese Member-Funktion ist eine Hilfsfunktion zum Erstellen von Image-Renderings von DIB-Images im Speicher.</span><span class="sxs-lookup"><span data-stu-id="a712e-128">This member function is a helper function used for creating memory image renderings of DIB images.</span></span> <span data-ttu-id="a712e-129">Sie wird von der Basisklassen Implementierung von [**cbasecontrolvideo:: Get-/timage**](cbasecontrolvideo-getcurrentimage.md) aufgerufen, wenn ein **null**-_pvideoimage_ -Parameter an diese Member-Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a712e-129">It is called from the base class implementation of [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) when a **NULL**_pVideoImage_ parameter is passed to that member function.</span></span> <span data-ttu-id="a712e-130">Folglich erstellt diese Member-Funktion eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur und gibt Sie zurück, wobei die Informationen in *pbuffersize* und *psourcerect* verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a712e-130">As a result, this member function constructs and returns a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, using the information in *pBufferSize* and *pSourceRect*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a712e-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a712e-131">Requirements</span></span>



| <span data-ttu-id="a712e-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a712e-132">Requirement</span></span> | <span data-ttu-id="a712e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a712e-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a712e-134">Header</span><span class="sxs-lookup"><span data-stu-id="a712e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="a712e-135"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a712e-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a712e-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a712e-136">Library</span></span><br/> | <dl> <span data-ttu-id="a712e-137">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a712e-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a712e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a712e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a712e-139">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a712e-139">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




