---
description: Kontextmenü Handler werden auch als Kontextmenü Handler oder Verb Handler bezeichnet. Ein Kontextmenü Handler ist ein Typ eines Dateityp Handlers.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Anpassen eines Kontextmenüs mithilfe dynamischer Verben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980184"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a><span data-ttu-id="45c24-104">Anpassen eines Kontextmenüs mithilfe dynamischer Verben</span><span class="sxs-lookup"><span data-stu-id="45c24-104">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>

<span data-ttu-id="45c24-105">Kontextmenü Handler werden auch als Kontextmenü Handler oder Verb Handler bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="45c24-105">Shortcut menu handlers are also known as context menu handlers or verb handlers.</span></span> <span data-ttu-id="45c24-106">Ein Kontextmenü Handler ist ein Typ eines Dateityp Handlers.</span><span class="sxs-lookup"><span data-stu-id="45c24-106">A shortcut menu handler is a type of file type handler.</span></span>

<span data-ttu-id="45c24-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="45c24-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="45c24-108">Informationen zu statischen und dynamischen Verben</span><span class="sxs-lookup"><span data-stu-id="45c24-108">About Static and Dynamic Verbs</span></span>](#about-static-and-dynamic-verbs)
-   [<span data-ttu-id="45c24-109">Funktionsweise von Kontextmenü Handlern mit dynamischen Verben</span><span class="sxs-lookup"><span data-stu-id="45c24-109">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [<span data-ttu-id="45c24-110">Vermeiden von Kollisionen aufgrund von nicht qualifizierten Verb Namen</span><span class="sxs-lookup"><span data-stu-id="45c24-110">Avoiding Collisions Due to Unqualified Verb Names</span></span>](#avoiding-collisions-due-to-unqualified-verb-names)
-   [<span data-ttu-id="45c24-111">Registrieren eines Kontextmenü Handlers mit einem dynamischen Verb</span><span class="sxs-lookup"><span data-stu-id="45c24-111">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [<span data-ttu-id="45c24-112">Implementieren der IContextMenu-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="45c24-112">Implementing the IContextMenu Interface</span></span>](#implementing-the-icontextmenu-interface)
    -   [<span data-ttu-id="45c24-113">IContextMenu:: getcommandstring-Methode</span><span class="sxs-lookup"><span data-stu-id="45c24-113">IContextMenu::GetCommandString Method</span></span>](#icontextmenugetcommandstring-method)
    -   [<span data-ttu-id="45c24-114">IContextMenu:: InvokeCommand-Methode</span><span class="sxs-lookup"><span data-stu-id="45c24-114">IContextMenu::InvokeCommand Method</span></span>](#icontextmenuinvokecommand-method)
    -   [<span data-ttu-id="45c24-115">IContextMenu:: querycontextmenu-Methode</span><span class="sxs-lookup"><span data-stu-id="45c24-115">IContextMenu::QueryContextMenu Method</span></span>](#icontextmenuquerycontextmenu-method)
-   [<span data-ttu-id="45c24-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45c24-116">Related topics</span></span>](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a><span data-ttu-id="45c24-117">Informationen zu statischen und dynamischen Verben</span><span class="sxs-lookup"><span data-stu-id="45c24-117">About Static and Dynamic Verbs</span></span>

<span data-ttu-id="45c24-118">Wir empfehlen Ihnen dringend, ein Kontextmenü mit einer der statischen Verb-Methoden zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="45c24-118">We strongly encourage you to implement a shortcut menu using one of the static verb methods.</span></span> <span data-ttu-id="45c24-119">Es wird empfohlen, die Anweisungen im Abschnitt "Anpassen eines Kontextmenüs mit statischen Verben" unter [Erstellen von Kontextmenü Handlern](context-menu-handlers.md)zu befolgen.</span><span class="sxs-lookup"><span data-stu-id="45c24-119">We recommend that you follow the instructions provided in the "Customizing a Shortcut Menu using Static Verbs" section of [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="45c24-120">Informationen zum dynamischen Verhalten von statischen Verben in Windows 7 und höher finden Sie unter "Get Dynamic Behavior for static Verbs" unter [Erstellen von Kontextmenü Handlern](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="45c24-120">To get dynamic behavior for static verbs in Windows 7 and later, see "Getting Dynamic Behavior for Static Verbs" in [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="45c24-121">Ausführliche Informationen über die statische Verb-Implementierung und welche dynamischen Verben zu vermeiden sind, finden [Sie unter Auswählen eines statischen oder dynamischen Verbs für](shortcut-choose-method.md)das Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="45c24-121">For details on static verb implementation, and which dynamic verbs to avoid, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span>

<span data-ttu-id="45c24-122">Wenn Sie das Kontextmenü für einen Dateityp erweitern müssen, indem Sie für den Dateityp ein dynamisches Verb registrieren, befolgen Sie die Anweisungen weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="45c24-122">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided later in this topic.</span></span>

> [!Note]  
> <span data-ttu-id="45c24-123">Beim Registrieren von Handlern, die im Kontext von 32-Bit-Anwendungen funktionieren, gibt es spezielle Überlegungen für 64-Bit-Windows: Wenn Shellverben im Kontext einer 32-Bit-Anwendung aufgerufen werden, leitet das WOW64-Subsystem den Dateisystem Zugriff auf einige Pfade um.</span><span class="sxs-lookup"><span data-stu-id="45c24-123">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="45c24-124">Wenn der exe-Handler in einem dieser Pfade gespeichert ist, kann in diesem Kontext nicht darauf zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="45c24-124">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="45c24-125">Als Problem Umgehung speichern Sie die exe-Datei in einem Pfad, der nicht umgeleitet wird, oder speichern Sie eine Stubversion der exe-Datei, die die tatsächliche Version gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="45c24-125">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a><span data-ttu-id="45c24-126">Funktionsweise von Kontextmenü Handlern mit dynamischen Verben</span><span class="sxs-lookup"><span data-stu-id="45c24-126">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>

<span data-ttu-id="45c24-127">Neben [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)exportieren Kontextmenü Handler die folgenden zusätzlichen Schnittstellen, um das Messaging zu verarbeiten, das zum Implementieren von vom Besitzer gezeichneten Menü Elementen erforderlich ist:</span><span class="sxs-lookup"><span data-stu-id="45c24-127">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), shortcut menu handlers export the following additional interfaces to handle the messaging needed to implement owner-drawn menu items:</span></span>

-   <span data-ttu-id="45c24-128">[**Ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obligatorisch)</span><span class="sxs-lookup"><span data-stu-id="45c24-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (mandatory)</span></span>
-   <span data-ttu-id="45c24-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obligatorisch)</span><span class="sxs-lookup"><span data-stu-id="45c24-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (mandatory)</span></span>
-   <span data-ttu-id="45c24-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (optional)</span><span class="sxs-lookup"><span data-stu-id="45c24-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (optional)</span></span>
-   <span data-ttu-id="45c24-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (optional)</span><span class="sxs-lookup"><span data-stu-id="45c24-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (optional)</span></span>

<span data-ttu-id="45c24-132">Weitere Informationen zu Menü Elementen, die vom Besitzer gezeichnet werden, finden Sie im Abschnitt *Erstellen von Owner-Drawn Menü Elemente* in [Verwenden von Menüs](../menurc/using-menus.md).</span><span class="sxs-lookup"><span data-stu-id="45c24-132">For more information on owner-drawn menu items, see the *Creating Owner-Drawn Menu Items* section in [Using Menus](../menurc/using-menus.md).</span></span>

<span data-ttu-id="45c24-133">Shell verwendet die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle zum Initialisieren des Handlers.</span><span class="sxs-lookup"><span data-stu-id="45c24-133">Shell uses the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface to initialize the handler.</span></span> <span data-ttu-id="45c24-134">Wenn die Shell [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)aufruft, übergibt Sie ein Datenobjekt mit dem Namen des Objekts und einem Zeiger auf eine Element Bezeichner-Liste (PIDL) des Ordners, der die Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="45c24-134">When the Shell calls [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), it passes in a data object with the object's name and a pointer to an item identifier list (PIDL) of the folder that contains the file.</span></span> <span data-ttu-id="45c24-135">Der *hkeyprogid* -Parameter ist der Registrierungs Speicherort, unter dem das Handle des Kontextmenüs registriert wird.</span><span class="sxs-lookup"><span data-stu-id="45c24-135">The *hkeyProgID* parameter is the registry location under which the shortcut menu handle is registered.</span></span> <span data-ttu-id="45c24-136">Die **ishellextinit:: Initialize** -Methode muss den Dateinamen aus dem Datenobjekt extrahieren und den Namen und den Zeiger des Ordners für die spätere Verwendung auf eine Element Bezeichner Liste (PIDL) speichern.</span><span class="sxs-lookup"><span data-stu-id="45c24-136">The **IShellExtInit::Initialize** method must extract the file name from the data object and store the name and the folder's pointer to an item identifier list (PIDL) for later use.</span></span> <span data-ttu-id="45c24-137">Weitere Informationen zur Initialisierung von Handlern finden Sie unter [Implementieren von ishellextinit](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="45c24-137">For more information on handler initialization, see [Implementing IShellExtInit](handlers.md).</span></span>

<span data-ttu-id="45c24-138">Wenn Verben in einem Kontextmenü angezeigt werden, werden Sie zuerst erkannt, dann dem Benutzer präsentiert und schließlich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="45c24-138">When verbs are presented in a shortcut menu, they are first discovered, then presented to the user, and finally invoked.</span></span> <span data-ttu-id="45c24-139">In der folgenden Liste werden diese drei Schritte ausführlicher beschrieben:</span><span class="sxs-lookup"><span data-stu-id="45c24-139">The following list describes these three steps in more detail:</span></span>

1.  <span data-ttu-id="45c24-140">Die Shell ruft [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)auf, das eine Gruppe von Verben zurückgibt, die auf dem Zustand der Elemente oder des Systems basieren können.</span><span class="sxs-lookup"><span data-stu-id="45c24-140">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which returns a set of verbs that can be based on the state of the items or the system.</span></span>
2.  <span data-ttu-id="45c24-141">Das System übergibt ein **HMENU** -handle, das von der-Methode zum Hinzufügen von Elementen zum Kontextmenü verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="45c24-141">The system passes in an **HMENU** handle that the method can use to add items to the shortcut menu.</span></span>
3.  <span data-ttu-id="45c24-142">Wenn der Benutzer auf eines der Elemente des Handlers klickt, ruft die Shell [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)auf.</span><span class="sxs-lookup"><span data-stu-id="45c24-142">If the user clicks one of the handler's items, the Shell calls [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span> <span data-ttu-id="45c24-143">Der Handler kann dann den entsprechenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="45c24-143">The handler can then execute the appropriate command.</span></span>

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a><span data-ttu-id="45c24-144">Vermeiden von Kollisionen aufgrund von nicht qualifizierten Verb Namen</span><span class="sxs-lookup"><span data-stu-id="45c24-144">Avoiding Collisions Due to Unqualified Verb Names</span></span>

<span data-ttu-id="45c24-145">Da Verben pro Typ registriert sind, kann der gleiche Verb Name für Verben auf unterschiedlichen Elementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45c24-145">Because verbs are registered per type, the same verb name can be used for verbs on different items.</span></span> <span data-ttu-id="45c24-146">Dies ermöglicht es Anwendungen, auf allgemeine Verben unabhängig vom Elementtyp zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="45c24-146">Doing so enables applications to refer to common verbs independent of the item type.</span></span> <span data-ttu-id="45c24-147">Diese Funktion ist zwar nützlich, aber die Verwendung von nicht qualifizierten Namen kann zu Konflikten mit mehreren unabhängigen Softwareanbietern (ISVs) führen, die denselben Verb Namen auswählen.</span><span class="sxs-lookup"><span data-stu-id="45c24-147">While this functionality is useful, the use of unqualified names can result in collisions with multiple independent software vendors (ISVs) that choose the same verb name.</span></span> <span data-ttu-id="45c24-148">Um dies zu vermeiden, stellen Sie immer wie folgt Verben mit dem ISV-Namen vor:</span><span class="sxs-lookup"><span data-stu-id="45c24-148">To avoid this, always prefix verbs with the ISV name as follows:</span></span>

`ISV_Name.verb`

<span data-ttu-id="45c24-149">Verwenden Sie immer eine anwendungsspezifische ProgID.</span><span class="sxs-lookup"><span data-stu-id="45c24-149">Always use an application specific ProgID.</span></span> <span data-ttu-id="45c24-150">Durch die Übernahme der Konvention zum Mapping der Dateinamenerweiterung zu einem von ISV bereitgestellten ProgID werden potenzielle Konflikte vermieden.</span><span class="sxs-lookup"><span data-stu-id="45c24-150">Adopting the convention of mapping the file name extension to an ISV provided ProgID avoids potential collisions.</span></span> <span data-ttu-id="45c24-151">Da jedoch einige Elementtypen diese Zuordnung nicht verwenden, ist es erforderlich, dass Hersteller eindeutige Namen besitzen.</span><span class="sxs-lookup"><span data-stu-id="45c24-151">However, because some item types do not use this mapping, there is a need for vendor-unique names.</span></span> <span data-ttu-id="45c24-152">Beim Hinzufügen eines Verbs zu einer vorhandenen ProgID, bei der das Verb möglicherweise bereits registriert ist, müssen Sie zuerst den Registrierungsschlüssel für das alte Verb entfernen, bevor Sie Ihr eigenes Verb hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="45c24-152">When adding a verb to an existing ProgID that might already have that verb registered, you must first remove the registry key for the old verb before adding your own verb.</span></span> <span data-ttu-id="45c24-153">Sie müssen dies tun, um zu vermeiden, dass die Verb Informationen aus den beiden Verben zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="45c24-153">You must do so to avoid merging the verb information from the two verbs.</span></span> <span data-ttu-id="45c24-154">Wenn dies nicht der Fall ist, führt dies zu unvorhersehbarem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="45c24-154">Failure to do so results in unpredictable behavior.</span></span>

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a><span data-ttu-id="45c24-155">Registrieren eines Kontextmenü Handlers mit einem dynamischen Verb</span><span class="sxs-lookup"><span data-stu-id="45c24-155">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>

<span data-ttu-id="45c24-156">Kontextmenü Handler sind entweder einem Dateityp oder einem Ordner zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="45c24-156">Shortcut menu handlers are associated with either a file type or a folder.</span></span> <span data-ttu-id="45c24-157">Bei Dateitypen wird der Handler unter dem folgenden Unterschlüssel registriert.</span><span class="sxs-lookup"><span data-stu-id="45c24-157">For file types, the handler is registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="45c24-158">Um einen Kontextmenü Handler entweder einem Dateityp oder einem Ordner zuzuordnen, erstellen Sie zunächst unter dem Unterschlüssel **ContextMenuHandlers** einen Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="45c24-158">To associate a shortcut menu handler with either a file type or a folder, first create a subkey under the **ContextMenuHandlers** subkey.</span></span> <span data-ttu-id="45c24-159">Benennen Sie den Unterschlüssel für den Handler, und legen Sie den Standardwert des unter Schlüssels auf das Zeichen folgen Format der CLSID-GUID (Class Identifier) des Handlers fest.</span><span class="sxs-lookup"><span data-stu-id="45c24-159">Name the subkey for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="45c24-160">Wenn Sie dann einem Kontextmenü Handler verschiedene Arten von Ordnern zuordnen möchten, registrieren Sie den Handler auf die gleiche Weise wie für einen Dateityp, aber unter dem *foldertype* -Unterschlüssel, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="45c24-160">Then to associate a shortcut menu handler with different kinds of folders, register the handler the same way you would for a file type, but under the *FolderType* subkey as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="45c24-161">Weitere Informationen zu den Ordner Typen, für die Sie Handler registrieren können, finden Sie unter [Registrieren von Shellerweiterungs Handlern](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="45c24-161">For more information about about which folder types you can register handlers for, see [Registering Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="45c24-162">Wenn einem Dateityp ein Kontextmenü zugeordnet ist, wird durch Doppelklicken auf ein Objekt normalerweise der Standardbefehl gestartet, und die [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) -Methode des Handlers wird nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="45c24-162">If a file type has a shortcut menu associated with it, then double-clicking an object normally launches the default command, and the handler's [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) method is not called.</span></span> <span data-ttu-id="45c24-163">Um anzugeben, dass die **IContextMenu:: querycontextmenu** -Methode des Handlers aufgerufen werden soll, wenn auf ein Objekt Doppel geklickt wird, erstellen Sie einen Unterschlüssel unter dem **CLSID** -Unterschlüssel des Handlers, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="45c24-163">To specify that the handler's **IContextMenu::QueryContextMenu** method should be called when an object is double-clicked, create a subkey under the handler's **CLSID** subkey as shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

<span data-ttu-id="45c24-164">Wenn ein Objekt, das dem Handler zugeordnet ist, doppelt geklickt wird, wird [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) mit dem **CMF-Flag \_ DefaultOnly** aufgerufen, das im *uFlags* -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="45c24-164">When an object associated with the handler is double-clicked, [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) is called with the **CMF\_DEFAULTONLY** flag set in the *uFlags* parameter.</span></span>

<span data-ttu-id="45c24-165">Mit Kontextmenü Handlern sollte der Unterschlüssel " **maychangedefaultmenu** " nur dann festgelegt werden, wenn Sie möglicherweise das Standard Verb des Kontextmenüs ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="45c24-165">Shortcut menu handlers should set the **MayChangeDefaultMenu** subkey only if they might need to change the shortcut menu's default verb.</span></span> <span data-ttu-id="45c24-166">Das Festlegen dieses unter Schlüssels zwingt das Laden der DLL-Datei des Handlers, wenn auf ein zugeordnetes Element Doppel geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="45c24-166">Setting this subkey forces the system to load the handler's DLL when an associated item is double-clicked.</span></span> <span data-ttu-id="45c24-167">Wenn Ihr Handler das Standardverb nicht ändert, sollten Sie diesen Unterschlüssel nicht festlegen, da dies dazu führt, dass das System die dll unnötig lädt.</span><span class="sxs-lookup"><span data-stu-id="45c24-167">If your handler does not change the default verb, you should not set this subkey because doing so causes the system to load your DLL unnecessarily.</span></span>

<span data-ttu-id="45c24-168">Das folgende Beispiel veranschaulicht Registrierungseinträge, die einen Kontextmenü Handler für einen MYP-Dateityp aktivieren.</span><span class="sxs-lookup"><span data-stu-id="45c24-168">The following example illustrates registry entries that enable a shortcut menu handler for an .myp file type.</span></span> <span data-ttu-id="45c24-169">Der **CLSID** -Unterschlüssel des Handlers enthält einen **maychangedefaultmenu** -Unterschlüssel, um sicherzustellen, dass der Handler aufgerufen wird, wenn der Benutzer auf ein verknüpftes Objekt doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="45c24-169">The handler's **CLSID** subkey includes a **MayChangeDefaultMenu** subkey to guarantee that the handler is called when the user double-clicks a related object.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a><span data-ttu-id="45c24-170">Implementieren der IContextMenu-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="45c24-170">Implementing the IContextMenu Interface</span></span>

<span data-ttu-id="45c24-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) ist die leistungsfähigste, aber auch die komplizierteste Methode, die implementiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="45c24-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="45c24-172">Es wird dringend empfohlen, dass Sie ein Verb mithilfe einer der statischen Verb-Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="45c24-172">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="45c24-173">Weitere Informationen finden Sie unter [Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="45c24-173">For more information, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span> <span data-ttu-id="45c24-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) verfügt über drei Methoden: **getcommandstring**, **InvokeCommand** und **querycontextmenu**, die hier ausführlich erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="45c24-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, **GetCommandString**, **InvokeCommand**, and **QueryContextMenu**, which are discussed here in detail.</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="45c24-175">IContextMenu:: getcommandstring-Methode</span><span class="sxs-lookup"><span data-stu-id="45c24-175">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="45c24-176">Die [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) -Methode des Handlers wird verwendet, um den kanonischen Namen eines Verbs zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="45c24-176">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="45c24-177">Diese Methode ist optional.</span><span class="sxs-lookup"><span data-stu-id="45c24-177">This method is optional.</span></span> <span data-ttu-id="45c24-178">In Windows XP und früheren Versionen von Windows wird diese Methode verwendet, um den Hilfetext abzurufen, der in der Statusleiste für ein Menü Element angezeigt wird, wenn Windows-Explorer über eine Status Leiste verfügt.</span><span class="sxs-lookup"><span data-stu-id="45c24-178">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="45c24-179">Der *idcmd* -Parameter enthält den bezeichneroffset des Befehls, der beim [**Aufrufen von IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="45c24-179">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="45c24-180">Wenn eine Hilfe Zeichenfolge angefordert wird, wird *uFlags* auf **GCS \_ helptextw** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="45c24-180">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="45c24-181">Kopieren Sie die Hilfe Zeichenfolge in den *pszName* -Puffer, und wandeln Sie Sie in ein **pwstr** um.</span><span class="sxs-lookup"><span data-stu-id="45c24-181">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="45c24-182">Die Verb Zeichenfolge wird angefordert, indem *uFlags* auf **GCS- \_ verbw** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="45c24-182">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="45c24-183">Kopieren Sie die entsprechende Zeichenfolge wie bei der Hilfe Zeichenfolge in *pszName*.</span><span class="sxs-lookup"><span data-stu-id="45c24-183">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="45c24-184">Die **\_ validatew** -Flags für **GCS \_ validatea** und GCS werden von Kontextmenü Handlern nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="45c24-184">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="45c24-185">Im folgenden Beispiel wird eine einfache Implementierung von [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) veranschaulicht, die dem im Abschnitt [IContextMenu:: querycontextmenu-Methode](#icontextmenuquerycontextmenu-method) in diesem Thema angegebenen [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) -Beispiel entspricht.</span><span class="sxs-lookup"><span data-stu-id="45c24-185">The following example shows a simple implementation of [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](#icontextmenuquerycontextmenu-method) section of this topic.</span></span> <span data-ttu-id="45c24-186">Da der Handler nur ein Menü Element hinzufügt, gibt es nur einen Satz von Zeichen folgen, die zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="45c24-186">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="45c24-187">Die-Methode testet, ob *idcmd* gültig ist, und gibt, wenn dies der Fall ist, die angeforderte Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="45c24-187">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="45c24-188">Die [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) -Funktion wird verwendet, um die angeforderte Zeichenfolge nach *pszName* zu kopieren, um sicherzustellen, dass die kopierte Zeichenfolge die Größe des durch *cchName* angegebenen Puffers nicht überschreitet.</span><span class="sxs-lookup"><span data-stu-id="45c24-188">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="45c24-189">In diesem Beispiel wird nur die Unterstützung für die Unicode-Werte von *uFlags* implementiert, da nur diese seit Windows 2000 in Windows-Explorer verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="45c24-189">This example only implements support for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```C++
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="45c24-190">IContextMenu:: InvokeCommand-Methode</span><span class="sxs-lookup"><span data-stu-id="45c24-190">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="45c24-191">Diese Methode wird aufgerufen, wenn ein Benutzer auf ein Menü Element klickt, um den Handler anzuweisen, den zugehörigen Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="45c24-191">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="45c24-192">Der *pici* -Parameter verweist auf eine-Struktur, die die erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="45c24-192">The *pici* parameter points to a structure that contains the information required.</span></span>

<span data-ttu-id="45c24-193">Obwohl *pici* in shlobj. h als [**cminvokecommandinfo**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) -Struktur deklariert ist, verweist es in der Praxis häufig auf eine [**cminvokecommandinfoex**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="45c24-193">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="45c24-194">Diese Struktur ist eine erweiterte Version von **cminvokecommandinfo** und verfügt über mehrere zusätzliche Member, die es ermöglichen, Unicode-Zeichen folgen zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="45c24-194">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="45c24-195">Überprüfen Sie das **CBSIZE** -Member von *pici* , um zu bestimmen, welche Struktur übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="45c24-195">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="45c24-196">Wenn es sich um eine [**cminvokecommandinfoex**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) -Struktur handelt und für den **fmask** -Member das **CMIC \_ mask- \_ Unicode** -Flag festgelegt ist, wandeln Sie *pici* in **cminvokecommandinfoex** um.</span><span class="sxs-lookup"><span data-stu-id="45c24-196">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="45c24-197">Dadurch kann Ihre Anwendung die Unicode-Informationen verwenden, die in den letzten fünf Membern der Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="45c24-197">This enables your application to use the Unicode information contained in the last five members of the structure.</span></span>

<span data-ttu-id="45c24-198">Der **lpverb** -oder **lpverbw** -Member der Struktur wird verwendet, um den auszuführenden Befehl zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="45c24-198">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="45c24-199">Befehle werden auf eine der beiden folgenden Arten identifiziert:</span><span class="sxs-lookup"><span data-stu-id="45c24-199">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="45c24-200">Durch die Verb Zeichenfolge des Befehls</span><span class="sxs-lookup"><span data-stu-id="45c24-200">By the command's verb string</span></span>
-   <span data-ttu-id="45c24-201">Nach dem bezeichneroffset des Befehls</span><span class="sxs-lookup"><span data-stu-id="45c24-201">By the command's identifier offset</span></span>

<span data-ttu-id="45c24-202">Um zwischen diesen beiden Fällen zu unterscheiden, überprüfen Sie das höchst wertige Wort **lpverb** für die ANSI-Groß-/Kleinschreibung oder **lpverbw** für den Unicode-Fall.</span><span class="sxs-lookup"><span data-stu-id="45c24-202">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="45c24-203">Wenn das hochwertige Wort nicht NULL ist, enthält **lpverb** oder **lpverbw** eine Verb Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="45c24-203">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="45c24-204">Wenn das hochwertige Wort 0 (null) ist, befindet sich der Befehls Offset im nieder wertigen Wort **lpverb**.</span><span class="sxs-lookup"><span data-stu-id="45c24-204">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="45c24-205">Das folgende Beispiel zeigt eine einfache Implementierung von [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) , die den Beispielen " [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) " und " [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) " entspricht, die vor und nach diesem Abschnitt angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="45c24-205">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="45c24-206">Die-Methode bestimmt zunächst, welche Struktur an Sie übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="45c24-206">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="45c24-207">Anschließend bestimmt er, ob der Befehl durch seinen Offset oder sein Verb gekennzeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="45c24-207">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="45c24-208">Wenn **lpverb** oder **lpverbw** ein gültiges Verb oder einen gültigen Offset enthält, zeigt die Methode ein Meldungs Feld an.</span><span class="sxs-lookup"><span data-stu-id="45c24-208">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```C++
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="45c24-209">IContextMenu:: querycontextmenu-Methode</span><span class="sxs-lookup"><span data-stu-id="45c24-209">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="45c24-210">Die Shell ruft [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) auf, damit der Kontextmenü Handler dem Menü die Menü Elemente hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="45c24-210">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="45c24-211">Sie übergibt den **HMENU** -Handle im *HMENU* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="45c24-211">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="45c24-212">Der *indexmenu* -Parameter wird auf den Index festgelegt, der für das erste hinzu zufügende Menü Element verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="45c24-212">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="45c24-213">Alle vom Handler hinzugefügten Menü Elemente müssen über Bezeichner verfügen, die zwischen den Werten in den Parametern *idcmdfirst* und *idcmdlast* liegen.</span><span class="sxs-lookup"><span data-stu-id="45c24-213">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="45c24-214">In der Regel wird der erste Befehls Bezeichner auf *idcmdfirst* festgelegt, der für jeden zusätzlichen Befehl um eins (1) erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="45c24-214">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="45c24-215">Mit dieser Vorgehensweise können Sie die Überschreitung von *idcmdlast* vermeiden und die Anzahl der verfügbaren Bezeichner maximieren, falls die Shell mehr als einen Handler aufruft.</span><span class="sxs-lookup"><span data-stu-id="45c24-215">This practice helps you avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="45c24-216">Der *Befehls Offset* eines Element Bezeichners ist der Unterschied zwischen dem Bezeichner und dem Wert in *idcmdfirst*.</span><span class="sxs-lookup"><span data-stu-id="45c24-216">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="45c24-217">Speichern Sie den Offset der einzelnen Elemente, die der Handler dem Kontextmenü hinzufügt, da die Shell ihn möglicherweise zum Identifizieren des Elements verwendet, wenn es anschließend [**IContextMenu:: getcommandstring**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) oder [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)aufruft.</span><span class="sxs-lookup"><span data-stu-id="45c24-217">Store the offset of each item that your handler adds to the shortcut menu because the Shell might use it to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="45c24-218">Sie sollten jedem Befehl, den Sie hinzufügen, auch ein [Verb](launch.md) zuweisen.</span><span class="sxs-lookup"><span data-stu-id="45c24-218">You should also assign a [verb](launch.md) to each command you add.</span></span> <span data-ttu-id="45c24-219">Ein Verb ist eine Zeichenfolge, die anstelle des Offsets verwendet werden kann, um den Befehl zu identifizieren, wenn [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="45c24-219">A verb is a string that can be used instead of the offset to identify the command when [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="45c24-220">Sie wird auch von Funktionen wie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) zum Ausführen von Kontextmenü Befehlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="45c24-220">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="45c24-221">Es gibt drei Flags, die über den *uFlags* -Parameter übergeben werden können, die für Kontextmenü Handler relevant sind.</span><span class="sxs-lookup"><span data-stu-id="45c24-221">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="45c24-222">Diese werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="45c24-222">They are described in the following table.</span></span>



| <span data-ttu-id="45c24-223">Flag</span><span class="sxs-lookup"><span data-stu-id="45c24-223">Flag</span></span>             | <span data-ttu-id="45c24-224">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45c24-224">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45c24-225">CMF \_ DefaultOnly</span><span class="sxs-lookup"><span data-stu-id="45c24-225">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="45c24-226">Der Benutzer hat den Standardbefehl ausgewählt, in der Regel durch Doppelklicken auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="45c24-226">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="45c24-227">[**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) sollte die Steuerung an die Shell zurückgeben, ohne das Menü zu ändern.</span><span class="sxs-lookup"><span data-stu-id="45c24-227">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="45c24-228">CMF- \_ NODEFAULT</span><span class="sxs-lookup"><span data-stu-id="45c24-228">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="45c24-229">Kein Element im Menü sollte das Standardelement sein.</span><span class="sxs-lookup"><span data-stu-id="45c24-229">No item in the menu should be the default item.</span></span> <span data-ttu-id="45c24-230">Die-Methode sollte Ihre Befehle dem Menü hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="45c24-230">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="45c24-231">CMF \_ Normal</span><span class="sxs-lookup"><span data-stu-id="45c24-231">CMF\_NORMAL</span></span>      | <span data-ttu-id="45c24-232">Das Kontextmenü wird normal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45c24-232">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="45c24-233">Die-Methode sollte Ihre Befehle dem Menü hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="45c24-233">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="45c24-234">Verwenden Sie entweder [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) oder [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) , um der Liste Menü Elemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="45c24-234">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="45c24-235">Geben Sie anschließend einen **HRESULT** -Wert mit dem schwere **Grad \_ Success** an.</span><span class="sxs-lookup"><span data-stu-id="45c24-235">Then return an **HRESULT** value with the severity set to **SEVERITY\_SUCCESS**.</span></span> <span data-ttu-id="45c24-236">Legen Sie den Codewert auf den Offset des größten Befehls Bezeichners fest, der zugewiesen wurde, plus eins (1).</span><span class="sxs-lookup"><span data-stu-id="45c24-236">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="45c24-237">Nehmen Sie beispielsweise an, dass *idcmdfirst* auf 5 festgelegt ist und Sie dem Menü drei Elemente mit den Befehls bezeichlern 5, 7 und 8 hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="45c24-237">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="45c24-238">Der Rückgabewert muss sein `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .</span><span class="sxs-lookup"><span data-stu-id="45c24-238">The return value should be `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)`.</span></span>

<span data-ttu-id="45c24-239">Das folgende Beispiel zeigt eine einfache Implementierung von [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , mit der ein einzelner Befehl eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="45c24-239">The following example shows a simple implementation of [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="45c24-240">Der bezeichneroffset für den Befehl ist die IDM- \_ Anzeige, die auf 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="45c24-240">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="45c24-241">Die Variablen **m \_ pszverb** und **m \_ pwszverb** sind private Variablen, die zum Speichern der zugeordneten sprachunabhängigen Verb Zeichenfolge im ANSI-und Unicode-Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45c24-241">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```C++
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



<span data-ttu-id="45c24-242">Informationen zu anderen Verb Implementierungsaufgaben finden Sie unter [Erstellen von Kontextmenü Handlern](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="45c24-242">For other verb implementation tasks, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45c24-243">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45c24-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45c24-244">Kontextmenüs und Kontextmenü Handler</span><span class="sxs-lookup"><span data-stu-id="45c24-244">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="45c24-245">Verben und Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="45c24-245">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="45c24-246">Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="45c24-246">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="45c24-247">Bewährte Methoden für Kontextmenü Handler und Mehrfachauswahl Verben</span><span class="sxs-lookup"><span data-stu-id="45c24-247">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="45c24-248">Erstellen von Kontextmenü Handlern</span><span class="sxs-lookup"><span data-stu-id="45c24-248">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="45c24-249">Verweis auf das Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="45c24-249">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
