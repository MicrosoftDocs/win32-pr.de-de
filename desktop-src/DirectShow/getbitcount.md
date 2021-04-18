---
description: Die getbitcount-Funktion gibt die Anzahl der Bits pro Pixel zurück, die von einem angegebenen Video Untertyp verwendet werden. Diese Funktion ist nur für nicht komprimierte RGB-Untertypen gültig.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: Getbitcount-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368428"
---
# <a name="getbitcount-function"></a><span data-ttu-id="688fe-104">Getbitcount-Funktion</span><span class="sxs-lookup"><span data-stu-id="688fe-104">GetBitCount function</span></span>

<span data-ttu-id="688fe-105">Die- `GetBitCount` Funktion gibt die Anzahl der Bits pro Pixel zurück, die von einem angegebenen Video Untertyp verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="688fe-105">The `GetBitCount` function returns the number of bits per pixel used by a specified video subtype.</span></span> <span data-ttu-id="688fe-106">Diese Funktion ist nur für nicht komprimierte RGB-Untertypen gültig.</span><span class="sxs-lookup"><span data-stu-id="688fe-106">This function is valid for uncompressed RGB subtypes only.</span></span>

## <a name="syntax"></a><span data-ttu-id="688fe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="688fe-107">Syntax</span></span>


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="688fe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="688fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="688fe-109">*psubtype*</span><span class="sxs-lookup"><span data-stu-id="688fe-109">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="688fe-110">Zeiger auf einen Video Untertyp- **GUID**.</span><span class="sxs-lookup"><span data-stu-id="688fe-110">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="688fe-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="688fe-111">Return value</span></span>

<span data-ttu-id="688fe-112">Gibt die Anzahl der Bits pro Pixel für diesen Untertyp oder den Wert von "-Wert für die **\_ maximal** zulässige Größe zurück, wenn der Untertyp nicht erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="688fe-112">Returns the number of bits per pixel for this subtype, or the value **USHRT\_MAX** if the subtype is not recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="688fe-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="688fe-113">Requirements</span></span>



| <span data-ttu-id="688fe-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="688fe-114">Requirement</span></span> | <span data-ttu-id="688fe-115">Wert</span><span class="sxs-lookup"><span data-stu-id="688fe-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="688fe-116">Header</span><span class="sxs-lookup"><span data-stu-id="688fe-116">Header</span></span><br/>  | <dl> <span data-ttu-id="688fe-117"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="688fe-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="688fe-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="688fe-118">Library</span></span><br/> | <dl> <span data-ttu-id="688fe-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="688fe-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="688fe-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="688fe-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="688fe-121">Video-und Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="688fe-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




