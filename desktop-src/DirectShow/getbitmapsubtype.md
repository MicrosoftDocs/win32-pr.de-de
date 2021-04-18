---
description: Die getbitmapsubtype-Funktion gibt die untergeordnete GUID des Mediums für die angegebene Bitmap zurück.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Getbitmapsubtype-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364718"
---
# <a name="getbitmapsubtype-function"></a><span data-ttu-id="9723a-103">Getbitmapsubtype-Funktion</span><span class="sxs-lookup"><span data-stu-id="9723a-103">GetBitmapSubtype function</span></span>

<span data-ttu-id="9723a-104">Die- `GetBitmapSubtype` Funktion gibt die **GUID** für den Medien Untertyp für die angegebene Bitmap zurück.</span><span class="sxs-lookup"><span data-stu-id="9723a-104">The `GetBitmapSubtype` function returns the media subtype **GUID** for the specified bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="9723a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9723a-105">Syntax</span></span>


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="9723a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9723a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9723a-107">*pheader*</span><span class="sxs-lookup"><span data-stu-id="9723a-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="9723a-108">Zeiger auf eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9723a-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9723a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9723a-109">Return value</span></span>

<span data-ttu-id="9723a-110">Gibt die **GUID** des Medien Untertyps zurück.</span><span class="sxs-lookup"><span data-stu-id="9723a-110">Returns the media subtype **GUID**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9723a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9723a-111">Remarks</span></span>

<span data-ttu-id="9723a-112">Bei nicht komprimierten RGB-Typen ordnet diese Funktion dem Untertyp das **biBitCount** -Feld zu.</span><span class="sxs-lookup"><span data-stu-id="9723a-112">For uncompressed RGB types, this function maps the **biBitCount** field to the subtype.</span></span> <span data-ttu-id="9723a-113">Für komprimierte Video Typen verwendet diese Funktion die [**fourccmap**](fourccmap.md) -Klasse, um das **bicompression** -Feld dem Untertyp zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9723a-113">For compressed video types, this function uses the [**FOURCCMap**](fourccmap.md) class to map the **biCompression** field to the subtype.</span></span>

<span data-ttu-id="9723a-114">Wenn die Funktion dem Format nicht mit einem Untertyp entsprechen kann, ist der Rückgabewert GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="9723a-114">If the function cannot match the format to a subtype, the return value is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9723a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9723a-115">Requirements</span></span>



| <span data-ttu-id="9723a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9723a-116">Requirement</span></span> | <span data-ttu-id="9723a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9723a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9723a-118">Header</span><span class="sxs-lookup"><span data-stu-id="9723a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9723a-119"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9723a-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9723a-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9723a-120">Library</span></span><br/> | <dl> <span data-ttu-id="9723a-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9723a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9723a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9723a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9723a-123">Video-und Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="9723a-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




