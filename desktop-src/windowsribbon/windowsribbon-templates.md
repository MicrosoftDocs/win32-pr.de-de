---
title: Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien
description: Steuerelemente, die auf der Menüband-Befehlsleiste gehostet werden, unterliegen Layoutregeln, die vom Windows-Menübandframework erzwungen werden und auf einer Kombination aus Standardverhalten und Layoutvorlagen (sowohl frameworkdefiniert als auch benutzerdefiniert) basieren, wie im Menübandmarkup deklariert. Diese Regeln definieren das adaptive Layoutverhalten des Menübandframework, das beeinflusst, wie steuerelemente in der Befehlsleiste zur Laufzeit an verschiedene Menübandgrößen angepasst werden.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Windows-Menüband, Anpassen
- Menüband,Anpassen
- Windows-Menüband, SizeDefinition-Vorlagen
- Menüband, SizeDefinition-Vorlagen
- Windows-Menüband, benutzerdefinierte Vorlagen
- Menüband, benutzerdefinierte Vorlagen
- Anpassen des Windows-Menübands
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6576a672aa8c3d328a341370a7568595e988908
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444141"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a><span data-ttu-id="9f47e-111">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="9f47e-111">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>

<span data-ttu-id="9f47e-112">Steuerelemente, die auf der Menüband-Befehlsleiste gehostet werden, unterliegen Layoutregeln, die vom Windows-Menübandframework erzwungen werden und auf einer Kombination aus Standardverhalten und Layoutvorlagen (sowohl frameworkdefiniert als auch benutzerdefiniert) basieren, wie im Menübandmarkup deklariert.</span><span class="sxs-lookup"><span data-stu-id="9f47e-112">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Windows Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="9f47e-113">Diese Regeln definieren das adaptive Layoutverhalten des Menübandframework, das beeinflusst, wie steuerelemente in der Befehlsleiste zur Laufzeit an verschiedene Menübandgrößen angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="9f47e-113">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

-   [<span data-ttu-id="9f47e-114">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="9f47e-114">Introduction</span></span>](#introduction)
    -   [<span data-ttu-id="9f47e-115">MenübandgrößeDefinitionsvorlagen</span><span class="sxs-lookup"><span data-stu-id="9f47e-115">Ribbon SizeDefinition Templates</span></span>](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [<span data-ttu-id="9f47e-116">Benutzerdefinierte Vorlagen</span><span class="sxs-lookup"><span data-stu-id="9f47e-116">Custom Templates</span></span>](#custom-templates)
-   [<span data-ttu-id="9f47e-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9f47e-117">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="9f47e-118">Einführung</span><span class="sxs-lookup"><span data-stu-id="9f47e-118">Introduction</span></span>

<span data-ttu-id="9f47e-119">Adaptives Layout, wie durch das Menübandframework definiert, ist die Fähigkeit aller Steuerelemente auf der Menübandbenutzeroberfläche, ihre Organisation, Größe, Format und relative Skalierung basierend auf Änderungen an der Größe des Menübands zur Laufzeit dynamisch anzupassen.</span><span class="sxs-lookup"><span data-stu-id="9f47e-119">Adaptive layout, as defined by the Ribbon framework, is the ability of all controls within the ribbon UI to dynamically adjust their organization, size, format, and relative scale based on changes to the size of the ribbon at run time.</span></span>

<span data-ttu-id="9f47e-120">Das Framework macht adaptive Layoutfunktionen über eine Reihe von Markupelementen verfügbar, die für das Angeben und Anpassen verschiedener Layoutverhaltensverhalten dediert sind.</span><span class="sxs-lookup"><span data-stu-id="9f47e-120">The framework exposes adaptive layout functionality through a set of markup elements that are dedicated to specifying and customizing various layout behaviors.</span></span> <span data-ttu-id="9f47e-121">Eine Sammlung von Vorlagen namens [**SizeDefinitions**](windowsribbon-element-sizedefinition.md)wird durch das Framework definiert, von denen jede verschiedene Steuerelement- und Layoutszenarien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-121">A collection of templates, called [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), is defined by the framework, each of which support various control and layout scenarios.</span></span> <span data-ttu-id="9f47e-122">Das Framework unterstützt jedoch auch benutzerdefinierte Vorlagen, wenn die vordefinierten Vorlagen nicht die Benutzeroberflächenerfahrung oder layouts bereitstellen, die für eine Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f47e-122">However, the framework also supports custom templates should the predefined templates not provide the UI experience or layouts required by an application.</span></span>

<span data-ttu-id="9f47e-123">Um Steuerelemente in einem bevorzugten Layout mit einer bestimmten Menübandgröße anzuzeigen, funktionieren sowohl vordefinierte Vorlagen als auch benutzerdefinierte Vorlagen in Verbindung mit dem [**ScalingPolicy-Element.**](windowsribbon-element-scalingpolicy.md)</span><span class="sxs-lookup"><span data-stu-id="9f47e-123">To display controls in a preferred layout at a particular ribbon size, both predefined templates and custom templates work in conjunction with the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element.</span></span> <span data-ttu-id="9f47e-124">Dieses Element enthält ein Manifest der Größeneinstellungen, die das Framework beim Rendern des Menübands als Leitfaden verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f47e-124">This element contains a manifest of size preferences that the framework uses as a guide when rendering the ribbon.</span></span>

> [!Note]  
> <span data-ttu-id="9f47e-125">Das Menübandframework bietet Standardlayoutverhalten, das auf einer Reihe integrierter Heuristiken für die Organisation und Darstellung von Steuerelementen zur Laufzeit basiert, ohne dass die [**vordefinierten SizeDefinition-Vorlagen benötigt**](windowsribbon-element-sizedefinition.md) werden.</span><span class="sxs-lookup"><span data-stu-id="9f47e-125">The Ribbon framework provides default layout behaviors based on a set of built-in heuristics for the organization and presentation of controls at run time without the need for the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span> <span data-ttu-id="9f47e-126">Diese Funktion ist jedoch nur für Prototypzwecke vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="9f47e-126">However, this capability is intended for prototyping purposes only.</span></span>

 

### <a name="ribbon-sizedefinition-templates"></a><span data-ttu-id="9f47e-127">MenübandgrößeDefinitionsvorlagen</span><span class="sxs-lookup"><span data-stu-id="9f47e-127">Ribbon SizeDefinition Templates</span></span>

<span data-ttu-id="9f47e-128">Das Menübandframework bietet einen umfassenden Satz von [**SizeDefinition-Vorlagen,**](windowsribbon-element-sizedefinition.md) die Größe und Layoutverhalten für eine Gruppe von Menüband-Steuerelementen angeben. [](windowsribbon-controls-group.md)</span><span class="sxs-lookup"><span data-stu-id="9f47e-128">The Ribbon framework provides a comprehensive set of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates that specify size and layout behavior for a [Group](windowsribbon-controls-group.md) of Ribbon controls.</span></span> <span data-ttu-id="9f47e-129">Diese Vorlagen decken die gängigsten Szenarien zum Organisieren von Steuerelementen in einer Menübandanwendung ab.</span><span class="sxs-lookup"><span data-stu-id="9f47e-129">These templates cover most common scenarios for organizing controls in a Ribbon application.</span></span>

<span data-ttu-id="9f47e-130">Um eine konsistente Benutzeroberfläche für Menübandanwendungen zu erzwingen, erzwingt jede [**SizeDefinition-Vorlage**](windowsribbon-element-sizedefinition.md) Einschränkungen für die Steuerelemente oder die Von ihr unterstützten Steuerelementfamilien.</span><span class="sxs-lookup"><span data-stu-id="9f47e-130">To enforce a consistent user experience across Ribbon applications, each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template imposes restrictions on the controls or the family of controls it supports.</span></span>

<span data-ttu-id="9f47e-131">Die Schaltflächenfamilie von Steuerelementen umfasst beispielsweise Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9f47e-131">For example, the button family of controls includes:</span></span>

-   <span data-ttu-id="9f47e-132">[Button](windowsribbon-controls-button.md) (Schaltfläche)</span><span class="sxs-lookup"><span data-stu-id="9f47e-132">[Button](windowsribbon-controls-button.md)</span></span>
-   [<span data-ttu-id="9f47e-133">Umschaltfläche</span><span class="sxs-lookup"><span data-stu-id="9f47e-133">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)
-   [<span data-ttu-id="9f47e-134">Dropdownschaltfläche</span><span class="sxs-lookup"><span data-stu-id="9f47e-134">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)
-   [<span data-ttu-id="9f47e-135">Schaltfläche "Teilen"</span><span class="sxs-lookup"><span data-stu-id="9f47e-135">Split Button</span></span>](windowsribbon-controls-splitbutton.md)
-   [<span data-ttu-id="9f47e-136">Dropdownkatalog</span><span class="sxs-lookup"><span data-stu-id="9f47e-136">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
-   [<span data-ttu-id="9f47e-137">Split Button Gallery</span><span class="sxs-lookup"><span data-stu-id="9f47e-137">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
-   [<span data-ttu-id="9f47e-138">Dropdownliste Farbwähler</span><span class="sxs-lookup"><span data-stu-id="9f47e-138">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)

<span data-ttu-id="9f47e-139">Die Eingabefamilie von Steuerelementen umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9f47e-139">While the input family of controls includes:</span></span>

-   [<span data-ttu-id="9f47e-140">Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="9f47e-140">Combo Box</span></span>](windowsribbon-controls-combobox.md)
-   [<span data-ttu-id="9f47e-141">Spinner</span><span class="sxs-lookup"><span data-stu-id="9f47e-141">Spinner</span></span>](windowsribbon-controls-spinner.md)

<span data-ttu-id="9f47e-142">[Kontrollkästchen und](windowsribbon-controls-checkbox.md) [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) gehören weder zur Schaltflächenfamilie noch zur Eingabefamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-142">[Check Box](windowsribbon-controls-checkbox.md) and [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) do not belong to either the button family or the input family.</span></span> <span data-ttu-id="9f47e-143">Diese beiden Steuerelemente können nur verwendet werden, wenn sie explizit in einer [**SizeDefinition-Vorlage angegeben**](windowsribbon-element-sizedefinition.md) sind.</span><span class="sxs-lookup"><span data-stu-id="9f47e-143">These two controls can be used only where explicitly indicated in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

<span data-ttu-id="9f47e-144">Im Folgenden finden Sie eine Liste der [**SizeDefinition-Vorlagen**](windowsribbon-element-sizedefinition.md) mit einer Beschreibung des Layouts und der Steuerelemente, die für jede Vorlage zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="9f47e-144">The following is a list of the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates with a description of the layout and controls allowed by each template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f47e-145">Wenn die im Markup deklarierten Steuerelemente nicht genau dem in der zugeordneten [](windowsribbon-compilationerrors.md) Vorlage definierten Steuerelementtyp, [](windowsribbon-intentcl.md) der Reihenfolge und der Menge zugeordnet sind, wird ein Validierungsfehler vom Markupcompiler protokolliert, und die Kompilierung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="9f47e-145">If the controls declared in markup do not map exactly to control type, order, and quantity defined in the associated template, a [validation error](windowsribbon-compilationerrors.md) is logged by the [markup compiler](windowsribbon-intentcl.md) and compilation is terminated.</span></span>

 



<span data-ttu-id="9f47e-146">OneButton</span><span class="sxs-lookup"><span data-stu-id="9f47e-146">OneButton</span></span>

<span data-ttu-id="9f47e-147">Ein Steuerelement der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-147">One button-family control.</span></span><br/> <span data-ttu-id="9f47e-148">Nur große Gruppen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-148">Only Large group size is supported.</span></span><br/>

![Abbildung der Vorlage "onebutton sizedefinition".](images/overviews/sizedefinition-onebutton.png)

<span data-ttu-id="9f47e-150">TwoButtons</span><span class="sxs-lookup"><span data-stu-id="9f47e-150">TwoButtons</span></span>

<span data-ttu-id="9f47e-151">Zwei Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-151">Two button-family controls.</span></span><br/> <span data-ttu-id="9f47e-152">Es werden nur die Gruppengrößen Groß und Mittel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-152">Only Large and Medium group sizes are supported.</span></span><br/>

![Abbildung der Vorlage "twobuttons large sizedefinition".](images/overviews/sizedefinition-twobuttons-large.png)

![Abbildung der Vorlage twobuttons medium sizedefinition.](images/overviews/sizedefinition-twobuttons-medium.png)

<span data-ttu-id="9f47e-155">ThreeButtons</span><span class="sxs-lookup"><span data-stu-id="9f47e-155">ThreeButtons</span></span>

<span data-ttu-id="9f47e-156">Drei Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-156">Three button-family controls.</span></span><br/> <span data-ttu-id="9f47e-157">Es werden nur die Gruppengrößen Groß und Mittel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-157">Only Large and Medium group sizes are supported.</span></span><br/>

![Abbildung der Vorlage "Threebuttons large sizedefinition".](images/overviews/sizedefinition-threebuttons-large.png)

![Abbildung der Vorlage "Threebuttons medium sizedefinition".](images/overviews/sizedefinition-threebuttons-medium.png)

<span data-ttu-id="9f47e-160">ThreeButtons-OneBigAndTwoSmall</span><span class="sxs-lookup"><span data-stu-id="9f47e-160">ThreeButtons-OneBigAndTwoSmall</span></span>

<span data-ttu-id="9f47e-161">Drei Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-161">Three button-family controls.</span></span><br/> <span data-ttu-id="9f47e-162">Die erste Schaltfläche wird in allen drei Größen deutlich dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-162">The first button is presented prominently in all three sizes.</span></span><br/>

![Abbildung der Vorlage threebuttons-onebigandtwosmall large sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![Abbildung der Vorlage threebuttons-onebigandtwosmall medium sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![Abbildung der Vorlage threebuttons-onebigandtwosmall small sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

<span data-ttu-id="9f47e-166">ThreeButtonsAndOneCheckBox</span><span class="sxs-lookup"><span data-stu-id="9f47e-166">ThreeButtonsAndOneCheckBox</span></span>

<span data-ttu-id="9f47e-167">Drei Steuerelemente der Schaltflächenfamilie, die von einem einzelnen CheckBox-Steuerelement begleitet werden.</span><span class="sxs-lookup"><span data-stu-id="9f47e-167">Three button-family controls accompanied by a single CheckBox control.</span></span><br/> <span data-ttu-id="9f47e-168">Es werden nur die Gruppengrößen Groß und Mittel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-168">Only Large and Medium group sizes are supported.</span></span><br/>

![Abbildung der Vorlage threebuttonsandonecheckbox large sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![Abbildung der Vorlage threebuttonsandonecheckbox medium sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

<span data-ttu-id="9f47e-171">FourButtons</span><span class="sxs-lookup"><span data-stu-id="9f47e-171">FourButtons</span></span>

<span data-ttu-id="9f47e-172">Vier Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-172">Four button-family controls.</span></span><br/>

![Abbildung der Vorlage "Fourbuttons large sizedefinition".](images/overviews/sizedefinition-fourbuttons-large.png)

![Abbildung der Vorlage "Fourbuttons medium sizedefinition".](images/overviews/sizedefinition-fourbuttons-medium.png)

![Abbildung der Small-SizeDefinition-Vorlage für vierButtons.](images/overviews/sizedefinition-fourbuttons-small.png)

<span data-ttu-id="9f47e-176">FiveButtons</span><span class="sxs-lookup"><span data-stu-id="9f47e-176">FiveButtons</span></span>

<span data-ttu-id="9f47e-177">Fünf Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-177">Five button-family controls.</span></span><br/>

![Abbildung der Vorlage "Fivebuttons large sizedefinition".](images/overviews/sizedefinition-fivebuttons-large.png)

![Abbildung der Vorlage fivebuttons medium sizedefinition.](images/overviews/sizedefinition-fivebuttons-medium.png)

![Abbildung der Small-SizeDefinition-Vorlage für fivebuttons.](images/overviews/sizedefinition-fivebuttons-small.png)

<span data-ttu-id="9f47e-181">FiveOrSixButtons</span><span class="sxs-lookup"><span data-stu-id="9f47e-181">FiveOrSixButtons</span></span>

<span data-ttu-id="9f47e-182">Fünf Steuerelemente der Schaltflächenfamilie und eine optionale sechste Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="9f47e-182">Five button-family controls and an optional sixth button.</span></span><br/>

![Abbildung der Vorlage "fiveorsixbuttons large sizedefinition".](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![Abbildung der Vorlage fiveorsixbuttons medium sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![Abbildung der Small SizeDefinition-Vorlage für fiveorsixbuttons.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

<span data-ttu-id="9f47e-186">SixButtons</span><span class="sxs-lookup"><span data-stu-id="9f47e-186">SixButtons</span></span>

<span data-ttu-id="9f47e-187">Sechs Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-187">Six button-family controls.</span></span><br/>

![Abbildung der Vorlage "large sizedefinition" von sixbuttons.](images/overviews/sizedefinition-sixbuttons-large.png)

![Abbildung der Vorlage "sixbuttons medium sizedefinition".](images/overviews/sizedefinition-sixbuttons-medium.png)

![Abbildung der Vorlage "Sixbuttons small sizedefinition".](images/overviews/sizedefinition-sixbuttons-small.png)

<span data-ttu-id="9f47e-191">SixButtons-TwoColumns</span><span class="sxs-lookup"><span data-stu-id="9f47e-191">SixButtons-TwoColumns</span></span>

<span data-ttu-id="9f47e-192">Sechs Steuerelemente der Schaltflächenfamilie (alternative Darstellung).</span><span class="sxs-lookup"><span data-stu-id="9f47e-192">Six button-family controls (alternate presentation).</span></span><br/>

![Abbildung der Vorlage "sixbuttons-twocolumns large sizedefinition".](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![sixbuttons-twocolumns medium sizedefinition template.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![Abbildung der Vorlage "sixbuttons-twocolumns small sizedefinition".](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

<span data-ttu-id="9f47e-196">SevenButtons</span><span class="sxs-lookup"><span data-stu-id="9f47e-196">SevenButtons</span></span>

<span data-ttu-id="9f47e-197">Sieben Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-197">Seven button-family controls.</span></span><br/>

![Abbildung der Vorlage "sevenbuttons large sizedefinition".](images/overviews/sizedefinition-sevenbuttons-large.png)

![Abbildung der Vorlage "sevenbuttons mediumsizedefinition".](images/overviews/sizedefinition-sevenbuttons-medium.png)

![Abbildung der Vorlage "Sevenbuttons small sizedefinition".](images/overviews/sizedefinition-sevenbuttons-small.png)

<span data-ttu-id="9f47e-201">EightButtons</span><span class="sxs-lookup"><span data-stu-id="9f47e-201">EightButtons</span></span>

<span data-ttu-id="9f47e-202">Acht Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-202">Eight button-family controls.</span></span><br/>

![Abbildung der Vorlage "eightbuttons-lastthreesmall large sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![Abbildung der Vorlage "eightbuttons-lastthreesmall medium sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![Abbildung der Vorlage "eightbuttons-lastthreesmall small sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

<span data-ttu-id="9f47e-206">EightButtons-LastThreeSmall</span><span class="sxs-lookup"><span data-stu-id="9f47e-206">EightButtons-LastThreeSmall</span></span>

<span data-ttu-id="9f47e-207">Acht Steuerelemente der Schaltflächenfamilie (alternative Darstellung).</span><span class="sxs-lookup"><span data-stu-id="9f47e-207">Eight button-family controls (alternate presentation).</span></span><br/>

> [!Note]  
> <span data-ttu-id="9f47e-208">Alle mit dieser Vorlage deklarierten Steuerelementelemente müssen in zwei [**ControlGroup-Elementen**](windowsribbon-element-controlgroup.md) enthalten sein: eines für die ersten fünf Elemente und eines für die letzten drei Elemente.</span><span class="sxs-lookup"><span data-stu-id="9f47e-208">All control elements declared with this template must be contained in two [**ControlGroup**](windowsribbon-element-controlgroup.md) elements: one for the first five elements and one for the last three elements.</span></span>

<br/> <span data-ttu-id="9f47e-209">Im folgenden Beispiel wird das für diese Vorlage erforderliche Markup veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="9f47e-209">The following example demonstrates the markup required for this template.</span></span><br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![Abbildung der Vorlage "eightbuttons large sizedefinition".](images/overviews/sizedefinition-eightbuttons-large.png)

![Abbildung der Vorlage "Eightbuttons medium sizedefinition".](images/overviews/sizedefinition-eightbuttons-medium.png)

![Abbildung der Vorlage "eightbuttons small sizedefinition".](images/overviews/sizedefinition-eightbuttons-small.png)

<span data-ttu-id="9f47e-213">NineButtons</span><span class="sxs-lookup"><span data-stu-id="9f47e-213">NineButtons</span></span>

<span data-ttu-id="9f47e-214">Neun Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-214">Nine button-family controls.</span></span>

![Abbildung der Vorlage "ninebuttons large sizedefinition".](images/overviews/sizedefinition-ninebuttons-large.png)

![Abbildung der Vorlage "ninebuttons medium sizedefinition".](images/overviews/sizedefinition-ninebuttons-medium.png)

![Abbildung der Vorlage "ninebuttons small sizedefinition".](images/overviews/sizedefinition-ninebuttons-small.png)

<span data-ttu-id="9f47e-218">TenButtons</span><span class="sxs-lookup"><span data-stu-id="9f47e-218">TenButtons</span></span>

<span data-ttu-id="9f47e-219">Zehn Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-219">Ten button-family controls.</span></span>

![Abbildung der Vorlage "tenbuttons large sizedefinition".](images/overviews/sizedefinition-tenbuttons-large.png)

![Abbildung der Vorlage "Tenbuttons medium sizedefinition".](images/overviews/sizedefinition-tenbuttons-medium.png)

![Abbildung der Vorlage "tenbuttons small sizedefinition".](images/overviews/sizedefinition-tenbuttons-small.png)

<span data-ttu-id="9f47e-223">ElferButtons</span><span class="sxs-lookup"><span data-stu-id="9f47e-223">ElevenButtons</span></span>

<span data-ttu-id="9f47e-224">Elf Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-224">Eleven button-family controls.</span></span>

![Abbildung der Vorlage "elfbuttons large sizedefinition".](images/overviews/sizedefinition-elevenbuttons-large.png)

![Abbildung der Vorlage für die mittlere Größendefinition von elfButtons.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![Abbildung der Vorlage "elfbuttons small sizedefinition".](images/overviews/sizedefinition-elevenbuttons-small.png)

<span data-ttu-id="9f47e-228">OneFontControl</span><span class="sxs-lookup"><span data-stu-id="9f47e-228">OneFontControl</span></span>

<span data-ttu-id="9f47e-229">Ein [**FontControl -Zeichen.**](windowsribbon-element-fontcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="9f47e-229">One [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

<span data-ttu-id="9f47e-230">Es werden nur große und mittlere Gruppengrößen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-230">Only Large and Medium group sizes are supported.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f47e-231">Das Einschließen von [**FontControl**](windowsribbon-element-fontcontrol.md) in eine benutzerdefinierte Vorlagendefinition wird vom Framework nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-231">Including a [**FontControl**](windowsribbon-element-fontcontrol.md) within a custom template definition is not supported by the framework.</span></span>

 

![Abbildung der Onefontcontrol-Vorlage "large sizedefinition".](images/overviews/sizedefinition-onefontcontrol-large.png)

![Abbildung der Vorlage onefontcontrol medium sizedefinition.](images/overviews/sizedefinition-onefontcontrol-medium.png)

<span data-ttu-id="9f47e-234">OneInRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="9f47e-234">OneInRibbonGallery</span></span>

<span data-ttu-id="9f47e-235">Ein [**InRibbonGallery-Steuerelement.**](windowsribbon-element-inribbongallery.md)</span><span class="sxs-lookup"><span data-stu-id="9f47e-235">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control.</span></span>

<span data-ttu-id="9f47e-236">Nur große und kleine Gruppengrößen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-236">Only Large and Small group sizes are supported.</span></span>

![Abbildung der Vorlage oneinribbongallery large sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![Abbildung der Vorlage oneinribbongallery small sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-small.png)

<span data-ttu-id="9f47e-239">InRibbonGalleryAndBigButton</span><span class="sxs-lookup"><span data-stu-id="9f47e-239">InRibbonGalleryAndBigButton</span></span>

<span data-ttu-id="9f47e-240">Ein [**InRibbonGallery-Steuerelement**](windowsribbon-element-inribbongallery.md) und ein Steuerelement der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-240">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control and a button-family control.</span></span>

<span data-ttu-id="9f47e-241">Nur große und kleine Gruppengrößen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-241">Only Large and Small group sizes are supported.</span></span>

![Abbildung der Vorlage inribbongalleryandbigbigbutton large sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![Abbildung der Vorlage inribbongalleryandbigbigbutton small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

<span data-ttu-id="9f47e-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span><span class="sxs-lookup"><span data-stu-id="9f47e-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span></span>

<span data-ttu-id="9f47e-245">Ein [Menübandkatalog-Steuerelement](windowsribbon-controls-inribbongallery.md) und zwei oder drei Steuerelemente der Schaltflächenfamilie.</span><span class="sxs-lookup"><span data-stu-id="9f47e-245">One [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control and two or three button-family controls.</span></span>

<span data-ttu-id="9f47e-246">Der Katalog wird auf die Popupdarstellung in den Gruppengrößen "Mittel" und "Klein" reduziert.</span><span class="sxs-lookup"><span data-stu-id="9f47e-246">The gallery collapses to Popup representation in Medium and Small group sizes.</span></span>

![Abbildung der Vorlage inribbongalleryandbuttons-galleryscalesfirst large sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![Abbildung der Vorlage inribbongalleryandbuttons-galleryscalesfirst medium sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![Abbildung der Vorlage inribbongalleryandbuttons-galleryscalesfirst small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

<span data-ttu-id="9f47e-250">ButtonGroups</span><span class="sxs-lookup"><span data-stu-id="9f47e-250">ButtonGroups</span></span>

<span data-ttu-id="9f47e-251">Eine komplexe Anordnung von 32 Steuerelementen der Schaltflächenfamilie (die meisten sind optional).</span><span class="sxs-lookup"><span data-stu-id="9f47e-251">A complex arrangement of 32 button-family controls (most of which are optional).</span></span>

> [!Note]  
> <span data-ttu-id="9f47e-252">Abgesehen von der optionalen Schaltfläche in voller Größe der großen ButtonGroups-Vorlage müssen alle mit dieser Vorlage deklarierten Steuerelementelemente in [**ControlGroup-Elementen**](windowsribbon-element-controlgroup.md) enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="9f47e-252">Aside from the optional full-sized button of the large ButtonGroups template, all control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="9f47e-253">Im folgenden Beispiel wird das Markup veranschaulicht, das erforderlich ist, um alle 32 Steuerelementelemente (erforderlich und optional) mit dieser Vorlage anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9f47e-253">The following example demonstrates the markup required to display all 32 control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![Abbildung der GroßenDefinitionsvorlage für Schaltflächengruppen.](images/overviews/sizedefinition-buttongroups-large.png)

![Abbildung der Vorlage für mittlere Größendefinition von Schaltflächengruppen.](images/overviews/sizedefinition-buttongroups-medium.png)

![Abbildung der Vorlage für kleine Größendefinitionen von Schaltflächengruppen.](images/overviews/sizedefinition-buttongroups-small.png)

<span data-ttu-id="9f47e-257">ButtonGroupsAndInputs</span><span class="sxs-lookup"><span data-stu-id="9f47e-257">ButtonGroupsAndInputs</span></span>

<span data-ttu-id="9f47e-258">Zwei Steuerelemente der Eingabefamilie (das zweite ist optional), gefolgt von einer komplexen Anordnung von 29 Steuerelementen der Schaltflächenfamilie (die meisten sind optional).</span><span class="sxs-lookup"><span data-stu-id="9f47e-258">Two input-family controls (the second is optional) followed by a complex arrangement of 29 button-family controls (most of which are optional).</span></span>

<span data-ttu-id="9f47e-259">Es werden nur große und mittlere Gruppengrößen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-259">Only Large and Medium group sizes are supported.</span></span>

> [!Note]  
> <span data-ttu-id="9f47e-260">Alle mit dieser Vorlage deklarierten Steuerelementelemente müssen in [**ControlGroup-Elementen**](windowsribbon-element-controlgroup.md) enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="9f47e-260">All control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="9f47e-261">Im folgenden Beispiel wird das Markup veranschaulicht, das zum Anzeigen aller (erforderlichen und optionalen) Steuerelementelemente mit dieser Vorlage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9f47e-261">The following example demonstrates the markup required to display all control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![Abbildung der Vorlage "buttongroups", "large sizedefinition".](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![Abbildung der Vorlage "buttongroups's medium sizedefinition".](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

<span data-ttu-id="9f47e-264">BigButtonsAndSmallButtonsOrInputs</span><span class="sxs-lookup"><span data-stu-id="9f47e-264">BigButtonsAndSmallButtonsOrInputs</span></span>

<span data-ttu-id="9f47e-265">Zwei Steuerelemente der Schaltflächenfamilie (beide optional), gefolgt von zwei oder drei Schaltflächen- oder Eingabefamilien-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="9f47e-265">Two button-family controls (both optional) followed by two or three button or input-family controls.</span></span>

<span data-ttu-id="9f47e-266">Es werden nur große und mittlere Gruppengrößen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-266">Only Large and Medium group sizes are supported.</span></span>

![Abbildung der Vorlage bigbuttonsandsmallbuttonsorinputs large sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![Abbildung der Vorlage bigbuttonsandsmallbuttonsorinputs medium sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a><span data-ttu-id="9f47e-269">Beispiel für "Basic SizeDefinition"</span><span class="sxs-lookup"><span data-stu-id="9f47e-269">Basic SizeDefinition Example</span></span>

<span data-ttu-id="9f47e-270">Im folgenden Codebeispiel wird veranschaulicht, wie eine [**SizeDefinition-Vorlage**](windowsribbon-element-sizedefinition.md) im Menübandmarkup deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="9f47e-270">The following code example provides a basic demonstration of how to declare a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template in Ribbon markup.</span></span>

<span data-ttu-id="9f47e-271">*OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) wird für dieses spezielle Beispiel verwendet, aber alle Frameworkvorlagen werden auf ähnliche Weise angegeben.</span><span class="sxs-lookup"><span data-stu-id="9f47e-271">The *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) is used for this particular example, but all framework templates are specified in a similar fashion.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a><span data-ttu-id="9f47e-272">Beispiel für komplexe GrößeDefinition mit Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="9f47e-272">Complex SizeDefinition Example with Scaling Policies</span></span>

<span data-ttu-id="9f47e-273">Das Reduzierungsverhalten von [**SizeDefinition-Vorlagen**](windowsribbon-element-sizedefinition.md) kann durch die Verwendung von Skalierungsrichtlinien im Menübandmarkup gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="9f47e-273">The collapsing behavior of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates can be controlled through the use of scaling policies in the Ribbon markup.</span></span>

<span data-ttu-id="9f47e-274">Das [**ScalingPolicy-Element**](windowsribbon-element-scalingpolicy.md) enthält ein Manifest von [**ScalingPolicy.IdealSizes-**](windowsribbon-element-scalingpolicy-idealsizes.md) und [**Scale-Deklarationen,**](windowsribbon-element-scale.md) die adaptive Layouteinstellungen für ein oder mehrere [**Group-Elemente**](windowsribbon-element-group.md) angeben, wenn die Größe des Menübands geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9f47e-274">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

> [!Note]  
> <span data-ttu-id="9f47e-275">Es wird dringend empfohlen, ausreichende Skalierungsrichtliniendetails anzugeben, sodass die meisten, wenn nicht alle [**Gruppenelemente**](windowsribbon-element-group.md) einem [**Scale-Element**](windowsribbon-element-scale.md) zugeordnet werden, bei dem das *Size-Attribut* gleich `Popup` ist.</span><span class="sxs-lookup"><span data-stu-id="9f47e-275">It is highly recommended that adequate scaling policy detail be specified such that most, if not all, [**Group**](windowsribbon-element-group.md) elements are associated with a [**Scale**](windowsribbon-element-scale.md) element where the *Size* attribute is equal to `Popup`.</span></span> <span data-ttu-id="9f47e-276">Auf diese Weise kann das Framework das Menüband in der kleinstmöglichen Größe rendern und die breite palette von Anzeigegeräten unterstützen, bevor automatisch ein Bildlaufmechanismus eingeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f47e-276">Doing so allows the framework to render the ribbon at the smallest size possible, and support the broadest range of display devices, before automatically introducing a scrolling mechanism.</span></span>

 

<span data-ttu-id="9f47e-277">Im folgenden Codebeispiel wird ein [**ScalingPolicy-Manifest**](windowsribbon-element-scalingpolicy.md) veranschaulicht, das eine [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition-Einstellung**](windowsribbon-element-sizedefinition.md) für jede von vier Gruppen von Steuerelementen auf einer Registerkarte **Home** angibt. Darüber hinaus werden [**Skalierungselemente**](windowsribbon-element-scale.md) angegeben, um das Reduzierungsverhalten jeder Gruppe in absteigender Größenreihenfolge zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="9f47e-277">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a><span data-ttu-id="9f47e-278">Benutzerdefinierte Vorlagen</span><span class="sxs-lookup"><span data-stu-id="9f47e-278">Custom Templates</span></span>

<span data-ttu-id="9f47e-279">Wenn das Standardlayoutverhalten und die vordefinierten [**SizeDefinition-Vorlagen**](windowsribbon-element-sizedefinition.md) nicht die Flexibilität oder Unterstützung für ein bestimmtes Layoutszenario bieten, werden benutzerdefinierte Vorlagen vom Menübandframework über das [**Ribbon.SizeDefinitions-Element**](windowsribbon-element-ribbon-sizedefinitions.md) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f47e-279">If the default layout behaviors and the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates do not offer the flexibility or support for a particular layout scenario, custom templates are supported by the Ribbon framework through the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="9f47e-280">Benutzerdefinierte Vorlagen können auf zwei Arten deklariert werden: eine eigenständige Methode, die das [**Ribbon.SizeDefinitions-Element**](windowsribbon-element-ribbon-sizedefinitions.md) zum Deklarieren von wiederverwendbaren, benannten Vorlagen oder eine [**Gruppenspezifische**](windowsribbon-element-group.md)Inlinemethode verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f47e-280">Custom templates can be declared in two ways: a standalone method using the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element for declaring reusable, named templates or an inline method that is [**Group**](windowsribbon-element-group.md)-specific.</span></span>

### <a name="standalone-template"></a><span data-ttu-id="9f47e-281">Eigenständige Vorlage</span><span class="sxs-lookup"><span data-stu-id="9f47e-281">Standalone Template</span></span>

<span data-ttu-id="9f47e-282">Das folgende Codebeispiel veranschaulicht eine einfache, wiederverwendbare benutzerdefinierte Vorlage.</span><span class="sxs-lookup"><span data-stu-id="9f47e-282">The following code example illustrates a basic, reusable custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a><span data-ttu-id="9f47e-283">Inlinevorlage</span><span class="sxs-lookup"><span data-stu-id="9f47e-283">Inline Template</span></span>

<span data-ttu-id="9f47e-284">Die folgenden Codebeispiele veranschaulichen eine einfache benutzerdefinierte Inlinevorlage für eine Gruppe von vier Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="9f47e-284">The following code examples illustrate a basic inline custom template for a group of four buttons.</span></span>

<span data-ttu-id="9f47e-285">Dieser Codeabschnitt zeigt die Befehlsdeklarationen für eine Gruppe von Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="9f47e-285">This section of code shows the Command declarations for a group of buttons.</span></span> <span data-ttu-id="9f47e-286">Hier werden auch große und kleine Imageressourcen angegeben.</span><span class="sxs-lookup"><span data-stu-id="9f47e-286">Large and small image resources are also specified here.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="9f47e-287">In diesem Codeabschnitt wird veranschaulicht, wie Sie große, mittlere und kleine [**GroupSizeDefinition-Vorlagen**](windowsribbon-element-groupsizedefinition.md) definieren, um die vier Schaltflächen in verschiedenen Größen und Layouts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9f47e-287">This section of code demonstrates how to define large, medium, and small [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) templates to display the four buttons at various sizes and layouts.</span></span> <span data-ttu-id="9f47e-288">Die [**ScalingPolicy-Deklaration**](windowsribbon-element-scalingpolicy.md) für die Registerkarte definiert, welche Vorlage für eine Gruppe von Steuerelementen verwendet wird, basierend auf der Größe und dem Speicherplatz des Menübands, die für die aktive Registerkarte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f47e-288">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) declaration for the tab defines which template is used for a group of controls based on the ribbon size and space required by the active tab.</span></span>


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



<span data-ttu-id="9f47e-289">Die folgenden Abbildungen zeigen, wie die Vorlagen aus dem vorherigen Beispiel auf die Menüband-Benutzeroberfläche angewendet werden, um eine Verringerung der Menübandgröße zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9f47e-289">The following images show how the templates from the previous example are applied to the ribbon UI to accommodate a decrease in ribbon size.</span></span>



|  <span data-ttu-id="9f47e-290">Typ</span><span class="sxs-lookup"><span data-stu-id="9f47e-290">Type</span></span>  |      <span data-ttu-id="9f47e-291">Image</span><span class="sxs-lookup"><span data-stu-id="9f47e-291">Image</span></span>                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f47e-292">Large</span><span class="sxs-lookup"><span data-stu-id="9f47e-292">Large</span></span>  | ![Abbildung einer inline großen benutzerdefinierten Vorlage.](images/overviews/sizedefinition-custom-large.png)   |
| <span data-ttu-id="9f47e-294">Medium</span><span class="sxs-lookup"><span data-stu-id="9f47e-294">Medium</span></span> | ![Abbildung einer benutzerdefinierten Inlinevorlage mit mittlerem Inline-](images/overviews/sizedefinition-custom-medium.png) |
| <span data-ttu-id="9f47e-296">Small</span><span class="sxs-lookup"><span data-stu-id="9f47e-296">Small</span></span>  | ![Abbildung einer kleinen benutzerdefinierten Inlinevorlage.](images/overviews/sizedefinition-custom-small.png)   |
| <span data-ttu-id="9f47e-298">Popup</span><span class="sxs-lookup"><span data-stu-id="9f47e-298">Popup</span></span>  | ![Abbildung einer benutzerdefinierten Inline-Popupvorlage.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a><span data-ttu-id="9f47e-300">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f47e-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f47e-301">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="9f47e-301">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[<span data-ttu-id="9f47e-302">**Skalieren**</span><span class="sxs-lookup"><span data-stu-id="9f47e-302">**Scale**</span></span>](windowsribbon-element-scale.md)
</dt> <dt>

[<span data-ttu-id="9f47e-303">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="9f47e-303">**Group**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

 

 





