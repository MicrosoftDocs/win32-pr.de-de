---
title: Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung
description: Benutzeroberflächenautomatisierungs-Steuerelement Typen sind Eigenschaften, die als bekannte Bezeichner fungieren, die die Art des Steuer Elements angeben, das ein bestimmtes UI-Element darstellt, z. b. ein Kombinations Feld oder eine Schaltfläche.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- UI-Automatisierung, Übersicht über Steuerelement Typen
- UI-Automatisierung, UIA_LocalizedControlTypePropertyId-Eigenschaft
- Steuerelement Typen, Info
- Steuerelement Typen, Voraussetzungen
- Steuerelement Typen, Voraussetzungen
- Steuerelement Typen, vordefiniert
- Steuerelement Typen, UIA_LocalizedControlTypePropertyId-Eigenschaft
- vordefinierte Steuerelement Typen
- UIA_LocalizedControlTypePropertyId-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516823"
---
# <a name="ui-automation-control-types-overview"></a><span data-ttu-id="c4dd5-112">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="c4dd5-112">UI Automation Control Types Overview</span></span>

<span data-ttu-id="c4dd5-113">Benutzeroberflächenautomatisierungs-Steuerelement Typen sind Eigenschaften, die als bekannte Bezeichner fungieren, die die Art des Steuer Elements angeben, das ein bestimmtes UI-Element darstellt, z. b. ein Kombinations Feld oder eine Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-113">Microsoft UI Automation control types are properties that serve as well-known identifiers that indicate the kind of control that a particular UI element represents, such as a combo box or a button.</span></span> <span data-ttu-id="c4dd5-114">Client Anwendungen verwenden den-Typ, um die Funktionen eines Steuer Elements zu identifizieren und zu bestimmen, wie mit ihm interagiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-114">Client applications use the type to identify the capabilities of a control and to determine how to interact with it.</span></span>

<span data-ttu-id="c4dd5-115">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="c4dd5-115">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="c4dd5-116">Anforderungen für Steuerelementtypen der Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="c4dd5-116">UI Automation Control Type Requisites</span></span>](#ui-automation-control-type-requisites)
-   [<span data-ttu-id="c4dd5-117">Die LocalizedControlType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c4dd5-117">The LocalizedControlType Property</span></span>](#the-localizedcontroltype-property)
-   [<span data-ttu-id="c4dd5-118">Aktuelle Steuerelementtypen der Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="c4dd5-118">Current UI Automation Control Types</span></span>](#current-ui-automation-control-types)
-   [<span data-ttu-id="c4dd5-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-119">Related topics</span></span>](#related-topics)

## <a name="ui-automation-control-type-requisites"></a><span data-ttu-id="c4dd5-120">Anforderungen für Steuerelementtypen der Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="c4dd5-120">UI Automation Control Type Requisites</span></span>

<span data-ttu-id="c4dd5-121">Jedem Benutzeroberflächenautomatisierungs-Steuerelement ist eine Reihe von Bedingungen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-121">Each UI Automation control type has a set of conditions associated with it.</span></span> <span data-ttu-id="c4dd5-122">Wenn ein Anbieter einem Steuerelement einen Steuerelement Typen zuweist, muss der Anbieter sicherstellen, dass das Steuerelement alle Bedingungen erfüllt, die diesem Steuerelement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-122">When a provider assigns a control type to a control, the provider must ensure that the control meets all of the conditions associated with that control type.</span></span> <span data-ttu-id="c4dd5-123">Die Bedingungen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c4dd5-123">The conditions include the following:</span></span>

-   <span data-ttu-id="c4dd5-124">Benutzeroberflächenautomatisierungs-Steuerelement Muster: jeder Steuer ungstyp verfügt über eine Reihe von Steuerelement Mustern, die vom Steuerelement unterstützt werden müssen, eine optionale Menge und eine Menge, die vom Steuerelement nicht unterstützt werden darf</span><span class="sxs-lookup"><span data-stu-id="c4dd5-124">UI Automation control patterns: Each control type has a set of control patterns that the control must support, a set that is optional, and a set that the control must not support.</span></span>
-   <span data-ttu-id="c4dd5-125">Eigenschaftswerte für die Benutzeroberflächenautomatisierung: Jeder Steuerelementtyp hat einen Satz von Eigenschaften, die das Steuerelement unterstützen muss.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-125">UI Automation property values: Each control type has a set of properties that the control must support.</span></span>
-   <span data-ttu-id="c4dd5-126">Ereignisse für die Benutzeroberflächenautomatisierung: Jeder Steuerelementtyp hat einen Satz von Ereignissen, die das Steuerelement unterstützen muss.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-126">UI Automation events: Each control type has a set of events that the control must support.</span></span>
-   <span data-ttu-id="c4dd5-127">Baumstruktur der Benutzeroberflächenautomatisierung: Jeder Steuerelementtyp definiert, wie das Steuerelement in der Baumstruktur der Benutzeroberflächenautomatisierung dargestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-127">UI Automation tree structure: Each control type defines how the control must appear in the UI Automation tree structure.</span></span>

<span data-ttu-id="c4dd5-128">Wenn ein Steuerelement die Bedingungen für einen bestimmten Steuer Elementtyp erfüllt, gibt der [**iuiautomationelement:: currentcontroltype**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (oder der [**iuiautomationelement:: cachedcontroltype**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype))-Eigenschafts Wert diesen Steuer Elementtyp an.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-128">When a control meets the conditions for a particular control type, the [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (or [**IUIAutomationElement::CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) property value will indicate that control type.</span></span>

<span data-ttu-id="c4dd5-129">Wenn das Steuerelement die Spezifikationen für einen bestimmten Steuer Elementtyp nicht erfüllt, verwenden Sie [**UIA \_ customcontroltypeid**](uiauto-controltype-ids.md) als Steuer Elementtyp-ID, und beschreiben Sie das Steuerelement vollständig, indem Sie die entsprechenden Steuerelement Muster und-Eigenschaften verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-129">If your control does not meet the specifications for a particular control type, use [**UIA\_CustomControlTypeId**](uiauto-controltype-ids.md) as the control type ID, and completely describe the control by using the relevant control patterns and properties.</span></span> <span data-ttu-id="c4dd5-130">Sie können auch die [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft auf eine Zeichenfolge festlegen, die den Typ des Steuer Elements am besten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-130">You can also set the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property to a string that best describes the type of your control.</span></span>

## <a name="the-localizedcontroltype-property"></a><span data-ttu-id="c4dd5-131">Die LocalizedControlType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c4dd5-131">The LocalizedControlType Property</span></span>

<span data-ttu-id="c4dd5-132">Wenn Sie ein vordefiniertes Steuerelement für die Beschreibung des Steuer Elements verwenden, verwenden Sie den Standardwert für die [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft, und lassen Sie die Benutzeroberflächen Automatisierung eine lokalisierte Zeichenfolge bereit, die Anbieter ordnungsgemäß verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-132">If you use a predefined control type to describe your control, use the default value for the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property and allow UI Automation to provide a localized string for providers to expose properly.</span></span> <span data-ttu-id="c4dd5-133">Wenn Sie das Steuerelement nicht mithilfe eines vordefinierten Steuerelement Typs beschreiben können, legen Sie die Eigenschaft **UIA \_ localizedcontroltypepropertyid** auf eine lokalisierte Zeichenfolge fest, die den Typ des Steuer Elements exakt beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-133">If you cannot use a predefined control type to describe your control, set the **UIA\_LocalizedControlTypePropertyId** property to a localized string that accurately describes the type of your control.</span></span> <span data-ttu-id="c4dd5-134">Die Zeichenfolge sollte präzise, aber genau genug sein, damit eine Hilfstechnologie wie z. b. eine Sprachausgabe in der Benutzeroberfläche den Benutzer über den Typ des Steuer Elements informieren kann.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-134">The string should be concise, yet accurate enough that an assistive technology such as a screen reader can use it in the UI to inform the user of the control's type.</span></span>

## <a name="current-ui-automation-control-types"></a><span data-ttu-id="c4dd5-135">Aktuelle Steuerelementtypen der Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="c4dd5-135">Current UI Automation Control Types</span></span>

<span data-ttu-id="c4dd5-136">In den folgenden Themen werden die Steuerelement Typen der Benutzeroberflächen Automatisierung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c4dd5-136">The following topics describe the UI Automation control types.</span></span> <span data-ttu-id="c4dd5-137">Für jeden Steuerelement Typ enthält die Beschreibung den Satz von Bedingungen, die ein Steuerelement vom angegebenen Typ unterstützen muss:</span><span class="sxs-lookup"><span data-stu-id="c4dd5-137">For each control type, the description includes the set of conditions that a control of the given type must support:</span></span>

-   <span data-ttu-id="c4dd5-138">Appbar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-138">AppBar Control Type</span></span>
-   [<span data-ttu-id="c4dd5-139">Button-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-139">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="c4dd5-140">Typ des Kalender Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="c4dd5-140">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="c4dd5-141">CheckBox-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-141">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="c4dd5-142">ComboBox-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-142">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="c4dd5-143">DataGrid-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-143">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="c4dd5-144">DataItem-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-144">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="c4dd5-145">Dokument Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="c4dd5-145">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="c4dd5-146">Steuerelement-Typ bearbeiten</span><span class="sxs-lookup"><span data-stu-id="c4dd5-146">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="c4dd5-147">Gruppen Steuerungstyp</span><span class="sxs-lookup"><span data-stu-id="c4dd5-147">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="c4dd5-148">Header Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="c4dd5-148">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="c4dd5-149">Header Item-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c4dd5-149">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="c4dd5-150">Hyperlink-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-150">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="c4dd5-151">Bild Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="c4dd5-151">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="c4dd5-152">List-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-152">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="c4dd5-153">ListItem-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c4dd5-153">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="c4dd5-154">Menu-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-154">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="c4dd5-155">MenuBar-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c4dd5-155">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="c4dd5-156">MenuItem-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c4dd5-156">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="c4dd5-157">Pane-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-157">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="c4dd5-158">ProgressBar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-158">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="c4dd5-159">RadioButton-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c4dd5-159">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="c4dd5-160">ScrollBar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-160">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="c4dd5-161">Typ des semanticzoom-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="c4dd5-161">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="c4dd5-162">Separator-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-162">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="c4dd5-163">Slider-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-163">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="c4dd5-164">Spinner-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-164">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="c4dd5-165">SplitButton-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c4dd5-165">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="c4dd5-166">StatusBar-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c4dd5-166">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="c4dd5-167">Register Steuerungstyp</span><span class="sxs-lookup"><span data-stu-id="c4dd5-167">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="c4dd5-168">TabItem-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c4dd5-168">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="c4dd5-169">Table-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-169">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="c4dd5-170">Text Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="c4dd5-170">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="c4dd5-171">Thumb-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c4dd5-171">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="c4dd5-172">TitleBar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-172">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="c4dd5-173">ToolBar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-173">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="c4dd5-174">ToolTip-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-174">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="c4dd5-175">Struktur Steuerungstyp</span><span class="sxs-lookup"><span data-stu-id="c4dd5-175">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="c4dd5-176">TreeItem-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-176">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="c4dd5-177">Fenster Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="c4dd5-177">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="c4dd5-178">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4dd5-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c4dd5-179">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="c4dd5-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c4dd5-180">Steuerelement-Typbezeichner</span><span class="sxs-lookup"><span data-stu-id="c4dd5-180">Control Type Identifiers</span></span>](uiauto-controltype-ids.md)
</dt> <dt>

<span data-ttu-id="c4dd5-181">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c4dd5-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c4dd5-182">Unterstützen der Benutzeroberflächenautomatisierungs</span><span class="sxs-lookup"><span data-stu-id="c4dd5-182">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[<span data-ttu-id="c4dd5-183">Benutzeroberflächenautomatisierungs-Unterstützung für Standardsteuerelemente</span><span class="sxs-lookup"><span data-stu-id="c4dd5-183">UI Automation Support for Standard Controls</span></span>](uiauto-controlsupport.md)
</dt> <dt>

[<span data-ttu-id="c4dd5-184">Grundlagen der Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="c4dd5-184">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 