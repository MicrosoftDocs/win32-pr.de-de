---
description: Steht für die möglichen Handschrift Erkennungs Wort Übereinstimmungen für icontextnode-Objekte.
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: Ianalysisalternate-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214683"
---
# <a name="ianalysisalternate-interface"></a><span data-ttu-id="f628d-103">Ianalysisalternate-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f628d-103">IAnalysisAlternate interface</span></span>

<span data-ttu-id="f628d-104">Steht für die möglichen Handschrift Erkennungs Wort Übereinstimmungen für [**icontextnode**](icontextnode.md) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="f628d-104">Represents the possible handwriting recognition word matches for [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="f628d-105">Member</span><span class="sxs-lookup"><span data-stu-id="f628d-105">Members</span></span>

<span data-ttu-id="f628d-106">Die **ianalysisalternate** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f628d-106">The **IAnalysisAlternate** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f628d-107">**Ianalysisalternate** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f628d-107">**IAnalysisAlternate** also has these types of members:</span></span>

-   [<span data-ttu-id="f628d-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="f628d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f628d-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="f628d-109">Methods</span></span>

<span data-ttu-id="f628d-110">Die **ianalysisalternate** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f628d-110">The **IAnalysisAlternate** interface has these methods.</span></span>



| <span data-ttu-id="f628d-111">Methode</span><span class="sxs-lookup"><span data-stu-id="f628d-111">Method</span></span>                                                                          | <span data-ttu-id="f628d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f628d-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f628d-113">**Getalternatenodes**</span><span class="sxs-lookup"><span data-stu-id="f628d-113">**GetAlternateNodes**</span></span>](ianalysisalternate-getalternatenodes.md)               | <span data-ttu-id="f628d-114">Ruft die [**icontextnode**](icontextnode.md) -Objekte ab, die mit dieser alternativen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="f628d-114">Retrieves the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span><br/>                                                       |
| [<span data-ttu-id="f628d-115">**Getrecognitionconfidence**</span><span class="sxs-lookup"><span data-stu-id="f628d-115">**GetRecognitionConfidence**</span></span>](ianalysisalternate-getrecognitionconfidence.md) | <span data-ttu-id="f628d-116">Ruft einen Wert ab, der die Vertrauens Ebene angibt, die der [**iinkanalyzer**](iinkanalyzer.md) in der Genauigkeit von **ianalysisalternate** hat.</span><span class="sxs-lookup"><span data-stu-id="f628d-116">Retrieves a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the **IAnalysisAlternate**.</span></span><br/> |
| [<span data-ttu-id="f628d-117">**GetRecognizedString**</span><span class="sxs-lookup"><span data-stu-id="f628d-117">**GetRecognizedString**</span></span>](ianalysisalternate-getrecognizedstring.md)           | <span data-ttu-id="f628d-118">Ruft den erkannten Zeichen folgen Wert des **ianalysisalternate** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="f628d-118">Retrieves the recognized string value of the **IAnalysisAlternate** object.</span></span><br/>                                                                               |
| [<span data-ttu-id="f628d-119">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="f628d-119">**GetStrokeIds**</span></span>](ianalysisalternate-getstrokeids.md)                         | <span data-ttu-id="f628d-120">Ruft die Strich Bezeichner ab, die diesem **ianalysisalternate**-Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f628d-120">Retrieves the stroke identifiers that are associated with this **IAnalysisAlternate**.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="f628d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f628d-121">Remarks</span></span>

<span data-ttu-id="f628d-122">Es gibt viele Variationen der Benutzer Handschrift.</span><span class="sxs-lookup"><span data-stu-id="f628d-122">There are many variations in users' handwriting.</span></span> <span data-ttu-id="f628d-123">Aus diesem Grund kann die Handschrifterkennung manchmal in Text konvertieren, der sich von dem beabsichtigten Benutzer unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="f628d-123">For that reason, handwriting recognizers can sometimes convert handwriting into text that is different from what the user intended.</span></span> <span data-ttu-id="f628d-124">Wenn ein [**iinkanalyzer**](iinkanalyzer.md) eine Analyse für eine Auflistung von Strichen durchführt, sucht **iinkanalyzer** nach dem wahrscheinlichsten Satz von Wörtern, den die Handschrift darstellt.</span><span class="sxs-lookup"><span data-stu-id="f628d-124">When an [**IInkAnalyzer**](iinkanalyzer.md) performs analysis on a collection of strokes, the **IInkAnalyzer** finds the most likely set of words that the handwriting represents.</span></span> <span data-ttu-id="f628d-125">Außerdem findet der **iinkanalyzer** auch Sätze alternativer Erkennungs Übereinstimmungen, die in einer [**ianalysisalterors**](ianalysisalternates.md) -Auflistung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f628d-125">In addition, the **IInkAnalyzer** also finds sets of alternative recognition matches, which are stored in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span> <span data-ttu-id="f628d-126">Damit ein Benutzer Erkennungs Alternativen nutzen kann, müssen Sie eine Benutzeroberfläche erstellen, die es dem Benutzer ermöglicht, die richtige **ianalysisalternate** auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f628d-126">In order for a user to take advantage of recognition alternates, you must create a user interface that allows the user to select the correct **IAnalysisAlternate**.</span></span>

<span data-ttu-id="f628d-127">**Ianalysisalternate** -Objekte werden in der Regel durch die [**iinkanalyzer:: getalteraten-Methode**](iinkanalyzer-getalternates.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f628d-127">**IAnalysisAlternate** objects are generally obtained through [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md).</span></span> <span data-ttu-id="f628d-128">Das erste **ianalysisalternate** -Objekt in der Auflistung ist das, was [**iinkanalyzer**](iinkanalyzer.md) als wahrscheinlichste Alternative ansieht.</span><span class="sxs-lookup"><span data-stu-id="f628d-128">The first **IAnalysisAlternate** object in the collection is what the [**IInkAnalyzer**](iinkanalyzer.md) considers to be the most likely alternate.</span></span>

<span data-ttu-id="f628d-129">Diese Schnittstelle entspricht [System. Windows. Ink. AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) im .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f628d-129">This interface is equivalent to [System.Windows.Ink.AnalysisCore.AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="f628d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f628d-130">Requirements</span></span>



| <span data-ttu-id="f628d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f628d-131">Requirement</span></span> | <span data-ttu-id="f628d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f628d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f628d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f628d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f628d-134">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f628d-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f628d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f628d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f628d-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f628d-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f628d-137">Header</span><span class="sxs-lookup"><span data-stu-id="f628d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f628d-138"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f628d-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f628d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f628d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f628d-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f628d-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f628d-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f628d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f628d-142">**Ianalysisalteraten**</span><span class="sxs-lookup"><span data-stu-id="f628d-142">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="f628d-143">**Iinkanalyzer:: getalternatesforcontextnodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="f628d-143">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="f628d-144">**Iinkanalyzer:: getalternatesforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="f628d-144">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="f628d-145">**Iinkanalyzer:: getalteraten-Methode**</span><span class="sxs-lookup"><span data-stu-id="f628d-145">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="f628d-146">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="f628d-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

