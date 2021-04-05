---
description: Die Tabelle CustomAction bietet die Möglichkeit, benutzerdefinierten Code und Daten in die Installation zu integrieren. Die Quelle des ausgeführten Codes kann ein in der Datenbank enthaltener Stream, eine zuletzt installierte Datei oder eine vorhandene ausführbare Datei sein.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Tabelle "CustomAction"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752321"
---
# <a name="customaction-table"></a><span data-ttu-id="6aa1d-104">Tabelle "CustomAction"</span><span class="sxs-lookup"><span data-stu-id="6aa1d-104">CustomAction Table</span></span>

<span data-ttu-id="6aa1d-105">Die Tabelle CustomAction bietet die Möglichkeit, benutzerdefinierten Code und Daten in die Installation zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-105">The CustomAction table provides the means of integrating custom code and data into the installation.</span></span> <span data-ttu-id="6aa1d-106">Die Quelle des ausgeführten Codes kann ein in der Datenbank enthaltener Stream, eine zuletzt installierte Datei oder eine vorhandene ausführbare Datei sein.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-106">The source of the code that is executed can be a stream contained within the database, a recently installed file, or an existing executable file.</span></span>

<span data-ttu-id="6aa1d-107">Die CustomAction-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-107">The CustomAction table has the following columns.</span></span>



| <span data-ttu-id="6aa1d-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="6aa1d-108">Column</span></span>       | <span data-ttu-id="6aa1d-109">Typ</span><span class="sxs-lookup"><span data-stu-id="6aa1d-109">Type</span></span>                               | <span data-ttu-id="6aa1d-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="6aa1d-110">Key</span></span> | <span data-ttu-id="6aa1d-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="6aa1d-111">Nullable</span></span> |
|--------------|------------------------------------|-----|----------|
| <span data-ttu-id="6aa1d-112">Aktion</span><span class="sxs-lookup"><span data-stu-id="6aa1d-112">Action</span></span>       | [<span data-ttu-id="6aa1d-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="6aa1d-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="6aa1d-114">J</span><span class="sxs-lookup"><span data-stu-id="6aa1d-114">Y</span></span>   | <span data-ttu-id="6aa1d-115">N</span><span class="sxs-lookup"><span data-stu-id="6aa1d-115">N</span></span>        |
| <span data-ttu-id="6aa1d-116">type</span><span class="sxs-lookup"><span data-stu-id="6aa1d-116">Type</span></span>         | [<span data-ttu-id="6aa1d-117">Integer</span><span class="sxs-lookup"><span data-stu-id="6aa1d-117">Integer</span></span>](integer.md)             | <span data-ttu-id="6aa1d-118">N</span><span class="sxs-lookup"><span data-stu-id="6aa1d-118">N</span></span>   | <span data-ttu-id="6aa1d-119">N</span><span class="sxs-lookup"><span data-stu-id="6aa1d-119">N</span></span>        |
| <span data-ttu-id="6aa1d-120">`Source`</span><span class="sxs-lookup"><span data-stu-id="6aa1d-120">Source</span></span>       | [<span data-ttu-id="6aa1d-121">CustomSource</span><span class="sxs-lookup"><span data-stu-id="6aa1d-121">CustomSource</span></span>](customsource.md)   | <span data-ttu-id="6aa1d-122">N</span><span class="sxs-lookup"><span data-stu-id="6aa1d-122">N</span></span>   | <span data-ttu-id="6aa1d-123">J</span><span class="sxs-lookup"><span data-stu-id="6aa1d-123">Y</span></span>        |
| <span data-ttu-id="6aa1d-124">Ziel</span><span class="sxs-lookup"><span data-stu-id="6aa1d-124">Target</span></span>       | [<span data-ttu-id="6aa1d-125">Großformatige</span><span class="sxs-lookup"><span data-stu-id="6aa1d-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="6aa1d-126">N</span><span class="sxs-lookup"><span data-stu-id="6aa1d-126">N</span></span>   | <span data-ttu-id="6aa1d-127">J</span><span class="sxs-lookup"><span data-stu-id="6aa1d-127">Y</span></span>        |
| <span data-ttu-id="6aa1d-128">ExtendedType</span><span class="sxs-lookup"><span data-stu-id="6aa1d-128">ExtendedType</span></span> | [<span data-ttu-id="6aa1d-129">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="6aa1d-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="6aa1d-130">N</span><span class="sxs-lookup"><span data-stu-id="6aa1d-130">N</span></span>   | <span data-ttu-id="6aa1d-131">J</span><span class="sxs-lookup"><span data-stu-id="6aa1d-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6aa1d-132">Spalten</span><span class="sxs-lookup"><span data-stu-id="6aa1d-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6aa1d-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="6aa1d-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="6aa1d-134">Name der Aktion.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-134">Name of the action.</span></span> <span data-ttu-id="6aa1d-135">Die Aktion wird normalerweise in einer Sequenz Tabelle angezeigt, sofern Sie nicht von einer anderen benutzerdefinierten Aktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-135">The action normally appears in a sequence table unless it is called by another custom action.</span></span> <span data-ttu-id="6aa1d-136">Wenn der Name mit einer integrierten Aktion übereinstimmt, wird die benutzerdefinierte Aktion nie aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-136">If the name matches any built-in action, then the custom action is never called.</span></span>

<span data-ttu-id="6aa1d-137">Primärer Tabellenschlüssel.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-137">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="6aa1d-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte</span><span class="sxs-lookup"><span data-stu-id="6aa1d-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="6aa1d-139">Ein Feld mit Flagbits, das den Basistyp der benutzerdefinierten Aktion und Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-139">A field of flag bits specifying the basic type of custom action and options.</span></span> <span data-ttu-id="6aa1d-140">Eine Liste der grundlegenden Typen finden Sie [in der Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md) .</span><span class="sxs-lookup"><span data-stu-id="6aa1d-140">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a list of the basic types.</span></span> <span data-ttu-id="6aa1d-141">Weitere Informationen finden Sie unter [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md), Optionen für die [Ausführung von benutzerdefinierten](custom-action-execution-scheduling-options.md)Aktionen, ausgeblendete [Ziel](custom-action-hidden-target-option.md)Optionen und [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md)</span><span class="sxs-lookup"><span data-stu-id="6aa1d-141">See [Custom Action Return Processing Options](custom-action-return-processing-options.md), [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md), [Custom Action Hidden Target Option](custom-action-hidden-target-option.md), and [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aa1d-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Ausgangs</span><span class="sxs-lookup"><span data-stu-id="6aa1d-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="6aa1d-143">Ein Eigenschaftsname oder ein externer Schlüssel in einer anderen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-143">A property name or external key into another table.</span></span> <span data-ttu-id="6aa1d-144">Eine Erläuterung der möglichen benutzerdefinierten Aktions Quellen finden Sie unter [benutzerdefinierte Aktions Quellen](custom-action-sources.md) und [in der Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md).</span><span class="sxs-lookup"><span data-stu-id="6aa1d-144">For a discussion of the possible custom action sources, see [Custom Action Sources](custom-action-sources.md) and the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span> <span data-ttu-id="6aa1d-145">Die Quell Spalte kann z. b. einen externen Schlüssel in die erste Spalte einer der folgenden Tabellen enthalten, die die Quelle des benutzerdefinierten Aktionscodes enthält.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-145">For example, the Source column may contain an external key into the first column of one of the following tables containing the source of the custom action code.</span></span>

<span data-ttu-id="6aa1d-146">[Verzeichnis Tabelle](directory-table.md) zum Aufrufen vorhandener ausführbarer Dateien.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-146">[Directory table](directory-table.md) for calling existing executables.</span></span>

<span data-ttu-id="6aa1d-147">[Dateitabelle](file-table.md) zum Aufrufen von ausführbaren Dateien und DLLs, die soeben installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-147">[File table](file-table.md) for calling executables and DLLs that have just been installed.</span></span>

<span data-ttu-id="6aa1d-148">[Binäre Tabelle](binary-table.md) zum Aufrufen von ausführbaren Dateien, DLLs und Daten, die in der Datenbank gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-148">[Binary table](binary-table.md) for calling executables, DLLs, and data stored in the database.</span></span>

<span data-ttu-id="6aa1d-149">[Eigenschaften Tabelle](property-table.md) zum Aufrufen von ausführbaren Dateien, deren Pfade von einer Eigenschaft aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-149">[Property table](property-table.md) for calling executables whose paths are held by a property.</span></span>

</dd> <dt>

<span data-ttu-id="6aa1d-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Spar</span><span class="sxs-lookup"><span data-stu-id="6aa1d-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="6aa1d-151">Ein Ausführungs Parameter, der vom Basistyp der benutzerdefinierten Aktion abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-151">An execution parameter that depends on the basic type of custom action.</span></span> <span data-ttu-id="6aa1d-152">In der [Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md) finden Sie eine Beschreibung der Informationen, die in diesem Feld für die einzelnen Typen von benutzerdefinierten Aktionen eingegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-152">See the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a description of what should be entered in this field for each type of custom action.</span></span> <span data-ttu-id="6aa1d-153">Beispielsweise kann dieses Feld abhängig von der benutzerdefinierten Aktion Folgendes enthalten.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-153">For example, this field may contain the following depending on the custom action.</span></span>



| <span data-ttu-id="6aa1d-154">Ziel</span><span class="sxs-lookup"><span data-stu-id="6aa1d-154">Target</span></span>                                    | <span data-ttu-id="6aa1d-155">Benutzerdefinierte Aktion</span><span class="sxs-lookup"><span data-stu-id="6aa1d-155">Custom action</span></span>                         |
|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="6aa1d-156">Einstiegspunkt (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="6aa1d-156">Entry point (required)</span></span>                    | <span data-ttu-id="6aa1d-157">Aufrufen einer DLL.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-157">Calling a DLL.</span></span>                        |
| <span data-ttu-id="6aa1d-158">Name der ausführbaren Datei mit Argumenten (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="6aa1d-158">Executable name with arguments (required)</span></span> | <span data-ttu-id="6aa1d-159">Aufrufen einer vorhandenen ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-159">Calling an existing executable.</span></span>       |
| <span data-ttu-id="6aa1d-160">Befehlszeilenargumente (optional)</span><span class="sxs-lookup"><span data-stu-id="6aa1d-160">Command line arguments (optional)</span></span>         | <span data-ttu-id="6aa1d-161">Aufrufen einer soeben installierten ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-161">Calling an executable just installed.</span></span> |
| <span data-ttu-id="6aa1d-162">Ziel Dateiname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="6aa1d-162">Target file name (required)</span></span>               | <span data-ttu-id="6aa1d-163">Erstellen einer Datei aus benutzerdefinierten Daten.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-163">Creating a file from custom data.</span></span>     |
| <span data-ttu-id="6aa1d-164">Null</span><span class="sxs-lookup"><span data-stu-id="6aa1d-164">Null</span></span>                                      | <span data-ttu-id="6aa1d-165">Ausführen von Skriptcode.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-165">Executing script code.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="6aa1d-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span><span class="sxs-lookup"><span data-stu-id="6aa1d-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span></span>
</dt> <dd>

<span data-ttu-id="6aa1d-167">Geben Sie in diesem Feld den **msidbcustomaction typepatchuninstall** -Wert ein, um eine benutzerdefinierte Aktion mit der [Option zum Deinstallieren von benutzerdefinierten Aktionen](custom-action-patch-uninstall-option.md)anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-167">Enter the **msidbCustomActionTypePatchUninstall** value in this field to specify a custom action with the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md).</span></span>

<span data-ttu-id="6aa1d-168">**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-168">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="6aa1d-169">Diese Option ist ab Windows Installer 4,5 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-169">This option is available beginning with Windows Installer 4.5.</span></span>

</dd> </dl>

<span data-ttu-id="6aa1d-170">Weitere Informationen finden Sie in den Themen unter [benutzerdefinierte Aktionen](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6aa1d-170">For more information, see all the topics under [Custom Actions](custom-actions.md).</span></span>

## <a name="validation"></a><span data-ttu-id="6aa1d-171">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="6aa1d-171">Validation</span></span>

<dl>

[<span data-ttu-id="6aa1d-172">ICE03</span><span class="sxs-lookup"><span data-stu-id="6aa1d-172">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6aa1d-173">ICE06</span><span class="sxs-lookup"><span data-stu-id="6aa1d-173">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6aa1d-174">ICE12</span><span class="sxs-lookup"><span data-stu-id="6aa1d-174">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="6aa1d-175">ICE27</span><span class="sxs-lookup"><span data-stu-id="6aa1d-175">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="6aa1d-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="6aa1d-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="6aa1d-177">ICE63</span><span class="sxs-lookup"><span data-stu-id="6aa1d-177">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="6aa1d-178">ICE68</span><span class="sxs-lookup"><span data-stu-id="6aa1d-178">ICE68</span></span>](ice68.md)  
[<span data-ttu-id="6aa1d-179">ICE72</span><span class="sxs-lookup"><span data-stu-id="6aa1d-179">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="6aa1d-180">ICE75</span><span class="sxs-lookup"><span data-stu-id="6aa1d-180">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="6aa1d-181">ICE77</span><span class="sxs-lookup"><span data-stu-id="6aa1d-181">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="6aa1d-182">ICE80</span><span class="sxs-lookup"><span data-stu-id="6aa1d-182">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="6aa1d-183">ICE88</span><span class="sxs-lookup"><span data-stu-id="6aa1d-183">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="6aa1d-184">ICE93</span><span class="sxs-lookup"><span data-stu-id="6aa1d-184">ICE93</span></span>](ice93.md)  
</dl>

 

 



