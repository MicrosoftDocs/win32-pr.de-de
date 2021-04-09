---
description: Die Registrierungs Tabelle enthält die Registrierungsinformationen, die von der Anwendung in der Systemregistrierung festgelegt werden müssen.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Registrierungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959656"
---
# <a name="registry-table"></a><span data-ttu-id="68d7f-103">Registrierungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="68d7f-103">Registry Table</span></span>

<span data-ttu-id="68d7f-104">Die Registrierungs Tabelle enthält die Registrierungsinformationen, die von der Anwendung in der Systemregistrierung festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="68d7f-104">The Registry table holds the registry information that the application needs to set in the system registry.</span></span>

<span data-ttu-id="68d7f-105">Die Registrierungs Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="68d7f-105">The Registry table has the following columns.</span></span>



| <span data-ttu-id="68d7f-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="68d7f-106">Column</span></span>      | <span data-ttu-id="68d7f-107">Typ</span><span class="sxs-lookup"><span data-stu-id="68d7f-107">Type</span></span>                         | <span data-ttu-id="68d7f-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="68d7f-108">Key</span></span> | <span data-ttu-id="68d7f-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="68d7f-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="68d7f-110">Registrierung</span><span class="sxs-lookup"><span data-stu-id="68d7f-110">Registry</span></span>    | [<span data-ttu-id="68d7f-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="68d7f-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="68d7f-112">J</span><span class="sxs-lookup"><span data-stu-id="68d7f-112">Y</span></span>   | <span data-ttu-id="68d7f-113">N</span><span class="sxs-lookup"><span data-stu-id="68d7f-113">N</span></span>        |
| <span data-ttu-id="68d7f-114">Root</span><span class="sxs-lookup"><span data-stu-id="68d7f-114">Root</span></span>        | [<span data-ttu-id="68d7f-115">Integer</span><span class="sxs-lookup"><span data-stu-id="68d7f-115">Integer</span></span>](integer.md)       | <span data-ttu-id="68d7f-116">N</span><span class="sxs-lookup"><span data-stu-id="68d7f-116">N</span></span>   | <span data-ttu-id="68d7f-117">N</span><span class="sxs-lookup"><span data-stu-id="68d7f-117">N</span></span>        |
| <span data-ttu-id="68d7f-118">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="68d7f-118">Key</span></span>         | [<span data-ttu-id="68d7f-119">Regfad</span><span class="sxs-lookup"><span data-stu-id="68d7f-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="68d7f-120">N</span><span class="sxs-lookup"><span data-stu-id="68d7f-120">N</span></span>   | <span data-ttu-id="68d7f-121">N</span><span class="sxs-lookup"><span data-stu-id="68d7f-121">N</span></span>        |
| <span data-ttu-id="68d7f-122">Name</span><span class="sxs-lookup"><span data-stu-id="68d7f-122">Name</span></span>        | [<span data-ttu-id="68d7f-123">Großformatige</span><span class="sxs-lookup"><span data-stu-id="68d7f-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="68d7f-124">N</span><span class="sxs-lookup"><span data-stu-id="68d7f-124">N</span></span>   | <span data-ttu-id="68d7f-125">J</span><span class="sxs-lookup"><span data-stu-id="68d7f-125">Y</span></span>        |
| <span data-ttu-id="68d7f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="68d7f-126">Value</span></span>       | [<span data-ttu-id="68d7f-127">Großformatige</span><span class="sxs-lookup"><span data-stu-id="68d7f-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="68d7f-128">N</span><span class="sxs-lookup"><span data-stu-id="68d7f-128">N</span></span>   | <span data-ttu-id="68d7f-129">J</span><span class="sxs-lookup"><span data-stu-id="68d7f-129">Y</span></span>        |
| <span data-ttu-id="68d7f-130">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="68d7f-130">Component\_</span></span> | [<span data-ttu-id="68d7f-131">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="68d7f-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="68d7f-132">N</span><span class="sxs-lookup"><span data-stu-id="68d7f-132">N</span></span>   | <span data-ttu-id="68d7f-133">N</span><span class="sxs-lookup"><span data-stu-id="68d7f-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="68d7f-134">Spalten</span><span class="sxs-lookup"><span data-stu-id="68d7f-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="68d7f-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registrierungs</span><span class="sxs-lookup"><span data-stu-id="68d7f-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registry</span></span>
</dt> <dd>

<span data-ttu-id="68d7f-136">Der Primärschlüssel, der zum Identifizieren eines Registrierungsdaten Satzes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68d7f-136">Primary key used to identify a registry record.</span></span>

</dd> <dt>

<span data-ttu-id="68d7f-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Fasst</span><span class="sxs-lookup"><span data-stu-id="68d7f-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="68d7f-138">Der vordefinierte Stamm Schlüssel für den Registrierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="68d7f-138">The predefined root key for the registry value.</span></span> <span data-ttu-id="68d7f-139">Geben Sie in diesem Feld den Wert-1 ein, um den Stamm Schlüssel vom Installationstyp abhängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="68d7f-139">Enter a value of -1 in this field to make the root key dependent on the type of installation.</span></span> <span data-ttu-id="68d7f-140">Geben Sie einen der anderen Werte in der folgenden Tabelle ein, um zu erzwingen, dass der Registrierungs Wert unter einem bestimmten Stamm Schlüssel geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="68d7f-140">Enter one of the other values in the following table to force the registry value to be written under a particular root key.</span></span>



| <span data-ttu-id="68d7f-141">Konstante</span><span class="sxs-lookup"><span data-stu-id="68d7f-141">Constant</span></span>                          | <span data-ttu-id="68d7f-142">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="68d7f-142">Hexadecimal</span></span> | <span data-ttu-id="68d7f-143">Decimal</span><span class="sxs-lookup"><span data-stu-id="68d7f-143">Decimal</span></span> | <span data-ttu-id="68d7f-144">Stamm Schlüssel</span><span class="sxs-lookup"><span data-stu-id="68d7f-144">Root key</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68d7f-145">(none)</span><span class="sxs-lookup"><span data-stu-id="68d7f-145">(none)</span></span>                            | <span data-ttu-id="68d7f-146">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="68d7f-146">\- 0x001</span></span>    | <span data-ttu-id="68d7f-147">-1</span><span class="sxs-lookup"><span data-stu-id="68d7f-147">-1</span></span>      | <span data-ttu-id="68d7f-148">Wenn es sich um eine benutzerspezifische Installation handelt, wird der Registrierungs Wert unter **HKEY \_ Current \_ User** geschrieben.</span><span class="sxs-lookup"><span data-stu-id="68d7f-148">If this is a per-user installation, the registry value is written under **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="68d7f-149">Wenn es sich um eine Computer spezifische Installation handelt, wird der Registrierungs Wert unter **HKEY \_ local \_ Machine** geschrieben.</span><span class="sxs-lookup"><span data-stu-id="68d7f-149">If this is a per-machine installation, the registry value is written under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="68d7f-150">Beachten Sie, dass eine Computer spezifische Installation durch Festlegen der [**ALLUSERS**](allusers.md) -Eigenschaft auf 1 angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="68d7f-150">Note that a per-machine installation is specified by setting the [**ALLUSERS**](allusers.md) property to 1.</span></span><br/>                |
| <span data-ttu-id="68d7f-151">**msidbregistryrootclassesroot**</span><span class="sxs-lookup"><span data-stu-id="68d7f-151">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="68d7f-152">0x000</span><span class="sxs-lookup"><span data-stu-id="68d7f-152">0x000</span></span>       | <span data-ttu-id="68d7f-153">0</span><span class="sxs-lookup"><span data-stu-id="68d7f-153">0</span></span>       | <span data-ttu-id="68d7f-154">**HKEY \_ Klassen \_** Stamm: das Installationsprogramm schreibt oder entfernt den Wert aus der **HKCU- \\ Software \\ Klassen** Hive während der Installation im [Installations Kontext](installation-context.md)pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="68d7f-154">**HKEY\_CLASSES\_ROOT** The installer writes or removes the value from the **HKCU\\Software\\Classes** hive during installation in the per-user [installation context](installation-context.md).</span></span><br/> <span data-ttu-id="68d7f-155">Der Installer schreibt oder entfernt den Wert aus der **HKLM- \\ Software \\ Klassen** Struktur während der Installation pro Computer.</span><span class="sxs-lookup"><span data-stu-id="68d7f-155">The installer writes or removes the value from the **HKLM\\Software\\Classes** hive during per-machine installations.</span></span><br/> |
| <span data-ttu-id="68d7f-156">**msidbregistryrootcurrentuser**</span><span class="sxs-lookup"><span data-stu-id="68d7f-156">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="68d7f-157">0x001</span><span class="sxs-lookup"><span data-stu-id="68d7f-157">0x001</span></span>       | <span data-ttu-id="68d7f-158">1</span><span class="sxs-lookup"><span data-stu-id="68d7f-158">1</span></span>       | <span data-ttu-id="68d7f-159">**Aktueller HKEY- \_ \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="68d7f-159">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="68d7f-160">**msidbregistryrootlocalmachine**</span><span class="sxs-lookup"><span data-stu-id="68d7f-160">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="68d7f-161">0x002</span><span class="sxs-lookup"><span data-stu-id="68d7f-161">0x002</span></span>       | <span data-ttu-id="68d7f-162">2</span><span class="sxs-lookup"><span data-stu-id="68d7f-162">2</span></span>       | <span data-ttu-id="68d7f-163">**lokaler HKEY- \_ \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="68d7f-163">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="68d7f-164">**msidbregistryrootusers**</span><span class="sxs-lookup"><span data-stu-id="68d7f-164">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="68d7f-165">0x003</span><span class="sxs-lookup"><span data-stu-id="68d7f-165">0x003</span></span>       | <span data-ttu-id="68d7f-166">3</span><span class="sxs-lookup"><span data-stu-id="68d7f-166">3</span></span>       | <span data-ttu-id="68d7f-167">**HKEY- \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="68d7f-167">**HKEY\_USERS**</span></span>                                                                                                                                                                                                                                                                                                                              |



 

<span data-ttu-id="68d7f-168">Beachten Sie, dass in der **HKCU** -Hive geschriebene Registrierungseinträge auf eine Komponente verweisen, in der das registrykeypath-Bit in der Spalte Attribute der [Komponenten Tabelle](component-table.md)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="68d7f-168">Note that it is recommended that registry entries written to the **HKCU** hive reference a component having the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="68d7f-169">Dadurch wird sichergestellt, dass das Installationsprogramm die erforderlichen Registrierungseinträge schreibt, wenn sich mehrere Benutzer auf demselben Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="68d7f-169">This ensures that the installer writes the necessary registry entries when there are multiple users on the same computer.</span></span>

</dd> <dt>

<span data-ttu-id="68d7f-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen</span><span class="sxs-lookup"><span data-stu-id="68d7f-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="68d7f-171">Der lokalisierbare Schlüssel für den Registrierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="68d7f-171">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="68d7f-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="68d7f-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="68d7f-173">Diese Spalte enthält den Namen des Registrierungs Werts (lokalisierbar).</span><span class="sxs-lookup"><span data-stu-id="68d7f-173">This column contains the registry value name (localizable).</span></span> <span data-ttu-id="68d7f-174">Wenn dieser Wert NULL ist, werden die in die Spalte Wert eingegebenen Daten in den Standard Registrierungsschlüssel geschrieben.</span><span class="sxs-lookup"><span data-stu-id="68d7f-174">If this is Null, then the data entered into the Value column are written to the default registry key.</span></span>

<span data-ttu-id="68d7f-175">Wenn die Value-Spalte NULL ist, haben die Zeichen folgen, die in der folgenden Tabelle in der Spalte "Name" angezeigt werden, eine besondere Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="68d7f-175">If the Value column is Null, then the strings shown in the following table in the Name column have special significance.</span></span>



| <span data-ttu-id="68d7f-176">String</span><span class="sxs-lookup"><span data-stu-id="68d7f-176">String</span></span> | <span data-ttu-id="68d7f-177">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="68d7f-177">Meaning</span></span>                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | <span data-ttu-id="68d7f-178">Der Schlüssel muss bei der Installation der Komponente erstellt werden, falls er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="68d7f-178">The key is to be created, if absent, when the component is installed.</span></span>                                                                                                                            |
| \-     | <span data-ttu-id="68d7f-179">Wenn die Komponente deinstalliert wird, muss der Schlüssel ggf. mit allen zugehörigen Werten und unter Schlüsseln gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="68d7f-179">The key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span>                                                                                     |
| \*     | <span data-ttu-id="68d7f-180">Der Schlüssel muss bei der Installation der Komponente erstellt werden, falls er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="68d7f-180">The key is to be created, if absent, when the component is installed.</span></span> <span data-ttu-id="68d7f-181">Außerdem muss der Schlüssel bei der Deinstallation der Komponente ggf. mit allen zugehörigen Werten und unter Schlüsseln gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="68d7f-181">Additionally, the key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span> |



 

<span data-ttu-id="68d7f-182">Beachten Sie, dass die [Tabelle removeregistry](removeregistry-table.md) verwendet werden muss, wenn ein installierter Registrierungsschlüssel mit seinen Werten und unter Schlüsseln gelöscht werden soll, wenn die Komponente installiert ist.</span><span class="sxs-lookup"><span data-stu-id="68d7f-182">Note that the [RemoveRegistry table](removeregistry-table.md) must be used if an installed registry key is to be deleted, with its values and subkeys, when the component is installed.</span></span>

</dd> <dt>

<span data-ttu-id="68d7f-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="68d7f-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="68d7f-184">Diese Spalte ist der lokalisierbare Registrierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="68d7f-184">This column is the localizable registry value.</span></span> <span data-ttu-id="68d7f-185">Das Feld ist [formatiert](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="68d7f-185">The field is [Formatted](formatted.md).</span></span> <span data-ttu-id="68d7f-186">Wenn der Wert einem der folgenden Präfixe (d. h. Wert) angefügt wird, \# % wird der Wert wie in der Tabelle beschrieben interpretiert.</span><span class="sxs-lookup"><span data-stu-id="68d7f-186">If the value is attached to one of the following prefixes (i.e. \#%*value*) then the value is interpreted as described in the table.</span></span> <span data-ttu-id="68d7f-187">Beachten Sie, dass jedes Präfix mit einem Nummern Zeichen ( \# ) beginnt.</span><span class="sxs-lookup"><span data-stu-id="68d7f-187">Note that each prefix begins with a number sign (\#).</span></span> <span data-ttu-id="68d7f-188">Wenn der Wert mit zwei oder mehr aufeinander folgenden Nummern Zeichen ( \# ) beginnt, wird der erste \# ignoriert, und der Wert wird als Zeichenfolge interpretiert und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="68d7f-188">If the value begins with two or more consecutive number signs (\#), the first \# is ignored and value is interpreted and stored as a string.</span></span>



| <span data-ttu-id="68d7f-189">Präfix</span><span class="sxs-lookup"><span data-stu-id="68d7f-189">Prefix</span></span> | <span data-ttu-id="68d7f-190">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="68d7f-190">Meaning</span></span>                                                                        |
|--------|--------------------------------------------------------------------------------|
| <span data-ttu-id="68d7f-191">\#Stuben</span><span class="sxs-lookup"><span data-stu-id="68d7f-191">\#x</span></span>    | <span data-ttu-id="68d7f-192">Der Wert wird interpretiert und als Hexadezimalwert (reg \_ Binary) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="68d7f-192">The value is interpreted and stored as a hexadecimal value (REG\_BINARY).</span></span>      |
| \#%    | <span data-ttu-id="68d7f-193">Der Wert wird interpretiert und als erweiterbare Zeichenfolge (reg \_ Expand \_ SZ) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="68d7f-193">The value is interpreted and stored as an expandable string (REG\_EXPAND\_SZ).</span></span> |
| \#     | <span data-ttu-id="68d7f-194">Der Wert wird interpretiert und als ganze Zahl gespeichert (reg \_ DWORD).</span><span class="sxs-lookup"><span data-stu-id="68d7f-194">The value is interpreted and stored as an integer (REG\_DWORD).</span></span>                |



 

-   <span data-ttu-id="68d7f-195">Wenn der Wert die Sequenz Tilde enthält \[ ~ \] , wird der Wert als eine durch Null getrennte Liste von Zeichen folgen (reg \_ \_ MultiSZ) interpretiert.</span><span class="sxs-lookup"><span data-stu-id="68d7f-195">If the value contains the sequence tilde \[~\], then the value is interpreted as a Null-delimited list of strings (REG\_MULTI\_SZ).</span></span> <span data-ttu-id="68d7f-196">Um z. b. eine Liste anzugeben, die die drei Zeichen folgen a, b und c enthält, verwenden Sie "a \[ ~ \] b \[ ~ \] c".</span><span class="sxs-lookup"><span data-stu-id="68d7f-196">For example, to specify a list containing the three strings a, b and c, use "a\[~\]b\[~\]c".</span></span>
-   <span data-ttu-id="68d7f-197">Die Sequenz \[ ~ \] innerhalb des Werts trennt die einzelnen Zeichen folgen und wird als NULL-Zeichen interpretiert und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="68d7f-197">The sequence \[~\] within the value separates the individual strings and is interpreted and stored as a Null character.</span></span>
-   <span data-ttu-id="68d7f-198">Wenn eine \[ ~ \] der Zeichen folgen Liste vorangestellt ist, werden die Zeichen folgen an alle vorhandenen Registrierungs Wert Zeichenfolgen angehängt.</span><span class="sxs-lookup"><span data-stu-id="68d7f-198">If a \[~\] precedes the string list, the strings are to be appended to any existing registry value strings.</span></span> <span data-ttu-id="68d7f-199">Wenn bereits eine Anfüge Zeichenfolge im Registrierungs Wert vorhanden ist, wird das ursprüngliche Vorkommen der Zeichenfolge entfernt.</span><span class="sxs-lookup"><span data-stu-id="68d7f-199">If an appending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="68d7f-200">Wenn ein \[ ~ \] auf das Ende der Zeichen folgen Liste folgt, werden die Zeichen folgen allen vorhandenen Registrierungs Wert Zeichenfolgen vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="68d7f-200">If a \[~\] follows the end of the string list, the strings are to be prepended to any existing registry value strings.</span></span> <span data-ttu-id="68d7f-201">Wenn bereits eine ausstehende Zeichenfolge im Registrierungs Wert vorhanden ist, wird das ursprüngliche Vorkommen der Zeichenfolge entfernt.</span><span class="sxs-lookup"><span data-stu-id="68d7f-201">If a prepending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="68d7f-202">Wenn ein \[ ~ \] sowohl am Anfang als auch am Ende oder weder am Anfang noch am Ende der Zeichen folgen Liste vorhanden ist, müssen die Zeichen folgen vorhandene Registrierungs Wert Zeichenfolgen ersetzen.</span><span class="sxs-lookup"><span data-stu-id="68d7f-202">If a \[~\] is at both the beginning and the end or at neither the beginning nor the end of the string list, the strings are to replace any existing registry value strings.</span></span>
-   <span data-ttu-id="68d7f-203">Andernfalls wird der Wert interpretiert und als Zeichenfolge (reg \_ SZ) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="68d7f-203">Otherwise, the value is interpreted and stored as a string (REG\_SZ).</span></span>

</dd> <dt>

<span data-ttu-id="68d7f-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="68d7f-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="68d7f-205">Externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md) , die auf die Komponente verweist, mit der die Installation des Registrierungs Werts gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="68d7f-205">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68d7f-206">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68d7f-206">Remarks</span></span>

<span data-ttu-id="68d7f-207">Die Aktionen " [schreiteregistryvalues](writeregistryvalues-action.md) " und " [removeregistryvalues](removeregistryvalues-action.md) " in [*Sequenz Tabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="68d7f-207">The [WriteRegistryValues](writeregistryvalues-action.md) and [RemoveRegistryValues](removeregistryvalues-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="68d7f-208">Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="68d7f-208">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="68d7f-209">Die Registrierungsinformationen werden in die Systemregistrierung geschrieben, wenn die entsprechende Komponente für die lokale Installation ausgewählt oder von der Quelle aus ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="68d7f-209">The registry information is written out to the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="68d7f-210">Beachten Sie, dass das Installationsprogramm einen Registrierungsschlüssel entfernt, nachdem der letzte Wert oder Unterschlüssel unter dem Schlüssel entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="68d7f-210">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="68d7f-211">Um zu verhindern, dass ein leerer Registrierungsschlüssel beim Deinstallieren von entfernt wird, schreiben Sie einen Dummy-Wert unter dem Schlüssel, den Sie aufbewahren müssen, und geben Sie in der Spalte Name den Wert + ein.</span><span class="sxs-lookup"><span data-stu-id="68d7f-211">To prevent an empty registry key from being removed when uninstalling, write a dummy value under the key you need to keep and enter + in the Name column.</span></span> <span data-ttu-id="68d7f-212">Wenn \* in der Spalte Name ist, wird der Schlüssel mit allen zugehörigen Werten und unter Schlüsseln gelöscht, wenn die Komponente entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="68d7f-212">If \* is in the Name column, the key is deleted, with all of its values and subkeys, when the component is removed.</span></span>

<span data-ttu-id="68d7f-213">Eine benutzerdefinierte Aktion kann verwendet werden, um der Registrierungs Tabelle während einer Installation, einer Neuinstallation oder einer Reparatur Transaktion Zeilen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="68d7f-213">A custom action can be used to add rows to the Registry table during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="68d7f-214">Diese Zeilen bleiben in der Registrierungs Tabelle nicht erhalten, und die Informationen sind nur während der aktuellen Transaktion verfügbar.</span><span class="sxs-lookup"><span data-stu-id="68d7f-214">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="68d7f-215">Die benutzerdefinierte Aktion muss daher bei jeder Installation, deinstalstallation oder Reparatur Transaktion ausgeführt werden, die die Informationen in diesen zusätzlichen Zeilen benötigt.</span><span class="sxs-lookup"><span data-stu-id="68d7f-215">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="68d7f-216">Die benutzerdefinierte Aktion muss vor den Aktionen [removeregistryvalues](removeregistryvalues-action.md) und [schreiteregistryvalues](writeregistryvalues-action.md) in der Aktions Sequenz erfolgen.</span><span class="sxs-lookup"><span data-stu-id="68d7f-216">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

<span data-ttu-id="68d7f-217">Informationen zum Sichern eines Registrierungsschlüssels finden Sie in der Tabelle " [msilockpermissionsex](msilockpermissionsex-table.md) " und in der [Tabelle "lockberechtigungs](lockpermissions-table.md)Tabelle".</span><span class="sxs-lookup"><span data-stu-id="68d7f-217">For information on how to secure a registry key see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="68d7f-218">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="68d7f-218">Validation</span></span>

<dl>

[<span data-ttu-id="68d7f-219">ICE02</span><span class="sxs-lookup"><span data-stu-id="68d7f-219">ICE02</span></span>](ice02.md)  
[<span data-ttu-id="68d7f-220">ICE03</span><span class="sxs-lookup"><span data-stu-id="68d7f-220">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="68d7f-221">ICE06</span><span class="sxs-lookup"><span data-stu-id="68d7f-221">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="68d7f-222">ICE32</span><span class="sxs-lookup"><span data-stu-id="68d7f-222">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="68d7f-223">ICE38</span><span class="sxs-lookup"><span data-stu-id="68d7f-223">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="68d7f-224">ICE43</span><span class="sxs-lookup"><span data-stu-id="68d7f-224">ICE43</span></span>](ice43.md)  
[<span data-ttu-id="68d7f-225">ICE46</span><span class="sxs-lookup"><span data-stu-id="68d7f-225">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="68d7f-226">ICE49</span><span class="sxs-lookup"><span data-stu-id="68d7f-226">ICE49</span></span>](ice49.md)  
[<span data-ttu-id="68d7f-227">ICE53</span><span class="sxs-lookup"><span data-stu-id="68d7f-227">ICE53</span></span>](ice53.md)  
[<span data-ttu-id="68d7f-228">ICE55</span><span class="sxs-lookup"><span data-stu-id="68d7f-228">ICE55</span></span>](ice55.md)  
[<span data-ttu-id="68d7f-229">ICE57</span><span class="sxs-lookup"><span data-stu-id="68d7f-229">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="68d7f-230">ICE70</span><span class="sxs-lookup"><span data-stu-id="68d7f-230">ICE70</span></span>](ice70.md)  
[<span data-ttu-id="68d7f-231">ICE80</span><span class="sxs-lookup"><span data-stu-id="68d7f-231">ICE80</span></span>](ice80.md)  
</dl>

 

 




