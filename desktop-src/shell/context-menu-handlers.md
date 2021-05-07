---
description: Kontextmenühandler, die auch als Kontextmenühandler oder Verbhandler bezeichnet werden, sind ein Typ von Dateityphandler. Wie alle diese Handler handelt es sich dabei um IN-Process-Component Object Model (COM)-Objekte, die als DLLs implementiert werden.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Erstellen von Kontextmenühandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd2611c492d517e9312ec2a4e1c95d7f1aa0fea
ms.sourcegitcommit: 05b3d7f137ef9bbddf4049215cb11d55b935997e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2021
ms.locfileid: "108800971"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="9ddbb-104">Erstellen von Kontextmenühandlern</span><span class="sxs-lookup"><span data-stu-id="9ddbb-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="9ddbb-105">Kontextmenühandler, die auch als Kontextmenühandler oder Verbhandler bezeichnet werden, sind ein Typ von Dateityphandler.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="9ddbb-106">Diese Handler können auf eine Weise veranlasst werden, die dazu führt, dass sie in ihrem eigenen Prozess, im Explorer oder in anderen Prozessen von Drittanbietern geladen werden.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-106">These handlers may be impelmented in a way that causes them to load in their own process or in the explorer, or other 3rd party processes.</span></span> <span data-ttu-id="9ddbb-107">Gehen Sie beim Erstellen von Prozesshandlern mit Vorsicht vor, da sie dem Prozess schaden können, der sie lädt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-107">Take care when creating in-process handlers as they can cause harm to the process that loads them.</span></span>

> [!Note]  
> <span data-ttu-id="9ddbb-108">Bei der Registrierung von Handlern, die im Kontext von 32-Bit-Anwendungen funktionieren, gibt es besondere Überlegungen für 64-Bit-basierte Versionen von Windows: Wenn sie im Kontext einer Anwendung mit unterschiedlicher Bitheit aufgerufen werden, leitet das WOW64-Subsystem den Dateisystemzugriff auf einige Pfade um.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-108">There are special considerations for 64-bit based versions of Windows when registering handlers that work in the context of 32-bit applications: when invoked in the context of an application of different bitness, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="9ddbb-109">Wenn ihr EXE-Handler in einem dieser Pfade gespeichert ist, kann in diesem Kontext nicht darauf zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-109">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="9ddbb-110">Speichern Sie daher ihre EXE-Datei entweder in einem Pfad, der nicht umgeleitet wird, oder speichern Sie eine Stubversion Ihrer EXE-Datei, die die echte Version startet.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-110">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

<span data-ttu-id="9ddbb-111">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="9ddbb-112">Kanonische Verben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-112">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="9ddbb-113">Erweiterte Verben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-113">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="9ddbb-114">Anpassen eines Kontextmenüs mit statischen Verben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-114">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="9ddbb-115">Aktivieren des Handlers mithilfe der IDropTarget-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9ddbb-115">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="9ddbb-116">Angeben der Position und Reihenfolge statischer Verben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-116">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="9ddbb-117">Positionieren von Verben am oberen oder unteren Rand des Menüs</span><span class="sxs-lookup"><span data-stu-id="9ddbb-117">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="9ddbb-118">Erstellen von statischen kaskadierenden Menüs</span><span class="sxs-lookup"><span data-stu-id="9ddbb-118">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="9ddbb-119">Abrufen des dynamischen Verhaltens für statische Verben mithilfe der erweiterten Abfragesyntax</span><span class="sxs-lookup"><span data-stu-id="9ddbb-119">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="9ddbb-120">Veraltet: Zuordnen von Verben zu dynamischer Datenaustausch Befehlen</span><span class="sxs-lookup"><span data-stu-id="9ddbb-120">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="9ddbb-121">Abschließen von Verbimplementierungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-121">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="9ddbb-122">Anpassen des Kontextmenüs für vordefinierte Shellobjekte</span><span class="sxs-lookup"><span data-stu-id="9ddbb-122">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="9ddbb-123">Erweitern eines neuen Untermenüs</span><span class="sxs-lookup"><span data-stu-id="9ddbb-123">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="9ddbb-124">Unterdrücken von Verben und Steuern der Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="9ddbb-124">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="9ddbb-125">Verwenden des Verbauswahlmodells</span><span class="sxs-lookup"><span data-stu-id="9ddbb-125">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="9ddbb-126">Verwenden von Elementattributen</span><span class="sxs-lookup"><span data-stu-id="9ddbb-126">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="9ddbb-127">Implementieren von benutzerdefinierten Verben für Ordner über Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="9ddbb-127">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="9ddbb-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9ddbb-128">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="9ddbb-129">Kanonische Verben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-129">Canonical Verbs</span></span>

<span data-ttu-id="9ddbb-130">Anwendungen sind in der Regel dafür verantwortlich, lokalisierte Anzeigezeichenfolgen für die von ihnen definierten Verben bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-130">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="9ddbb-131">Um jedoch ein gewisses Maß an Sprachunabhängigkeit zu gewährleisten, definiert das System einen Standardsatz häufig verwendeter Verben, die als kanonische Verben bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-131">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="9ddbb-132">Ein kanonisches Verb wird dem Benutzer nie angezeigt und kann mit jeder beliebigen Benutzeroberflächensprache verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-132">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="9ddbb-133">Das System verwendet den kanonischen Namen, um automatisch eine ordnungsgemäß lokalisierte Anzeigezeichenfolge zu generieren.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-133">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="9ddbb-134">Beispielsweise ist die Anzeigezeichenfolge des geöffneten Verbs auf **Öffnen** auf einem englischen System und auf die deutsche Entsprechung in einem deutschen System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-134">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>


| <span data-ttu-id="9ddbb-135">Kanonisches Verb</span><span class="sxs-lookup"><span data-stu-id="9ddbb-135">Canonical verb</span></span> | <span data-ttu-id="9ddbb-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ddbb-136">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="9ddbb-137">Öffnen</span><span class="sxs-lookup"><span data-stu-id="9ddbb-137">Open</span></span>           | <span data-ttu-id="9ddbb-138">Öffnet die Datei oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-138">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="9ddbb-139">Opennew</span><span class="sxs-lookup"><span data-stu-id="9ddbb-139">Opennew</span></span>        | <span data-ttu-id="9ddbb-140">Öffnet die Datei oder den Ordner in einem neuen Fenster.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-140">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="9ddbb-141">Drucken</span><span class="sxs-lookup"><span data-stu-id="9ddbb-141">Print</span></span>          | <span data-ttu-id="9ddbb-142">Gibt die Datei aus.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-142">Prints the file.</span></span>                                                     |
| <span data-ttu-id="9ddbb-143">Printto</span><span class="sxs-lookup"><span data-stu-id="9ddbb-143">Printto</span></span>        | <span data-ttu-id="9ddbb-144">Ermöglicht dem Benutzer das Drucken einer Datei durch Ziehen auf ein Druckerobjekt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-144">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="9ddbb-145">Erkunden</span><span class="sxs-lookup"><span data-stu-id="9ddbb-145">Explore</span></span>        | <span data-ttu-id="9ddbb-146">Öffnet Windows-Explorer mit dem ausgewählten Ordner.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-146">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="9ddbb-147">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ddbb-147">Properties</span></span>     | <span data-ttu-id="9ddbb-148">Öffnet das Eigenschaftenblatt des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-148">Opens the object's property sheet.</span></span>                                   |

> [!Note]  
> <span data-ttu-id="9ddbb-149">Das **Printto-Verb** ist ebenfalls kanonisch, wird jedoch nie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-149">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="9ddbb-150">Dadurch kann der Benutzer eine Datei drucken, indem er sie auf ein Druckerobjekt zieht.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-150">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

<span data-ttu-id="9ddbb-151">Kontextmenühandler können ihre eigenen kanonischen Verben über [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) mit **GCS \_ VERBW** oder **GCS \_ VERBA bereitstellen.**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-151">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="9ddbb-152">Das System verwendet die kanonischen Verben als zweiten Parameter (*lpOperation*), der an [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)übergeben wird, und ist [**die CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). **LpVerb-Member,** der an die [**IContextMenu::InvokeCommand-Methode übergeben**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-152">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="9ddbb-153">Erweiterte Verben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-153">Extended Verbs</span></span>

<span data-ttu-id="9ddbb-154">Wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, werden im Kontextmenü die Standardverben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-154">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="9ddbb-155">Möglicherweise möchten Sie Befehle in einigen Kontextmenüs hinzufügen und unterstützen, die nicht in jedem Kontextmenü angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-155">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="9ddbb-156">Sie können beispielsweise Befehle verwenden, die nicht häufig verwendet werden oder für erfahrene Benutzer vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-156">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="9ddbb-157">Aus diesem Grund können Sie auch ein oder mehrere erweiterte Verben definieren.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-157">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="9ddbb-158">Diese Verben ähneln normalen Verben, unterscheiden sich jedoch durch ihre Registrierung von normalen Verben.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-158">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="9ddbb-159">Um Zugriff auf erweiterte Verben zu erhalten, muss der Benutzer mit der rechten Maustaste auf ein Objekt klicken, während er die UMSCHALTTASTE drückt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-159">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="9ddbb-160">Wenn der Benutzer dies tut, werden die erweiterten Verben zusätzlich zu den Standardverben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-160">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="9ddbb-161">Sie können die Registrierung verwenden, um ein oder mehrere erweiterte Verben zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-161">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="9ddbb-162">Die zugeordneten Befehle werden nur angezeigt, wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt und gleichzeitig die UMSCHALTTASTE drückt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-162">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="9ddbb-163">Um ein Verb als erweitert zu definieren, fügen Sie dem Unterschlüssel des Verbs einen "erweiterten" **REG \_ SZ-Wert** hinzu.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-163">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="9ddbb-164">Dem Wert sollten keine Daten zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-164">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="9ddbb-165">Anpassen eines Kontextmenüs mit statischen Verben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-165">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="9ddbb-166">Nach [dem Auswählen eines statischen oder](shortcut-choose-method.md) dynamischen Verbs für das Kontextmenü können Sie das Kontextmenü für einen Dateityp erweitern, indem Sie ein statisches Verb für den Dateityp registrieren.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-166">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="9ddbb-167">Fügen Sie hierzu  einen Shell-Unterschlüssel unterhalb des Unterschlüssels für die ProgID der Anwendung hinzu, die dem Dateityp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-167">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="9ddbb-168">Optional können Sie ein Standardverb für den Dateityp definieren,  indem Sie es als Standardwert des Shell-Unterschlüssels festlegen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-168">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="9ddbb-169">Das Standardverb wird zuerst im Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-169">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="9ddbb-170">Der Zweck besteht darin, der Shell ein Verb bereitzustellen, das sie verwenden kann, wenn die [**ShellExecuteEx-Funktion**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) aufgerufen wird, aber kein Verb angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-170">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="9ddbb-171">Die Shell wählt nicht unbedingt das Standardverb aus, wenn **ShellExecuteEx** auf diese Weise verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-171">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="9ddbb-172">Die Shell verwendet das erste verfügbare Verb in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-172">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="9ddbb-173">Das Standardverb</span><span class="sxs-lookup"><span data-stu-id="9ddbb-173">The default verb</span></span>
2.  <span data-ttu-id="9ddbb-174">Das erste Verb in der Registrierung, wenn die Verbreihenfolge angegeben ist</span><span class="sxs-lookup"><span data-stu-id="9ddbb-174">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="9ddbb-175">Das **Open-Verb**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-175">The **Open** verb</span></span>
4.  <span data-ttu-id="9ddbb-176">Das **Open With-Verb**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-176">The **Open With** verb</span></span>

<span data-ttu-id="9ddbb-177">Wenn keines der aufgeführten Verben verfügbar ist, schlägt der Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-177">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="9ddbb-178">Erstellen Sie einen Unterschlüssel für jedes Verb, das Sie unter dem Shell-Unterschlüssel hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-178">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="9ddbb-179">Für jeden dieser Unterschlüssel muss ein **REG \_ SZ-Wert** auf die Anzeigezeichenfolge des Verbs (lokalisierte Zeichenfolge) festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-179">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="9ddbb-180">Erstellen Sie für jeden Verbunterschlüssel einen Befehlsunterschlüssel mit dem Standardwert, der auf die Befehlszeile zum Aktivieren der Elemente festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-180">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="9ddbb-181">Bei kanonischen Verben wie **Öffnen** und **Drucken** können Sie die Anzeigezeichenfolge weglassen, da das System automatisch eine ordnungsgemäß lokalisierte Zeichenfolge anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-181">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="9ddbb-182">Bei nicht kanonischen Verben wird die Verbzeichenfolge angezeigt, wenn Sie die Anzeigezeichenfolge weglassen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-182">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="9ddbb-183">Beachten Sie im folgenden Registrierungsbeispiel Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-183">In the following registry example, note that:</span></span>

-   <span data-ttu-id="9ddbb-184">Da **Doit** kein kanonisches Verb ist, wird ihm ein Anzeigename zugewiesen, der durch Drücken der D-Taste ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-184">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="9ddbb-185">Das **Printto-Verb** wird nicht im Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-185">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="9ddbb-186">Durch die Einbindung in die Registrierung kann der Benutzer jedoch Dateien drucken, indem er sie auf einem Druckersymbol ablegen kann.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-186">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="9ddbb-187">Für jedes Verb wird ein Unterschlüssel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-187">One subkey is shown for each verb.</span></span> <span data-ttu-id="9ddbb-188">**%1 stellt** den Dateinamen und **%2 den** Druckernamen dar.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-188">**%1** represents the file name and **%2** the printer name.</span></span>

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

<span data-ttu-id="9ddbb-189">Das folgende Diagramm veranschaulicht die Erweiterung des Kontextmenüs in Übereinstimmung mit den oben genannten Registrierungseinträgen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-189">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="9ddbb-190">Dieses Kontextmenü enthält **die Verben Öffnen**, Do **It** und **Drucken** mit **Do It** als Standardverb.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-190">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![Screenshot des Standardverb-Kontextmenüs](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="9ddbb-192">Aktivieren des Handlers mithilfe der IDropTarget-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9ddbb-192">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="9ddbb-193">dynamischer Datenaustausch (DDE) ist veraltet. verwenden [**Sie stattdessen IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)</span><span class="sxs-lookup"><span data-stu-id="9ddbb-193">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="9ddbb-194">**IDropTarget ist** stabiler und verfügt über eine bessere Aktivierungsunterstützung, da es die COM-Aktivierung des Handlers verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-194">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="9ddbb-195">Bei der Auswahl mehrerer Elemente unterliegt **IDropTarget** nicht den Puffergrößeneinschränkungen in DDE und [**CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)</span><span class="sxs-lookup"><span data-stu-id="9ddbb-195">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="9ddbb-196">Außerdem werden Elemente als Datenobjekt an die Anwendung übergeben, das mithilfe der [**SHCreateShellItemArrayFromDataObject-Funktion**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) in ein Elementarray konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-196">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="9ddbb-197">Dies ist einfacher, und namespace-Informationen gehen nicht verloren, wenn das Element in einen Pfad für Befehlszeilen- oder DDE-Protokolle konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-197">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="9ddbb-198">Weitere Informationen zu [**IDropTarget-**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) und Shell-Abfragen für Dateiassozattribute finden Sie unter [Wahrgenommene Typen und Anwendungsregistrierung.](fa-perceivedtypes.md)</span><span class="sxs-lookup"><span data-stu-id="9ddbb-198">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="9ddbb-199">Angeben der Position und Reihenfolge statischer Verben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-199">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="9ddbb-200">Normalerweise werden Verben in einem Kontextmenü basierend darauf geordnet, wie sie aufzählen. -Enumeration basiert zuerst auf der Reihenfolge des Zuordnungsarrays und dann auf der Reihenfolge der Elemente im Zuordnungsarray, wie durch die Sortierreihenfolge der Registrierung definiert.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-200">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="9ddbb-201">Verben können durch Angabe des Standardwerts des Shell-Unterschlüssels für den Zuordnungseintrag geordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-201">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="9ddbb-202">Dieser Standardwert kann ein einzelnes Element enthalten, das an der oberen Position des Kontextmenüs angezeigt wird, oder eine Liste von Elementen, die durch Leerzeichen oder Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-202">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="9ddbb-203">Im letzteren Fall ist das erste Element in der Liste das Standardelement, und die anderen Verben werden direkt darunter in der angegebenen Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-203">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="9ddbb-204">Der folgende Registrierungseintrag erzeugt beispielsweise Kontextmenüverben in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-204">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="9ddbb-205">Anzeige</span><span class="sxs-lookup"><span data-stu-id="9ddbb-205">Display</span></span>
2.  <span data-ttu-id="9ddbb-206">Gadgets</span><span class="sxs-lookup"><span data-stu-id="9ddbb-206">Gadgets</span></span>
3.  <span data-ttu-id="9ddbb-207">Personalisierung</span><span class="sxs-lookup"><span data-stu-id="9ddbb-207">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="9ddbb-208">Auf ähnliche Weise erzeugt der folgende Registrierungseintrag Kontextmenüverben in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-208">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="9ddbb-209">Personalisierung</span><span class="sxs-lookup"><span data-stu-id="9ddbb-209">Personalization</span></span>
2.  <span data-ttu-id="9ddbb-210">Gadgets</span><span class="sxs-lookup"><span data-stu-id="9ddbb-210">Gadgets</span></span>
3.  <span data-ttu-id="9ddbb-211">Anzeige</span><span class="sxs-lookup"><span data-stu-id="9ddbb-211">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="9ddbb-212">Positionieren von Verben am oberen oder unteren Rand des Menüs</span><span class="sxs-lookup"><span data-stu-id="9ddbb-212">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="9ddbb-213">Das folgende Registrierungsattribut kann verwendet werden, um ein Verb am oberen oder unteren Rand des Menüs zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-213">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="9ddbb-214">Wenn es mehrere Verben gibt, die dieses Attribut angeben, erhält das letzte, das dies tun soll, Priorität:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-214">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="9ddbb-215">Erstellen statischer kaskadierender Menüs</span><span class="sxs-lookup"><span data-stu-id="9ddbb-215">Creating Static Cascading Menus</span></span>

<span data-ttu-id="9ddbb-216">In Windows 7 und höher wird die Implementierung von kaskadierenden Menüs über Registrierungseinstellungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-216">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="9ddbb-217">Vor Windows 7 war die Erstellung kaskadierender Menüs nur über die Implementierung der [**IContextMenu-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) möglich.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-217">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="9ddbb-218">Unter Windows 7 und höher sollten Sie nur dann auf COM-codebasierte Lösungen zurückgreifen, wenn die statischen Methoden nicht ausreichen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-218">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="9ddbb-219">Der folgende Screenshot enthält ein Beispiel für ein kaskadierendes Menü.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-219">The following screen shot provides an example of a cascading menu.</span></span>

![Screenshot eines Beispiels für ein kaskadierendes Menü](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="9ddbb-221">In Windows 7 und höher gibt es drei Möglichkeiten, kaskadierende Menüs zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-221">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="9ddbb-222">Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag "SubCommands"</span><span class="sxs-lookup"><span data-stu-id="9ddbb-222">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="9ddbb-223">Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="9ddbb-223">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="9ddbb-224">Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9ddbb-224">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="9ddbb-225">Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag "SubCommands"</span><span class="sxs-lookup"><span data-stu-id="9ddbb-225">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="9ddbb-226">In Windows 7 und höher können Sie den Eintrag Unterbefehle verwenden, um kaskadierende Menüs mithilfe des folgenden Verfahrens zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-226">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="9ddbb-227">**So erstellen Sie ein kaskadierenden Menü mithilfe des Eintrags SubCommands**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-227">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="9ddbb-228">Erstellen Sie unter HKEY CLASSES ROOT ProgID shell **(HKEY \_ CLASSES \_ ROOT** \\ *ProgID-Shell)* einen Unterschlüssel, \\  um Ihr kaskadiertes Menü zu darstellen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-228">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="9ddbb-229">In diesem Beispiel geben wir diesem Unterschlüssel den Namen *CascadeTest*.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-229">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="9ddbb-230">Stellen Sie sicher, dass der Standardwert des *CascadeTest-Unterschlüssels* leer ist und **als (Wert nicht festgelegt) angezeigt wird.**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-230">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="9ddbb-231">Fügen Sie *ihrem CascadeTest-Unterschlüssel* einen EINTRAG VOM TYP **REG \_ SZ** hinzu, und weisen Sie ihm den Text zu, der als Name im Kontextmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-231">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="9ddbb-232">In diesem Beispiel weisen wir ihm "Test Cascade Menu" zu.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-232">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="9ddbb-233">Fügen Sie ihrem *CascadeTest-Unterschlüssel* einen SubCommands-Eintrag vom Typ **REG \_ SZ** hinzu, dem die Liste der Verben, die im Menü angezeigt werden sollen, in der Reihenfolge ihrer Darstellung zugewiesen ist( durch Semikolons getrennt).</span><span class="sxs-lookup"><span data-stu-id="9ddbb-233">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="9ddbb-234">Hier weisen wir beispielsweise eine Reihe von vom System bereitgestellten Verben zu:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-234">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="9ddbb-235">Implementieren Sie benutzerdefinierte Verben mithilfe einer der Implementierungsmethoden für statische Verben, und listen Sie sie unter dem **CommandStore-Unterschlüssel** auf, wie in diesem Beispiel für ein fiktives *Verb VerbName gezeigt:*</span><span class="sxs-lookup"><span data-stu-id="9ddbb-235">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

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
> <span data-ttu-id="9ddbb-236">Diese Methode hat den Vorteil, dass die benutzerdefinierten Verben einmal registriert und wiederverwendet werden können, indem der Verbname unter dem Eintrag SubCommandsaufgelistet wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-236">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="9ddbb-237">Es ist jedoch erforderlich, dass die Anwendung über die Berechtigung zum Ändern der Registrierung unter **HKEY \_ LOCAL MACHINE \_ verfügt.**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-237">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="9ddbb-238">Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="9ddbb-238">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="9ddbb-239">In Windows 7 und höher können Sie den Eintrag ExtendedSubCommandKey verwenden, um erweiterte kaskadierenden Menüs zu erstellen: kaskadierenden Menüs in kaskadierenden Menüs.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-239">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="9ddbb-240">Der folgende Screenshot ist ein Beispiel für ein erweitertes kaskadierenden Menü.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-240">The following screen shot is an example of an extended cascading menu.</span></span>

![Screenshot mit erweitertem Kaskadierungsmenü für Geräte](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="9ddbb-242">Da **HKEY \_ CLASSES \_ ROOT** eine Kombination aus **HKEY CURRENT \_ \_ USER** und **HKEY LOCAL \_ \_ MACHINE** ist, können Sie alle benutzerdefinierten Verben unter dem **Unterschlüssel HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Classes** registrieren.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-242">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="9ddbb-243">Der Hauptvorteil besteht darin, dass keine erhöhten Berechtigungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-243">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="9ddbb-244">Darüber hinaus können andere Dateizuordnungen diesen gesamten Satz von Verben wiederverwenden, indem derselbe ExtendedSubCommandsKey-Unterschlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-244">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="9ddbb-245">Wenn Sie diesen Satz von Verben nicht wiederverwenden müssen, können Sie die Verben unter dem übergeordneten Element auflisten, aber sicherstellen, dass der Standardwert des übergeordneten Elements leer ist.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-245">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="9ddbb-246">**So erstellen Sie ein kaskadierendes Menü mit einem ExtendedSubCommandsKey-Eintrag**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-246">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="9ddbb-247">Erstellen Sie unter **HKEY \_ CLASSES \_ ROOT** \\ *ProgID* shell einen \\  Unterschlüssel, um Ihr kaskadierendes Menü darzustellen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-247">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="9ddbb-248">In diesem Beispiel geben wir diesem Unterschlüssel den Namen *CascadeTest2.*</span><span class="sxs-lookup"><span data-stu-id="9ddbb-248">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="9ddbb-249">Stellen Sie sicher, dass der Standardwert des *CascadeTest-Unterschlüssels* leer ist und als **(Wert nicht festgelegt)** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-249">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="9ddbb-250">Fügen Sie Ihrem *CascadeTest-Unterschlüssel* einen ENTRYVerb-Eintrag vom Typ **REG \_ SZ** hinzu, und weisen Sie ihm den Text zu, der im Kontextmenü als Name angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-250">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="9ddbb-251">In diesem Beispiel weisen wir ihm "Test Cascade Menu" zu.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-251">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="9ddbb-252">Fügen Sie unter dem erstellten *CascadeTest-Unterschlüssel* einen Unterschlüssel **ExtendedSubCommandsKey** hinzu, und fügen Sie dann die Dokumentunterkommands (vom **Reg \_ SZ-Typ)** hinzu. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-252">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

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

    <span data-ttu-id="9ddbb-253">Stellen Sie sicher, dass der Standardwert des Unterschlüssels *Test Cascade Menu 2* leer ist und als **(Wert nicht festgelegt) angezeigt** wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-253">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="9ddbb-254">Füllen Sie die Unterverbs mit einer der folgenden statischen Verbimplementierungen auf.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-254">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="9ddbb-255">Beachten Sie, dass der CommandFlags-Unterschlüssel EXPCMDFLAGS-Werte darstellt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-255">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="9ddbb-256">Wenn Sie vor oder nach dem kaskadierten Menüelement ein Trennzeichen hinzufügen möchten, verwenden Sie ECF \_ SEPARATORBEFORE (0x20) oder ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="9ddbb-256">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="9ddbb-257">Eine Beschreibung dieser Windows 7- und höher-Flags finden Sie unter [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="9ddbb-257">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="9ddbb-258">ECF \_ SEPARATORBEFORE funktioniert nur für die Menüelemente der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-258">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="9ddbb-259">WORDVerb ist vom Typ **REG \_ SZ,** und CommandFlags ist vom Typ **REG \_ DWORD.**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-259">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

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

<span data-ttu-id="9ddbb-260">Der folgende Screenshot zeigt die vorherigen Beispiele für Registrierungsschlüsseleinträge.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-260">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![Screenshot eines Beispiels für ein kaskadierendes Menü mit Auswahlmöglichkeiten für Editor und Wordpad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="9ddbb-262">Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9ddbb-262">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="9ddbb-263">Eine weitere Option zum Hinzufügen von Verben zu einem kaskadierenden Menü ist [**über IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="9ddbb-263">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="9ddbb-264">Mit dieser Methode können Datenquellen, die ihre Befehlsmodulbefehle über [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) bereitstellen, diese Befehle als Verben in einem Kontextmenü verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-264">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="9ddbb-265">In Windows 7 und höher können Sie mit [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) die gleiche Verbimplementierung wie mit [**IContextMenu bereitstellen.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)</span><span class="sxs-lookup"><span data-stu-id="9ddbb-265">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="9ddbb-266">Die folgenden beiden Screenshots veranschaulichen die Verwendung von kaskadierenden Menüs im **Ordner Geräte.**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-266">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Screenshot: Beispiel für ein kaskadiertes Menü im Ordner "devices"](images/file-assoc/filecascademenu.png)

<span data-ttu-id="9ddbb-268">Der folgende Screenshot veranschaulicht eine weitere Implementierung eines kaskadierenden Menüs im **Ordner Geräte.**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-268">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![Screenshot: Beispiel für ein kaskadiertes Menü im Ordner "devices"](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="9ddbb-270">Da [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) nur die In-Process-Aktivierung unterstützt, wird sie für die Verwendung durch Shell-Datenquellen empfohlen, die die Implementierung zwischen Befehlen und Kontextmenüs gemeinsam nutzen müssen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-270">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="9ddbb-271">Abrufen des dynamischen Verhaltens für statische Verben mithilfe der erweiterten Abfragesyntax</span><span class="sxs-lookup"><span data-stu-id="9ddbb-271">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="9ddbb-272">Die erweiterte Abfragesyntax (Advanced Query Syntax, AQS) kann eine Bedingung ausdrücken, die mithilfe von Eigenschaften des Elements ausgewertet wird, für das das Verb instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-272">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="9ddbb-273">Dieses System funktioniert nur mit schnellen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-273">This system works only with fast properties.</span></span> <span data-ttu-id="9ddbb-274">Dies sind Eigenschaften, die die Shell-Datenquelle als schnell meldet, indem [sie nicht "SHCOLSTATE \_ SLOW"](/windows/win32/api/shtypes/ne-shtypes-shcolstate) aus [**IShellFolder2::GetDefaultColumnState zurücksendet.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate)</span><span class="sxs-lookup"><span data-stu-id="9ddbb-274">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="9ddbb-275">Windows 7 und höher unterstützen kanonische Werte, die Probleme bei lokalisierten Builds vermeiden.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-275">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="9ddbb-276">Die folgende kanonische Syntax ist für lokalisierte Builds erforderlich, um diese Windows 7-Erweiterung nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-276">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="9ddbb-277">Im folgenden Beispielregistrierungseintrag:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-277">In the following example registry entry:</span></span>

-   <span data-ttu-id="9ddbb-278">Der **AppliesTo-Wert** steuert, ob das Verb angezeigt oder ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-278">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="9ddbb-279">Der DefaultAppliesTo-Wert steuert, welches Verb der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-279">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="9ddbb-280">Der HasLUAShield-Wert steuert, ob ein UAC-Schutz (User Account Control) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-280">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="9ddbb-281">In diesem Beispiel macht der **DefaultAppliesTo-Wert** dieses Verb zum Standard für jede Datei mit dem Wort "exampleText1" im Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-281">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="9ddbb-282">Der **AppliesTo-Wert** aktiviert das Verb für jede Datei mit "exampleText1" im Namen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-282">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="9ddbb-283">Der **HasLUAShield-Wert** zeigt den Shield für Dateien mit "exampleText2" im Namen an.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-283">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="9ddbb-284">Fügen Sie den **Befehlsunterschlüssel** und einen Wert hinzu:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-284">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="9ddbb-285">In der Windows 7-Registrierung finden Sie unter **HKEY \_ CLASSES ROOT \_ drive** \\  ein Beispiel für BitLocker-Verben, die den folgenden Ansatz verwenden:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-285">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="9ddbb-286">AppliesTo = System.Volume.BitlockerProtection:=2</span><span class="sxs-lookup"><span data-stu-id="9ddbb-286">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="9ddbb-287">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean \# True</span><span class="sxs-lookup"><span data-stu-id="9ddbb-287">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="9ddbb-288">Weitere Informationen zu AQS finden Sie unter [Erweiterte Abfragesyntax.](../search/-search-3x-advancedquerysyntax.md)</span><span class="sxs-lookup"><span data-stu-id="9ddbb-288">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="9ddbb-289">Veraltet: Zuordnen von Verben zu dynamischer Datenaustausch Befehlen</span><span class="sxs-lookup"><span data-stu-id="9ddbb-289">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="9ddbb-290">DDE ist veraltet. Verwenden Sie stattdessen [**IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)</span><span class="sxs-lookup"><span data-stu-id="9ddbb-290">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="9ddbb-291">DDE ist veraltet, da zum Ermitteln des DDE-Servers eine Broadcastfenstermeldung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-291">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="9ddbb-292">Ein DDE-Server hängt die Broadcastfensternachricht und hängt daher DDE-Konversationen für andere Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-292">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="9ddbb-293">Es ist üblich, dass eine einzelne hängen gebliebene Anwendung dazu führt, dass nachfolgende Hängen auf der gesamten Benutzerfreundlichkeit hängen bleiben.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-293">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="9ddbb-294">Die [**IDropTarget-Methode**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) ist robuster und bietet eine bessere Aktivierungsunterstützung, da sie die COM-Aktivierung des Handlers verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-294">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="9ddbb-295">Bei der Auswahl mehrerer Elemente unterliegt **IDropTarget** nicht den Puffergrößenbeschränkungen, die sowohl in DDE als auch im [**CreateProcess-Element**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)zu finden sind.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-295">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="9ddbb-296">Außerdem werden Elemente als Datenobjekt an die Anwendung übergeben, das mithilfe der [**SHCreateShellItemArrayFromDataObject-Funktion**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) in ein Elementarray konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-296">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="9ddbb-297">Dies ist einfacher und geht nicht wie beim Konvertieren des Elements in einen Pfad für Befehlszeilen- oder DDE-Protokolle verloren.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-297">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="9ddbb-298">Weitere Informationen zu [**IDropTarget-**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) und Shell-Abfragen für Dateizuordnungsattribute finden Sie unter [Wahrgenommene Typen und Anwendungsregistrierung.](fa-perceivedtypes.md)</span><span class="sxs-lookup"><span data-stu-id="9ddbb-298">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="9ddbb-299">Abschließen von Verbimplementierungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-299">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="9ddbb-300">Die folgenden Aufgaben zum Implementieren von Verben sind sowohl für statische als auch für dynamische Verbimplementierungen relevant.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-300">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="9ddbb-301">Weitere Informationen zu dynamischen Verben finden Sie unter [Anpassen eines Kontextmenüs mit dynamischen Verben.](shortcut-menu-using-dynamic-verbs.md)</span><span class="sxs-lookup"><span data-stu-id="9ddbb-301">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="9ddbb-302">Anpassen des Kontextmenüs für vordefinierte Shellobjekte</span><span class="sxs-lookup"><span data-stu-id="9ddbb-302">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="9ddbb-303">Viele vordefinierte Shellobjekte verfügen über Kontextmenüs, die angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-303">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="9ddbb-304">Registrieren Sie den Befehl auf die gleiche Weise wie typische Dateitypen, verwenden Sie jedoch den Namen des vordefinierten Objekts als Dateitypnamen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-304">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="9ddbb-305">Eine Liste vordefinierter Objekte finden Sie im Abschnitt *Predefined Shell Objects* (Vordefinierte Shellobjekte) von Creating Shell Extension Handlers (Erstellen [von Shellerweiterungshandlern).](handlers.md)</span><span class="sxs-lookup"><span data-stu-id="9ddbb-305">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="9ddbb-306">Die vordefinierten Shellobjekte, deren Kontextmenüs durch Hinzufügen von Verben in der Registrierung angepasst werden können, werden in der Tabelle mit dem Wort Verb markiert.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-306">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="9ddbb-307">Erweitern eines neuen Untermenüs</span><span class="sxs-lookup"><span data-stu-id="9ddbb-307">Extending a New Submenu</span></span>

<span data-ttu-id="9ddbb-308">Wenn ein Benutzer das Menü **Datei** in Windows-Explorer, wird einer der angezeigten Befehle **New (Neu) angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-308">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="9ddbb-309">Wenn Sie diesen Befehl auswählen, wird ein Untermenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-309">Selecting this command displays a submenu.</span></span> <span data-ttu-id="9ddbb-310">Standardmäßig enthält das Untermenü die beiden Befehle **Ordner** und **Verknüpfung,** mit denen Benutzer Unterordner und Verknüpfungen erstellen können.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-310">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="9ddbb-311">Dieses Untermenü kann um Dateierstellungsbefehle für jeden Dateityp erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-311">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="9ddbb-312">Um dem Untermenü Neu  einen Dateierstellungsbefehl hinzuzufügen, müssen die Dateien Ihrer Anwendung über einen zugeordneten Dateityp verfügen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-312">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="9ddbb-313">Fügen Sie unter dem Dateinamen einen **ShellNeuen** Unterschlüssel ein.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-313">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="9ddbb-314">Wenn der **Befehl** Neu im Menü Datei **ausgewählt** ist, fügt die Shell dem Untermenü Neu den **Dateityp** hinzu.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-314">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="9ddbb-315">Die Anzeigezeichenfolge des Befehls ist die beschreibende Zeichenfolge, die der ProgID des Programms zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-315">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="9ddbb-316">Um die Dateierstellungsmethode anzugeben, weisen Sie dem **Unterschlüssel ShellNeu** einen oder mehrere Datenwerte zu.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-316">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="9ddbb-317">Die verfügbaren Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-317">The available values are listed in the following table.</span></span>



| <span data-ttu-id="9ddbb-318">ShellNeuer Unterschlüsselwert</span><span class="sxs-lookup"><span data-stu-id="9ddbb-318">ShellNew subkey value</span></span> | <span data-ttu-id="9ddbb-319">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ddbb-319">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ddbb-320">Befehl</span><span class="sxs-lookup"><span data-stu-id="9ddbb-320">Command</span></span>               | <span data-ttu-id="9ddbb-321">Führt eine Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-321">Executes an application.</span></span> <span data-ttu-id="9ddbb-322">Dieser **REG \_ SZ-Wert** gibt den Pfad der auszuführenden Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-322">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="9ddbb-323">Beispielsweise können Sie festlegen, dass ein Assistent gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-323">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="9ddbb-324">Daten</span><span class="sxs-lookup"><span data-stu-id="9ddbb-324">Data</span></span>                  | <span data-ttu-id="9ddbb-325">Erstellt eine Datei mit angegebenen Daten.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-325">Creates a file containing specified data.</span></span> <span data-ttu-id="9ddbb-326">Dieser **REG \_ BINARY-Wert** gibt die Daten der Datei an.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-326">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="9ddbb-327">**Daten** werden ignoriert, wenn entweder **NullFile** oder **FileName** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-327">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="9ddbb-328">FileName</span><span class="sxs-lookup"><span data-stu-id="9ddbb-328">FileName</span></span>              | <span data-ttu-id="9ddbb-329">Erstellt eine Datei, die eine Kopie einer angegebenen Datei ist.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-329">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="9ddbb-330">Dieser **REG \_ SZ-Wert** gibt den vollqualifizierten Pfad der zu kopierenden Datei an.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-330">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="9ddbb-331">NULLFile</span><span class="sxs-lookup"><span data-stu-id="9ddbb-331">NullFile</span></span>              | <span data-ttu-id="9ddbb-332">Erstellt eine leere Datei.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-332">Creates an empty file.</span></span> <span data-ttu-id="9ddbb-333">**NullFile** hat keinen Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-333">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="9ddbb-334">Wenn **NULLFile** angegeben wird, werden die Registrierungswerte **Data** und **FileName** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-334">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="9ddbb-335">Das folgende Beispiel für den Registrierungsschlüssel und der Screenshot veranschaulichen das **Untermenü "New"** für den Dateityp ".myp-ms".</span><span class="sxs-lookup"><span data-stu-id="9ddbb-335">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="9ddbb-336">Sie verfügt über den Befehl **MyProgram Application**.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-336">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="9ddbb-337">Der Screenshot veranschaulicht das Untermenü **"Neu".**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-337">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="9ddbb-338">Wenn ein Benutzer im Untermenü **Neu** die Option **MyProgram-Anwendung** auswählt, erstellt die Shell eine Datei mit dem Namen **New MyProgram Application.myp-ms** und übergibt sie an **MyProgram.exe**.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-338">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![Screenshot des Windows-Explorers mit einem neuen Befehl "myprogram application" im Untermenü "new"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="9ddbb-340">Erstellen von Drag & Drop-Handlern</span><span class="sxs-lookup"><span data-stu-id="9ddbb-340">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="9ddbb-341">Das grundlegende Verfahren zum Implementieren eines Drag & Drop-Handlers ist das gleiche wie bei herkömmlichen Kontextmenühandlern.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-341">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="9ddbb-342">Kontextmenühandler verwenden jedoch normalerweise nur den [**IDataObject-Zeiger,**](/windows/win32/api/objidl/nn-objidl-idataobject) der an die [**IShellExtInit::Initialize-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) des Handlers übergeben wird, um den Namen des Objekts zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-342">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="9ddbb-343">Ein Drag & Drop-Handler könnte einen komplexeren Datenhandler implementieren, um das Verhalten des gezogenen Objekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-343">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="9ddbb-344">Wenn ein Benutzer mit der rechten Maustaste auf ein Shell-Objekt klickt, um ein Objekt zu ziehen, wird ein Kontextmenü angezeigt, wenn der Benutzer versucht, das Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-344">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="9ddbb-345">Der folgende Screenshot veranschaulicht ein typisches Drag & Drop-Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-345">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![Screenshot des Drag & Drop-Kontextmenüs](images/context-menu/context-dragdrop.png)

<span data-ttu-id="9ddbb-347">Ein Drag & Drop-Handler ist ein Kontextmenühandler, der diesem Kontextmenü Elemente hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-347">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="9ddbb-348">Drag & Drop-Handler werden in der Regel unter dem folgenden Unterschlüssel registriert.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-348">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="9ddbb-349">Fügen Sie unter dem **DragDropHandlers-Unterschlüssel** einen Unterschlüssel namens für den Drag & Drop-Handler hinzu, und legen Sie den Standardwert des Unterschlüssels auf die Zeichenfolgenform der KLASSENbezeichner-GUID (CLSID) des Handlers fest.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-349">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="9ddbb-350">Im folgenden Beispiel wird der Drag & **Drop-Handler MyDD** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-350">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="9ddbb-351">Unterdrücken von Verben und Steuern der Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="9ddbb-351">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="9ddbb-352">Sie können windows-Richtlinieneinstellungen verwenden, um die Sichtbarkeit von Verben zu steuern.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-352">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="9ddbb-353">Verben können durch Richtlinieneinstellungen unterdrückt werden, indem dem Registrierungsunterschlüssel des Verbs ein **SuppressionPolicy-Wert** oder ein **SuppressionPolicyEx-GUID-Wert** hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-353">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="9ddbb-354">Legen Sie den Wert des **Unterschlüssels SuppressionPolicy** auf die Richtlinien-ID fest.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-354">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="9ddbb-355">Wenn die Richtlinie aktiviert ist, werden das Verb und der zugehörige Kontextmenüeintrag unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-355">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="9ddbb-356">Mögliche Richtlinien-ID-Werte finden Sie in der [**RESTRICTIONS-Enumeration.**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions)</span><span class="sxs-lookup"><span data-stu-id="9ddbb-356">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="9ddbb-357">Verwenden des Verbauswahlmodells</span><span class="sxs-lookup"><span data-stu-id="9ddbb-357">Employing the Verb Selection Model</span></span>

<span data-ttu-id="9ddbb-358">Registrierungswerte müssen für Verben festgelegt werden, um Situationen zu behandeln, in denen ein Benutzer ein einzelnes Element, mehrere Elemente oder eine Auswahl aus einem Element auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-358">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="9ddbb-359">Ein Verb erfordert separate Registrierungswerte für jede dieser drei Situationen, die das Verb unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-359">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="9ddbb-360">Die möglichen Werte für das Verbauswahlmodell lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-360">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="9ddbb-361">Geben Sie den MultiSelectModel-Wert für alle Verben an.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-361">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="9ddbb-362">Wenn der MultiSelectModel-Wert nicht angegeben ist, wird er von dem Typ der von Ihnen gewählten Verbimplementierung abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-362">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="9ddbb-363">Für COM-basierte Methoden (z. B. DropTarget und ExecuteCommand) wird **der Player** und für die anderen Methoden **document** angenommen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-363">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="9ddbb-364">Geben Sie **Single** für Verben an, die nur eine einzelne Auswahl unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-364">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="9ddbb-365">Geben Sie **Player** für Verben an, die eine beliebige Anzahl von Elementen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-365">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="9ddbb-366">Geben Sie **Dokument** für Verben an, die ein Fenster der obersten Ebene für jedes Element erstellen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-366">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="9ddbb-367">Dies schränkt die Anzahl der aktivierten Elemente ein und verhindert, dass die Systemressourcen nicht mehr verfügbar sind, wenn der Benutzer zu viele Fenster öffnet.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-367">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="9ddbb-368">Wenn die Anzahl der ausgewählten Elemente nicht mit dem Verbauswahlmodell übereinstimmt oder die in der folgenden Tabelle beschriebenen Standardgrenzwerte über dem Wert liegt, wird das Verb nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-368">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="9ddbb-369">Typ der Verbimplementierungen</span><span class="sxs-lookup"><span data-stu-id="9ddbb-369">Type of verb implementation</span></span> | <span data-ttu-id="9ddbb-370">Dokument</span><span class="sxs-lookup"><span data-stu-id="9ddbb-370">Document</span></span> | <span data-ttu-id="9ddbb-371">Player</span><span class="sxs-lookup"><span data-stu-id="9ddbb-371">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="9ddbb-372">Alt</span><span class="sxs-lookup"><span data-stu-id="9ddbb-372">Legacy</span></span>                      | <span data-ttu-id="9ddbb-373">15 Elemente</span><span class="sxs-lookup"><span data-stu-id="9ddbb-373">15 items</span></span> | <span data-ttu-id="9ddbb-374">100 Elemente</span><span class="sxs-lookup"><span data-stu-id="9ddbb-374">100 items</span></span> |
| <span data-ttu-id="9ddbb-375">COM</span><span class="sxs-lookup"><span data-stu-id="9ddbb-375">COM</span></span>                         | <span data-ttu-id="9ddbb-376">15 Elemente</span><span class="sxs-lookup"><span data-stu-id="9ddbb-376">15 items</span></span> | <span data-ttu-id="9ddbb-377">Keine Begrenzung</span><span class="sxs-lookup"><span data-stu-id="9ddbb-377">No limit</span></span>  |



 

<span data-ttu-id="9ddbb-378">Im Folgenden werden Beispielregistrierungseinträge mit dem MultiSelectModel-Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-378">The following are example registry entries using the MultiSelectModel value.</span></span>

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

### <a name="using-item-attributes"></a><span data-ttu-id="9ddbb-379">Verwenden von Elementattributen</span><span class="sxs-lookup"><span data-stu-id="9ddbb-379">Using Item Attributes</span></span>

<span data-ttu-id="9ddbb-380">Die [**SFGAO-Flagwerte**](sfgao.md) der Shellattribute für ein Element können getestet werden, um zu bestimmen, ob das Verb aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-380">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="9ddbb-381">Um dieses Attributfeature zu verwenden, fügen Sie die folgenden **REG \_ DWORD-Werte** unter dem Verb hinzu:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-381">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="9ddbb-382">Der AttributeMask-Wert gibt den [**SFGAO-Wert**](sfgao.md) der Bitwerte der Maske an, mit der getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-382">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="9ddbb-383">Der AttributeValue-Wert gibt den [**SFGAO-Wert**](sfgao.md) der getesteten Bits an.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-383">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="9ddbb-384">Das ImpliedSelectionModel gibt 0 (null) für Elementverben oder ungleich 0 (null) für Verben im Kontextmenü im Hintergrund an.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-384">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="9ddbb-385">Im folgenden Beispielregistrierungseintrag ist AttributeMask auf [**SFGAO \_ READONLY**](sfgao.md) (0x40000) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-385">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

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

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="9ddbb-386">Implementieren von benutzerdefinierten Verben für Ordner über Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="9ddbb-386">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="9ddbb-387">In Windows 7 und höher können Sie einem Ordner verbs über Desktop.ini hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-387">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="9ddbb-388">Weitere Informationen zu Desktop.ini-Dateien finden Sie unter [Anpassen von Ordnern mit Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="9ddbb-388">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="9ddbb-389">Desktop.ini Dateien sollten immer als System hidden **(System** ausgeblendet) gekennzeichnet sein, damit sie benutzern  +   nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-389">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="9ddbb-390">**Um benutzerdefinierte Verben für Ordner über eine Desktop.ini hinzuzufügen, führen Sie die folgenden Schritte aus:**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-390">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="9ddbb-391">Erstellen Sie einen Ordner, der als **schreibgeschützt oder** System gekennzeichnet **ist.**</span><span class="sxs-lookup"><span data-stu-id="9ddbb-391">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="9ddbb-392">Erstellen Sie Desktop.ini-Datei, die ein \[ enthält. ShellClassInfo \] DirectoryClass=Folder ProgID.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-392">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="9ddbb-393">Erstellen Sie in der Registrierung **HKEY \_ CLASSES \_ ROOT** \\ **Folder ProgID** mit dem Wert CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-393">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="9ddbb-394">Der CanUseForDirectory-Wert vermeidet den Missbrauch von ProgIDs, die festgelegt sind, um nicht an der Implementierung benutzerdefinierter Verben für Ordner teilzunehmen, Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-394">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="9ddbb-395">Fügen Sie Verben unter dem **Unterschlüssel Folder** ProgID hinzu, z. B.:</span><span class="sxs-lookup"><span data-stu-id="9ddbb-395">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="9ddbb-396">Diese Verben können das Standardverb sein. In diesem Fall wird das Verb durch Doppelklicken auf den Ordner aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9ddbb-396">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9ddbb-397">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9ddbb-397">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ddbb-398">Bewährte Methoden für Kontextmenühandler und Mehrfachauswahlverben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-398">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="9ddbb-399">Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="9ddbb-399">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="9ddbb-400">Anpassen eines Kontextmenüs mit dynamischen Verben</span><span class="sxs-lookup"><span data-stu-id="9ddbb-400">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="9ddbb-401">Kontextmenüs und Kontextmenühandler</span><span class="sxs-lookup"><span data-stu-id="9ddbb-401">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="9ddbb-402">Verben und Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="9ddbb-402">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="9ddbb-403">Kontextmenüreferenz</span><span class="sxs-lookup"><span data-stu-id="9ddbb-403">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
