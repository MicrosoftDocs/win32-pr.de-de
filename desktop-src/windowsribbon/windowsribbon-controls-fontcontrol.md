---
title: Schriftart-Steuerelement
description: Um die Integration und Konfiguration der Schriftart Unterstützung in Anwendungen zu vereinfachen, die Textverarbeitungs-und Textbearbeitungs Funktionen erfordern, bietet das Windows-Menüband-Framework ein spezielles Schriftart Steuerelement, das eine Vielzahl von Schriftart Eigenschaften wie z. b. Schriftart Name, Stil, Punktgröße und Effekte verfügbar macht.
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390575"
---
# <a name="font-control"></a><span data-ttu-id="07500-103">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="07500-103">Font Control</span></span>

<span data-ttu-id="07500-104">Um die Integration und Konfiguration der Schriftart Unterstützung in Anwendungen zu vereinfachen, die Textverarbeitungs-und Textbearbeitungs Funktionen erfordern, bietet das Windows-Menüband-Framework ein spezielles Schriftart Steuerelement, das eine Vielzahl von Schriftart Eigenschaften wie z. b. Schriftart Name, Stil, Punktgröße und Effekte verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="07500-104">To simplify the integration and configuration of font support in applications that require word processing and text editing capabilities, the Windows Ribbon framework provides a specialized Font Control that exposes a wide range of font properties such as typeface name, style, point size, and effects.</span></span>

-   [<span data-ttu-id="07500-105">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="07500-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="07500-106">Eine konsistente Darstellung</span><span class="sxs-lookup"><span data-stu-id="07500-106">A Consistent Experience</span></span>](#a-consistent-experience)
-   [<span data-ttu-id="07500-107">Einfache Integration und Konfiguration</span><span class="sxs-lookup"><span data-stu-id="07500-107">Easy Integration and Configuration</span></span>](#easy-integration-and-configuration)
-   [<span data-ttu-id="07500-108">Ausrichtung mit allgemeinen GDI-Text Strukturen</span><span class="sxs-lookup"><span data-stu-id="07500-108">Alignment with Common GDI Text Structures</span></span>](#alignment-with-common-gdi-text-structures)
-   [<span data-ttu-id="07500-109">Hinzufügen eines FontControl-Elements</span><span class="sxs-lookup"><span data-stu-id="07500-109">Add a FontControl</span></span>](#add-a-fontcontrol)
    -   [<span data-ttu-id="07500-110">Deklarieren eines FontControl im Markup</span><span class="sxs-lookup"><span data-stu-id="07500-110">Declaring a FontControl in Markup</span></span>](#declaring-a-fontcontrol-in-markup)
    -   [<span data-ttu-id="07500-111">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07500-111">Font Control Properties</span></span>](#font-control-properties)
-   [<span data-ttu-id="07500-112">Definieren eines FontControl-Befehls Handlers</span><span class="sxs-lookup"><span data-stu-id="07500-112">Define a FontControl Command Handler</span></span>](#define-a-fontcontrol-command-handler)
-   [<span data-ttu-id="07500-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07500-113">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="07500-114">Einführung</span><span class="sxs-lookup"><span data-stu-id="07500-114">Introduction</span></span>

<span data-ttu-id="07500-115">Das Schriftart Steuerelement ist ein zusammengesetztes Steuerelement, das aus Schaltflächen, UMSCHALT Flächen, Dropdown-Listenfeldern und Kombinations Feldern besteht, die alle zum Angeben einer bestimmten Schriftart Eigenschaft oder Formatierungs Option verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07500-115">The Font Control is a composite control that consists of buttons, toggle buttons, drop-down list boxes, and combo boxes, all of which are used to specify a particular font property or formatting option.</span></span>

<span data-ttu-id="07500-116">Der folgende Screenshot zeigt das Menüband-Schriftart-Steuerelement in WordPad für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="07500-116">The following screen shot shows the Ribbon Font Control in WordPad for Windows 7.</span></span>

![Screenshot des FontControl-Elements, bei dem das richfont-Attribut auf "true" festgelegt ist.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a><span data-ttu-id="07500-118">Eine konsistente Darstellung</span><span class="sxs-lookup"><span data-stu-id="07500-118">A Consistent Experience</span></span>

<span data-ttu-id="07500-119">Das Schriftart-Steuerelement ist ein integriertes Menüband-Steuerelement und verbessert die allgemeinen Funktionen für Schriftart Verwaltung, Auswahl und Formatierung und bietet eine umfangreiche, konsistente Benutzer Funktionalität für alle multifunktionsleistenanwendungen.</span><span class="sxs-lookup"><span data-stu-id="07500-119">As a built-in Ribbon control, the Font Control improves overall font management, selection and formatting functionality, and provides a rich, consistent user experience across all Ribbon applications.</span></span>

<span data-ttu-id="07500-120">Diese konsistente Darstellung umfasst</span><span class="sxs-lookup"><span data-stu-id="07500-120">This consistent experience includes</span></span>

-   <span data-ttu-id="07500-121">Standardisierte Formatierung und Auswahl von Schriftarten in Menüband-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="07500-121">Standardized formatting and selection of fonts across Ribbon applications.</span></span>
-   <span data-ttu-id="07500-122">Standardisierte Schriftart Darstellung über Menüband-Anwendungen hinweg.</span><span class="sxs-lookup"><span data-stu-id="07500-122">Standardized font representation across Ribbon applications.</span></span>
-   <span data-ttu-id="07500-123">Automatisch, in Windows 7, die Schriftart Aktivierung, die auf der Einstellung zum **anzeigen** oder **Ausblenden** der einzelnen Schriftart in der Systemsteuerung der **Schriftarten** basiert.</span><span class="sxs-lookup"><span data-stu-id="07500-123">Automatic, in Windows 7, font activation that is based on the **Show** or **Hide** setting for each font in the **Fonts** control panel.</span></span> <span data-ttu-id="07500-124">Das Schriftart Steuerelement zeigt nur die Schriftarten an, die auf **anzeigen** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="07500-124">The Font Control only displays those fonts that are set to **Show**.</span></span>
    > [!Note]  
    > <span data-ttu-id="07500-125">In Windows Vista bietet die **Schriftarten** -Systemsteuerung keine Funktionen zum **anzeigen** oder **Ausblenden** , sodass alle Schriftarten aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="07500-125">In Windows Vista, the **Fonts** control panel does not offer the **Show** or **Hide** functionality, so all fonts are activated.</span></span>

     

-   <span data-ttu-id="07500-126">Schriftart Verwaltung, die direkt über das-Steuerelement verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="07500-126">Font management that is available directly from the control.</span></span>

    <span data-ttu-id="07500-127">Der folgende Screenshot zeigt, dass der Zugriff auf die Schrift **Arten** -Systemsteuerung direkt über das Schriftart Steuerelement möglich ist.</span><span class="sxs-lookup"><span data-stu-id="07500-127">The following screen shot shows that the **Fonts** control panel can be accessed directly from the Font Control.</span></span>

    ![Screenshot der Schriftart Familien Liste in WordPad für Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   <span data-ttu-id="07500-129">Unterstützung für die automatische Vorschau.</span><span class="sxs-lookup"><span data-stu-id="07500-129">Support for auto-preview.</span></span>
-   <span data-ttu-id="07500-130">Verfügbar machen von Schriftarten, die für einen Benutzer am relevantesten sind, z. b.</span><span class="sxs-lookup"><span data-stu-id="07500-130">Exposure of fonts that are most relevant to a user, such as</span></span>
    -   <span data-ttu-id="07500-131">Lokalisierte Schriftart Listen für internationale Benutzer.</span><span class="sxs-lookup"><span data-stu-id="07500-131">Localized font lists for international users.</span></span>
    -   <span data-ttu-id="07500-132">Auf dem Eingabegerät basierende Schriftart Listen.</span><span class="sxs-lookup"><span data-stu-id="07500-132">Font lists based on input device.</span></span>

    > [!Note]  
    > <span data-ttu-id="07500-133">Die Unterstützung für diese Funktionalität ist auf keiner Plattform verfügbar, die älter als Windows 7 ist.</span><span class="sxs-lookup"><span data-stu-id="07500-133">Support for this functionality is not available on any platform older than Windows 7.</span></span>

     

## <a name="easy-integration-and-configuration"></a><span data-ttu-id="07500-134">Einfache Integration und Konfiguration</span><span class="sxs-lookup"><span data-stu-id="07500-134">Easy Integration and Configuration</span></span>

<span data-ttu-id="07500-135">Durch die Bereitstellung von standardmäßigen, wiederverwendbaren und leicht verwendbaren Funktionen erleichtert das Menüband-Schriftart Steuerelement das Integrieren der Schriftart Unterstützung in eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="07500-135">By providing standard, reusable, and easily consumed functionality, the Ribbon Font Control eases the burden of integrating font support into an application.</span></span>

<span data-ttu-id="07500-136">Die Details der Schriftart Auswahl und-Formatierung werden in ein eigenständiges logisches Element umschließt, das</span><span class="sxs-lookup"><span data-stu-id="07500-136">The details of font selection and formatting are wrapped in one, self-contained logical element that</span></span>

-   <span data-ttu-id="07500-137">Eliminiert die komplexe Verwaltung von Steuerungs Abhängigkeiten, die typisch für die Implementierungen von Schriftart Steuerelementen sind.</span><span class="sxs-lookup"><span data-stu-id="07500-137">Eliminates the complex management of control interdependencies typical of font control implementations.</span></span>
-   <span data-ttu-id="07500-138">Erfordert einen einzelnen Befehls Handler für alle Funktionen, die von den untergeordneten Steuerelementen für Schriftart Steuerelemente verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="07500-138">Requires a single Command handler for all functionality exposed by the Font Control sub-controls.</span></span>

<span data-ttu-id="07500-139">Mit diesem einzelnen Befehls Handler kann das Schriftart Steuerelement die Funktionalität verschiedener untergeordneter Steuerelemente intern verwalten. ein unter Steuerelement interagiert niemals direkt mit der Anwendung, unabhängig von der Funktion.</span><span class="sxs-lookup"><span data-stu-id="07500-139">This single Command handler allows the Font Control to manage the functionality of various sub-controls internally; a sub-control never interacts directly with the application, regardless of its function.</span></span>

<span data-ttu-id="07500-140">Weitere Funktionen des Schriftart Steuer Elements sind u. a.</span><span class="sxs-lookup"><span data-stu-id="07500-140">Other features of the Font Control include</span></span>

-   <span data-ttu-id="07500-141">Automatische, dpi-fähige Generierung eines WYSIWYG (was Sie sehen, was Sie sehen) Bitmap-Darstellung für jede Schriftart im Menü **Schriftfamilie** .</span><span class="sxs-lookup"><span data-stu-id="07500-141">Automatic, DPI-aware generation of a WYSIWYG (what you see is what you get) bitmap representation for each font in the **Font family** menu.</span></span>
-   <span data-ttu-id="07500-142">Integration von [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .</span><span class="sxs-lookup"><span data-stu-id="07500-142">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) integration.</span></span>
-   <span data-ttu-id="07500-143">Lokalisierte Bitmaps und Quick Infos der Schriftart Familie.</span><span class="sxs-lookup"><span data-stu-id="07500-143">Localized font family bitmaps and tooltips.</span></span>
-   <span data-ttu-id="07500-144">Schriftart Enumeration, Gruppierung und Metadaten für die Verwaltung und Darstellung von Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="07500-144">Font enumeration, grouping, and metadata for managing and presenting fonts.</span></span>
    > [!Note]  
    > <span data-ttu-id="07500-145">Die Unterstützung für diese Funktionalität ist auf keiner Plattform verfügbar, die älter als Windows 7 ist.</span><span class="sxs-lookup"><span data-stu-id="07500-145">Support for this functionality is not available on any platform older than Windows 7 .</span></span>

     

-   <span data-ttu-id="07500-146">Die Farbauswahl für **Textfarbe** und **Texthervorhebungen** , die das [Dropdown-Farb](windowsribbon-controls-dropdowncolorpicker.md) Auswahl Verhalten der Multifunktionsleiste widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="07500-146">The **Text color** and **Text highlight color** drop-down color pickers that mirror the Ribbon [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md) behavior.</span></span>
-   <span data-ttu-id="07500-147">Unterstützung der automatischen Vorschau von allen Galerie basierten untergeordneten Steuerelementen auf Schriftart Steuerelementen: **Schriftfamilie**, **Schrift** Grad, **Textfarbe** und **Text** Hervorhebungs Farbe.</span><span class="sxs-lookup"><span data-stu-id="07500-147">Support of auto-previewing by all Font Control gallery-based sub-controls: **Font family**, **Font size**, **Text color**, and **Text highlight color**.</span></span>

## <a name="alignment-with-common-gdi-text-structures"></a><span data-ttu-id="07500-148">Ausrichtung mit allgemeinen GDI-Text Strukturen</span><span class="sxs-lookup"><span data-stu-id="07500-148">Alignment with Common GDI Text Structures</span></span>

<span data-ttu-id="07500-149">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) -Text Stapel Komponenten werden verwendet, um die Schriftart Auswahl und Formatierungsfunktionen über das Menüband-Schriftart Steuerelement verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="07500-149">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text stack components are used to expose font selection and formatting functionality through the Ribbon Font Control.</span></span> <span data-ttu-id="07500-150">Die verschiedenen von der [LOGFONT-Struktur](/windows/win32/api/wingdi/ns-wingdi-logfonta), der [chooonfont-Struktur](/windows/win32/api/commdlg/ns-commdlg-choosefonta)und der [CHARFORMAT2-Struktur](/windows/win32/api/richedit/ns-richedit-charformat2a) unterstützten Schriftart Funktionen werden durch die untergeordneten Steuerelemente verfügbar gemacht, die im Schriftart Steuerelement enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="07500-150">The various font features supported by the [LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a) are exposed through the sub-controls that are included in the Font Control.</span></span>

<span data-ttu-id="07500-151">Die untergeordneten Steuerelemente, die im Schriftart Steuerelement angezeigt werden, sind von der im Menüband-Markup deklarierten *fonttype* -Vorlage abhängig.</span><span class="sxs-lookup"><span data-stu-id="07500-151">The sub-controls that are displayed in the Font Control depend on the *FontType* template declared in the Ribbon markup.</span></span> <span data-ttu-id="07500-152">Die *fonttype* -Vorlagen (im folgenden Abschnitt ausführlich erläutert) sind so konzipiert, dass Sie mit den allgemeinen [Windows Graphics Device Interface-Textstrukturen (GDI)](../gdi/windows-gdi.md) ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="07500-152">The *FontType* templates (discussed in further detail in the following section) are designed to align with the common [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text structures.</span></span>

## <a name="add-a-fontcontrol"></a><span data-ttu-id="07500-153">Hinzufügen eines FontControl-Elements</span><span class="sxs-lookup"><span data-stu-id="07500-153">Add a FontControl</span></span>

<span data-ttu-id="07500-154">In diesem Abschnitt werden die grundlegenden Schritte zum Hinzufügen eines Schriftart Steuer Elements zu einer Menü Bandanwendung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="07500-154">This section outlines the basic steps for adding a Font Control to a Ribbon application.</span></span>

### <a name="declaring-a-fontcontrol-in-markup"></a><span data-ttu-id="07500-155">Deklarieren eines FontControl im Markup</span><span class="sxs-lookup"><span data-stu-id="07500-155">Declaring a FontControl in Markup</span></span>

<span data-ttu-id="07500-156">Wie andere Menü Band Steuerelemente wird das Schriftart Steuerelement im Markup mit einem [**FontControl**](windowsribbon-element-fontcontrol.md) -Element deklariert und einer Befehls Deklaration über eine Befehls-ID zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="07500-156">Like other Ribbon controls, the Font Control is declared in markup with a [**FontControl**](windowsribbon-element-fontcontrol.md) element and associated with a Command declaration through a Command ID.</span></span> <span data-ttu-id="07500-157">Wenn die Anwendung kompiliert wird, wird die Befehls-ID verwendet, um den Befehl an einen Befehls Handler in der Host Anwendung zu binden.</span><span class="sxs-lookup"><span data-stu-id="07500-157">When the application is compiled, the Command ID is used to bind the Command to a Command handler in the host application.</span></span>

> [!Note]  
> <span data-ttu-id="07500-158">Wenn keine Befehls-ID mit dem [**FontControl**](windowsribbon-element-fontcontrol.md) im Markup deklariert ist, wird eine von dem Framework generiert.</span><span class="sxs-lookup"><span data-stu-id="07500-158">If no Command ID is declared with the [**FontControl**](windowsribbon-element-fontcontrol.md) in markup, then one is generated by the framework.</span></span>

 

<span data-ttu-id="07500-159">Da die untergeordneten Steuerelemente des Schriftart-Steuer Elements nicht direkt verfügbar gemacht werden, ist die Anpassung des Schriftart-Steuer Elements auf drei vom Framework definierte *fonttype* -Layoutvorlagen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="07500-159">Because the sub-controls of the Font Control are not exposed directly, customization of the Font Control is limited to three *FontType* layout templates defined by the framework.</span></span>

<span data-ttu-id="07500-160">Weitere Anpassungen des Schriftart Steuer Elements können durch Kombinieren der Layoutvorlage mit [**FontControl**](windowsribbon-element-fontcontrol.md) -Attributen wie *ishighlightbuttonvisible*, *isstrikepulbuttonvisible* und *isunderlinebuttonvisible* durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="07500-160">Further customization of the Font Control can be accomplished by combining the layout template with [**FontControl**](windowsribbon-element-fontcontrol.md) attributes such as *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible*, and *IsUnderlineButtonVisible*.</span></span>

> [!Note]  
> <span data-ttu-id="07500-161">Die Funktionen der Schriftart, die von den Standardvorlagen und Attributen für Schriftart Steuerelemente verfügbar gemacht werden, erfordern eine benutzerdefinierte Implementierung des Schriftart Steuer Elements, die sich außerhalb des Umfangs dieses Artikels befindet</span><span class="sxs-lookup"><span data-stu-id="07500-161">Font functionality beyond that exposed by the standard Font Control templates and attributes requires a custom font control implementation that is outside the scope of this article.</span></span>

 

<span data-ttu-id="07500-162">In der folgenden Tabelle sind die Schriftart Steuerelement Vorlagen und der Edit-Steuerelement Typen aufgeführt, an denen jede Vorlage ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="07500-162">The following table lists the Font Control templates and the edit control type that each template is aligned with.</span></span>



| <span data-ttu-id="07500-163">Vorlage</span><span class="sxs-lookup"><span data-stu-id="07500-163">Template</span></span>      | <span data-ttu-id="07500-164">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="07500-164">Supports</span></span>                                                                 |
|---------------|--------------------------------------------------------------------------|
| <span data-ttu-id="07500-165">Fontonly</span><span class="sxs-lookup"><span data-stu-id="07500-165">FontOnly</span></span>      | [<span data-ttu-id="07500-166">LogFont-Struktur</span><span class="sxs-lookup"><span data-stu-id="07500-166">LOGFONT Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| <span data-ttu-id="07500-167">Fontwithcolor</span><span class="sxs-lookup"><span data-stu-id="07500-167">FontWithColor</span></span> | [<span data-ttu-id="07500-168">Chooonfont-Struktur</span><span class="sxs-lookup"><span data-stu-id="07500-168">CHOOSEFONT Structure</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| <span data-ttu-id="07500-169">Richfont</span><span class="sxs-lookup"><span data-stu-id="07500-169">RichFont</span></span>      | [<span data-ttu-id="07500-170">CHARFORMAT2-Struktur</span><span class="sxs-lookup"><span data-stu-id="07500-170">CHARFORMAT2 Structure</span></span>](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

<span data-ttu-id="07500-171">In der folgenden Tabelle werden die-Steuerelemente aufgelistet, die den einzelnen Vorlagen zugeordnet sind, und die Steuerelemente identifiziert, die für eine zugeordnete Vorlage optional sind.</span><span class="sxs-lookup"><span data-stu-id="07500-171">The following table lists the controls that are associated with each template and identifies the controls that are optional for an associated template.</span></span>



<span data-ttu-id="07500-172">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="07500-172">Controls</span></span>

<span data-ttu-id="07500-173">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="07500-173">Templates</span></span>

<span data-ttu-id="07500-174">**Richfont**</span><span class="sxs-lookup"><span data-stu-id="07500-174">**RichFont**</span></span>

<span data-ttu-id="07500-175">**Fontwithcolor**</span><span class="sxs-lookup"><span data-stu-id="07500-175">**FontWithColor**</span></span>

<span data-ttu-id="07500-176">**Fontonly**</span><span class="sxs-lookup"><span data-stu-id="07500-176">**FontOnly**</span></span>

<span data-ttu-id="07500-177">Standard</span><span class="sxs-lookup"><span data-stu-id="07500-177">Default</span></span>

<span data-ttu-id="07500-178">Optional</span><span class="sxs-lookup"><span data-stu-id="07500-178">Optional</span></span>

<span data-ttu-id="07500-179">Standard</span><span class="sxs-lookup"><span data-stu-id="07500-179">Default</span></span>

<span data-ttu-id="07500-180">Optional</span><span class="sxs-lookup"><span data-stu-id="07500-180">Optional</span></span>

<span data-ttu-id="07500-181">Standard</span><span class="sxs-lookup"><span data-stu-id="07500-181">Default</span></span>

<span data-ttu-id="07500-182">Optional</span><span class="sxs-lookup"><span data-stu-id="07500-182">Optional</span></span>

<span data-ttu-id="07500-183">Kombinations Feld " **Schriftgröße** "</span><span class="sxs-lookup"><span data-stu-id="07500-183">**Font size** combo box</span></span>

<span data-ttu-id="07500-184">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-184">Yes</span></span>

<span data-ttu-id="07500-185">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-185">No</span></span>

<span data-ttu-id="07500-186">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-186">Yes</span></span>

<span data-ttu-id="07500-187">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-187">No</span></span>

<span data-ttu-id="07500-188">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-188">Yes</span></span>

<span data-ttu-id="07500-189">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-189">No</span></span>

<span data-ttu-id="07500-190">Kombinations Feld " **Schriftfamilie** "</span><span class="sxs-lookup"><span data-stu-id="07500-190">**Font family** combo box</span></span>

<span data-ttu-id="07500-191">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-191">Yes</span></span>

<span data-ttu-id="07500-192">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-192">No</span></span>

<span data-ttu-id="07500-193">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-193">Yes</span></span>

<span data-ttu-id="07500-194">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-194">No</span></span>

<span data-ttu-id="07500-195">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-195">Yes</span></span>

<span data-ttu-id="07500-196">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-196">No</span></span>

<span data-ttu-id="07500-197">Schaltfläche " **vergrößern** "</span><span class="sxs-lookup"><span data-stu-id="07500-197">**Grow font** button</span></span>

<span data-ttu-id="07500-198">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-198">Yes</span></span>

<span data-ttu-id="07500-199">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-199">Yes</span></span>

<span data-ttu-id="07500-200">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-200">Yes</span></span>

<span data-ttu-id="07500-201">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-201">Yes</span></span>

\-

\-

<span data-ttu-id="07500-202">Schaltfläche " **verkleinern** "</span><span class="sxs-lookup"><span data-stu-id="07500-202">**Shrink font** button</span></span>

<span data-ttu-id="07500-203">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-203">Yes</span></span>

<span data-ttu-id="07500-204">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-204">Yes</span></span>

<span data-ttu-id="07500-205">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-205">Yes</span></span>

<span data-ttu-id="07500-206">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-206">Yes</span></span>

\-

\-

<span data-ttu-id="07500-207">**Fett** Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="07500-207">**Bold** button</span></span>

<span data-ttu-id="07500-208">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-208">Yes</span></span>

<span data-ttu-id="07500-209">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-209">No</span></span>

<span data-ttu-id="07500-210">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-210">Yes</span></span>

<span data-ttu-id="07500-211">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-211">No</span></span>

<span data-ttu-id="07500-212">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-212">Yes</span></span>

<span data-ttu-id="07500-213">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-213">No</span></span>

<span data-ttu-id="07500-214">**Kursiv** Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="07500-214">**Italic** button</span></span>

<span data-ttu-id="07500-215">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-215">Yes</span></span>

<span data-ttu-id="07500-216">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-216">No</span></span>

<span data-ttu-id="07500-217">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-217">Yes</span></span>

<span data-ttu-id="07500-218">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-218">No</span></span>

<span data-ttu-id="07500-219">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-219">Yes</span></span>

<span data-ttu-id="07500-220">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-220">No</span></span>

<span data-ttu-id="07500-221">Unter **Streichung**</span><span class="sxs-lookup"><span data-stu-id="07500-221">**Underline** button</span></span>

<span data-ttu-id="07500-222">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-222">Yes</span></span>

<span data-ttu-id="07500-223">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-223">No</span></span>

<span data-ttu-id="07500-224">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-224">Yes</span></span>

<span data-ttu-id="07500-225">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-225">Yes</span></span>

<span data-ttu-id="07500-226">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-226">Yes</span></span>

<span data-ttu-id="07500-227">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-227">Yes</span></span>

<span data-ttu-id="07500-228">Schaltfläche " **durch** gestrichen"</span><span class="sxs-lookup"><span data-stu-id="07500-228">**Strikethrough** button</span></span>

<span data-ttu-id="07500-229">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-229">Yes</span></span>

<span data-ttu-id="07500-230">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-230">No</span></span>

<span data-ttu-id="07500-231">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-231">Yes</span></span>

<span data-ttu-id="07500-232">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-232">Yes</span></span>

<span data-ttu-id="07500-233">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-233">Yes</span></span>

<span data-ttu-id="07500-234">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-234">Yes</span></span>

<span data-ttu-id="07500-235">**Schaltfläche** "index"</span><span class="sxs-lookup"><span data-stu-id="07500-235">**Subscript** button</span></span>

<span data-ttu-id="07500-236">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-236">Yes</span></span>

<span data-ttu-id="07500-237">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-237">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="07500-238">**SuperScript** -Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="07500-238">**Superscript** button</span></span>

<span data-ttu-id="07500-239">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-239">Yes</span></span>

<span data-ttu-id="07500-240">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-240">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="07500-241">**Text** Hervorhebungs Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="07500-241">**Text highlight color** button</span></span>

<span data-ttu-id="07500-242">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-242">Yes</span></span>

<span data-ttu-id="07500-243">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-243">No</span></span>

<span data-ttu-id="07500-244">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-244">Yes</span></span>

<span data-ttu-id="07500-245">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-245">Yes</span></span>

\-

\-

<span data-ttu-id="07500-246">**Textfarbe** -Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="07500-246">**Text color** button</span></span>

<span data-ttu-id="07500-247">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-247">Yes</span></span>

<span data-ttu-id="07500-248">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-248">No</span></span>

<span data-ttu-id="07500-249">Ja</span><span class="sxs-lookup"><span data-stu-id="07500-249">Yes</span></span>

<span data-ttu-id="07500-250">Nein</span><span class="sxs-lookup"><span data-stu-id="07500-250">No</span></span>

\-

\-



 

<span data-ttu-id="07500-251">Wenn das Layoutverhalten eines Schriftart Steuer Elements deklariert wird, bietet das Menüband-Framework eine optionale *sizedefinition* -Layoutvorlage, `OneFontControl` , die zwei unter Steuerungs Konfigurationen auf der Grundlage der Größe des Menübands und des für das Schriftart Steuerelement verfügbaren Speicherplatzes definiert.</span><span class="sxs-lookup"><span data-stu-id="07500-251">When the layout behavior of a Font Control is declared, the Ribbon framework provides an optional *SizeDefinition* layout template, `OneFontControl`, that defines two sub-control configurations based on the size of the Ribbon and the space available for the Font Control.</span></span> <span data-ttu-id="07500-252">Weitere Informationen finden Sie unter [Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="07500-252">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

### <a name="adding-a-fontcontrol-to-a-ribbon"></a><span data-ttu-id="07500-253">Hinzufügen eines FontControl zu einem Menüband</span><span class="sxs-lookup"><span data-stu-id="07500-253">Adding a FontControl to a Ribbon</span></span>

<span data-ttu-id="07500-254">Die folgenden Codebeispiele veranschaulichen die grundlegenden Markup Anforderungen zum Hinzufügen eines Schriftart Steuer Elements zu einem Menüband:</span><span class="sxs-lookup"><span data-stu-id="07500-254">The following code examples demonstrate the basic markup requirements for adding a Font Control to a Ribbon:</span></span>

<span data-ttu-id="07500-255">In diesem Code Abschnitt wird das [**FontControl**](windowsribbon-element-fontcontrol.md) -Befehls Deklarations Markup angezeigt, einschließlich der [**Register**](windowsribbon-element-tab.md) Karten-und [**Gruppen**](windowsribbon-element-group.md) Befehle, die für die Anzeige eines Steuer Elements im [**Menüband**](windowsribbon-element-ribbon.md)erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="07500-255">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup, including the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) Commands that are required for displaying a control in the [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="07500-256">Dieser Code Abschnitt zeigt das Markup, das erforderlich ist, um ein [**FontControl**](windowsribbon-element-fontcontrol.md) -Element mit einem [**Befehl**](windowsribbon-element-command.md) über eine Befehls-ID zu deklarieren und zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="07500-256">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a [**Command**](windowsribbon-element-command.md) through a Command ID.</span></span> <span data-ttu-id="07500-257">Dieses spezielle Beispiel umfasst die [**Register**](windowsribbon-element-tab.md) Karten-und [**Gruppen**](windowsribbon-element-group.md) Deklarationen mit Skalierungs Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="07500-257">This particular example includes the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) declarations, with scaling preferences.</span></span>


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a><span data-ttu-id="07500-258">Hinzufügen eines FontControl zu einem contextpopup</span><span class="sxs-lookup"><span data-stu-id="07500-258">Adding a FontControl to a ContextPopup</span></span>

<span data-ttu-id="07500-259">Das Hinzufügen eines Schriftart-Steuer Elements zu einem [Kontext-Popup](windowsribbon-controls-contextpopup.md) erfordert eine ähnliche Vorgehensweise wie das Hinzufügen eines Schriftart-Steuer Elements zum Menüband.</span><span class="sxs-lookup"><span data-stu-id="07500-259">Adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md) requires a procedure similar to that of adding a Font Control to the Ribbon.</span></span> <span data-ttu-id="07500-260">Ein Schriftart-Steuerelement in einer [**MiniToolbar**](windowsribbon-element-minitoolbar.md) ist jedoch auf den Satz von Standard untergeordneten Steuerelementen beschränkt, die allen Schriftart Steuerelement Vorlagen gemeinsam sind: **Schriftfamilie**, **Schrift** Grad, **Fett** und **kursiv**.</span><span class="sxs-lookup"><span data-stu-id="07500-260">However, a Font Control in a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is restricted to the set of default sub-controls that are common to all Font Control templates: **Font family**, **Font size**, **Bold**, and **Italic**.</span></span>

<span data-ttu-id="07500-261">Die folgenden Codebeispiele veranschaulichen die grundlegenden Markup Anforderungen zum Hinzufügen eines Schriftart Steuer Elements zu einem [Kontext-Popup](windowsribbon-controls-contextpopup.md):</span><span class="sxs-lookup"><span data-stu-id="07500-261">The following code examples demonstrate the basic markup requirements for adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md):</span></span>

<span data-ttu-id="07500-262">Dieser Code Abschnitt zeigt das [**FontControl**](windowsribbon-element-fontcontrol.md) -Befehls Deklarations Markup, das für die Anzeige eines **FontControl** -Elements im [**contextpopup**](windowsribbon-element-contextpopup.md)erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="07500-262">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup that is required for displaying a **FontControl** in the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



<span data-ttu-id="07500-263">Dieser Code Abschnitt zeigt das Markup, das erforderlich ist, um ein [**FontControl**](windowsribbon-element-fontcontrol.md) -Element mit einem Befehl über eine Befehls-ID zu deklarieren und zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="07500-263">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a Command through a Command ID.</span></span>


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a><span data-ttu-id="07500-264">KeyTips</span><span class="sxs-lookup"><span data-stu-id="07500-264">Keytips</span></span>

<span data-ttu-id="07500-265">Auf jedes untergeordnete Steuerelement im Menüband-Schriftart Steuerelement kann über eine Tastenkombination oder KeyTip zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="07500-265">Each sub-control in the Ribbon Font Control is accessible through a keyboard shortcut, or keytip.</span></span> <span data-ttu-id="07500-266">Dieser KeyTip ist vordefiniert und wird den einzelnen untergeordneten Steuerelementen vom Framework zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="07500-266">This keytip is predefined and assigned to each sub-control by the framework.</span></span>

<span data-ttu-id="07500-267">Wenn dem [**FontControl**](windowsribbon-element-fontcontrol.md) -Element im Markup ein *KeyTip* -Attribut Wert zugewiesen wird, wird dieser Wert als Präfix zu dem vom Framework definierten KeyTip hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="07500-267">If a *Keytip* attribute value is assigned to the [**FontControl**](windowsribbon-element-fontcontrol.md) element in markup, this value is added as a prefix to the framework-defined keytip.</span></span>

> [!Note]  
> <span data-ttu-id="07500-268">Die Anwendung sollte eine Einzelzeichen Regel für dieses Präfix erzwingen.</span><span class="sxs-lookup"><span data-stu-id="07500-268">The application should enforce a single-character rule for this prefix.</span></span>

 

<span data-ttu-id="07500-269">In der folgenden Tabelle sind die vom Framework definierten KeyTips aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="07500-269">The following table lists the keytips defined by the framework.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07500-270">Unter Kontrolle</span><span class="sxs-lookup"><span data-stu-id="07500-270">Sub-control</span></span></th>
<th><span data-ttu-id="07500-271">KeyTip</span><span class="sxs-lookup"><span data-stu-id="07500-271">Keytip</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07500-272">Schriftfamilie</span><span class="sxs-lookup"><span data-stu-id="07500-272">Font family</span></span></td>
<td><span data-ttu-id="07500-273">F</span><span class="sxs-lookup"><span data-stu-id="07500-273">F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07500-274">Schriftschnitt</span><span class="sxs-lookup"><span data-stu-id="07500-274">Font style</span></span></td>
<td><span data-ttu-id="07500-275">T</span><span class="sxs-lookup"><span data-stu-id="07500-275">T</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07500-276">Schriftgrad</span><span class="sxs-lookup"><span data-stu-id="07500-276">Font size</span></span></td>
<td><span data-ttu-id="07500-277">E</span><span class="sxs-lookup"><span data-stu-id="07500-277">S</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07500-278">Schriftart vergrößern</span><span class="sxs-lookup"><span data-stu-id="07500-278">Grow font</span></span></td>
<td><span data-ttu-id="07500-279">G</span><span class="sxs-lookup"><span data-stu-id="07500-279">G</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07500-280">Schriftart verkleinern</span><span class="sxs-lookup"><span data-stu-id="07500-280">Shrink font</span></span></td>
<td><span data-ttu-id="07500-281">K</span><span class="sxs-lookup"><span data-stu-id="07500-281">K</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07500-282">Fett</span><span class="sxs-lookup"><span data-stu-id="07500-282">Bold</span></span></td>
<td><span data-ttu-id="07500-283">B</span><span class="sxs-lookup"><span data-stu-id="07500-283">B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07500-284">Kursiv</span><span class="sxs-lookup"><span data-stu-id="07500-284">Italic</span></span></td>
<td><span data-ttu-id="07500-285">I</span><span class="sxs-lookup"><span data-stu-id="07500-285">I</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07500-286">Underline</span><span class="sxs-lookup"><span data-stu-id="07500-286">Underline</span></span></td>
<td><span data-ttu-id="07500-287">U</span><span class="sxs-lookup"><span data-stu-id="07500-287">U</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07500-288">Durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="07500-288">Strikethrough</span></span></td>
<td><span data-ttu-id="07500-289">X</span><span class="sxs-lookup"><span data-stu-id="07500-289">X</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07500-290">Hochgestellt</span><span class="sxs-lookup"><span data-stu-id="07500-290">Superscript</span></span></td>
<td><span data-ttu-id="07500-291">Y oder Z</span><span class="sxs-lookup"><span data-stu-id="07500-291">Y or Z</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="07500-292">Wenn das <em>KeyTip</em> -Attribut nicht im Markup deklariert ist, lautet der standardkeytip Y. Andernfalls ist der standardkeytip <em>KeyTip</em> + Z.</span><span class="sxs-lookup"><span data-stu-id="07500-292">If the <em>Keytip</em> attribute is not declared in markup, the default keytip is Y; otherwise, the default keytip is <em>Keytip</em> + Z.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07500-293">Tiefgestellt</span><span class="sxs-lookup"><span data-stu-id="07500-293">Subscript</span></span></td>
<td><span data-ttu-id="07500-294">A</span><span class="sxs-lookup"><span data-stu-id="07500-294">A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07500-295">Schriftfarbe</span><span class="sxs-lookup"><span data-stu-id="07500-295">Font color</span></span></td>
<td><span data-ttu-id="07500-296">C</span><span class="sxs-lookup"><span data-stu-id="07500-296">C</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07500-297">Schriftart Hervorhebung</span><span class="sxs-lookup"><span data-stu-id="07500-297">Font highlight</span></span></td>
<td><span data-ttu-id="07500-298">H</span><span class="sxs-lookup"><span data-stu-id="07500-298">H</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="07500-299">Das empfohlene Präfix für eine MUI-Multifunktionsleiste (mehrsprachige Benutzeroberfläche) ist "F", wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="07500-299">The recommended prefix for a Multilingual User Interface (MUI) EN-US Ribbon is 'F', as shown in the following example.</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="07500-300">Der folgende Screenshot veranschaulicht die Schriftart Steuerelement-KeyTips, wie Sie im vorherigen Beispiel definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="07500-300">The following screen shot illustrates the Font Control keytips as they are defined in the previous example.</span></span>

![Screenshot der FontControl-KeyTips in WordPad für Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a><span data-ttu-id="07500-302">Die Ressourcen Datei des Menübands</span><span class="sxs-lookup"><span data-stu-id="07500-302">The Ribbon Resource File</span></span>

<span data-ttu-id="07500-303">Wenn die Markup Datei kompiliert wird, wird eine Ressourcen Datei generiert, die alle Ressourcen Verweise für die Multifunktionsleistenanwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="07500-303">When the markup file is compiled, a resource file that contains all resource references for the Ribbon application is generated.</span></span>

<span data-ttu-id="07500-304">Beispiel für eine einfache Ressourcen Datei:</span><span class="sxs-lookup"><span data-stu-id="07500-304">Example of a simple resource file:</span></span>


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a><span data-ttu-id="07500-305">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07500-305">Font Control Properties</span></span>

<span data-ttu-id="07500-306">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Schriftart Steuerelement und die zugehörigen untergeordneten Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="07500-306">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Font Control and its constituent sub-controls.</span></span>

<span data-ttu-id="07500-307">In der Regel wird eine Schriftart-Steuerelement Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="07500-307">Typically, a Font Control property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="07500-308">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="07500-308">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="07500-309">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="07500-309">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="07500-310">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="07500-310">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="07500-311">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="07500-311">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="07500-312">In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Schriftart-Steuerelement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="07500-312">The following table lists the property keys that are associated with the Font Control.</span></span>



| <span data-ttu-id="07500-313">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="07500-313">Property Key</span></span>                                                                                                                  | <span data-ttu-id="07500-314">Notizen</span><span class="sxs-lookup"><span data-stu-id="07500-314">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07500-315">UI- \_ pkey \_ fontproperties</span><span class="sxs-lookup"><span data-stu-id="07500-315">UI\_PKEY\_FontProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | <span data-ttu-id="07500-316">Macht alle Schriftart Steuerelement-untersteuerungseigenschaften als [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07500-316">Exposes, in aggregate as an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) object, all Font Control sub-control properties.</span></span><br/> <span data-ttu-id="07500-317">Das Framework fragt diese Eigenschaft ab, wenn `UI_INVALIDATIONS_VALUE` als Wert von *Flags* im [**iuiframework:: invalidateuicommand-Befehl**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="07500-317">The framework queries this property when `UI_INVALIDATIONS_VALUE` is passed as the value of *flags* in the call to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span><br/> |
| [<span data-ttu-id="07500-318">UI \_ pkey \_ fontproperties \_ changedproperties</span><span class="sxs-lookup"><span data-stu-id="07500-318">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | <span data-ttu-id="07500-319">Macht in Aggregat als [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Objekt nur Eigenschaften der Schriftart Steuerelement-unter Kontrolle verfügbar, die geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="07500-319">Exposes, in aggregate as an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object, only Font Control sub-control properties that have changed.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="07500-320">UI- \_ pkey- \_ KeyTip</span><span class="sxs-lookup"><span data-stu-id="07500-320">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | <span data-ttu-id="07500-321">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="07500-321">Can only be updated through invalidation.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="07500-322">UI- \_ pkey \_ aktiviert</span><span class="sxs-lookup"><span data-stu-id="07500-322">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | <span data-ttu-id="07500-323">Unterstützt [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) und [**iuiframework:: abtuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="07500-323">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>                                                                                                                                                                  |



 

<span data-ttu-id="07500-324">Zusätzlich zu den Eigenschaften, die vom Schriftart Steuerelement selbst unterstützt werden, definiert das Menüband-Framework auch einen [Eigenschafts Schlüssel](windowsribbon-reference-properties.md) für jedes untergeordnete Steuerelement der Schriftart Steuerung.</span><span class="sxs-lookup"><span data-stu-id="07500-324">In addition to the properties supported by the Font Control itself, the Ribbon framework also defines a [property key](windowsribbon-reference-properties.md) for each Font Control sub-control.</span></span> <span data-ttu-id="07500-325">Diese Eigenschafts Schlüssel und ihre Werte werden vom Framework über eine [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstellen Implementierung verfügbar gemacht, die die Methoden zum Verwalten einer Auflistung, auch als Eigenschaften Behälter bezeichnet, von Name-Wert-Paaren definiert.</span><span class="sxs-lookup"><span data-stu-id="07500-325">These property keys and their values are exposed by the framework through an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface implementation that defines the methods for managing a collection, also called a property bag, of name and value pairs.</span></span>

<span data-ttu-id="07500-326">Die Anwendung übersetzt die Schriftart Strukturen in Eigenschaften, auf die über die [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstellen Methoden zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="07500-326">The application translates the font structures to properties that are accessible through the [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface methods.</span></span> <span data-ttu-id="07500-327">Dieses Modell hebt den Unterschied zwischen dem Schriftart Steuerelement und den Windows-Graphics Device Interface (GDI)-Text Stapel Komponenten ([LOGFONT-Struktur](/windows/win32/api/wingdi/ns-wingdi-logfonta), [ausgewählter Schriftart Struktur](/windows/win32/api/commdlg/ns-commdlg-choosefonta)und [CHARFORMAT2-Struktur](/windows/win32/api/richedit/ns-richedit-charformat2a)) hervor, die vom Framework unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="07500-327">This model emphasizes the distinction between the Font Control and the Windows Graphics Device Interface (GDI) text stack components ([LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a)) that are supported by the framework.</span></span>

<span data-ttu-id="07500-328">In der folgenden Tabelle werden die einzelnen Steuerelemente und die zugehörigen Eigenschafts Schlüssel aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="07500-328">The following table lists the individual controls and their associated property keys.</span></span>



| <span data-ttu-id="07500-329">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="07500-329">Controls</span></span>                 | <span data-ttu-id="07500-330">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="07500-330">Property Key</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="07500-331">Notizen</span><span class="sxs-lookup"><span data-stu-id="07500-331">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07500-332">**Schriftgrad**</span><span class="sxs-lookup"><span data-stu-id="07500-332">**Font size**</span></span>            | [<span data-ttu-id="07500-333">Größe der Benutzeroberflächen- \_ pkey- \_ fontproperties \_</span><span class="sxs-lookup"><span data-stu-id="07500-333">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="07500-334">Wenn eine Fläche mit Hetero gener Größe hervorgehoben wird, legt das Menüband-Framework das Steuerelement **Schriftart Größe** auf Blank und den Wert von [UI \_ pkey \_ fontproperties \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md) auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="07500-334">When a run of heterogeneously sized text is highlighted, the Ribbon framework sets the **Font size** control to blank and the value of [UI\_PKEY\_FontProperties\_Size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) to 0.</span></span> <span data-ttu-id="07500-335">Wenn Sie auf die Schaltfläche **Schriftart vergrößern** oder **verkleinern** klicken, wird der gesamte markierte Text angepasst, aber der relative Unterschied in den Textgrößen wird beibehalten.</span><span class="sxs-lookup"><span data-stu-id="07500-335">When the **Grow font** or **Shrink font** button is clicked, all highlighted text is resized but the relative difference in text sizes is preserved.</span></span>                                                                                                                                                    |
| <span data-ttu-id="07500-336">**Schriftfamilie**</span><span class="sxs-lookup"><span data-stu-id="07500-336">**Font family**</span></span>          | [<span data-ttu-id="07500-337">UI \_ pkey \_ fontproperties- \_ Familie</span><span class="sxs-lookup"><span data-stu-id="07500-337">UI\_PKEY\_FontProperties\_Family</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | <span data-ttu-id="07500-338">GDI-Schriftfamilien Namen variieren je nach System Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="07500-338">GDI font family names vary with system locale.</span></span> <span data-ttu-id="07500-339">Wenn der Wert der [UI \_ pkey \_ fontproperties- \_ Familie](windowsribbon-reference-properties-uipkey-fontproperties-family.md) über Anwendungs Sitzungen hinweg beibehalten wird, sollte dieser Wert in jeder neuen Sitzung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="07500-339">As such, if the value of [UI\_PKEY\_FontProperties\_Family](windowsribbon-reference-properties-uipkey-fontproperties-family.md) is preserved across application sessions, that value should be retrieved on each new session.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="07500-340">**Schriftart vergrößern**</span><span class="sxs-lookup"><span data-stu-id="07500-340">**Grow font**</span></span>            | [<span data-ttu-id="07500-341">Größe der Benutzeroberflächen- \_ pkey- \_ fontproperties \_</span><span class="sxs-lookup"><span data-stu-id="07500-341">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="07500-342">Siehe **Schrift** Grad.</span><span class="sxs-lookup"><span data-stu-id="07500-342">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="07500-343">**Schriftart verkleinern**</span><span class="sxs-lookup"><span data-stu-id="07500-343">**Shrink font**</span></span>          | [<span data-ttu-id="07500-344">Größe der Benutzeroberflächen- \_ pkey- \_ fontproperties \_</span><span class="sxs-lookup"><span data-stu-id="07500-344">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="07500-345">Siehe **Schrift** Grad.</span><span class="sxs-lookup"><span data-stu-id="07500-345">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="07500-346">**Fett**</span><span class="sxs-lookup"><span data-stu-id="07500-346">**Bold**</span></span>                 | [<span data-ttu-id="07500-347">UI- \_ pkey \_ fontproperties \_ Fett</span><span class="sxs-lookup"><span data-stu-id="07500-347">UI\_PKEY\_FontProperties\_Bold</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="07500-348">**Kursiv**</span><span class="sxs-lookup"><span data-stu-id="07500-348">**Italic**</span></span>               | [<span data-ttu-id="07500-349">UI \_ pkey \_ fontproperties \_ kursiv</span><span class="sxs-lookup"><span data-stu-id="07500-349">UI\_PKEY\_FontProperties\_Italic</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="07500-350">**Streichen**</span><span class="sxs-lookup"><span data-stu-id="07500-350">**Underline**</span></span>            | [<span data-ttu-id="07500-351">Benutzeroberflächen- \_ pkey \_ fontproperties unter \_ streichen</span><span class="sxs-lookup"><span data-stu-id="07500-351">UI\_PKEY\_FontProperties\_Underline</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="07500-352">**Durchgestrichen**</span><span class="sxs-lookup"><span data-stu-id="07500-352">**Strikethrough**</span></span>        | [<span data-ttu-id="07500-353">UI- \_ pkey- \_ fontproperties \_ durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="07500-353">UI\_PKEY\_FontProperties\_Strikethrough</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="07500-354">**Index**</span><span class="sxs-lookup"><span data-stu-id="07500-354">**Subscript**</span></span>            | [<span data-ttu-id="07500-355">Benutzeroberflächen- \_ pkey \_ fontproperties \_ verticalpositionierung</span><span class="sxs-lookup"><span data-stu-id="07500-355">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="07500-356">Wenn die **Schaltfläche** "index" festgelegt ist, kann das **SuperScript** nicht auch festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="07500-356">If the **Subscript** button is set, then the **Superscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="07500-357">**Hochgestellt**</span><span class="sxs-lookup"><span data-stu-id="07500-357">**Superscript**</span></span>          | [<span data-ttu-id="07500-358">Benutzeroberflächen- \_ pkey \_ fontproperties \_ verticalpositionierung</span><span class="sxs-lookup"><span data-stu-id="07500-358">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="07500-359">Wenn die Schaltfläche **SuperScript** festgelegt ist, **kann der** Index nicht auch festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="07500-359">If the **Superscript** button is set, then the **Subscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="07500-360">**Text Hervorhebungs Farbe**</span><span class="sxs-lookup"><span data-stu-id="07500-360">**Text highlight color**</span></span> | <span data-ttu-id="07500-361">[Benutzeroberfläche \_ Pkey \_ fontproperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI \_ pkey \_ fontproperties \_ backgroundcolortype](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="07500-361">[UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI\_PKEY\_FontProperties\_BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span></span> | <span data-ttu-id="07500-362">Bietet die gleiche Funktionalität wie die `HighlightColors` Vorlage des [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="07500-362">Provides the same functionality as the `HighlightColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="07500-363">Es wird dringend empfohlen, dass nur ein ursprünglicher Text Hervorhebungs **Farbwert** von der Anwendung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="07500-363">We highly recommend that only an initial **Text highlight color** value be set by the application.</span></span> <span data-ttu-id="07500-364">Der zuletzt ausgewählte Wert sollte beibehalten und nicht festgelegt werden, wenn der Cursor innerhalb eines Dokuments neu positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="07500-364">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="07500-365">Dies ermöglicht einen schnellen Zugriff auf die letzte Auswahl des Benutzers, und die Farbauswahl muss nicht erneut geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="07500-365">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="07500-366">Farbsuhren können nicht angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="07500-366">Color swatches cannot be customized.</span></span><br/> |
| <span data-ttu-id="07500-367">**Textfarbe**</span><span class="sxs-lookup"><span data-stu-id="07500-367">**Text color**</span></span>           | <span data-ttu-id="07500-368">[Benutzeroberfläche \_ Pkey \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI \_ pkey \_ fontproperties \_ foregroundcolortype](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="07500-368">[UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI\_PKEY\_FontProperties\_ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span></span>           | <span data-ttu-id="07500-369">Bietet die gleiche Funktionalität wie die `StandardColors` Vorlage des [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="07500-369">Provides the same functionality as the `StandardColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="07500-370">Es wird dringend empfohlen, dass nur ein ursprünglicher **textfarbwert** von der Anwendung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="07500-370">We highly recommend that only an initial **Text color** value be set by the application.</span></span> <span data-ttu-id="07500-371">Der zuletzt ausgewählte Wert sollte beibehalten und nicht festgelegt werden, wenn der Cursor innerhalb eines Dokuments neu positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="07500-371">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="07500-372">Dies ermöglicht einen schnellen Zugriff auf die letzte Auswahl des Benutzers, und die Farbauswahl muss nicht erneut geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="07500-372">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="07500-373">Farbsuhren können nicht angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="07500-373">Color swatches cannot be customized.</span></span><br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a><span data-ttu-id="07500-374">Definieren eines FontControl-Befehls Handlers</span><span class="sxs-lookup"><span data-stu-id="07500-374">Define a FontControl Command Handler</span></span>

<span data-ttu-id="07500-375">In diesem Abschnitt werden die erforderlichen Schritte zum Binden eines Schriftart-Steuer Elements an einen Befehls Handler beschrieben.</span><span class="sxs-lookup"><span data-stu-id="07500-375">This section describes the steps required to bind a Font Control to a Command handler.</span></span>

> [!WARNING]
> <span data-ttu-id="07500-376">Jeder Versuch, ein Farbmuster aus der Farbauswahl eines Schriftart Steuer Elements auszuwählen, kann zu einer Zugriffsverletzung führen, wenn dem Steuerelement kein Befehls Handler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="07500-376">Any attempt to select a color swatch from the color picker of a Font Control may result in an access violation if no Command handler is associated with the control.</span></span>

 

<span data-ttu-id="07500-377">Im folgenden Codebeispiel wird veranschaulicht, wie im Markup deklarierte Befehle an einen Befehls Handler gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="07500-377">The following code example demonstrates how to bind Commands that are declared in markup to a Command handler.</span></span>


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



<span data-ttu-id="07500-378">Im folgenden Codebeispiel wird veranschaulicht, wie die [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Methode für ein Schriftart Steuerelement implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="07500-378">The following code example illustrates how to implement the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



<span data-ttu-id="07500-379">Im folgenden Codebeispiel wird veranschaulicht, wie die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Methode für ein Schriftart Steuerelement implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="07500-379">The following code example illustrates how to implement the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="07500-380">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07500-380">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07500-381">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07500-381">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="07500-382">**FontControl-Element**</span><span class="sxs-lookup"><span data-stu-id="07500-382">**FontControl element**</span></span>](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="07500-383">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07500-383">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="07500-384">FontControl-Beispiel</span><span class="sxs-lookup"><span data-stu-id="07500-384">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

