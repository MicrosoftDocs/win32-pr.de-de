---
description: Stellt die Fähigkeit dar, das Layout einer Auflistung von Strichen zu analysieren und Sie in Text und Grafiken aufzuteilen.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: InkDivider-Klasse (Msinkaut15. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: c0658504303968803bd2abff063694701d121390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352494"
---
# <a name="inkdivider-class"></a><span data-ttu-id="49126-103">InkDivider-Klasse</span><span class="sxs-lookup"><span data-stu-id="49126-103">InkDivider class</span></span>

<span data-ttu-id="49126-104">Stellt die Fähigkeit dar, das Layout einer Auflistung von Strichen zu analysieren und Sie in Text und Grafiken aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="49126-104">Represents the ability to analyze the layout of a collection of strokes and divide them into text and graphics.</span></span>

<span data-ttu-id="49126-105">**InkDivider** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="49126-105">**InkDivider** has these types of members:</span></span>

-   [<span data-ttu-id="49126-106">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="49126-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="49126-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="49126-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="49126-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49126-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="49126-109">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="49126-109">Interfaces</span></span>

<span data-ttu-id="49126-110">Diese Schnittstellen werden von der **InkDivider** -Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="49126-110">The **InkDivider** class defines these interfaces.</span></span>



| <span data-ttu-id="49126-111">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="49126-111">Interface</span></span>       | <span data-ttu-id="49126-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49126-112">Description</span></span>                                                          |
|:----------------|:---------------------------------------------------------------------|
| <span data-ttu-id="49126-113">**Iinkdivider**</span><span class="sxs-lookup"><span data-stu-id="49126-113">**IInkDivider**</span></span> | <span data-ttu-id="49126-114">Dieses Objekt implementiert die **iinkdivider** -com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="49126-114">This object implements the **IInkDivider** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="49126-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="49126-115">Methods</span></span>

<span data-ttu-id="49126-116">Die **InkDivider** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="49126-116">The **InkDivider** class has these methods.</span></span>



| <span data-ttu-id="49126-117">Methode</span><span class="sxs-lookup"><span data-stu-id="49126-117">Method</span></span>                              | <span data-ttu-id="49126-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49126-118">Description</span></span>                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49126-119">**Glie**</span><span class="sxs-lookup"><span data-stu-id="49126-119">**Divide**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | <span data-ttu-id="49126-120">Gibt ein [**iinkdivisionresult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) -Objekt zurück, das Strukturinformationen zu den Strichen im **InkDivider** -Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="49126-120">Returns an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object that contains structural information about the strokes in the **InkDivider** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="49126-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49126-121">Properties</span></span>

<span data-ttu-id="49126-122">Die **InkDivider** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="49126-122">The **InkDivider** class has these properties.</span></span>



| <span data-ttu-id="49126-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="49126-123">Property</span></span>                                                             | <span data-ttu-id="49126-124">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="49126-124">Access type</span></span>           | <span data-ttu-id="49126-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49126-125">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49126-126">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="49126-126">**LineHeight**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | <span data-ttu-id="49126-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="49126-127">Read/write</span></span><br/> | <span data-ttu-id="49126-128">Ruft die erwartete Handschrift Höhe in HIMETRIC-Einheiten ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="49126-128">Gets or sets the expected handwriting height in HIMETRIC units.</span></span><br/>                                                      |
| [<span data-ttu-id="49126-129">**Erkennungs Kontext**</span><span class="sxs-lookup"><span data-stu-id="49126-129">**RecognizerContext**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | <span data-ttu-id="49126-130">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="49126-130">Read/write</span></span><br/> | <span data-ttu-id="49126-131">Ruft das für die Handschrifterkennung verwendete [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="49126-131">Gets or sets the [**InkRecognizerContext**](inkrecognizercontext-class.md) object used for handwriting recognition.</span></span><br/> |
| [<span data-ttu-id="49126-132">**Striche**</span><span class="sxs-lookup"><span data-stu-id="49126-132">**Strokes**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | <span data-ttu-id="49126-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="49126-133">Read/write</span></span><br/> | <span data-ttu-id="49126-134">Ruft die im **InkDivider** -Objekt enthaltene [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="49126-134">Gets or sets the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained by the **InkDivider** object.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="49126-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49126-135">Remarks</span></span>

<span data-ttu-id="49126-136">Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="49126-136">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="49126-137">Das **InkDivider** -Objekt verwendet das Layout der Striche, die Reihenfolge, in der die Striche hinzugefügt werden, die Richtung, in der die Striche gezeichnet werden, und andere Faktoren zum Durchführen der Analyse der frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="49126-137">The **InkDivider** object uses the layout of the strokes, the order in which the strokes are added, the direction in which the strokes are drawn, and other factors to perform the analysis of the ink.</span></span> <span data-ttu-id="49126-138">Die vom **InkDivider** -Objekt analysierten [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ist in der [**Striche**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) -Eigenschaft des **InkDivider** -Objekts enthalten.</span><span class="sxs-lookup"><span data-stu-id="49126-138">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the **InkDivider** object analyzes is contained in the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property of the **InkDivider** object.</span></span> <span data-ttu-id="49126-139">Das **InkDivider** -Objekt analysiert die inkstrokes-Auflistung dynamisch, wenn Sie Sie der Auflistung hinzufügen oder daraus löschen, aber es führt keine Änderung der Striche aus.</span><span class="sxs-lookup"><span data-stu-id="49126-139">The **InkDivider** object dynamically analyzes the InkStrokes collection as you add to or delete from the collection, but it performs no modification of the strokes.</span></span>

<span data-ttu-id="49126-140">Die Analyseergebnisse werden in einem [**iinkdivisionresult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="49126-140">The analysis results are returned in an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="49126-141">Das **InkDivider** -Objekt verwendet ein [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt, um die Striche genauer aufzuteilen und den Ergebnissen eine Erkennungs Zeichenfolge zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="49126-141">The **InkDivider** object uses an [**InkRecognizerContext**](inkrecognizercontext-class.md) object to more accurately divide the strokes and to assign a recognition string to the results.</span></span>

> [!Note]  
> <span data-ttu-id="49126-142">Das **InkDivider** -Objekt verwendet die Standard Eigenschafts Einstellungen des [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="49126-142">The **InkDivider** object uses the default property settings of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="49126-143">Wenn Sie dem **InkDivider** -Objekt keinen Erkennungs Kontext zuweisen, analysiert das **InkDivider** -Objekt weiterhin die frei Hand Eingaben, dividiert die Striche jedoch weniger genau und ordnet der Divisions Ergebnisse keinen Text zu.</span><span class="sxs-lookup"><span data-stu-id="49126-143">If you do not assign a recognizer context to the **InkDivider** object, the **InkDivider** object still analyzes the ink, but it divides the strokes less accurately and does not associate text with the division results.</span></span>

> [!Note]  
> <span data-ttu-id="49126-144">Die [**erkenzercontext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) -Eigenschaft sollte festgelegt werden, bevor der [**Striche**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) -Eigenschaft Striche hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="49126-144">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property should be set before adding strokes to the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property.</span></span> <span data-ttu-id="49126-145">Nach dem Hinzufügen von Strichen zum **InkDivider** -Objekt kann die Eigenschaft " **erkennzercontext** " nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="49126-145">After strokes have been added to the **InkDivider** object, the **RecognizerContext** property cannot be changed.</span></span>

 

<span data-ttu-id="49126-146">Der **InkDivider** unterstützt derzeit keine vertikalen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="49126-146">The **InkDivider** does not currently support vertical languages.</span></span> <span data-ttu-id="49126-147">Damit das **InkDivider** -Objekt diese Sprachen ordnungsgemäß erkennt, muss das [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekt für die Sprache die kostenlose Eingabe Funktion unterstützen, und die Zeichen müssen von links nach rechts geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="49126-147">For the **InkDivider** object to recognize these languages properly the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object for the language must support the free input capability and the characters must be written from left to right.</span></span>

## <a name="requirements"></a><span data-ttu-id="49126-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49126-148">Requirements</span></span>



| <span data-ttu-id="49126-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49126-149">Requirement</span></span> | <span data-ttu-id="49126-150">Wert</span><span class="sxs-lookup"><span data-stu-id="49126-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49126-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49126-151">Minimum supported client</span></span><br/> | <span data-ttu-id="49126-152">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49126-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="49126-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49126-153">Minimum supported server</span></span><br/> | <span data-ttu-id="49126-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="49126-154">None supported</span></span><br/>                                                                                               |
| <span data-ttu-id="49126-155">Header</span><span class="sxs-lookup"><span data-stu-id="49126-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="49126-156"><dt>Msinkaut15. h (erfordert auch Msinkaut15 \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="49126-156"><dt>Msinkaut15.h (also requires Msinkaut15\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="49126-157">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="49126-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="49126-158"><dt>Inkdiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49126-158"><dt>Inkdiv.dll</dt></span></span> </dl>                                   |



## <a name="see-also"></a><span data-ttu-id="49126-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49126-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49126-160">**Iinkdivisionresult-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="49126-160">**IInkDivisionResult Interface**</span></span>](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[<span data-ttu-id="49126-161">**Inkrecognizercontext-Klasse**</span><span class="sxs-lookup"><span data-stu-id="49126-161">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

<span data-ttu-id="49126-162">[Inkstrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="49126-162">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

