---
description: Die GetBitmapPalette-Funktion gibt den ersten Paletteneintrag in einer videoinfoheader-Struktur zurück.
ms.assetid: 7c620f81-31d9-408f-954d-aeff39f93956
title: GetBitmapPalette-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa4139c7aaece3e92a26fbf69fc02b8759f1613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354179"
---
# <a name="getbitmappalette-function"></a><span data-ttu-id="1c934-103">GetBitmapPalette-Funktion</span><span class="sxs-lookup"><span data-stu-id="1c934-103">GetBitmapPalette function</span></span>

<span data-ttu-id="1c934-104">Die- `GetBitmapPalette` Funktion gibt den ersten Paletteneintrag in einer [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="1c934-104">The `GetBitmapPalette` function returns the first palette entry in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c934-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c934-105">Syntax</span></span>


```C++
const RGBQUAD* GetBitmapPalette(
   const VIDEOINFOHEADER *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1c934-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c934-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c934-107">*pvideoinfo*</span><span class="sxs-lookup"><span data-stu-id="1c934-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="1c934-108">Zeiger auf eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1c934-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c934-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c934-109">Return value</span></span>

<span data-ttu-id="1c934-110">Gibt einen Zeiger auf den ersten Paletteneintrag zurück.</span><span class="sxs-lookup"><span data-stu-id="1c934-110">Returns a pointer to the first palette entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c934-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c934-111">Requirements</span></span>



| <span data-ttu-id="1c934-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c934-112">Requirement</span></span> | <span data-ttu-id="1c934-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1c934-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c934-114">Header</span><span class="sxs-lookup"><span data-stu-id="1c934-114">Header</span></span><br/>  | <dl> <span data-ttu-id="1c934-115"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c934-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1c934-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1c934-116">Library</span></span><br/> | <dl> <span data-ttu-id="1c934-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1c934-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




