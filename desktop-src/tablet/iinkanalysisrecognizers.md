---
description: Enthält eine Auflistung von-Objekten, die die iinkanalysiserkenzer-Schnittstelle implementieren und die die Fähigkeit zum Erkennen von Handschrift, Objekten oder Gesten darstellen.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Iinkanalysiserkenzers-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343718"
---
# <a name="iinkanalysisrecognizers-interface"></a><span data-ttu-id="567c4-103">Iinkanalysiserkenzers-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="567c4-103">IInkAnalysisRecognizers interface</span></span>

<span data-ttu-id="567c4-104">Enthält eine Auflistung von-Objekten, die die [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Schnittstelle implementieren und die die Fähigkeit zum Erkennen von Handschrift, Objekten oder Gesten darstellen.</span><span class="sxs-lookup"><span data-stu-id="567c4-104">Contains a collection of objects that implement the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) interface and that represent the ability to recognize handwriting, objects, or gestures.</span></span>

## <a name="members"></a><span data-ttu-id="567c4-105">Member</span><span class="sxs-lookup"><span data-stu-id="567c4-105">Members</span></span>

<span data-ttu-id="567c4-106">Die **iinkanalysiserkenzers** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="567c4-106">The **IInkAnalysisRecognizers** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="567c4-107">**Iinkanalysiserkenzers** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="567c4-107">**IInkAnalysisRecognizers** also has these types of members:</span></span>

-   [<span data-ttu-id="567c4-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="567c4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="567c4-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="567c4-109">Methods</span></span>

<span data-ttu-id="567c4-110">Die **iinkanalysiserkenzers** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="567c4-110">The **IInkAnalysisRecognizers** interface has these methods.</span></span>



| <span data-ttu-id="567c4-111">Methode</span><span class="sxs-lookup"><span data-stu-id="567c4-111">Method</span></span>                                                                               | <span data-ttu-id="567c4-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="567c4-112">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="567c4-113">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="567c4-113">**GetCount**</span></span>](iinkanalysisrecognizers-getcount.md)                                 | <span data-ttu-id="567c4-114">Ruft die Anzahl der [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekte in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="567c4-114">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span><br/> |
| [<span data-ttu-id="567c4-115">**Getinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="567c4-115">**GetInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | <span data-ttu-id="567c4-116">Ruft das [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Element am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="567c4-116">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="567c4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="567c4-117">Remarks</span></span>

<span data-ttu-id="567c4-118">Die [**iinkanalyzer:: getinkanalysiserkenzersbypriority-Methoden**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) Methode von [**iinkanalyzer**](iinkanalyzer.md) gibt eine **iinkanalysiserkenzers** -Sammlung zurück, die die auf dem aktuellen Tablet PC verfügbaren frei Hand erkenungen enthält.</span><span class="sxs-lookup"><span data-stu-id="567c4-118">The [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method of [**IInkAnalyzer**](iinkanalyzer.md) returns an **IInkAnalysisRecognizers** collection containing the ink recognizers available on the current Tablet PC.</span></span>

<span data-ttu-id="567c4-119">Bei einer Spracherkennung gibt die [**iinkanalysiserkenzer:: GetLanguages**](iinkanalysisrecognizer-getlanguages.md) -Methode ein nicht leeres Array zurück.</span><span class="sxs-lookup"><span data-stu-id="567c4-119">For a language recognizer, the [**IInkAnalysisRecognizer::GetLanguages**](iinkanalysisrecognizer-getlanguages.md) method returns a non-empty array.</span></span> <span data-ttu-id="567c4-120">Bei Gesten Erkennungs Programmen und Objekt erkenzern gibt die **iinkanalysiserkenzer:: GetLanguages** -Methode ein leeres Array zurück.</span><span class="sxs-lookup"><span data-stu-id="567c4-120">For both gesture recognizers and object recognizers, the **IInkAnalysisRecognizer::GetLanguages** method returns an empty array.</span></span>

## <a name="requirements"></a><span data-ttu-id="567c4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="567c4-121">Requirements</span></span>



| <span data-ttu-id="567c4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="567c4-122">Requirement</span></span> | <span data-ttu-id="567c4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="567c4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="567c4-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="567c4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="567c4-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="567c4-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="567c4-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="567c4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="567c4-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="567c4-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="567c4-128">Header</span><span class="sxs-lookup"><span data-stu-id="567c4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="567c4-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="567c4-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="567c4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="567c4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="567c4-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="567c4-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="567c4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="567c4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="567c4-133">**Iinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="567c4-133">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="567c4-134">**Iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode**</span><span class="sxs-lookup"><span data-stu-id="567c4-134">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="567c4-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="567c4-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

