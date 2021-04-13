---
title: Value-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IValueProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Value-Steuerelement Musters
- UI-Automatisierung, wertsteuer Element Muster
- UI-Automatisierung, IValueProvider
- IValueProvider
- Implementieren von Wert Steuerungs Mustern für Benutzeroberflächen Automatisierung
- Wertsteuer Element Muster
- Steuerelement Muster, IValueProvider
- Steuerelement Muster, Implementieren des Benutzeroberflächenautomatisierungs-Werts
- Steuerelement Muster, Wert
- Schnittstellen, IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390656"
---
# <a name="value-control-pattern"></a><span data-ttu-id="f6b0f-113">Value-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="f6b0f-113">Value Control Pattern</span></span>

<span data-ttu-id="f6b0f-114">Beschreibt Richtlinien und Konventionen für das Implementieren von [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-114">Describes guidelines and conventions for implementing [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="f6b0f-115">Das **value** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die einen systeminternen Wert aufweisen, der nicht einen Bereich umfasst und als Zeichenfolge dargestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-115">The **Value** control pattern is used to support controls that have an intrinsic value not spanning a range and that can be represented as a string.</span></span>

<span data-ttu-id="f6b0f-116">Die Wert Zeichenfolge kann je nach Steuerelement und den zugehörigen Einstellungen bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-116">The value string can be editable, depending on the control and its settings.</span></span> <span data-ttu-id="f6b0f-117">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="f6b0f-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="f6b0f-118">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="f6b0f-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f6b0f-119">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="f6b0f-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="f6b0f-120">Erforderliche Member für **IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="f6b0f-120">Required Members for **IValueProvider**</span></span>](#required-members-for-ivalueprovider)
-   [<span data-ttu-id="f6b0f-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6b0f-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="f6b0f-122">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="f6b0f-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="f6b0f-123">Beachten Sie beim Implementieren des **value** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="f6b0f-123">When implementing the **Value** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="f6b0f-124">Steuerelemente wie ein Listenelement oder Strukturelement müssen das **value** -Steuerelement Muster unterstützen, wenn der Wert eines der Elemente unabhängig vom aktuellen Bearbeitungsmodus des Steuer Elements bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-124">Controls such as a list item or tree item must support the **Value** control pattern if the value of any of the items is editable, regardless of the current edit mode of the control.</span></span> <span data-ttu-id="f6b0f-125">Das übergeordnete Steuerelement muss auch das **value** -Steuerelement Muster unterstützen, wenn die untergeordneten Elemente bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-125">The parent control must also support the **Value** control pattern if the child items are editable.</span></span> <span data-ttu-id="f6b0f-126">Die folgende Abbildung zeigt ein Beispiel für ein bearbeitbares Listenelement.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-126">The following image shows an example of an editable list item.</span></span>

    ![Darstellung des bearbeitbaren Listen Elements](images/uia-valuepattern-editable-listitem.jpg)

- <span data-ttu-id="f6b0f-128">Ein-und mehrzeilige Bearbeitungs Steuerelemente müssen [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) implementieren, um Ihren schreibgeschützten Inhalt verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-128">Single and multi-line edit controls must implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) to expose their read-only content.</span></span>
- <span data-ttu-id="f6b0f-129">Mehrzeilige Bearbeitungs Steuerelemente müssen [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) implementieren, wenn deren Inhalt geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-129">Multi-line edit controls must implement [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) if their contents can be changed.</span></span>
- <span data-ttu-id="f6b0f-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) unterstützt nicht das Abrufen von Formatierungsinformationen oder Teil Zeichenfolgen-Werten.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) does not support the retrieval of formatting information or substring values.</span></span> <span data-ttu-id="f6b0f-131">Implementieren Sie [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in diesen Szenarien.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-131">Implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in these scenarios.</span></span>
- <span data-ttu-id="f6b0f-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) muss von Steuerelementen wie dem Auswahl Steuerelement für die Farbauswahl von Microsoft Word (siehe folgende Abbildung) implementiert werden, das die Zeichen folgen Zuordnung zwischen einem Farbwert (z. b. "gelb") und einem entsprechenden internen [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) -Wert unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) must be implemented by controls such as the color picker selection control from Microsoft Word (see the following image), which supports string mapping between a color value (for example, "yellow") and an equivalent internal [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) value.</span></span>

    ![Abbildung zur Darstellung der Zeichen folgen Zuordnung von Farbmustern](images/uia-valuepattern-colorpicker.jpg)

- <span data-ttu-id="f6b0f-134">Für ein Steuerelement sollte dessen **isaktivierte** Eigenschaft auf **true** festgelegt sein, und die [**ITextProvider:: isread only**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) -Eigenschaft muss auf **false** festgelegt werden, bevor ein Aufrufen von [**ITextProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-134">A control should have its **IsEnabled** property set to **TRUE** and its [**ITextProvider::IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) property set to **FALSE** before allowing a call to [**ITextProvider::SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span></span>

## <a name="required-members-for-ivalueprovider"></a><span data-ttu-id="f6b0f-135">Erforderliche Member für **IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="f6b0f-135">Required Members for **IValueProvider**</span></span>

<span data-ttu-id="f6b0f-136">Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-136">The following properties and methods are required for implementing the [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) interface.</span></span>



| <span data-ttu-id="f6b0f-137">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="f6b0f-137">Required members</span></span>                                       | <span data-ttu-id="f6b0f-138">Memberart</span><span class="sxs-lookup"><span data-stu-id="f6b0f-138">Member type</span></span> | <span data-ttu-id="f6b0f-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f6b0f-139">Notes</span></span> |
|--------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="f6b0f-140">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="f6b0f-140">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | <span data-ttu-id="f6b0f-141">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6b0f-141">Property</span></span>    | <span data-ttu-id="f6b0f-142">Keine</span><span class="sxs-lookup"><span data-stu-id="f6b0f-142">None</span></span>  |
| [<span data-ttu-id="f6b0f-143">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f6b0f-143">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | <span data-ttu-id="f6b0f-144">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6b0f-144">Property</span></span>    | <span data-ttu-id="f6b0f-145">Keine</span><span class="sxs-lookup"><span data-stu-id="f6b0f-145">None</span></span>  |
| [<span data-ttu-id="f6b0f-146">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="f6b0f-146">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | <span data-ttu-id="f6b0f-147">Methode</span><span class="sxs-lookup"><span data-stu-id="f6b0f-147">Method</span></span>      | <span data-ttu-id="f6b0f-148">Keine</span><span class="sxs-lookup"><span data-stu-id="f6b0f-148">None</span></span>  |



 

<span data-ttu-id="f6b0f-149">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-149">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6b0f-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6b0f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6b0f-151">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="f6b0f-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="f6b0f-152">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="f6b0f-152">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="f6b0f-153">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="f6b0f-153">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="f6b0f-154">Text-und TextRange-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="f6b0f-154">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 