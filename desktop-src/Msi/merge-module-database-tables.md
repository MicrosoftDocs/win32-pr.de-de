---
description: Die folgenden Tabellen sind in einem standardmäßigen Mergemodul erforderlich.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Modul Datenbanktabellen zusammenführen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351432"
---
# <a name="merge-module-database-tables"></a><span data-ttu-id="f92eb-103">Modul Datenbanktabellen zusammenführen</span><span class="sxs-lookup"><span data-stu-id="f92eb-103">Merge Module Database Tables</span></span>

<span data-ttu-id="f92eb-104">Die folgenden Tabellen sind in einem standardmäßigen Mergemodul erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f92eb-104">The following tables are required in a standard merge module.</span></span>



| <span data-ttu-id="f92eb-105">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="f92eb-105">Table name</span></span>                                       | <span data-ttu-id="f92eb-106">Kommentar</span><span class="sxs-lookup"><span data-stu-id="f92eb-106">Comment</span></span>                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f92eb-107">Komponente</span><span class="sxs-lookup"><span data-stu-id="f92eb-107">Component</span></span>](component-table.md)                 | <span data-ttu-id="f92eb-108">Benötigten</span><span class="sxs-lookup"><span data-stu-id="f92eb-108">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="f92eb-109">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="f92eb-109">Directory</span></span>](directory-table.md)                 | <span data-ttu-id="f92eb-110">Benötigten</span><span class="sxs-lookup"><span data-stu-id="f92eb-110">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="f92eb-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="f92eb-111">FeatureComponents</span></span>](featurecomponents-table.md) | <span data-ttu-id="f92eb-112">Benötigten</span><span class="sxs-lookup"><span data-stu-id="f92eb-112">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="f92eb-113">File</span><span class="sxs-lookup"><span data-stu-id="f92eb-113">File</span></span>](file-table.md)                           | <span data-ttu-id="f92eb-114">Benötigten</span><span class="sxs-lookup"><span data-stu-id="f92eb-114">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="f92eb-115">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="f92eb-115">ModuleSignature</span></span>](modulesignature-table.md)     | <span data-ttu-id="f92eb-116">Benötigten In der Installer-Datenbank zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="f92eb-116">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="f92eb-117">Listet die Informationen auf, die ein Mergemodul identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f92eb-117">Lists the information identifying a merge module.</span></span> |
| [<span data-ttu-id="f92eb-118">Modulecomponents</span><span class="sxs-lookup"><span data-stu-id="f92eb-118">ModuleComponents</span></span>](modulecomponents-table.md)   | <span data-ttu-id="f92eb-119">Benötigten In der Installer-Datenbank zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="f92eb-119">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="f92eb-120">Listet alle Komponenten im Mergemodul auf.</span><span class="sxs-lookup"><span data-stu-id="f92eb-120">Lists all the components in the merge module.</span></span>     |



 

<span data-ttu-id="f92eb-121">Die folgenden Tabellen treten nur in Mergemodulen oder anderen Installer-Datenbanken auf, die bereits mit einem Mergemodul kombiniert wurden.</span><span class="sxs-lookup"><span data-stu-id="f92eb-121">The following tables only occur in merge modules or other installer databases that have already been combined with a merge module.</span></span>



| <span data-ttu-id="f92eb-122">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="f92eb-122">Table name</span></span>                                     | <span data-ttu-id="f92eb-123">Kommentar</span><span class="sxs-lookup"><span data-stu-id="f92eb-123">Comment</span></span>                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f92eb-124">Moduleabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="f92eb-124">ModuleDependency</span></span>](moduledependency-table.md) | <span data-ttu-id="f92eb-125">In der Installer-Datenbank zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="f92eb-125">Merged into the installer database.</span></span> <span data-ttu-id="f92eb-126">Listet andere für dieses Mergemodul erforderliche Mergemodule auf.</span><span class="sxs-lookup"><span data-stu-id="f92eb-126">Lists other merge modules required by this merge module.</span></span>                |
| [<span data-ttu-id="f92eb-127">Moduleausschluss</span><span class="sxs-lookup"><span data-stu-id="f92eb-127">ModuleExclusion</span></span>](moduleexclusion-table.md)   | <span data-ttu-id="f92eb-128">In der Installer-Datenbank zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="f92eb-128">Merged into the installer database.</span></span> <span data-ttu-id="f92eb-129">Listet andere Mergemodule auf, die mit diesem Mergemodul nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="f92eb-129">Lists other merge modules that are incompatible with this merge module.</span></span> |



 

<span data-ttu-id="f92eb-130">Die folgenden modulesequence-Tabellen treten nur in Mergemodulen auf.</span><span class="sxs-lookup"><span data-stu-id="f92eb-130">The following ModuleSequence tables only occur in merge modules.</span></span>



| <span data-ttu-id="f92eb-131">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="f92eb-131">Table name</span></span>                                                             | <span data-ttu-id="f92eb-132">Kommentar</span><span class="sxs-lookup"><span data-stu-id="f92eb-132">Comment</span></span>                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f92eb-133">Moduleadminuisequence</span><span class="sxs-lookup"><span data-stu-id="f92eb-133">ModuleAdminUISequence</span></span>](moduleadminuisequence-table.md)               | <span data-ttu-id="f92eb-134">Führt Aktionen in der [Tabelle AdminUISequence](adminuisequence-table.md)zusammen.</span><span class="sxs-lookup"><span data-stu-id="f92eb-134">Merges actions into the [AdminUISequence table](adminuisequence-table.md).</span></span>               |
| [<span data-ttu-id="f92eb-135">Moduleadminexecutesequence</span><span class="sxs-lookup"><span data-stu-id="f92eb-135">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)     | <span data-ttu-id="f92eb-136">Führt Aktionen in der [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)zusammen.</span><span class="sxs-lookup"><span data-stu-id="f92eb-136">Merges actions into the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>     |
| [<span data-ttu-id="f92eb-137">Moduleadvtuisequence</span><span class="sxs-lookup"><span data-stu-id="f92eb-137">ModuleAdvtUISequence</span></span>](moduleadvtuisequence-table.md)                 | <span data-ttu-id="f92eb-138">Verwenden Sie diese Tabelle nicht.</span><span class="sxs-lookup"><span data-stu-id="f92eb-138">Do not use this table.</span></span> <span data-ttu-id="f92eb-139">Weitere Informationen finden Sie unter [advtuisequence Table](advtuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f92eb-139">For details, see [AdvtUISequence table](advtuisequence-table.md).</span></span> |
| [<span data-ttu-id="f92eb-140">Moduleadvtexecutesequence</span><span class="sxs-lookup"><span data-stu-id="f92eb-140">ModuleAdvtExecuteSequence</span></span>](moduleadvtexecutesequence-table.md)       | <span data-ttu-id="f92eb-141">Führt Aktionen in der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)zusammen.</span><span class="sxs-lookup"><span data-stu-id="f92eb-141">Merges actions into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>       |
| [<span data-ttu-id="f92eb-142">Moduleignoretable</span><span class="sxs-lookup"><span data-stu-id="f92eb-142">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)                       | <span data-ttu-id="f92eb-143">Listet die Tabellen im Modul auf, die nicht in der MSI-Datei zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f92eb-143">Lists tables in the module that are not merged into the .msi file.</span></span>                        |
| [<span data-ttu-id="f92eb-144">Moduleinstalluisequence</span><span class="sxs-lookup"><span data-stu-id="f92eb-144">ModuleInstallUISequence</span></span>](moduleinstalluisequence-table.md)           | <span data-ttu-id="f92eb-145">Führt Aktionen in der [Tabelle "InstallUISequence](installuisequence-table.md)" aus.</span><span class="sxs-lookup"><span data-stu-id="f92eb-145">Merges actions into the [InstallUISequence table](installuisequence-table.md).</span></span>           |
| [<span data-ttu-id="f92eb-146">Moduleinstallexecutesequence</span><span class="sxs-lookup"><span data-stu-id="f92eb-146">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md) | <span data-ttu-id="f92eb-147">Führt Aktionen in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)zusammen.</span><span class="sxs-lookup"><span data-stu-id="f92eb-147">Merges actions into the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> |



 

<span data-ttu-id="f92eb-148">Die folgenden Tabellen sind in jedem konfigurierbaren Mergemodul erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f92eb-148">The following tables are required in every configurable merge module.</span></span> <span data-ttu-id="f92eb-149">Zum Erstellen eines konfigurierbaren Mergemoduls ist Mergemod.dll 2,0 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f92eb-149">Mergemod.dll 2.0 or later is required to create configurable merge module.</span></span> <span data-ttu-id="f92eb-150">Weitere Informationen finden Sie unter [konfigurierbare Mergemodule](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="f92eb-150">For details, see [Configurable Merge Modules](configurable-merge-modules.md).</span></span>



| <span data-ttu-id="f92eb-151">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="f92eb-151">Table name</span></span>                                                 | <span data-ttu-id="f92eb-152">Kommentar</span><span class="sxs-lookup"><span data-stu-id="f92eb-152">Comment</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f92eb-153">ModuleSubstitution-Tabelle</span><span class="sxs-lookup"><span data-stu-id="f92eb-153">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)   | <span data-ttu-id="f92eb-154">Benötigten Diese Tabelle wird nicht in der Ziel Installations Datenbank zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="f92eb-154">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="f92eb-155">Gibt die konfigurierbaren Felder in der Zieldatenbank an und stellt eine Vorlage für die Konfiguration der einzelnen Felder bereit.</span><span class="sxs-lookup"><span data-stu-id="f92eb-155">Specifies the configurable fields in the target database and provides a template for the configuration of each field.</span></span> |
| [<span data-ttu-id="f92eb-156">ModuleConfiguration-Tabelle</span><span class="sxs-lookup"><span data-stu-id="f92eb-156">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md) | <span data-ttu-id="f92eb-157">Benötigten Diese Tabelle wird nicht in der Ziel Installations Datenbank zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="f92eb-157">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="f92eb-158">Identifiziert die konfigurierbaren Attribute des Moduls.</span><span class="sxs-lookup"><span data-stu-id="f92eb-158">Identifies the configurable attributes of the module.</span></span>                                                                 |



 

<span data-ttu-id="f92eb-159">Die folgenden Installer-Tabellen können nicht in einem standardmäßigen Mergemodul auftreten.</span><span class="sxs-lookup"><span data-stu-id="f92eb-159">The following installer tables cannot occur in a standard merge module.</span></span>

-   [<span data-ttu-id="f92eb-160">Bbcontrol</span><span class="sxs-lookup"><span data-stu-id="f92eb-160">BBControl</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="f92eb-161">Billboard</span><span class="sxs-lookup"><span data-stu-id="f92eb-161">Billboard</span></span>](billboard-table.md)
-   [<span data-ttu-id="f92eb-162">Ccpsearch</span><span class="sxs-lookup"><span data-stu-id="f92eb-162">CCPSearch</span></span>](ccpsearch-table.md)
-   [<span data-ttu-id="f92eb-163">Fehler</span><span class="sxs-lookup"><span data-stu-id="f92eb-163">Error</span></span>](error-table.md)
-   [<span data-ttu-id="f92eb-164">Feature</span><span class="sxs-lookup"><span data-stu-id="f92eb-164">Feature</span></span>](feature-table.md)
-   [<span data-ttu-id="f92eb-165">LaunchCondition-Tabelle</span><span class="sxs-lookup"><span data-stu-id="f92eb-165">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="f92eb-166">Medien</span><span class="sxs-lookup"><span data-stu-id="f92eb-166">Media</span></span>](media-table.md)
-   [<span data-ttu-id="f92eb-167">Patch</span><span class="sxs-lookup"><span data-stu-id="f92eb-167">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="f92eb-168">Upgrade</span><span class="sxs-lookup"><span data-stu-id="f92eb-168">Upgrade</span></span>](upgrade-table.md)

<span data-ttu-id="f92eb-169">Die folgenden Installer-Tabellen sind optional in Mergemodulen.</span><span class="sxs-lookup"><span data-stu-id="f92eb-169">The following installer tables are optional in merge modules.</span></span>

-   [<span data-ttu-id="f92eb-170">Action Text</span><span class="sxs-lookup"><span data-stu-id="f92eb-170">ActionText</span></span>](actiontext-table.md)
-   [<span data-ttu-id="f92eb-171">"AdminExecuteSequence"</span><span class="sxs-lookup"><span data-stu-id="f92eb-171">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="f92eb-172">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="f92eb-172">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="f92eb-173">AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f92eb-173">AdvtExecuteSequence</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="f92eb-174">Advtuisequence</span><span class="sxs-lookup"><span data-stu-id="f92eb-174">AdvtUISequence</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="f92eb-175">AppId</span><span class="sxs-lookup"><span data-stu-id="f92eb-175">AppId</span></span>](appid-table.md)
-   [<span data-ttu-id="f92eb-176">AppSearch</span><span class="sxs-lookup"><span data-stu-id="f92eb-176">AppSearch</span></span>](appsearch-table.md)
-   [<span data-ttu-id="f92eb-177">BindImage</span><span class="sxs-lookup"><span data-stu-id="f92eb-177">BindImage</span></span>](bindimage-table.md)
-   [<span data-ttu-id="f92eb-178">CheckBox</span><span class="sxs-lookup"><span data-stu-id="f92eb-178">CheckBox</span></span>](checkbox-table.md)
-   [<span data-ttu-id="f92eb-179">Klasse</span><span class="sxs-lookup"><span data-stu-id="f92eb-179">Class</span></span>](class-table.md)
-   [<span data-ttu-id="f92eb-180">ComboBox</span><span class="sxs-lookup"><span data-stu-id="f92eb-180">ComboBox</span></span>](combobox-table.md)
-   [<span data-ttu-id="f92eb-181">Complocator</span><span class="sxs-lookup"><span data-stu-id="f92eb-181">CompLocator</span></span>](complocator-table.md)
-   [<span data-ttu-id="f92eb-182">Steuerung</span><span class="sxs-lookup"><span data-stu-id="f92eb-182">Control</span></span>](control-table.md)
-   [<span data-ttu-id="f92eb-183">ControlCondition</span><span class="sxs-lookup"><span data-stu-id="f92eb-183">ControlCondition</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="f92eb-184">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="f92eb-184">CreateFolder</span></span>](createfolder-table.md)
-   [<span data-ttu-id="f92eb-185">CustomAction</span><span class="sxs-lookup"><span data-stu-id="f92eb-185">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="f92eb-186">Dialogfeld</span><span class="sxs-lookup"><span data-stu-id="f92eb-186">Dialog</span></span>](dialog-table.md)
-   [<span data-ttu-id="f92eb-187">Drlocator</span><span class="sxs-lookup"><span data-stu-id="f92eb-187">DrLocator</span></span>](drlocator-table.md)
-   [<span data-ttu-id="f92eb-188">Duplicatefile</span><span class="sxs-lookup"><span data-stu-id="f92eb-188">DuplicateFile</span></span>](duplicatefile-table.md)
-   [<span data-ttu-id="f92eb-189">Umgebung</span><span class="sxs-lookup"><span data-stu-id="f92eb-189">Environment</span></span>](environment-table.md)
-   [<span data-ttu-id="f92eb-190">Tabelle EventMapping</span><span class="sxs-lookup"><span data-stu-id="f92eb-190">EventMapping</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="f92eb-191">Erweiterung</span><span class="sxs-lookup"><span data-stu-id="f92eb-191">Extension</span></span>](extension-table.md)
-   [<span data-ttu-id="f92eb-192">Schriftart</span><span class="sxs-lookup"><span data-stu-id="f92eb-192">Font</span></span>](font-table.md)
-   [<span data-ttu-id="f92eb-193">Symbol:</span><span class="sxs-lookup"><span data-stu-id="f92eb-193">Icon</span></span>](icon-table.md)
-   [<span data-ttu-id="f92eb-194">INIFILE</span><span class="sxs-lookup"><span data-stu-id="f92eb-194">IniFile</span></span>](inifile-table.md)
-   [<span data-ttu-id="f92eb-195">Inilocator</span><span class="sxs-lookup"><span data-stu-id="f92eb-195">IniLocator</span></span>](inilocator-table.md)
-   [<span data-ttu-id="f92eb-196">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f92eb-196">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="f92eb-197">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="f92eb-197">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="f92eb-198">ListBox</span><span class="sxs-lookup"><span data-stu-id="f92eb-198">ListBox</span></span>](listbox-table.md)
-   [<span data-ttu-id="f92eb-199">ListView</span><span class="sxs-lookup"><span data-stu-id="f92eb-199">ListView</span></span>](listview-table.md)
-   [<span data-ttu-id="f92eb-200">Medi</span><span class="sxs-lookup"><span data-stu-id="f92eb-200">MIME</span></span>](mime-table.md)
-   [<span data-ttu-id="f92eb-201">MoveFile</span><span class="sxs-lookup"><span data-stu-id="f92eb-201">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="f92eb-202">Odbcatcher Tribute</span><span class="sxs-lookup"><span data-stu-id="f92eb-202">ODBCAttribute</span></span>](odbcattribute-table.md)
-   [<span data-ttu-id="f92eb-203">ODBCDatasource</span><span class="sxs-lookup"><span data-stu-id="f92eb-203">ODBCDataSource</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="f92eb-204">Odbcdriver</span><span class="sxs-lookup"><span data-stu-id="f92eb-204">ODBCDriver</span></span>](odbcdriver-table.md)
-   [<span data-ttu-id="f92eb-205">Odbcsourceattribute</span><span class="sxs-lookup"><span data-stu-id="f92eb-205">ODBCSourceAttribute</span></span>](odbcsourceattribute-table.md)
-   [<span data-ttu-id="f92eb-206">Odbctranslator</span><span class="sxs-lookup"><span data-stu-id="f92eb-206">ODBCTranslator</span></span>](odbctranslator-table.md)
-   [<span data-ttu-id="f92eb-207">ProgID-Tabelle</span><span class="sxs-lookup"><span data-stu-id="f92eb-207">ProgID Table</span></span>](progid-table.md)
-   [<span data-ttu-id="f92eb-208">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f92eb-208">Property</span></span>](property-table.md)
-   [<span data-ttu-id="f92eb-209">PublishComponent</span><span class="sxs-lookup"><span data-stu-id="f92eb-209">PublishComponent</span></span>](publishcomponent-table.md)
-   [<span data-ttu-id="f92eb-210">RadioButton</span><span class="sxs-lookup"><span data-stu-id="f92eb-210">RadioButton</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="f92eb-211">Registrierungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="f92eb-211">Registry Table</span></span>](registry-table.md)
-   [<span data-ttu-id="f92eb-212">Reglocator</span><span class="sxs-lookup"><span data-stu-id="f92eb-212">RegLocator</span></span>](reglocator-table.md)
-   [<span data-ttu-id="f92eb-213">RemoveFile aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f92eb-213">RemoveFile</span></span>](removefile-table.md)
-   [<span data-ttu-id="f92eb-214">Removeinifile</span><span class="sxs-lookup"><span data-stu-id="f92eb-214">RemoveIniFile</span></span>](removeinifile-table.md)
-   [<span data-ttu-id="f92eb-215">Removeregistry</span><span class="sxs-lookup"><span data-stu-id="f92eb-215">RemoveRegistry</span></span>](removeregistry-table.md)
-   [<span data-ttu-id="f92eb-216">ReserveCost</span><span class="sxs-lookup"><span data-stu-id="f92eb-216">ReserveCost</span></span>](reservecost-table.md)
-   [<span data-ttu-id="f92eb-217">Selfreg</span><span class="sxs-lookup"><span data-stu-id="f92eb-217">SelfReg</span></span>](selfreg-table.md)
-   [<span data-ttu-id="f92eb-218">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="f92eb-218">ServiceControl</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="f92eb-219">Serviceingestall</span><span class="sxs-lookup"><span data-stu-id="f92eb-219">ServiceInstall</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="f92eb-220">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="f92eb-220">Shortcut</span></span>](shortcut-table.md)
-   [<span data-ttu-id="f92eb-221">Signature</span><span class="sxs-lookup"><span data-stu-id="f92eb-221">Signature</span></span>](signature-table.md)
-   [<span data-ttu-id="f92eb-222">Textart</span><span class="sxs-lookup"><span data-stu-id="f92eb-222">TextStyle</span></span>](textstyle-table.md)
-   [<span data-ttu-id="f92eb-223">Export der Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f92eb-223">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="f92eb-224">UIText</span><span class="sxs-lookup"><span data-stu-id="f92eb-224">UIText</span></span>](uitext-table.md)
-   [<span data-ttu-id="f92eb-225">Verb</span><span class="sxs-lookup"><span data-stu-id="f92eb-225">Verb</span></span>](verb-table.md)

 

 



