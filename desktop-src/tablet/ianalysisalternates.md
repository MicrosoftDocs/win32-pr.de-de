---
description: Enthält eine Auflistung von-Objekten, die die ianalysisalternate-Schnittstelle implementieren und die das Ergebnis der frei Hand Analyse sind.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Ianalysisalteraten-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4e43feaa40f519707531894936bf34ce19e57723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372839"
---
# <a name="ianalysisalternates-interface"></a><span data-ttu-id="d2cbf-103">Ianalysisalteraten-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d2cbf-103">IAnalysisAlternates interface</span></span>

<span data-ttu-id="d2cbf-104">Enthält eine Auflistung von-Objekten, die die [**ianalysisalternate**](ianalysisalternate.md) -Schnittstelle implementieren und die das Ergebnis der frei Hand Analyse sind.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-104">Contains a collection of objects that implement the [**IAnalysisAlternate**](ianalysisalternate.md) interface and that are the result of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="d2cbf-105">Member</span><span class="sxs-lookup"><span data-stu-id="d2cbf-105">Members</span></span>

<span data-ttu-id="d2cbf-106">Die **ianalysisalteraten** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-106">The **IAnalysisAlternates** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d2cbf-107">**Ianalysisalteraten** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d2cbf-107">**IAnalysisAlternates** also has these types of members:</span></span>

-   [<span data-ttu-id="d2cbf-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="d2cbf-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d2cbf-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="d2cbf-109">Methods</span></span>

<span data-ttu-id="d2cbf-110">Die **ianalysisalteraten** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-110">The **IAnalysisAlternates** interface has these methods.</span></span>



| <span data-ttu-id="d2cbf-111">Methode</span><span class="sxs-lookup"><span data-stu-id="d2cbf-111">Method</span></span>                                                                   | <span data-ttu-id="d2cbf-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2cbf-112">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2cbf-113">**Getanalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="d2cbf-113">**GetAnalysisAlternate**</span></span>](ianalysisalternates-getanalysisalternate.md) | <span data-ttu-id="d2cbf-114">Ruft das [**ianalysisalternate**](ianalysisalternate.md) -Objekt am angegebenen Index in der Collection ab.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-114">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span><br/>                   |
| [<span data-ttu-id="d2cbf-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="d2cbf-115">**GetCount**</span></span>](ianalysisalternates-getcount.md)                         | <span data-ttu-id="d2cbf-116">Ruft die Anzahl der [**ianalysisalternate**](ianalysisalternate.md) -Objekte ab, die in der **ianalysisalteraten** -Auflistung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-116">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the **IAnalysisAlternates** collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d2cbf-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2cbf-117">Remarks</span></span>

<span data-ttu-id="d2cbf-118">Diese Schnittstelle entspricht der [**System. Windows. Ink. AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) -Klasse in der .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-118">This interface is equivalent to the [**System.Windows.Ink.AnalysisCore.AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2cbf-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2cbf-119">Requirements</span></span>



| <span data-ttu-id="d2cbf-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2cbf-120">Requirement</span></span> | <span data-ttu-id="d2cbf-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d2cbf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2cbf-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2cbf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2cbf-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2cbf-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d2cbf-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2cbf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2cbf-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d2cbf-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d2cbf-126">Header</span><span class="sxs-lookup"><span data-stu-id="d2cbf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2cbf-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d2cbf-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d2cbf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d2cbf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2cbf-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2cbf-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d2cbf-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2cbf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2cbf-131">**Ianalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="d2cbf-131">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="d2cbf-132">**Iinkanalyzer:: getalteraten-Methode**</span><span class="sxs-lookup"><span data-stu-id="d2cbf-132">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="d2cbf-133">**Iinkanalyzer:: getalternatesforcontextnodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="d2cbf-133">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="d2cbf-134">**Iinkanalyzer:: getalternatesforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="d2cbf-134">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="d2cbf-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="d2cbf-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

