---
description: System Steuerungselemente, die in einer DLL implementiert sind, die die CPlApplet-Funktion exportiert, haben unterschiedliche Registrierungsanforderungen als exe-Dateien.
title: Registrieren von dll-System Steuerungselementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756505"
---
# <a name="how-to-register-dll-control-panel-items"></a><span data-ttu-id="4eb21-103">Registrieren von dll-System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="4eb21-103">How to Register DLL Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="4eb21-104">Aktuelle Implementierungs Richtlinien gibt an, dass neue System Steuerungselemente als exe-Dateien anstatt als cpl-Dateien implementiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4eb21-104">Current implementation guidelines state that new Control Panel items should be implemented as .exe files rather than .cpl files.</span></span> <span data-ttu-id="4eb21-105">Die folgenden Informationen sind hauptsächlich für Legacy Zwecke enthalten.</span><span class="sxs-lookup"><span data-stu-id="4eb21-105">The following information is included mainly for legacy purposes.</span></span>

 

<span data-ttu-id="4eb21-106">System Steuerungselemente, die in einer DLL implementiert sind, die die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion exportiert, haben unterschiedliche Registrierungsanforderungen als exe-Dateien.</span><span class="sxs-lookup"><span data-stu-id="4eb21-106">Control Panel items that are implemented in a DLL that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function have different registration requirements than .exe files.</span></span> <span data-ttu-id="4eb21-107">Ab Windows XP sollten im Ordner "Programme" des Ordners der zugehörigen Anwendung neue DLLs für System Steuerungselemente installiert werden.</span><span class="sxs-lookup"><span data-stu-id="4eb21-107">As of Windows XP, new Control Panel item DLLs should be installed in the associated application's folder under the Program Files folder.</span></span> <span data-ttu-id="4eb21-108">Elemente, die im Verzeichnis "System32" mit der Erweiterung ". cpl" gespeichert sind, müssen nicht registriert werden. Sie werden automatisch in der Systemsteuerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4eb21-108">Items that are stored in the System32 directory with a .cpl extension do not need to be registered; they are automatically shown in the Control Panel.</span></span> <span data-ttu-id="4eb21-109">Alle anderen System Steuerungselemente, die **CPlApplet** verwenden, müssen auf eine von zwei Arten registriert werden:</span><span class="sxs-lookup"><span data-stu-id="4eb21-109">All other Control Panel items that use **CPlApplet** must be registered in one of two ways:</span></span>

-   <span data-ttu-id="4eb21-110">Wenn das System Steuerungselement für alle Benutzer verfügbar sein soll, registrieren Sie den Pfad auf Computer Basis, indem Sie den Wert " **reg \_ Expand \_ SZ** " zu **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Systemsteuerung** \\ **CPLS** unter Key festlegen. Legen Sie dabei auf den DLL-Pfad fest.</span><span class="sxs-lookup"><span data-stu-id="4eb21-110">If the Control Panel item is to be available to all users, register the path on a per-computer basis by adding a **REG\_EXPAND\_SZ** value to the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Control Panel**\\**Cpls** subkey, set to the DLL path.</span></span>
-   <span data-ttu-id="4eb21-111">Wenn das System Steuerungselement auf Benutzerbasis verfügbar sein soll, verwenden Sie den **aktuellen HKEY- \_ \_ Benutzer** als Stamm Schlüssel anstelle des **lokalen HKEY- \_ \_** Computers.</span><span class="sxs-lookup"><span data-stu-id="4eb21-111">If the Control Panel item is to be available on a per-user basis, use **HKEY\_CURRENT\_USER** as the root key instead of **HKEY\_LOCAL\_MACHINE**.</span></span>

<span data-ttu-id="4eb21-112">In den folgenden zwei Beispielen wird das System Steuerungselement *mycplapp* registriert.</span><span class="sxs-lookup"><span data-stu-id="4eb21-112">The following two examples register the *MyCplApp* Control Panel item.</span></span> <span data-ttu-id="4eb21-113">Die dll wird MyCpl.cpl benannt und befindet sich im Anwendungsverzeichnis *MyCorp \\ myapp* .</span><span class="sxs-lookup"><span data-stu-id="4eb21-113">The DLL is named MyCpl.cpl and is located in the *MyCorp\\MyApp* application directory.</span></span> <span data-ttu-id="4eb21-114">Dieses erste Beispiel veranschaulicht die Registrierung pro Computer.</span><span class="sxs-lookup"><span data-stu-id="4eb21-114">This first example illustrates per-computer registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="4eb21-115">Instructions</span><span class="sxs-lookup"><span data-stu-id="4eb21-115">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="4eb21-116">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="4eb21-116">Step 1:</span></span>

<span data-ttu-id="4eb21-117">Fügen Sie diese Informationen in die Registrierung ein, um das vorhanden sein der CPL-Datei zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="4eb21-117">Add this information to the registry to register the existence of the .cpl file.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a><span data-ttu-id="4eb21-118">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="4eb21-118">Step 2:</span></span>

<span data-ttu-id="4eb21-119">**Windows Vista und höher:** Fügen Sie der Registrierung diese zusätzlichen Informationen hinzu, um eine GUID für das System Steuerungselement bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4eb21-119">**Windows Vista and later:** Add this additional information to the registry to provide a GUID for the Control Panel item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

<span data-ttu-id="4eb21-120">Durch das Erstellen einer GUID zur eindeutigen Identifizierung des System Steuerungs Elements können Sie der Systemsteuerung Aufgaben Verknüpfungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4eb21-120">By generating a GUID to uniquely identify the Control Panel item, you can add task links to the Control Panel.</span></span> <span data-ttu-id="4eb21-121">Ohne diese GUID gibt es keine Möglichkeit, dass die Aufgaben Verknüpfungen mit dem System Steuerungselement verknüpft werden können.</span><span class="sxs-lookup"><span data-stu-id="4eb21-121">Without this GUID, there is no way for the task links to be associated with the Control Panel item.</span></span> <span data-ttu-id="4eb21-122">Weitere Informationen finden Sie unter [Erstellen durch suchbarer Aufgaben Verknüpfungen für ein System Steuerungselement](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="4eb21-122">See [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="4eb21-123">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="4eb21-123">Step 3:</span></span>

<span data-ttu-id="4eb21-124">**Windows Vista und höher:** Fügen Sie der Registrierung die folgenden Informationen hinzu, um einen kanonischen Namen für das Element zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4eb21-124">**Windows Vista and later:** Add the following information to the registry to create a canonical name for the item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

<span data-ttu-id="4eb21-125">Wenn Sie einen kanonischen Namen hinzufügen, können Benutzer das System Steuerungselement über eine Befehlszeile starten, indem Sie eingeben `control.exe /name MyCorporation.MyCpl` .</span><span class="sxs-lookup"><span data-stu-id="4eb21-125">By adding a canonical name, users can launch the Control Panel item from a command line by entering `control.exe /name MyCorporation.MyCpl`.</span></span> <span data-ttu-id="4eb21-126">Dies ermöglicht es auch, eine Implementierung von einer CPL-Datei in eine exe-Datei zu einem späteren Zeitpunkt zu ändern, ohne dass Programme aufgerufen werden müssen, um Änderungen vorzunehmen, da Sie das Element weiterhin durch den kanonischen Namen öffnen können.</span><span class="sxs-lookup"><span data-stu-id="4eb21-126">This also makes it possible to change an implementation from a .cpl file to a .exe file later, without requiring calling programs to make any changes since they can continue opening the item through its canonical name.</span></span> <span data-ttu-id="4eb21-127">Weitere Informationen zu kanonischen Namen finden Sie unter [Ausführen von System Steuerungselementen](executing-control-panel-items.md).</span><span class="sxs-lookup"><span data-stu-id="4eb21-127">For more information on canonical names, see [Executing Control Panel Items](executing-control-panel-items.md).</span></span>

### <a name="step-4"></a><span data-ttu-id="4eb21-128">Schritt 4:</span><span class="sxs-lookup"><span data-stu-id="4eb21-128">Step 4:</span></span>

<span data-ttu-id="4eb21-129">**Windows Vista und höher:** Fügen Sie der Registrierung die folgenden Informationen hinzu, um ein System Steuerungselement einer oder mehreren Kategorien zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="4eb21-129">**Windows Vista and later:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="4eb21-130">**Windows XP:** Fügen Sie der Registrierung die folgenden Informationen hinzu, um ein System Steuerungselement einer oder mehreren Kategorien zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="4eb21-130">**Windows XP:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="4eb21-131">In diesem Beispiel wird das Element der Kategorie 3 zugewiesen, d. h. Netzwerk und Internet.</span><span class="sxs-lookup"><span data-stu-id="4eb21-131">This example assigns the item to category 3, which is Network and Internet.</span></span> <span data-ttu-id="4eb21-132">Wenn Sie ein Element mehreren Kategorien hinzufügen möchten, geben Sie die Liste als reg- \_ SZ-Wert an, der durch Kommas getrennt ist, z. b. "3, 8".</span><span class="sxs-lookup"><span data-stu-id="4eb21-132">To add an item to multiple categories, provide the list as a REG\_SZ value separated by commas, such as "3,8".</span></span> <span data-ttu-id="4eb21-133">Werte können als Dezimal oder hexadezimal angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4eb21-133">Values can be provided as either decimal or hexadecimal.</span></span> <span data-ttu-id="4eb21-134">Beachten Sie, dass die Möglichkeit zum Hinzufügen eines Elements zu mehreren Kategorien nur in Windows XP Service Pack 2 (SP2) und höher möglich ist.</span><span class="sxs-lookup"><span data-stu-id="4eb21-134">Note that the ability to add an item to multiple categories is only possible in Windows XP Service Pack 2 (SP2) and later.</span></span> <span data-ttu-id="4eb21-135">Alle möglichen Werte finden Sie unter [Zuweisen von System Steuerungs Kategorien](assigning-control-panel-categories.md) .</span><span class="sxs-lookup"><span data-stu-id="4eb21-135">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for all possible values.</span></span>

### <a name="step-5"></a><span data-ttu-id="4eb21-136">Schritt 5:</span><span class="sxs-lookup"><span data-stu-id="4eb21-136">Step 5:</span></span>

<span data-ttu-id="4eb21-137">**Windows Vista und höher:** Fügen Sie der Registrierung die folgenden Informationen hinzu, um auf eine XML-Datei zum Speichern von Aufgaben Verknüpfungen für das Element zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="4eb21-137">**Windows Vista and later:** Add the following information to the registry to create and point to an XML file to hold task links for the item.</span></span> <span data-ttu-id="4eb21-138">Der Wert muss ein REG SZ-Pfad sein, \_ wie hier gezeigt, oder ein Modul und eine Ressourcen-ID (z. b. "C: \\ Program Files \\ MyCorp \\ myapp \\MyApp.exe,-31"), wenn es sich um eine eingebettete Ressource handelt.</span><span class="sxs-lookup"><span data-stu-id="4eb21-138">The value must be a REG\_SZ path as shown here or a module and resource ID (for example, "C:\\Program Files\\MyCorp\\MyApp\\MyApp.exe,-31") if it is an embedded resource.</span></span> <span data-ttu-id="4eb21-139">Der Speicherort der XML-Datei muss vollständig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4eb21-139">The location of the XML file should be fully specified.</span></span> <span data-ttu-id="4eb21-140">Eine Umgebungsvariable, z. b .% Program Files%, kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4eb21-140">It cannot use an environment variable such as %ProgramFiles%.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

<span data-ttu-id="4eb21-141">Weitere Informationen zu Aufgaben Verknüpfungen und zum Erstellen der XML-Datei, um Sie zu speichern, finden Sie unter [Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="4eb21-141">For more details on task links and how to create the XML file to hold them, see [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4eb21-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4eb21-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eb21-143">System Steuerungselemente werden registriert</span><span class="sxs-lookup"><span data-stu-id="4eb21-143">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="4eb21-144">Registrieren von ausführbaren System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="4eb21-144">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
