---
title: Textchild-Steuerelement Muster
description: Führt Richtlinien und Konventionen zum Implementieren von itextchildprovider ein, einschließlich Informationen zu Eigenschaften und Methoden. Das textchild-Steuerelement Muster wird verwendet, um auf den nächsten Vorgänger eines Elements zuzugreifen, der das Text-Steuerelement Muster unterstützt.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines textchild-Steuerelement Musters
- UI-Automatisierung, textchild-Steuerelement Muster
- UI-Automatisierung, itextchildprovider
- ITextChildProvider
- Implementieren von textchild-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- Textchild-Steuerelement Muster
- Steuerelement Muster, itextchildprovider
- Steuerelement Muster, Implementieren von Benutzeroberflächen Automatisierung-textchild
- Steuerelement Muster, textchild
- Schnittstellen, itextchildprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21102abfef7cee0553850ac01c4f759f81988e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729953"
---
# <a name="textchild-control-pattern"></a><span data-ttu-id="d9859-114">Textchild-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="d9859-114">TextChild Control Pattern</span></span>

<span data-ttu-id="d9859-115">Führt Richtlinien und Konventionen zum Implementieren von [**itextchildprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider)ein, einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="d9859-115">Introduces guidelines and conventions for implementing [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), including information about properties and methods.</span></span> <span data-ttu-id="d9859-116">Das **textchild** -Steuerelement Muster wird verwendet, um auf den nächsten Vorgänger eines Elements zuzugreifen, der das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d9859-116">The **TextChild** control pattern is used to access an element’s nearest ancestor that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>

<span data-ttu-id="d9859-117">Angenommen, Text in einem Dokument enthält ein eingebettetes Bild und einen Hyperlink, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d9859-117">For example, suppose text in a document contains an embedded image and a hyperlink as shown in the following image.</span></span>

![Screenshot mit Text, der ein eingebettetes Bild und einen Hyperlink enthält](images/textchild-pattern.png)

<span data-ttu-id="d9859-119">Wenn Sie Microsoft UI Automation-Tools verwenden, um die Benutzeroberflächenautomatisierungs-Struktur für diesen Dokumentinhalt zu überprüfen, wird möglicherweise ein Dokument Element mit einem untergeordneten Element angezeigt, das das Bild darstellt, und ein weiteres untergeordnetes Element, das den Hyperlink darstellt</span><span class="sxs-lookup"><span data-stu-id="d9859-119">If you use Microsoft UI Automation tools to examine the UI Automation tree for this document content, it might show a document element with one child element that represents the image, and another child element that represents the hyperlink.</span></span> <span data-ttu-id="d9859-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d9859-120">For example:</span></span>

![Screenshot, der zeigt, wie Sie eine Beispiel-UI-Automatisierungs Elementstruktur melden](images/textchild-pattern-tree.png)

<span data-ttu-id="d9859-122">In der Regel unterstützt das Document-Element im vorangehenden Beispiel das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster, die beiden untergeordneten Elemente des Document-Elements jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="d9859-122">Typically, the document element in the preceding example supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, but the two children of the document element do not.</span></span> <span data-ttu-id="d9859-123">Wenn eine Benutzeroberflächenautomatisierungs-Client Anwendung über einen Verweis auf das Bildelement-oder Hyperlink-Element verfügt, kann der Client das **textchild** -Steuerelement Muster als bequeme Methode zum Zugreifen auf das TextControl-Muster verwenden, das vom enthaltenden Dokument Element verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="d9859-123">If a UI Automation client application has a reference to the image element or hyperlink element, the client can use the **TextChild** control pattern as a convenient way to access the Textcontrol pattern exposed by the containing document element.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="d9859-124">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="d9859-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="d9859-125">Beachten Sie beim Implementieren der [**itextchildprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) -Schnittstelle die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="d9859-125">When implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="d9859-126">Die [**itextchildprovider:: Text Container**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) -Eigenschaft sollte das nächste Vorgänger Element angeben, das die [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) -Schnittstelle unterstützt, unabhängig davon, ob auch Elemente in der Vorgänger Kette **ITextProvider** unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d9859-126">The [**ITextChildProvider::TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) property should specify the nearest ancestor element that supports [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) interface, regardless of whether elements higher in the ancestor chain also support **ITextProvider**.</span></span>
-   <span data-ttu-id="d9859-127">Ein Element sollte nicht sowohl die [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) -als auch die [itextchildprovider \* \*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d9859-127">An element should not support both the [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) and the [ITextChildProvider\*\*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>
- <span data-ttu-id="d9859-128">Ein Element, das [**itextchildprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) implementiert, muss ein untergeordnetes Element oder ein Nachfolger Element eines Elements sein, das [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider)implementiert.</span><span class="sxs-lookup"><span data-stu-id="d9859-128">An element that implements [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) must be a child, or descendent, of an element that implements [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span></span> <span data-ttu-id="d9859-129">Es ist nicht erforderlich, dass dieses Element auch das [Text-Steuerelement Muster](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange)implementiert.</span><span class="sxs-lookup"><span data-stu-id="d9859-129">It is not required that this element also implement the [Text control pattern](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span></span>
-   <span data-ttu-id="d9859-130">Die [**itextchildprovider:: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) -Eigenschaft sollte denselben Textbereich angeben, den das enthaltende Text Anbieter Element zurückgibt, wenn die zugehörige [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) -Funktion mit dem untergeordneten Text-Element als eingeschlossenes untergeordnetes Element aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d9859-130">The [**ITextChildProvider::TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) property should specify the same text range as the one that the containing text provider element returns when its [**ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) function is called with the text child element as the enclosed child element.</span></span>

## <a name="required-members-for-itextchildprovider"></a><span data-ttu-id="d9859-131">Erforderliche Member für **itextchildprovider**</span><span class="sxs-lookup"><span data-stu-id="d9859-131">Required Members for **ITextChildProvider**</span></span>

<span data-ttu-id="d9859-132">Diese Eigenschaften und Methoden sind für die Implementierung der [**itextchildprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d9859-132">These properties and methods are required for implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>



| <span data-ttu-id="d9859-133">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="d9859-133">Required members</span></span>                                                     | <span data-ttu-id="d9859-134">Memberart</span><span class="sxs-lookup"><span data-stu-id="d9859-134">Member type</span></span> | <span data-ttu-id="d9859-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9859-135">Notes</span></span> |
|----------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="d9859-136">**Text Container**</span><span class="sxs-lookup"><span data-stu-id="d9859-136">**TextContainer**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | <span data-ttu-id="d9859-137">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d9859-137">Property</span></span>    | <span data-ttu-id="d9859-138">Keine</span><span class="sxs-lookup"><span data-stu-id="d9859-138">None</span></span>  |
| [<span data-ttu-id="d9859-139">**TextRange**</span><span class="sxs-lookup"><span data-stu-id="d9859-139">**TextRange**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | <span data-ttu-id="d9859-140">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d9859-140">Property</span></span>    | <span data-ttu-id="d9859-141">Keine</span><span class="sxs-lookup"><span data-stu-id="d9859-141">None</span></span>  |



 

<span data-ttu-id="d9859-142">Diesem Steuerelementmuster sind keine Methoden oder Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d9859-142">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9859-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d9859-143">Related topics</span></span>

<span data-ttu-id="d9859-144">**Licher**</span><span class="sxs-lookup"><span data-stu-id="d9859-144">**Conceptual**</span></span>

- [<span data-ttu-id="d9859-145">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="d9859-145">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
- [<span data-ttu-id="d9859-146">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="d9859-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
- [<span data-ttu-id="d9859-147">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="d9859-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)