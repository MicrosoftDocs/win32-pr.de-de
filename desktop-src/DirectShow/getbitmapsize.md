---
description: Die getbitmapsize-Funktion berechnet die Anzahl der Bytes, die für eine geräteunabhängige Bitmap (DIB) erforderlich sind. Diese Funktion ruft einfach das dibsize-Makro auf.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: Getbitmapsize-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351334"
---
# <a name="getbitmapsize-function"></a><span data-ttu-id="9d3a3-104">Getbitmapsize-Funktion</span><span class="sxs-lookup"><span data-stu-id="9d3a3-104">GetBitmapSize function</span></span>

<span data-ttu-id="9d3a3-105">Die- `GetBitmapSize` Funktion berechnet die Anzahl der Bytes, die für eine geräteunabhängige Bitmap (DIB) erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9d3a3-105">The `GetBitmapSize` function calculates the number of bytes required by a device-independent bitmap (DIB).</span></span> <span data-ttu-id="9d3a3-106">Diese Funktion ruft einfach das [**dibsize**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) -Makro auf.</span><span class="sxs-lookup"><span data-stu-id="9d3a3-106">This function simply calls the [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) macro.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3a3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d3a3-107">Syntax</span></span>


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="9d3a3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d3a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d3a3-109">*pheader*</span><span class="sxs-lookup"><span data-stu-id="9d3a3-109">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3a3-110">Zeiger auf eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9d3a3-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d3a3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d3a3-111">Return value</span></span>

<span data-ttu-id="9d3a3-112">Gibt die Größe in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="9d3a3-112">Returns the size in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d3a3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d3a3-113">Requirements</span></span>



| <span data-ttu-id="9d3a3-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d3a3-114">Requirement</span></span> | <span data-ttu-id="9d3a3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9d3a3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d3a3-116">Header</span><span class="sxs-lookup"><span data-stu-id="9d3a3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9d3a3-117"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d3a3-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9d3a3-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d3a3-118">Library</span></span><br/> | <dl> <span data-ttu-id="9d3a3-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9d3a3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d3a3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d3a3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d3a3-121">Video-und Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="9d3a3-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




