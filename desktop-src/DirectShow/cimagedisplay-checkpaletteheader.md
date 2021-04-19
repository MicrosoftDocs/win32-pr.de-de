---
description: Die checkpaletteheader-Methode überprüft die Paletteneinträge in einer videoinfo-Struktur.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Cimagedisplay. checkpaletteheader-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361650"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a><span data-ttu-id="8cda7-103">Cimagedisplay. checkpaletteheader-Methode</span><span class="sxs-lookup"><span data-stu-id="8cda7-103">CImageDisplay.CheckPaletteHeader method</span></span>

<span data-ttu-id="8cda7-104">Die- `CheckPaletteHeader` Methode überprüft die Paletteneinträge in einer [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8cda7-104">The `CheckPaletteHeader` method validates the palette entries in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cda7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cda7-105">Syntax</span></span>


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="8cda7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cda7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cda7-107">*pinput*</span><span class="sxs-lookup"><span data-stu-id="8cda7-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="8cda7-108">Zeiger auf eine **videoinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8cda7-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cda7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cda7-109">Return value</span></span>

<span data-ttu-id="8cda7-110">Gibt **true** zurück, wenn die Paletteneinträge gültig sind, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="8cda7-110">Returns **TRUE** if the palette entries are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cda7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cda7-111">Remarks</span></span>

<span data-ttu-id="8cda7-112">Wenn das Bildformat nicht palettisiert ist, überprüft die Methode, ob **biclrused** gleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="8cda7-112">If the image format is not palettized, the method verifies that **biClrUsed** equals zero.</span></span> <span data-ttu-id="8cda7-113">Andernfalls überprüft die Methode, ob das **bicompression** -Flag BI \_ RGB ist. **biclrimportant** ist nicht größer als **biclrused**. und die Anzahl der Paletteneinträge unter Berücksichtigung der Farbtiefe den maximalen Wert nicht überschreitet.</span><span class="sxs-lookup"><span data-stu-id="8cda7-113">Otherwise, the method verifies that the **biCompression** flag is BI\_RGB; **biClrImportant** is not greater than **biClrUsed**; and the number of palette entries does not exceed the maximum, given the color depth.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cda7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cda7-114">Requirements</span></span>



| <span data-ttu-id="8cda7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cda7-115">Requirement</span></span> | <span data-ttu-id="8cda7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8cda7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cda7-117">Header</span><span class="sxs-lookup"><span data-stu-id="8cda7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8cda7-118"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8cda7-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8cda7-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8cda7-119">Library</span></span><br/> | <dl> <span data-ttu-id="8cda7-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8cda7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cda7-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cda7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cda7-122">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8cda7-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




