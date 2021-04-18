---
title: Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien
description: Steuerelemente, die in der Menüband-Befehlsleiste gehostet werden, unterliegen Layoutregeln, die vom Windows-Menü Band Framework erzwungen werden, und basieren auf einer Kombination aus Standardverhalten und Layoutvorlagen (sowohl Framework-definiert als auch Benutzer definiert), wie im Menü Band Markup Diese Regeln definieren das Verhalten des adaptiven Layouts des Multifunktionsleisten-Frameworks, das beeinflussen, wie die Steuerelemente in der Befehlsleiste zur Laufzeit an verschiedene Menü Bandgrößen angepasst werden.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Windows-Menüband, anpassen
- Multifunktionsleiste, anpassen
- Windows-Multifunktionsleiste, sizedefinition-Vorlagen
- Multifunktionsleiste, sizedefinition-Vorlagen
- Windows-Menüband, benutzerdefinierte Vorlagen
- Multifunktionsleiste, benutzerdefinierte Vorlagen
- Anpassen des Menübands von Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b12618f88576cddeff119534215e501216193c3
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2020
ms.locfileid: "104569881"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a><span data-ttu-id="a0235-111">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="a0235-111">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>

<span data-ttu-id="a0235-112">Steuerelemente, die in der Menüband-Befehlsleiste gehostet werden, unterliegen Layoutregeln, die vom Windows-Menü Band Framework erzwungen werden, und basieren auf einer Kombination aus Standardverhalten und Layoutvorlagen (sowohl Framework-definiert als auch Benutzer definiert), wie im Menü Band Markup</span><span class="sxs-lookup"><span data-stu-id="a0235-112">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Windows Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="a0235-113">Diese Regeln definieren das Verhalten des adaptiven Layouts des Multifunktionsleisten-Frameworks, das beeinflussen, wie die Steuerelemente in der Befehlsleiste zur Laufzeit an verschiedene Menü Bandgrößen angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="a0235-113">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

-   [<span data-ttu-id="a0235-114">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="a0235-114">Introduction</span></span>](#introduction)
    -   [<span data-ttu-id="a0235-115">Menü Band-sizedefinition-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="a0235-115">Ribbon SizeDefinition Templates</span></span>](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [<span data-ttu-id="a0235-116">Benutzerdefinierte Vorlagen</span><span class="sxs-lookup"><span data-stu-id="a0235-116">Custom Templates</span></span>](#custom-templates)
-   [<span data-ttu-id="a0235-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a0235-117">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="a0235-118">Einführung</span><span class="sxs-lookup"><span data-stu-id="a0235-118">Introduction</span></span>

<span data-ttu-id="a0235-119">Das Adaptive Layout, wie im Menüband-Framework definiert, ist die Fähigkeit aller Steuerelemente auf der Multifunktionsleisten-Benutzeroberfläche, die Organisation, Größe, das Format und die relative Skalierung basierend auf den Änderungen an der Größe des Menübands zur Laufzeit dynamisch anzupassen.</span><span class="sxs-lookup"><span data-stu-id="a0235-119">Adaptive layout, as defined by the Ribbon framework, is the ability of all controls within the ribbon UI to dynamically adjust their organization, size, format, and relative scale based on changes to the size of the ribbon at run time.</span></span>

<span data-ttu-id="a0235-120">Das Framework stellt mithilfe eines Satzes von Markup Elementen, die für die Angabe und Anpassung verschiedener layoutverhaltensweisen vorgesehen sind, Adaptive Layoutfunktionen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a0235-120">The framework exposes adaptive layout functionality through a set of markup elements that are dedicated to specifying and customizing various layout behaviors.</span></span> <span data-ttu-id="a0235-121">Eine Auflistung von Vorlagen, die als [**sizedefinitions**](windowsribbon-element-sizedefinition.md)bezeichnet wird, wird durch das Framework definiert, von denen jedes verschiedene Steuerungs-und Layoutszenarien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-121">A collection of templates, called [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), is defined by the framework, each of which support various control and layout scenarios.</span></span> <span data-ttu-id="a0235-122">Das Framework unterstützt jedoch auch benutzerdefinierte Vorlagen, wenn die vordefinierten Vorlagen nicht die Benutzeroberfläche oder die Layouts bereitstellen, die für eine Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a0235-122">However, the framework also supports custom templates should the predefined templates not provide the UI experience or layouts required by an application.</span></span>

<span data-ttu-id="a0235-123">Zum Anzeigen von Steuerelementen in einem bevorzugten Layout auf einer bestimmten Menü Band Größe funktionieren sowohl vordefinierte Vorlagen als auch benutzerdefinierte Vorlagen in Verbindung mit dem [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="a0235-123">To display controls in a preferred layout at a particular ribbon size, both predefined templates and custom templates work in conjunction with the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element.</span></span> <span data-ttu-id="a0235-124">Dieses Element enthält ein Manifest von Größen Einstellungen, das vom Framework beim Rendern des Menübands als Leitfaden verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0235-124">This element contains a manifest of size preferences that the framework uses as a guide when rendering the ribbon.</span></span>

> [!Note]  
> <span data-ttu-id="a0235-125">Das Menüband-Framework bietet Standardlayout-Verhalten, das auf einer Reihe integrierter Heuristik für die Organisation und Darstellung von Steuerelementen zur Laufzeit basiert, ohne dass die vordefinierten [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="a0235-125">The Ribbon framework provides default layout behaviors based on a set of built-in heuristics for the organization and presentation of controls at run time without the need for the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span> <span data-ttu-id="a0235-126">Diese Funktion ist jedoch nur für prototypenzwecke gedacht.</span><span class="sxs-lookup"><span data-stu-id="a0235-126">However, this capability is intended for prototyping purposes only.</span></span>

 

### <a name="ribbon-sizedefinition-templates"></a><span data-ttu-id="a0235-127">Menü Band-sizedefinition-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="a0235-127">Ribbon SizeDefinition Templates</span></span>

<span data-ttu-id="a0235-128">Das Menüband-Framework bietet einen umfassenden Satz von [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen, die das Größen-und Layoutverhalten für eine [Gruppe](windowsribbon-controls-group.md) von Menü Band Steuerelementen angeben.</span><span class="sxs-lookup"><span data-stu-id="a0235-128">The Ribbon framework provides a comprehensive set of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates that specify size and layout behavior for a [Group](windowsribbon-controls-group.md) of Ribbon controls.</span></span> <span data-ttu-id="a0235-129">Diese Vorlagen behandeln die häufigsten Szenarien zum Organisieren von Steuerelementen in einer Menüband-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a0235-129">These templates cover most common scenarios for organizing controls in a Ribbon application.</span></span>

<span data-ttu-id="a0235-130">Um eine konsistente Benutzer Darstellung über Multifunktionsleisten-Anwendungen hinweg zu erzwingen, erzwingt jede [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlage Beschränkungen für die Steuerelemente oder die von ihr unterstützte Steuerelement Familie.</span><span class="sxs-lookup"><span data-stu-id="a0235-130">To enforce a consistent user experience across Ribbon applications, each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template imposes restrictions on the controls or the family of controls it supports.</span></span>

<span data-ttu-id="a0235-131">Die Schaltflächen Familie der Steuerelemente umfasst z. b. Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a0235-131">For example, the button family of controls includes:</span></span>

-   [<span data-ttu-id="a0235-132">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="a0235-132">Button</span></span>](windowsribbon-controls-button.md)
-   [<span data-ttu-id="a0235-133">UMSCHALT Fläche</span><span class="sxs-lookup"><span data-stu-id="a0235-133">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)
-   [<span data-ttu-id="a0235-134">Dropdown Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="a0235-134">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)
-   [<span data-ttu-id="a0235-135">Trenn Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="a0235-135">Split Button</span></span>](windowsribbon-controls-splitbutton.md)
-   [<span data-ttu-id="a0235-136">Dropdown-Katalog</span><span class="sxs-lookup"><span data-stu-id="a0235-136">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
-   [<span data-ttu-id="a0235-137">Split Button-Katalog</span><span class="sxs-lookup"><span data-stu-id="a0235-137">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
-   [<span data-ttu-id="a0235-138">Dropdown-Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="a0235-138">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)

<span data-ttu-id="a0235-139">Die Eingabe Familie der Steuerelemente umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a0235-139">While the input family of controls includes:</span></span>

-   [<span data-ttu-id="a0235-140">Kombinations Feld</span><span class="sxs-lookup"><span data-stu-id="a0235-140">Combo Box</span></span>](windowsribbon-controls-combobox.md)
-   [<span data-ttu-id="a0235-141">Spinner</span><span class="sxs-lookup"><span data-stu-id="a0235-141">Spinner</span></span>](windowsribbon-controls-spinner.md)

<span data-ttu-id="a0235-142">Das [Kontrollkästchen](windowsribbon-controls-checkbox.md) und der [in-Ribbon-](windowsribbon-controls-inribbongallery.md) Katalog gehören weder zur Schaltflächen Familie noch zur Eingabe Familie.</span><span class="sxs-lookup"><span data-stu-id="a0235-142">[Check Box](windowsribbon-controls-checkbox.md) and [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) do not belong to either the button family or the input family.</span></span> <span data-ttu-id="a0235-143">Diese beiden Steuerelemente können nur verwendet werden, wenn Sie explizit in einer [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlage angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0235-143">These two controls can be used only where explicitly indicated in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

<span data-ttu-id="a0235-144">Im folgenden finden Sie eine Liste der [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen mit einer Beschreibung des Layouts und der Steuerelemente, die für jede Vorlage zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a0235-144">The following is a list of the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates with a description of the layout and controls allowed by each template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0235-145">Wenn die in Markup deklarierten Steuerelemente nicht exakt der Steuerung von Typ, Reihenfolge und Menge zugeordnet werden, die in der zugeordneten Vorlage definiert ist, wird vom [Markup Compiler](windowsribbon-intentcl.md) ein [Validierungs Fehler](windowsribbon-compilationerrors.md) protokolliert, und die Kompilierung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="a0235-145">If the controls declared in markup do not map exactly to control type, order, and quantity defined in the associated template, a [validation error](windowsribbon-compilationerrors.md) is logged by the [markup compiler](windowsribbon-intentcl.md) and compilation is terminated.</span></span>

 



<span data-ttu-id="a0235-146">OneButton</span><span class="sxs-lookup"><span data-stu-id="a0235-146">OneButton</span></span>

<span data-ttu-id="a0235-147">Ein Schaltflächen-familiensteuer Element.</span><span class="sxs-lookup"><span data-stu-id="a0235-147">One button-family control.</span></span><br/> <span data-ttu-id="a0235-148">Es wird nur eine große Gruppengröße unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-148">Only Large group size is supported.</span></span><br/>

![Bild der oneButton-sizedefinition-Vorlage.](images/overviews/sizedefinition-onebutton.png)

<span data-ttu-id="a0235-150">Twobuttons</span><span class="sxs-lookup"><span data-stu-id="a0235-150">TwoButtons</span></span>

<span data-ttu-id="a0235-151">Zwei Schaltflächen-familiensteuer Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-151">Two button-family controls.</span></span><br/> <span data-ttu-id="a0235-152">Nur große und mittlere Gruppengrößen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-152">Only Large and Medium group sizes are supported.</span></span><br/>

![Bild der Vorlage "twobuttons Large sizedefinition".](images/overviews/sizedefinition-twobuttons-large.png)

![Bild der "twobuttons mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-twobuttons-medium.png)

<span data-ttu-id="a0235-155">Drei Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="a0235-155">ThreeButtons</span></span>

<span data-ttu-id="a0235-156">Drei Schaltflächen-familiensteuer Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-156">Three button-family controls.</span></span><br/> <span data-ttu-id="a0235-157">Nur große und mittlere Gruppengrößen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-157">Only Large and Medium group sizes are supported.</span></span><br/>

![Bild der großen sizedefinition-Vorlage mit drei Schaltflächen.](images/overviews/sizedefinition-threebuttons-large.png)

![Bild der mittleren sizedefinition-Vorlage mit drei Buttons.](images/overviews/sizedefinition-threebuttons-medium.png)

<span data-ttu-id="a0235-160">ThreeButtons-OneBigAndTwoSmall</span><span class="sxs-lookup"><span data-stu-id="a0235-160">ThreeButtons-OneBigAndTwoSmall</span></span>

<span data-ttu-id="a0235-161">Drei Schaltflächen-familiensteuer Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-161">Three button-family controls.</span></span><br/> <span data-ttu-id="a0235-162">Die erste Schaltfläche wird in allen drei Größen hervorgehoben dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a0235-162">The first button is presented prominently in all three sizes.</span></span><br/>

![Bild der drei-Schaltflächen: onebigandtwosmall Large sizedefinition-Vorlage.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![Abbildung von "Dreifach Buttons": onebigandtwosmall Mittel sizedefinition-Vorlage.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![Abbildung von "Dreifach Buttons": onebigandtwosmall Small sizedefinition-Vorlage.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

<span data-ttu-id="a0235-166">Dreibuttonsandonecheckbox</span><span class="sxs-lookup"><span data-stu-id="a0235-166">ThreeButtonsAndOneCheckBox</span></span>

<span data-ttu-id="a0235-167">Drei Schaltflächen-familiensteuer Elemente, die von einem einzelnen CheckBox-Steuerelement begleitet werden</span><span class="sxs-lookup"><span data-stu-id="a0235-167">Three button-family controls accompanied by a single CheckBox control.</span></span><br/> <span data-ttu-id="a0235-168">Nur große und mittlere Gruppengrößen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-168">Only Large and Medium group sizes are supported.</span></span><br/>

![Bild der großen sizedefinition-Vorlage "dreibuttonsandonecheckbox".](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![Bild der "dreibuttonsandonecheckbox mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

<span data-ttu-id="a0235-171">Fourbuttons</span><span class="sxs-lookup"><span data-stu-id="a0235-171">FourButtons</span></span>

<span data-ttu-id="a0235-172">Vier Schaltflächen-familiensteuer Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-172">Four button-family controls.</span></span><br/>

![Bild der Vorlage "große sizedefinition" von fourbuttons.](images/overviews/sizedefinition-fourbuttons-large.png)

![Bild der "fourbuttons mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-fourbuttons-medium.png)

![Bild der "fourbuttons Small sizedefinition"-Vorlage.](images/overviews/sizedefinition-fourbuttons-small.png)

<span data-ttu-id="a0235-176">Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="a0235-176">FiveButtons</span></span>

<span data-ttu-id="a0235-177">Fünf Schaltflächen-familiensteuer Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-177">Five button-family controls.</span></span><br/>

![Bild der Vorlage "große sizedefinition" für "fvebuttons".](images/overviews/sizedefinition-fivebuttons-large.png)

![Bild der "fvebuttons mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-fivebuttons-medium.png)

![Bild der Vorlage "Small sizedefinition" von "List".](images/overviews/sizedefinition-fivebuttons-small.png)

<span data-ttu-id="a0235-181">"Fveorsixbuttons"</span><span class="sxs-lookup"><span data-stu-id="a0235-181">FiveOrSixButtons</span></span>

<span data-ttu-id="a0235-182">Fünf Schaltflächen-familiensteuer Elemente und eine optionale sechste Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="a0235-182">Five button-family controls and an optional sixth button.</span></span><br/>

![Bild der Vorlage "große sizedefinition" von "fveorsixbuttons".](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![Bild der "fveorsixbuttons mittelgroßen sizedefinition"-Vorlage.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![Bild der "tvorsixbuttons Small sizedefinition"-Vorlage.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

<span data-ttu-id="a0235-186">Sixbuttons</span><span class="sxs-lookup"><span data-stu-id="a0235-186">SixButtons</span></span>

<span data-ttu-id="a0235-187">Sechs Schaltflächen-familiensteuer Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-187">Six button-family controls.</span></span><br/>

![Bild der sixbuttons-Vorlage "große sizedefinition".](images/overviews/sizedefinition-sixbuttons-large.png)

![Bild der sixbuttons mittelgroßen sizedefinition-Vorlage.](images/overviews/sizedefinition-sixbuttons-medium.png)

![Bild der sixbuttons Small sizedefinition-Vorlage.](images/overviews/sizedefinition-sixbuttons-small.png)

<span data-ttu-id="a0235-191">SixButtons-TwoColumns</span><span class="sxs-lookup"><span data-stu-id="a0235-191">SixButtons-TwoColumns</span></span>

<span data-ttu-id="a0235-192">Sechs Schaltflächen-familiensteuer Elemente (alternative Darstellung).</span><span class="sxs-lookup"><span data-stu-id="a0235-192">Six button-family controls (alternate presentation).</span></span><br/>

![Bild von sixbuttons-twocolumns Large sizedefinition-Vorlage.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![sixbuttons-twocolumns mittlere sizedefinition-Vorlage.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![Bild von sixbuttons-twocolumns Small sizedefinition-Vorlage.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

<span data-ttu-id="a0235-196">Sevenbuttons</span><span class="sxs-lookup"><span data-stu-id="a0235-196">SevenButtons</span></span>

<span data-ttu-id="a0235-197">Sieben Schaltflächen-familiensteuer Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-197">Seven button-family controls.</span></span><br/>

![Bild der Vorlage "große sizedefinition" von sevenbuttons.](images/overviews/sizedefinition-sevenbuttons-large.png)

![Bild der Vorlage "mediensizedefinition" von sevenbuttons.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![Bild der "sevenbuttons Small sizedefinition"-Vorlage.](images/overviews/sizedefinition-sevenbuttons-small.png)

<span data-ttu-id="a0235-201">Eightbuttons</span><span class="sxs-lookup"><span data-stu-id="a0235-201">EightButtons</span></span>

<span data-ttu-id="a0235-202">Acht Schaltflächen-familiensteuer Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-202">Eight button-family controls.</span></span><br/>

![Bild der Vorlage "eightbuttons-lastthreesmall Large sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![Bild der Vorlage "eightbuttons-lastthreesmall Mittel sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![Bild der Vorlage "eightbuttons-lastthreesmall Small sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

<span data-ttu-id="a0235-206">EightButtons-LastThreeSmall</span><span class="sxs-lookup"><span data-stu-id="a0235-206">EightButtons-LastThreeSmall</span></span>

<span data-ttu-id="a0235-207">Acht Schaltflächen-familiensteuer Elemente (alternative Darstellung).</span><span class="sxs-lookup"><span data-stu-id="a0235-207">Eight button-family controls (alternate presentation).</span></span><br/>

> [!Note]  
> <span data-ttu-id="a0235-208">Alle Steuerelemente, die mit dieser Vorlage deklariert werden, müssen in zwei [**controlgroup**](windowsribbon-element-controlgroup.md) -Elementen enthalten sein: einer für die ersten fünf Elemente und einer für die letzten drei Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-208">All control elements declared with this template must be contained in two [**ControlGroup**](windowsribbon-element-controlgroup.md) elements: one for the first five elements and one for the last three elements.</span></span>

<br/> <span data-ttu-id="a0235-209">Im folgenden Beispiel wird das für diese Vorlage erforderliche Markup veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a0235-209">The following example demonstrates the markup required for this template.</span></span><br/>

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



![Bild der "eightbuttons Large sizedefinition"-Vorlage.](images/overviews/sizedefinition-eightbuttons-large.png)

![Bild der Vorlage "eightbuttons mittlere sizedefinition".](images/overviews/sizedefinition-eightbuttons-medium.png)

![Bild der eightbuttons Small sizedefinition-Vorlage.](images/overviews/sizedefinition-eightbuttons-small.png)

<span data-ttu-id="a0235-213">Neunschalt Flächen</span><span class="sxs-lookup"><span data-stu-id="a0235-213">NineButtons</span></span>

<span data-ttu-id="a0235-214">Neun Schaltflächen-familiensteuer Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-214">Nine button-family controls.</span></span>

![Abbildung von "neunschalt Flächen große sizedefinition"-Vorlage.](images/overviews/sizedefinition-ninebuttons-large.png)

![Bild der "neunbuttons mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-ninebuttons-medium.png)

![Abbildung von "neunbuttons Small sizedefinition Template".](images/overviews/sizedefinition-ninebuttons-small.png)

<span data-ttu-id="a0235-218">Tenbuttons</span><span class="sxs-lookup"><span data-stu-id="a0235-218">TenButtons</span></span>

<span data-ttu-id="a0235-219">Zehn Schaltflächen-familiensteuer Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-219">Ten button-family controls.</span></span>

![Bild der "tenbuttons Large sizedefinition"-Vorlage.](images/overviews/sizedefinition-tenbuttons-large.png)

![Bild der Vorlage "tenbuttons Mittel (mittlere sizedefinition)".](images/overviews/sizedefinition-tenbuttons-medium.png)

![Bild der "tenbuttons Small sizedefinition"-Vorlage.](images/overviews/sizedefinition-tenbuttons-small.png)

<span data-ttu-id="a0235-223">Elevumbuttons</span><span class="sxs-lookup"><span data-stu-id="a0235-223">ElevenButtons</span></span>

<span data-ttu-id="a0235-224">Elf Steuerelemente der Schaltflächen-Familie.</span><span class="sxs-lookup"><span data-stu-id="a0235-224">Eleven button-family controls.</span></span>

![Bild der elevenbuttons Large sizedefinition-Vorlage.](images/overviews/sizedefinition-elevenbuttons-large.png)

![Bild der elevenbuttons mittelgroßen sizedefinition-Vorlage.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![Bild der elevenbuttons Small sizedefinition-Vorlage.](images/overviews/sizedefinition-elevenbuttons-small.png)

<span data-ttu-id="a0235-228">Onefontcontrol</span><span class="sxs-lookup"><span data-stu-id="a0235-228">OneFontControl</span></span>

<span data-ttu-id="a0235-229">Ein [**FontControl**](windowsribbon-element-fontcontrol.md)-Element.</span><span class="sxs-lookup"><span data-stu-id="a0235-229">One [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

<span data-ttu-id="a0235-230">Nur große und mittlere Gruppengrößen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-230">Only Large and Medium group sizes are supported.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0235-231">Das Einschließen eines [**FontControl**](windowsribbon-element-fontcontrol.md) -Elements in eine benutzerdefinierte Vorlagen Definition wird vom Framework nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-231">Including a [**FontControl**](windowsribbon-element-fontcontrol.md) within a custom template definition is not supported by the framework.</span></span>

 

![Bild der Vorlage "große sizedefinition" von onefontcontrol.](images/overviews/sizedefinition-onefontcontrol-large.png)

![Bild der "onefontcontrol mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-onefontcontrol-medium.png)

<span data-ttu-id="a0235-234">Oneinribbongallery</span><span class="sxs-lookup"><span data-stu-id="a0235-234">OneInRibbonGallery</span></span>

<span data-ttu-id="a0235-235">Ein [**inribbongallery**](windowsribbon-element-inribbongallery.md) -Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a0235-235">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control.</span></span>

<span data-ttu-id="a0235-236">Nur große und Kleine Gruppengrößen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-236">Only Large and Small group sizes are supported.</span></span>

![Bild der Vorlage "große sizedefinition" von oneinribbongallery.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![Bild der "oneinribbongallery Small sizedefinition"-Vorlage.](images/overviews/sizedefinition-oneinribbongallery-small.png)

<span data-ttu-id="a0235-239">Inribbongalleryandbigbutton</span><span class="sxs-lookup"><span data-stu-id="a0235-239">InRibbonGalleryAndBigButton</span></span>

<span data-ttu-id="a0235-240">Ein [**inribbongallery**](windowsribbon-element-inribbongallery.md) -Steuerelement und ein Schaltflächen-familiensteuer Element.</span><span class="sxs-lookup"><span data-stu-id="a0235-240">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control and a button-family control.</span></span>

<span data-ttu-id="a0235-241">Nur große und Kleine Gruppengrößen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-241">Only Large and Small group sizes are supported.</span></span>

![Bild der inribbongalleryandbigbutton Large sizedefinition-Vorlage.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![Bild der inribbongalleryandbigbutton Small sizedefinition-Vorlage.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

<span data-ttu-id="a0235-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span><span class="sxs-lookup"><span data-stu-id="a0235-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span></span>

<span data-ttu-id="a0235-245">Ein [in-Ribbon](windowsribbon-controls-inribbongallery.md) -Katalog Steuerelement und zwei oder drei Schaltflächen-familiensteuer Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0235-245">One [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control and two or three button-family controls.</span></span>

<span data-ttu-id="a0235-246">Der Katalog wird auf die Popup Darstellung in mittelgroßen und kleinen Gruppengrößen reduziert.</span><span class="sxs-lookup"><span data-stu-id="a0235-246">The gallery collapses to Popup representation in Medium and Small group sizes.</span></span>

![Bild der inribbongalleryandbuttons-galleryscalesfirst Large sizedefinition-Vorlage.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![Bild der inribbongalleryandbuttons-galleryscalesfirst mittelgroßen sizedefinition-Vorlage.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![Bild der inribbongalleryandbuttons-galleryscalesfirst Small sizedefinition-Vorlage.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

<span data-ttu-id="a0235-250">Buttongroups</span><span class="sxs-lookup"><span data-stu-id="a0235-250">ButtonGroups</span></span>

<span data-ttu-id="a0235-251">Eine komplexe Anordnung von 32-Schaltflächen-familiensteuer Elementen (die meisten sind optional).</span><span class="sxs-lookup"><span data-stu-id="a0235-251">A complex arrangement of 32 button-family controls (most of which are optional).</span></span>

> [!Note]  
> <span data-ttu-id="a0235-252">Abgesehen von der optionalen vollständigen Schaltfläche der Vorlage für große buttongroups müssen alle Steuerelemente, die mit dieser Vorlage deklariert werden, in [**controlgroup**](windowsribbon-element-controlgroup.md) -Elementen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="a0235-252">Aside from the optional full-sized button of the large ButtonGroups template, all control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="a0235-253">Das folgende Beispiel zeigt das Markup, das erforderlich ist, um alle 32-Steuerelement Elemente (erforderlich und optional) mit dieser Vorlage anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0235-253">The following example demonstrates the markup required to display all 32 control elements (required and optional) with this template.</span></span>


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



![Bild der buttongroups Large sizedefinition-Vorlage.](images/overviews/sizedefinition-buttongroups-large.png)

![Bild der buttongroups mittelgroßen sizedefinition-Vorlage.](images/overviews/sizedefinition-buttongroups-medium.png)

![Bild der buttongroups Small sizedefinition-Vorlage.](images/overviews/sizedefinition-buttongroups-small.png)

<span data-ttu-id="a0235-257">Buttongroupsandinputs</span><span class="sxs-lookup"><span data-stu-id="a0235-257">ButtonGroupsAndInputs</span></span>

<span data-ttu-id="a0235-258">Zwei eingabefamiliensteuerelemente (die zweite ist optional), gefolgt von einer komplexen Anordnung von 29 Schaltflächen-familiensteuer Elementen (die meisten sind optional).</span><span class="sxs-lookup"><span data-stu-id="a0235-258">Two input-family controls (the second is optional) followed by a complex arrangement of 29 button-family controls (most of which are optional).</span></span>

<span data-ttu-id="a0235-259">Nur große und mittlere Gruppengrößen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-259">Only Large and Medium group sizes are supported.</span></span>

> [!Note]  
> <span data-ttu-id="a0235-260">Alle Steuerelemente, die mit dieser Vorlage deklariert werden, müssen in [**controlgroup**](windowsribbon-element-controlgroup.md) -Elementen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="a0235-260">All control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="a0235-261">Das folgende Beispiel zeigt das Markup, das erforderlich ist, um alle Steuerelemente (erforderlich und optional) mit dieser Vorlage anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0235-261">The following example demonstrates the markup required to display all control elements (required and optional) with this template.</span></span>


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



![Bild der buttongroupsandinputs Large sizedefinition-Vorlage.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![Bild der buttongroupsandinputs mittelgroßen sizedefinition-Vorlage.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

<span data-ttu-id="a0235-264">Bigbuttonsandsmallbuttonsorinputs</span><span class="sxs-lookup"><span data-stu-id="a0235-264">BigButtonsAndSmallButtonsOrInputs</span></span>

<span data-ttu-id="a0235-265">Zwei Schaltflächen-familiensteuer Elemente (optional), gefolgt von zwei oder drei Schaltflächen-oder eingabefamiliensteuerelementen.</span><span class="sxs-lookup"><span data-stu-id="a0235-265">Two button-family controls (both optional) followed by two or three button or input-family controls.</span></span>

<span data-ttu-id="a0235-266">Nur große und mittlere Gruppengrößen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-266">Only Large and Medium group sizes are supported.</span></span>

![Abbildung der Vorlage "große sizedefinition" von bigbuttonsandsmallbuttonsorinputs.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![Bild der "bigbuttonsandsmallbuttonsorinputs mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a><span data-ttu-id="a0235-269">Einfaches Beispiel für sizedefinition</span><span class="sxs-lookup"><span data-stu-id="a0235-269">Basic SizeDefinition Example</span></span>

<span data-ttu-id="a0235-270">Das folgende Codebeispiel veranschaulicht, wie Sie eine [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlage im Menü Band Markup deklarieren.</span><span class="sxs-lookup"><span data-stu-id="a0235-270">The following code example provides a basic demonstration of how to declare a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template in Ribbon markup.</span></span>

<span data-ttu-id="a0235-271">Die " *oneinribbongallery* " [**sizedefinition**](windowsribbon-element-sizedefinition.md) wird für dieses spezielle Beispiel verwendet, aber alle frameworkvorlagen sind auf ähnliche Weise angegeben.</span><span class="sxs-lookup"><span data-stu-id="a0235-271">The *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) is used for this particular example, but all framework templates are specified in a similar fashion.</span></span>


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



### <a name="complex-sizedefinition-example-with-scaling-policies"></a><span data-ttu-id="a0235-272">Komplexes sizedefinition-Beispiel mit Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="a0235-272">Complex SizeDefinition Example with Scaling Policies</span></span>

<span data-ttu-id="a0235-273">Das reduzierende Verhalten von [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen kann durch die Verwendung von Skalierungs Richtlinien im Menüband-Markup gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="a0235-273">The collapsing behavior of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates can be controlled through the use of scaling policies in the Ribbon markup.</span></span>

<span data-ttu-id="a0235-274">Das [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Element enthält ein Manifest der [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) -und [**Scale**](windowsribbon-element-scale.md) -Deklarationen, die Adaptive Layouteinstellungen für ein oder mehrere [**Gruppen**](windowsribbon-element-group.md) Elemente angeben, wenn die Größe des Menübands geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a0235-274">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

> [!Note]  
> <span data-ttu-id="a0235-275">Es wird dringend empfohlen, dass ausreichend Details zur Skalierungs Richtlinie angegeben werden, sodass die meisten, wenn nicht alle [**Gruppen**](windowsribbon-element-group.md) Elemente einem [**Scale**](windowsribbon-element-scale.md) -Element zugeordnet sind, in dem das *size* -Attribut gleich ist `Popup` .</span><span class="sxs-lookup"><span data-stu-id="a0235-275">It is highly recommended that adequate scaling policy detail be specified such that most, if not all, [**Group**](windowsribbon-element-group.md) elements are associated with a [**Scale**](windowsribbon-element-scale.md) element where the *Size* attribute is equal to `Popup`.</span></span> <span data-ttu-id="a0235-276">Auf diese Weise kann das-Framework das Menüband mit der kleinsten Größe darstellen und die breiteste Palette von Anzeigegeräten unterstützen, bevor es automatisch einen scrollmechanismus einführt.</span><span class="sxs-lookup"><span data-stu-id="a0235-276">Doing so allows the framework to render the ribbon at the smallest size possible, and support the broadest range of display devices, before automatically introducing a scrolling mechanism.</span></span>

 

<span data-ttu-id="a0235-277">Das folgende Codebeispiel veranschaulicht ein [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Manifest, das eine [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Einstellung für jede von vier Gruppen von Steuerelementen auf einer Registerkarte **Home** angibt. Außerdem werden [**Skalierungs**](windowsribbon-element-scale.md) Elemente angegeben, um das reduzierende Verhalten der einzelnen Gruppen in absteigender Reihenfolge zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="a0235-277">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



### <a name="custom-templates"></a><span data-ttu-id="a0235-278">Benutzerdefinierte Vorlagen</span><span class="sxs-lookup"><span data-stu-id="a0235-278">Custom Templates</span></span>

<span data-ttu-id="a0235-279">Wenn das Standardlayoutverhalten und die vordefinierten [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen die Flexibilität oder Unterstützung für ein bestimmtes Layoutszenario nicht bieten, werden benutzerdefinierte Vorlagen durch das Ribbon [**. sizedefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) -Element vom Multifunktionsleisten-Framework unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0235-279">If the default layout behaviors and the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates do not offer the flexibility or support for a particular layout scenario, custom templates are supported by the Ribbon framework through the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="a0235-280">Benutzerdefinierte Vorlagen können auf zweierlei Weise deklariert werden: eine eigenständige Methode, die das [**Ribbon. sizedefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) -Element verwendet, um wiederverwendbare, benannte Vorlagen oder eine Inline Methode, die [**Gruppen**](windowsribbon-element-group.md)spezifisch ist, zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="a0235-280">Custom templates can be declared in two ways: a standalone method using the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element for declaring reusable, named templates or an inline method that is [**Group**](windowsribbon-element-group.md)-specific.</span></span>

### <a name="standalone-template"></a><span data-ttu-id="a0235-281">Eigenständige Vorlage</span><span class="sxs-lookup"><span data-stu-id="a0235-281">Standalone Template</span></span>

<span data-ttu-id="a0235-282">Das folgende Codebeispiel veranschaulicht eine einfache, wiederverwendbare benutzerdefinierte Vorlage.</span><span class="sxs-lookup"><span data-stu-id="a0235-282">The following code example illustrates a basic, reusable custom template.</span></span>


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



### <a name="inline-template"></a><span data-ttu-id="a0235-283">Inline Vorlage</span><span class="sxs-lookup"><span data-stu-id="a0235-283">Inline Template</span></span>

<span data-ttu-id="a0235-284">Die folgenden Codebeispiele veranschaulichen eine einfache Inline benutzerdefinierte Vorlage für eine Gruppe von vier Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="a0235-284">The following code examples illustrate a basic inline custom template for a group of four buttons.</span></span>

<span data-ttu-id="a0235-285">In diesem Code Abschnitt werden die Befehls Deklarationen für eine Gruppe von Schaltflächen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a0235-285">This section of code shows the Command declarations for a group of buttons.</span></span> <span data-ttu-id="a0235-286">Hier werden auch große und kleine Bild Ressourcen angegeben.</span><span class="sxs-lookup"><span data-stu-id="a0235-286">Large and small image resources are also specified here.</span></span>


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



<span data-ttu-id="a0235-287">In diesem Code Abschnitt wird veranschaulicht, wie Sie die Vorlagen "Large", "Medium" und "Small [**groupsizedefinition**](windowsribbon-element-groupsizedefinition.md) " definieren, um die vier Schaltflächen in verschiedenen Größen und Layouts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0235-287">This section of code demonstrates how to define large, medium, and small [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) templates to display the four buttons at various sizes and layouts.</span></span> <span data-ttu-id="a0235-288">Die [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Deklaration für die Registerkarte definiert, welche Vorlage für eine Gruppe von Steuerelementen basierend auf der Menü Band Größe und dem für die aktive Registerkarte erforderlichen Speicherplatz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0235-288">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) declaration for the tab defines which template is used for a group of controls based on the ribbon size and space required by the active tab.</span></span>


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



<span data-ttu-id="a0235-289">Die folgenden Bilder veranschaulichen, wie die Vorlagen aus dem vorherigen Beispiel auf die Multifunktionsleisten-Benutzeroberfläche angewendet werden, um eine Verkleinerung der Menüband-Größe zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a0235-289">The following images show how the templates from the previous example are applied to the ribbon UI to accommodate a decrease in ribbon size.</span></span>



|        |                                                                                                    |
|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0235-290">Groß</span><span class="sxs-lookup"><span data-stu-id="a0235-290">Large</span></span>  | ![Bild einer großen benutzerdefinierten Inline Vorlage.](images/overviews/sizedefinition-custom-large.png)   |
| <span data-ttu-id="a0235-292">Medium</span><span class="sxs-lookup"><span data-stu-id="a0235-292">Medium</span></span> | ![Bild einer benutzerdefinierten Inline-Vorlage.](images/overviews/sizedefinition-custom-medium.png) |
| <span data-ttu-id="a0235-294">Klein</span><span class="sxs-lookup"><span data-stu-id="a0235-294">Small</span></span>  | ![Bild einer kleinen benutzerdefinierten Inline Vorlage.](images/overviews/sizedefinition-custom-small.png)   |
| <span data-ttu-id="a0235-296">Popup</span><span class="sxs-lookup"><span data-stu-id="a0235-296">Popup</span></span>  | ![Bild einer benutzerdefinierten Inline-Popup Vorlage.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a><span data-ttu-id="a0235-298">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a0235-298">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0235-299">**Sizedefinition**</span><span class="sxs-lookup"><span data-stu-id="a0235-299">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[<span data-ttu-id="a0235-300">**Migen**</span><span class="sxs-lookup"><span data-stu-id="a0235-300">**Scale**</span></span>](windowsribbon-element-scale.md)
</dt> <dt>

[<span data-ttu-id="a0235-301">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="a0235-301">**Group**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

 

 





