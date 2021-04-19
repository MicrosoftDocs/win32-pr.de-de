---
description: Die Updateformat-Methode füllt einige optionale Member der videoinfo-Struktur aus.
ms.assetid: 5ca34fa0-eef4-44f5-bbcc-e686e5181d86
title: Cimagedisplay. Updateformat-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.UpdateFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6966da171e37e1cc285afc1872d221ca7aad99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370098"
---
# <a name="cimagedisplayupdateformat-method"></a><span data-ttu-id="65bf0-103">Cimagedisplay. Updateformat-Methode</span><span class="sxs-lookup"><span data-stu-id="65bf0-103">CImageDisplay.UpdateFormat method</span></span>

<span data-ttu-id="65bf0-104">Die- `UpdateFormat` Methode füllt einige optionale Member der [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="65bf0-104">The `UpdateFormat` method fills in some optional members of the [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="65bf0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65bf0-105">Syntax</span></span>


```C++
HRESULT UpdateFormat(
   VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="65bf0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65bf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65bf0-107">*pvideoinfo*</span><span class="sxs-lookup"><span data-stu-id="65bf0-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="65bf0-108">Zeiger auf eine **videoinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="65bf0-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65bf0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65bf0-109">Return value</span></span>

<span data-ttu-id="65bf0-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="65bf0-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="65bf0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65bf0-111">Remarks</span></span>

<span data-ttu-id="65bf0-112">Diese Methode legt die **biclrused**-, **biclrimportant**-und **bisizeimage** -Member auf die richtigen Werte fest und löscht die Quell-und Ziel Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="65bf0-112">This method sets the **biClrUsed**, **biClrImportant**, and **biSizeImage** members to the correct values, and clears the source and target rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="65bf0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65bf0-113">Requirements</span></span>



| <span data-ttu-id="65bf0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65bf0-114">Requirement</span></span> | <span data-ttu-id="65bf0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="65bf0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65bf0-116">Header</span><span class="sxs-lookup"><span data-stu-id="65bf0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="65bf0-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65bf0-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="65bf0-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65bf0-118">Library</span></span><br/> | <dl> <span data-ttu-id="65bf0-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="65bf0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65bf0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65bf0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65bf0-121">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="65bf0-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




