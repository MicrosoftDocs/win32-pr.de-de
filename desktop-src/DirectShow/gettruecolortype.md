---
description: Die gettruecolortype-Funktion Ruft den lesbaren Namen eines Video Untertyps ab.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: Gettruecolortype-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c262031045eed3755fe2d19d3bd703a347e6117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364974"
---
# <a name="gettruecolortype-function"></a><span data-ttu-id="52a7a-103">Gettruecolortype-Funktion</span><span class="sxs-lookup"><span data-stu-id="52a7a-103">GetTrueColorType function</span></span>

<span data-ttu-id="52a7a-104">Die **gettruecolortype** -Funktion Ruft den lesbaren Namen eines Video Untertyps ab.</span><span class="sxs-lookup"><span data-stu-id="52a7a-104">The **GetTrueColorType** function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a7a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52a7a-105">Syntax</span></span>


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="52a7a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52a7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52a7a-107">*pheader*</span><span class="sxs-lookup"><span data-stu-id="52a7a-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="52a7a-108">Zeiger auf eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur, die die Bitmap definiert.</span><span class="sxs-lookup"><span data-stu-id="52a7a-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52a7a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52a7a-109">Return value</span></span>

<span data-ttu-id="52a7a-110">Gibt mediasubtype \_ RGB555 oder mediasubtype \_ RGB565 zurück.</span><span class="sxs-lookup"><span data-stu-id="52a7a-110">Returns MEDIASUBTYPE\_RGB555 or MEDIASUBTYPE\_RGB565.</span></span>

## <a name="requirements"></a><span data-ttu-id="52a7a-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52a7a-111">Requirements</span></span>



| <span data-ttu-id="52a7a-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52a7a-112">Requirement</span></span> | <span data-ttu-id="52a7a-113">Wert</span><span class="sxs-lookup"><span data-stu-id="52a7a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52a7a-114">Header</span><span class="sxs-lookup"><span data-stu-id="52a7a-114">Header</span></span><br/>  | <dl> <span data-ttu-id="52a7a-115"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52a7a-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="52a7a-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52a7a-116">Library</span></span><br/> | <dl> <span data-ttu-id="52a7a-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="52a7a-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a7a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52a7a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a7a-119">Video-und Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="52a7a-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




