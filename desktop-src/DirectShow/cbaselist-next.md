---
description: Die nächste Methode ruft die nächste Position in der Liste ab.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Cbaselist. Next-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367049"
---
# <a name="cbaselistnext-method"></a><span data-ttu-id="8e86a-103">Cbaselist. Next-Methode</span><span class="sxs-lookup"><span data-stu-id="8e86a-103">CBaseList.Next method</span></span>

<span data-ttu-id="8e86a-104">Die- `Next` Methode ruft die nächste Position in der Liste ab.</span><span class="sxs-lookup"><span data-stu-id="8e86a-104">The `Next` method retrieves the next position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e86a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e86a-105">Syntax</span></span>


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="8e86a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e86a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e86a-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="8e86a-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="8e86a-108">Positionswert.</span><span class="sxs-lookup"><span data-stu-id="8e86a-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e86a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e86a-109">Return value</span></span>

<span data-ttu-id="8e86a-110">Gibt den Positionsindikator zurück, der der von *POS* angegebenen Position folgt.</span><span class="sxs-lookup"><span data-stu-id="8e86a-110">Returns the position indicator that follows the position specified by *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e86a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e86a-111">Remarks</span></span>

<span data-ttu-id="8e86a-112">Wenn *POS* die letzte Position in der Liste ist, gibt die Methode **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="8e86a-112">If *pos* is the last position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="8e86a-113">Wenn *POS* **null** ist, gibt die Methode die erste Position in der Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="8e86a-113">If *pos* is **NULL**, the method returns the first position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e86a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e86a-114">Requirements</span></span>



| <span data-ttu-id="8e86a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e86a-115">Requirement</span></span> | <span data-ttu-id="8e86a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8e86a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e86a-117">Header</span><span class="sxs-lookup"><span data-stu-id="8e86a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8e86a-118"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e86a-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8e86a-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8e86a-119">Library</span></span><br/> | <dl> <span data-ttu-id="8e86a-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8e86a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e86a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e86a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e86a-122">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8e86a-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




