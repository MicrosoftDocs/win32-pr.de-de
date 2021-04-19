---
description: Bestimmt, ob ein Quell Rechteck gültig ist.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Cbasecontrolvideo. checksourcerect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa219687dabcf9124662e3269d157fb0a163a6a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366055"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a><span data-ttu-id="25e4e-103">Cbasecontrolvideo. checksourcerect-Methode</span><span class="sxs-lookup"><span data-stu-id="25e4e-103">CBaseControlVideo.CheckSourceRect method</span></span>

<span data-ttu-id="25e4e-104">Bestimmt, ob ein Quell Rechteck gültig ist.</span><span class="sxs-lookup"><span data-stu-id="25e4e-104">Determines if a source rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="25e4e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="25e4e-105">Syntax</span></span>


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="25e4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25e4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25e4e-107">*psourcerect*</span><span class="sxs-lookup"><span data-stu-id="25e4e-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="25e4e-108">Zeiger auf das zu Überprüfung des Quell Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="25e4e-108">Pointer to the source rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25e4e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25e4e-109">Return value</span></span>

<span data-ttu-id="25e4e-110">Gibt "E \_ invalidArg" zurück, wenn es ungültig ist; andernfalls wird "noError (S OK)" zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="25e4e-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="25e4e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25e4e-111">Remarks</span></span>

<span data-ttu-id="25e4e-112">Diese Member-Funktion überprüft, ob das angeforderte Quell Rechteck das verfügbare Quellvideo nicht überschreitet.</span><span class="sxs-lookup"><span data-stu-id="25e4e-112">This member function checks that the source rectangle requested does not exceed the available source video.</span></span> <span data-ttu-id="25e4e-113">Die linke und die obere Koordinate dürfen nicht negativ sein, und die Breite und die Höhe dürfen nicht den rechten und unteren Rand des Videos überschreiten.</span><span class="sxs-lookup"><span data-stu-id="25e4e-113">The left and top coordinates cannot be negative, and the width and height cannot exceed the right and bottom of the video.</span></span>

## <a name="requirements"></a><span data-ttu-id="25e4e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25e4e-114">Requirements</span></span>



| <span data-ttu-id="25e4e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25e4e-115">Requirement</span></span> | <span data-ttu-id="25e4e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="25e4e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25e4e-117">Header</span><span class="sxs-lookup"><span data-stu-id="25e4e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="25e4e-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25e4e-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="25e4e-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25e4e-119">Library</span></span><br/> | <dl> <span data-ttu-id="25e4e-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="25e4e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e4e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25e4e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e4e-122">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="25e4e-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




