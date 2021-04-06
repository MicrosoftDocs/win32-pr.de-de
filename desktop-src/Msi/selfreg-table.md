---
description: Die Tabelle selfreg enthält Informationen zu Modulen, die selbst registriert werden müssen.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Selfreg-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5895b1d23369a7c121547fed841731b5d3e76ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760146"
---
# <a name="selfreg-table"></a><span data-ttu-id="c16b3-103">Selfreg-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c16b3-103">SelfReg Table</span></span>

<span data-ttu-id="c16b3-104">Die Tabelle selfreg enthält Informationen zu Modulen, die selbst registriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c16b3-104">The SelfReg table contains information about modules that need to be self registered.</span></span> <span data-ttu-id="c16b3-105">Der Installer Ruft die [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) -Funktion während der Installation des Moduls auf. [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) wird während der Installation des Moduls aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c16b3-105">The installer calls the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function during installation of the module; it calls [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) during uninstallation of the module.</span></span> <span data-ttu-id="c16b3-106">EXE-Dateien werden vom Installationsprogramm nicht selbst registriert.</span><span class="sxs-lookup"><span data-stu-id="c16b3-106">The installer does not self register EXE files.</span></span>

<span data-ttu-id="c16b3-107">Die Tabelle selfreg weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="c16b3-107">The SelfReg table has the following columns.</span></span>



| <span data-ttu-id="c16b3-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="c16b3-108">Column</span></span> | <span data-ttu-id="c16b3-109">Typ</span><span class="sxs-lookup"><span data-stu-id="c16b3-109">Type</span></span>                         | <span data-ttu-id="c16b3-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c16b3-110">Key</span></span> | <span data-ttu-id="c16b3-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="c16b3-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="c16b3-112">Datei\_</span><span class="sxs-lookup"><span data-stu-id="c16b3-112">File\_</span></span> | [<span data-ttu-id="c16b3-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="c16b3-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="c16b3-114">J</span><span class="sxs-lookup"><span data-stu-id="c16b3-114">Y</span></span>   | <span data-ttu-id="c16b3-115">N</span><span class="sxs-lookup"><span data-stu-id="c16b3-115">N</span></span>        |
| <span data-ttu-id="c16b3-116">„Cost“ (Kosten)</span><span class="sxs-lookup"><span data-stu-id="c16b3-116">Cost</span></span>   | [<span data-ttu-id="c16b3-117">Integer</span><span class="sxs-lookup"><span data-stu-id="c16b3-117">Integer</span></span>](integer.md)       | <span data-ttu-id="c16b3-118">N</span><span class="sxs-lookup"><span data-stu-id="c16b3-118">N</span></span>   | <span data-ttu-id="c16b3-119">J</span><span class="sxs-lookup"><span data-stu-id="c16b3-119">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c16b3-120">Spalten</span><span class="sxs-lookup"><span data-stu-id="c16b3-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c16b3-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_</span><span class="sxs-lookup"><span data-stu-id="c16b3-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="c16b3-122">Externer Schlüssel in die erste Spalte der [Dateitabelle](file-table.md) , die das Modul angibt, das registriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c16b3-122">External key into the first column of the [File table](file-table.md) indicating the module that needs to be registered.</span></span>

</dd> <dt>

<span data-ttu-id="c16b3-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Preis</span><span class="sxs-lookup"><span data-stu-id="c16b3-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="c16b3-124">Die Kosten für die Registrierung des Moduls in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c16b3-124">The cost of registering the module in bytes.</span></span> <span data-ttu-id="c16b3-125">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="c16b3-125">This must be a non-negative number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c16b3-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c16b3-126">Remarks</span></span>

<span data-ttu-id="c16b3-127">Die Autoren von Installationspaketen werden dringend von der Verwendung der Selbstregistrierung abgeraten.</span><span class="sxs-lookup"><span data-stu-id="c16b3-127">Installation package authors are strongly advised against using self registration.</span></span> <span data-ttu-id="c16b3-128">Stattdessen sollten Sie Module registrieren, indem Sie eine oder mehrere Tabellen erstellen, die für diesen Zweck vom Installationsprogramm bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c16b3-128">Instead they should register modules by authoring one or more tables provided by the installer for this purpose.</span></span> <span data-ttu-id="c16b3-129">Weitere Informationen finden Sie unter [Gruppe "Registrierungs Tabellen](registry-tables-group.md)".</span><span class="sxs-lookup"><span data-stu-id="c16b3-129">For more information, see [Registry Tables Group](registry-tables-group.md).</span></span> <span data-ttu-id="c16b3-130">Viele der Vorteile eines zentralen Installations Diensts gehen bei der Selbstregistrierung verloren, da in der Regel selbst Registrierungs Routinen wichtige Konfigurationsinformationen ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="c16b3-130">Many of the benefits of having a central installer service are lost with self registration because self-registration routines tend to hide critical configuration information.</span></span> <span data-ttu-id="c16b3-131">Gründe für die Vermeidung der Selbstregistrierung:</span><span class="sxs-lookup"><span data-stu-id="c16b3-131">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="c16b3-132">Das Rollback einer Installation mit selbst registrierten Modulen kann nicht sicher mithilfe von " [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) " durchgeführt werden, da es keine Möglichkeit gibt, zu sagen, ob die selbst registrierten Schlüssel von einem anderen Feature oder einer Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c16b3-132">Rollback of an installation with self-registered modules cannot be safely done using [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) because there is no way of telling if the self-registered keys are used by another feature or application.</span></span>
-   <span data-ttu-id="c16b3-133">Die Möglichkeit zur Verwendung von Ankündigungen wird verringert, wenn die Registrierung der Klassen-oder Erweiterungs Server in selbst Registrierungs Routinen erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c16b3-133">The ability to use advertisement is reduced if Class or extension server registration is performed within self-registration routines.</span></span>
-   <span data-ttu-id="c16b3-134">Der Installer verarbeitet automatisch HKCR-Schlüssel in den Registrierungs Tabellen für Benutzer-oder Computer spezifische Installationen.</span><span class="sxs-lookup"><span data-stu-id="c16b3-134">The installer automatically handles HKCR keys in the registry tables for both per-user or per-machine installations.</span></span> <span data-ttu-id="c16b3-135">[**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) -Routinen unterstützen derzeit nicht das Konzept eines benutzerspezifischen HKCR-Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="c16b3-135">[**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) routines currently do not support the notion of a per-user HKCR key.</span></span>
-   <span data-ttu-id="c16b3-136">Wenn mehrere Benutzer eine selbst registrierte Anwendung auf dem gleichen Computer verwenden, muss jeder Benutzer die Anwendung beim ersten Ausführen installieren.</span><span class="sxs-lookup"><span data-stu-id="c16b3-136">If multiple users are using a self-registered application on the same computer, each user must install the application the first time they run it.</span></span> <span data-ttu-id="c16b3-137">Andernfalls kann das Installationsprogramm nicht einfach ermitteln, ob die richtigen HKCU-Registrierungsschlüssel vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c16b3-137">Otherwise the installer cannot easily determine that the proper HKCU registry keys exist.</span></span>
-   <span data-ttu-id="c16b3-138">Dem [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) kann der Zugriff auf Netzwerkressourcen, z. b. Typbibliotheken, verweigert werden, wenn eine Komponente sowohl als "aus der Quelle ausführen" angegeben ist als auch in der Tabelle "selfreg" aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="c16b3-138">The [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) can be denied access to network resources such as type libraries if a component is both specified as run-from-source and is listed in the SelfReg table.</span></span> <span data-ttu-id="c16b3-139">Dies kann dazu führen, dass bei der Installation der Komponente während einer administrativen Installation ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c16b3-139">This can cause the installation of the component to fail to during an administrative installation.</span></span>
-   <span data-ttu-id="c16b3-140">Selbst registrierte DLLs sind anfälliger für Codierungsfehler, da der für [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) erforderliche neue Code für jede DLL häufig anders ist.</span><span class="sxs-lookup"><span data-stu-id="c16b3-140">Self-registering DLLs are more susceptible to coding errors because the new code required for [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) is commonly different for each DLL.</span></span> <span data-ttu-id="c16b3-141">Verwenden Sie stattdessen die Registrierungs Tabellen in der-Datenbank, um den vorhandenen Code zu nutzen, der vom Installationsprogramm bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c16b3-141">Instead use the registry tables in the database to take advantage of existing code provided by the installer.</span></span>
-   <span data-ttu-id="c16b3-142">Selbst registrierte DLLs können manchmal mit zusätzlichen DLLs verknüpft werden, die nicht vorhanden sind oder die falsche Version sind.</span><span class="sxs-lookup"><span data-stu-id="c16b3-142">Self-registering DLLs can sometimes link to auxiliary DLLs that are not present or are the wrong version.</span></span> <span data-ttu-id="c16b3-143">Im Gegensatz dazu kann das Installationsprogramm die DLLs unter Verwendung der Registrierungs Tabellen registrieren, ohne dass vom aktuellen Status des Systems abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="c16b3-143">In contrast, the installer can register the DLLs using the registry tables with no dependency on the current state of the system.</span></span>

> [!Note]  
> <span data-ttu-id="c16b3-144">Sie können nicht die Reihenfolge angeben, in der der Installer mithilfe der [SelfRegModules](selfregmodules-action.md) -und [selfunregmodules](selfunregmodules-action.md) -Aktionen selbst registrierte DLLs registriert bzw. die Registrierung aufheben.</span><span class="sxs-lookup"><span data-stu-id="c16b3-144">You cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="c16b3-145">Siehe [angeben der Reihenfolge der Selbstregistrierung](specifying-the-order-of-self-registration.md).</span><span class="sxs-lookup"><span data-stu-id="c16b3-145">See [Specifying the Order of Self Registration](specifying-the-order-of-self-registration.md).</span></span>

 

## <a name="validation"></a><span data-ttu-id="c16b3-146">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="c16b3-146">Validation</span></span>

<dl>

[<span data-ttu-id="c16b3-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="c16b3-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c16b3-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="c16b3-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c16b3-149">ICE32</span><span class="sxs-lookup"><span data-stu-id="c16b3-149">ICE32</span></span>](ice32.md)  
</dl>

 

 
