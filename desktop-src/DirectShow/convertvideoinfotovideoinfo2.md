---
description: Die ConvertVideoInfoToVideoInfo2-Funktion konvertiert einen Medientyp, der videoinfoheader verwendet, zu einem, der VIDEOINFOHEADER2 verwendet.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: ConvertVideoInfoToVideoInfo2-Funktion (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54611c83c30ad65a806a077dc51c933a9f881636
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106363206"
---
# <a name="convertvideoinfotovideoinfo2-function"></a><span data-ttu-id="4a02a-103">ConvertVideoInfoToVideoInfo2-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a02a-103">ConvertVideoInfoToVideoInfo2 function</span></span>

<span data-ttu-id="4a02a-104">Die- `ConvertVideoInfoToVideoInfo2` Funktion konvertiert einen Medientyp, der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) verwendet, in einen, der [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a02a-104">The `ConvertVideoInfoToVideoInfo2` function converts a media type that uses [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) to one that uses [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a02a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a02a-105">Syntax</span></span>


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="4a02a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a02a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a02a-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="4a02a-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="4a02a-108">Zeiger auf die zu konvertierende zu- [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a02a-108">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to convert.</span></span> <span data-ttu-id="4a02a-109">Die-Struktur muss über eine Format-Format- \_ Video Info verfügen.</span><span class="sxs-lookup"><span data-stu-id="4a02a-109">The structure must have format type FORMAT\_VideoInfo.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a02a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a02a-110">Return value</span></span>

<span data-ttu-id="4a02a-111">Gibt " \_ OK" oder "E \_ outo" zurück.</span><span class="sxs-lookup"><span data-stu-id="4a02a-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a02a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a02a-112">Remarks</span></span>

<span data-ttu-id="4a02a-113">Diese Funktion ordnet eine neue **VIDEOINFOHEADER2** -Struktur zu, kopiert die Member der **videoinfoheader** -Struktur in Sie und ersetzt die alte-Struktur durch die neue-Struktur im Format Block des Medientyps.</span><span class="sxs-lookup"><span data-stu-id="4a02a-113">This function allocates a new **VIDEOINFOHEADER2** structure, copies the members of the **VIDEOINFOHEADER** structure into it, and replaces the old structure with the new structure in the format block of the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a02a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a02a-114">Requirements</span></span>



| <span data-ttu-id="4a02a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a02a-115">Requirement</span></span> | <span data-ttu-id="4a02a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4a02a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a02a-117">Header</span><span class="sxs-lookup"><span data-stu-id="4a02a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4a02a-118"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a02a-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a02a-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4a02a-119">Library</span></span><br/> | <dl> <span data-ttu-id="4a02a-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4a02a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a02a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a02a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a02a-122">Video-und Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="4a02a-122">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




