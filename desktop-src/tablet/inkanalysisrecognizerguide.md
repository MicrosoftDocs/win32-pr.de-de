---
description: Gibt das Handbuch oder den Bereich an, in dem frei Hand Eingaben gezeichnet und erkannt werden.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: Inkanalysiserkenzerguide-Struktur (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356742"
---
# <a name="inkanalysisrecognizerguide-structure"></a><span data-ttu-id="2a97c-103">Inkanalysiserkenzerguide-Struktur</span><span class="sxs-lookup"><span data-stu-id="2a97c-103">InkAnalysisRecognizerGuide structure</span></span>

<span data-ttu-id="2a97c-104">Gibt das Handbuch oder den Bereich an, in dem frei Hand Eingaben gezeichnet und erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="2a97c-104">Specifies the guide, or area where ink is drawn and recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a97c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a97c-105">Syntax</span></span>


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a><span data-ttu-id="2a97c-106">Member</span><span class="sxs-lookup"><span data-stu-id="2a97c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2a97c-107">**rectbeschreitingbox**</span><span class="sxs-lookup"><span data-stu-id="2a97c-107">**rectWritingBox**</span></span>
</dt> <dd>

<span data-ttu-id="2a97c-108">Der unsichtbare Schreibbereich des Erkennungs Handbuchs, in dem geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a97c-108">The invisible writing area of the recognition guide in which writing can actually take place.</span></span>

</dd> <dt>

<span data-ttu-id="2a97c-109">**rectdrawnbox**</span><span class="sxs-lookup"><span data-stu-id="2a97c-109">**rectDrawnBox**</span></span>
</dt> <dd>

<span data-ttu-id="2a97c-110">Das Rechteck, das auf dem Tablet-Bildschirm gezeichnet wird und in dem geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="2a97c-110">The rectangle that is drawn on the tablet screen and in which writing takes place.</span></span>

</dd> <dt>

<span data-ttu-id="2a97c-111">**Crows**</span><span class="sxs-lookup"><span data-stu-id="2a97c-111">**cRows**</span></span>
</dt> <dd>

<span data-ttu-id="2a97c-112">Die Anzahl der Zeilen im Feld Erkennungs Handbuch.</span><span class="sxs-lookup"><span data-stu-id="2a97c-112">The number of rows in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="2a97c-113">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="2a97c-113">**cColumns**</span></span>
</dt> <dd>

<span data-ttu-id="2a97c-114">Die Anzahl der Spalten im Feld Erkennungs Handbuch.</span><span class="sxs-lookup"><span data-stu-id="2a97c-114">The number of columns in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="2a97c-115">**vervollständigen**</span><span class="sxs-lookup"><span data-stu-id="2a97c-115">**midline**</span></span>
</dt> <dd>

<span data-ttu-id="2a97c-116">Die Höhe des Feld Erkennungs Handbuchs in der Mitte.</span><span class="sxs-lookup"><span data-stu-id="2a97c-116">The midline height of the recognition guide box.</span></span> <span data-ttu-id="2a97c-117">Die mittlere Höhe ist der Abstand zwischen der Baseline und der Mitte des gezeichneten Felds.</span><span class="sxs-lookup"><span data-stu-id="2a97c-117">The midline height is the distance from the baseline to the midline, of the drawn box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a97c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a97c-118">Remarks</span></span>

<span data-ttu-id="2a97c-119">Ein **inkanalysiserkenzerguide** definiert einen erwarteten Bereich von Eingaben, z. b. eine Linie oder Felder für Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2a97c-119">An **InkAnalysisRecognizerGuide** defines an expected area of input, such as a line or boxes, for characters.</span></span> <span data-ttu-id="2a97c-120">Eine **inkanalysiserkenzerguide** -Struktur kann nur auf einem Kontext Knoten des Analyse Hinweises festgelegt werden (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="2a97c-120">An **InkAnalysisRecognizerGuide** structure can be set only on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="2a97c-121">Der [**iinkanalyzer**](iinkanalyzer.md) verwendet den Speicherort des Knoten "Analyse Hinweis" und die Speicherorte der frei Hand Striche, um dem Knoten "Analyse Hinweis" einen Strich zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2a97c-121">The [**IInkAnalyzer**](iinkanalyzer.md) uses the location of the analysis hint node and the locations of the ink strokes to associate a stroke with the analysis hint node.</span></span> <span data-ttu-id="2a97c-122">Bei allen Strichen mit einer Zuordnung zum Knoten des Analyse Hinweises wird das angegebene **inkanalysiserkenzerguide** verwendet, wenn es von einem **iinkanalyzer** erkannt wird, vorausgesetzt, der **iinkanalyzer** unterstützt das **inkanalysiserkenzerguide**.</span><span class="sxs-lookup"><span data-stu-id="2a97c-122">Any strokes with an association to the analysis hint node will have the specified **InkAnalysisRecognizerGuide** used when recognized by an **IInkAnalyzer**, provided the **IInkAnalyzer** supports the **InkAnalysisRecognizerGuide**.</span></span> <span data-ttu-id="2a97c-123">Die Werte, die in der **inkanalysiserkenzerguide** -Klasse ausgedrückt werden, sind immer relativ zum Speicherort des Analysis Hint-Knotens und werden in Freihand Raumkoordinaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="2a97c-123">The values expressed in the **InkAnalysisRecognizerGuide** class are always relative to the location of the analysis hint node and are specified in ink space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a97c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a97c-124">Requirements</span></span>



| <span data-ttu-id="2a97c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a97c-125">Requirement</span></span> | <span data-ttu-id="2a97c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2a97c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a97c-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a97c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2a97c-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a97c-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2a97c-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a97c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2a97c-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2a97c-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2a97c-131">Header</span><span class="sxs-lookup"><span data-stu-id="2a97c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a97c-132"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2a97c-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a97c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a97c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a97c-134">Eigenschaften des Analyse Hinweises</span><span class="sxs-lookup"><span data-stu-id="2a97c-134">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="2a97c-135">**Iinkanalyzer:: feateanalysishint-Methode**</span><span class="sxs-lookup"><span data-stu-id="2a97c-135">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="2a97c-136">**Icontextnode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="2a97c-136">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="2a97c-137">**Icontextnode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="2a97c-137">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="2a97c-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="2a97c-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




