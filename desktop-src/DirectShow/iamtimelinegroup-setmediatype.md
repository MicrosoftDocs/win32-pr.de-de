---
description: Die setmediatype-Methode legt den unkomprimierten Medientyp für die Gruppe fest.
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: 'Iamtimelinegroup:: setmediatype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a7c5366525b51367a5348bc47b9acbe0fb799db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359731"
---
# <a name="iamtimelinegroupsetmediatype-method"></a><span data-ttu-id="0a669-103">Iamtimelinegroup:: setmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="0a669-103">IAMTimelineGroup::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="0a669-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="0a669-104">\[Deprecated.</span></span> <span data-ttu-id="0a669-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="0a669-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0a669-106">Die- `SetMediaType` Methode legt den unkomprimierten Medientyp für die Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="0a669-106">The `SetMediaType` method sets the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a669-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a669-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="0a669-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a669-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a669-109">*PMT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a669-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a669-110">Ein Zeiger auf eine [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die das Format beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0a669-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure describing the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a669-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a669-111">Return value</span></span>

<span data-ttu-id="0a669-112">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="0a669-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="0a669-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0a669-113">Return code</span></span>                                                                                             | <span data-ttu-id="0a669-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a669-114">Description</span></span>                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="0a669-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a669-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="0a669-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0a669-116">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="0a669-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="0a669-117"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="0a669-118">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="0a669-118">**NULL** pointer argument.</span></span><br/>           |
| <dl> <span data-ttu-id="0a669-119"><dt>**VFW \_ E \_ invalidmediatype**</dt></span><span class="sxs-lookup"><span data-stu-id="0a669-119"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="0a669-120">Der angegebene Medientyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0a669-120">The specified media type is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0a669-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a669-121">Remarks</span></span>

<span data-ttu-id="0a669-122">Die folgenden Medientypen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="0a669-122">The following media types are supported:</span></span>

-   <span data-ttu-id="0a669-123">Unkomprimiertes RGB-Video</span><span class="sxs-lookup"><span data-stu-id="0a669-123">Uncompressed RGB video</span></span>
-   <span data-ttu-id="0a669-124">16 Bits pro Pixel, 555-Format (mediasubtype \_ RGB555)</span><span class="sxs-lookup"><span data-stu-id="0a669-124">16 bits per pixel, 555 format (MEDIASUBTYPE\_RGB555)</span></span>
-   <span data-ttu-id="0a669-125">24 Bits pro Pixel (mediasubtype \_ RGB24)</span><span class="sxs-lookup"><span data-stu-id="0a669-125">24 bits per pixel (MEDIASUBTYPE\_RGB24)</span></span>
-   <span data-ttu-id="0a669-126">32 Bits pro Pixel, mit Alpha (mediasubtype \_ ARGB32, nicht mediasubtype \_ RGB32)</span><span class="sxs-lookup"><span data-stu-id="0a669-126">32 bits per pixel, with alpha (MEDIASUBTYPE\_ARGB32, not MEDIASUBTYPE\_RGB32)</span></span>
-   <span data-ttu-id="0a669-127">16-Bit-Stereo PCM-Audiodatei (mediasubtype \_ PCM)</span><span class="sxs-lookup"><span data-stu-id="0a669-127">16-bit stereo PCM audio (MEDIASUBTYPE\_PCM)</span></span>

<span data-ttu-id="0a669-128">Video Typen müssen für den \_ Formattyp und den [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) für den Format-Block Video Info Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a669-128">Video types must use FORMAT\_VideoInfo for the format type and [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) for the format block.</span></span> <span data-ttu-id="0a669-129">Das [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a669-129">The [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format is not supported.</span></span> <span data-ttu-id="0a669-130">Außerdem werden Top-Down-Videoformate (*biheight* < 0) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a669-130">Also, top-down video formats (*biHeight* < 0) are not supported.</span></span>

<span data-ttu-id="0a669-131">Um ein Komprimierungs Format für die Gruppe anzugeben, rufen Sie die [**iamtimelinegroup::**](iamtimelinegroup-setsmartrecompressformat.md) "-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="0a669-131">To specify a compression format for the group, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="0a669-132">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="0a669-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0a669-133">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="0a669-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0a669-134">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0a669-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a669-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a669-135">Requirements</span></span>



| <span data-ttu-id="0a669-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a669-136">Requirement</span></span> | <span data-ttu-id="0a669-137">Wert</span><span class="sxs-lookup"><span data-stu-id="0a669-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a669-138">Header</span><span class="sxs-lookup"><span data-stu-id="0a669-138">Header</span></span><br/>  | <dl> <span data-ttu-id="0a669-139"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0a669-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0a669-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0a669-140">Library</span></span><br/> | <dl> <span data-ttu-id="0a669-141"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="0a669-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a669-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a669-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a669-143">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a669-143">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="0a669-144">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="0a669-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




