---
description: 'Die querydirection-Methode ruft die Richtung der PIN (Eingabe oder Ausgabe) ab. Diese Methode implementiert die IPin:: querydirection-Methode.'
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Cbasepin. querydirection-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370705"
---
# <a name="cbasepinquerydirection-method"></a><span data-ttu-id="6468c-104">Cbasepin. querydirection-Methode</span><span class="sxs-lookup"><span data-stu-id="6468c-104">CBasePin.QueryDirection method</span></span>

<span data-ttu-id="6468c-105">Die- `QueryDirection` Methode ruft die Richtung der PIN (Eingabe oder Ausgabe) ab.</span><span class="sxs-lookup"><span data-stu-id="6468c-105">The `QueryDirection` method retrieves the direction of the pin (input or output).</span></span> <span data-ttu-id="6468c-106">Diese Methode implementiert die [**IPin:: querydirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6468c-106">This method implements the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6468c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6468c-107">Syntax</span></span>


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a><span data-ttu-id="6468c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6468c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6468c-109">*ppindir*</span><span class="sxs-lookup"><span data-stu-id="6468c-109">*pPinDir*</span></span> 
</dt> <dd>

<span data-ttu-id="6468c-110">Ein Zeiger auf eine Variable, die einen Member des enumerierten Typs der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) empfängt.</span><span class="sxs-lookup"><span data-stu-id="6468c-110">Pointer to a variable that receives a member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6468c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6468c-111">Return value</span></span>

<span data-ttu-id="6468c-112">Gibt den S \_ OK-oder E- \_ Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="6468c-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="6468c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6468c-113">Requirements</span></span>



| <span data-ttu-id="6468c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6468c-114">Requirement</span></span> | <span data-ttu-id="6468c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6468c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6468c-116">Header</span><span class="sxs-lookup"><span data-stu-id="6468c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6468c-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6468c-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6468c-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6468c-118">Library</span></span><br/> | <dl> <span data-ttu-id="6468c-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6468c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6468c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6468c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6468c-121">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6468c-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




