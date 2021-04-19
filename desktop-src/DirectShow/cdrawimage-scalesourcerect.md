---
description: Die scalesourcerect-Methode skaliert ein Rechteck, wenn es einen Unterschied zwischen der nativen Videogröße und dem Medientyp Format gibt.
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: Cdrawimage. scalesourcerect-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369572"
---
# <a name="cdrawimagescalesourcerect-method"></a><span data-ttu-id="cd24a-103">Cdrawimage. scalesourcerect-Methode</span><span class="sxs-lookup"><span data-stu-id="cd24a-103">CDrawImage.ScaleSourceRect method</span></span>

<span data-ttu-id="cd24a-104">Die `ScaleSourceRect` -Methode skaliert ein Rechteck, wenn es einen Unterschied zwischen der nativen Videogröße und dem Medientyp Format gibt.</span><span class="sxs-lookup"><span data-stu-id="cd24a-104">The `ScaleSourceRect` method scales a rectangle, if there is a difference between the native video size and the media type format.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd24a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd24a-105">Syntax</span></span>


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="cd24a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd24a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd24a-107">*psource*</span><span class="sxs-lookup"><span data-stu-id="cd24a-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="cd24a-108">Zeiger auf ein nicht skaliertes Rechteck.</span><span class="sxs-lookup"><span data-stu-id="cd24a-108">Pointer to an unscaled rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd24a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd24a-109">Return value</span></span>

<span data-ttu-id="cd24a-110">Gibt das skalierte Rechteck zurück.</span><span class="sxs-lookup"><span data-stu-id="cd24a-110">Returns the scaled rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd24a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd24a-111">Remarks</span></span>

<span data-ttu-id="cd24a-112">In der **cdrawimage** -Klasse gibt diese Methode *psource* ohne Änderung zurück.</span><span class="sxs-lookup"><span data-stu-id="cd24a-112">In the **CDrawImage** class, this method returns *pSource* without any change.</span></span> <span data-ttu-id="cd24a-113">Sie können diese Methode überschreiben, wenn der Filter das eingehende Video Bild ausdehnt.</span><span class="sxs-lookup"><span data-stu-id="cd24a-113">You can override this method if the filter stretches the incoming video image.</span></span> <span data-ttu-id="cd24a-114">Beispielsweise könnte die Größe des nativen Videos 320 240 lauten, der Medientyp der Eingabe-PIN kann jedoch 640 480 lauten.</span><span class="sxs-lookup"><span data-stu-id="cd24a-114">For example, the native video size might be 320   240, but the media type on the input pin might be 640   480.</span></span> <span data-ttu-id="cd24a-115">In diesem Fall muss der Filter das Quell Rechteck mit dem Faktor 2 skalieren.</span><span class="sxs-lookup"><span data-stu-id="cd24a-115">In that case the filter would need to scale the source rectangle by a factor of 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd24a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd24a-116">Requirements</span></span>



| <span data-ttu-id="cd24a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd24a-117">Requirement</span></span> | <span data-ttu-id="cd24a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cd24a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd24a-119">Header</span><span class="sxs-lookup"><span data-stu-id="cd24a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cd24a-120"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd24a-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cd24a-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cd24a-121">Library</span></span><br/> | <dl> <span data-ttu-id="cd24a-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="cd24a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd24a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd24a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd24a-124">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cd24a-124">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




