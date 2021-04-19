---
description: Die Element \_ Variable "m endsample" gibt die Endzeit des neuesten Beispiels an.
ms.assetid: 694815b6-8da5-4174-b2c7-7d686a557c6c
title: 'Cdrawimage:: m_EndSample Member (winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_EndSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78268e8335d6dd8c24497a9e4d74b0caab205a99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373800"
---
# <a name="cdrawimagem_endsample-member"></a><span data-ttu-id="54300-103">Cdrawimage:: m- \_ endsample-Member</span><span class="sxs-lookup"><span data-stu-id="54300-103">CDrawImage::m\_EndSample member</span></span>

<span data-ttu-id="54300-104">Die `m_EndSample` Member-Variable gibt die Endzeit des neuesten Beispiels an.</span><span class="sxs-lookup"><span data-stu-id="54300-104">The `m_EndSample` member variable specifies the stop time of the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="54300-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54300-105">Syntax</span></span>


```C++
CRefTime m_EndSample;
```



## <a name="remarks"></a><span data-ttu-id="54300-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54300-106">Remarks</span></span>

<span data-ttu-id="54300-107">Der Wert ist nur innerhalb der [**cdrawimage::D isplaysampletimes**](cdrawimage-displaysampletimes.md) -Methode gültig.</span><span class="sxs-lookup"><span data-stu-id="54300-107">The value is only valid inside the [**CDrawImage::DisplaySampleTimes**](cdrawimage-displaysampletimes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="54300-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54300-108">Requirements</span></span>



| <span data-ttu-id="54300-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54300-109">Requirement</span></span> | <span data-ttu-id="54300-110">Wert</span><span class="sxs-lookup"><span data-stu-id="54300-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54300-111">Header</span><span class="sxs-lookup"><span data-stu-id="54300-111">Header</span></span><br/>  | <dl> <span data-ttu-id="54300-112"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54300-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="54300-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54300-113">Library</span></span><br/> | <dl> <span data-ttu-id="54300-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="54300-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54300-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54300-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54300-116">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="54300-116">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




