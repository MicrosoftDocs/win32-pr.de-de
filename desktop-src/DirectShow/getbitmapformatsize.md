---
description: Die getbitmapformatsize-Funktion berechnet die erforderliche Größe für eine videoinfo-Struktur, die eine angegebene BITMAPINFOHEADER-Struktur enthalten kann.
ms.assetid: a559415a-070f-4674-be12-a65a46025809
title: Getbitmapformatsize-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapFormatSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39a64f6d975e403de6c177906b23ef7e09f29ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373776"
---
# <a name="getbitmapformatsize-function"></a><span data-ttu-id="22473-103">Getbitmapformatsize-Funktion</span><span class="sxs-lookup"><span data-stu-id="22473-103">GetBitmapFormatSize function</span></span>

<span data-ttu-id="22473-104">Die- `GetBitmapFormatSize` Funktion berechnet die erforderliche Größe für eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur, die eine angegebene [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="22473-104">The `GetBitmapFormatSize` function calculates the size needed for a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that can hold a specified [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="22473-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22473-105">Syntax</span></span>


```C++
LONG GetBitmapFormatSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="22473-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22473-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22473-107">*pheader*</span><span class="sxs-lookup"><span data-stu-id="22473-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="22473-108">Zeiger auf eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="22473-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22473-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22473-109">Return value</span></span>

<span data-ttu-id="22473-110">Gibt die Größe in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="22473-110">Returns the size, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="22473-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22473-111">Remarks</span></span>

<span data-ttu-id="22473-112">Auf eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur folgen möglicherweise Farb Masken oder Paletteneinträge, sodass es schwierig sein kann, die Anzahl von Bytes zu bestimmen, die erforderlich sind, um eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur aus einer vorhandenen **BITMAPINFOHEADER** -Struktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="22473-112">A [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure might be followed by color masks or palette entries, so it can be difficult to determine the number of bytes required to construct a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure from an existing **BITMAPINFOHEADER** structure.</span></span>

<span data-ttu-id="22473-113">Um eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur in eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur zu kopieren, verwenden Sie das [**Header**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) Makro, das den korrekten Offset berechnet.</span><span class="sxs-lookup"><span data-stu-id="22473-113">To copy a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure into a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure, use the [**HEADER**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) macro, which calculates the correct offset.</span></span>

## <a name="examples"></a><span data-ttu-id="22473-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22473-114">Examples</span></span>


```
LONG size = GetBitmapFormatSize(&bmi);

VIDEOINFO *pVi = static_cast<VIDEOINFO*>(CoTaskMemAlloc(size));

if (pVi != NULL)
{
    CopyMemory(HEADER(pVi), &bmi, sizeof(BITMAPINFOHEADER));
}
```



## <a name="requirements"></a><span data-ttu-id="22473-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22473-115">Requirements</span></span>



| <span data-ttu-id="22473-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22473-116">Requirement</span></span> | <span data-ttu-id="22473-117">Wert</span><span class="sxs-lookup"><span data-stu-id="22473-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22473-118">Header</span><span class="sxs-lookup"><span data-stu-id="22473-118">Header</span></span><br/>  | <dl> <span data-ttu-id="22473-119"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22473-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="22473-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22473-120">Library</span></span><br/> | <dl> <span data-ttu-id="22473-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="22473-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22473-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22473-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22473-123">Video-und Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="22473-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




