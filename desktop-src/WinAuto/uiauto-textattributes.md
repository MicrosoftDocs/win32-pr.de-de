---
title: Benutzeroberflächenautomatisierungs-Text Attribute
description: In diesem Thema wird beschrieben, wie die Microsoft-Benutzeroberflächen Automatisierung die Format-und Stileigenschaften (Text Attribute) von Textinhalten verfügbar macht und eine Liste unterstützter Text Attribute bereitstellt.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- UI-Automatisierung, Text Attribute
- Text Attribute, Informationen zu
- Text Attribute, Variant-Typen
- Text Attribute, Datentypen
- Benutzeroberflächen Automatisierung, Liste der Attribute
- UI-Automatisierung, Liste von Textattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b011203111a6484156921d63cc27bb11b017e596
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341536"
---
# <a name="ui-automation-text-attributes"></a><span data-ttu-id="f3d55-109">Benutzeroberflächenautomatisierungs-Text Attribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-109">UI Automation Text Attributes</span></span>

<span data-ttu-id="f3d55-110">In diesem Thema wird beschrieben, wie die Microsoft-Benutzeroberflächen Automatisierung die Format-und Stileigenschaften (*Text Attribute*) von Textinhalten verfügbar macht und eine Liste unterstützter Text Attribute bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f3d55-110">This topic describes how Microsoft UI Automation exposes the format and style properties (*text attributes*) of textual content, and provides a list of supported text attributes.</span></span>

<span data-ttu-id="f3d55-111">Benutzeroberflächenautomatisierungs-Anbieter machen Text Attribute über die [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) -und [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) -Methode des [TextRange](uiauto-about-text-and-textrange-patterns.md) -Steuerelement Musters verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3d55-111">UI Automation providers expose text attributes through the [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) and [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) methods of the [TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern.</span></span> <span data-ttu-id="f3d55-112">Client Anwendungen verwenden die [**iuiautomationtextrange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) -Methode, um den Wert eines bestimmten Text Attributs für einen Textbereich abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f3d55-112">Client applications use the [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) method to retrieve the value of a particular text attribute for a text range.</span></span> <span data-ttu-id="f3d55-113">Clients können die [**iuiautomationtextrange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) -Methode verwenden, um einen Textbereich nach Text zu durchsuchen, der über ein bestimmtes Attribut verfügt.</span><span class="sxs-lookup"><span data-stu-id="f3d55-113">Clients can use the [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) method to search a text range for text that has a particular attribute.</span></span> <span data-ttu-id="f3d55-114">Wenn ein übereinstimmender Text gefunden wird, erstellt die-Methode einen neuen Textbereich, der den übereinstimmenden Text enthält.</span><span class="sxs-lookup"><span data-stu-id="f3d55-114">If any matching text is found, the method creates a new text range that contains the matching text.</span></span>

<span data-ttu-id="f3d55-115">Die Text Attribute in der folgenden Liste werden vom **TextRange** -Steuerelement Muster unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f3d55-115">The text attributes in the following list are supported by the **TextRange** control pattern.</span></span> <span data-ttu-id="f3d55-116">Die Attributnamen stammen aus den Benutzeroberflächenautomatisierungs-Text Attribut bezeichnerbezeichner.</span><span class="sxs-lookup"><span data-stu-id="f3d55-116">The attribute names are derived from the UI Automation text attribute identifiers.</span></span> <span data-ttu-id="f3d55-117">Das **AnimationStyle** -Attribut wird z. b. von Clients als [**UIA \_ animationstyleattributeid**](uiauto-textattribute-ids.md) (definiert in UIAutomationClient. h) und von Anbietern als **Text \_ AnimationStyle-Attribut- \_ \_ GUID** (definiert in uiautomationcoreapi. h) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f3d55-117">For example, the **AnimationStyle** attribute is identified by clients as [**UIA\_AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (defined in Uiautomationclient.h) and by providers as **Text\_AnimationStyle\_Attribute\_GUID** (defined in Uiautomationcoreapi.h).</span></span> <span data-ttu-id="f3d55-118">Weitere Informationen zu den einzelnen unterstützten Textattributen finden Sie unter [**Text Attribut**](uiauto-textattribute-ids.md)Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f3d55-118">For more information about each supported text attribute, see [**Text Attribute Identifiers**](uiauto-textattribute-ids.md).</span></span>

> [!Note]  
> <span data-ttu-id="f3d55-119">Einige der aufgeführten Attribute werden ab Windows 8 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f3d55-119">Some of the attributes listed are supported starting with Windows 8.</span></span> <span data-ttu-id="f3d55-120">Hinweise zur Versions Unterstützung finden Sie unter [**Text Attribut**](uiauto-textattribute-ids.md) Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f3d55-120">See [**Text Attribute Identifiers**](uiauto-textattribute-ids.md) for notes regarding version support.</span></span>

 

<span data-ttu-id="f3d55-121">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="f3d55-121">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f3d55-122">Anmerkungsattribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-122">Annotation Attributes</span></span>](#annotation-attributes)
-   [<span data-ttu-id="f3d55-123">Schriftartattribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-123">Font Attributes</span></span>](#font-attributes)
-   [<span data-ttu-id="f3d55-124">Sprach Attribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-124">Language Attributes</span></span>](#language-attributes)
-   [<span data-ttu-id="f3d55-125">Link-Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-125">Link Attribute</span></span>](#link-attribute)
-   [<span data-ttu-id="f3d55-126">Seitenrand Attribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-126">Page Margin Attributes</span></span>](#page-margin-attributes)
-   [<span data-ttu-id="f3d55-127">Text Ausrichtungs Attribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-127">Text Alignment Attributes</span></span>](#text-alignment-attributes)
-   [<span data-ttu-id="f3d55-128">Textfarbattribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-128">Text Color Attributes</span></span>](#text-color-attributes)
-   [<span data-ttu-id="f3d55-129">Attribute für die Text Dekoration</span><span class="sxs-lookup"><span data-stu-id="f3d55-129">Text Decoration Attributes</span></span>](#text-decoration-attributes)
-   [<span data-ttu-id="f3d55-130">Textstilattribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-130">Text Style Attributes</span></span>](#text-style-attributes)
-   [<span data-ttu-id="f3d55-131">Interaktions-und Auswahl Attribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-131">Interaction and Selection Attributes</span></span>](#interaction-and-selection-attributes)
-   [<span data-ttu-id="f3d55-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3d55-132">Related topics</span></span>](#related-topics)

## <a name="annotation-attributes"></a><span data-ttu-id="f3d55-133">Anmerkungsattribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-133">Annotation Attributes</span></span>

<span data-ttu-id="f3d55-134">Anmerkung-Objekte und-Anmerkungen sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3d55-134">Annotation objects and annotation types are available through the following attributes.</span></span>



| <span data-ttu-id="f3d55-135">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-135">Attribute</span></span>             | <span data-ttu-id="f3d55-136">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f3d55-136">Identifier</span></span>                                                            |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="f3d55-137">**Annotationobjects**</span><span class="sxs-lookup"><span data-stu-id="f3d55-137">**AnnotationObjects**</span></span> | [<span data-ttu-id="f3d55-138">**UIA \_ annotationobjecungsattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-138">**UIA\_AnnotationObjectsAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="f3d55-139">**Annotationtypes**</span><span class="sxs-lookup"><span data-stu-id="f3d55-139">**AnnotationTypes**</span></span>   | [<span data-ttu-id="f3d55-140">**UIA \_ annotationtypesattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-140">**UIA\_AnnotationTypesAttributeId**</span></span>](uiauto-textattribute-ids.md)   |



 

## <a name="font-attributes"></a><span data-ttu-id="f3d55-141">Schriftartattribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-141">Font Attributes</span></span>

<span data-ttu-id="f3d55-142">Name, Größe und Gewichtung einer Schriftart sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3d55-142">The name, size, and weight of a font is available through the following attributes.</span></span>



| <span data-ttu-id="f3d55-143">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-143">Attribute</span></span>      | <span data-ttu-id="f3d55-144">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f3d55-144">Identifier</span></span>                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d55-145">**FontName**</span><span class="sxs-lookup"><span data-stu-id="f3d55-145">**FontName**</span></span>   | [<span data-ttu-id="f3d55-146">**UIA \_ fontnameattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-146">**UIA\_FontNameAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="f3d55-147">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="f3d55-147">**FontSize**</span></span>   | [<span data-ttu-id="f3d55-148">**UIA \_ fontsizeattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-148">**UIA\_FontSizeAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="f3d55-149">**Schriftbreite**</span><span class="sxs-lookup"><span data-stu-id="f3d55-149">**FontWeight**</span></span> | [<span data-ttu-id="f3d55-150">**UIA \_ fontweightattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-150">**UIA\_FontWeightAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a><span data-ttu-id="f3d55-151">Sprach Attribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-151">Language Attributes</span></span>

<span data-ttu-id="f3d55-152">Informationen zur Sprache des Texts sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3d55-152">Information about the language of the text is available through the following attributes.</span></span>



| <span data-ttu-id="f3d55-153">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-153">Attribute</span></span>              | <span data-ttu-id="f3d55-154">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f3d55-154">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d55-155">**Kultur**</span><span class="sxs-lookup"><span data-stu-id="f3d55-155">**Culture**</span></span>            | [<span data-ttu-id="f3d55-156">**UIA \_ cultureattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-156">**UIA\_CultureAttributeId**</span></span>](uiauto-textattribute-ids.md)                       |
| <span data-ttu-id="f3d55-157">**TextFlowDirections**</span><span class="sxs-lookup"><span data-stu-id="f3d55-157">**TextFlowDirections**</span></span> | [<span data-ttu-id="f3d55-158">**UIA- \_ textflowdirectionsattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-158">**UIA\_TextFlowDirectionsAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a><span data-ttu-id="f3d55-159">Link-Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-159">Link Attribute</span></span>

<span data-ttu-id="f3d55-160">Mit dem folgenden Attribut wird der Textbereich bereitstellt, der das Ziel eines Links in einem Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="f3d55-160">The following attribute provides the text range that is the target of a link in a document.</span></span>



| <span data-ttu-id="f3d55-161">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-161">Attribute</span></span> | <span data-ttu-id="f3d55-162">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f3d55-162">Identifier</span></span>                                                                   |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="f3d55-163">**Link**</span><span class="sxs-lookup"><span data-stu-id="f3d55-163">**Link**</span></span>  | [<span data-ttu-id="f3d55-164">**UIA \_ linkattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-164">**UIA\_LinkAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a><span data-ttu-id="f3d55-165">Seitenrand Attribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-165">Page Margin Attributes</span></span>

<span data-ttu-id="f3d55-166">Die Begrenzungs Rechtecke eines Text Bereichs machen die Koordinaten des Texts auf der Seite nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3d55-166">The bounding rectangles of a text range do not expose the coordinates of the text in the page.</span></span> <span data-ttu-id="f3d55-167">Ein Anbieter kann jedoch die Seitenrand Informationen mithilfe der folgenden Text Attribute verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="f3d55-167">However, a provider can expose the page margin information using the following text attributes.</span></span>



| <span data-ttu-id="f3d55-168">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-168">Attribute</span></span>          | <span data-ttu-id="f3d55-169">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f3d55-169">Identifier</span></span>                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d55-170">**MarginBottom**</span><span class="sxs-lookup"><span data-stu-id="f3d55-170">**MarginBottom**</span></span>   | [<span data-ttu-id="f3d55-171">**UIA \_ marginbottomattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-171">**UIA\_MarginBottomAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="f3d55-172">**MarginLeading**</span><span class="sxs-lookup"><span data-stu-id="f3d55-172">**MarginLeading**</span></span>  | [<span data-ttu-id="f3d55-173">**UIA \_ marginleadingattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-173">**UIA\_MarginLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)   |
| <span data-ttu-id="f3d55-174">**MarginTop**</span><span class="sxs-lookup"><span data-stu-id="f3d55-174">**MarginTop**</span></span>      | [<span data-ttu-id="f3d55-175">**UIA \_ margintopattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-175">**UIA\_MarginTopAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="f3d55-176">**MarginTrailing**</span><span class="sxs-lookup"><span data-stu-id="f3d55-176">**MarginTrailing**</span></span> | [<span data-ttu-id="f3d55-177">**UIA \_ margintrailingattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-177">**UIA\_MarginTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a><span data-ttu-id="f3d55-178">Text Ausrichtungs Attribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-178">Text Alignment Attributes</span></span>

<span data-ttu-id="f3d55-179">Informationen zur Textausrichtung, z. b. Einzug, Tabulator Einstellungen und horizontale Ausrichtung, sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3d55-179">Information about text alignment such as indentation, tab settings, and horizontal alignment is available through the following attributes.</span></span>



| <span data-ttu-id="f3d55-180">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-180">Attribute</span></span>                   | <span data-ttu-id="f3d55-181">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f3d55-181">Identifier</span></span>                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d55-182">**HorizontalTextAlignment**</span><span class="sxs-lookup"><span data-stu-id="f3d55-182">**HorizontalTextAlignment**</span></span> | [<span data-ttu-id="f3d55-183">**UIA \_ horizontaltextalignmentattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-183">**UIA\_HorizontalTextAlignmentAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="f3d55-184">**Indentationfirstline**</span><span class="sxs-lookup"><span data-stu-id="f3d55-184">**IndentationFirstLine**</span></span>    | [<span data-ttu-id="f3d55-185">**UIA \_ indentationfirstlineattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-185">**UIA\_IndentationFirstLineAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="f3d55-186">**Indentationleading**</span><span class="sxs-lookup"><span data-stu-id="f3d55-186">**IndentationLeading**</span></span>      | [<span data-ttu-id="f3d55-187">**UIA \_ indentationleadingattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-187">**UIA\_IndentationLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="f3d55-188">**Indentationtrailing**</span><span class="sxs-lookup"><span data-stu-id="f3d55-188">**IndentationTrailing**</span></span>     | [<span data-ttu-id="f3d55-189">**UIA \_ indentationtrailingattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-189">**UIA\_IndentationTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="f3d55-190">**Registerkarten**</span><span class="sxs-lookup"><span data-stu-id="f3d55-190">**Tabs**</span></span>                    | [<span data-ttu-id="f3d55-191">**UIA \_ tabsattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-191">**UIA\_TabsAttributeId**</span></span>](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a><span data-ttu-id="f3d55-192">Textfarbattribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-192">Text Color Attributes</span></span>

<span data-ttu-id="f3d55-193">Die Vordergrund-und Hintergrund Textfarben sind über die folgenden Text Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3d55-193">The foreground and background text colors are available through the following text attributes.</span></span> <span data-ttu-id="f3d55-194">Beide Farben werden als [**COLORREF**](/windows/desktop/gdi/colorref) -Datentyp angegeben.</span><span class="sxs-lookup"><span data-stu-id="f3d55-194">Both colors are specified as a [**COLORREF**](/windows/desktop/gdi/colorref) data type.</span></span>



| <span data-ttu-id="f3d55-195">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-195">Attribute</span></span>           | <span data-ttu-id="f3d55-196">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f3d55-196">Identifier</span></span>                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d55-197">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="f3d55-197">**BackgroundColor**</span></span> | [<span data-ttu-id="f3d55-198">**UIA \_ backgroundcolorattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-198">**UIA\_BackgroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="f3d55-199">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="f3d55-199">**ForegroundColor**</span></span> | [<span data-ttu-id="f3d55-200">**UIA \_ foregroundcolorattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-200">**UIA\_ForegroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a><span data-ttu-id="f3d55-201">Attribute für die Text Dekoration</span><span class="sxs-lookup"><span data-stu-id="f3d55-201">Text Decoration Attributes</span></span>

<span data-ttu-id="f3d55-202">Text Dekorationen enthalten Bereiche wie z. b. Aufzählungs Zeichen, Unterstreichung und Animationen.</span><span class="sxs-lookup"><span data-stu-id="f3d55-202">Text decorations include areas such as bullets, underlining, and animations.</span></span> <span data-ttu-id="f3d55-203">Wenn Text führende Aufzählungen oder Ziffern enthält, sollte das Symbol oder der Text, der für die Aufzählungs Zeichen oder die Zahl verwendet wird, ggf. im Textstream enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="f3d55-203">If text includes leading bullets or numbers, the symbol or text used for the bullet or number should be included in the text stream, if applicable.</span></span>

<span data-ttu-id="f3d55-204">Informationen zu Text Dekorationen sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3d55-204">Information about text decorations is available through the following attributes.</span></span>



| <span data-ttu-id="f3d55-205">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-205">Attribute</span></span>              | <span data-ttu-id="f3d55-206">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f3d55-206">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d55-207">**AnimationStyle**</span><span class="sxs-lookup"><span data-stu-id="f3d55-207">**AnimationStyle**</span></span>     | [<span data-ttu-id="f3d55-208">**UIA \_ animationstyleattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-208">**UIA\_AnimationStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="f3d55-209">**Kugel Stil**</span><span class="sxs-lookup"><span data-stu-id="f3d55-209">**BulletStyle**</span></span>        | [<span data-ttu-id="f3d55-210">**UIA \_ -"bulletstyleattributeid"**</span><span class="sxs-lookup"><span data-stu-id="f3d55-210">**UIA\_BulletStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)               |
| <span data-ttu-id="f3d55-211">**OutlineStyles**</span><span class="sxs-lookup"><span data-stu-id="f3d55-211">**OutlineStyles**</span></span>      | [<span data-ttu-id="f3d55-212">**UIA \_ outlinestylesattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-212">**UIA\_OutlineStylesAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="f3d55-213">**OverlineColor**</span><span class="sxs-lookup"><span data-stu-id="f3d55-213">**OverlineColor**</span></span>      | [<span data-ttu-id="f3d55-214">**UIA \_ overlinecolorattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-214">**UIA\_OverlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="f3d55-215">**OverlineStyle**</span><span class="sxs-lookup"><span data-stu-id="f3d55-215">**OverlineStyle**</span></span>      | [<span data-ttu-id="f3d55-216">**UIA \_ overlinestyleattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-216">**UIA\_OverlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="f3d55-217">**StrikeThrough-Farbe**</span><span class="sxs-lookup"><span data-stu-id="f3d55-217">**StrikethroughColor**</span></span> | [<span data-ttu-id="f3d55-218">**UIA \_ StrikeThrough colorattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-218">**UIA\_StrikethroughColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="f3d55-219">**StrikeThrough-Stil**</span><span class="sxs-lookup"><span data-stu-id="f3d55-219">**StrikethroughStyle**</span></span> | [<span data-ttu-id="f3d55-220">**UIA \_ -Strip Item-Funktion**</span><span class="sxs-lookup"><span data-stu-id="f3d55-220">**UIA\_StrikethroughStyleAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="f3d55-221">**Unterlinecolor**</span><span class="sxs-lookup"><span data-stu-id="f3d55-221">**UnderlineColor**</span></span>     | [<span data-ttu-id="f3d55-222">**UIA \_ underlinecolorattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-222">**UIA\_UnderlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="f3d55-223">**Unterlinestyle**</span><span class="sxs-lookup"><span data-stu-id="f3d55-223">**UnderlineStyle**</span></span>     | [<span data-ttu-id="f3d55-224">**UIA \_ underlinestyleattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-224">**UIA\_UnderlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a><span data-ttu-id="f3d55-225">Textstilattribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-225">Text Style Attributes</span></span>

<span data-ttu-id="f3d55-226">Informationen zu Textformaten sind auch über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3d55-226">Information about text styles is available though the following attributes.</span></span>



| <span data-ttu-id="f3d55-227">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-227">Attribute</span></span>         | <span data-ttu-id="f3d55-228">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f3d55-228">Identifier</span></span>                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d55-229">**CapStyle**</span><span class="sxs-lookup"><span data-stu-id="f3d55-229">**CapStyle**</span></span>      | [<span data-ttu-id="f3d55-230">**UIA \_ capstyleattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-230">**UIA\_CapStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="f3d55-231">**IsHidden**</span><span class="sxs-lookup"><span data-stu-id="f3d55-231">**IsHidden**</span></span>      | [<span data-ttu-id="f3d55-232">**UIA- \_ ishiddenattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-232">**UIA\_IsHiddenAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="f3d55-233">**IsItalic**</span><span class="sxs-lookup"><span data-stu-id="f3d55-233">**IsItalic**</span></span>      | [<span data-ttu-id="f3d55-234">**UIA \_ isitali| tributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-234">**UIA\_IsItalicAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="f3d55-235">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="f3d55-235">**IsReadOnly**</span></span>    | [<span data-ttu-id="f3d55-236">**UIA \_ isumlyattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-236">**UIA\_IsReadOnlyAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="f3d55-237">**IsSuperscript**</span><span class="sxs-lookup"><span data-stu-id="f3d55-237">**IsSuperscript**</span></span> | [<span data-ttu-id="f3d55-238">**UIA \_ issuperscriptattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-238">**UIA\_IsSuperscriptAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="f3d55-239">**Isabonniert**</span><span class="sxs-lookup"><span data-stu-id="f3d55-239">**IsSubscript**</span></span>   | [<span data-ttu-id="f3d55-240">**UIA \_ isabonptattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-240">**UIA\_IsSubscriptAttributeId**</span></span>](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a><span data-ttu-id="f3d55-241">Interaktions-und Auswahl Attribute</span><span class="sxs-lookup"><span data-stu-id="f3d55-241">Interaction and Selection Attributes</span></span>

<span data-ttu-id="f3d55-242">Informationen zur aktuellen Textauswahl im Bereich Bereich und Fokus sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3d55-242">Information about current text selection in the range and focus state is available though the following attributes.</span></span>



| <span data-ttu-id="f3d55-243">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3d55-243">Attribute</span></span>              | <span data-ttu-id="f3d55-244">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f3d55-244">Identifier</span></span>                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d55-245">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="f3d55-245">**IsActive**</span></span>           | [<span data-ttu-id="f3d55-246">**UIA \_ isactiveattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-246">**UIA\_IsActiveAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="f3d55-247">**Selectionactiveend**</span><span class="sxs-lookup"><span data-stu-id="f3d55-247">**SelectionActiveEnd**</span></span> | [<span data-ttu-id="f3d55-248">**UIA \_ selectionactiveendattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-248">**UIA\_SelectionActiveEndAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="f3d55-249">**CaretPosition**</span><span class="sxs-lookup"><span data-stu-id="f3d55-249">**CaretPosition**</span></span>      | [<span data-ttu-id="f3d55-250">**UIA \_ caretpositionattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-250">**UIA\_CaretPositionAttributeId**</span></span>](uiauto-textattribute-ids.md)      |
| <span data-ttu-id="f3d55-251">**Caretbidimode**</span><span class="sxs-lookup"><span data-stu-id="f3d55-251">**CaretBidiMode**</span></span>      | [<span data-ttu-id="f3d55-252">**UIA \_ caretbidimodeattributeid**</span><span class="sxs-lookup"><span data-stu-id="f3d55-252">**UIA\_CaretBidiModeAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a><span data-ttu-id="f3d55-253">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3d55-253">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f3d55-254">**Licher**</span><span class="sxs-lookup"><span data-stu-id="f3d55-254">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f3d55-255">Informationen zu Benutzeroberflächenautomatisierungs-Text und TextRange-Steuerelement Mustern</span><span class="sxs-lookup"><span data-stu-id="f3d55-255">About the UI Automation Text and TextRange Control Patterns</span></span>](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[<span data-ttu-id="f3d55-256">Text-und TextRange-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="f3d55-256">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="f3d55-257">Arbeiten mit Text basierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="f3d55-257">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 