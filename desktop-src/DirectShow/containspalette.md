---
description: Die containspalette-Funktion bestimmt, ob eine angegebene videoinfoheader-Struktur eine Palette enthält.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: Containspalette-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9417d9dd39f958e4a4caf68ef368d231a2097de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371405"
---
# <a name="containspalette-function"></a><span data-ttu-id="cbc4c-103">Containspalette-Funktion</span><span class="sxs-lookup"><span data-stu-id="cbc4c-103">ContainsPalette function</span></span>

<span data-ttu-id="cbc4c-104">Die **containspalette** -Funktion bestimmt, ob eine angegebene [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur eine Palette enthält.</span><span class="sxs-lookup"><span data-stu-id="cbc4c-104">The **ContainsPalette** function determines whether a specified [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure contains a palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc4c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbc4c-105">Syntax</span></span>


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a><span data-ttu-id="cbc4c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbc4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc4c-107">*pvideoinfo*</span><span class="sxs-lookup"><span data-stu-id="cbc4c-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc4c-108">Zeiger auf eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cbc4c-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc4c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cbc4c-109">Return value</span></span>

<span data-ttu-id="cbc4c-110">Gibt **true** zurück, wenn die Bittiefe 8 oder kleiner (**bmiheader. biBitCount**) ist, oder wenn die Anzahl der Farbindizes größer als 0 (**bmiheader. biclrused**) ist.</span><span class="sxs-lookup"><span data-stu-id="cbc4c-110">Returns **TRUE** if the bitdepth is 8 or less (**bmiHeader.biBitCount**), or the number of color indexes is more than zero (**bmiHeader.biClrUsed**).</span></span> <span data-ttu-id="cbc4c-111">Gibt andernfalls **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="cbc4c-111">Returns **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc4c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbc4c-112">Requirements</span></span>



| <span data-ttu-id="cbc4c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbc4c-113">Requirement</span></span> | <span data-ttu-id="cbc4c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cbc4c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc4c-115">Header</span><span class="sxs-lookup"><span data-stu-id="cbc4c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="cbc4c-116"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbc4c-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cbc4c-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cbc4c-117">Library</span></span><br/> | <dl> <span data-ttu-id="cbc4c-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="cbc4c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbc4c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbc4c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc4c-120">Video-und Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="cbc4c-120">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




