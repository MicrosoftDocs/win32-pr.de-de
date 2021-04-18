---
description: Startzeit. In der Standardeinstellung ist dieser Wert auf 0 festgelegt.
ms.assetid: bafa69c3-ead0-4409-abbf-4e8cc325e5f9
title: 'Csourceseeking:: m_rtStart Member (ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStart
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc7bf18f23177095328c1faee8dd8da28e830b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371642"
---
# <a name="csourceseekingm_rtstart-member"></a><span data-ttu-id="b1cac-104">Csourceseeking:: m \_ rtstart-Member</span><span class="sxs-lookup"><span data-stu-id="b1cac-104">CSourceSeeking::m\_rtStart member</span></span>

<span data-ttu-id="b1cac-105">Startzeit.</span><span class="sxs-lookup"><span data-stu-id="b1cac-105">Start time.</span></span> <span data-ttu-id="b1cac-106">In der Standardeinstellung ist dieser Wert auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1cac-106">By default, the value is set to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1cac-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1cac-107">Syntax</span></span>


```C++
CRefTime m_rtStart;
```



## <a name="remarks"></a><span data-ttu-id="b1cac-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1cac-108">Remarks</span></span>

<span data-ttu-id="b1cac-109">Halten Sie den kritischen Abschnitt **m \_ Plock** vor dem Zugriff auf diese Variable gedrückt.</span><span class="sxs-lookup"><span data-stu-id="b1cac-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1cac-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1cac-110">Requirements</span></span>



| <span data-ttu-id="b1cac-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1cac-111">Requirement</span></span> | <span data-ttu-id="b1cac-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b1cac-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1cac-113">Header</span><span class="sxs-lookup"><span data-stu-id="b1cac-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b1cac-114"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1cac-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b1cac-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b1cac-115">Library</span></span><br/> | <dl> <span data-ttu-id="b1cac-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b1cac-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1cac-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1cac-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1cac-118">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b1cac-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




