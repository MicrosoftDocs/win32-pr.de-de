---
description: Stellt den Bereich dar, den die Erkennung verwendet, in dem frei Hand Eingaben gezeichnet werden können. Der Bereich wird als Erkennungs Handbuch bezeichnet.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: InkRecognizerGuide-Klasse (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 55729513f748afc87f184b73eaba976184307bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218578"
---
# <a name="inkrecognizerguide-class"></a><span data-ttu-id="9c29b-104">InkRecognizerGuide-Klasse</span><span class="sxs-lookup"><span data-stu-id="9c29b-104">InkRecognizerGuide class</span></span>

<span data-ttu-id="9c29b-105">Stellt den Bereich dar, den die Erkennung verwendet, in dem frei Hand Eingaben gezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="9c29b-105">Represents the area that the recognizer uses in which ink can be drawn.</span></span> <span data-ttu-id="9c29b-106">Der Bereich wird als Erkennungs Handbuch bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9c29b-106">The area is known as the recognition guide.</span></span>

<span data-ttu-id="9c29b-107">**InkRecognizerGuide** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9c29b-107">**InkRecognizerGuide** has these types of members:</span></span>

-   [<span data-ttu-id="9c29b-108">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9c29b-108">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="9c29b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c29b-109">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="9c29b-110">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9c29b-110">Interfaces</span></span>

<span data-ttu-id="9c29b-111">Diese Schnittstellen werden von der **InkRecognizerGuide** -Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="9c29b-111">The **InkRecognizerGuide** class defines these interfaces.</span></span>



| <span data-ttu-id="9c29b-112">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9c29b-112">Interface</span></span>               | <span data-ttu-id="9c29b-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c29b-113">Description</span></span>                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="9c29b-114">**Iinkrecognizerguide**</span><span class="sxs-lookup"><span data-stu-id="9c29b-114">**IInkRecognizerGuide**</span></span> | <span data-ttu-id="9c29b-115">Dieses Objekt implementiert die **iinkrecognizerguide** -com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9c29b-115">This object implements the **IInkRecognizerGuide** COM interface.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9c29b-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c29b-116">Properties</span></span>

<span data-ttu-id="9c29b-117">Die **InkRecognizerGuide** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9c29b-117">The **InkRecognizerGuide** class has these properties.</span></span>



| <span data-ttu-id="9c29b-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9c29b-118">Property</span></span>                                                       | <span data-ttu-id="9c29b-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="9c29b-119">Access type</span></span>           | <span data-ttu-id="9c29b-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c29b-120">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c29b-121">**Spalten**</span><span class="sxs-lookup"><span data-stu-id="9c29b-121">**Columns**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | <span data-ttu-id="9c29b-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9c29b-122">Read/write</span></span><br/> | <span data-ttu-id="9c29b-123">Ruft die Anzahl der Spalten im Führungs Feld ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="9c29b-123">Gets or sets the number of columns in the guide box.</span></span><br/>                                                                |
| [<span data-ttu-id="9c29b-124">**Drawnbox**</span><span class="sxs-lookup"><span data-stu-id="9c29b-124">**DrawnBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | <span data-ttu-id="9c29b-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9c29b-125">Read/write</span></span><br/> | <span data-ttu-id="9c29b-126">Ruft das Feld ab, das physisch auf dem Bildschirm des Tablets gezeichnet wird und in dem geschrieben wird, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="9c29b-126">Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place.</span></span><br/>              |
| [<span data-ttu-id="9c29b-127">**Guidedata**</span><span class="sxs-lookup"><span data-stu-id="9c29b-127">**GuideData**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | <span data-ttu-id="9c29b-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9c29b-128">Read/write</span></span><br/> | <span data-ttu-id="9c29b-129">Ruft Führungs Daten für C++-Entwickler ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="9c29b-129">Gets or sets guide data for C++ developers.</span></span><br/>                                                                         |
| [<span data-ttu-id="9c29b-130">**Vervollständigen**</span><span class="sxs-lookup"><span data-stu-id="9c29b-130">**Midline**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | <span data-ttu-id="9c29b-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9c29b-131">Read/write</span></span><br/> | <span data-ttu-id="9c29b-132">Ruft die Höhe des Mittelpunkts ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="9c29b-132">Gets or sets the midline height.</span></span> <span data-ttu-id="9c29b-133">Die Höhe des Mittelpunkts liegt zwischen der Baseline und der Mitte der gezeichneten Box.</span><span class="sxs-lookup"><span data-stu-id="9c29b-133">The midline height is distance from the baseline to the midline, of the drawn box.</span></span><br/> |
| [<span data-ttu-id="9c29b-134">**Streitigkeiten**</span><span class="sxs-lookup"><span data-stu-id="9c29b-134">**Rows**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | <span data-ttu-id="9c29b-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9c29b-135">Read/write</span></span><br/> | <span data-ttu-id="9c29b-136">Ruft die Anzahl der Zeilen im Führungs Feld ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="9c29b-136">Gets or sets the number of rows in the guide box.</span></span><br/>                                                                   |
| [<span data-ttu-id="9c29b-137">**Beschreibbox**</span><span class="sxs-lookup"><span data-stu-id="9c29b-137">**WritingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | <span data-ttu-id="9c29b-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9c29b-138">Read/write</span></span><br/> | <span data-ttu-id="9c29b-139">Ruft den nicht sichtbaren Schreibbereich des Handbuchs ab, in dem geschrieben werden kann, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="9c29b-139">Gets or sets the invisible writing area of the guide box in which writing can actually take place.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="9c29b-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c29b-140">Remarks</span></span>

<span data-ttu-id="9c29b-141">Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="9c29b-141">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method.</span></span>

<span data-ttu-id="9c29b-142">Standardmäßig gibt es keine Erkennungs Anleitung.</span><span class="sxs-lookup"><span data-stu-id="9c29b-142">By default, there is no recognizer guide.</span></span> <span data-ttu-id="9c29b-143">In einem standardhandbuch sind alle Eigenschaftswerte auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c29b-143">A default guide has all property values set to 0.</span></span> <span data-ttu-id="9c29b-144">Sie müssen die Eigenschaften dieses-Objekts verwenden, um das Handbuch festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9c29b-144">You must use the properties of this object to set the guide.</span></span>

<span data-ttu-id="9c29b-145">Wenn die Anwendung Richtlinien auf dem Bildschirm gezeichnet hat, auf dem der Benutzer zu schreiben erwartet, sollte die Anwendung die Werte der Eigenschaften des Erkennungs Leitfadens festlegen, um die Erkennung zu informieren.</span><span class="sxs-lookup"><span data-stu-id="9c29b-145">If the application has drawn guidelines on the screen on which the user is expected to write, the application should set the values of the properties of the recognizer guide to inform the recognizer.</span></span> <span data-ttu-id="9c29b-146">Diese Eigenschaften sind nur für die Verwendung durch die Erkennung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="9c29b-146">These properties are for the recognizer's use only.</span></span> <span data-ttu-id="9c29b-147">Wenn Sie Sie festlegen, zeichnen Sie visuelle Hinweise auf der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="9c29b-147">Setting them does not, by itself, draw visual clues on the display.</span></span> <span data-ttu-id="9c29b-148">Die Anwendung oder das Steuerelement zeichnet die visuellen Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9c29b-148">The application or the control draws the visual clues.</span></span>

<span data-ttu-id="9c29b-149">Das Erkennungs Handbuch kann aus Zeilen und Spalten bestehen, und diese geben der Erkennung einen besseren Kontext zum Durchführen der Erkennung.</span><span class="sxs-lookup"><span data-stu-id="9c29b-149">The recognizer guide can consist of rows and columns, and these give the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="9c29b-150">Buchstaben wie "t" und "I" lassen sich leichter erkennen, wenn ein Leitfaden verwendet wird, um dem frei Hand Kontext Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="9c29b-150">Letters such as "t" and "I" are more easily recognized when a guide is used to give context to the ink.</span></span> <span data-ttu-id="9c29b-151">Beispielsweise können Sie horizontale Linien auf einem Bildschirm zeichnen, die anzeigen, wo das Schreiben erfolgen soll (dieser Richtlinientyp würde nur aus Zeilen und ohne Spalten bestehen).</span><span class="sxs-lookup"><span data-stu-id="9c29b-151">For example, you can draw horizontal lines on a screen, that show where writing should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="9c29b-152">Durch das Schreiben in den Zeilen wird die Erkennungsgenauigkeit verbessert, anstatt etwas beliebiges Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="9c29b-152">By writing on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="9c29b-153">Das Handbuch gibt die Grenzen des frei Hand Zeichens in frei Hand Raumkoordinaten an.</span><span class="sxs-lookup"><span data-stu-id="9c29b-153">The guide specifies the boundaries of the ink in ink space coordinates.</span></span>

<span data-ttu-id="9c29b-154">Die [**drawnbox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) -Eigenschaft kann ein Feld definieren, das der Größe entspricht, die kleiner ist als das von der Eigenschaft " [**Write Box**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) " definierte Feld.</span><span class="sxs-lookup"><span data-stu-id="9c29b-154">The [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) property can define a box which is the same size as or smaller than the box defined by the [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) property.</span></span>

<span data-ttu-id="9c29b-155">Die folgende Abbildung zeigt die Elemente eines Erkennungs Leitfadens mit zwei Zeilen und ohne Spalten.</span><span class="sxs-lookup"><span data-stu-id="9c29b-155">The following figure shows the elements of a recognizer guide with two rows and no columns.</span></span>

![Abbildung der Elemente des Erkennungs Leitfadens](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

<span data-ttu-id="9c29b-157">Zusätzlich zum Zeichnen von Linien auf dem Bildschirm, die Benutzer anzeigen, für die Sie schreiben möchten, können Sie Zellen auf dem Bildschirm zeichnen, in denen Zeichen oder Wörter geschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="9c29b-157">In addition to drawing lines on the screen that show users where to write, you can draw cells on the screen in which characters or words are written.</span></span> <span data-ttu-id="9c29b-158">Dies wird als eingegebene Eingabe bezeichnet und ist für einige asiatische Sprachen nützlich.</span><span class="sxs-lookup"><span data-stu-id="9c29b-158">This is called boxed input and is useful with some Asian languages.</span></span> <span data-ttu-id="9c29b-159">Um zu ermitteln, ob die Erkennung in der Lage ist, eine eingegebene Eingabe aufzurufen, müssen Sie die Eigenschaft [**Funktionen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) des [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekts aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9c29b-159">To determine if the recognizer is capable of boxed input, call the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object.</span></span>

<span data-ttu-id="9c29b-160">Die folgende Abbildung zeigt eine Erkennungs Anleitung mit vier Spalten.</span><span class="sxs-lookup"><span data-stu-id="9c29b-160">The following figure shows a recognizer guide with four columns.</span></span>

![Darstellung des Erkennungs Leitfadens mit vier Spalten](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a><span data-ttu-id="9c29b-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c29b-162">Requirements</span></span>



| <span data-ttu-id="9c29b-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c29b-163">Requirement</span></span> | <span data-ttu-id="9c29b-164">Wert</span><span class="sxs-lookup"><span data-stu-id="9c29b-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c29b-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c29b-165">Minimum supported client</span></span><br/> | <span data-ttu-id="9c29b-166">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c29b-166">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9c29b-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c29b-167">Minimum supported server</span></span><br/> | <span data-ttu-id="9c29b-168">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9c29b-168">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9c29b-169">Header</span><span class="sxs-lookup"><span data-stu-id="9c29b-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c29b-170"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9c29b-170"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9c29b-171">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9c29b-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c29b-172"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c29b-172"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9c29b-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c29b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c29b-174">**Iinkrecognizer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9c29b-174">**IInkRecognizer Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[<span data-ttu-id="9c29b-175">**Inkrecognizercontext-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9c29b-175">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

