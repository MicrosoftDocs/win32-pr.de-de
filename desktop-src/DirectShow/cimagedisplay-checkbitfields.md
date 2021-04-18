---
description: Die checkbitfields-Methode überprüft die Farb Masken in einer videoinfo-Struktur.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Cimagedisplay. checkbitfields-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358257"
---
# <a name="cimagedisplaycheckbitfields-method"></a><span data-ttu-id="69746-103">Cimagedisplay. checkbitfields-Methode</span><span class="sxs-lookup"><span data-stu-id="69746-103">CImageDisplay.CheckBitFields method</span></span>

<span data-ttu-id="69746-104">Die- `CheckBitFields` Methode überprüft die Farb Masken in einer [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="69746-104">The `CheckBitFields` method validates the color masks in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="69746-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69746-105">Syntax</span></span>


```C++
BOOL CheckBitFields(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="69746-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="69746-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69746-107">*pinput*</span><span class="sxs-lookup"><span data-stu-id="69746-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="69746-108">Zeiger auf eine **videoinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="69746-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69746-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69746-109">Return value</span></span>

<span data-ttu-id="69746-110">Gibt **true** zurück, wenn die Farb Masken gültig sind, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="69746-110">Returns **TRUE** if the color masks are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="69746-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69746-111">Remarks</span></span>

<span data-ttu-id="69746-112">Diese Methode überprüft, ob die Farb Maske für jede Farbkomponente zwischen 1 und 8 Bits lang ist, und dass jede Farb Maske eine zusammenhängende Sequenz von Bits ist.</span><span class="sxs-lookup"><span data-stu-id="69746-112">This method verifies that the color mask for each color component is between one and eight bits long, and that each color mask is a contiguous sequence of bits.</span></span> <span data-ttu-id="69746-113">Diese Methode wird nur aufgerufen, wenn der **bicompression** -Member auf BI Bitfields festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="69746-113">Call this method only when the **biCompression** member is set to BI\_BITFIELDS.</span></span>

## <a name="requirements"></a><span data-ttu-id="69746-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69746-114">Requirements</span></span>



| <span data-ttu-id="69746-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69746-115">Requirement</span></span> | <span data-ttu-id="69746-116">Wert</span><span class="sxs-lookup"><span data-stu-id="69746-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69746-117">Header</span><span class="sxs-lookup"><span data-stu-id="69746-117">Header</span></span><br/>  | <dl> <span data-ttu-id="69746-118"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69746-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="69746-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="69746-119">Library</span></span><br/> | <dl> <span data-ttu-id="69746-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="69746-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69746-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69746-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69746-122">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="69746-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




