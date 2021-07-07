---
title: Benutzeroberflächenautomatisierung Textattribute
description: In diesem Thema wird beschrieben, wie Microsoft Benutzeroberflächenautomatisierung die Format- und Stileigenschaften (Textattribute) von Textinhalten verfügbar macht und eine Liste der unterstützten Textattribute enthält.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- Benutzeroberflächenautomatisierung,Textattribute
- Textattribute,About
- Textattribute,Variant-Typen
- Textattribute,Datentypen
- Benutzeroberflächenautomatisierung,Liste der Attribute
- Benutzeroberflächenautomatisierung,Liste der Textattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8ae2d51a222e3833d0dd95fa6c048114a370a6
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353623"
---
# <a name="ui-automation-text-attributes"></a><span data-ttu-id="0d859-109">Benutzeroberflächenautomatisierung Textattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-109">UI Automation Text Attributes</span></span>

<span data-ttu-id="0d859-110">In diesem Thema wird beschrieben, wie Microsoft Benutzeroberflächenautomatisierung die Format- und Formateigenschaften *(* Textattribute ) von Textinhalten verfügbar macht und eine Liste der unterstützten Textattribute enthält.</span><span class="sxs-lookup"><span data-stu-id="0d859-110">This topic describes how Microsoft UI Automation exposes the format and style properties (*text attributes*) of textual content, and provides a list of supported text attributes.</span></span>

<span data-ttu-id="0d859-111">Benutzeroberflächenautomatisierung anbieter machen Textattribute über die [**Methoden GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) und [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) des [TextRange-Steuerelementmusters](uiauto-about-text-and-textrange-patterns.md) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d859-111">UI Automation providers expose text attributes through the [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) and [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) methods of the [TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern.</span></span> <span data-ttu-id="0d859-112">Clientanwendungen verwenden die [**IUIAutomationTextRange::GetAttributeValue-Methode,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) um den Wert eines bestimmten Textattributs für einen Textbereich abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0d859-112">Client applications use the [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) method to retrieve the value of a particular text attribute for a text range.</span></span> <span data-ttu-id="0d859-113">Clients können die [**IUIAutomationTextRange::FindAttribute-Methode verwenden,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) um einen Textbereich nach Text zu durchsuchen, der über ein bestimmtes Attribut verfügt.</span><span class="sxs-lookup"><span data-stu-id="0d859-113">Clients can use the [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) method to search a text range for text that has a particular attribute.</span></span> <span data-ttu-id="0d859-114">Wenn übereinstimmenden Text gefunden wird, erstellt die Methode einen neuen Textbereich, der den übereinstimmenden Text enthält.</span><span class="sxs-lookup"><span data-stu-id="0d859-114">If any matching text is found, the method creates a new text range that contains the matching text.</span></span>

<span data-ttu-id="0d859-115">Die Textattribute in der folgenden Liste werden vom **TextRange-Steuerelementmuster** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d859-115">The text attributes in the following list are supported by the **TextRange** control pattern.</span></span> <span data-ttu-id="0d859-116">Die Attributnamen werden von den Benutzeroberflächenautomatisierung Textattributbezeichnern abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0d859-116">The attribute names are derived from the UI Automation text attribute identifiers.</span></span> <span data-ttu-id="0d859-117">Das **AnimationStyle-Attribut** wird beispielsweise von Clients als [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definiert in Uiautomationclient.h) und von Anbietern als **Text \_ AnimationStyle \_ Attribute \_ GUID** (definiert in Uiautomationcoreapi.h) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0d859-117">For example, the **AnimationStyle** attribute is identified by clients as [**UIA\_AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (defined in Uiautomationclient.h) and by providers as **Text\_AnimationStyle\_Attribute\_GUID** (defined in Uiautomationcoreapi.h).</span></span> <span data-ttu-id="0d859-118">Weitere Informationen zu jedem unterstützten Textattribut finden Sie unter [**Textattributbezeichner**](uiauto-textattribute-ids.md).</span><span class="sxs-lookup"><span data-stu-id="0d859-118">For more information about each supported text attribute, see [**Text Attribute Identifiers**](uiauto-textattribute-ids.md).</span></span>

> [!Note]  
> <span data-ttu-id="0d859-119">Einige der aufgeführten Attribute werden ab Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0d859-119">Some of the attributes listed are supported starting with Windows 8.</span></span> <span data-ttu-id="0d859-120">Hinweise [**zur Versionsunterstützung finden**](uiauto-textattribute-ids.md) Sie unter Textattributbezeichner.</span><span class="sxs-lookup"><span data-stu-id="0d859-120">See [**Text Attribute Identifiers**](uiauto-textattribute-ids.md) for notes regarding version support.</span></span>

 

<span data-ttu-id="0d859-121">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="0d859-121">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="0d859-122">Anmerkungsattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-122">Annotation Attributes</span></span>](#annotation-attributes)
-   [<span data-ttu-id="0d859-123">Schriftartattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-123">Font Attributes</span></span>](#font-attributes)
-   [<span data-ttu-id="0d859-124">Sprachattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-124">Language Attributes</span></span>](#language-attributes)
-   [<span data-ttu-id="0d859-125">Linkattribut</span><span class="sxs-lookup"><span data-stu-id="0d859-125">Link Attribute</span></span>](#link-attribute)
-   [<span data-ttu-id="0d859-126">Seitenrandattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-126">Page Margin Attributes</span></span>](#page-margin-attributes)
-   [<span data-ttu-id="0d859-127">Textausrichtungsattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-127">Text Alignment Attributes</span></span>](#text-alignment-attributes)
-   [<span data-ttu-id="0d859-128">Textfarbattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-128">Text Color Attributes</span></span>](#text-color-attributes)
-   [<span data-ttu-id="0d859-129">Textdekorationsattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-129">Text Decoration Attributes</span></span>](#text-decoration-attributes)
-   [<span data-ttu-id="0d859-130">Textformatattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-130">Text Style Attributes</span></span>](#text-style-attributes)
-   [<span data-ttu-id="0d859-131">Interaktions- und Auswahlattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-131">Interaction and Selection Attributes</span></span>](#interaction-and-selection-attributes)
-   [<span data-ttu-id="0d859-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0d859-132">Related topics</span></span>](#related-topics)

## <a name="annotation-attributes"></a><span data-ttu-id="0d859-133">Anmerkungsattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-133">Annotation Attributes</span></span>

<span data-ttu-id="0d859-134">Anmerkungsobjekte und Anmerkungstypen sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d859-134">Annotation objects and annotation types are available through the following attributes.</span></span>



| <span data-ttu-id="0d859-135">attribute</span><span class="sxs-lookup"><span data-stu-id="0d859-135">Attribute</span></span>             | <span data-ttu-id="0d859-136">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0d859-136">Identifier</span></span>                                                            |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0d859-137">**AnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="0d859-137">**AnnotationObjects**</span></span> | [<span data-ttu-id="0d859-138">**UIA \_ AnnotationObjectsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-138">**UIA\_AnnotationObjectsAttributeId**</span></span>](uiauto-annotation-type-identifiers.md) |
| <span data-ttu-id="0d859-139">**AnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="0d859-139">**AnnotationTypes**</span></span>   | [<span data-ttu-id="0d859-140">**UIA \_ AnnotationTypesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-140">**UIA\_AnnotationTypesAttributeId**</span></span>](uiauto-annotation-type-identifiers.md)   |



 

## <a name="font-attributes"></a><span data-ttu-id="0d859-141">Schriftartattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-141">Font Attributes</span></span>

<span data-ttu-id="0d859-142">Der Name, die Größe und die Gewichtung einer Schriftart sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d859-142">The name, size, and weight of a font is available through the following attributes.</span></span>



| <span data-ttu-id="0d859-143">attribute</span><span class="sxs-lookup"><span data-stu-id="0d859-143">Attribute</span></span>      | <span data-ttu-id="0d859-144">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0d859-144">Identifier</span></span>                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d859-145">**FontName**</span><span class="sxs-lookup"><span data-stu-id="0d859-145">**FontName**</span></span>   | [<span data-ttu-id="0d859-146">**UIA \_ FontNameAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-146">**UIA\_FontNameAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="0d859-147">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="0d859-147">**FontSize**</span></span>   | [<span data-ttu-id="0d859-148">**UIA \_ FontSizeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-148">**UIA\_FontSizeAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="0d859-149">**Schriftbreite**</span><span class="sxs-lookup"><span data-stu-id="0d859-149">**FontWeight**</span></span> | [<span data-ttu-id="0d859-150">**UIA \_ FontWeightAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-150">**UIA\_FontWeightAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a><span data-ttu-id="0d859-151">Sprachattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-151">Language Attributes</span></span>

<span data-ttu-id="0d859-152">Informationen zur Sprache des Texts sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d859-152">Information about the language of the text is available through the following attributes.</span></span>



| <span data-ttu-id="0d859-153">attribute</span><span class="sxs-lookup"><span data-stu-id="0d859-153">Attribute</span></span>              | <span data-ttu-id="0d859-154">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0d859-154">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d859-155">**Kultur**</span><span class="sxs-lookup"><span data-stu-id="0d859-155">**Culture**</span></span>            | [<span data-ttu-id="0d859-156">**UIA \_ CultureAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-156">**UIA\_CultureAttributeId**</span></span>](uiauto-textattribute-ids.md)                       |
| <span data-ttu-id="0d859-157">**TextFlowDirections**</span><span class="sxs-lookup"><span data-stu-id="0d859-157">**TextFlowDirections**</span></span> | [<span data-ttu-id="0d859-158">**UIA \_ TextFlowDirectionsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-158">**UIA\_TextFlowDirectionsAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a><span data-ttu-id="0d859-159">Linkattribut</span><span class="sxs-lookup"><span data-stu-id="0d859-159">Link Attribute</span></span>

<span data-ttu-id="0d859-160">Das folgende Attribut stellt den Textbereich zur Auswahl, der das Ziel eines Links in einem Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="0d859-160">The following attribute provides the text range that is the target of a link in a document.</span></span>



| <span data-ttu-id="0d859-161">attribute</span><span class="sxs-lookup"><span data-stu-id="0d859-161">Attribute</span></span> | <span data-ttu-id="0d859-162">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0d859-162">Identifier</span></span>                                                                   |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="0d859-163">**Link**</span><span class="sxs-lookup"><span data-stu-id="0d859-163">**Link**</span></span>  | [<span data-ttu-id="0d859-164">**UIA \_ LinkAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-164">**UIA\_LinkAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a><span data-ttu-id="0d859-165">Seitenrandattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-165">Page Margin Attributes</span></span>

<span data-ttu-id="0d859-166">Die umgebundenen Rechtecke eines Textbereichs machen die Koordinaten des Texts auf der Seite nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d859-166">The bounding rectangles of a text range do not expose the coordinates of the text in the page.</span></span> <span data-ttu-id="0d859-167">Ein Anbieter kann die Seitenrandinformationen jedoch mithilfe der folgenden Textattribute verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="0d859-167">However, a provider can expose the page margin information using the following text attributes.</span></span>



| <span data-ttu-id="0d859-168">attribute</span><span class="sxs-lookup"><span data-stu-id="0d859-168">Attribute</span></span>          | <span data-ttu-id="0d859-169">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0d859-169">Identifier</span></span>                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d859-170">**MarginBottom**</span><span class="sxs-lookup"><span data-stu-id="0d859-170">**MarginBottom**</span></span>   | [<span data-ttu-id="0d859-171">**UIA \_ MarginBottomAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-171">**UIA\_MarginBottomAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="0d859-172">**MarginLeading**</span><span class="sxs-lookup"><span data-stu-id="0d859-172">**MarginLeading**</span></span>  | [<span data-ttu-id="0d859-173">**UIA \_ MarginLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-173">**UIA\_MarginLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)   |
| <span data-ttu-id="0d859-174">**MarginTop**</span><span class="sxs-lookup"><span data-stu-id="0d859-174">**MarginTop**</span></span>      | [<span data-ttu-id="0d859-175">**UIA \_ MarginTopAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-175">**UIA\_MarginTopAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0d859-176">**MarginTrailing**</span><span class="sxs-lookup"><span data-stu-id="0d859-176">**MarginTrailing**</span></span> | [<span data-ttu-id="0d859-177">**UIA \_ MarginTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-177">**UIA\_MarginTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a><span data-ttu-id="0d859-178">Textausrichtungsattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-178">Text Alignment Attributes</span></span>

<span data-ttu-id="0d859-179">Informationen zur Textausrichtung wie Einzug, Registerkarteneinstellungen und horizontale Ausrichtung sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d859-179">Information about text alignment such as indentation, tab settings, and horizontal alignment is available through the following attributes.</span></span>



| <span data-ttu-id="0d859-180">attribute</span><span class="sxs-lookup"><span data-stu-id="0d859-180">Attribute</span></span>                   | <span data-ttu-id="0d859-181">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0d859-181">Identifier</span></span>                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d859-182">**HorizontalTextAlignment**</span><span class="sxs-lookup"><span data-stu-id="0d859-182">**HorizontalTextAlignment**</span></span> | [<span data-ttu-id="0d859-183">**UIA \_ HorizontalTextAlignmentAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-183">**UIA\_HorizontalTextAlignmentAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0d859-184">**IndentationFirstLine**</span><span class="sxs-lookup"><span data-stu-id="0d859-184">**IndentationFirstLine**</span></span>    | [<span data-ttu-id="0d859-185">**UIA \_ IndentationFirstLineAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-185">**UIA\_IndentationFirstLineAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="0d859-186">**EinzugLeading**</span><span class="sxs-lookup"><span data-stu-id="0d859-186">**IndentationLeading**</span></span>      | [<span data-ttu-id="0d859-187">**UIA \_ IndentationLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-187">**UIA\_IndentationLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0d859-188">**EinzugTrailing**</span><span class="sxs-lookup"><span data-stu-id="0d859-188">**IndentationTrailing**</span></span>     | [<span data-ttu-id="0d859-189">**UIA \_ IndentationTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-189">**UIA\_IndentationTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="0d859-190">**Registerkarten**</span><span class="sxs-lookup"><span data-stu-id="0d859-190">**Tabs**</span></span>                    | [<span data-ttu-id="0d859-191">**UIA \_ TabsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-191">**UIA\_TabsAttributeId**</span></span>](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a><span data-ttu-id="0d859-192">Textfarbattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-192">Text Color Attributes</span></span>

<span data-ttu-id="0d859-193">Die Vordergrund- und Hintergrundtextfarben sind über die folgenden Textattribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d859-193">The foreground and background text colors are available through the following text attributes.</span></span> <span data-ttu-id="0d859-194">Beide Farben werden als [**COLORREF-Datentyp**](/windows/desktop/gdi/colorref) angegeben.</span><span class="sxs-lookup"><span data-stu-id="0d859-194">Both colors are specified as a [**COLORREF**](/windows/desktop/gdi/colorref) data type.</span></span>



| <span data-ttu-id="0d859-195">attribute</span><span class="sxs-lookup"><span data-stu-id="0d859-195">Attribute</span></span>           | <span data-ttu-id="0d859-196">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0d859-196">Identifier</span></span>                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d859-197">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="0d859-197">**BackgroundColor**</span></span> | [<span data-ttu-id="0d859-198">**UIA \_ BackgroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-198">**UIA\_BackgroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0d859-199">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="0d859-199">**ForegroundColor**</span></span> | [<span data-ttu-id="0d859-200">**UIA \_ ForegroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-200">**UIA\_ForegroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a><span data-ttu-id="0d859-201">Textdekorationsattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-201">Text Decoration Attributes</span></span>

<span data-ttu-id="0d859-202">Textdekorationen umfassen Bereiche wie Aufzählungszeichen, Unterstriche und Animationen.</span><span class="sxs-lookup"><span data-stu-id="0d859-202">Text decorations include areas such as bullets, underlining, and animations.</span></span> <span data-ttu-id="0d859-203">Wenn Text führende Aufzählungszeichen oder Zahlen enthält, sollte das Symbol oder der Text, der für das Aufzählungszeichen oder die Zahl verwendet wird, ggf. in den Textstream aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="0d859-203">If text includes leading bullets or numbers, the symbol or text used for the bullet or number should be included in the text stream, if applicable.</span></span>

<span data-ttu-id="0d859-204">Informationen zu Textdekorationen sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d859-204">Information about text decorations is available through the following attributes.</span></span>



| <span data-ttu-id="0d859-205">attribute</span><span class="sxs-lookup"><span data-stu-id="0d859-205">Attribute</span></span>              | <span data-ttu-id="0d859-206">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0d859-206">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d859-207">**AnimationStyle**</span><span class="sxs-lookup"><span data-stu-id="0d859-207">**AnimationStyle**</span></span>     | [<span data-ttu-id="0d859-208">**UIA \_ AnimationStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-208">**UIA\_AnimationStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="0d859-209">**Bulletstyle**</span><span class="sxs-lookup"><span data-stu-id="0d859-209">**BulletStyle**</span></span>        | [<span data-ttu-id="0d859-210">**UIA \_ BulletStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-210">**UIA\_BulletStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)               |
| <span data-ttu-id="0d859-211">**OutlineStyles**</span><span class="sxs-lookup"><span data-stu-id="0d859-211">**OutlineStyles**</span></span>      | [<span data-ttu-id="0d859-212">**UIA \_ OutlineStylesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-212">**UIA\_OutlineStylesAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0d859-213">**OverlineColor**</span><span class="sxs-lookup"><span data-stu-id="0d859-213">**OverlineColor**</span></span>      | [<span data-ttu-id="0d859-214">**UIA \_ OverlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-214">**UIA\_OverlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0d859-215">**OverlineStyle**</span><span class="sxs-lookup"><span data-stu-id="0d859-215">**OverlineStyle**</span></span>      | [<span data-ttu-id="0d859-216">**UIA \_ OverlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-216">**UIA\_OverlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0d859-217">**StrikethroughColor**</span><span class="sxs-lookup"><span data-stu-id="0d859-217">**StrikethroughColor**</span></span> | [<span data-ttu-id="0d859-218">**UIA \_ StrikethroughColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-218">**UIA\_StrikethroughColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0d859-219">**StrikethroughStyle**</span><span class="sxs-lookup"><span data-stu-id="0d859-219">**StrikethroughStyle**</span></span> | [<span data-ttu-id="0d859-220">**UIA \_ StrikethroughStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-220">**UIA\_StrikethroughStyleAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0d859-221">**UnderlineColor**</span><span class="sxs-lookup"><span data-stu-id="0d859-221">**UnderlineColor**</span></span>     | [<span data-ttu-id="0d859-222">**UIA \_ UnderlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-222">**UIA\_UnderlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="0d859-223">**UnderlineStyle**</span><span class="sxs-lookup"><span data-stu-id="0d859-223">**UnderlineStyle**</span></span>     | [<span data-ttu-id="0d859-224">**UIA \_ UnderlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-224">**UIA\_UnderlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a><span data-ttu-id="0d859-225">Textformatattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-225">Text Style Attributes</span></span>

<span data-ttu-id="0d859-226">Informationen zu Textformaten sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d859-226">Information about text styles is available though the following attributes.</span></span>



| <span data-ttu-id="0d859-227">attribute</span><span class="sxs-lookup"><span data-stu-id="0d859-227">Attribute</span></span>         | <span data-ttu-id="0d859-228">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0d859-228">Identifier</span></span>                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d859-229">**CapStyle**</span><span class="sxs-lookup"><span data-stu-id="0d859-229">**CapStyle**</span></span>      | [<span data-ttu-id="0d859-230">**UIA \_ CapStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-230">**UIA\_CapStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0d859-231">**IsHidden**</span><span class="sxs-lookup"><span data-stu-id="0d859-231">**IsHidden**</span></span>      | [<span data-ttu-id="0d859-232">**UIA \_ IsHiddenAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-232">**UIA\_IsHiddenAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0d859-233">**IsItalic**</span><span class="sxs-lookup"><span data-stu-id="0d859-233">**IsItalic**</span></span>      | [<span data-ttu-id="0d859-234">**UIA \_ IsItalicAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-234">**UIA\_IsItalicAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0d859-235">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="0d859-235">**IsReadOnly**</span></span>    | [<span data-ttu-id="0d859-236">**UIA \_ IsReadOnlyAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-236">**UIA\_IsReadOnlyAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="0d859-237">**IsSuperscript**</span><span class="sxs-lookup"><span data-stu-id="0d859-237">**IsSuperscript**</span></span> | [<span data-ttu-id="0d859-238">**UIA \_ IsSuperscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-238">**UIA\_IsSuperscriptAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0d859-239">**IsSubscript**</span><span class="sxs-lookup"><span data-stu-id="0d859-239">**IsSubscript**</span></span>   | [<span data-ttu-id="0d859-240">**UIA \_ IsSubscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-240">**UIA\_IsSubscriptAttributeId**</span></span>](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a><span data-ttu-id="0d859-241">Interaktions- und Auswahlattribute</span><span class="sxs-lookup"><span data-stu-id="0d859-241">Interaction and Selection Attributes</span></span>

<span data-ttu-id="0d859-242">Informationen zur aktuellen Textauswahl im Bereich und Fokuszustand sind über die folgenden Attribute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d859-242">Information about current text selection in the range and focus state is available though the following attributes.</span></span>



| <span data-ttu-id="0d859-243">attribute</span><span class="sxs-lookup"><span data-stu-id="0d859-243">Attribute</span></span>              | <span data-ttu-id="0d859-244">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0d859-244">Identifier</span></span>                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d859-245">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="0d859-245">**IsActive**</span></span>           | [<span data-ttu-id="0d859-246">**UIA \_ IsActiveAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-246">**UIA\_IsActiveAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0d859-247">**SelectionActiveEnd**</span><span class="sxs-lookup"><span data-stu-id="0d859-247">**SelectionActiveEnd**</span></span> | [<span data-ttu-id="0d859-248">**UIA \_ SelectionActiveEndAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-248">**UIA\_SelectionActiveEndAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0d859-249">**CaretPosition**</span><span class="sxs-lookup"><span data-stu-id="0d859-249">**CaretPosition**</span></span>      | [<span data-ttu-id="0d859-250">**UIA \_ CaretPositionAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-250">**UIA\_CaretPositionAttributeId**</span></span>](uiauto-textattribute-ids.md)      |
| <span data-ttu-id="0d859-251">**CaretBidiMode**</span><span class="sxs-lookup"><span data-stu-id="0d859-251">**CaretBidiMode**</span></span>      | [<span data-ttu-id="0d859-252">**UIA \_ CaretBidiModeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="0d859-252">**UIA\_CaretBidiModeAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a><span data-ttu-id="0d859-253">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d859-253">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0d859-254">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="0d859-254">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0d859-255">Informationen zu Benutzeroberflächenautomatisierung Text- und TextRange-Steuerelementmustern</span><span class="sxs-lookup"><span data-stu-id="0d859-255">About the UI Automation Text and TextRange Control Patterns</span></span>](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[<span data-ttu-id="0d859-256">Text- und TextRange-Steuerelementmuster</span><span class="sxs-lookup"><span data-stu-id="0d859-256">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="0d859-257">Arbeiten mit textbasierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="0d859-257">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 