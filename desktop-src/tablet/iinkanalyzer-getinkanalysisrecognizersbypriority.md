---
description: Ruft eine geordnete Auflistung von iinkanalysiserkenzer-Objekten ab.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'Iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862687"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a><span data-ttu-id="d1ce5-103">Iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode</span><span class="sxs-lookup"><span data-stu-id="d1ce5-103">IInkAnalyzer::GetInkAnalysisRecognizersByPriority method</span></span>

<span data-ttu-id="d1ce5-104">Ruft eine geordnete Auflistung von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="d1ce5-104">Retrieves an ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1ce5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1ce5-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a><span data-ttu-id="d1ce5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1ce5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1ce5-107">*ppinkanalysiserkenzers* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d1ce5-107">*ppInkAnalysisRecognizers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1ce5-108">Eine geordnete Auflistung von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="d1ce5-108">An ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1ce5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1ce5-109">Return value</span></span>

<span data-ttu-id="d1ce5-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d1ce5-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d1ce5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1ce5-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="d1ce5-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppinkanalysiserkenzers* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="d1ce5-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppInkAnalysisRecognizers* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="d1ce5-113">Die Reihenfolge der erkenungen in dieser Auflistung gibt die Reihenfolge an, in der [**iinkanalyzer**](iinkanalyzer.md) die verfügbaren erkenungen auswertet.</span><span class="sxs-lookup"><span data-stu-id="d1ce5-113">The order of the recognizers in this collection indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available recognizers.</span></span> <span data-ttu-id="d1ce5-114">**Iinkanalyzer** verwendet die Sprache der Striche als primäres Kriterium für das Anwenden eines [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="d1ce5-114">The **IInkAnalyzer** uses the language of the strokes as its primary criterion for applying an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="d1ce5-115">Als sekundäres Kriterium vergleicht **iinkanalyzer** Analyse Hinweis Informationen mit den unterstützten Funktionen eines **iinkanalysiserkenzer** -Objekts (siehe [**iinkanalysiserkenzer:: getfunktionen**](iinkanalysisrecognizer-getcapabilities.md)).</span><span class="sxs-lookup"><span data-stu-id="d1ce5-115">As a secondary criterion, the **IInkAnalyzer** compares analysis hint information against an **IInkAnalysisRecognizer** object's supported capabilities (see [**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)).</span></span> <span data-ttu-id="d1ce5-116">Weitere Informationen zu Analyse hinweisen finden Sie unter [**iinkanalyzer:: erkreateanalysishint-Methode**](iinkanalyzer-createanalysishint.md).</span><span class="sxs-lookup"><span data-stu-id="d1ce5-116">For more information about analysis hints, see [**IInkAnalyzer::CreateAnalysisHint Method**](iinkanalyzer-createanalysishint.md).</span></span>

<span data-ttu-id="d1ce5-117">Wenn mehr als ein [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) einen sprach Bezeichner unterstützt, verwendet [**iinkanalyzer**](iinkanalyzer.md) einen "First-Fit"-Algorithmus, um den ersten **iinkanalysiserkenzer** auszuwählen, um Striche dieser Sprache zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="d1ce5-117">If more than one [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports a language identifier, the [**IInkAnalyzer**](iinkanalyzer.md) uses a "first-fit" algorithm to select the first **IInkAnalysisRecognizer** to analyze strokes of that language.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1ce5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1ce5-118">Requirements</span></span>



| <span data-ttu-id="d1ce5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1ce5-119">Requirement</span></span> | <span data-ttu-id="d1ce5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d1ce5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ce5-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1ce5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1ce5-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1ce5-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d1ce5-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1ce5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1ce5-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d1ce5-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d1ce5-125">Header</span><span class="sxs-lookup"><span data-stu-id="d1ce5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1ce5-126"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d1ce5-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d1ce5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d1ce5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1ce5-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1ce5-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d1ce5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1ce5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1ce5-130">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="d1ce5-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d1ce5-131">**Iinkanalysiserkenzers**</span><span class="sxs-lookup"><span data-stu-id="d1ce5-131">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="d1ce5-132">**Iinkanalyzer:: sethighestpriorityinkanalysiserkenzer-Methode**</span><span class="sxs-lookup"><span data-stu-id="d1ce5-132">**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer Method**</span></span>](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="d1ce5-133">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="d1ce5-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

