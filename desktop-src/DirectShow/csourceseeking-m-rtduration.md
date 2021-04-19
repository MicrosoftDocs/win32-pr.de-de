---
description: 'Dauer des Streams. Standardmäßig wird der Wert auf den Wert der csourceseeking:: m rtstoppt-Element Variablen festgelegt \_ .'
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'Csourceseeking:: m_rtDuration Member (ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361982"
---
# <a name="csourceseekingm_rtduration-member"></a><span data-ttu-id="d0c33-104">Csourceseeking:: m \_ rtduration-Member</span><span class="sxs-lookup"><span data-stu-id="d0c33-104">CSourceSeeking::m\_rtDuration member</span></span>

<span data-ttu-id="d0c33-105">Dauer des Streams.</span><span class="sxs-lookup"><span data-stu-id="d0c33-105">Duration of the stream.</span></span> <span data-ttu-id="d0c33-106">Standardmäßig wird der Wert auf den Wert der [**csourceseeking:: m \_ rtstoppt**](csourceseeking-m-rtstop.md) -Element Variablen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d0c33-106">By default, the value is set to the value of the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c33-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0c33-107">Syntax</span></span>


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a><span data-ttu-id="d0c33-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0c33-108">Remarks</span></span>

<span data-ttu-id="d0c33-109">Halten Sie den kritischen Abschnitt **m \_ Plock** vor dem Zugriff auf diese Variable gedrückt.</span><span class="sxs-lookup"><span data-stu-id="d0c33-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c33-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0c33-110">Requirements</span></span>



| <span data-ttu-id="d0c33-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0c33-111">Requirement</span></span> | <span data-ttu-id="d0c33-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d0c33-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c33-113">Header</span><span class="sxs-lookup"><span data-stu-id="d0c33-113">Header</span></span><br/>  | <dl> <span data-ttu-id="d0c33-114"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0c33-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0c33-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d0c33-115">Library</span></span><br/> | <dl> <span data-ttu-id="d0c33-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d0c33-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c33-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0c33-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c33-118">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d0c33-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




