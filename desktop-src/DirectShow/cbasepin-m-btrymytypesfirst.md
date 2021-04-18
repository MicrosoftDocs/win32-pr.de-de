---
description: Flag, das angibt, ob die PIN vor denen der empfangenden Pin ihre eigenen bevorzugten Medientypen ausprobiert.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'Cbasepin:: m_bTryMyTypesFirst Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f98021b6ba97d32974f26ac4e76ca31fa54e5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371275"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a><span data-ttu-id="b80c0-103">Cbasepin:: m \_ btrymytypesfirst-Member</span><span class="sxs-lookup"><span data-stu-id="b80c0-103">CBasePin::m\_bTryMyTypesFirst member</span></span>

<span data-ttu-id="b80c0-104">Flag, das angibt, ob die PIN vor denen der empfangenden Pin ihre eigenen bevorzugten Medientypen ausprobiert.</span><span class="sxs-lookup"><span data-stu-id="b80c0-104">Flag that indicates whether the pin tries its own preferred media types before those of the receiving pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b80c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b80c0-105">Syntax</span></span>


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a><span data-ttu-id="b80c0-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b80c0-106">Remarks</span></span>

<span data-ttu-id="b80c0-107">Dieses Flag ist standardmäßig auf **false** eingestellt.</span><span class="sxs-lookup"><span data-stu-id="b80c0-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="b80c0-108">Wenn das Flag " **true**" ist, kehrt die [**cbasepin:: agreemediatype**](cbasepin-agreemediatype.md) -Methode die Reihenfolge um, in der die Medientypen ausprobiert werden.</span><span class="sxs-lookup"><span data-stu-id="b80c0-108">If the flag is **TRUE**, the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method reverses the order in which it tries media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="b80c0-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b80c0-109">Requirements</span></span>



| <span data-ttu-id="b80c0-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b80c0-110">Requirement</span></span> | <span data-ttu-id="b80c0-111">Wert</span><span class="sxs-lookup"><span data-stu-id="b80c0-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b80c0-112">Header</span><span class="sxs-lookup"><span data-stu-id="b80c0-112">Header</span></span><br/>  | <dl> <span data-ttu-id="b80c0-113"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b80c0-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b80c0-114">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b80c0-114">Library</span></span><br/> | <dl> <span data-ttu-id="b80c0-115">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b80c0-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b80c0-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b80c0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b80c0-117">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b80c0-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




