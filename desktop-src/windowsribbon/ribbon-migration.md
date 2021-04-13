---
title: Migrieren zum Windows-Menü Band Framework
description: Eine Anwendung, die auf herkömmlichen Menüs, Symbolleisten und Dialogfeldern basiert, kann auf die umfangreiche, dynamische und Kontext gesteuerte Benutzeroberfläche des Windows-Menü Band Framework-befehlssystems migriert werden.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Windows-Menüband, Migrieren zu
- Multifunktionsleiste, Migrieren zu
- Migrieren zu Windows-Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74822781f891815c6eb30d9e15a7f7efaa983fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473596"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a><span data-ttu-id="94a39-106">Migrieren zum Windows-Menü Band Framework</span><span class="sxs-lookup"><span data-stu-id="94a39-106">Migrating to the Windows Ribbon Framework</span></span>

<span data-ttu-id="94a39-107">Eine Anwendung, die auf herkömmlichen Menüs, Symbolleisten und Dialogfeldern basiert, kann auf die umfangreiche, dynamische und Kontext gesteuerte Benutzeroberfläche des Windows-Menü Band Framework-befehlssystems migriert werden.</span><span class="sxs-lookup"><span data-stu-id="94a39-107">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven UI of the Windows Ribbon framework Command system.</span></span> <span data-ttu-id="94a39-108">Dies ist eine einfache und effektive Möglichkeit, um die Anwendung zu modernisieren und zu beleben und gleichzeitig die Barrierefreiheit, die Benutzerfreundlichkeit und die Auffindbarkeit ihrer Funktionalität zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="94a39-108">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

## <a name="introduction"></a><span data-ttu-id="94a39-109">Einführung</span><span class="sxs-lookup"><span data-stu-id="94a39-109">Introduction</span></span>

<span data-ttu-id="94a39-110">Im allgemeinen umfasst die Migration einer vorhandenen Anwendung zum Menüband-Framework Folgendes:</span><span class="sxs-lookup"><span data-stu-id="94a39-110">In general, migrating an existing application to the Ribbon framework involves the following:</span></span>

-   <span data-ttu-id="94a39-111">Entwerfen eines Menüband-Layouts und einer Steuerelement Organisation, das die Funktionalität der vorhandenen Anwendung verfügbar macht und flexibel genug ist, um neue Funktionen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="94a39-111">Designing a Ribbon layout and control organization that exposes the functionality of the existing application and is flexible enough to support new functionality.</span></span>
-   <span data-ttu-id="94a39-112">Anpassen des Codes der vorhandenen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="94a39-112">Adapting the code of the existing application.</span></span>
-   <span data-ttu-id="94a39-113">Migrieren vorhandener Anwendungs Ressourcen (Zeichen folgen und Bilder) zum Menüband-Framework.</span><span class="sxs-lookup"><span data-stu-id="94a39-113">Migrating existing application resources (strings and images) to the Ribbon framework.</span></span>

> [!Note]  
> <span data-ttu-id="94a39-114">Die [Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx) für die Multifunktionsleisten-Benutzeroberfläche sollten überprüft werden, um festzustellen, ob die Anwendung für eine Multifunktionsleisten-Benutzeroberfläche geeignet ist</span><span class="sxs-lookup"><span data-stu-id="94a39-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed to determine if the application is a suitable candidate for a Ribbon UI.</span></span>

 

## <a name="design-the-ribbon-layout"></a><span data-ttu-id="94a39-115">Entwerfen des Menüband-Layouts</span><span class="sxs-lookup"><span data-stu-id="94a39-115">Design the Ribbon Layout</span></span>

<span data-ttu-id="94a39-116">Mögliche Entwurfs-und Steuerelement Layouts der Multifunktionsleiste können durch Ausführen der folgenden Schritte identifiziert werden:</span><span class="sxs-lookup"><span data-stu-id="94a39-116">Potential Ribbon UI designs and control layouts can be identified by performing these steps:</span></span>

1.  <span data-ttu-id="94a39-117">Bestandsaufnahme aller vorhandenen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="94a39-117">Taking inventory of all existing functionality.</span></span>
2.  <span data-ttu-id="94a39-118">Übersetzen dieser Funktionalität in Menü Band Befehle.</span><span class="sxs-lookup"><span data-stu-id="94a39-118">Translating this functionality into Ribbon Commands.</span></span>
3.  <span data-ttu-id="94a39-119">Organisieren der Befehle in logische Gruppen.</span><span class="sxs-lookup"><span data-stu-id="94a39-119">Organizing the Commands into logical groups.</span></span>

### <a name="take-inventory"></a><span data-ttu-id="94a39-120">Inventur übernehmen</span><span class="sxs-lookup"><span data-stu-id="94a39-120">Take Inventory</span></span>

<span data-ttu-id="94a39-121">Im Menüband-Framework werden die Funktionen, die von einer Anwendung verfügbar gemacht werden, die den Zustand oder die Ansicht eines Arbeitsbereichs oder Dokuments bearbeitet, als Befehl angesehen.</span><span class="sxs-lookup"><span data-stu-id="94a39-121">In the Ribbon framework, the functionality exposed by an application that manipulates the state or the view of a workspace or document is considered a command.</span></span> <span data-ttu-id="94a39-122">Was einen Befehl ausmacht, kann variieren und hängt von der Art und Domäne der vorhandenen Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="94a39-122">What constitutes a command may vary and depends on the nature and domain of the existing application.</span></span>

<span data-ttu-id="94a39-123">In der folgenden Tabelle sind die grundlegenden Befehle für eine hypothetische Text Bearbeitungs Anwendung aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="94a39-123">The following table lists a set of basic commands for a hypothetical text editing application:</span></span>



| <span data-ttu-id="94a39-124">Symbol</span><span class="sxs-lookup"><span data-stu-id="94a39-124">Symbol</span></span>           | <span data-ttu-id="94a39-125">id</span><span class="sxs-lookup"><span data-stu-id="94a39-125">ID</span></span>     | <span data-ttu-id="94a39-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94a39-126">Description</span></span>               |
|------------------|--------|---------------------------|
| <span data-ttu-id="94a39-127">ID- \_ Datei \_ neu</span><span class="sxs-lookup"><span data-stu-id="94a39-127">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="94a39-128">0xe100</span><span class="sxs-lookup"><span data-stu-id="94a39-128">0xE100</span></span> | <span data-ttu-id="94a39-129">Neues Dokument</span><span class="sxs-lookup"><span data-stu-id="94a39-129">New document</span></span>              |
| <span data-ttu-id="94a39-130">ID- \_ Datei \_ Speichern</span><span class="sxs-lookup"><span data-stu-id="94a39-130">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="94a39-131">0xe103</span><span class="sxs-lookup"><span data-stu-id="94a39-131">0xE103</span></span> | <span data-ttu-id="94a39-132">Dokument speichern</span><span class="sxs-lookup"><span data-stu-id="94a39-132">Save document</span></span>             |
| <span data-ttu-id="94a39-133">ID- \_ Datei ( \_ SaveAs)</span><span class="sxs-lookup"><span data-stu-id="94a39-133">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="94a39-134">0xe104</span><span class="sxs-lookup"><span data-stu-id="94a39-134">0xE104</span></span> | <span data-ttu-id="94a39-135">Speichern unter... Dialog</span><span class="sxs-lookup"><span data-stu-id="94a39-135">Save As... (dialog)</span></span>       |
| <span data-ttu-id="94a39-136">ID- \_ Datei \_ geöffnet</span><span class="sxs-lookup"><span data-stu-id="94a39-136">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="94a39-137">0xe101</span><span class="sxs-lookup"><span data-stu-id="94a39-137">0xE101</span></span> | <span data-ttu-id="94a39-138">Öffnen Sie... Dialog</span><span class="sxs-lookup"><span data-stu-id="94a39-138">Open... (dialog)</span></span>          |
| <span data-ttu-id="94a39-139">ID- \_ Datei \_ Beenden</span><span class="sxs-lookup"><span data-stu-id="94a39-139">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="94a39-140">0xe102</span><span class="sxs-lookup"><span data-stu-id="94a39-140">0xE102</span></span> | <span data-ttu-id="94a39-141">Beenden der Anwendung</span><span class="sxs-lookup"><span data-stu-id="94a39-141">Exit the application</span></span>      |
| <span data-ttu-id="94a39-142">ID- \_ Bearbeitung \_ rückgängig</span><span class="sxs-lookup"><span data-stu-id="94a39-142">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="94a39-143">0xe12b</span><span class="sxs-lookup"><span data-stu-id="94a39-143">0xE12B</span></span> | <span data-ttu-id="94a39-144">Rückgängig</span><span class="sxs-lookup"><span data-stu-id="94a39-144">Undo</span></span>                      |
| <span data-ttu-id="94a39-145">ID- \_ Bearbeitungs \_ Ausschnitt</span><span class="sxs-lookup"><span data-stu-id="94a39-145">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="94a39-146">0xe123</span><span class="sxs-lookup"><span data-stu-id="94a39-146">0xE123</span></span> | <span data-ttu-id="94a39-147">Ausgewählten Text ausschneiden</span><span class="sxs-lookup"><span data-stu-id="94a39-147">Cut selected text</span></span>         |
| <span data-ttu-id="94a39-148">ID zum \_ Bearbeiten der \_ Kopie</span><span class="sxs-lookup"><span data-stu-id="94a39-148">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="94a39-149">0xe122</span><span class="sxs-lookup"><span data-stu-id="94a39-149">0xE122</span></span> | <span data-ttu-id="94a39-150">Ausgewählten Text kopieren</span><span class="sxs-lookup"><span data-stu-id="94a39-150">Copy selected text</span></span>        |
| <span data-ttu-id="94a39-151">ID \_ Bearbeiten, \_ Einfügen</span><span class="sxs-lookup"><span data-stu-id="94a39-151">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="94a39-152">0xe125</span><span class="sxs-lookup"><span data-stu-id="94a39-152">0xE125</span></span> | <span data-ttu-id="94a39-153">Text aus Zwischenablage einfügen</span><span class="sxs-lookup"><span data-stu-id="94a39-153">Paste text from clipboard</span></span> |
| <span data-ttu-id="94a39-154">ID- \_ Bearbeitung \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="94a39-154">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="94a39-155">0xe120</span><span class="sxs-lookup"><span data-stu-id="94a39-155">0xE120</span></span> | <span data-ttu-id="94a39-156">Ausgewählten Text löschen</span><span class="sxs-lookup"><span data-stu-id="94a39-156">Delete selected text</span></span>      |
| <span data-ttu-id="94a39-157">Vergrößern der ID- \_ Ansicht \_</span><span class="sxs-lookup"><span data-stu-id="94a39-157">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="94a39-158">1242</span><span class="sxs-lookup"><span data-stu-id="94a39-158">1242</span></span>   | <span data-ttu-id="94a39-159">Zoom... Dialog</span><span class="sxs-lookup"><span data-stu-id="94a39-159">Zoom... (dialog)</span></span>          |



 

<span data-ttu-id="94a39-160">Sehen Sie sich die vorhandenen Menüs und Symbolleisten an, wenn Sie ein Inventar von Befehlen aufbauen.</span><span class="sxs-lookup"><span data-stu-id="94a39-160">Look beyond existing menus and toolbars when building an inventory of commands.</span></span> <span data-ttu-id="94a39-161">Denken Sie daran, wie Benutzer mit dem Arbeitsbereich interagieren können.</span><span class="sxs-lookup"><span data-stu-id="94a39-161">Consider all the ways a user can interact with the workspace.</span></span> <span data-ttu-id="94a39-162">Obwohl nicht jeder Befehl für die Einbindung in das Menüband geeignet ist, kann diese Übung sehr gut Befehle verfügbar machen, die zuvor von Benutzeroberflächen Ebenen verdeckt wurden.</span><span class="sxs-lookup"><span data-stu-id="94a39-162">Even though not every command is suitable for inclusion in the Ribbon, this exercise may very well expose commands that were previously obscured by layers of UI.</span></span>

### <a name="translate"></a><span data-ttu-id="94a39-163">Translate</span><span class="sxs-lookup"><span data-stu-id="94a39-163">Translate</span></span>

<span data-ttu-id="94a39-164">Nicht jeder Befehl muss in der Menüband-Benutzeroberfläche dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="94a39-164">Not every command needs to be represented in the Ribbon UI.</span></span> <span data-ttu-id="94a39-165">Wenn Sie z. b. Text eingeben, eine Auswahl ändern, einen Bildlauf durchführen oder die Einfügemarke mit der Maus bewegen, sind diese als Befehle im hypothetischen Text-Editor qualifiziert. Diese können jedoch nicht in einer Befehlsleiste verfügbar gemacht werden, da jeweils eine direkte Interaktion mit der Benutzeroberfläche der Anwendung besteht.</span><span class="sxs-lookup"><span data-stu-id="94a39-165">For example, entering text, changing a selection, scrolling, or moving the insertion-point with the mouse all qualify as commands in the hypothetical text editor, however, these are not suitable to expose in a command bar as each involves a direct interaction with the UI of the application.</span></span>

<span data-ttu-id="94a39-166">Im Gegensatz dazu werden einige Funktionen möglicherweise nicht als Befehl im herkömmlichen Sinne betrachtet.</span><span class="sxs-lookup"><span data-stu-id="94a39-166">Conversely, some functionality may not be thought of as a command in the traditional sense.</span></span> <span data-ttu-id="94a39-167">Anstatt z. b. in einem Dialogfeld verborgen zu sein, können Seitenränder im Menüband als Gruppe von Spinner-Steuerelementen in einer Kontext Registerkarte oder im [Anwendungsmodus](ribbon-applicationmodes.md)dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="94a39-167">For example, instead of being buried in a dialog box, printer page-margin adjustments could be represented in the Ribbon as a group of Spinner controls in a contextual tab or [application mode](ribbon-applicationmodes.md).</span></span>

> [!Note]  
> <span data-ttu-id="94a39-168">Notieren Sie sich die numerische ID, die jedem Befehl zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="94a39-168">Make note of the numeric ID that may be assigned to each command.</span></span> <span data-ttu-id="94a39-169">Einige Benutzeroberflächen-Frameworks, wie z. b. Microsoft Foundation Classes (MFC), definieren IDs für Befehle, z. b. die Datei und das Bearbeitungs Menü (0xe100 bis 0xe200).</span><span class="sxs-lookup"><span data-stu-id="94a39-169">Some UI frameworks, such as Microsoft Foundation Classes (MFC), define IDs for commands such as the file and edit menu (0xE100 to 0xE200).</span></span>

 

### <a name="organize"></a><span data-ttu-id="94a39-170">Organisieren</span><span class="sxs-lookup"><span data-stu-id="94a39-170">Organize</span></span>

<span data-ttu-id="94a39-171">Bevor Sie versuchen, die Befehls Inventur zu organisieren, sollten Sie die [Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx) für die Multifunktionsleisten-Benutzeroberfläche auf bewährte Methoden beim Implementieren einer Multifunktionsleisten-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="94a39-171">Before attempting to organize the command inventory, the [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed for best practices when implementing a Ribbon UI.</span></span>

<span data-ttu-id="94a39-172">Im Allgemeinen können die folgenden Regeln auf die Menü Band Befehls Organisation angewendet werden:</span><span class="sxs-lookup"><span data-stu-id="94a39-172">In general, the following rules can be applied to Ribbon Command organization:</span></span>

-   <span data-ttu-id="94a39-173">Befehle, die für die Datei oder die gesamte Anwendung ausgeführt werden, gehören höchstwahrscheinlich im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="94a39-173">Commands that operate on the file or the overall application most likely belong in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="94a39-174">Häufig verwendete Befehle, wie z. b. Ausschneiden, kopieren und Einfügen (wie im Beispiel Text-Editor), werden in der Regel auf einer Standard Registerkarte Home abgelegt. In komplexeren Anwendungen können Sie an anderer Stelle in der Menüband-Benutzeroberfläche dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="94a39-174">Frequently used Commands such as Cut, Copy, and Paste (as in the text editor example) are typically placed on a default home tab. In more complex applications, they may be duplicated elsewhere in the Ribbon UI.</span></span>
-   <span data-ttu-id="94a39-175">Wichtige oder häufig verwendete Befehle können die Standard Einbindung in der [Symbolleiste für den schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md)rechtfertigen.</span><span class="sxs-lookup"><span data-stu-id="94a39-175">Important or frequently used Commands might warrant default inclusion in the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="94a39-176">Das Menüband-Framework stellt außerdem die ContextMenu-und MiniToolbar-Steuerelemente über die contextpopup-Ansicht bereit.</span><span class="sxs-lookup"><span data-stu-id="94a39-176">The Ribbon framework also provides ContextMenu and MiniToolbar controls through the ContextPopup View.</span></span> <span data-ttu-id="94a39-177">Diese Features sind nicht obligatorisch, aber wenn Ihre Anwendung über mindestens ein vorhandenes Kontextmenü verfügt, kann die Verwendung der enthaltenen Befehle möglicherweise die Wiederverwendung der vorhandenen Codebasis mit automatischer Bindung an vorhandene Ressourcen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="94a39-177">These features are not mandatory, but if your application has one or more existing context menus then migrating the commands they contain may allow the reuse of the existing codebase with automatic binding to existing resources.</span></span>

<span data-ttu-id="94a39-178">Da jede Anwendung unterschiedlich ist, lesen Sie die Richtlinien, und versuchen Sie, Sie so umfassend wie möglich anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="94a39-178">Because every application is different, read the guidelines and try to apply them to the fullest extent possible.</span></span> <span data-ttu-id="94a39-179">Eines der Ziele des Multifunktionsleisten-Frameworks ist das Bereitstellen einer vertrauten, konsistenten Benutzer Darstellung. dieses Ziel ist besser, wenn die Entwürfe für neue Anwendungen vorhandene Multifunktionsleisten-Anwendungen so weit wie möglich spiegeln.</span><span class="sxs-lookup"><span data-stu-id="94a39-179">One of the goals of the Ribbon framework is to provide a familiar, consistent user experience and this goal will be more achievable if designs for new applications mirror existing Ribbon applications as much as possible.</span></span>

## <a name="adapt-your-code"></a><span data-ttu-id="94a39-180">Anpassen Ihres Codes</span><span class="sxs-lookup"><span data-stu-id="94a39-180">Adapt Your Code</span></span>

<span data-ttu-id="94a39-181">Nachdem die Menüband-Befehle identifiziert und in logische Gruppierungen organisiert wurden, hängt die Anzahl der Schritte, die bei der Einbindung des Multifunktionsleisten-Frameworks in vorhandenen Anwendungscode aufgetreten sind, von der Komplexität der ursprünglichen Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="94a39-181">Once the Ribbon Commands have been identified and organized into logical groupings, the number of steps involved when incorporating the Ribbon framework into existing application code depends on the complexity of the original application.</span></span> <span data-ttu-id="94a39-182">Im Allgemeinen gibt es drei grundlegende Schritte:</span><span class="sxs-lookup"><span data-stu-id="94a39-182">In general, there are three basic steps:</span></span>

-   <span data-ttu-id="94a39-183">Erstellen Sie das Menüband-Markup auf der Grundlage der Befehls Organisation und Layoutspezifikation.</span><span class="sxs-lookup"><span data-stu-id="94a39-183">Create the Ribbon markup based on the Command organization and layout specification.</span></span>
-   <span data-ttu-id="94a39-184">Ersetzen Sie die Legacy Menü-und Symbolleisten Funktionalität durch Multifunktionsleisten-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="94a39-184">Replace legacy menu and toolbar functionality with Ribbon functionality.</span></span>
-   <span data-ttu-id="94a39-185">Implementieren Sie einen iuicommandhandler-Adapter.</span><span class="sxs-lookup"><span data-stu-id="94a39-185">Implement an IUICommandHandler adapter.</span></span>

### <a name="create-the-markup"></a><span data-ttu-id="94a39-186">Markup erstellen</span><span class="sxs-lookup"><span data-stu-id="94a39-186">Create The Markup</span></span>

<span data-ttu-id="94a39-187">Die Liste der Befehle sowie deren Organisation und Layout werden über die Menüband-Markup Datei deklariert, die vom [Menüband-Markup Compiler](windowsribbon-intentcl.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94a39-187">The list of commands as well as their organization and layout are declared through the Ribbon markup file which is consumed by the [Ribbon markup compiler](windowsribbon-intentcl.md).</span></span>

> [!Note]  
> <span data-ttu-id="94a39-188">Viele der Schritte, die erforderlich sind, um eine vorhandene Anwendung anzupassen, ähneln den Schritten, die zum Starten einer neuen Multifunktionsleistenanwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="94a39-188">Many of the steps required to adapt an existing application are similar to those required to start a new Ribbon application.</span></span> <span data-ttu-id="94a39-189">Weitere Informationen finden Sie im Tutorial [Erstellen einer Menüband-Anwendung](windowsribbon-stepbystep.md) für eine neue Exemplarische Vorgehensweise für eine Menüband-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="94a39-189">For more information, see the [Creating a Ribbon Application](windowsribbon-stepbystep.md) tutorial for a new Ribbon application walkthrough.</span></span>

 

<span data-ttu-id="94a39-190">Es gibt zwei primäre Abschnitte zum Menü Band Markup.</span><span class="sxs-lookup"><span data-stu-id="94a39-190">There are two primary sections to the Ribbon markup.</span></span> <span data-ttu-id="94a39-191">Der erste Abschnitt ist ein Manifest von Befehlen und den zugehörigen Ressourcen (Zeichen folgen und Bilder).</span><span class="sxs-lookup"><span data-stu-id="94a39-191">The first section is a manifest of Commands and their associated resources (strings and images).</span></span> <span data-ttu-id="94a39-192">Der zweite Abschnitt gibt die Struktur und die Platzierung von Steuerelementen auf dem Menüband an.</span><span class="sxs-lookup"><span data-stu-id="94a39-192">The second section specifies the structure and placement of controls on the Ribbon.</span></span>

<span data-ttu-id="94a39-193">Das Markup für den einfachen Text-Editor kann in etwa wie im folgenden Beispiel aussehen:</span><span class="sxs-lookup"><span data-stu-id="94a39-193">The markup for the simple text editor might look something like the following example:</span></span>

> [!Note]  
> <span data-ttu-id="94a39-194">Bild-und Zeichen folgen Ressourcen werden weiter unten in diesem Artikel behandelt.</span><span class="sxs-lookup"><span data-stu-id="94a39-194">Image and string resources are covered later in this article.</span></span>

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



<span data-ttu-id="94a39-195">Um das erneute definieren von Symbolen zu vermeiden, die von einem UI-Framework wie MFC definiert werden, verwendet das vorherige Beispiel für jeden Befehl etwas andere Symbolnamen (ID- \_ Datei \_ New und ID \_ cmd \_ New).</span><span class="sxs-lookup"><span data-stu-id="94a39-195">To avoid redefining symbols that are defined by a UI framework such as MFC, the previous example uses slightly different symbol names for each Command (ID\_FILE\_NEW versus ID\_CMD\_NEW).</span></span> <span data-ttu-id="94a39-196">Die numerische ID, die den einzelnen Befehlen zugewiesen ist, muss jedoch unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="94a39-196">However, the numeric ID assigned to each Command must remain the same.</span></span>

<span data-ttu-id="94a39-197">Um die Markup Datei in eine Anwendung zu integrieren, konfigurieren Sie einen benutzerdefinierten Buildschritt, um den Menü Band Markup Compiler (UICC.exe) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="94a39-197">To integrate the markup file into an application, configure a custom build step to run the Ribbon markup compiler, UICC.exe.</span></span> <span data-ttu-id="94a39-198">Die resultierenden Header-und Ressourcen Dateien werden dann in das vorhandene Projekt integriert.</span><span class="sxs-lookup"><span data-stu-id="94a39-198">The resulting header and resource files are then incorporated into the existing project.</span></span> <span data-ttu-id="94a39-199">Wenn die Menüband-Anwendung für den Beispiel Text-Editor den Namen "ribbonpad" hat, ist eine benutzerdefinierte Buildbefehlszeile ähnlich der folgenden erforderlich:</span><span class="sxs-lookup"><span data-stu-id="94a39-199">If the example text editor Ribbon application is named "RibbonPad", a custom-build command line similar to the following is required:</span></span>


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



<span data-ttu-id="94a39-200">Der Markup Compiler erstellt eine Binärdatei, eine Header Datei (H) und eine Ressourcen Datei (RC).</span><span class="sxs-lookup"><span data-stu-id="94a39-200">The markup compiler creates a binary file, a header (H) file and a resource (RC) file.</span></span> <span data-ttu-id="94a39-201">Da die vorhandene Anwendung wahrscheinlich über eine vorhandene RC-Datei verfügt, müssen Sie die generierten H-und RC-Dateien in diese RC-Datei einschließen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="94a39-201">Because the existing application likely has an existing RC file, include the generated H and RC files in that RC file, as shown in the following example:</span></span>


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a><span data-ttu-id="94a39-202">Legacy Menüs und Symbolleisten ersetzen</span><span class="sxs-lookup"><span data-stu-id="94a39-202">Replace Legacy Menus and Toolbars</span></span>

<span data-ttu-id="94a39-203">Zum Ersetzen von Standardmenüs und Symbolleisten durch ein Menüband in einer Legacy Anwendung ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="94a39-203">Replacing standard menus and toolbars with a ribbon in a legacy application requires the following:</span></span>

1.  <span data-ttu-id="94a39-204">Entfernen Sie Symbolleisten-und Menü Ressourcen Verweise aus der Ressourcen Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="94a39-204">Remove toolbar and menu resource references from the application's resource file.</span></span>
2.  <span data-ttu-id="94a39-205">Löscht den gesamten Initialisierungs Code der Symbolleisten-und Menüleiste.</span><span class="sxs-lookup"><span data-stu-id="94a39-205">Delete all toolbar and menu bar initialization code.</span></span>
3.  <span data-ttu-id="94a39-206">Löschen Sie den Code, der zum Anfügen einer Symbolleiste oder einer Menüleiste an das Fenster der obersten Ebene der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94a39-206">Delete any code used to attach a toolbar or menu bar to the top-level window of the application.</span></span>
4.  <span data-ttu-id="94a39-207">Instanziieren Sie das Menüband-Framework.</span><span class="sxs-lookup"><span data-stu-id="94a39-207">Instantiate the Ribbon framework.</span></span>
5.  <span data-ttu-id="94a39-208">Fügen Sie das Menüband an das Fenster der obersten Ebene der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="94a39-208">Attach the ribbon to the top-level window of the application.</span></span>
6.  <span data-ttu-id="94a39-209">Laden Sie das kompilierte Markup.</span><span class="sxs-lookup"><span data-stu-id="94a39-209">Load the compiled markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94a39-210">Vorhandene Statusleiste und Tastatur Verknüpfungs Tabellen sollten beibehalten werden, da das Menüband-Framework diese Features nicht ersetzt.</span><span class="sxs-lookup"><span data-stu-id="94a39-210">Existing status bar and keyboard shortcut tables should be preserved as the Ribbon framework does not replace these features.</span></span>

 

<span data-ttu-id="94a39-211">Im folgenden Beispiel wird veranschaulicht, wie das Framework mithilfe von [**iuiframework:: Initialisieren**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize)initialisiert wird:</span><span class="sxs-lookup"><span data-stu-id="94a39-211">The following example demonstrates how to initialize the framework using [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span></span>


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



<span data-ttu-id="94a39-212">Im folgenden Beispiel wird veranschaulicht, wie [**iuiframework:: loadui**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) verwendet wird, um das kompilierte Markup zu laden:</span><span class="sxs-lookup"><span data-stu-id="94a39-212">The following example demonstrates how to use [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to load the compiled markup:</span></span>


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



<span data-ttu-id="94a39-213">Die capplication-Klasse, auf die oben verwiesen wird, muss ein paar von Component Object Model (com)-Schnittstellen implementieren, die durch das Menüband-Framework definiert werden: [**iuiapplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) und [**iuicommandhandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span><span class="sxs-lookup"><span data-stu-id="94a39-213">The CApplication class, referred to above, must implement a pair of Component Object Model (COM) interfaces defined by the Ribbon framework: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) and [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span></span>

<span data-ttu-id="94a39-214">[**Iuiapplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) stellt die Haupt Rückruf Schnittstelle zwischen dem Framework und der Anwendung bereit (z. b. wird die Höhe des Menübands über [**iuiapplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)kommuniziert), während die Rückrufe für einzelne Befehle als Antwort auf [**iuiapplication:: onkreateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="94a39-214">[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) provides the main callback interface between the framework and the application (for example, the height of the ribbon is communicated through [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) while the callbacks for individual Commands are provided in response to [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span></span>

<span data-ttu-id="94a39-215">**Tipp:** Einige Anwendungs Frameworks, wie z. b. MFC, erfordern, dass die Höhe der Menü Band Leiste beim Rendern des Dokument Raums der Anwendung berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="94a39-215">**Tip:** Some application frameworks, such as MFC, require that the height of the ribbon bar be taken into account when rendering the document space of the application.</span></span> <span data-ttu-id="94a39-216">In diesen Fällen ist das Hinzufügen eines ausgeblendeten Fensters zum Überlagern der Menü Band Leiste und das Erzwingen des Dokument Raums zur gewünschten Höhe erforderlich.</span><span class="sxs-lookup"><span data-stu-id="94a39-216">In these cases, the addition of a hidden window to overlay the ribbon bar and force the document space to the desired height is necessary.</span></span> <span data-ttu-id="94a39-217">Ein Beispiel für diesen Ansatz, bei dem eine Layoutfunktion basierend auf der von der [**iuiribbon:: GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) -Methode zurückgegebenen Menüband-Höhe aufgerufen wird, finden Sie im [htmleditribbon-Beispiel](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="94a39-217">For an example of this approach, where a layout function is called based on the ribbon height returned by the [**IUIRibbon::GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) method, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

<span data-ttu-id="94a39-218">Im folgenden Codebeispiel wird eine [**iuiapplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) -Implementierung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="94a39-218">The following code example demonstrates an [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) implementation:</span></span>


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a><span data-ttu-id="94a39-219">Implementieren eines iuicommandhandler-Adapters</span><span class="sxs-lookup"><span data-stu-id="94a39-219">Implement an IUICommandHandler Adapter</span></span>

<span data-ttu-id="94a39-220">Abhängig vom Entwurf der ursprünglichen Anwendung ist es möglicherweise einfacher, mehrere Befehls Handlerimplementierungen zu haben, oder einen einzelnen Bridging-Befehls Handler, der die vorhandene Anwendungs Befehls Logik aufruft.</span><span class="sxs-lookup"><span data-stu-id="94a39-220">Depending on the design of the original application, it may be easier to have multiple Command handler implementations, or a single bridging Command handler that invokes the existing-application command logic.</span></span> <span data-ttu-id="94a39-221">Viele Anwendungen verwenden \_ für diesen Zweck WM-befehlsnachrichten, bei denen es ausreichend ist, einen einzelnen Befehls Handler für alle Zwecke bereitzustellen, der einfach WM- \_ Befehls Meldungen an das Fenster der obersten Ebene weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="94a39-221">Many applications use WM\_COMMAND messages for this purpose where it is sufficient to provide a single, all-purpose command handler that simply forwards WM\_COMMAND messages to the top-level window.</span></span>

<span data-ttu-id="94a39-222">Bei diesem Ansatz ist jedoch eine spezielle Behandlung für Befehle wie " **Exit** " oder " **Close**" erforderlich.</span><span class="sxs-lookup"><span data-stu-id="94a39-222">However, this approach requires special handling for Commands such as **Exit** or **Close**.</span></span> <span data-ttu-id="94a39-223">Da das Menüband nicht zerstört werden kann, während es eine Fenster Nachricht verarbeitet, \_ sollte die WM close-Nachricht an den UI-Thread der Anwendung gesendet werden und sollte nicht synchron verarbeitet werden, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="94a39-223">Because the Ribbon cannot be destroyed while it's processing a window message, the WM\_CLOSE message should be posted to the UI thread of the application and should not be processed synchronously, as shown in the following example:</span></span>


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a><span data-ttu-id="94a39-224">Migrieren von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="94a39-224">Migrating Resources</span></span>

<span data-ttu-id="94a39-225">Wenn das Manifest der Befehle definiert wurde, die Struktur des Menübands deklariert wurde und der Anwendungscode zum Hosten des Menüband-Frameworks angepasst wurde, ist der letzte Schritt die Angabe von Zeichen folgen-und Bild Ressourcen für jeden Befehl.</span><span class="sxs-lookup"><span data-stu-id="94a39-225">When the manifest of commands has been defined, the structure of the Ribbon has been declared, and the application code adapted to host the Ribbon framework, the final step is the specification of string and image resources for each Command.</span></span>

> [!Note]  
> <span data-ttu-id="94a39-226">Zeichen folgen-und Bild Ressourcen werden in der Regel in der Markup Datei bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="94a39-226">String and image resources are typically provided in the markup file.</span></span> <span data-ttu-id="94a39-227">Sie können jedoch Programm gesteuert durch Implementieren der [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode generiert oder ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="94a39-227">However, they can be generated or replaced programmatically by implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

 

### <a name="string-resources"></a><span data-ttu-id="94a39-228">Zeichen folgen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="94a39-228">String Resources</span></span>

<span data-ttu-id="94a39-229">[**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) ist die häufigste Zeichen folgen Eigenschaft, die für einen Befehl definiert ist.</span><span class="sxs-lookup"><span data-stu-id="94a39-229">[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is the most common string property defined for a Command.</span></span> <span data-ttu-id="94a39-230">Diese werden als Text Beschriftungen für Registerkarten, Gruppen und einzelne Steuerelemente gerendert.</span><span class="sxs-lookup"><span data-stu-id="94a39-230">These are rendered as the text labels for tabs, groups, and individual controls.</span></span> <span data-ttu-id="94a39-231">Eine Bezeichnungs Zeichenfolge aus einem Legacy Menü Element kann in der Regel für einen **Befehl. labeltitle** ohne große Bearbeitung wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94a39-231">A label string from a legacy menu item can typically be re-used for a **Command.LabelTitle** without much editing.</span></span>

<span data-ttu-id="94a39-232">Die folgenden Konventionen haben sich jedoch bei der Einführung des Menübands geändert:</span><span class="sxs-lookup"><span data-stu-id="94a39-232">However, the following conventions have changed with the advent of the Ribbon:</span></span>

-   <span data-ttu-id="94a39-233">Das Auslassungs Zeichen (...), das verwendet wird, um einen Befehl zum Starten des Dialog Felds anzugeben, ist nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="94a39-233">The ellipsis (...) suffix, used to indicate a dialog-launching command, is no longer necessary.</span></span>
-   <span data-ttu-id="94a39-234">Das kaufmännische und-Objekt (&) kann weiterhin verwendet werden, um eine Tastenkombination für einen Befehl anzugeben, der in einem Menü angezeigt wird, die vom Framework unterstützte [**Command. KeyTip**](windowsribbon-element-command-keytip.md) -Eigenschaft erfüllt jedoch einen ähnlichen Zweck.</span><span class="sxs-lookup"><span data-stu-id="94a39-234">The ampersand (&) can still be used to indicate a keyboard-shortcut for a Command that appears in a menu, but the [**Command.Keytip**](windowsribbon-element-command-keytip.md) property supported by the framework fulfills a similar purpose.</span></span>

<span data-ttu-id="94a39-235">Wenn Sie auf das Beispiel Text-Editor zurückverweisen, können die folgenden Zeichen folgen für "labeltitle" und "KeyTip" angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="94a39-235">Referring back to the text editor example, the following strings for LabelTitle and Keytip could be specified:</span></span>



| <span data-ttu-id="94a39-236">Symbol</span><span class="sxs-lookup"><span data-stu-id="94a39-236">Symbol</span></span>           | <span data-ttu-id="94a39-237">Ursprüngliche Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="94a39-237">Original string</span></span> | <span data-ttu-id="94a39-238">Labeltitle-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="94a39-238">LabelTitle string</span></span> | <span data-ttu-id="94a39-239">KeyTip-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="94a39-239">Keytip string</span></span> |
|------------------|-----------------|-------------------|---------------|
| <span data-ttu-id="94a39-240">ID- \_ Datei \_ neu</span><span class="sxs-lookup"><span data-stu-id="94a39-240">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="94a39-241">Neu &</span><span class="sxs-lookup"><span data-stu-id="94a39-241">&New</span></span>            | <span data-ttu-id="94a39-242">Neu &</span><span class="sxs-lookup"><span data-stu-id="94a39-242">&New</span></span>              | <span data-ttu-id="94a39-243">N</span><span class="sxs-lookup"><span data-stu-id="94a39-243">N</span></span>             |
| <span data-ttu-id="94a39-244">ID- \_ Datei \_ Speichern</span><span class="sxs-lookup"><span data-stu-id="94a39-244">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="94a39-245">&speichern</span><span class="sxs-lookup"><span data-stu-id="94a39-245">&Save</span></span>           | <span data-ttu-id="94a39-246">&speichern</span><span class="sxs-lookup"><span data-stu-id="94a39-246">&Save</span></span>             | <span data-ttu-id="94a39-247">E</span><span class="sxs-lookup"><span data-stu-id="94a39-247">S</span></span>             |
| <span data-ttu-id="94a39-248">ID- \_ Datei ( \_ SaveAs)</span><span class="sxs-lookup"><span data-stu-id="94a39-248">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="94a39-249">&speichern unter...</span><span class="sxs-lookup"><span data-stu-id="94a39-249">Save &As…</span></span>       | <span data-ttu-id="94a39-250">&speichern unter</span><span class="sxs-lookup"><span data-stu-id="94a39-250">Save &as</span></span>          | <span data-ttu-id="94a39-251">A</span><span class="sxs-lookup"><span data-stu-id="94a39-251">A</span></span>             |
| <span data-ttu-id="94a39-252">ID- \_ Datei \_ geöffnet</span><span class="sxs-lookup"><span data-stu-id="94a39-252">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="94a39-253">&geöffnet...</span><span class="sxs-lookup"><span data-stu-id="94a39-253">&Open…</span></span>          | <span data-ttu-id="94a39-254">&amp;Open</span><span class="sxs-lookup"><span data-stu-id="94a39-254">&Open</span></span>             | <span data-ttu-id="94a39-255">O</span><span class="sxs-lookup"><span data-stu-id="94a39-255">O</span></span>             |
| <span data-ttu-id="94a39-256">ID- \_ Datei \_ Beenden</span><span class="sxs-lookup"><span data-stu-id="94a39-256">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="94a39-257">&Beenden</span><span class="sxs-lookup"><span data-stu-id="94a39-257">E&xit</span></span>           | <span data-ttu-id="94a39-258">&Beenden</span><span class="sxs-lookup"><span data-stu-id="94a39-258">E&xit</span></span>             | <span data-ttu-id="94a39-259">X</span><span class="sxs-lookup"><span data-stu-id="94a39-259">X</span></span>             |
| <span data-ttu-id="94a39-260">ID- \_ Bearbeitung \_ rückgängig</span><span class="sxs-lookup"><span data-stu-id="94a39-260">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="94a39-261">&rückgängig machen</span><span class="sxs-lookup"><span data-stu-id="94a39-261">&Undo</span></span>           | <span data-ttu-id="94a39-262">Rückgängig</span><span class="sxs-lookup"><span data-stu-id="94a39-262">Undo</span></span>              | <span data-ttu-id="94a39-263">Z</span><span class="sxs-lookup"><span data-stu-id="94a39-263">Z</span></span>             |
| <span data-ttu-id="94a39-264">ID- \_ Bearbeitungs \_ Ausschnitt</span><span class="sxs-lookup"><span data-stu-id="94a39-264">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="94a39-265">Cu&t</span><span class="sxs-lookup"><span data-stu-id="94a39-265">Cu&t</span></span>            | <span data-ttu-id="94a39-266">Cu&t</span><span class="sxs-lookup"><span data-stu-id="94a39-266">Cu&t</span></span>              | <span data-ttu-id="94a39-267">X</span><span class="sxs-lookup"><span data-stu-id="94a39-267">X</span></span>             |
| <span data-ttu-id="94a39-268">ID zum \_ Bearbeiten der \_ Kopie</span><span class="sxs-lookup"><span data-stu-id="94a39-268">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="94a39-269">&Kopie</span><span class="sxs-lookup"><span data-stu-id="94a39-269">&Copy</span></span>           | <span data-ttu-id="94a39-270">&Kopie</span><span class="sxs-lookup"><span data-stu-id="94a39-270">&Copy</span></span>             | <span data-ttu-id="94a39-271">C</span><span class="sxs-lookup"><span data-stu-id="94a39-271">C</span></span>             |
| <span data-ttu-id="94a39-272">ID \_ Bearbeiten, \_ Einfügen</span><span class="sxs-lookup"><span data-stu-id="94a39-272">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="94a39-273">&einfügen</span><span class="sxs-lookup"><span data-stu-id="94a39-273">&Paste</span></span>          | <span data-ttu-id="94a39-274">&einfügen</span><span class="sxs-lookup"><span data-stu-id="94a39-274">&Paste</span></span>            | <span data-ttu-id="94a39-275">V</span><span class="sxs-lookup"><span data-stu-id="94a39-275">V</span></span>             |
| <span data-ttu-id="94a39-276">ID- \_ Bearbeitung \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="94a39-276">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="94a39-277">&löschen</span><span class="sxs-lookup"><span data-stu-id="94a39-277">&Delete</span></span>         | <span data-ttu-id="94a39-278">&löschen</span><span class="sxs-lookup"><span data-stu-id="94a39-278">&Delete</span></span>           | <span data-ttu-id="94a39-279">D</span><span class="sxs-lookup"><span data-stu-id="94a39-279">D</span></span>             |
| <span data-ttu-id="94a39-280">Vergrößern der ID- \_ Ansicht \_</span><span class="sxs-lookup"><span data-stu-id="94a39-280">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="94a39-281">&Zoom...</span><span class="sxs-lookup"><span data-stu-id="94a39-281">&Zoom…</span></span>          | <span data-ttu-id="94a39-282">Zoom</span><span class="sxs-lookup"><span data-stu-id="94a39-282">Zoom</span></span>              | <span data-ttu-id="94a39-283">Z</span><span class="sxs-lookup"><span data-stu-id="94a39-283">Z</span></span>             |



 

<span data-ttu-id="94a39-284">Im folgenden finden Sie eine Liste anderer Zeichen folgen Eigenschaften, die für die meisten Befehle festgelegt werden sollten:</span><span class="sxs-lookup"><span data-stu-id="94a39-284">The following is a list of other string properties which should be set on most Commands:</span></span>

-   [<span data-ttu-id="94a39-285">**Command. labeldescription**</span><span class="sxs-lookup"><span data-stu-id="94a39-285">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)
-   [<span data-ttu-id="94a39-286">**Command. ToolTipTitle**</span><span class="sxs-lookup"><span data-stu-id="94a39-286">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
-   [<span data-ttu-id="94a39-287">**Command. tooltipdescription**</span><span class="sxs-lookup"><span data-stu-id="94a39-287">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)

<span data-ttu-id="94a39-288">Registerkarten, Gruppen und andere Funktionen der Multifunktionsleisten-Benutzeroberfläche können jetzt mit allen angegebenen Zeichen folgen-und Bild Ressourcen deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="94a39-288">Tabs, Groups, and other Ribbon UI features can now be declared with all string and image resources specified.</span></span>

<span data-ttu-id="94a39-289">Im folgenden Menüband-Markup Beispiel werden verschiedene Zeichen folgen Ressourcen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="94a39-289">The following Ribbon markup example demonstrates various string resources:</span></span>


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a><span data-ttu-id="94a39-290">Bild Ressourcen</span><span class="sxs-lookup"><span data-stu-id="94a39-290">Image Resources</span></span>

<span data-ttu-id="94a39-291">Das Menüband-Framework unterstützt Bildformate, die ein viel reicheres Aussehen und Gefühl bieten als die Bildformate, die von vorherigen Menü-und Symbolleisten Komponenten unterstützt</span><span class="sxs-lookup"><span data-stu-id="94a39-291">The Ribbon framework supports image formats that provide a much richer look and feel than the image formats supported by previous menu and toolbar components.</span></span>

<span data-ttu-id="94a39-292">Für Windows 8 und höher unterstützt das Menüband-Framework die folgenden Grafikformate: 32-Bit-ARGB-Bitmap-Dateien (BMP) und Portable Network Graphics-Dateien (PNG) mit Transparenz.</span><span class="sxs-lookup"><span data-stu-id="94a39-292">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="94a39-293">Für Windows 7 und früher müssen Bild Ressourcen dem standardmäßigen BMP-Grafikformat entsprechen, das in Windows verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94a39-293">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="94a39-294">Vorhandene Bilddateien können in beide Formate konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="94a39-294">Existing image files can be converted to either format.</span></span> <span data-ttu-id="94a39-295">Die Ergebnisse sind jedoch möglicherweise kleiner als zufriedenstellend, wenn die Bilddateien Antialiasing und Transparenz nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="94a39-295">However, the results may be less than satisfactory if the image files do not support antialiasing and transparency.</span></span>

 

<span data-ttu-id="94a39-296">Es ist nicht möglich, eine einzelne Standardgröße für Bild Ressourcen im Menüband-Framework anzugeben.</span><span class="sxs-lookup"><span data-stu-id="94a39-296">It is not possible to specify a single default size for image resources in the Ribbon framework.</span></span> <span data-ttu-id="94a39-297">Um das [Adaptive Layout](windowsribbon-templates.md) von Steuerelementen zu unterstützen, können Bilder jedoch in zwei Größen (groß und klein) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="94a39-297">However, to support [adaptive layout](windowsribbon-templates.md) of controls, images can be specified in two sizes (large and small) .</span></span> <span data-ttu-id="94a39-298">Alle Bilder im Menüband-Framework werden entsprechend der dpi-Auflösung (dpi) der Anzeige mit der exakten gerenderten Größe skaliert, die von dieser dpi-Einstellung abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="94a39-298">All images in the Ribbon framework are scaled according to the dots per inch (dpi) resolution of the display with the exact rendered size dependent on this dpi setting.</span></span> <span data-ttu-id="94a39-299">Weitere Informationen finden Sie unter [Angeben von Menüband-Bild Ressourcen](windowsribbon-imageformats.md) .</span><span class="sxs-lookup"><span data-stu-id="94a39-299">See [Specifying Ribbon Image Resources](windowsribbon-imageformats.md) for more information.</span></span>

<span data-ttu-id="94a39-300">Im folgenden Beispiel wird veranschaulicht, wie auf einen Satz von dpi-spezifischen Bildern im Markup verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="94a39-300">The following example demonstrates how a set of dpi-specific images are referenced in markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="94a39-301">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94a39-301">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94a39-302">Angeben von Menüband-Bild Ressourcen</span><span class="sxs-lookup"><span data-stu-id="94a39-302">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 