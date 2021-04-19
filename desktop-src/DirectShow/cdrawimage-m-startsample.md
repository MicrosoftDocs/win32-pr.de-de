---
description: Die \_ Member-Variable m startsample gibt die Startzeit des neuesten Beispiels an.
ms.assetid: 2e6d6893-d57b-4009-a6ec-40dc0878d9c4
title: 'Cdrawimage:: m_StartSample Member (winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_StartSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fd8039b1d37d0e61a150ed6c6944f0052089b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373943"
---
# <a name="cdrawimagem_startsample-member"></a><span data-ttu-id="3663b-103">Cdrawimage:: m \_ startsample-Member</span><span class="sxs-lookup"><span data-stu-id="3663b-103">CDrawImage::m\_StartSample member</span></span>

<span data-ttu-id="3663b-104">Die Member-Variable **m \_ startsample** gibt die Startzeit des neuesten Beispiels an.</span><span class="sxs-lookup"><span data-stu-id="3663b-104">The **m\_StartSample** member variable specifies the start time of the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="3663b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3663b-105">Syntax</span></span>


```C++
CRefTime m_StartSample;
```



## <a name="remarks"></a><span data-ttu-id="3663b-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3663b-106">Remarks</span></span>

<span data-ttu-id="3663b-107">Der Wert ist nur innerhalb der [**cdrawimage::D isplaysampletimes**](cdrawimage-displaysampletimes.md) -Methode gültig.</span><span class="sxs-lookup"><span data-stu-id="3663b-107">The value is only valid inside the [**CDrawImage::DisplaySampleTimes**](cdrawimage-displaysampletimes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3663b-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3663b-108">Requirements</span></span>



| <span data-ttu-id="3663b-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3663b-109">Requirement</span></span> | <span data-ttu-id="3663b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="3663b-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3663b-111">Header</span><span class="sxs-lookup"><span data-stu-id="3663b-111">Header</span></span><br/>  | <dl> <span data-ttu-id="3663b-112"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3663b-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3663b-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3663b-113">Library</span></span><br/> | <dl> <span data-ttu-id="3663b-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3663b-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3663b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3663b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3663b-116">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3663b-116">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




