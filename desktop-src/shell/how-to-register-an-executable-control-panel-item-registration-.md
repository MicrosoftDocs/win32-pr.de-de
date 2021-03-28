---
description: Für System Steuerungselemente, die als exe-Dateien implementiert sind, sind keine speziellen Exporte oder Nachrichten Behandlung erforderlich. Beliebige exe-Dateien können als Befehls Objekt registriert werden, damit Sie im Ordnersystem Steuerung mit einem Einstiegspunkt angezeigt werden.
title: Registrieren von ausführbaren System Steuerungselementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042244"
---
# <a name="how-to-register-executable-control-panel-items"></a><span data-ttu-id="a7db5-104">Registrieren von ausführbaren System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="a7db5-104">How to Register Executable Control Panel Items</span></span>

<span data-ttu-id="a7db5-105">Für System Steuerungselemente, die als exe-Dateien implementiert sind, sind keine speziellen Exporte oder Nachrichten Behandlung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7db5-105">For Control Panel items that are implemented as .exe files, no special exports or message handling is required.</span></span> <span data-ttu-id="a7db5-106">Beliebige exe-Dateien können als Befehls Objekt registriert werden, damit Sie im Ordnersystem Steuerung mit einem Einstiegspunkt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a7db5-106">Any .exe file can be registered as a command object to appear with an entry point in the Control Panel folder.</span></span>

<span data-ttu-id="a7db5-107">Hier wird ein Beispiel verwendet, um die Registrierungsanforderungen zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="a7db5-107">An example is used here to demonstrate the registration requirements.</span></span> <span data-ttu-id="a7db5-108">Das Beispiel zeigt, wie ein System Steuerungselement namens **meine Einstellungen** als Befehls Objekt registriert wird, sodass es im Fenstersystem Steuerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a7db5-108">The example shows how to register a Control Panel item called **My Settings** as a command object so that it appears in the Control Panel window.</span></span> <span data-ttu-id="a7db5-109">Das Fenster **meine Einstellungen** wird auch angezeigt, wenn der Befehl `MyApp.exe /settings` ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7db5-109">The **My Settings** window also appears when the command `MyApp.exe /settings` is run.</span></span>

## <a name="instructions"></a><span data-ttu-id="a7db5-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="a7db5-110">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="a7db5-111">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="a7db5-111">Step 1:</span></span>

<span data-ttu-id="a7db5-112">Generieren Sie eine GUID für das System Steuerungselement.</span><span class="sxs-lookup"><span data-stu-id="a7db5-112">Generate a GUID for the Control Panel item.</span></span> <span data-ttu-id="a7db5-113">Durch die GUID wird das System Steuerungselement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a7db5-113">The GUID uniquely identifies the Control Panel item.</span></span> <span data-ttu-id="a7db5-114">In diesem Beispiel `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` ist die GUID des System Steuerungs Elements.</span><span class="sxs-lookup"><span data-stu-id="a7db5-114">In this example, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` is the GUID of the Control Panel item.</span></span>

### <a name="step-2"></a><span data-ttu-id="a7db5-115">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="a7db5-115">Step 2:</span></span>

<span data-ttu-id="a7db5-116">Fügen Sie der Registrierung unter Verwendung der GUID als Name einen Unterschlüssel wie folgt hinzu.</span><span class="sxs-lookup"><span data-stu-id="a7db5-116">Using the GUID as a name, add a subkey to the registry as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

<span data-ttu-id="a7db5-117">Die Daten für den Standardeintrag sind einfach der reg \_ SZ-Name des System Steuerungs Elements.</span><span class="sxs-lookup"><span data-stu-id="a7db5-117">The data for the Default entry is simply the REG\_SZ name of the Control Panel item.</span></span> <span data-ttu-id="a7db5-118">Der Standardeintrag kann nützlich sein, um den GUID-Eintrag zu identifizieren, ist aber optional.</span><span class="sxs-lookup"><span data-stu-id="a7db5-118">The Default entry can be useful to identify the GUID entry, but it is optional.</span></span>

### <a name="step-3"></a><span data-ttu-id="a7db5-119">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="a7db5-119">Step 3:</span></span>

<span data-ttu-id="a7db5-120">Fügen Sie der Registrierung unter Verwendung der GUID als Name einen Unterschlüssel und die zugehörigen Einträge wie folgt hinzu.</span><span class="sxs-lookup"><span data-stu-id="a7db5-120">Using the GUID as a name, add a subkey and its entries to the registry as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   <span data-ttu-id="a7db5-121">**Default**.</span><span class="sxs-lookup"><span data-stu-id="a7db5-121">**Default**.</span></span> <span data-ttu-id="a7db5-122">REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a7db5-122">REG\_SZ.</span></span> <span data-ttu-id="a7db5-123">Der Anzeige Name für das System Steuerungselement.</span><span class="sxs-lookup"><span data-stu-id="a7db5-123">The display name for the Control Panel item.</span></span>
-   <span data-ttu-id="a7db5-124">**LocalizedString**.</span><span class="sxs-lookup"><span data-stu-id="a7db5-124">**LocalizedString**.</span></span> <span data-ttu-id="a7db5-125">Optional.</span><span class="sxs-lookup"><span data-stu-id="a7db5-125">Optional.</span></span> <span data-ttu-id="a7db5-126">Reg \_ SZ oder reg \_ Expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a7db5-126">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="a7db5-127">Der Modulname und die Zeichen folgen Tabellen-ID des lokalisierten Namens des System Steuerungs Elements.</span><span class="sxs-lookup"><span data-stu-id="a7db5-127">The module name and string table ID of the localized name of the Control Panel item.</span></span> <span data-ttu-id="a7db5-128">Das Format ist ein "at"-Zeichen (@), gefolgt vom Namen der exe-oder DLL-Datei, die die MUI-Zeichen folgen Tabelle (mehrsprachige Benutzeroberfläche) enthält.</span><span class="sxs-lookup"><span data-stu-id="a7db5-128">The format is an "at" sign (@) followed by the name of the .exe or .dll that contains the Multilingual User Interface (MUI) string table.</span></span> <span data-ttu-id="a7db5-129">Umgebungsvariablen können als Ersatz für einen Teil des Pfads verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7db5-129">Environment variables can be used as a substitute for a part of the path.</span></span> <span data-ttu-id="a7db5-130">Auf den Pfad und den Dateinamen folgt ein Komma (,) und ein Bindestrich (-), gefolgt von der ID in der Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a7db5-130">The path and file name is followed by a comma (,) and a hyphen (-), followed by the ID in the string table.</span></span>

    <span data-ttu-id="a7db5-131">Wenn das Modul nicht über eine Zeichen folgen Tabelle verfügt, kann dieser Eintrag einfach die Anzeige Name-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="a7db5-131">If the module does not have a string table, then this entry can simply be the display name string.</span></span> <span data-ttu-id="a7db5-132">Wenn Sie anstelle einer Zeichen folgen Tabelle nur die Anzeige Name-Zeichenfolge verwenden, wird der Name nicht an die aktuelle Anzeige Sprache angepasst.</span><span class="sxs-lookup"><span data-stu-id="a7db5-132">If you use only the display name string rather than a string table, the name does not adjust to the current display language.</span></span>

-   <span data-ttu-id="a7db5-133">**Infotipp**.</span><span class="sxs-lookup"><span data-stu-id="a7db5-133">**InfoTip**.</span></span> <span data-ttu-id="a7db5-134">Reg \_ SZ oder reg \_ Expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a7db5-134">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="a7db5-135">Eine Beschreibung des System Steuerungs Elements.</span><span class="sxs-lookup"><span data-stu-id="a7db5-135">A description of the Control Panel item.</span></span> <span data-ttu-id="a7db5-136">Diese Informationen werden in einem infotip angezeigt, der angezeigt wird, wenn mit dem Mauszeiger auf das Element Symbol gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a7db5-136">This information is shown in an InfoTip that is displayed when the mouse hovers over the item's icon.</span></span> <span data-ttu-id="a7db5-137">Die Syntax ist identisch mit der, die für LocalizedString verwendet wird, einschließlich der Option, einfach anstelle eines Zeichen folgen Tabellen Verweises eine Zeichenfolge bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a7db5-137">The syntax is the same as that used for LocalizedString, including the option of simply providing a string rather than a string table reference.</span></span>
-   <span data-ttu-id="a7db5-138">**System. ApplicationName**.</span><span class="sxs-lookup"><span data-stu-id="a7db5-138">**System.ApplicationName**.</span></span> <span data-ttu-id="a7db5-139">REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a7db5-139">REG\_SZ.</span></span> <span data-ttu-id="a7db5-140">Der kanonische Name des Elements.</span><span class="sxs-lookup"><span data-stu-id="a7db5-140">The canonical name of the item.</span></span> <span data-ttu-id="a7db5-141">Der Befehl des Formulars `control.exe /name System.ApplicationName` öffnet das Element, z. b `control.exe /name MyCorporation.MySettings` ..</span><span class="sxs-lookup"><span data-stu-id="a7db5-141">The command of form `control.exe /name System.ApplicationName` opens the item; for example, `control.exe /name MyCorporation.MySettings`.</span></span> <span data-ttu-id="a7db5-142">Weitere Informationen zur Verwendung von Control.exe finden Sie unter [Ausführen von System Steuerungselementen](executing-control-panel-items.md) .</span><span class="sxs-lookup"><span data-stu-id="a7db5-142">See [Executing Control Panel Items](executing-control-panel-items.md) for more information on the use of Control.exe.</span></span>
-   <span data-ttu-id="a7db5-143">**System. ControlPanel. Category**.</span><span class="sxs-lookup"><span data-stu-id="a7db5-143">**System.ControlPanel.Category**.</span></span> <span data-ttu-id="a7db5-144">REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a7db5-144">REG\_SZ.</span></span> <span data-ttu-id="a7db5-145">Ein-Wert, der die System Steuerungs Kategorien deklariert, in denen das Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a7db5-145">A value that declares the Control Panel categories where the item appears.</span></span> <span data-ttu-id="a7db5-146">Mehrere Kategorien werden durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="a7db5-146">Multiple categories are separated by commas.</span></span> <span data-ttu-id="a7db5-147">Im obigen Beispiel gibt der-Eintrag an, dass das Element **meine Einstellungen** in den Kategorien Darstellung **und Personalisierung** und **Programme** angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7db5-147">In the case of the example above, the entry specifies that the **My Settings** item should appear in both the **Appearance and Personalization** and **Programs** categories.</span></span> <span data-ttu-id="a7db5-148">Weitere Kategoriewerte finden Sie unter [Zuweisen von System Steuerungs Kategorien](assigning-control-panel-categories.md) .</span><span class="sxs-lookup"><span data-stu-id="a7db5-148">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for possible category values.</span></span>
-   <span data-ttu-id="a7db5-149">**System. Software. tasksfileurl**.</span><span class="sxs-lookup"><span data-stu-id="a7db5-149">**System.Software.TasksFileUrl**.</span></span> <span data-ttu-id="a7db5-150">Reg \_ SZ oder reg \_ Expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a7db5-150">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="a7db5-151">Der Pfad der XML-Datei, die [Aufgaben Verknüpfungen](creating-searchable-task-links.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="a7db5-151">The path of the XML file that defines [task links](creating-searchable-task-links.md).</span></span> <span data-ttu-id="a7db5-152">Dies kann ein direkter Dateipfad sein, wie im Beispiel gezeigt, oder eine eingebettete Ressource, die als Modulname und Ressourcen-ID angegeben ist, z. b. "% Program Files% \\ MyCorp \\ myapp \\MyApp.exe,-31".</span><span class="sxs-lookup"><span data-stu-id="a7db5-152">This can be a direct file path as shown in the example, or an embedded resource specified as a module name and resource ID such as "%ProgramFiles%\\MyCorp\\MyApp\\MyApp.exe,-31".</span></span>

### <a name="step-4"></a><span data-ttu-id="a7db5-153">Schritt 4:</span><span class="sxs-lookup"><span data-stu-id="a7db5-153">Step 4:</span></span>

<span data-ttu-id="a7db5-154">Fügen Sie unter demselben GUID-Unterschlüssel der Registrierung den folgenden Unterschlüssel hinzu, um den Pfad der Datei anzugeben, die das Symbol und die Ressourcen-ID des Bilds in dieser Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="a7db5-154">Under that same GUID subkey, add the following subkey to the registry to provide the path of the file that contains the icon and the resource ID of the image within that file.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

<span data-ttu-id="a7db5-155">Beachten Sie, dass die Syntax in der Regel mit den oben erläuterten lokaltzeichen-und infotip-Einträgen vergleichbar ist, dass kein @-Zeichen als Präfix im reg \_ SZ-oder reg Expand-SZ-Eintrag verwendet wird, \_ \_ der den Pfad angibt.</span><span class="sxs-lookup"><span data-stu-id="a7db5-155">Note that while the syntax is otherwise similar to the LocalizedString and InfoTip entries discussed earlier, no '@' character is used as a prefix in the REG\_SZ or REG\_EXPAND\_SZ entry that specifies the path.</span></span>

### <a name="step-5"></a><span data-ttu-id="a7db5-156">Schritt 5:</span><span class="sxs-lookup"><span data-stu-id="a7db5-156">Step 5:</span></span>

<span data-ttu-id="a7db5-157">Fügen Sie der Registrierung die folgenden Informationen hinzu, um den Befehl bereitzustellen, der vom System aufgerufen wird, wenn der Benutzer die Systemsteuerung öffnet.</span><span class="sxs-lookup"><span data-stu-id="a7db5-157">Add the following information to the registry to provide the command that is called by the system when the user opens the Control Panel.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a><span data-ttu-id="a7db5-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a7db5-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7db5-159">System Steuerungselemente werden registriert</span><span class="sxs-lookup"><span data-stu-id="a7db5-159">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="a7db5-160">Registrieren von dll-System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="a7db5-160">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



