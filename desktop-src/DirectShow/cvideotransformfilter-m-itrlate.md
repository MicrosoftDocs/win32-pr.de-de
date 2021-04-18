---
description: Gibt an, wie spät die Stichproben am Renderer in Bezugszeit Einheiten eintreffen. Syntax.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Cvideotransformfilter:: m_itrLate Member (vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365526"
---
# <a name="cvideotransformfilterm_itrlate-member"></a><span data-ttu-id="a73c2-104">Cvideotransformfilter:: m \_ itrlate-Element</span><span class="sxs-lookup"><span data-stu-id="a73c2-104">CVideoTransformFilter::m\_itrLate member</span></span>

<span data-ttu-id="a73c2-105">Gibt an, wie spät die Stichproben am Renderer in Bezugszeit Einheiten eintreffen.</span><span class="sxs-lookup"><span data-stu-id="a73c2-105">Indicates how late the samples are arriving at the renderer, in reference time units.</span></span> <span data-ttu-id="a73c2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a73c2-106">Syntax</span></span>

## <a name="syntax"></a><span data-ttu-id="a73c2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a73c2-107">Syntax</span></span>


```C++
int m_itrLate;
```



## <a name="remarks"></a><span data-ttu-id="a73c2-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a73c2-108">Remarks</span></span>

<span data-ttu-id="a73c2-109">Wenn der Filter eine Qualitäts Nachricht von Downstream empfängt, speichert er den oder bei Verzögerung-Wert in dieser Variablen.</span><span class="sxs-lookup"><span data-stu-id="a73c2-109">When the filter receives a quality message from downstream, it stores the lateness value in this variable.</span></span> <span data-ttu-id="a73c2-110">Beim Löschen des Filters wird dieser Wert aktualisiert, indem die Dauer der einzelnen Frames subtrahieren.</span><span class="sxs-lookup"><span data-stu-id="a73c2-110">As the filter drops frames, it updates this value by subtracting the duration of each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73c2-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a73c2-111">Requirements</span></span>



| <span data-ttu-id="a73c2-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a73c2-112">Requirement</span></span> | <span data-ttu-id="a73c2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a73c2-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a73c2-114">Header</span><span class="sxs-lookup"><span data-stu-id="a73c2-114">Header</span></span><br/>  | <dl> <span data-ttu-id="a73c2-115"><dt>Vtrans. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a73c2-115"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a73c2-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a73c2-116">Library</span></span><br/> | <dl> <span data-ttu-id="a73c2-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a73c2-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a73c2-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a73c2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73c2-119">**Cvideotransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a73c2-119">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




