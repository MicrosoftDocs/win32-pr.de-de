---
description: Die setcontrolvideopin-Methode legt die vom Filter verwendete PIN fest.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Cbasecontrolvideo. setcontrolvideopin-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369422"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a><span data-ttu-id="c2e22-103">Cbasecontrolvideo. setcontrolvideopin-Methode</span><span class="sxs-lookup"><span data-stu-id="c2e22-103">CBaseControlVideo.SetControlVideoPin method</span></span>

<span data-ttu-id="c2e22-104">Die- `SetControlVideoPin` Methode legt die vom Filter verwendete PIN fest.</span><span class="sxs-lookup"><span data-stu-id="c2e22-104">The `SetControlVideoPin` method sets the pin used by the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2e22-105">Syntax</span></span>


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="c2e22-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2e22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e22-107">*ppin*</span><span class="sxs-lookup"><span data-stu-id="c2e22-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="c2e22-108">Zeiger auf die PIN, mit der die Schnittstelle synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c2e22-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e22-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2e22-109">Return value</span></span>

<span data-ttu-id="c2e22-110">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="c2e22-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2e22-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2e22-111">Remarks</span></span>

<span data-ttu-id="c2e22-112">Die-Schnittstelle kann nur aufgerufen werden, wenn der Filter erfolgreich verbunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c2e22-112">The interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="c2e22-113">Das-Objekt wird durch diese Methode an die PIN übergeben, mit der es synchronisiert wird. in den meisten Fällen wird festgestellt, ob die PIN verbunden ist, wenn Sie über eine Schnittstellen Methode mit dem Namen verfügt, und \_ \_ \_ Wenn Sie fehlschlägt, wird VFW E nicht verbunden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c2e22-113">The object is passed through this method to the pin with which it is synchronized; in most cases it will determine if the pin is connected when it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e22-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2e22-114">Requirements</span></span>



| <span data-ttu-id="c2e22-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2e22-115">Requirement</span></span> | <span data-ttu-id="c2e22-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c2e22-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e22-117">Header</span><span class="sxs-lookup"><span data-stu-id="c2e22-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c2e22-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2e22-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c2e22-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2e22-119">Library</span></span><br/> | <dl> <span data-ttu-id="c2e22-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c2e22-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e22-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2e22-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e22-122">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c2e22-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




