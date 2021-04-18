---
description: Die Layoutanalyse basiert auf einer Striche-Auflistung und klassifiziert die Striche in Handschrift-und Zeichnungs Elemente. Das Divider-Objekt ermöglicht den Zugriff auf die Features der Tablet PC-Layoutanalyse.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Layoutanalyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0901e7c7df96bec5ea3972f643469033fbb22ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351734"
---
# <a name="layout-analysis"></a><span data-ttu-id="40262-104">Layoutanalyse</span><span class="sxs-lookup"><span data-stu-id="40262-104">Layout Analysis</span></span>

<span data-ttu-id="40262-105">Die Layoutanalyse basiert auf einer [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung und klassifiziert die Striche in Handschrift-und Zeichnungs Elemente.</span><span class="sxs-lookup"><span data-stu-id="40262-105">Layout analysis operates on a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection and classifies the strokes into handwriting and drawing elements.</span></span> <span data-ttu-id="40262-106">Das [**Divider**](inkdivider-class.md) -Objekt ermöglicht den Zugriff auf die Features der Tablet PC-Layoutanalyse.</span><span class="sxs-lookup"><span data-stu-id="40262-106">The [**Divider**](inkdivider-class.md) object provides access to the Tablet PC layout analysis features.</span></span>

<span data-ttu-id="40262-107">In der folgenden Tabelle werden die strukturellen Elementtypen der [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) -Enumeration beschrieben, in die das unter [**Teiler**](inkdivider-class.md) -Objekt Striche klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="40262-107">The following table describes the structural element types of the [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration into which the [**Divider**](inkdivider-class.md) object classifies strokes.</span></span>



| <span data-ttu-id="40262-108">type</span><span class="sxs-lookup"><span data-stu-id="40262-108">Type</span></span>          | <span data-ttu-id="40262-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40262-109">Description</span></span>                                                                      |
|---------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="40262-110">**Segment**</span><span class="sxs-lookup"><span data-stu-id="40262-110">**Segment**</span></span>   | <span data-ttu-id="40262-111">Ein Erkennungs Segment.</span><span class="sxs-lookup"><span data-stu-id="40262-111">A recognition segment.</span></span><br/>                                                |
| <span data-ttu-id="40262-112">**Line**</span><span class="sxs-lookup"><span data-stu-id="40262-112">**Line**</span></span>      | <span data-ttu-id="40262-113">Eine Handschrift Zeile, die ein oder mehrere Erkennungs Segmente enthält.</span><span class="sxs-lookup"><span data-stu-id="40262-113">A line of handwriting that contains one or more recognition segments.</span></span><br/> |
| <span data-ttu-id="40262-114">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="40262-114">**Paragraph**</span></span> | <span data-ttu-id="40262-115">Ein Block von Strichen, der eine oder mehrere Zeilen der Handschrift enthält.</span><span class="sxs-lookup"><span data-stu-id="40262-115">A block of strokes that contains one or more lines of handwriting.</span></span><br/>    |
| <span data-ttu-id="40262-116">**Zeichnung**</span><span class="sxs-lookup"><span data-stu-id="40262-116">**Drawing**</span></span>   | <span data-ttu-id="40262-117">Frei Handschrift.</span><span class="sxs-lookup"><span data-stu-id="40262-117">Ink that is not handwriting.</span></span><br/>                                          |



 

<span data-ttu-id="40262-118">Das [**Divider**](inkdivider-class.md) -Objekt verfügt über eine [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die das **Divider** -Objekt dynamisch analysiert, wenn Sie der Auflistung hinzufügen oder daraus löschen.</span><span class="sxs-lookup"><span data-stu-id="40262-118">The [**Divider**](inkdivider-class.md) object has a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection, which the **Divider** object dynamically analyzes each time you add to or delete from the collection.</span></span> <span data-ttu-id="40262-119">Das **Divider** -Objekt ist nicht serialisierbar, und der Analyse Zustand kann nicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="40262-119">The **Divider** object is not serializable, and you cannot save its analysis state.</span></span> <span data-ttu-id="40262-120">Folglich ist das **Divider** -Objekt für Anwendungen konzipiert, die zwischen gemischtem Handschrift und Zeichnungs Eingaben unterscheiden müssen, aber keine großen Mengen von frei Hand Eingaben zwischen den Sitzungen neu analysieren müssen.</span><span class="sxs-lookup"><span data-stu-id="40262-120">Thus the **Divider** object is designed for applications that must differentiate between mixed handwriting and drawing input, but do not need to reanalyze large amounts of ink between sessions.</span></span>

<span data-ttu-id="40262-121">Sie können eine statische Momentaufnahme des aktuellen Analyse Ergebnisses abrufen, die in einem [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) -Objekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="40262-121">You can obtain a static snapshot of the current analysis result, which is returned in a [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span> <span data-ttu-id="40262-122">Sie können [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) -Objekte abrufen, die jeweils ein einzelnes Strukturelement eines **DivisionResult** -Objekts darstellen.</span><span class="sxs-lookup"><span data-stu-id="40262-122">You can obtain [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) objects, each which represents a single structural element of a **DivisionResult** object.</span></span> <span data-ttu-id="40262-123">Die Objekte " **DivisionResult** " und " **DivisionUnit** " sind nicht serialisierbar.</span><span class="sxs-lookup"><span data-stu-id="40262-123">The **DivisionResult** and **DivisionUnit** objects are not serializable.</span></span> <span data-ttu-id="40262-124">Zustandsinformationen aus diesen Objekten sind jedoch verfügbar.</span><span class="sxs-lookup"><span data-stu-id="40262-124">However, state information from these objects is available.</span></span>

<span data-ttu-id="40262-125">Das [**Divider**](inkdivider-class.md) -Objekt funktioniert nur mit der Handschrift von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="40262-125">The [**Divider**](inkdivider-class.md) object works only with left-to-right handwriting.</span></span> <span data-ttu-id="40262-126">Damit das unter **Teiler** -Objekt vertikale Sprachen, wie z. b. Chinesisch, ordnungsgemäß analysieren kann, müssen die Zeichen von links nach rechts und nicht von oben nach unten gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="40262-126">For the **Divider** object to analyze vertical languages such as Chinese correctly, the characters must be drawn left-to-right instead of top-to-bottom.</span></span>

 

