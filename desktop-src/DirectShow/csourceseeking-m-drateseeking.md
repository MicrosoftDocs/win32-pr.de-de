---
description: Wiedergabe Rate. Standardmäßig ist der Wert auf 1,0 festgelegt.
ms.assetid: 835ddbe8-2017-4a4a-8f10-b3f33a8215a7
title: 'Csourceseeking:: m_dRateSeeking Member (ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dRateSeeking
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1055a420316868db6374798c0295339dd74ac172
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368598"
---
# <a name="csourceseekingm_drateseeking-member"></a><span data-ttu-id="6fe29-104">Csourceseeking:: m \_ drateseeking-Member</span><span class="sxs-lookup"><span data-stu-id="6fe29-104">CSourceSeeking::m\_dRateSeeking member</span></span>

<span data-ttu-id="6fe29-105">Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="6fe29-105">Playback rate.</span></span> <span data-ttu-id="6fe29-106">Standardmäßig ist der Wert auf 1,0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6fe29-106">By default, the value is set to 1.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe29-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fe29-107">Syntax</span></span>


```C++
double m_dRateSeeking;
```



## <a name="remarks"></a><span data-ttu-id="6fe29-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fe29-108">Remarks</span></span>

<span data-ttu-id="6fe29-109">Halten Sie den kritischen Abschnitt **m \_ Plock** vor dem Zugriff auf diese Variable gedrückt.</span><span class="sxs-lookup"><span data-stu-id="6fe29-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe29-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fe29-110">Requirements</span></span>



| <span data-ttu-id="6fe29-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fe29-111">Requirement</span></span> | <span data-ttu-id="6fe29-112">Wert</span><span class="sxs-lookup"><span data-stu-id="6fe29-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe29-113">Header</span><span class="sxs-lookup"><span data-stu-id="6fe29-113">Header</span></span><br/>  | <dl> <span data-ttu-id="6fe29-114"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fe29-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6fe29-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6fe29-115">Library</span></span><br/> | <dl> <span data-ttu-id="6fe29-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6fe29-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fe29-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fe29-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe29-118">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6fe29-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




