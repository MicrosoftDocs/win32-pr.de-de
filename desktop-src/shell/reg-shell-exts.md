---
description: Ein shellerweiterungshandlerobjekt muss registriert werden, bevor es von der Shell verwendet werden kann. In diesem Thema wird eine allgemeine Erörterung der Registrierung eines Shellerweiterungs Handlers erläutert.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registrieren von Shellerweiterungs Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca50bfaff984884b74ecc8572d4af9d96c55d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980201"
---
# <a name="registering-shell-extension-handlers"></a><span data-ttu-id="fbd00-104">Registrieren von Shellerweiterungs Handlern</span><span class="sxs-lookup"><span data-stu-id="fbd00-104">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="fbd00-105">Ein shellerweiterungshandlerobjekt muss registriert werden, bevor es von der Shell verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fbd00-105">A Shell extension handler object must be registered before the Shell can use it.</span></span> <span data-ttu-id="fbd00-106">In diesem Thema wird eine allgemeine Erörterung der Registrierung eines Shellerweiterungs Handlers erläutert.</span><span class="sxs-lookup"><span data-stu-id="fbd00-106">This topic is a general discussion of how to register a Shell extension handler.</span></span>

<span data-ttu-id="fbd00-107">Jedes Mal, wenn Sie einen Shellerweiterungs Handler erstellen oder ändern, ist es wichtig, das System zu benachrichtigen, dass Sie eine Änderung vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="fbd00-107">Any time you create or change a Shell extension handler, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="fbd00-108">Rufen Sie hierzu " [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)" auf, und geben Sie das **shcne-Ereignis " \_ assocchanged** " an.</span><span class="sxs-lookup"><span data-stu-id="fbd00-108">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="fbd00-109">Wenn Sie **shchangenotify** nicht aufrufen, wird die Änderung möglicherweise erst erkannt, wenn das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="fbd00-109">If you do not call **SHChangeNotify**, the change might not be recognized until the system is rebooted.</span></span>

<span data-ttu-id="fbd00-110">Für Windows 2000-Systeme gelten einige zusätzliche Faktoren.</span><span class="sxs-lookup"><span data-stu-id="fbd00-110">There are some additional factors that apply to Windows 2000 systems.</span></span> <span data-ttu-id="fbd00-111">Weitere Informationen finden Sie im Abschnitt [Registrieren von Shellerweiterungs Handlern auf Windows 2000-Systemen](#registering-shell-extension-handlers) .</span><span class="sxs-lookup"><span data-stu-id="fbd00-111">For details, see the [Registering Shell Extension Handlers on Windows 2000 Systems](#registering-shell-extension-handlers) section.</span></span>

<span data-ttu-id="fbd00-112">Wie bei Component Object Model allen COM-Objekten müssen Sie mithilfe eines Tools wie Guidgen.exe, das mit dem Windows Software Development Kit (SDK) bereitgestellt wird, eine GUID für den Handler erstellen.</span><span class="sxs-lookup"><span data-stu-id="fbd00-112">As with all Component Object Model (COM) objects, you must create a GUID for the handler using a tool such as Guidgen.exe, which is provided with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fbd00-113">Erstellen Sie unter **HKEY \_ Classes \_ root** \\ **CLSID** einen Unterschlüssel, dessen Name die Zeichen folgen Form dieser GUID ist.</span><span class="sxs-lookup"><span data-stu-id="fbd00-113">Create a subkey under **HKEY\_CLASSES\_ROOT**\\**CLSID** whose name is the string form of that GUID.</span></span> <span data-ttu-id="fbd00-114">Da es sich bei Shellerweiterungs Handlern um Prozess interne Server handelt, müssen Sie auch unter diesem GUID-Unterschlüssel einen **InProcServer32** -Unterschlüssel erstellen, wobei der (standardmäßige) Wert auf den Pfad der DLL des Handler festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fbd00-114">Because Shell extension handlers are in-process servers, you also must create an **InprocServer32** subkey under that GUID subkey with the (Default) value set to the path of the handler's DLL.</span></span> <span data-ttu-id="fbd00-115">Verwenden Sie das Apartment Threading Modell.</span><span class="sxs-lookup"><span data-stu-id="fbd00-115">Use the apartment threading model.</span></span> <span data-ttu-id="fbd00-116">Das folgende Beispiel soll dies erläutern:</span><span class="sxs-lookup"><span data-stu-id="fbd00-116">An example is shown here:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

<span data-ttu-id="fbd00-117">Jedes Mal, wenn die Shell eine Aktion ausführt, die einen Shellerweiterungs Handler einschließen kann, prüft Sie den entsprechenden Registrierungs Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="fbd00-117">Any time the Shell takes an action that can involve a Shell extension handler, it checks the appropriate registry subkey.</span></span> <span data-ttu-id="fbd00-118">Der Unterschlüssel, unter dem ein Erweiterungs Handler registriert ist, wenn er aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fbd00-118">The subkey under which an extension handler is registered controls when it will be called.</span></span> <span data-ttu-id="fbd00-119">Beispielsweise ist es üblich, dass ein Kontextmenü Handler aufgerufen wird, wenn die Shell ein Kontextmenü für einen Member eines [Dateityps](fa-file-types.md)anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fbd00-119">For instance, it is a common practice to have a shortcut menu handler called when the Shell displays a shortcut menu for a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="fbd00-120">In diesem Fall muss der Handler unter dem **ProgID** -Unterschlüssel des Dateityps registriert werden.</span><span class="sxs-lookup"><span data-stu-id="fbd00-120">In this case, the handler must be registered under the file type's **ProgID** subkey.</span></span>

<span data-ttu-id="fbd00-121">In diesem Thema werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="fbd00-121">This topic discusses the following subjects:</span></span>

-   [<span data-ttu-id="fbd00-122">Handlernamen</span><span class="sxs-lookup"><span data-stu-id="fbd00-122">Handler Names</span></span>](#handler-names)
-   [<span data-ttu-id="fbd00-123">Vordefinierte Shellobjekte</span><span class="sxs-lookup"><span data-stu-id="fbd00-123">Predefined Shell Objects</span></span>](#predefined-shell-objects)
-   [<span data-ttu-id="fbd00-124">Beispiel für eine erweiterungshandlerregistrierung</span><span class="sxs-lookup"><span data-stu-id="fbd00-124">Example of an Extension Handler Registration</span></span>](#example-of-an-extension-handler-registration)
    -   [<span data-ttu-id="fbd00-125">Registrieren von Shellerweiterungs Handlern</span><span class="sxs-lookup"><span data-stu-id="fbd00-125">Registering Shell Extension Handlers</span></span>](#registering-shell-extension-handlers)
-   [<span data-ttu-id="fbd00-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fbd00-126">Related topics</span></span>](#related-topics)

## <a name="handler-names"></a><span data-ttu-id="fbd00-127">Handlernamen</span><span class="sxs-lookup"><span data-stu-id="fbd00-127">Handler Names</span></span>

<span data-ttu-id="fbd00-128">Erstellen Sie zum Aktivieren eines Shellerweiterungs Handlers einen Unterschlüssel mit dem Namen des unter Schlüssels des Handlers (siehe unten) unter dem **shellex** -Unterschlüssel der **ProgID** (für Dateitypen) oder dem shellobjekttypnamen (für [vordefinierte \_ \_ Shellobjekte](handlers.md)).</span><span class="sxs-lookup"><span data-stu-id="fbd00-128">To enable a Shell extension handler, create a subkey with the handler subkey name (see below) under the **ShellEx** subkey of either the **ProgID** (for file types) or the Shell object type name (for [predefined\_shell\_objects](handlers.md)).</span></span>

<span data-ttu-id="fbd00-129">Wenn Sie z. b. einen Erweiterungs Handler für das Kontextmenü für MyProgram. 1 registrieren möchten, erstellen Sie zunächst den folgenden Unterschlüssel:</span><span class="sxs-lookup"><span data-stu-id="fbd00-129">For example, if you wanted to register a shortcut menu extension handler for MyProgram.1, you begin by creating the following subkey:</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

<span data-ttu-id="fbd00-130">Erstellen Sie für die folgenden Handler einen Unterschlüssel unter dem Unterschlüssel Name des unter Schlüssels "Handler", der als Zeichen folgen Version des Klassen Bezeichners (CLSID) der Shellerweiterung bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="fbd00-130">For the following handlers, create a subkey underneath the "Handler Subkey name" subkey named as the string version of the class identifier (CLSID) of the Shell extension.</span></span> <span data-ttu-id="fbd00-131">Mehrere Erweiterungen können unter dem Namen des unter Schlüssels des Handlers registriert werden, indem mehrere Unterschlüssel erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fbd00-131">Multiple extensions can be registered under the handler subkey name by creating multiple subkeys.</span></span>



| <span data-ttu-id="fbd00-132">Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-132">Handler</span></span>                 | <span data-ttu-id="fbd00-133">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fbd00-133">Interface</span></span>          | <span data-ttu-id="fbd00-134">Name des unter Schlüssels des Handlers</span><span class="sxs-lookup"><span data-stu-id="fbd00-134">Handler Subkey Name</span></span>       |
|-------------------------|--------------------|---------------------------|
| <span data-ttu-id="fbd00-135">Spalten Anbieter Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-135">Column provider handler</span></span> | <span data-ttu-id="fbd00-136">Icolumnprovider</span><span class="sxs-lookup"><span data-stu-id="fbd00-136">IColumnProvider</span></span>    | <span data-ttu-id="fbd00-137">**Columnhandlers**</span><span class="sxs-lookup"><span data-stu-id="fbd00-137">**ColumnHandlers**</span></span>        |
| <span data-ttu-id="fbd00-138">Kontextmenü Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-138">Shortcut menu handler</span></span>   | <span data-ttu-id="fbd00-139">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="fbd00-139">IContextMenu</span></span>       | <span data-ttu-id="fbd00-140">**ContextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="fbd00-140">**ContextMenuHandlers**</span></span>   |
| <span data-ttu-id="fbd00-141">Copyhook-Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-141">Copyhook handler</span></span>        | <span data-ttu-id="fbd00-142">Icopyhook</span><span class="sxs-lookup"><span data-stu-id="fbd00-142">ICopyHook</span></span>          | <span data-ttu-id="fbd00-143">**Copyhuokhandlers**</span><span class="sxs-lookup"><span data-stu-id="fbd00-143">**CopyHookHandlers**</span></span>      |
| <span data-ttu-id="fbd00-144">Drag &amp; Drop-Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-144">Drag-and-drop handler</span></span>   | <span data-ttu-id="fbd00-145">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="fbd00-145">IContextMenu</span></span>       | <span data-ttu-id="fbd00-146">**Dragdrophandlers**</span><span class="sxs-lookup"><span data-stu-id="fbd00-146">**DragDropHandlers**</span></span>      |
| <span data-ttu-id="fbd00-147">Eigenschaftenblatthandler</span><span class="sxs-lookup"><span data-stu-id="fbd00-147">Property sheet handler</span></span>  | <span data-ttu-id="fbd00-148">Ishellpropsheetext</span><span class="sxs-lookup"><span data-stu-id="fbd00-148">IShellPropSheetExt</span></span> | <span data-ttu-id="fbd00-149">**Propertysheethandlers**</span><span class="sxs-lookup"><span data-stu-id="fbd00-149">**PropertySheetHandlers**</span></span> |



 

<span data-ttu-id="fbd00-150">Bei den folgenden Handlern ist der Standardwert für den Schlüssel Name des unter Schlüssels "Handler" die Zeichen folgen Version der CLSID der Shellerweiterung.</span><span class="sxs-lookup"><span data-stu-id="fbd00-150">For the following handlers, the default value of the "Handler Subkey Name" key is the string version of the CLSID of the Shell extension.</span></span> <span data-ttu-id="fbd00-151">Für diese Handler kann nur eine Erweiterung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="fbd00-151">Only one extension can be registered for these handlers.</span></span>



| <span data-ttu-id="fbd00-152">Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-152">Handler</span></span>                 | <span data-ttu-id="fbd00-153">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fbd00-153">Interface</span></span>            | <span data-ttu-id="fbd00-154">Name des unter Schlüssels des Handlers</span><span class="sxs-lookup"><span data-stu-id="fbd00-154">Handler Subkey Name</span></span>                        |
|-------------------------|----------------------|--------------------------------------------|
| <span data-ttu-id="fbd00-155">Daten Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-155">Data handler</span></span>            | <span data-ttu-id="fbd00-156">IDataObject</span><span class="sxs-lookup"><span data-stu-id="fbd00-156">IDataObject</span></span>          | <span data-ttu-id="fbd00-157">**DataHandler**</span><span class="sxs-lookup"><span data-stu-id="fbd00-157">**DataHandler**</span></span>                            |
| <span data-ttu-id="fbd00-158">Drop-Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-158">Drop handler</span></span>            | <span data-ttu-id="fbd00-159">IDropTarget</span><span class="sxs-lookup"><span data-stu-id="fbd00-159">IDropTarget</span></span>          | <span data-ttu-id="fbd00-160">**Drophandler**</span><span class="sxs-lookup"><span data-stu-id="fbd00-160">**DropHandler**</span></span>                            |
| <span data-ttu-id="fbd00-161">Symbol Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-161">Icon handler</span></span>            | <span data-ttu-id="fbd00-162">Iextracticona/W</span><span class="sxs-lookup"><span data-stu-id="fbd00-162">IExtractIconA/W</span></span>      | <span data-ttu-id="fbd00-163">**Iconhandler**</span><span class="sxs-lookup"><span data-stu-id="fbd00-163">**IconHandler**</span></span>                            |
| <span data-ttu-id="fbd00-164">Miniatur Ansichts Bild Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-164">Thumbnail image handler</span></span> | <span data-ttu-id="fbd00-165">IThumbnailProvider</span><span class="sxs-lookup"><span data-stu-id="fbd00-165">IThumbnailProvider</span></span>   | <span data-ttu-id="fbd00-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span><span class="sxs-lookup"><span data-stu-id="fbd00-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span></span> |
| <span data-ttu-id="fbd00-167">QuickInfo-Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-167">Infotip handler</span></span>         | <span data-ttu-id="fbd00-168">Iqueryinfo</span><span class="sxs-lookup"><span data-stu-id="fbd00-168">IQueryInfo</span></span>           | <span data-ttu-id="fbd00-169">**{00021500-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="fbd00-169">**{00021500-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="fbd00-170">Shelllink (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fbd00-170">Shell link (ANSI)</span></span>       | <span data-ttu-id="fbd00-171">IShellLinkA</span><span class="sxs-lookup"><span data-stu-id="fbd00-171">IShellLinkA</span></span>          | <span data-ttu-id="fbd00-172">**{000214ee-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="fbd00-172">**{000214EE-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="fbd00-173">Shelllink (Unicode)</span><span class="sxs-lookup"><span data-stu-id="fbd00-173">Shell link (UNICODE)</span></span>    | <span data-ttu-id="fbd00-174">Ishelllinkw</span><span class="sxs-lookup"><span data-stu-id="fbd00-174">IShellLinkW</span></span>          | <span data-ttu-id="fbd00-175">**{0002149-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="fbd00-175">**{000214F9-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="fbd00-176">Strukturierter Speicher</span><span class="sxs-lookup"><span data-stu-id="fbd00-176">Structured storage</span></span>      | <span data-ttu-id="fbd00-177">IStorage</span><span class="sxs-lookup"><span data-stu-id="fbd00-177">IStorage</span></span>             | <span data-ttu-id="fbd00-178">**{0000000b-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="fbd00-178">**{0000000B-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="fbd00-179">Metadaten</span><span class="sxs-lookup"><span data-stu-id="fbd00-179">Metadata</span></span>                | <span data-ttu-id="fbd00-180">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="fbd00-180">IPropertySetStorage</span></span>  | <span data-ttu-id="fbd00-181">**Propertyhandler**</span><span class="sxs-lookup"><span data-stu-id="fbd00-181">**PropertyHandler**</span></span>                        |
| <span data-ttu-id="fbd00-182">An Startmenü anheften</span><span class="sxs-lookup"><span data-stu-id="fbd00-182">Pin to Start Menu</span></span>       | <span data-ttu-id="fbd00-183">Istartmenupinnedlist</span><span class="sxs-lookup"><span data-stu-id="fbd00-183">IStartMenuPinnedList</span></span> | <span data-ttu-id="fbd00-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span><span class="sxs-lookup"><span data-stu-id="fbd00-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span></span> |
| <span data-ttu-id="fbd00-185">An Taskleiste anheften</span><span class="sxs-lookup"><span data-stu-id="fbd00-185">Pin to Taskbar</span></span>          |                      | <span data-ttu-id="fbd00-186">**{90aa3a4e-1cba-4233-B8BB-535773d48449}**</span><span class="sxs-lookup"><span data-stu-id="fbd00-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span></span> |



 

<span data-ttu-id="fbd00-187">Die angegebenen Unterschlüssel zum Hinzufügen einer **PIN zum Startmenü** und zum Anheften **an die Taskleiste** an das Kontextmenü eines Elements sind nur für Dateitypen erforderlich, die den [IsShortcut](./links.md) -Eintrag enthalten.</span><span class="sxs-lookup"><span data-stu-id="fbd00-187">The subkeys specified to add **Pin to Start Menu** and **Pin to Taskbar** to an item's shortcut menu are only required for file types that include the [IsShortCut](./links.md) entry.</span></span>

## <a name="predefined-shell-objects"></a><span data-ttu-id="fbd00-188">Vordefinierte Shellobjekte</span><span class="sxs-lookup"><span data-stu-id="fbd00-188">Predefined Shell Objects</span></span>

<span data-ttu-id="fbd00-189">Die Shell definiert zusätzliche Objekte unter **HKEY \_ Classes \_ root** , die auf die gleiche Weise wie Dateitypen erweitert werden können.</span><span class="sxs-lookup"><span data-stu-id="fbd00-189">The Shell defines additional objects under **HKEY\_CLASSES\_ROOT** which can be extended in the same way as file types.</span></span> <span data-ttu-id="fbd00-190">Wenn Sie z. b. einen Eigenschaften Blatt Handler für alle Dateien hinzufügen möchten, können Sie sich unter dem **propertysheethandlers** -Unterschlüssel registrieren.</span><span class="sxs-lookup"><span data-stu-id="fbd00-190">For example, to add a property sheet handler for all files, you can register under the **PropertySheetHandlers** subkey.</span></span>

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

<span data-ttu-id="fbd00-191">In der folgenden Tabelle sind die verschiedenen Unterschlüssel von **HKEY- \_ Klassen \_ root** , unter denen Erweiterungs Handler registriert werden können, zu finden.</span><span class="sxs-lookup"><span data-stu-id="fbd00-191">The following table gives the various subkeys of **HKEY\_CLASSES\_ROOT** under which extension handlers can be registered.</span></span> <span data-ttu-id="fbd00-192">Beachten Sie, dass viele Erweiterungs Handler nicht unter allen aufgelisteten unter Schlüsseln registriert werden können.</span><span class="sxs-lookup"><span data-stu-id="fbd00-192">Note that many extension handlers cannot be registered under all of the listed subkeys.</span></span> <span data-ttu-id="fbd00-193">Weitere Informationen finden Sie in der Dokumentation des jeweiligen Handlers.</span><span class="sxs-lookup"><span data-stu-id="fbd00-193">For further details, see the specific handler's documentation.</span></span>



| <span data-ttu-id="fbd00-194">Unterschlüssel</span><span class="sxs-lookup"><span data-stu-id="fbd00-194">Subkey</span></span>                    | <span data-ttu-id="fbd00-195">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbd00-195">Description</span></span>                                                          | <span data-ttu-id="fbd00-196">Mögliche Handler</span><span class="sxs-lookup"><span data-stu-id="fbd00-196">Possible Handlers</span></span>                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="fbd00-197">\**\** _</span><span class="sxs-lookup"><span data-stu-id="fbd00-197">\**\** _</span></span>                    | <span data-ttu-id="fbd00-198">Alle Dateien</span><span class="sxs-lookup"><span data-stu-id="fbd00-198">All files</span></span>                                                            | <span data-ttu-id="fbd00-199">Kontextmenü, Eigenschaften Blatt, Verben (siehe unten)</span><span class="sxs-lookup"><span data-stu-id="fbd00-199">Shortcut Menu, Property Sheet, Verbs (see below)</span></span> |
| <span data-ttu-id="fbd00-200">_ *AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="fbd00-200">_ *AllFileSystemObjects*\*</span></span>  | <span data-ttu-id="fbd00-201">Alle Dateien und Datei Ordner</span><span class="sxs-lookup"><span data-stu-id="fbd00-201">All files and file folders</span></span>                                           | <span data-ttu-id="fbd00-202">Kontextmenü, Eigenschaften Blatt, Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-202">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="fbd00-203">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="fbd00-203">**Folder**</span></span>                | <span data-ttu-id="fbd00-204">Alle Ordner</span><span class="sxs-lookup"><span data-stu-id="fbd00-204">All folders</span></span>                                                          | <span data-ttu-id="fbd00-205">Kontextmenü, Eigenschaften Blatt, Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-205">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="fbd00-206">**Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="fbd00-206">**Directory**</span></span>             | <span data-ttu-id="fbd00-207">Datei Ordner</span><span class="sxs-lookup"><span data-stu-id="fbd00-207">File folders</span></span>                                                         | <span data-ttu-id="fbd00-208">Kontextmenü, Eigenschaften Blatt, Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-208">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="fbd00-209">**Verzeichnis \\ Hintergrund**</span><span class="sxs-lookup"><span data-stu-id="fbd00-209">**Directory\\Background**</span></span> | <span data-ttu-id="fbd00-210">Hintergrund des Datei Ordners</span><span class="sxs-lookup"><span data-stu-id="fbd00-210">File folder background</span></span>                                               | <span data-ttu-id="fbd00-211">Nur Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="fbd00-211">Shortcut Menu only</span></span>                               |
| <span data-ttu-id="fbd00-212">**DesktopBackground**</span><span class="sxs-lookup"><span data-stu-id="fbd00-212">**DesktopBackground**</span></span>     | <span data-ttu-id="fbd00-213">Desktop Hintergrund (Windows 7 und höher)</span><span class="sxs-lookup"><span data-stu-id="fbd00-213">Desktop background (Windows 7 and higher)</span></span>                            | <span data-ttu-id="fbd00-214">Kontextmenü, Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-214">Shortcut Menu, Verbs</span></span>                             |
| <span data-ttu-id="fbd00-215">**Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="fbd00-215">**Drive**</span></span>                 | <span data-ttu-id="fbd00-216">Alle Laufwerke in "MyComputer", z. b. "C: \\ "</span><span class="sxs-lookup"><span data-stu-id="fbd00-216">All drives in MyComputer, such as "C:\\"</span></span>                             | <span data-ttu-id="fbd00-217">Kontextmenü, Eigenschaften Blatt, Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-217">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="fbd00-218">**Network**</span><span class="sxs-lookup"><span data-stu-id="fbd00-218">**Network**</span></span>               | <span data-ttu-id="fbd00-219">Gesamtes Netzwerk (unter "meine Netzwerk Plätze")</span><span class="sxs-lookup"><span data-stu-id="fbd00-219">Entire network (under My Network Places)</span></span>                             | <span data-ttu-id="fbd00-220">Kontextmenü, Eigenschaften Blatt, Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-220">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="fbd00-221">**\\Netzwerktyp\\\#**</span><span class="sxs-lookup"><span data-stu-id="fbd00-221">**Network\\Type\\\#**</span></span>     | <span data-ttu-id="fbd00-222">Alle Objekte des Typs \# (siehe unten)</span><span class="sxs-lookup"><span data-stu-id="fbd00-222">All objects of type \# (see below)</span></span>                                   | <span data-ttu-id="fbd00-223">Kontextmenü, Eigenschaften Blatt, Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-223">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="fbd00-224">**NetShare**</span><span class="sxs-lookup"><span data-stu-id="fbd00-224">**NetShare**</span></span>              | <span data-ttu-id="fbd00-225">Alle Netzwerkfreigaben</span><span class="sxs-lookup"><span data-stu-id="fbd00-225">All network shares</span></span>                                                   | <span data-ttu-id="fbd00-226">Kontextmenü, Eigenschaften Blatt, Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-226">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="fbd00-227">**Netserver**</span><span class="sxs-lookup"><span data-stu-id="fbd00-227">**NetServer**</span></span>             | <span data-ttu-id="fbd00-228">Alle Netzwerkserver</span><span class="sxs-lookup"><span data-stu-id="fbd00-228">All network servers</span></span>                                                  | <span data-ttu-id="fbd00-229">Kontextmenü, Eigenschaften Blatt, Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-229">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="fbd00-230">*Name des Netzwerk \_ Anbieters \_*</span><span class="sxs-lookup"><span data-stu-id="fbd00-230">*network\_provider\_name*</span></span> | <span data-ttu-id="fbd00-231">Alle Objekte, die vom Netzwerkanbieter "*Netzwerk \_ Anbieter \_ Name*" bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="fbd00-231">All objects provided by network provider "*network\_provider\_name*"</span></span> | <span data-ttu-id="fbd00-232">Kontextmenü, Eigenschaften Blatt, Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-232">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="fbd00-233">**Drucker**</span><span class="sxs-lookup"><span data-stu-id="fbd00-233">**Printers**</span></span>              | <span data-ttu-id="fbd00-234">Alle Drucker</span><span class="sxs-lookup"><span data-stu-id="fbd00-234">All printers</span></span>                                                         | <span data-ttu-id="fbd00-235">Kontextmenü, Eigenschaften Blatt</span><span class="sxs-lookup"><span data-stu-id="fbd00-235">Shortcut Menu, Property Sheet</span></span>                    |
| <span data-ttu-id="fbd00-236">**AudioCD**</span><span class="sxs-lookup"><span data-stu-id="fbd00-236">**AudioCD**</span></span>               | <span data-ttu-id="fbd00-237">AudioCD in CD-Laufwerk</span><span class="sxs-lookup"><span data-stu-id="fbd00-237">Audio CD in CD drive</span></span>                                                 | <span data-ttu-id="fbd00-238">Nur Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-238">Verbs only</span></span>                                       |
| <span data-ttu-id="fbd00-239">**DVD**</span><span class="sxs-lookup"><span data-stu-id="fbd00-239">**DVD**</span></span>                   | <span data-ttu-id="fbd00-240">DVD-Laufwerk (Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="fbd00-240">DVD drive (Windows 2000)</span></span>                                             | <span data-ttu-id="fbd00-241">Kontextmenü, Eigenschaften Blatt, Verben</span><span class="sxs-lookup"><span data-stu-id="fbd00-241">Shortcut Menu, Property Sheet, Verbs</span></span>             |



 

### <a name="notes"></a><span data-ttu-id="fbd00-242">Notizen</span><span class="sxs-lookup"><span data-stu-id="fbd00-242">Notes</span></span>

-   <span data-ttu-id="fbd00-243">Der Zugriff auf das Kontextmenü des Datei Ordners wird durch einen Rechtsklick innerhalb eines Datei Ordners, aber nicht über den Inhalt des Ordners erreicht.</span><span class="sxs-lookup"><span data-stu-id="fbd00-243">The file folder background shortcut menu is accessed by right-clicking within a file folder, but not over any of the folder's contents.</span></span>
-   <span data-ttu-id="fbd00-244">"Verbs" sind spezielle Befehle, die unter **HKEY \_ Classes \_ root** \\ *subkey* \\ **Shell** \\ **Verb** registriert sind.</span><span class="sxs-lookup"><span data-stu-id="fbd00-244">"Verbs" are special commands registered under **HKEY\_CLASSES\_ROOT**\\*Subkey*\\**Shell**\\**Verb**.</span></span>
-   <span data-ttu-id="fbd00-245">Für den \\ **Netzwerktyp** \\ **\#** \# ist "" ein Netzwerk Anbietertyp Code in Dezimal.</span><span class="sxs-lookup"><span data-stu-id="fbd00-245">For **Network**\\**Type**\\**\#**, "\#" is a network provider type code in decimal.</span></span> <span data-ttu-id="fbd00-246">Der Typ Code des Netzwerk Anbieters ist das hohe Wort eines Netzwerk Typs.</span><span class="sxs-lookup"><span data-stu-id="fbd00-246">The network provider type code is the high word of a network type.</span></span> <span data-ttu-id="fbd00-247">Die Liste der Netzwerktypen wird in der "winnetwk. h"-Header Datei (wnnc \_ net \_ \* Values) angegeben.</span><span class="sxs-lookup"><span data-stu-id="fbd00-247">The list of network types is given in the Winnetwk.h header file (WNNC\_NET\_\* values).</span></span> <span data-ttu-id="fbd00-248">Beispielsweise ist wnnc \_ net \_ Shiva 0x00330000, daher wäre der entsprechende typunter Schlüssel **HKEY \_ Classes \_ root** \\ **Network** \\ **Type** \\ **51**.</span><span class="sxs-lookup"><span data-stu-id="fbd00-248">For example, WNNC\_NET\_SHIVA is 0x00330000, so the corresponding type subkey would be **HKEY\_CLASSES\_ROOT**\\**Network**\\**Type**\\**51**.</span></span>
-   <span data-ttu-id="fbd00-249">der *Name \_ des \_ Netzwerk Anbieters wird* von [**wnetgetprovidername**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)angegeben, wobei die Leerzeichen in Unterstriche konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="fbd00-249">"*network\_provider\_name*" is a network provider name as specified by [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), with the spaces converted into underscores.</span></span> <span data-ttu-id="fbd00-250">Wenn z. b. der Microsoft-Netzwerk Netzwerkanbieter installiert ist, lautet sein Anbieter Name "Microsoft Windows-Netzwerk", und der entsprechende *Netzwerk \_ Anbieter \_ Name* lautet **Microsoft \_ Windows- \_ Netzwerk**.</span><span class="sxs-lookup"><span data-stu-id="fbd00-250">For example, if the Microsoft Networking network provider is installed, its provider name is "Microsoft Windows Network", and the corresponding *network\_provider\_name* is **Microsoft\_Windows\_Network**.</span></span>

## <a name="example-of-an-extension-handler-registration"></a><span data-ttu-id="fbd00-251">Beispiel für eine erweiterungshandlerregistrierung</span><span class="sxs-lookup"><span data-stu-id="fbd00-251">Example of an Extension Handler Registration</span></span>

<span data-ttu-id="fbd00-252">Um einen bestimmten Handler zu aktivieren, erstellen Sie unter dem Typ Unterschlüssel des Erweiterungs Handlers einen Unterschlüssel mit dem Namen des Handlers.</span><span class="sxs-lookup"><span data-stu-id="fbd00-252">To enable a particular handler, create a subkey under the extension handler type subkey with the name of the handler.</span></span> <span data-ttu-id="fbd00-253">Die Shell verwendet nicht den Namen des Handlers, aber Sie muss sich von allen anderen Namen unter diesem typunter Schlüssel unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="fbd00-253">The Shell does not use the handler's name, but it must be different from all other names under that type subkey.</span></span> <span data-ttu-id="fbd00-254">Legen Sie den Standardwert des Namens unter Schlüssels auf die Zeichen folgen Form der GUID des Handlers fest.</span><span class="sxs-lookup"><span data-stu-id="fbd00-254">Set the default value of the name subkey to the string form of the handler's GUID.</span></span>

<span data-ttu-id="fbd00-255">Das folgende Beispiel veranschaulicht Registrierungseinträge, die Erweiterungs Handler für Kontextmenü und Eigenschaften Seiten mithilfe des Dateityps example. MYP ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="fbd00-255">The following example illustrates registry entries that enable shortcut menu and property sheet extension handlers, using an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a><span data-ttu-id="fbd00-256">Registrieren von Shellerweiterungs Handlern</span><span class="sxs-lookup"><span data-stu-id="fbd00-256">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="fbd00-257">Das in diesem Abschnitt beschriebene Registrierungsverfahren muss für alle Windows-Systeme befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="fbd00-257">The registration procedure discussed in this section must be followed for all Windows systems.</span></span> <span data-ttu-id="fbd00-258">Bei späteren Systemen ist jedoch möglicherweise ein zusätzlicher Schritt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fbd00-258">However, with later systems, an additional step might be necessary.</span></span> <span data-ttu-id="fbd00-259">Da diese neueren Versionen von Windows für die Verwendung in einer verwalteten Umgebung entworfen wurden, kann der Zugriff auf die Registrierung administrativ eingeschränkt werden, was einen etwas anderen Ansatz für die Installation erfordert, als im vorherigen Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fbd00-259">Because these later versions of Windows are designed to be used in a managed environment, access to the registry could be administratively restricted, requiring a somewhat different approach to installation than described in the previous section.</span></span>

> [!Note]  
> <span data-ttu-id="fbd00-260">Setup Programme sollten in der Regel nicht direkt in die Registrierung schreiben.</span><span class="sxs-lookup"><span data-stu-id="fbd00-260">Setup programs should generally not write directly to the registry.</span></span> <span data-ttu-id="fbd00-261">Stattdessen sollte Setup mit Windows Installer Paketen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fbd00-261">Instead, setup should be accomplished with Windows Installer packages.</span></span> <span data-ttu-id="fbd00-262">Diese Tools stellen sicher, dass die Software ordnungsgemäß ausgeführt wird und den Zugriff auf Funktionen wie die benutzerspezifische Klassen Registrierung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="fbd00-262">These tools ensure that software runs well and provides access to capabilities such as per-user class registration.</span></span>

 

<span data-ttu-id="fbd00-263">Shellerweiterungs Handler werden im Shellprozess ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbd00-263">Shell extension handlers run in the Shell process.</span></span> <span data-ttu-id="fbd00-264">Da es sich um einen System Prozess handelt, kann der Administrator eines Systems shellerweiterungshandler auf die in einer genehmigten Liste beschränken, indem der EnforceShellExtensionSecurity-Wert des **Explorer** -Schlüssels auf 1 festgelegt wird, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="fbd00-264">Because it is a system process, the administrator of a system can limit Shell extension handlers to those on an approved list by setting the EnforceShellExtensionSecurity value of the **Explorer** key to 1 as shown here:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

<span data-ttu-id="fbd00-265">Zum Platzieren eines Shellerweiterungs Handlers in der genehmigten Liste erstellen Sie einen **reg \_ SZ** -Wert, dessen Name die Zeichen folgen Form der GUID des Handlers unter dem **genehmigten** Unterschlüssel ist.</span><span class="sxs-lookup"><span data-stu-id="fbd00-265">To place a Shell extension handler on the approved list, create a **REG\_SZ** value whose name is the string form of the handler's GUID under the **Approved** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

<span data-ttu-id="fbd00-266">Im folgenden Beispiel werden z. b. die Handler *myCommand* und *mypropsheet* der genehmigten Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fbd00-266">For example, the following example adds the *MyCommand* and *MyPropSheet* handlers to the approved list.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

<span data-ttu-id="fbd00-267">Die Shell verwendet nicht den Wert, der der GUID zugewiesen ist, sondern sollte so festgelegt werden, dass die Überprüfung der Registrierung erleichtert wird.</span><span class="sxs-lookup"><span data-stu-id="fbd00-267">The Shell does not use the value that is assigned to the GUID, but it should be set to make inspecting the registry easier.</span></span>

<span data-ttu-id="fbd00-268">Die Setup Anwendung kann dem **genehmigten** Unterschlüssel nur Werte hinzufügen, wenn die Person, die die Anwendung installiert, über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="fbd00-268">Your setup application can add values to the **Approved** subkey only if the person installing the application has sufficient privileges.</span></span> <span data-ttu-id="fbd00-269">Wenn beim Versuch, einen Erweiterungs Handler hinzuzufügen, ein Fehler auftritt, sollten Sie den Benutzer darüber informieren, dass Administratorrechte erforderlich sind, um die Anwendung vollständig zu installieren.</span><span class="sxs-lookup"><span data-stu-id="fbd00-269">If the attempt to add an extension handler fails, you should inform the user that administrative privileges are required to fully install the application.</span></span> <span data-ttu-id="fbd00-270">Wenn der Handler für die Anwendung unverzichtbar ist, sollten Sie das Setup fehlschlagen und den Benutzer bitten, sich an einen Administrator zu wenden.</span><span class="sxs-lookup"><span data-stu-id="fbd00-270">If the handler is essential to the application, you should fail the setup and notify the user to contact an administrator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbd00-271">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fbd00-271">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbd00-272">Initialisieren von Shellerweiterungs Handlern</span><span class="sxs-lookup"><span data-stu-id="fbd00-272">Initializing Shell Extension Handlers</span></span>](int-shell-exts.md)
</dt> </dl>

 

 
