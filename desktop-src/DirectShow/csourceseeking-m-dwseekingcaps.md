---
description: Suchfunktionen.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'Csourceseeking:: m_dwSeekingCaps Member (ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372571"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a><span data-ttu-id="8480e-103">Csourceseeking:: m \_ dwseekingcaps-Member</span><span class="sxs-lookup"><span data-stu-id="8480e-103">CSourceSeeking::m\_dwSeekingCaps member</span></span>

<span data-ttu-id="8480e-104">Suchfunktionen.</span><span class="sxs-lookup"><span data-stu-id="8480e-104">Seeking capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="8480e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8480e-105">Syntax</span></span>


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a><span data-ttu-id="8480e-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8480e-106">Remarks</span></span>

<span data-ttu-id="8480e-107">Standardmäßig wird der Wert auf die bitweise Kombination der folgenden Flags festgelegt:</span><span class="sxs-lookup"><span data-stu-id="8480e-107">By default, the value is set to the bitwise combination of the following flags:</span></span>

-   <span data-ttu-id="8480e-108">Sucht nach " \_ \_ canseekforward"</span><span class="sxs-lookup"><span data-stu-id="8480e-108">AM\_SEEKING\_CanSeekForwards</span></span>
-   <span data-ttu-id="8480e-109">Sucht nach " \_ \_ canseekabwärts"</span><span class="sxs-lookup"><span data-stu-id="8480e-109">AM\_SEEKING\_CanSeekBackwards</span></span>
-   <span data-ttu-id="8480e-110">Sucht nach " \_ \_ canseekabsolute"</span><span class="sxs-lookup"><span data-stu-id="8480e-110">AM\_SEEKING\_CanSeekAbsolute</span></span>
-   <span data-ttu-id="8480e-111">\_Sucht nach \_ cangetstoppos</span><span class="sxs-lookup"><span data-stu-id="8480e-111">AM\_SEEKING\_CanGetStopPos</span></span>
-   <span data-ttu-id="8480e-112">\_Suche nach \_ cangetduration</span><span class="sxs-lookup"><span data-stu-id="8480e-112">AM\_SEEKING\_CanGetDuration</span></span>

<span data-ttu-id="8480e-113">Wenn der Filter einen anderen Satz von Funktionen unterstützt, überschreiben Sie diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="8480e-113">If the filter supports a different set of capabilities, override this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8480e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8480e-114">Requirements</span></span>



| <span data-ttu-id="8480e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8480e-115">Requirement</span></span> | <span data-ttu-id="8480e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8480e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8480e-117">Header</span><span class="sxs-lookup"><span data-stu-id="8480e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8480e-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8480e-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8480e-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8480e-119">Library</span></span><br/> | <dl> <span data-ttu-id="8480e-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8480e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8480e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8480e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8480e-122">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8480e-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




