---
description: Die Methode checkheaderordinüberprüft eine BITMAPINFOHEADER-Struktur. Diese Methode ist nur für nicht komprimierte RGB-Typen, nicht für komprimierte Typen oder YUV-Typen nützlich.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Cimagedisplay. checkheadergültigkeit-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364597"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a><span data-ttu-id="19b83-104">Cimagedisplay. checkheadergültigkeit-Methode</span><span class="sxs-lookup"><span data-stu-id="19b83-104">CImageDisplay.CheckHeaderValidity method</span></span>

<span data-ttu-id="19b83-105">Die- `CheckHeaderValidity` Methode überprüft eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="19b83-105">The `CheckHeaderValidity` method validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="19b83-106">Diese Methode ist nur für nicht komprimierte RGB-Typen, nicht für komprimierte Typen oder YUV-Typen nützlich.</span><span class="sxs-lookup"><span data-stu-id="19b83-106">This method is useful only for uncompressed RGB types, not for compressed types or YUV types.</span></span>

## <a name="syntax"></a><span data-ttu-id="19b83-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="19b83-107">Syntax</span></span>


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="19b83-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="19b83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19b83-109">*pinput*</span><span class="sxs-lookup"><span data-stu-id="19b83-109">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="19b83-110">Zeiger auf eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur, die die **BITMAPINFOHEADER** -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="19b83-110">Pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure containing the **BITMAPINFOHEADER** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19b83-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19b83-111">Return value</span></span>

<span data-ttu-id="19b83-112">Gibt **true** zurück, wenn der **BITMAPINFOHEADER** gültig ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="19b83-112">Returns **TRUE** if the **BITMAPINFOHEADER** is valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="19b83-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19b83-113">Remarks</span></span>

<span data-ttu-id="19b83-114">Diese Methode überprüft, ob die Bild Dimensionen nicht negativ sind. der Komprimierungstyp ist BI \_ RGB-oder BI- \_ Bitfields; die Farbtiefe und die Farb Masken sind gültig. der **Biplane** -Member ist gleich 1, und die **bisize** -und **bisizeimage** -Member sind richtig.</span><span class="sxs-lookup"><span data-stu-id="19b83-114">This method checks that the image dimensions are non-negative; the compression type is BI\_RGB or BI\_BITFIELDS; the color depth and color masks are valid; the **biPlanes** member equals one; and the **biSize** and **biSizeImage** members are correct.</span></span> <span data-ttu-id="19b83-115">Er prüft außerdem ggf., ob häufige Fehler in den paletteneinträgen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="19b83-115">It also checks for common errors in the palette entries, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="19b83-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19b83-116">Requirements</span></span>



| <span data-ttu-id="19b83-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19b83-117">Requirement</span></span> | <span data-ttu-id="19b83-118">Wert</span><span class="sxs-lookup"><span data-stu-id="19b83-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19b83-119">Header</span><span class="sxs-lookup"><span data-stu-id="19b83-119">Header</span></span><br/>  | <dl> <span data-ttu-id="19b83-120"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19b83-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="19b83-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19b83-121">Library</span></span><br/> | <dl> <span data-ttu-id="19b83-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="19b83-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19b83-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19b83-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19b83-124">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="19b83-124">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




