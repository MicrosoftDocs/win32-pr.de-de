---
description: Die checktargetrect-Methode bestimmt, ob ein Ziel Rechteck gültig ist.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Cbasecontrolvideo. checktargetrect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368508"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a><span data-ttu-id="ecb3b-103">Cbasecontrolvideo. checktargetrect-Methode</span><span class="sxs-lookup"><span data-stu-id="ecb3b-103">CBaseControlVideo.CheckTargetRect method</span></span>

<span data-ttu-id="ecb3b-104">Die- `CheckTargetRect` Methode bestimmt, ob ein Ziel Rechteck gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ecb3b-104">The `CheckTargetRect` method determines if a target rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb3b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecb3b-105">Syntax</span></span>


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="ecb3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecb3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb3b-107">*ptargetrect*</span><span class="sxs-lookup"><span data-stu-id="ecb3b-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="ecb3b-108">Zeiger auf das zu Überprüfung des Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="ecb3b-108">Pointer to the target rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb3b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ecb3b-109">Return value</span></span>

<span data-ttu-id="ecb3b-110">Gibt "E \_ invalidArg" zurück, wenn es ungültig ist; andernfalls wird "noError (S OK)" zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="ecb3b-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="ecb3b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ecb3b-111">Remarks</span></span>

<span data-ttu-id="ecb3b-112">Diese Member-Funktion bestimmt, ob das angeforderte Ziel Rechteck gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ecb3b-112">This member function determines if the target rectangle requested is valid.</span></span> <span data-ttu-id="ecb3b-113">Da das Ziel Rechteck eine Position im logischen Client des Fensters angibt, können die Koordinaten negativ sein, obwohl die Gesamtbreite und Höhe nicht 0 (null) oder ein negativer Wert sein dürfen.</span><span class="sxs-lookup"><span data-stu-id="ecb3b-113">Because the destination rectangle specifies a position in the logical client of the window, the coordinates can be negative, although the overall width and height cannot be zero or a negative value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb3b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecb3b-114">Requirements</span></span>



| <span data-ttu-id="ecb3b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ecb3b-115">Requirement</span></span> | <span data-ttu-id="ecb3b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ecb3b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb3b-117">Header</span><span class="sxs-lookup"><span data-stu-id="ecb3b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ecb3b-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecb3b-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ecb3b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ecb3b-119">Library</span></span><br/> | <dl> <span data-ttu-id="ecb3b-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ecb3b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb3b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecb3b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb3b-122">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ecb3b-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




