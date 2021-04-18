---
description: Die makepalette-Methode erstellt eine logische Palette aus der Farbtabelle in einem Videoformat.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Cimagepalette. makepalette-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364584"
---
# <a name="cimagepalettemakepalette-method"></a><span data-ttu-id="44f60-103">Cimagepalette. makepalette-Methode</span><span class="sxs-lookup"><span data-stu-id="44f60-103">CImagePalette.MakePalette method</span></span>

<span data-ttu-id="44f60-104">Mit der- `MakePalette` Methode wird eine logische Palette aus der Farbtabelle in einem Videoformat erstellt.</span><span class="sxs-lookup"><span data-stu-id="44f60-104">The `MakePalette` method creates a logical palette from the color table in a video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="44f60-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="44f60-105">Syntax</span></span>


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="44f60-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44f60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44f60-107">*pvideoinfo*</span><span class="sxs-lookup"><span data-stu-id="44f60-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="44f60-108">Zeiger auf eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur, die die Farbtabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="44f60-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the color table.</span></span>

</dd> <dt>

<span data-ttu-id="44f60-109">*szdevice*</span><span class="sxs-lookup"><span data-stu-id="44f60-109">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="44f60-110">Zeiger auf eine Zeichenfolge, die den Namen des Anzeige Geräts enthält, wie von der GDI-Funktion " **EnumDisplayDevices** " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44f60-110">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="44f60-111">Legen Sie diesen Parameter auf **null** fest, um das Haupt Anzeigegerät zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="44f60-111">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44f60-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44f60-112">Return value</span></span>

<span data-ttu-id="44f60-113">Wenn erfolgreich, wird ein Handle für die Palette zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44f60-113">If successful, returns a handle to the palette.</span></span> <span data-ttu-id="44f60-114">Andernfalls wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44f60-114">Otherwise, returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="44f60-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44f60-115">Requirements</span></span>



| <span data-ttu-id="44f60-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44f60-116">Requirement</span></span> | <span data-ttu-id="44f60-117">Wert</span><span class="sxs-lookup"><span data-stu-id="44f60-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44f60-118">Header</span><span class="sxs-lookup"><span data-stu-id="44f60-118">Header</span></span><br/>  | <dl> <span data-ttu-id="44f60-119"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44f60-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="44f60-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="44f60-120">Library</span></span><br/> | <dl> <span data-ttu-id="44f60-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="44f60-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44f60-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44f60-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f60-123">**Cimagepalette-Klasse**</span><span class="sxs-lookup"><span data-stu-id="44f60-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




