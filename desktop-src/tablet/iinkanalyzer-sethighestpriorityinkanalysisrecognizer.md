---
description: Verschiebt den angegebenen iinkanalysiserkenzer an die erste Position in der Liste der frei Hand erkenungen des iinkanalyzer-Objekts.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'Iinkanalyzer:: sethighestpriorityinkanalysiserkenzer-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862683"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a><span data-ttu-id="152fc-103">Iinkanalyzer:: sethighestpriorityinkanalysiserkenzer-Methode</span><span class="sxs-lookup"><span data-stu-id="152fc-103">IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer method</span></span>

<span data-ttu-id="152fc-104">Verschiebt den angegebenen [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) an die erste Position in der Liste der frei Hand erkenungen des [**iinkanalyzer**](iinkanalyzer.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="152fc-104">Moves the specified [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to the first position in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

## <a name="syntax"></a><span data-ttu-id="152fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="152fc-105">Syntax</span></span>


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="152fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="152fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="152fc-107">*pinkanalysiserkenzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="152fc-107">*pInkAnalysisRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="152fc-108">Der [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) , der an der ersten Position platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="152fc-108">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to place in the first position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="152fc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="152fc-109">Return value</span></span>

<span data-ttu-id="152fc-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="152fc-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="152fc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="152fc-111">Remarks</span></span>

<span data-ttu-id="152fc-112">Um die Liste der frei Hand erkenungen in der Reihenfolge der Priorität abzurufen, wenden Sie sich an die [**iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span><span class="sxs-lookup"><span data-stu-id="152fc-112">To get the list of ink recognizers in priority order, call [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span></span>

<span data-ttu-id="152fc-113">Diese Methode wirkt sich nicht auf die Reihenfolge der restlichen [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekte in der Liste der frei Hand erkenungen des [**iinkanalyzer**](iinkanalyzer.md) -Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="152fc-113">This method does not affect the order of the rest of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

<span data-ttu-id="152fc-114">Die Reihenfolge der von der [**iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) zurückgegebenen Handschrift erkenungen gibt die Reihenfolge an, in der [**iinkanalyzer**](iinkanalyzer.md) die verfügbaren [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekte auswertet.</span><span class="sxs-lookup"><span data-stu-id="152fc-114">The order of the ink recognizers returned by [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

<span data-ttu-id="152fc-115">Die Verwendung der frei Hand erkenungen wird basierend auf ihrer Reihenfolge in der Liste ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="152fc-115">Use of the ink recognizers is evaluated based on their order in the list.</span></span>

<span data-ttu-id="152fc-116">Während der Handschrift Analyse durchläuft [**iinkanalyzer**](iinkanalyzer.md) die frei Hand erkenungen in der Liste, bis eine Erkennung gefunden wird, die die Sprache und andere Eigenschaften der Striche unterstützt.</span><span class="sxs-lookup"><span data-stu-id="152fc-116">During ink analysis, the [**IInkAnalyzer**](iinkanalyzer.md) iterates through the ink recognizers in its list until it finds a recognizer that supports the language and other properties of the strokes.</span></span> <span data-ttu-id="152fc-117">Diese Erkennung wird zur frei Handerkennung für diese Striche verwendet.</span><span class="sxs-lookup"><span data-stu-id="152fc-117">This recognizer is used for ink recognition for those strokes.</span></span>

<span data-ttu-id="152fc-118">Wenn [**iinkanalyzer**](iinkanalyzer.md) keinen [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) findet, der einen Satz von Strichen während der Analyse unterstützt, generiert **iinkanalyzer** eine [**ianalysiswarning**](ianalysiswarning.md) mit dem Warnungs Code **AnalysisWarningCode \_ inkanalysiserkenzernotinstallierte** (siehe [**ianalysiswarning:: getwarningcode**](ianalysiswarning-getwarningcode.md)).</span><span class="sxs-lookup"><span data-stu-id="152fc-118">If the [**IInkAnalyzer**](iinkanalyzer.md) does not find an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that supports a set of strokes during analysis, the **IInkAnalyzer** generates an [**IAnalysisWarning**](ianalysiswarning.md) with a warning code of **AnalysisWarningCode\_InkAnalysisRecognizerNotInstalled** (see [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="152fc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="152fc-119">Requirements</span></span>



| <span data-ttu-id="152fc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="152fc-120">Requirement</span></span> | <span data-ttu-id="152fc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="152fc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="152fc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="152fc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="152fc-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="152fc-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="152fc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="152fc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="152fc-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="152fc-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="152fc-126">Header</span><span class="sxs-lookup"><span data-stu-id="152fc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="152fc-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="152fc-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="152fc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="152fc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="152fc-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="152fc-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="152fc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="152fc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152fc-131">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="152fc-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="152fc-132">**Iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode**</span><span class="sxs-lookup"><span data-stu-id="152fc-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="152fc-133">**Iinkanalysiserkenzers**</span><span class="sxs-lookup"><span data-stu-id="152fc-133">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="152fc-134">**Ianalysiswarning**</span><span class="sxs-lookup"><span data-stu-id="152fc-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="152fc-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="152fc-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




