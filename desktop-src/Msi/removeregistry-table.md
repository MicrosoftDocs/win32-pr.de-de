---
description: Die Tabelle "removeregistry" enthält die Registrierungsinformationen, die von der Anwendung aus der Systemregistrierung gelöscht werden müssen.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Removeregistry-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de39edd15484ac4bcda675ec8bffaca0540a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959984"
---
# <a name="removeregistry-table"></a><span data-ttu-id="b1565-103">Removeregistry-Tabelle</span><span class="sxs-lookup"><span data-stu-id="b1565-103">RemoveRegistry Table</span></span>

<span data-ttu-id="b1565-104">Die Tabelle "removeregistry" enthält die Registrierungsinformationen, die von der Anwendung aus der Systemregistrierung gelöscht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b1565-104">The RemoveRegistry table contains the registry information the application needs to delete from the system registry.</span></span>

<span data-ttu-id="b1565-105">Die removeregistry-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="b1565-105">The RemoveRegistry table has the following columns.</span></span>



| <span data-ttu-id="b1565-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="b1565-106">Column</span></span>         | <span data-ttu-id="b1565-107">Typ</span><span class="sxs-lookup"><span data-stu-id="b1565-107">Type</span></span>                         | <span data-ttu-id="b1565-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b1565-108">Key</span></span> | <span data-ttu-id="b1565-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="b1565-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="b1565-110">Removeregistry</span><span class="sxs-lookup"><span data-stu-id="b1565-110">RemoveRegistry</span></span> | [<span data-ttu-id="b1565-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b1565-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="b1565-112">J</span><span class="sxs-lookup"><span data-stu-id="b1565-112">Y</span></span>   | <span data-ttu-id="b1565-113">N</span><span class="sxs-lookup"><span data-stu-id="b1565-113">N</span></span>        |
| <span data-ttu-id="b1565-114">Root</span><span class="sxs-lookup"><span data-stu-id="b1565-114">Root</span></span>           | [<span data-ttu-id="b1565-115">Integer</span><span class="sxs-lookup"><span data-stu-id="b1565-115">Integer</span></span>](integer.md)       | <span data-ttu-id="b1565-116">N</span><span class="sxs-lookup"><span data-stu-id="b1565-116">N</span></span>   | <span data-ttu-id="b1565-117">N</span><span class="sxs-lookup"><span data-stu-id="b1565-117">N</span></span>        |
| <span data-ttu-id="b1565-118">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b1565-118">Key</span></span>            | [<span data-ttu-id="b1565-119">Regfad</span><span class="sxs-lookup"><span data-stu-id="b1565-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="b1565-120">N</span><span class="sxs-lookup"><span data-stu-id="b1565-120">N</span></span>   | <span data-ttu-id="b1565-121">N</span><span class="sxs-lookup"><span data-stu-id="b1565-121">N</span></span>        |
| <span data-ttu-id="b1565-122">Name</span><span class="sxs-lookup"><span data-stu-id="b1565-122">Name</span></span>           | [<span data-ttu-id="b1565-123">Großformatige</span><span class="sxs-lookup"><span data-stu-id="b1565-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b1565-124">N</span><span class="sxs-lookup"><span data-stu-id="b1565-124">N</span></span>   | <span data-ttu-id="b1565-125">J</span><span class="sxs-lookup"><span data-stu-id="b1565-125">Y</span></span>        |
| <span data-ttu-id="b1565-126">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="b1565-126">Component\_</span></span>    | [<span data-ttu-id="b1565-127">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b1565-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="b1565-128">N</span><span class="sxs-lookup"><span data-stu-id="b1565-128">N</span></span>   | <span data-ttu-id="b1565-129">N</span><span class="sxs-lookup"><span data-stu-id="b1565-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b1565-130">Spalten</span><span class="sxs-lookup"><span data-stu-id="b1565-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b1565-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>Removeregistry</span><span class="sxs-lookup"><span data-stu-id="b1565-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span></span>
</dt> <dd>

<span data-ttu-id="b1565-132">Der Schlüssel für diese Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b1565-132">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="b1565-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Fasst</span><span class="sxs-lookup"><span data-stu-id="b1565-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="b1565-134">Der vordefinierte Stamm Schlüssel für den Registrierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="b1565-134">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="b1565-135">Konstante</span><span class="sxs-lookup"><span data-stu-id="b1565-135">Constant</span></span>                          | <span data-ttu-id="b1565-136">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="b1565-136">Hexadecimal</span></span> | <span data-ttu-id="b1565-137">Decimal</span><span class="sxs-lookup"><span data-stu-id="b1565-137">Decimal</span></span> | <span data-ttu-id="b1565-138">Stamm Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b1565-138">Root key</span></span>                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1565-139">(none)</span><span class="sxs-lookup"><span data-stu-id="b1565-139">(none)</span></span>                            | <span data-ttu-id="b1565-140">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="b1565-140">\- 0x001</span></span>    | <span data-ttu-id="b1565-141">-1</span><span class="sxs-lookup"><span data-stu-id="b1565-141">-1</span></span>      | <span data-ttu-id="b1565-142">**HKEY \_ Das \_** Installationsprogramm des aktuellen Benutzers legt diesen Schlüssel fest, während eine Installation pro Benutzer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1565-142">**HKEY\_CURRENT\_USER** Installer sets this key while doing a per-user installation.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="b1565-143">(none)</span><span class="sxs-lookup"><span data-stu-id="b1565-143">(none)</span></span>                            | <span data-ttu-id="b1565-144">-0x001</span><span class="sxs-lookup"><span data-stu-id="b1565-144">-0x001</span></span>      | <span data-ttu-id="b1565-145">-1</span><span class="sxs-lookup"><span data-stu-id="b1565-145">-1</span></span>      | <span data-ttu-id="b1565-146">**HKEY \_ Das Installationsprogramm für den lokalen \_ Computer** legt diesen Schlüssel fest, während eine Installation aller Benutzer mit [**ALLUSERS**](allusers.md) auf 1 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b1565-146">**HKEY\_LOCAL\_MACHINE** Installer sets this key while doing an all-users installation with [**ALLUSERS**](allusers.md) set to 1.</span></span><br/>                                                                       |
| <span data-ttu-id="b1565-147">**msidbregistryrootclassesroot**</span><span class="sxs-lookup"><span data-stu-id="b1565-147">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="b1565-148">0x000</span><span class="sxs-lookup"><span data-stu-id="b1565-148">0x000</span></span>       | <span data-ttu-id="b1565-149">0</span><span class="sxs-lookup"><span data-stu-id="b1565-149">0</span></span>       | <span data-ttu-id="b1565-150">**HKEY \_ Klassen \_** Stamm: das Installationsprogramm entfernt den Wert aus den **HKCU- \\ Software \\ Klassen** Hive während der Installationen im Einzelbenutzer-und computerspezifischen [Installations Kontext](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="b1565-150">**HKEY\_CLASSES\_ROOT** The installer removes the value from the **HKCU\\Software\\Classes** hive during installations in the per-user and per-machine [installation context](installation-context.md).</span></span><br/> |
| <span data-ttu-id="b1565-151">**msidbregistryrootcurrentuser**</span><span class="sxs-lookup"><span data-stu-id="b1565-151">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="b1565-152">0x001</span><span class="sxs-lookup"><span data-stu-id="b1565-152">0x001</span></span>       | <span data-ttu-id="b1565-153">1</span><span class="sxs-lookup"><span data-stu-id="b1565-153">1</span></span>       | <span data-ttu-id="b1565-154">**Aktueller HKEY- \_ \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b1565-154">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="b1565-155">**msidbregistryrootlocalmachine**</span><span class="sxs-lookup"><span data-stu-id="b1565-155">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="b1565-156">0x002</span><span class="sxs-lookup"><span data-stu-id="b1565-156">0x002</span></span>       | <span data-ttu-id="b1565-157">2</span><span class="sxs-lookup"><span data-stu-id="b1565-157">2</span></span>       | <span data-ttu-id="b1565-158">**lokaler HKEY- \_ \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="b1565-158">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="b1565-159">**msidbregistryrootusers**</span><span class="sxs-lookup"><span data-stu-id="b1565-159">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="b1565-160">0x003</span><span class="sxs-lookup"><span data-stu-id="b1565-160">0x003</span></span>       | <span data-ttu-id="b1565-161">3</span><span class="sxs-lookup"><span data-stu-id="b1565-161">3</span></span>       | <span data-ttu-id="b1565-162">**HKEY- \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b1565-162">**HKEY\_USERS**</span></span>                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="b1565-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen</span><span class="sxs-lookup"><span data-stu-id="b1565-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="b1565-164">Der lokalisierbare Schlüssel für den Registrierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="b1565-164">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="b1565-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="b1565-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="b1565-166">Der lokalisierbare Name des Registrierungs Werts.</span><span class="sxs-lookup"><span data-stu-id="b1565-166">The localizable registry value name.</span></span>

<span data-ttu-id="b1565-167">Die folgende Zeichenfolge in der Spalte Name hat eine besondere Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="b1565-167">The following string in the Name column has special significance.</span></span>



| <span data-ttu-id="b1565-168">String</span><span class="sxs-lookup"><span data-stu-id="b1565-168">String</span></span> | <span data-ttu-id="b1565-169">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b1565-169">Meaning</span></span>                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1565-170">"-"</span><span class="sxs-lookup"><span data-stu-id="b1565-170">"-"</span></span>    | <span data-ttu-id="b1565-171">Wenn die Komponente installiert ist, muss der Schlüssel ggf. mit allen zugehörigen Werten und unter Schlüsseln gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b1565-171">The key is to be deleted, if present, with all of its values and subkeys, when the component is installed.</span></span> |



 

<span data-ttu-id="b1565-172">Beachten Sie, dass die [Registrierungs Tabelle](registry-table.md) zum Erstellen oder Entfernen eines Registrierungsschlüssels verwendet werden soll, wenn die Komponente entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b1565-172">Note that the [Registry table](registry-table.md) should be used to create or remove a registry key when the component is removed.</span></span>

</dd> <dt>

<span data-ttu-id="b1565-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="b1565-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="b1565-174">Externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md) , die auf die Komponente verweist, die das Löschen des Registrierungs Werts steuert.</span><span class="sxs-lookup"><span data-stu-id="b1565-174">External key into the first column of the [Component table](component-table.md) referencing the component that controls the deletion of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1565-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1565-175">Remarks</span></span>

<span data-ttu-id="b1565-176">Die Registrierungsinformationen werden aus der Systemregistrierung gelöscht, wenn die entsprechende Komponente für die lokale Installation ausgewählt oder von der Quelle aus ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="b1565-176">The registry information is deleted from the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="b1565-177">Diese Tabelle wird beim Ausführen der [removeregistryvalues-Aktion](removeregistryvalues-action.md) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b1565-177">This table is referred to when the [RemoveRegistryValues action](removeregistryvalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="b1565-178">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="b1565-178">Validation</span></span>

<dl>

[<span data-ttu-id="b1565-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="b1565-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b1565-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="b1565-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b1565-181">ICE32</span><span class="sxs-lookup"><span data-stu-id="b1565-181">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b1565-182">ICE46</span><span class="sxs-lookup"><span data-stu-id="b1565-182">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="b1565-183">ICE69</span><span class="sxs-lookup"><span data-stu-id="b1565-183">ICE69</span></span>](ice69.md)  
</dl>

 

 




