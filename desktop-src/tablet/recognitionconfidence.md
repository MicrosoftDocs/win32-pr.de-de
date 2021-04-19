---
description: Gibt die Vertrauens Ebene an, die der iinkanalyzer in der Genauigkeit des Erkennungs Ergebnisses hat.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Erkentionconfidence-Enumeration (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351559"
---
# <a name="recognitionconfidence-enumeration"></a><span data-ttu-id="ca66b-103">Erkentionconfidence-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ca66b-103">RecognitionConfidence enumeration</span></span>

<span data-ttu-id="ca66b-104">Gibt die Vertrauens Ebene an, die der [**iinkanalyzer**](iinkanalyzer.md) in der Genauigkeit des Erkennungs Ergebnisses hat.</span><span class="sxs-lookup"><span data-stu-id="ca66b-104">Indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the recognition result.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca66b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca66b-105">Syntax</span></span>


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a><span data-ttu-id="ca66b-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ca66b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ca66b-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**Erkentionconfidence \_ Strong**</span><span class="sxs-lookup"><span data-stu-id="ca66b-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence\_Strong**</span></span>
</dt> <dd>

<span data-ttu-id="ca66b-108">Sicheres Vertrauen im Ergebnis oder bei Alternativen.</span><span class="sxs-lookup"><span data-stu-id="ca66b-108">Strong confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="ca66b-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**Erkennungs Konfidenz \_ zwischen**</span><span class="sxs-lookup"><span data-stu-id="ca66b-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence\_Intermediate**</span></span>
</dt> <dd>

<span data-ttu-id="ca66b-110">Zwischen Vertrauen im Ergebnis oder Alternativen.</span><span class="sxs-lookup"><span data-stu-id="ca66b-110">Intermediate confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="ca66b-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**Erkennunkonfidenz \_ Mangel**</span><span class="sxs-lookup"><span data-stu-id="ca66b-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence\_Poor**</span></span>
</dt> <dd>

<span data-ttu-id="ca66b-112">Mangelhafte Zuverlässigkeit im Ergebnis oder Alternativen.</span><span class="sxs-lookup"><span data-stu-id="ca66b-112">Poor confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="ca66b-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**\_Erkennunbekanntem Erkennungs Vertrauen**</span><span class="sxs-lookup"><span data-stu-id="ca66b-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="ca66b-114">Das [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Element, das den erkannten Text generiert hat, unterstützt keine Vertrauens Ebenen.</span><span class="sxs-lookup"><span data-stu-id="ca66b-114">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that generated the recognized text does not support confidence levels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca66b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca66b-115">Remarks</span></span>

<span data-ttu-id="ca66b-116">[**Iinkanalyzer**](iinkanalyzer.md) verwendet mindestens ein [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekt, um Handschrift in Text zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="ca66b-116">The [**IInkAnalyzer**](iinkanalyzer.md) uses one or more [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects to convert handwriting to text.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca66b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca66b-117">Requirements</span></span>



| <span data-ttu-id="ca66b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca66b-118">Requirement</span></span> | <span data-ttu-id="ca66b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ca66b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca66b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca66b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ca66b-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca66b-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ca66b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca66b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ca66b-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ca66b-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ca66b-124">Header</span><span class="sxs-lookup"><span data-stu-id="ca66b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca66b-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ca66b-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca66b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca66b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca66b-127">**Ianalysisalternate:: getrecognitionconfidence-Methode**</span><span class="sxs-lookup"><span data-stu-id="ca66b-127">**IAnalysisAlternate::GetRecognitionConfidence Method**</span></span>](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="ca66b-128">**Icontextnode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ca66b-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="ca66b-129">Kontext Knoten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca66b-129">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="ca66b-130">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="ca66b-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




