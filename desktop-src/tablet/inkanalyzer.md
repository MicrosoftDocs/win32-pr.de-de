---
description: Implementiert die iinkanalyzer-Schnittstelle.
ms.assetid: f17de375-a0fe-4024-bf2a-60f8de8b0345
title: InkAnalyzer-Klasse (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalyzer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 49eeb04b1568bbef785f7d750315e0ea39491d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344879"
---
# <a name="inkanalyzer-class"></a><span data-ttu-id="d5fa7-103">InkAnalyzer-Klasse</span><span class="sxs-lookup"><span data-stu-id="d5fa7-103">InkAnalyzer class</span></span>

<span data-ttu-id="d5fa7-104">Implementiert die [**iinkanalyzer**](iinkanalyzer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d5fa7-104">Implements the [**IInkAnalyzer**](iinkanalyzer.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5fa7-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5fa7-105">Remarks</span></span>

<span data-ttu-id="d5fa7-106">Diese Klasse implementiert die [**iinkanalyzer**](iinkanalyzer.md) -com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d5fa7-106">This class implements the [**IInkAnalyzer**](iinkanalyzer.md) COM interface.</span></span>

<span data-ttu-id="d5fa7-107">[ \_ Ianalysitsvents](-ianalysisevents.md) ist die Standard Quelle für Ereignisse und stellt Standard Ereignisse für [**iinkanalyzer**](iinkanalyzer.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="d5fa7-107">[\_IAnalysisEvents](-ianalysisevents.md) is the default source of events and provides standard events for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="d5fa7-108">[**\_ Ianalysisproxyevents**](-ianalysisproxyevents.md) stellt die Daten Proxy Ereignisse für [**iinkanalyzer**](iinkanalyzer.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="d5fa7-108">[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md) provides the data proxy events for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="d5fa7-109">Weitere Informationen finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d5fa7-109">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5fa7-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5fa7-110">Requirements</span></span>



| <span data-ttu-id="d5fa7-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5fa7-111">Requirement</span></span> | <span data-ttu-id="d5fa7-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d5fa7-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5fa7-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5fa7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d5fa7-114">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5fa7-114">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d5fa7-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5fa7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d5fa7-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d5fa7-116">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d5fa7-117">Header</span><span class="sxs-lookup"><span data-stu-id="d5fa7-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5fa7-118"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d5fa7-118"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d5fa7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d5fa7-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5fa7-120"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5fa7-120"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d5fa7-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5fa7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5fa7-122">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="d5fa7-122">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="d5fa7-123">**Ianalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="d5fa7-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="d5fa7-124">**Ianalysisstatus**</span><span class="sxs-lookup"><span data-stu-id="d5fa7-124">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="d5fa7-125">**Icontextlink**</span><span class="sxs-lookup"><span data-stu-id="d5fa7-125">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="d5fa7-126">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="d5fa7-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d5fa7-127">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="d5fa7-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




