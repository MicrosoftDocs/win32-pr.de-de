---
description: Mit der CopyPalette-Methode wird die Palette aus einer beliebigen videoinfo-Struktur in eine beliebige, von einer beliebigen Struktur über videoinfo-Struktur
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Cimagepalette. CopyPalette-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371512"
---
# <a name="cimagepalettecopypalette-method"></a><span data-ttu-id="be036-103">Cimagepalette. CopyPalette-Methode</span><span class="sxs-lookup"><span data-stu-id="be036-103">CImagePalette.CopyPalette method</span></span>

<span data-ttu-id="be036-104">Die- `CopyPalette` Methode kopiert die Palette aus einer beliebigen [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur in eine beliebige paletsierte **videoinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="be036-104">The `CopyPalette` method copies the palette from any [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure to any palettized **VIDEOINFO** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="be036-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be036-105">Syntax</span></span>


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a><span data-ttu-id="be036-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be036-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be036-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="be036-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="be036-108">Zeiger auf den Quell Medientyp.</span><span class="sxs-lookup"><span data-stu-id="be036-108">Pointer to the source media type.</span></span>

</dd> <dt>

<span data-ttu-id="be036-109">*pDest*</span><span class="sxs-lookup"><span data-stu-id="be036-109">*pDest*</span></span> 
</dt> <dd>

<span data-ttu-id="be036-110">Zeiger auf den Zielmedientyp.</span><span class="sxs-lookup"><span data-stu-id="be036-110">Pointer to the destination media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be036-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be036-111">Return value</span></span>

<span data-ttu-id="be036-112">Gibt "S OK" zurück, \_ Wenn die Palette kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="be036-112">Returns S\_OK if the palette was copied.</span></span> <span data-ttu-id="be036-113">Gibt "false" zurück, \_ Wenn entweder der Quell-oder Ziel Medientyp keine Palette hat.</span><span class="sxs-lookup"><span data-stu-id="be036-113">Returns S\_FALSE if either the source or destination media type does not have a palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="be036-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be036-114">Remarks</span></span>

<span data-ttu-id="be036-115">Der *pdest* -Medientyp muss ein paletsiertes Format mit einer Farbtiefe von 8 Bits oder weniger sein.</span><span class="sxs-lookup"><span data-stu-id="be036-115">The *pDest* media type must be a palettized format with a color depth of 8 bits or less.</span></span> <span data-ttu-id="be036-116">Der *psrc* -Medientyp kann ein beliebiger [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Typ mit einer Palette sein, einschließlich YUV-und True-Color-Formaten mit paletteneinträgen.</span><span class="sxs-lookup"><span data-stu-id="be036-116">The *pSrc* media type can be any [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) type with a palette, including YUV and true-color formats with palette entries.</span></span> <span data-ttu-id="be036-117">Die-Methode kopiert die Paletteneinträge aus *psrc* in eine neue Palette und fügt die neue Palette an den *pdest* an.</span><span class="sxs-lookup"><span data-stu-id="be036-117">The method copies the palette entries from *pSrc* into a new palette, and attaches the new palette to *pDest*.</span></span>

## <a name="requirements"></a><span data-ttu-id="be036-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be036-118">Requirements</span></span>



| <span data-ttu-id="be036-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be036-119">Requirement</span></span> | <span data-ttu-id="be036-120">Wert</span><span class="sxs-lookup"><span data-stu-id="be036-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be036-121">Header</span><span class="sxs-lookup"><span data-stu-id="be036-121">Header</span></span><br/>  | <dl> <span data-ttu-id="be036-122"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be036-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be036-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="be036-123">Library</span></span><br/> | <dl> <span data-ttu-id="be036-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="be036-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be036-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be036-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be036-126">**Cimagepalette-Klasse**</span><span class="sxs-lookup"><span data-stu-id="be036-126">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




