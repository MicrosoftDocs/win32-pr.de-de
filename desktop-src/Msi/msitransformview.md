---
description: Diese temporäre Tabelle aktiviert die Option zum Deinstallieren von benutzerdefinierten Aktionen für benutzerdefinierte Aktionen, die von einem Patch hinzugefügt oder aktualisiert werden.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: Msitransformview
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb50c397c10ede3a21b40600952d50e55a5ba1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363302"
---
# <a name="msitransformview"></a><span data-ttu-id="d3f56-103">Msitransformview</span><span class="sxs-lookup"><span data-stu-id="d3f56-103">MsiTransformView</span></span>

<span data-ttu-id="d3f56-104">Diese temporäre Tabelle aktiviert die [Option zum Deinstallieren von benutzerdefinierten](custom-action-patch-uninstall-option.md) Aktionen für benutzerdefinierte Aktionen, die von einem Patch hinzugefügt oder aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d3f56-104">This temporary table enables the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) for custom actions added or updated by a patch.</span></span>

<span data-ttu-id="d3f56-105">Wenn ein Patch eine benutzerdefinierte Aktion hinzufügt oder aktualisiert, die über das **msidbcustomaction typepatchuninstall** -Attribut verfügt, führt Windows Installer die neue oder aktualisierte benutzerdefinierte Aktion aus, wenn der Patch deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="d3f56-105">If a patch adds or updates a custom action having the **msidbCustomActionTypePatchUninstall** attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="d3f56-106">Durch Windows Installer werden die Updates, die im Patch deinstalliert werden, für die benutzerdefinierte Aktion zum Deinstallieren von Patches verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d3f56-106">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="d3f56-107">Der Patch muss eine msitransformview- *<PatchGUID>* Tabelle enthalten, um diese Informationen für Windows Installer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d3f56-107">The patch must include a MsiTransformView *<PatchGUID>* table to provide this information to Windows Installer.</span></span> <span data-ttu-id="d3f56-108">Die Informationen in dieser Tabelle sind für jede unmittelbare benutzerdefinierte Aktion verfügbar und für verzögerte benutzerdefinierte Aktionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d3f56-108">The information in this table is available to any immediate custom action, and is unavailable to deferred custom actions.</span></span>

<span data-ttu-id="d3f56-109">**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d3f56-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="d3f56-110">Die [Option zum Deinstallieren des benutzerdefinierten Aktions Patches](custom-action-patch-uninstall-option.md) ist ab Windows Installer 4,5 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d3f56-110">The [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="d3f56-111">Diese Tabelle sollte den Namen "msitransformview *<PatchGUID>* Table" haben, wobei *<PatchGUID>* die GUID ist, die den Patch eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d3f56-111">This table should be named MsiTransformView *<PatchGUID>* Table, where *<PatchGUID>* is the GUID that uniquely identifies the patch.</span></span> <span data-ttu-id="d3f56-112">Die msitransformview- *<PatchGUID>* Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="d3f56-112">The MsiTransformView *<PatchGUID>* Table has the following columns.</span></span>



| <span data-ttu-id="d3f56-113">Spalte</span><span class="sxs-lookup"><span data-stu-id="d3f56-113">Column</span></span>  | <span data-ttu-id="d3f56-114">Typ</span><span class="sxs-lookup"><span data-stu-id="d3f56-114">Type</span></span>                         | <span data-ttu-id="d3f56-115">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d3f56-115">Key</span></span> | <span data-ttu-id="d3f56-116">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d3f56-116">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="d3f56-117">Tabelle</span><span class="sxs-lookup"><span data-stu-id="d3f56-117">Table</span></span>   | [<span data-ttu-id="d3f56-118">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d3f56-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="d3f56-119">J</span><span class="sxs-lookup"><span data-stu-id="d3f56-119">Y</span></span>   | <span data-ttu-id="d3f56-120">N</span><span class="sxs-lookup"><span data-stu-id="d3f56-120">N</span></span>        |
| <span data-ttu-id="d3f56-121">Column</span><span class="sxs-lookup"><span data-stu-id="d3f56-121">Column</span></span>  | [<span data-ttu-id="d3f56-122">Text</span><span class="sxs-lookup"><span data-stu-id="d3f56-122">Text</span></span>](text.md)             | <span data-ttu-id="d3f56-123">J</span><span class="sxs-lookup"><span data-stu-id="d3f56-123">Y</span></span>   | <span data-ttu-id="d3f56-124">N</span><span class="sxs-lookup"><span data-stu-id="d3f56-124">N</span></span>        |
| <span data-ttu-id="d3f56-125">Zeile</span><span class="sxs-lookup"><span data-stu-id="d3f56-125">Row</span></span>     | [<span data-ttu-id="d3f56-126">Text</span><span class="sxs-lookup"><span data-stu-id="d3f56-126">Text</span></span>](text.md)             | <span data-ttu-id="d3f56-127">J</span><span class="sxs-lookup"><span data-stu-id="d3f56-127">Y</span></span>   | <span data-ttu-id="d3f56-128">J</span><span class="sxs-lookup"><span data-stu-id="d3f56-128">Y</span></span>        |
| <span data-ttu-id="d3f56-129">Daten</span><span class="sxs-lookup"><span data-stu-id="d3f56-129">Data</span></span>    | [<span data-ttu-id="d3f56-130">Text</span><span class="sxs-lookup"><span data-stu-id="d3f56-130">Text</span></span>](text.md)             | <span data-ttu-id="d3f56-131">N</span><span class="sxs-lookup"><span data-stu-id="d3f56-131">N</span></span>   | <span data-ttu-id="d3f56-132">J</span><span class="sxs-lookup"><span data-stu-id="d3f56-132">Y</span></span>        |
| <span data-ttu-id="d3f56-133">Aktuell</span><span class="sxs-lookup"><span data-stu-id="d3f56-133">Current</span></span> | [<span data-ttu-id="d3f56-134">Text</span><span class="sxs-lookup"><span data-stu-id="d3f56-134">Text</span></span>](text.md)             | <span data-ttu-id="d3f56-135">N</span><span class="sxs-lookup"><span data-stu-id="d3f56-135">N</span></span>   | <span data-ttu-id="d3f56-136">J</span><span class="sxs-lookup"><span data-stu-id="d3f56-136">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="d3f56-137">Column</span><span class="sxs-lookup"><span data-stu-id="d3f56-137">Column</span></span>

<dl> <dt>

<span data-ttu-id="d3f56-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub</span><span class="sxs-lookup"><span data-stu-id="d3f56-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="d3f56-139">Der Name einer geänderten Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="d3f56-139">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="d3f56-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Kolumne</span><span class="sxs-lookup"><span data-stu-id="d3f56-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="d3f56-141">Der Name einer geänderten Tabellenspalte oder INSERT, DELETE, CREATE oder Drop.</span><span class="sxs-lookup"><span data-stu-id="d3f56-141">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="d3f56-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Zeile</span><span class="sxs-lookup"><span data-stu-id="d3f56-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="d3f56-143">Eine Liste der Primärschlüssel Werte, die durch Registerkarten getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="d3f56-143">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="d3f56-144">NULL-Primärschlüssel Werte werden durch ein einzelnes Leerzeichen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d3f56-144">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="d3f56-145">Ein NULL-Wert in dieser Spalte gibt eine Schema Änderung an.</span><span class="sxs-lookup"><span data-stu-id="d3f56-145">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="d3f56-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats</span><span class="sxs-lookup"><span data-stu-id="d3f56-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="d3f56-147">Daten, Name eines Datenstroms oder Spaltendefinition.</span><span class="sxs-lookup"><span data-stu-id="d3f56-147">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="d3f56-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Strömung</span><span class="sxs-lookup"><span data-stu-id="d3f56-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="d3f56-149">Aktueller Wert aus Verweis Datenbank oder Spalte a-Nummer.</span><span class="sxs-lookup"><span data-stu-id="d3f56-149">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3f56-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3f56-150">Remarks</span></span>

<span data-ttu-id="d3f56-151">Patch deinstallieren benutzerdefinierte Aktionen werden ausgeführt, wenn der Patch deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="d3f56-151">Patch uninstall custom actions run when the patch is uninstalled.</span></span> <span data-ttu-id="d3f56-152">Sie werden nicht ausgeführt, wenn das Produkt deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="d3f56-152">They do not run when the product is uninstalled.</span></span> <span data-ttu-id="d3f56-153">Verwenden Sie die [Option zum Deinstallieren von benutzerdefinierten Aktionen](custom-action-patch-uninstall-option.md) , und verwenden Sie diese Tabelle, um nur einen benutzerdefinierten auszuführen, wenn der Patch deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="d3f56-153">Use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) and this table to run a custom only when the patch is being uninstalled.</span></span>

<span data-ttu-id="d3f56-154">Ein Patch kann eine benutzerdefinierte Aktion, die im ursprünglichen Paket (MSI-Datei) bereitgestellt wird, aktualisieren. Um die aktualisierte Version der benutzerdefinierten Aktion auszuführen, wenn der Patch deinstalliert wird, markieren Sie die benutzerdefinierte Aktion mit dem **msidbcustomaction typepatchuninstall** -Attribut im ursprünglichen Paket.</span><span class="sxs-lookup"><span data-stu-id="d3f56-154">A patch can update a custom action provided in the original package (.msi file.) To run the updated version of the custom action when the patch is uninstalled, mark the custom action with the **msidbCustomActionTypePatchUninstall** attribute in the original package.</span></span>

 

 



