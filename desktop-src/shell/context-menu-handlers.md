---
description: Beim Einfügen von Kontextmenü Handlern, auch als Kontextmenü Handler oder Verb Handler bezeichnet, handelt es sich um einen Dateityp Handler. Wie bei allen solchen Handlern sind Sie in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Erstellen von Kontextmenü Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b7091483726c322a8ae18bace883af126d404
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "103869308"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="2ab34-104">Erstellen von Kontextmenü Handlern</span><span class="sxs-lookup"><span data-stu-id="2ab34-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="2ab34-105">Beim Einfügen von Kontextmenü Handlern, auch als Kontextmenü Handler oder Verb Handler bezeichnet, handelt es sich um einen Dateityp Handler.</span><span class="sxs-lookup"><span data-stu-id="2ab34-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="2ab34-106">Wie bei allen solchen Handlern sind Sie in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-106">Like all such handlers, they are in-process Component Object Model (COM) objects implemented as DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="2ab34-107">Beim Registrieren von Handlern, die im Kontext von 32-Bit-Anwendungen funktionieren, gibt es spezielle Überlegungen für 64-Bit-Windows: Wenn Shellverben im Kontext einer 32-Bit-Anwendung aufgerufen werden, leitet das WOW64-Subsystem den Dateisystem Zugriff auf einige Pfade um.</span><span class="sxs-lookup"><span data-stu-id="2ab34-107">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="2ab34-108">Wenn der exe-Handler in einem dieser Pfade gespeichert ist, kann in diesem Kontext nicht darauf zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-108">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="2ab34-109">Als Problem Umgehung speichern Sie die exe-Datei in einem Pfad, der nicht umgeleitet wird, oder speichern Sie eine Stubversion der exe-Datei, die die tatsächliche Version gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="2ab34-109">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

<span data-ttu-id="2ab34-110">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="2ab34-110">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="2ab34-111">Kanonische Verben</span><span class="sxs-lookup"><span data-stu-id="2ab34-111">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="2ab34-112">Erweiterte Verben</span><span class="sxs-lookup"><span data-stu-id="2ab34-112">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="2ab34-113">Anpassen eines Kontextmenüs mithilfe statischer Verben</span><span class="sxs-lookup"><span data-stu-id="2ab34-113">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="2ab34-114">Aktivieren des Handlers mithilfe der IDropTarget-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2ab34-114">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="2ab34-115">Angeben der Position und Reihenfolge statischer Verben</span><span class="sxs-lookup"><span data-stu-id="2ab34-115">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="2ab34-116">Positionieren von Verben am oberen oder unteren Rand des Menüs</span><span class="sxs-lookup"><span data-stu-id="2ab34-116">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="2ab34-117">Erstellen von statischen kaskadierenden Menüs</span><span class="sxs-lookup"><span data-stu-id="2ab34-117">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="2ab34-118">Erzielen von dynamischem Verhalten für statische Verben mithilfe der erweiterten Abfrage Syntax</span><span class="sxs-lookup"><span data-stu-id="2ab34-118">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="2ab34-119">Veraltet: Zuordnen von Verben zu dynamischer Datenaustausch Befehlen</span><span class="sxs-lookup"><span data-stu-id="2ab34-119">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="2ab34-120">Abschließen der Verb Implementierungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="2ab34-120">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="2ab34-121">Anpassen des Kontextmenüs für vordefinierte Shellobjekte</span><span class="sxs-lookup"><span data-stu-id="2ab34-121">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="2ab34-122">Erweitern eines neuen Untermenüs</span><span class="sxs-lookup"><span data-stu-id="2ab34-122">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="2ab34-123">Unterdrücken von Verbs</span><span class="sxs-lookup"><span data-stu-id="2ab34-123">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="2ab34-124">Verwenden des Verb Auswahl Modells</span><span class="sxs-lookup"><span data-stu-id="2ab34-124">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="2ab34-125">Verwenden von Element Attributen</span><span class="sxs-lookup"><span data-stu-id="2ab34-125">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="2ab34-126">Implementieren von benutzerdefinierten Verben für Ordner durch Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="2ab34-126">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="2ab34-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ab34-127">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="2ab34-128">Kanonische Verben</span><span class="sxs-lookup"><span data-stu-id="2ab34-128">Canonical Verbs</span></span>

<span data-ttu-id="2ab34-129">Anwendungen sind im Allgemeinen für die Bereitstellung lokalisierter Anzeige Zeichenfolgen für die von Ihnen definierten Verben verantwortlich</span><span class="sxs-lookup"><span data-stu-id="2ab34-129">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="2ab34-130">Um jedoch eine gewisse Sprachunabhängigkeit zu gewährleisten, definiert das System einen Standardsatz häufig verwendeter Verben, die als kanonische Verben bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-130">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="2ab34-131">Dem Benutzer wird nie ein kanonisches Verb angezeigt, das in jeder Benutzeroberflächen Sprache verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2ab34-131">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="2ab34-132">Das System verwendet den kanonischen Namen, um automatisch eine ordnungsgemäß lokalisierte Anzeige Zeichenfolge zu generieren.</span><span class="sxs-lookup"><span data-stu-id="2ab34-132">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="2ab34-133">Beispielsweise wird die Anzeige Zeichenfolge des geöffneten **Verbs auf ein** englisches System und auf das deutsche Äquivalent auf einem deutschen System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-133">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>



| <span data-ttu-id="2ab34-134">Kanonisches Verb</span><span class="sxs-lookup"><span data-stu-id="2ab34-134">Canonical verb</span></span> | <span data-ttu-id="2ab34-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ab34-135">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="2ab34-136">Öffnen</span><span class="sxs-lookup"><span data-stu-id="2ab34-136">Open</span></span>           | <span data-ttu-id="2ab34-137">Öffnet die Datei oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="2ab34-137">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="2ab34-138">OpenNew</span><span class="sxs-lookup"><span data-stu-id="2ab34-138">Opennew</span></span>        | <span data-ttu-id="2ab34-139">Öffnet die Datei oder den Ordner in einem neuen Fenster.</span><span class="sxs-lookup"><span data-stu-id="2ab34-139">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="2ab34-140">Drucken</span><span class="sxs-lookup"><span data-stu-id="2ab34-140">Print</span></span>          | <span data-ttu-id="2ab34-141">Druckt die Datei.</span><span class="sxs-lookup"><span data-stu-id="2ab34-141">Prints the file.</span></span>                                                     |
| <span data-ttu-id="2ab34-142">Printto</span><span class="sxs-lookup"><span data-stu-id="2ab34-142">Printto</span></span>        | <span data-ttu-id="2ab34-143">Ermöglicht dem Benutzer das Drucken einer Datei durchziehen auf ein Drucker Objekt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-143">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="2ab34-144">Erkunden</span><span class="sxs-lookup"><span data-stu-id="2ab34-144">Explore</span></span>        | <span data-ttu-id="2ab34-145">Öffnet den Windows-Explorer mit ausgewähltem Ordner.</span><span class="sxs-lookup"><span data-stu-id="2ab34-145">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="2ab34-146">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2ab34-146">Properties</span></span>     | <span data-ttu-id="2ab34-147">Öffnet das Eigenschaften Blatt des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2ab34-147">Opens the object's property sheet.</span></span>                                   |



 

> [!Note]  
> <span data-ttu-id="2ab34-148">Das **Printto** -Verb ist auch kanonisch, wird aber nie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-148">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="2ab34-149">Durch die Einbindung kann der Benutzer eine Datei drucken, indem er Sie auf ein Drucker Objekt zieht.</span><span class="sxs-lookup"><span data-stu-id="2ab34-149">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

 

<span data-ttu-id="2ab34-150">Kontextmenü Handler können **mithilfe von \_** [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) und **GCS \_ Verba** eigene kanonische Verben bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-150">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="2ab34-151">Das System verwendet die kanonischen Verben als zweiten Parameter (*lpoperation*), der an [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)übergeben wird, und ist [**cminvokecommandinfo**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). **lpverb** -Member, der an die [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-151">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="2ab34-152">Erweiterte Verben</span><span class="sxs-lookup"><span data-stu-id="2ab34-152">Extended Verbs</span></span>

<span data-ttu-id="2ab34-153">Wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, zeigt das Kontextmenü die Standard Verben an.</span><span class="sxs-lookup"><span data-stu-id="2ab34-153">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="2ab34-154">Möglicherweise möchten Sie Befehle in einigen Kontextmenüs hinzufügen und unterstützen, die nicht in jedem Kontextmenü angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-154">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="2ab34-155">Beispielsweise können Sie über Befehle verfügen, die nicht häufig verwendet werden oder für erfahrene Benutzer gedacht sind.</span><span class="sxs-lookup"><span data-stu-id="2ab34-155">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="2ab34-156">Aus diesem Grund können Sie auch ein oder mehrere erweiterte Verben definieren.</span><span class="sxs-lookup"><span data-stu-id="2ab34-156">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="2ab34-157">Diese Verben ähneln normalen Verben, werden jedoch durch die Art und Weise, in der Sie registriert sind, von normalen Verben unterschieden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-157">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="2ab34-158">Um Zugriff auf Erweiterte Verben zu erhalten, muss der Benutzer mit der rechten Maustaste auf ein Objekt klicken, während er die UMSCHALTTASTE drückt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-158">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="2ab34-159">Wenn der Benutzer dies tut, werden die erweiterten Verben zusätzlich zu den Standard Verben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-159">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="2ab34-160">Sie können die Registrierung verwenden, um ein oder mehrere erweiterte Verben zu definieren.</span><span class="sxs-lookup"><span data-stu-id="2ab34-160">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="2ab34-161">Die zugeordneten Befehle werden nur angezeigt, wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, während gleichzeitig die UMSCHALTTASTE gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-161">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="2ab34-162">Wenn Sie ein Verb als erweitert definieren möchten, fügen Sie dem Unterschlüssel des Verbs einen "erweiterten" **reg \_ SZ** -Wert hinzu.</span><span class="sxs-lookup"><span data-stu-id="2ab34-162">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="2ab34-163">Dem Wert dürfen keine Daten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-163">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="2ab34-164">Anpassen eines Kontextmenüs mithilfe statischer Verben</span><span class="sxs-lookup"><span data-stu-id="2ab34-164">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="2ab34-165">Nachdem Sie [ein statisches oder dynamisches Verb für das Kontextmenü ausgewählt](shortcut-choose-method.md) haben, können Sie das Kontextmenü für einen Dateityp erweitern, indem Sie für den Dateityp ein statisches Verb registrieren.</span><span class="sxs-lookup"><span data-stu-id="2ab34-165">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="2ab34-166">Fügen Sie hierzu unter dem Unterschlüssel für die ProgID der Anwendung, die dem Dateityp zugeordnet ist, einen **shellunterschlüssel** hinzu.</span><span class="sxs-lookup"><span data-stu-id="2ab34-166">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="2ab34-167">Optional können Sie ein Standard-Verb für den Dateityp definieren, indem Sie es als Standardwert für den **shellunterschlüssel** festlegen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-167">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="2ab34-168">Das Standardverb wird zuerst im Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-168">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="2ab34-169">Der Zweck besteht darin, die Shell mit einem Verb zu versehen, das Sie verwenden kann, wenn die [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) -Funktion aufgerufen wird, aber kein Verb angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-169">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="2ab34-170">Die Shell wählt nicht notwendigerweise das Standard Verb aus, wenn **ShellExecuteEx** auf diese Weise verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-170">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="2ab34-171">Die Shell verwendet das erste verfügbare Verb in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="2ab34-171">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="2ab34-172">Das Standardverb</span><span class="sxs-lookup"><span data-stu-id="2ab34-172">The default verb</span></span>
2.  <span data-ttu-id="2ab34-173">Das erste Verb in der Registrierung, wenn die Verb Reihenfolge angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2ab34-173">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="2ab34-174">Das **geöffnete** Verb</span><span class="sxs-lookup"><span data-stu-id="2ab34-174">The **Open** verb</span></span>
4.  <span data-ttu-id="2ab34-175">Das **geöffnete with** -Verb</span><span class="sxs-lookup"><span data-stu-id="2ab34-175">The **Open With** verb</span></span>

<span data-ttu-id="2ab34-176">Wenn keines der aufgelisteten Verben verfügbar ist, schlägt der Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="2ab34-176">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="2ab34-177">Erstellen Sie einen Unterschlüssel für jedes Verb, das Sie unter dem shellsubschlüssel hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="2ab34-177">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="2ab34-178">Jeder dieser Unterschlüssel muss über einen **reg \_ SZ** -Wert verfügen, der auf die Anzeige Zeichenfolge des Verbs (lokalisierte Zeichenfolge) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2ab34-178">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="2ab34-179">Erstellen Sie für jeden Verb Unterschlüssel einen Befehls Unterschlüssel, wobei der Standardwert auf die Befehlszeile zum Aktivieren der Elemente festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2ab34-179">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="2ab34-180">Für kanonische Verben wie z. b. **Öffnen** und **Drucken** können Sie die Anzeige Zeichenfolge weglassen, da das System automatisch eine ordnungsgemäß lokalisierte Zeichenfolge anzeigt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-180">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="2ab34-181">Wenn Sie für nicht kanonische Verben die Anzeige Zeichenfolge weglassen, wird die Verb Zeichenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-181">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="2ab34-182">Beachten Sie im folgenden Registrierungs Beispiel Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2ab34-182">In the following registry example, note that:</span></span>

-   <span data-ttu-id="2ab34-183">Da es sich bei **doit** nicht um ein kanonisches Verb handelt, wird ihm ein Anzeige Name zugewiesen, der durch Drücken der D-Taste ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2ab34-183">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="2ab34-184">Das **Printto** -Verb wird nicht im Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-184">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="2ab34-185">Allerdings ermöglicht die Einbindung in die Registrierung dem Benutzer das Drucken von Dateien, indem Sie Sie auf einem Druckersymbol ablegen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-185">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="2ab34-186">Ein Unterschlüssel wird für jedes Verb angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-186">One subkey is shown for each verb.</span></span> <span data-ttu-id="2ab34-187">**%1** stellt den Dateinamen und **%2** für den Drucker Namen dar.</span><span class="sxs-lookup"><span data-stu-id="2ab34-187">**%1** represents the file name and **%2** the printer name.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

<span data-ttu-id="2ab34-188">Das folgende Diagramm veranschaulicht die Erweiterung des Kontextmenüs in Übereinstimmung mit den oben aufgeführten Registrierungs Einträgen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-188">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="2ab34-189">In diesem Kontextmenü sind die Verben Open, **do**, and **Print** in Ihrem Menü **geöffnet**, wobei **es** als Standard Verb angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-189">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![Screenshot des Kontextmenüs "Do it default Verb"](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="2ab34-191">Aktivieren des Handlers mithilfe der IDropTarget-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2ab34-191">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="2ab34-192">Dynamischer Datenaustausch (DDE) ist veraltet. Verwenden Sie stattdessen [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="2ab34-192">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="2ab34-193">**IDropTarget** ist stabiler und bietet bessere Aktivierungs Unterstützung, da es die COM-Aktivierung des Handlers verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ab34-193">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="2ab34-194">Bei der Auswahl mehrerer Elemente unterliegt **IDropTarget** nicht den Einschränkungen für die Puffergröße, die sowohl in DDE als auch in der Datei " [**kreateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)" gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-194">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="2ab34-195">Außerdem werden Elemente als Datenobjekt an die Anwendung übergeben, das mithilfe der [**shkreateshellitemarrayfromdataobject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) -Funktion in ein Element Array konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2ab34-195">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="2ab34-196">Dies ist einfacher und verliert keine Namespace Informationen, die auftreten, wenn das Element in einen Pfad für Befehlszeilen-oder DDE-Protokolle konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-196">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="2ab34-197">Weitere Informationen zu [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -und Shell-Abfragen für Datei Zuordnungs Attribute finden Sie unter [wahrgenommene Typen und Anwendungs Registrierung](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="2ab34-197">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="2ab34-198">Angeben der Position und Reihenfolge statischer Verben</span><span class="sxs-lookup"><span data-stu-id="2ab34-198">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="2ab34-199">Verben werden normalerweise in einem Kontextmenü basierend auf der Enumeration angeordnet. die Enumeration basiert zuerst auf der Reihenfolge des Association-Arrays und dann auf der Reihenfolge der Elemente im Association-Array, wie in der Sortierreihenfolge der Registrierung definiert.</span><span class="sxs-lookup"><span data-stu-id="2ab34-199">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="2ab34-200">Verben können durch Angabe des Standardwerts für den shellunterschlüssel für den Zuordnungs Eintrag geordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-200">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="2ab34-201">Dieser Standardwert kann ein einzelnes Element enthalten, das an der obersten Position des Kontextmenüs angezeigt wird, oder eine Liste von Elementen, die durch Leerzeichen oder Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="2ab34-201">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="2ab34-202">Im letzteren Fall ist das erste Element in der Liste das Standardelement, und die anderen Verben werden direkt unterhalb in der angegebenen Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-202">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="2ab34-203">Der folgende Registrierungs Eintrag erzeugt z. b. Kontextmenü Verben in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="2ab34-203">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="2ab34-204">Anzeige</span><span class="sxs-lookup"><span data-stu-id="2ab34-204">Display</span></span>
2.  <span data-ttu-id="2ab34-205">Geschenken</span><span class="sxs-lookup"><span data-stu-id="2ab34-205">Gadgets</span></span>
3.  <span data-ttu-id="2ab34-206">Personalization</span><span class="sxs-lookup"><span data-stu-id="2ab34-206">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="2ab34-207">Entsprechend erzeugt der folgende Registrierungs Eintrag Kontextmenü Verben in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="2ab34-207">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="2ab34-208">Personalization</span><span class="sxs-lookup"><span data-stu-id="2ab34-208">Personalization</span></span>
2.  <span data-ttu-id="2ab34-209">Geschenken</span><span class="sxs-lookup"><span data-stu-id="2ab34-209">Gadgets</span></span>
3.  <span data-ttu-id="2ab34-210">Anzeige</span><span class="sxs-lookup"><span data-stu-id="2ab34-210">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="2ab34-211">Positionieren von Verben am oberen oder unteren Rand des Menüs</span><span class="sxs-lookup"><span data-stu-id="2ab34-211">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="2ab34-212">Das folgende Registrierungs Attribut kann verwendet werden, um ein Verb am oberen oder unteren Rand des Menüs zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="2ab34-212">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="2ab34-213">Wenn mehrere Verben vorhanden sind, die dieses Attribut angeben, erhält das letzte zu diesem Zweck Priorität:</span><span class="sxs-lookup"><span data-stu-id="2ab34-213">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="2ab34-214">Erstellen von statischen kaskadierenden Menüs</span><span class="sxs-lookup"><span data-stu-id="2ab34-214">Creating Static Cascading Menus</span></span>

<span data-ttu-id="2ab34-215">In Windows 7 und höher wird die Cascading-Menü Implementierung durch Registrierungs Einstellungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-215">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="2ab34-216">Vor Windows 7 war die Erstellung von kaskadierenden Menüs nur durch die Implementierung der [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) -Schnittstelle möglich.</span><span class="sxs-lookup"><span data-stu-id="2ab34-216">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="2ab34-217">In Windows 7 und höher sollten Sie auf com-Code basierende Lösungen nur zugreifen, wenn die statischen Methoden unzureichend sind.</span><span class="sxs-lookup"><span data-stu-id="2ab34-217">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="2ab34-218">Der folgende Screenshot zeigt ein Beispiel für ein Cascading-Menü.</span><span class="sxs-lookup"><span data-stu-id="2ab34-218">The following screen shot provides an example of a cascading menu.</span></span>

![Screenshot mit einem Beispiel für ein Cascading-Menü](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="2ab34-220">In Windows 7 und höher gibt es drei Möglichkeiten, Kaskadierende Menüs zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="2ab34-220">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="2ab34-221">Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag Unterbefehle</span><span class="sxs-lookup"><span data-stu-id="2ab34-221">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="2ab34-222">Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "extendedsubcommandskey"</span><span class="sxs-lookup"><span data-stu-id="2ab34-222">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="2ab34-223">Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2ab34-223">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="2ab34-224">Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag Unterbefehle</span><span class="sxs-lookup"><span data-stu-id="2ab34-224">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="2ab34-225">In Windows 7 und höher können Sie mithilfe des Eintrags Unterbefehle Cascading-Menüs erstellen, indem Sie das folgende Verfahren verwenden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-225">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="2ab34-226">**So erstellen Sie ein Cascading-Menü mithilfe des Eintrags "Unterbefehle"**</span><span class="sxs-lookup"><span data-stu-id="2ab34-226">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="2ab34-227">Erstellen Sie unter **HKEY \_ Classes \_ root** \\ *ProgID* \\ **Shell** einen Unterschlüssel, um Ihr Cascading-Menü darzustellen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-227">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="2ab34-228">In diesem Beispiel geben wir diesem Unterschlüssel den Namen *cascadetest*.</span><span class="sxs-lookup"><span data-stu-id="2ab34-228">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="2ab34-229">Stellen Sie sicher, dass der Standardwert des unter Schlüssels *caskadetten Test* leer ist und als **(Wert nicht festgelegt)** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-229">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="2ab34-230">Fügen Sie dem Unterschlüssel *caskadetten Test* einen MUIVerb-Eintrag vom Typ **reg \_ SZ** hinzu, und weisen Sie ihm den Text zu, der im Kontextmenü als Name angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-230">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="2ab34-231">In diesem Beispiel weisen wir ihm das Menü "Test Cascade Menu" zu.</span><span class="sxs-lookup"><span data-stu-id="2ab34-231">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="2ab34-232">Fügen Sie Ihrem *caskadetten Test* -Unterschlüssel einen Eintrag Unterbefehle des Typs **reg \_ SZ** , dem die Liste zugewiesen ist, demlimited durch Semikolons, der Verben hinzu, die im Menü angezeigt werden sollen, in der Reihenfolge der Darstellung.</span><span class="sxs-lookup"><span data-stu-id="2ab34-232">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="2ab34-233">Hier können Sie beispielsweise eine Reihe von vom System bereitgestellten Verben zuweisen:</span><span class="sxs-lookup"><span data-stu-id="2ab34-233">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="2ab34-234">Wenn Sie benutzerdefinierte Verben verwenden, implementieren Sie Sie mit einer der statischen Verb Implementierungs Methoden, und Listen Sie diese unter dem **commandstore** -Unterschlüssel auf, wie in diesem Beispiel für ein fiktives Verb *verbname* gezeigt:</span><span class="sxs-lookup"><span data-stu-id="2ab34-234">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> <span data-ttu-id="2ab34-235">Diese Methode hat den Vorteil, dass die benutzerdefinierten Verben einmalig registriert und wieder verwendet werden können, indem Sie den Verb Namen unter dem Eintrag Unterbefehle auflisten.</span><span class="sxs-lookup"><span data-stu-id="2ab34-235">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="2ab34-236">Allerdings muss die Anwendung über die Berechtigung zum Ändern der Registrierung unter **HKEY \_ local \_ Machine** verfügen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-236">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="2ab34-237">Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "extendedsubcommandskey"</span><span class="sxs-lookup"><span data-stu-id="2ab34-237">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="2ab34-238">In Windows 7 und höher können Sie den Eintrag extendedsubcommandkey verwenden, um erweiterte Cascading Menüs zu erstellen: Cascading Menüs in kaskadierenden Menüs.</span><span class="sxs-lookup"><span data-stu-id="2ab34-238">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="2ab34-239">Der folgende Screenshot zeigt ein Beispiel für ein erweitertes Cascading-Menü.</span><span class="sxs-lookup"><span data-stu-id="2ab34-239">The following screen shot is an example of an extended cascading menu.</span></span>

![Screenshot mit erweitertem Cascading-Menü für Geräte](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="2ab34-241">Da **HKEY \_ Classes \_ root** eine Kombination aus **HKEY \_ Current \_ User** und **HKEY \_ local \_ Machine** ist, können Sie alle benutzerdefinierten Verben unter dem Unterschlüssel **HKEY \_ Current \_ User** \\ **Software** \\ **Classes** registrieren.</span><span class="sxs-lookup"><span data-stu-id="2ab34-241">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="2ab34-242">Der Hauptvorteil besteht darin, dass keine erhöhte Berechtigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2ab34-242">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="2ab34-243">Außerdem können andere Dateizuordnungen diesen gesamten Satz von Verben wieder verwenden, indem Sie den gleichen extendedsubcommandskey-Unterschlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="2ab34-243">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="2ab34-244">Wenn Sie diesen Versatz nicht wieder verwenden müssen, können Sie die Verben unter dem übergeordneten Element auflisten, jedoch sicherstellen, dass der Standardwert des übergeordneten Elements leer ist.</span><span class="sxs-lookup"><span data-stu-id="2ab34-244">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="2ab34-245">**So erstellen Sie ein Cascading-Menü mithilfe eines extendedsubcommandskey-Eintrags**</span><span class="sxs-lookup"><span data-stu-id="2ab34-245">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="2ab34-246">Erstellen Sie unter **HKEY \_ Classes \_ root** \\ *ProgID* \\ **Shell** einen Unterschlüssel, um Ihr Cascading-Menü darzustellen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-246">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="2ab34-247">In diesem Beispiel geben wir diesem Unterschlüssel den Namen " *CascadeTest2*".</span><span class="sxs-lookup"><span data-stu-id="2ab34-247">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="2ab34-248">Stellen Sie sicher, dass der Standardwert des unter Schlüssels *caskadetten Test* leer ist und als **(Wert nicht festgelegt)** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-248">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="2ab34-249">Fügen Sie dem Unterschlüssel *caskadetten Test* einen MUIVerb-Eintrag vom Typ **reg \_ SZ** hinzu, und weisen Sie ihm den Text zu, der im Kontextmenü als Name angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-249">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="2ab34-250">In diesem Beispiel weisen wir ihm das Menü "Test Cascade Menu" zu.</span><span class="sxs-lookup"><span data-stu-id="2ab34-250">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="2ab34-251">Fügen Sie unter dem Unterschlüssel *caskadetten Test* , den Sie erstellt haben, einen Unterschlüssel **extendedsubcommandskey** hinzu, und fügen Sie dann die Dokument Unterbefehle (vom Typ " **reg \_ SZ** ") hinzu. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2ab34-251">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    <span data-ttu-id="2ab34-252">Stellen Sie sicher, dass der Standardwert des unter Schlüssels *Test Cascade Menu 2* leer und als **(Wert nicht festgelegt)** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-252">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="2ab34-253">Füllen Sie die subverben mithilfe einer der folgenden statischen Verb Implementierungen auf.</span><span class="sxs-lookup"><span data-stu-id="2ab34-253">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="2ab34-254">Beachten Sie, dass der commandflags-Unterschlüssel expcmdflags-Werte darstellt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-254">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="2ab34-255">Wenn Sie ein Trennzeichen vor oder nach dem kaskadierenden Menü Element hinzufügen möchten, verwenden Sie ECF \_ separatorbefore (0x20) oder ECF \_ separatorafter (0x40).</span><span class="sxs-lookup"><span data-stu-id="2ab34-255">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="2ab34-256">Eine Beschreibung dieser Flags von Windows 7 und höher finden Sie unter [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="2ab34-256">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="2ab34-257">ECF \_ separatorbefore funktioniert nur für Menü Elemente der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="2ab34-257">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="2ab34-258">MUIVerb ist vom Typ **reg \_ SZ**, und commandflags ist vom Typ **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2ab34-258">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

<span data-ttu-id="2ab34-259">Der folgende Screenshot zeigt eine Abbildung der vorherigen Beispiele für den Registrierungsschlüssel Eintrag.</span><span class="sxs-lookup"><span data-stu-id="2ab34-259">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![Screenshot mit einem Beispiel für ein kaskadieres Menü, das die Auswahl von Editor und WordPad anzeigt](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="2ab34-261">Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2ab34-261">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="2ab34-262">Eine weitere Option zum Hinzufügen von Verben zu einem kaskadierenden Menü ist die Verwendung von [**IExplorerCommand:: enumsubcommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="2ab34-262">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="2ab34-263">Diese Methode ermöglicht Datenquellen, die ihre Befehls Modul Befehle über [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) bereitstellen, diese Befehle als Verben in einem Kontextmenü zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-263">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="2ab34-264">In Windows 7 und höher können Sie die gleiche Verb-Implementierung mithilfe von [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) bereitstellen, wie Sie mit [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)möglich sind.</span><span class="sxs-lookup"><span data-stu-id="2ab34-264">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="2ab34-265">Die folgenden beiden Screenshots veranschaulichen die Verwendung von kaskadierenden Menüs im Ordner " **Geräte** ".</span><span class="sxs-lookup"><span data-stu-id="2ab34-265">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Screenshot, der ein Beispiel für ein kaskadieres Menü im Geräte Ordner anzeigt.](images/file-assoc/filecascademenu.png)

<span data-ttu-id="2ab34-267">Der folgende Screenshot veranschaulicht eine weitere Implementierung eines kaskadierenden Menüs im **Geräte** Ordner.</span><span class="sxs-lookup"><span data-stu-id="2ab34-267">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![Screenshot mit einem Beispiel für ein kaskadieres Menü im Geräte Ordner](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="2ab34-269">Da [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) nur die Prozess interne Aktivierung unterstützt, empfiehlt es sich, von shelldatenquellen zu verwenden, die die Implementierung zwischen Befehlen und Kontextmenüs freigeben müssen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-269">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="2ab34-270">Erzielen von dynamischem Verhalten für statische Verben mithilfe der erweiterten Abfrage Syntax</span><span class="sxs-lookup"><span data-stu-id="2ab34-270">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="2ab34-271">Mit der erweiterten Abfrage Syntax (AQS) kann eine Bedingung ausgedrückt werden, die mithilfe von Eigenschaften aus dem Element ausgewertet wird, für das das Verb instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-271">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="2ab34-272">Dieses System funktioniert nur mit schnellen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2ab34-272">This system works only with fast properties.</span></span> <span data-ttu-id="2ab34-273">Dies sind Eigenschaften, die die Shell-Datenquelle so schnell meldet, dass \* \* \* [\* shcolstate \_ langsam \* \* \*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) \* aus [**IShellFolder2:: getdefaultcolumnstate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate)nicht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-273">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="2ab34-274">Windows 7 und höher unterstützen kanonische Werte, mit denen Probleme bei lokalisierten Builds vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-274">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="2ab34-275">Die folgende kanonische Syntax ist für lokalisierte Builds erforderlich, um diese Windows 7-Erweiterung nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="2ab34-275">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="2ab34-276">Im folgenden Beispiel Registrierungs Eintrag:</span><span class="sxs-lookup"><span data-stu-id="2ab34-276">In the following example registry entry:</span></span>

-   <span data-ttu-id="2ab34-277">Der **appliesTo** -Wert steuert, ob das Verb angezeigt oder ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-277">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="2ab34-278">Der defaultappliesto-Wert steuert, welches Verb der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="2ab34-278">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="2ab34-279">Der hasluashield-Wert steuert, ob ein Schild für die Benutzerkontensteuerung (User Account Control, UAC) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-279">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="2ab34-280">In diesem Beispiel macht der **defaultappliesto** -Wert dieses Verb als Standardwert für jede Datei mit dem Wort "exampleText1" im Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-280">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="2ab34-281">Der **appliesTo** -Wert aktiviert das Verb für jede Datei mit dem Namen "exampleText1" im Namen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-281">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="2ab34-282">Der Wert **hasluashield** zeigt das Schild für Dateien mit dem Namen "exampleText2" im Namen an.</span><span class="sxs-lookup"><span data-stu-id="2ab34-282">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="2ab34-283">Fügen Sie den **Befehls** Unterschlüssel und einen Wert hinzu:</span><span class="sxs-lookup"><span data-stu-id="2ab34-283">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="2ab34-284">Informationen zur Windows 7-Registrierung finden Sie unter Stamm Laufwerk der **HKEY- \_ Klassen \_** \\  als Beispiel für BitLocker-Verben, die die folgende Methode verwenden:</span><span class="sxs-lookup"><span data-stu-id="2ab34-284">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="2ab34-285">AppliesTo = System. Volume. bitlockerprotection: = 2</span><span class="sxs-lookup"><span data-stu-id="2ab34-285">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="2ab34-286">System. Volume. bitlockerrequirements Sadmin: = System. structuredquerytype. Boolean \# true</span><span class="sxs-lookup"><span data-stu-id="2ab34-286">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="2ab34-287">Weitere Informationen zu AQS finden Sie unter [Erweiterte Abfrage Syntax](../search/-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="2ab34-287">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="2ab34-288">Veraltet: Zuordnen von Verben zu dynamischer Datenaustausch Befehlen</span><span class="sxs-lookup"><span data-stu-id="2ab34-288">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="2ab34-289">DDE ist veraltet. Verwenden Sie stattdessen [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="2ab34-289">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="2ab34-290">DDE ist veraltet, da es sich auf eine Übertragungs Fenster Meldung bezieht, um den DDE-Server zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2ab34-290">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="2ab34-291">Ein DDE-Server reagiert nicht mehr auf die Meldung des Übertragungs Fensters</span><span class="sxs-lookup"><span data-stu-id="2ab34-291">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="2ab34-292">Es kommt häufig vor, dass eine einzelne gesteckte Anwendung alle nachfolgenden Abstürze über die Benutzeroberflächen hinweg verursacht.</span><span class="sxs-lookup"><span data-stu-id="2ab34-292">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="2ab34-293">Die [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Methode ist robuster und bietet eine bessere Aktivierungs Unterstützung, da Sie die COM-Aktivierung des Handlers verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ab34-293">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="2ab34-294">Bei der Auswahl mehrerer Elemente unterliegt **IDropTarget** nicht den Einschränkungen für die Puffergröße, die sowohl in DDE als auch in der Datei " [**kreateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)" gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-294">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="2ab34-295">Außerdem werden Elemente als Datenobjekt an die Anwendung übergeben, das mithilfe der [**shkreateshellitemarrayfromdataobject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) -Funktion in ein Element Array konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2ab34-295">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="2ab34-296">Dies ist einfacher und verliert keine Namespace Informationen, die auftreten, wenn das Element in einen Pfad für Befehlszeilen-oder DDE-Protokolle konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-296">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="2ab34-297">Weitere Informationen zu [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -und Shell-Abfragen für Datei Zuordnungs Attribute finden Sie unter [wahrgenommene Typen und Anwendungs Registrierung](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="2ab34-297">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="2ab34-298">Abschließen der Verb Implementierungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="2ab34-298">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="2ab34-299">Die folgenden Aufgaben für das Implementieren von Verben sind für statische und dynamische Verb Implementierungen von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="2ab34-299">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="2ab34-300">Weitere Informationen zu dynamischen Verben finden [Sie unter Anpassen eines Kontextmenüs mithilfe dynamischer Verben](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="2ab34-300">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="2ab34-301">Anpassen des Kontextmenüs für vordefinierte Shellobjekte</span><span class="sxs-lookup"><span data-stu-id="2ab34-301">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="2ab34-302">Viele vordefinierte Shellobjekte verfügen über Kontextmenüs, die angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="2ab34-302">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="2ab34-303">Registrieren Sie den Befehl auf die gleiche Weise, wie Sie typische Dateitypen registrieren, aber verwenden Sie den Namen des vordefinierten Objekts als Dateityp Namen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-303">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="2ab34-304">Eine Liste der vordefinierten Objekte finden Sie im Abschnitt mit den *vordefinierten shellobjekten* unter [Erstellen von Shellerweiterungs Handlern](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="2ab34-304">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="2ab34-305">Die vordefinierten Shellobjekte, deren Kontextmenüs durch das Hinzufügen von Verben in der Registrierung angepasst werden können, werden in der Tabelle mit dem Wort "Verb" markiert.</span><span class="sxs-lookup"><span data-stu-id="2ab34-305">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="2ab34-306">Erweitern eines neuen Untermenüs</span><span class="sxs-lookup"><span data-stu-id="2ab34-306">Extending a New Submenu</span></span>

<span data-ttu-id="2ab34-307">Wenn ein Benutzer das Menü **Datei** in Windows-Explorer öffnet, ist einer der angezeigten Befehle **neu**.</span><span class="sxs-lookup"><span data-stu-id="2ab34-307">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="2ab34-308">Wenn Sie diesen Befehl auswählen, wird ein Untermenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-308">Selecting this command displays a submenu.</span></span> <span data-ttu-id="2ab34-309">Standardmäßig enthält das Untermenü zwei Befehle, **Ordner** und Verknüpfungen, die es Benutzern **ermöglichen, unter** Ordner und Verknüpfungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-309">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="2ab34-310">Dieses Untermenü kann so erweitert werden, dass es Datei Erstellungs Befehle für einen beliebigen Dateityp einschließt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-310">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="2ab34-311">Wenn Sie dem **neuen** Untermenü einen Befehl zum Erstellen von Dateien hinzufügen möchten, müssen die Dateien Ihrer Anwendung über einen zugeordneten Dateityp verfügen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-311">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="2ab34-312">Fügen Sie einen **ShellNew** -Unterschlüssel unter dem Dateinamen ein.</span><span class="sxs-lookup"><span data-stu-id="2ab34-312">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="2ab34-313">Wenn der **neue** Befehl im Menü **Datei** ausgewählt ist, fügt die Shell den Dateityp dem **neuen** Untermenü hinzu.</span><span class="sxs-lookup"><span data-stu-id="2ab34-313">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="2ab34-314">Die Anzeige Zeichenfolge des Befehls ist die beschreibende Zeichenfolge, die der ProgID des Programms zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-314">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="2ab34-315">Um die Datei Erstellungs Methode anzugeben, weisen Sie einen oder mehrere Datenwerte dem **ShellNew** -Unterschlüssel zu.</span><span class="sxs-lookup"><span data-stu-id="2ab34-315">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="2ab34-316">In der folgenden Tabelle sind die verfügbaren Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-316">The available values are listed in the following table.</span></span>



| <span data-ttu-id="2ab34-317">ShellNew-Unterschlüssel Wert</span><span class="sxs-lookup"><span data-stu-id="2ab34-317">ShellNew subkey value</span></span> | <span data-ttu-id="2ab34-318">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ab34-318">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab34-319">Befehl</span><span class="sxs-lookup"><span data-stu-id="2ab34-319">Command</span></span>               | <span data-ttu-id="2ab34-320">Führt eine Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="2ab34-320">Executes an application.</span></span> <span data-ttu-id="2ab34-321">Dieser **reg \_ SZ** -Wert gibt den Pfad der Anwendung an, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ab34-321">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="2ab34-322">Beispielsweise können Sie festlegen, dass ein Assistent gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-322">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="2ab34-323">Daten</span><span class="sxs-lookup"><span data-stu-id="2ab34-323">Data</span></span>                  | <span data-ttu-id="2ab34-324">Erstellt eine Datei mit den angegebenen Daten.</span><span class="sxs-lookup"><span data-stu-id="2ab34-324">Creates a file containing specified data.</span></span> <span data-ttu-id="2ab34-325">Dieser **reg- \_ Binär** Wert gibt die Daten der Datei an.</span><span class="sxs-lookup"><span data-stu-id="2ab34-325">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="2ab34-326">Die **Daten** werden ignoriert, wenn entweder die **nulldatei** oder der **Dateiname** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ab34-326">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="2ab34-327">FileName</span><span class="sxs-lookup"><span data-stu-id="2ab34-327">FileName</span></span>              | <span data-ttu-id="2ab34-328">Erstellt eine Datei, die eine Kopie einer angegebenen Datei ist.</span><span class="sxs-lookup"><span data-stu-id="2ab34-328">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="2ab34-329">Dieser **reg \_ SZ** -Wert gibt den voll qualifizierten Pfad der zu kopierenden Datei an.</span><span class="sxs-lookup"><span data-stu-id="2ab34-329">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="2ab34-330">Nulldatei</span><span class="sxs-lookup"><span data-stu-id="2ab34-330">NullFile</span></span>              | <span data-ttu-id="2ab34-331">Erstellt eine leere Datei.</span><span class="sxs-lookup"><span data-stu-id="2ab34-331">Creates an empty file.</span></span> <span data-ttu-id="2ab34-332">**NullFile** wurde kein Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-332">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="2ab34-333">Wenn **NullFile** angegeben ist, werden die Registrierungs Werte für den **Daten** -und **Dateinamen** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2ab34-333">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="2ab34-334">Das folgende Beispiel für einen Registrierungsschlüssel und einen Screenshot veranschaulichen das **neue** Untermenü für den Dateityp. MYP-ms.</span><span class="sxs-lookup"><span data-stu-id="2ab34-334">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="2ab34-335">Es verfügt über den Befehl **myprogram Application**.</span><span class="sxs-lookup"><span data-stu-id="2ab34-335">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="2ab34-336">Der Screenshot zeigt das **neue** Untermenü.</span><span class="sxs-lookup"><span data-stu-id="2ab34-336">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="2ab34-337">Wenn ein Benutzer im Untermenü **neu** die Option **myprogram-Anwendung** auswählt, erstellt die Shell eine Datei mit dem Namen **New myprogram Application. MYP-MS** und übergibt sie an **MyProgram.exe**.</span><span class="sxs-lookup"><span data-stu-id="2ab34-337">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![Screenshot von Windows-Explorer mit dem neuen Befehl "myprogram Application" im Untermenü "New"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="2ab34-339">Erstellen von Drag & Drop-Handlern</span><span class="sxs-lookup"><span data-stu-id="2ab34-339">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="2ab34-340">Das grundlegende Verfahren zum Implementieren eines Drag & Drop-Handlers ist das gleiche wie bei herkömmlichen Kontextmenü Handlern.</span><span class="sxs-lookup"><span data-stu-id="2ab34-340">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="2ab34-341">Bei Kontextmenü Handlern wird jedoch normalerweise nur der [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Zeiger verwendet, der an die [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode des Handler weitergeleitet wird, um den Namen des Objekts zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="2ab34-341">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="2ab34-342">Ein Drag & Drop-Handler könnte einen anspruchsvolleren Daten Handler implementieren, um das Verhalten des gezogenen Objekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2ab34-342">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="2ab34-343">Wenn ein Benutzer mit der rechten Maustaste auf ein Shellobjekt klickt, um ein Objekt zu ziehen, wird ein Kontextmenü angezeigt, wenn der Benutzer versucht, das Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-343">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="2ab34-344">Der folgende Screenshot zeigt ein typisches Kontextmenü für Drag & Drop.</span><span class="sxs-lookup"><span data-stu-id="2ab34-344">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![Screenshot des Kontextmenüs "Drag & amp; Drop"](images/context-menu/context-dragdrop.png)

<span data-ttu-id="2ab34-346">Ein Drag & Drop-Handler ist ein Kontextmenü Handler, der diesem Kontextmenü Elemente hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="2ab34-346">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="2ab34-347">Drag & Drop-Handler werden in der Regel unter dem folgenden Unterschlüssel registriert.</span><span class="sxs-lookup"><span data-stu-id="2ab34-347">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="2ab34-348">Fügen Sie unter dem Unterschlüssel **dragdrophandlers** für den Drag & Drop-Handler einen Unterschlüssel mit dem Namen hinzu, und legen Sie den Standardwert des unter Schlüssels auf das Zeichen folgen Format der Klassen Bezeichner-GUID (CLSID) des Handlers fest.</span><span class="sxs-lookup"><span data-stu-id="2ab34-348">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="2ab34-349">Im folgenden Beispiel wird der Drag & Drop-Handler von **mydd** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2ab34-349">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="2ab34-350">Unterdrücken von Verbs</span><span class="sxs-lookup"><span data-stu-id="2ab34-350">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="2ab34-351">Sie können Windows-Richtlinien Einstellungen verwenden, um die Sichtbarkeit zu steuern.</span><span class="sxs-lookup"><span data-stu-id="2ab34-351">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="2ab34-352">Verben können durch Richtlinien Einstellungen durch Hinzufügen eines **SuppressionPolicy** -Werts oder eines **suppressionpolicyex** -GUID-Werts zum Registrierungs Unterschlüssel des Verbs unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-352">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="2ab34-353">Legen Sie den Wert des unter Schlüssels **SuppressionPolicy** auf die Richtlinien-ID fest.</span><span class="sxs-lookup"><span data-stu-id="2ab34-353">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="2ab34-354">Wenn die Richtlinie aktiviert ist, werden das Verb und der zugehörige Kontextmenü Eintrag unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-354">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="2ab34-355">Mögliche Richtlinien-ID-Werte finden Sie unter der [**Einschränkungs**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="2ab34-355">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="2ab34-356">Verwenden des Verb Auswahl Modells</span><span class="sxs-lookup"><span data-stu-id="2ab34-356">Employing the Verb Selection Model</span></span>

<span data-ttu-id="2ab34-357">Registrierungs Werte müssen für Verben festgelegt werden, um Situationen zu behandeln, in denen ein Benutzer ein einzelnes Element, mehrere Elemente oder eine Auswahl aus einem Element auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="2ab34-357">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="2ab34-358">Ein Verb erfordert separate Registrierungs Werte für jede dieser drei Situationen, die das Verb unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-358">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="2ab34-359">Die möglichen Werte für das Verb Auswahl Modell lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2ab34-359">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="2ab34-360">Geben Sie den multiselectmodel-Wert für alle Verben an.</span><span class="sxs-lookup"><span data-stu-id="2ab34-360">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="2ab34-361">Wenn der multiselectmodel-Wert nicht angegeben wird, wird er vom Typ der Verb-Implementierung abgeleitet, den Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="2ab34-361">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="2ab34-362">Für com- **basierte Methoden (** z. b. "DropTarget" und "ExecuteCommand") wird angenommen, und für die anderen **Methoden wird angenommen** .</span><span class="sxs-lookup"><span data-stu-id="2ab34-362">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="2ab34-363">Geben Sie **Single** für Verben an, die nur eine einzelne Auswahl unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-363">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="2ab34-364">Geben Sie **Player** für Verben an, die eine beliebige Anzahl von Elementen unterstützen</span><span class="sxs-lookup"><span data-stu-id="2ab34-364">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="2ab34-365">Geben Sie ein **Dokument** für Verben an, die für jedes Element ein Fenster auf oberster Ebene erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-365">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="2ab34-366">Dadurch wird die Anzahl der aktivierten Elemente beschränkt, und es wird vermieden, dass Systemressourcen nicht mehr ausgelastet sind, wenn der Benutzer zu viele Fenster öffnet.</span><span class="sxs-lookup"><span data-stu-id="2ab34-366">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="2ab34-367">Wenn die Anzahl der ausgewählten Elemente nicht mit dem Verb Auswahl Modell identisch ist oder größer als die in der folgenden Tabelle aufgeführten Standard Limits ist, wird das Verb nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-367">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="2ab34-368">Typ der Verb Implementierung</span><span class="sxs-lookup"><span data-stu-id="2ab34-368">Type of verb implementation</span></span> | <span data-ttu-id="2ab34-369">Dokument</span><span class="sxs-lookup"><span data-stu-id="2ab34-369">Document</span></span> | <span data-ttu-id="2ab34-370">Player</span><span class="sxs-lookup"><span data-stu-id="2ab34-370">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="2ab34-371">Alt</span><span class="sxs-lookup"><span data-stu-id="2ab34-371">Legacy</span></span>                      | <span data-ttu-id="2ab34-372">15 Elemente</span><span class="sxs-lookup"><span data-stu-id="2ab34-372">15 items</span></span> | <span data-ttu-id="2ab34-373">100 Elemente</span><span class="sxs-lookup"><span data-stu-id="2ab34-373">100 items</span></span> |
| <span data-ttu-id="2ab34-374">COM</span><span class="sxs-lookup"><span data-stu-id="2ab34-374">COM</span></span>                         | <span data-ttu-id="2ab34-375">15 Elemente</span><span class="sxs-lookup"><span data-stu-id="2ab34-375">15 items</span></span> | <span data-ttu-id="2ab34-376">Keine Begrenzung</span><span class="sxs-lookup"><span data-stu-id="2ab34-376">No limit</span></span>  |



 

<span data-ttu-id="2ab34-377">Im folgenden finden Sie Beispiel Registrierungseinträge, die den multiselectmodel-Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-377">The following are example registry entries using the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a><span data-ttu-id="2ab34-378">Verwenden von Element Attributen</span><span class="sxs-lookup"><span data-stu-id="2ab34-378">Using Item Attributes</span></span>

<span data-ttu-id="2ab34-379">Die [**sfgao**](sfgao.md) -Flagwerte der shellattribute für ein Element können getestet werden, um zu bestimmen, ob das Verb aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ab34-379">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="2ab34-380">Um dieses Attribut zu verwenden, fügen Sie die folgenden **reg \_ DWORD** -Werte unter dem Verb hinzu:</span><span class="sxs-lookup"><span data-stu-id="2ab34-380">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="2ab34-381">Der attributemask-Wert gibt den [**sfgao**](sfgao.md) -Wert der Bitwerte der Maske an, die getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ab34-381">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="2ab34-382">Der AttributeValue-Wert gibt den [**sfgao**](sfgao.md) -Wert der zu testenden Bits an.</span><span class="sxs-lookup"><span data-stu-id="2ab34-382">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="2ab34-383">Das impliedselectionmodel gibt 0 (null) für Element Verben oder einen Wert ungleich 0 (null) für Verben im Hintergrund Kontextmenü an.</span><span class="sxs-lookup"><span data-stu-id="2ab34-383">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="2ab34-384">Im folgenden Beispiel Registrierungs Eintrag wird attributemask auf [**sfgao \_**](sfgao.md) schreibgeschützt (0x40000) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2ab34-384">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="2ab34-385">Implementieren von benutzerdefinierten Verben für Ordner durch Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="2ab34-385">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="2ab34-386">In Windows 7 und höher können Sie über Desktop.ini Verben zu einem Ordner hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2ab34-386">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="2ab34-387">Weitere Informationen zu Desktop.ini Dateien finden Sie unter [Anpassen von Ordnern mit Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="2ab34-387">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="2ab34-388">Desktop.ini Dateien sollten immer als ausgeblendet **markiert werden**  +   , damit Sie Benutzern nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2ab34-388">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="2ab34-389">**Um benutzerdefinierte Verben für Ordner über eine Desktop.ini Datei hinzuzufügen, führen Sie die folgenden Schritte aus:**</span><span class="sxs-lookup"><span data-stu-id="2ab34-389">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="2ab34-390">Erstellen **Sie** einen Ordner, der als schreibgeschützt oder als **System** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="2ab34-390">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="2ab34-391">Erstellen Sie eine Desktop.ini-Datei, die eine enthält \[ . Shellclassinfo \] directoryclass = Ordner ProgID.</span><span class="sxs-lookup"><span data-stu-id="2ab34-391">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="2ab34-392">Erstellen Sie in der Registrierung **HKEY- \_ Klassen \_** \\ **Stamm Ordner ProgID** mit dem Wert canusefordirectory.</span><span class="sxs-lookup"><span data-stu-id="2ab34-392">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="2ab34-393">Der Wert von "canusefordirectory" vermeidet den Missbrauch von ProgIDs, die nicht an der Implementierung benutzerdefinierter Verben für Ordner durch Desktop.ini beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="2ab34-393">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="2ab34-394">Fügen Sie unter dem **Ordner** ProgID Unterschlüssel Verben hinzu, z. b.:</span><span class="sxs-lookup"><span data-stu-id="2ab34-394">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="2ab34-395">Diese Verben können das Standardverb sein. in diesem Fall wird das Verb durch Doppelklicken auf den Ordner aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2ab34-395">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2ab34-396">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ab34-396">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ab34-397">Bewährte Methoden für Kontextmenü Handler und Mehrfachauswahl Verben</span><span class="sxs-lookup"><span data-stu-id="2ab34-397">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="2ab34-398">Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="2ab34-398">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="2ab34-399">Anpassen eines Kontextmenüs mithilfe dynamischer Verben</span><span class="sxs-lookup"><span data-stu-id="2ab34-399">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="2ab34-400">Kontextmenüs und Kontextmenü Handler</span><span class="sxs-lookup"><span data-stu-id="2ab34-400">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="2ab34-401">Verben und Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="2ab34-401">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="2ab34-402">Verweis auf das Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="2ab34-402">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
