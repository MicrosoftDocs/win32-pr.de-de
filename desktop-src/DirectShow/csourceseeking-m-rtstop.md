---
description: Endzeit. Standardmäßig ist der Wert auf eine sehr große Zahl festgelegt. Die abgeleitete Klasse kann den Wert im Konstruktor zurücksetzen oder wenn der Filter initialisiert wird.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'Csourceseeking:: m_rtStop Member (ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365527"
---
# <a name="csourceseekingm_rtstop-member"></a><span data-ttu-id="425bb-105">Csourceseeking:: m \_ rtstoppt-Member</span><span class="sxs-lookup"><span data-stu-id="425bb-105">CSourceSeeking::m\_rtStop member</span></span>

<span data-ttu-id="425bb-106">Endzeit.</span><span class="sxs-lookup"><span data-stu-id="425bb-106">Stop time.</span></span> <span data-ttu-id="425bb-107">Standardmäßig ist der Wert auf eine sehr große Zahl festgelegt.</span><span class="sxs-lookup"><span data-stu-id="425bb-107">By default, the value is set to a very large number.</span></span> <span data-ttu-id="425bb-108">Die abgeleitete Klasse kann den Wert im Konstruktor zurücksetzen oder wenn der Filter initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="425bb-108">The derived class can reset the value in its constructor, or when the filter is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="425bb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="425bb-109">Syntax</span></span>


```C++
CRefTime m_rtStop;
```



## <a name="remarks"></a><span data-ttu-id="425bb-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="425bb-110">Remarks</span></span>

<span data-ttu-id="425bb-111">Halten Sie den kritischen Abschnitt **m \_ Plock** vor dem Zugriff auf diese Variable gedrückt.</span><span class="sxs-lookup"><span data-stu-id="425bb-111">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="425bb-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="425bb-112">Requirements</span></span>



| <span data-ttu-id="425bb-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="425bb-113">Requirement</span></span> | <span data-ttu-id="425bb-114">Wert</span><span class="sxs-lookup"><span data-stu-id="425bb-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="425bb-115">Header</span><span class="sxs-lookup"><span data-stu-id="425bb-115">Header</span></span><br/>  | <dl> <span data-ttu-id="425bb-116"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="425bb-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="425bb-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="425bb-117">Library</span></span><br/> | <dl> <span data-ttu-id="425bb-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="425bb-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="425bb-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="425bb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="425bb-120">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="425bb-120">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




