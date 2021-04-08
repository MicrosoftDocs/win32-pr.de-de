---
description: Die ServiceControl-Tabelle wird zum Steuern installierter oder nicht installierter Dienste verwendet. Beachten Sie, dass Dienste, die sich auf das vorhanden sein einer Assembly im globalen Assemblycache (GAC) verlassen, nicht mithilfe der Tabellen ServiceInstall und ServiceControl installiert oder gestartet werden können.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: ServiceControl-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2abd123e937673694dffd53773a16fcbd704c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757626"
---
# <a name="servicecontrol-table"></a><span data-ttu-id="d68ae-103">ServiceControl-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d68ae-103">ServiceControl Table</span></span>

<span data-ttu-id="d68ae-104">Die ServiceControl-Tabelle wird zum Steuern installierter oder nicht installierter Dienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="d68ae-104">The ServiceControl table is used to control installed or uninstalled services.</span></span>

> [!Note]  
> <span data-ttu-id="d68ae-105">Dienste, die sich auf das vorhanden sein einer [Assembly](assemblies.md) im globalen Assemblycache (GAC) stützen, können nicht mit den Tabellen [ServiceInstall](serviceinstall-table.md) und ServiceControl installiert oder gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="d68ae-105">Services that rely on the presence of an [assembly](assemblies.md) in the Global Assembly Cache (GAC) cannot be installed or started using the [ServiceInstall](serviceinstall-table.md) and ServiceControl tables.</span></span> <span data-ttu-id="d68ae-106">Wenn Sie einen Dienst starten müssen, der von einer Assembly im GAC abhängt, müssen Sie eine benutzerdefinierte Aktion verwenden, die nach der [InstallFinalize-Aktion](installfinalize-action.md) oder einer [benutzerdefinierten Commit-Aktion](commit-custom-actions.md)sequenziert ist.</span><span class="sxs-lookup"><span data-stu-id="d68ae-106">If you need to start a service that depends on an assembly in the GAC, you must use a custom action sequenced after the [InstallFinalize action](installfinalize-action.md) or a [commit custom action](commit-custom-actions.md).</span></span> <span data-ttu-id="d68ae-107">Informationen zum Installieren von Assemblys im GAC finden Sie unter Installieren von Assemblys [im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md).</span><span class="sxs-lookup"><span data-stu-id="d68ae-107">For information about installing assemblies to the GAC see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md).</span></span>

 

<span data-ttu-id="d68ae-108">Die ServiceControl-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="d68ae-108">The ServiceControl table has the following columns.</span></span>



| <span data-ttu-id="d68ae-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="d68ae-109">Column</span></span>         | <span data-ttu-id="d68ae-110">Typ</span><span class="sxs-lookup"><span data-stu-id="d68ae-110">Type</span></span>                         | <span data-ttu-id="d68ae-111">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d68ae-111">Key</span></span> | <span data-ttu-id="d68ae-112">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d68ae-112">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="d68ae-113">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="d68ae-113">ServiceControl</span></span> | [<span data-ttu-id="d68ae-114">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d68ae-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="d68ae-115">J</span><span class="sxs-lookup"><span data-stu-id="d68ae-115">Y</span></span>   | <span data-ttu-id="d68ae-116">N</span><span class="sxs-lookup"><span data-stu-id="d68ae-116">N</span></span>        |
| <span data-ttu-id="d68ae-117">Name</span><span class="sxs-lookup"><span data-stu-id="d68ae-117">Name</span></span>           | [<span data-ttu-id="d68ae-118">Großformatige</span><span class="sxs-lookup"><span data-stu-id="d68ae-118">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d68ae-119">N</span><span class="sxs-lookup"><span data-stu-id="d68ae-119">N</span></span>   | <span data-ttu-id="d68ae-120">N</span><span class="sxs-lookup"><span data-stu-id="d68ae-120">N</span></span>        |
| <span data-ttu-id="d68ae-121">Ereignis</span><span class="sxs-lookup"><span data-stu-id="d68ae-121">Event</span></span>          | [<span data-ttu-id="d68ae-122">Integer</span><span class="sxs-lookup"><span data-stu-id="d68ae-122">Integer</span></span>](integer.md)       | <span data-ttu-id="d68ae-123">N</span><span class="sxs-lookup"><span data-stu-id="d68ae-123">N</span></span>   | <span data-ttu-id="d68ae-124">N</span><span class="sxs-lookup"><span data-stu-id="d68ae-124">N</span></span>        |
| <span data-ttu-id="d68ae-125">Argumente</span><span class="sxs-lookup"><span data-stu-id="d68ae-125">Arguments</span></span>      | [<span data-ttu-id="d68ae-126">Großformatige</span><span class="sxs-lookup"><span data-stu-id="d68ae-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d68ae-127">N</span><span class="sxs-lookup"><span data-stu-id="d68ae-127">N</span></span>   | <span data-ttu-id="d68ae-128">J</span><span class="sxs-lookup"><span data-stu-id="d68ae-128">Y</span></span>        |
| <span data-ttu-id="d68ae-129">Warten</span><span class="sxs-lookup"><span data-stu-id="d68ae-129">Wait</span></span>           | [<span data-ttu-id="d68ae-130">Integer</span><span class="sxs-lookup"><span data-stu-id="d68ae-130">Integer</span></span>](integer.md)       | <span data-ttu-id="d68ae-131">N</span><span class="sxs-lookup"><span data-stu-id="d68ae-131">N</span></span>   | <span data-ttu-id="d68ae-132">J</span><span class="sxs-lookup"><span data-stu-id="d68ae-132">Y</span></span>        |
| <span data-ttu-id="d68ae-133">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="d68ae-133">Component\_</span></span>    | [<span data-ttu-id="d68ae-134">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d68ae-134">Identifier</span></span>](identifier.md) | <span data-ttu-id="d68ae-135">N</span><span class="sxs-lookup"><span data-stu-id="d68ae-135">N</span></span>   | <span data-ttu-id="d68ae-136">N</span><span class="sxs-lookup"><span data-stu-id="d68ae-136">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d68ae-137">Spalten</span><span class="sxs-lookup"><span data-stu-id="d68ae-137">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d68ae-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span><span class="sxs-lookup"><span data-stu-id="d68ae-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span></span>
</dt> <dd>

<span data-ttu-id="d68ae-139">Dies ist der Primärschlüssel dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d68ae-139">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="d68ae-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="d68ae-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="d68ae-141">Diese Spalte ist die Zeichenfolge, die den Dienst benennt.</span><span class="sxs-lookup"><span data-stu-id="d68ae-141">This column is the string naming the service.</span></span> <span data-ttu-id="d68ae-142">Diese Spalte kann verwendet werden, um einen Dienst zu steuern, der nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d68ae-142">This column can be used to control a service that is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="d68ae-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Veranstalter</span><span class="sxs-lookup"><span data-stu-id="d68ae-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="d68ae-144">Diese Spalte enthält die Vorgänge, die für den benannten Dienst durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d68ae-144">This column contains the operations to be performed on the named service.</span></span> <span data-ttu-id="d68ae-145">Beachten Sie, dass beim Beenden eines Diensts alle Dienste, die von diesem Dienst abhängen, ebenfalls angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="d68ae-145">Note that when stopping a service, all services that depend on that service are also stopped.</span></span> <span data-ttu-id="d68ae-146">Wenn Sie einen Dienst löschen, der ausgeführt wird, beendet der Installer den Dienst.</span><span class="sxs-lookup"><span data-stu-id="d68ae-146">When deleting a service that is running, the installer stops the service.</span></span>

<span data-ttu-id="d68ae-147">Die Werte in diesem Feld sind Bitfelder, die zu einem einzelnen Wert zusammengefasst werden können, der mehrere Vorgänge darstellt.</span><span class="sxs-lookup"><span data-stu-id="d68ae-147">The values in this field are bit fields that can be combined into a single value that represents several operations.</span></span>

<span data-ttu-id="d68ae-148">Die folgenden Werte werden nur während einer-Installation verwendet.</span><span class="sxs-lookup"><span data-stu-id="d68ae-148">The following values are only used during an installation.</span></span>



| <span data-ttu-id="d68ae-149">Konstante</span><span class="sxs-lookup"><span data-stu-id="d68ae-149">Constant</span></span>                           | <span data-ttu-id="d68ae-150">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="d68ae-150">Hexadecimal</span></span> | <span data-ttu-id="d68ae-151">Decimal</span><span class="sxs-lookup"><span data-stu-id="d68ae-151">Decimal</span></span> | <span data-ttu-id="d68ae-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d68ae-152">Description</span></span>                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d68ae-153">**msidbservicecontroleventstart**</span><span class="sxs-lookup"><span data-stu-id="d68ae-153">**msidbServiceControlEventStart**</span></span>  | <span data-ttu-id="d68ae-154">0x001</span><span class="sxs-lookup"><span data-stu-id="d68ae-154">0x001</span></span>       | <span data-ttu-id="d68ae-155">1</span><span class="sxs-lookup"><span data-stu-id="d68ae-155">1</span></span>       | <span data-ttu-id="d68ae-156">Startet den Dienst während der [Start Services-Aktion](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="d68ae-156">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="d68ae-157">**msidbservicecontroleventhalte**</span><span class="sxs-lookup"><span data-stu-id="d68ae-157">**msidbServiceControlEventStop**</span></span>   | <span data-ttu-id="d68ae-158">0x002</span><span class="sxs-lookup"><span data-stu-id="d68ae-158">0x002</span></span>       | <span data-ttu-id="d68ae-159">2</span><span class="sxs-lookup"><span data-stu-id="d68ae-159">2</span></span>       | <span data-ttu-id="d68ae-160">Beendet den Dienst während der [Stop Services-Aktion](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="d68ae-160">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="d68ae-161">(none)</span><span class="sxs-lookup"><span data-stu-id="d68ae-161">(none)</span></span>                             | <span data-ttu-id="d68ae-162">0x004</span><span class="sxs-lookup"><span data-stu-id="d68ae-162">0x004</span></span>       | <span data-ttu-id="d68ae-163">4</span><span class="sxs-lookup"><span data-stu-id="d68ae-163">4</span></span>       | <reserved>                                                                   |
| <span data-ttu-id="d68ae-164">**msidbservicecontroleventdelete**</span><span class="sxs-lookup"><span data-stu-id="d68ae-164">**msidbServiceControlEventDelete**</span></span> | <span data-ttu-id="d68ae-165">0x008</span><span class="sxs-lookup"><span data-stu-id="d68ae-165">0x008</span></span>       | <span data-ttu-id="d68ae-166">8</span><span class="sxs-lookup"><span data-stu-id="d68ae-166">8</span></span>       | <span data-ttu-id="d68ae-167">Löscht den Dienst während der [Delta](deleteservices-action.md)Service-Aktion.</span><span class="sxs-lookup"><span data-stu-id="d68ae-167">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

<span data-ttu-id="d68ae-168">Die folgenden Werte werden nur während einer Deinstallation verwendet.</span><span class="sxs-lookup"><span data-stu-id="d68ae-168">The following values are only used during an uninstall.</span></span>



| <span data-ttu-id="d68ae-169">Konstante</span><span class="sxs-lookup"><span data-stu-id="d68ae-169">Constant</span></span>                                    | <span data-ttu-id="d68ae-170">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="d68ae-170">Hexadecimal</span></span> | <span data-ttu-id="d68ae-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="d68ae-171">Decimal</span></span> | <span data-ttu-id="d68ae-172">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d68ae-172">Description</span></span>                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d68ae-173">**msidbservicecontroleventuninstallstart**</span><span class="sxs-lookup"><span data-stu-id="d68ae-173">**msidbServiceControlEventUninstallStart**</span></span>  | <span data-ttu-id="d68ae-174">0x010</span><span class="sxs-lookup"><span data-stu-id="d68ae-174">0x010</span></span>       | <span data-ttu-id="d68ae-175">16</span><span class="sxs-lookup"><span data-stu-id="d68ae-175">16</span></span>      | <span data-ttu-id="d68ae-176">Startet den Dienst während der [Start Services-Aktion](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="d68ae-176">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="d68ae-177">**msidbservicecontroleventuninstallstopps**</span><span class="sxs-lookup"><span data-stu-id="d68ae-177">**msidbServiceControlEventUninstallStop**</span></span>   | <span data-ttu-id="d68ae-178">0x020</span><span class="sxs-lookup"><span data-stu-id="d68ae-178">0x020</span></span>       | <span data-ttu-id="d68ae-179">32</span><span class="sxs-lookup"><span data-stu-id="d68ae-179">32</span></span>      | <span data-ttu-id="d68ae-180">Beendet den Dienst während der [Stop Services-Aktion](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="d68ae-180">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="d68ae-181">(none)</span><span class="sxs-lookup"><span data-stu-id="d68ae-181">(none)</span></span>                                      | <span data-ttu-id="d68ae-182">0x040</span><span class="sxs-lookup"><span data-stu-id="d68ae-182">0x040</span></span>       | <span data-ttu-id="d68ae-183">64</span><span class="sxs-lookup"><span data-stu-id="d68ae-183">64</span></span>      | <reserved>                                                                   |
| <span data-ttu-id="d68ae-184">**msidbservicecontroleventuninstalldelete**</span><span class="sxs-lookup"><span data-stu-id="d68ae-184">**msidbServiceControlEventUninstallDelete**</span></span> | <span data-ttu-id="d68ae-185">0x080</span><span class="sxs-lookup"><span data-stu-id="d68ae-185">0x080</span></span>       | <span data-ttu-id="d68ae-186">128</span><span class="sxs-lookup"><span data-stu-id="d68ae-186">128</span></span>     | <span data-ttu-id="d68ae-187">Löscht den Dienst während der [Delta](deleteservices-action.md)Service-Aktion.</span><span class="sxs-lookup"><span data-stu-id="d68ae-187">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="d68ae-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentation</span><span class="sxs-lookup"><span data-stu-id="d68ae-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="d68ae-189">Eine Liste von Argumenten zum Starten von Diensten.</span><span class="sxs-lookup"><span data-stu-id="d68ae-189">A list of arguments for starting services.</span></span> <span data-ttu-id="d68ae-190">Die Argumente sind durch Null Zeichen voneinander getrennt \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="d68ae-190">The arguments are separated by null characters \[~\].</span></span> <span data-ttu-id="d68ae-191">Die Liste der Argumente 1, 2 und 3 wird z. b. wie folgt aufgelistet: 1 \[ ~ \] 2 \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="d68ae-191">For example, the list of arguments One, Two, and Three are listed as: One\[~\]Two\[~\]Three.</span></span>

</dd> <dt>

<span data-ttu-id="d68ae-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Warte</span><span class="sxs-lookup"><span data-stu-id="d68ae-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Wait</span></span>
</dt> <dd>

<span data-ttu-id="d68ae-193">Wenn Sie dieses Feld auf Null setzen oder den Wert 1 eingeben, wartet das Installationsprogramm maximal 30 Sekunden, bis der Dienst beendet ist, bevor der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d68ae-193">Leaving this field null or entering a value of 1 causes the installer to wait a maximum of 30 seconds for the service to complete before proceeding.</span></span> <span data-ttu-id="d68ae-194">Der Warte Vorgang kann verwendet werden, um zusätzliche Zeit für das Zurückgeben eines Fehler Fehlers durch ein kritisches Ereignis zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="d68ae-194">The wait can be used to allow additional time for a critical event to return a failure error.</span></span> <span data-ttu-id="d68ae-195">Der Wert 0 (null) bedeutet, dass nur gewartet werden soll, bis der Dienststeuerungs-Manager (SCM) meldet, dass sich dieser Dienst in einem ausstehenden Zustand befindet, bevor die Installation fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d68ae-195">A value of 0 in this field means to wait only until the service control manager (SCM) reports that this service is in a pending state before continuing with the installation.</span></span>

</dd> <dt>

<span data-ttu-id="d68ae-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="d68ae-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="d68ae-197">Externer Schlüssel für Spalte einer der [Komponenten Tabellen](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d68ae-197">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d68ae-198">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d68ae-198">Remarks</span></span>

<span data-ttu-id="d68ae-199">Die Aktionen " [Start Services](startservices-action.md)", " [Stop Services](stopservices-action.md)" und " [Delta Service](deleteservices-action.md) " in [*Sequenz Tabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d68ae-199">The [StartServices](startservices-action.md), [StopServices](stopservices-action.md), and [DeleteServices](deleteservices-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="d68ae-200">Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="d68ae-200">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="d68ae-201">Verwenden Sie die Spalte Name, um Dienste zu starten, zu verhindern oder zu löschen, die durch die-Installation ersetzt werden oder von einem neuen Dienst abhängen, der installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d68ae-201">Use the Name column to start, stop, or delete services that are being replaced by the installation or that are dependent upon a new service that is being installed.</span></span> <span data-ttu-id="d68ae-202">Wenn Sie z. b. MyService in die ServiceControl-Spalte eingeben, kann dieser Dienst in der Component-Spalte mit MyComponent verknüpft werden \_ .</span><span class="sxs-lookup"><span data-stu-id="d68ae-202">For example, entering MyService into the ServiceControl column can tie this service to MyComponent in the Component\_ column.</span></span> <span data-ttu-id="d68ae-203">Wenn das Bitfeld in der Ereignis Spalte für Start bei der Installation von festgelegt wird, startet das Installationsprogramm MyService, wenn MyComponent installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d68ae-203">If the bit field in the Event column is set for start while installing, then the installer starts MyService when installing MyComponent.</span></span>

## <a name="validation"></a><span data-ttu-id="d68ae-204">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="d68ae-204">Validation</span></span>

<dl>

[<span data-ttu-id="d68ae-205">ICE03</span><span class="sxs-lookup"><span data-stu-id="d68ae-205">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d68ae-206">ICE06</span><span class="sxs-lookup"><span data-stu-id="d68ae-206">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d68ae-207">ICE32</span><span class="sxs-lookup"><span data-stu-id="d68ae-207">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d68ae-208">ICE45</span><span class="sxs-lookup"><span data-stu-id="d68ae-208">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="d68ae-209">ICE46</span><span class="sxs-lookup"><span data-stu-id="d68ae-209">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="d68ae-210">ICE69</span><span class="sxs-lookup"><span data-stu-id="d68ae-210">ICE69</span></span>](ice69.md)  
</dl>

 

 



