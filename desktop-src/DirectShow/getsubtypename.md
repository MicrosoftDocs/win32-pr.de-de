---
description: Die getsubtypame-Funktion Ruft den lesbaren Namen eines Video Untertyps ab.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Getsubtypame-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358678"
---
# <a name="getsubtypename-function"></a><span data-ttu-id="c75ca-103">Getsubtypame-Funktion</span><span class="sxs-lookup"><span data-stu-id="c75ca-103">GetSubtypeName function</span></span>

<span data-ttu-id="c75ca-104">Die `GetSubtypeName` -Funktion Ruft den lesbaren Namen eines Video Untertyps ab.</span><span class="sxs-lookup"><span data-stu-id="c75ca-104">The `GetSubtypeName` function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75ca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c75ca-105">Syntax</span></span>


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="c75ca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c75ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c75ca-107">*psubtype*</span><span class="sxs-lookup"><span data-stu-id="c75ca-107">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="c75ca-108">Zeiger auf einen Video Untertyp- **GUID**.</span><span class="sxs-lookup"><span data-stu-id="c75ca-108">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c75ca-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c75ca-109">Return value</span></span>

<span data-ttu-id="c75ca-110">Gibt eine Zeichenfolge zurück, die den Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="c75ca-110">Returns a string containing the name.</span></span>

## <a name="requirements"></a><span data-ttu-id="c75ca-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c75ca-111">Requirements</span></span>



| <span data-ttu-id="c75ca-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c75ca-112">Requirement</span></span> | <span data-ttu-id="c75ca-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c75ca-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c75ca-114">Header</span><span class="sxs-lookup"><span data-stu-id="c75ca-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c75ca-115"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c75ca-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c75ca-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c75ca-116">Library</span></span><br/> | <dl> <span data-ttu-id="c75ca-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c75ca-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c75ca-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c75ca-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75ca-119">Video-und Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="c75ca-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




