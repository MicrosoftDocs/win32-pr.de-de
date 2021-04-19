---
description: Die reglocator-Tabelle enthält die Informationen, die für die Suche nach einer Datei oder einem Verzeichnis mithilfe der Registrierung erforderlich sind, oder um nach einem bestimmten Registrierungs Eintrag zu suchen. Diese Tabelle weist die folgenden Spalten auf.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: Reglocator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351663"
---
# <a name="reglocator-table"></a><span data-ttu-id="b80da-104">Reglocator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="b80da-104">RegLocator Table</span></span>

<span data-ttu-id="b80da-105">Die reglocator-Tabelle enthält die Informationen, die für die Suche nach einer Datei oder einem Verzeichnis mithilfe der Registrierung erforderlich sind, oder um nach einem bestimmten Registrierungs Eintrag zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b80da-105">The RegLocator table holds the information needed to search for a file or directory using the registry, or to search for a particular registry entry itself.</span></span> <span data-ttu-id="b80da-106">Diese Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="b80da-106">This table has the following columns.</span></span>



| <span data-ttu-id="b80da-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="b80da-107">Column</span></span>      | <span data-ttu-id="b80da-108">Typ</span><span class="sxs-lookup"><span data-stu-id="b80da-108">Type</span></span>                         | <span data-ttu-id="b80da-109">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b80da-109">Key</span></span> | <span data-ttu-id="b80da-110">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="b80da-110">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="b80da-111">Signatur\_</span><span class="sxs-lookup"><span data-stu-id="b80da-111">Signature\_</span></span> | [<span data-ttu-id="b80da-112">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b80da-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="b80da-113">J</span><span class="sxs-lookup"><span data-stu-id="b80da-113">Y</span></span>   | <span data-ttu-id="b80da-114">N</span><span class="sxs-lookup"><span data-stu-id="b80da-114">N</span></span>        |
| <span data-ttu-id="b80da-115">Root</span><span class="sxs-lookup"><span data-stu-id="b80da-115">Root</span></span>        | [<span data-ttu-id="b80da-116">Integer</span><span class="sxs-lookup"><span data-stu-id="b80da-116">Integer</span></span>](integer.md)       | <span data-ttu-id="b80da-117">N</span><span class="sxs-lookup"><span data-stu-id="b80da-117">N</span></span>   | <span data-ttu-id="b80da-118">N</span><span class="sxs-lookup"><span data-stu-id="b80da-118">N</span></span>        |
| <span data-ttu-id="b80da-119">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b80da-119">Key</span></span>         | [<span data-ttu-id="b80da-120">Regfad</span><span class="sxs-lookup"><span data-stu-id="b80da-120">RegPath</span></span>](regpath.md)       | <span data-ttu-id="b80da-121">N</span><span class="sxs-lookup"><span data-stu-id="b80da-121">N</span></span>   | <span data-ttu-id="b80da-122">N</span><span class="sxs-lookup"><span data-stu-id="b80da-122">N</span></span>        |
| <span data-ttu-id="b80da-123">Name</span><span class="sxs-lookup"><span data-stu-id="b80da-123">Name</span></span>        | [<span data-ttu-id="b80da-124">Großformatige</span><span class="sxs-lookup"><span data-stu-id="b80da-124">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b80da-125">N</span><span class="sxs-lookup"><span data-stu-id="b80da-125">N</span></span>   | <span data-ttu-id="b80da-126">J</span><span class="sxs-lookup"><span data-stu-id="b80da-126">Y</span></span>        |
| <span data-ttu-id="b80da-127">Typ</span><span class="sxs-lookup"><span data-stu-id="b80da-127">Type</span></span>        | [<span data-ttu-id="b80da-128">Integer</span><span class="sxs-lookup"><span data-stu-id="b80da-128">Integer</span></span>](integer.md)       | <span data-ttu-id="b80da-129">N</span><span class="sxs-lookup"><span data-stu-id="b80da-129">N</span></span>   | <span data-ttu-id="b80da-130">J</span><span class="sxs-lookup"><span data-stu-id="b80da-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b80da-131">Spalten</span><span class="sxs-lookup"><span data-stu-id="b80da-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b80da-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_</span><span class="sxs-lookup"><span data-stu-id="b80da-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="b80da-133">Der Wert im Feld Signatur \_ stellt eine eindeutige Signatur dar, bei der es sich um einen externen Schlüssel in Spalte 1 der [Signatur](signature-table.md) Tabelle handelt.</span><span class="sxs-lookup"><span data-stu-id="b80da-133">The value in the Signature\_ field represents a unique signature that is an external key into column one of the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="b80da-134">Wenn diese Signatur in der Signatur Tabelle vorhanden ist, wird die Suche nach einer Datei durchsucht.</span><span class="sxs-lookup"><span data-stu-id="b80da-134">If this signature is present in the Signature table, the search is for a file.</span></span> <span data-ttu-id="b80da-135">Wenn diese Signatur in der Signatur Tabelle nicht vorhanden ist und der Wert der Type-Spalte **msidblocatortyperawvalue** lautet, ist die Suche nach dem Namen des Registrierungsschlüssels, auf den von der reglocator-Tabelle verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b80da-135">If this signature is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the registry key name pointed to by the RegLocator table.</span></span> <span data-ttu-id="b80da-136">Andernfalls ist die Suche nach einem Verzeichnis, auf das von der reglocator-Tabelle verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b80da-136">Otherwise the search is for a directory pointed to by the RegLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="b80da-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Fasst</span><span class="sxs-lookup"><span data-stu-id="b80da-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="b80da-138">Der vordefinierte Stamm Schlüssel für den Registrierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="b80da-138">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="b80da-139">Konstante</span><span class="sxs-lookup"><span data-stu-id="b80da-139">Constant</span></span>                          | <span data-ttu-id="b80da-140">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="b80da-140">Hexadecimal</span></span> | <span data-ttu-id="b80da-141">Decimal</span><span class="sxs-lookup"><span data-stu-id="b80da-141">Decimal</span></span> | <span data-ttu-id="b80da-142">Stamm Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b80da-142">Root key</span></span>             |
|-----------------------------------|-------------|---------|----------------------|
| <span data-ttu-id="b80da-143">**msidbregistryrootclassesroot**</span><span class="sxs-lookup"><span data-stu-id="b80da-143">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="b80da-144">0x000</span><span class="sxs-lookup"><span data-stu-id="b80da-144">0x000</span></span>       | <span data-ttu-id="b80da-145">0</span><span class="sxs-lookup"><span data-stu-id="b80da-145">0</span></span>       | <span data-ttu-id="b80da-146">HKEY- \_ Klassen Stamm \_</span><span class="sxs-lookup"><span data-stu-id="b80da-146">HKEY\_CLASSES\_ROOT</span></span>  |
| <span data-ttu-id="b80da-147">**msidbregistryrootcurrentuser**</span><span class="sxs-lookup"><span data-stu-id="b80da-147">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="b80da-148">0x001</span><span class="sxs-lookup"><span data-stu-id="b80da-148">0x001</span></span>       | <span data-ttu-id="b80da-149">1</span><span class="sxs-lookup"><span data-stu-id="b80da-149">1</span></span>       | <span data-ttu-id="b80da-150">Aktueller HKEY- \_ \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="b80da-150">HKEY\_CURRENT\_USER</span></span>  |
| <span data-ttu-id="b80da-151">**msidbregistryrootlocalmachine**</span><span class="sxs-lookup"><span data-stu-id="b80da-151">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="b80da-152">0x002</span><span class="sxs-lookup"><span data-stu-id="b80da-152">0x002</span></span>       | <span data-ttu-id="b80da-153">2</span><span class="sxs-lookup"><span data-stu-id="b80da-153">2</span></span>       | <span data-ttu-id="b80da-154">lokaler HKEY- \_ \_ Computer</span><span class="sxs-lookup"><span data-stu-id="b80da-154">HKEY\_LOCAL\_MACHINE</span></span> |
| <span data-ttu-id="b80da-155">**msidbregistryrootusers**</span><span class="sxs-lookup"><span data-stu-id="b80da-155">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="b80da-156">0x003</span><span class="sxs-lookup"><span data-stu-id="b80da-156">0x003</span></span>       | <span data-ttu-id="b80da-157">3</span><span class="sxs-lookup"><span data-stu-id="b80da-157">3</span></span>       | <span data-ttu-id="b80da-158">HKEY- \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="b80da-158">HKEY\_USERS</span></span>          |



 

</dd> <dt>

<span data-ttu-id="b80da-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen</span><span class="sxs-lookup"><span data-stu-id="b80da-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="b80da-160">Der Schlüssel für den Registrierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="b80da-160">The key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="b80da-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="b80da-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="b80da-162">Der Name des Registrierungswerts.</span><span class="sxs-lookup"><span data-stu-id="b80da-162">The registry value name.</span></span> <span data-ttu-id="b80da-163">Wenn dieser Wert NULL ist, wird der Wert aus dem unbenannten oder Standardwert des Schlüssels abgerufen, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b80da-163">If this value is null, then the value from the key's unnamed or default value, if any, is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="b80da-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte</span><span class="sxs-lookup"><span data-stu-id="b80da-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="b80da-165">Ein Wert, der bestimmt, ob der Registrierungs Wert ein Dateiname, ein Verzeichnis Speicherort oder ein unformatierten Registrierungs Wert ist.</span><span class="sxs-lookup"><span data-stu-id="b80da-165">A value that determines if the registry value is a file name, a directory location, or raw registry value.</span></span>

<span data-ttu-id="b80da-166">In der folgenden Tabelle sind gültige Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b80da-166">The following table lists valid values.</span></span> <span data-ttu-id="b80da-167">Legen Sie einen der ersten drei Werte und **msidbLocatorType64bit** bei Bedarf fest.</span><span class="sxs-lookup"><span data-stu-id="b80da-167">Set one of the first three values and **msidbLocatorType64bit** if necessary.</span></span> <span data-ttu-id="b80da-168">Wenn der Eintrag in diesem Feld nicht vorhanden ist, wird Type auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b80da-168">If the entry in this field is absent, Type is set to be 1.</span></span>



| <span data-ttu-id="b80da-169">Konstante</span><span class="sxs-lookup"><span data-stu-id="b80da-169">Constant</span></span>                      | <span data-ttu-id="b80da-170">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="b80da-170">Hexadecimal</span></span> | <span data-ttu-id="b80da-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="b80da-171">Decimal</span></span> | <span data-ttu-id="b80da-172">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b80da-172">Description</span></span>                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b80da-173">**msidbloprojekttypedirectory**</span><span class="sxs-lookup"><span data-stu-id="b80da-173">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="b80da-174">0x000</span><span class="sxs-lookup"><span data-stu-id="b80da-174">0x000</span></span>       | <span data-ttu-id="b80da-175">0</span><span class="sxs-lookup"><span data-stu-id="b80da-175">0</span></span>       | <span data-ttu-id="b80da-176">Der Schlüssel Pfad ist ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="b80da-176">Key path is a directory.</span></span>                                                                                                                                           |
| <span data-ttu-id="b80da-177">**msidblo-typefilename**</span><span class="sxs-lookup"><span data-stu-id="b80da-177">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="b80da-178">0x001</span><span class="sxs-lookup"><span data-stu-id="b80da-178">0x001</span></span>       | <span data-ttu-id="b80da-179">1</span><span class="sxs-lookup"><span data-stu-id="b80da-179">1</span></span>       | <span data-ttu-id="b80da-180">Der Schlüssel Pfad ist ein Dateiname.</span><span class="sxs-lookup"><span data-stu-id="b80da-180">Key path is a file name.</span></span>                                                                                                                                           |
| <span data-ttu-id="b80da-181">**msidbloserortyperawvalue**</span><span class="sxs-lookup"><span data-stu-id="b80da-181">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="b80da-182">0x002</span><span class="sxs-lookup"><span data-stu-id="b80da-182">0x002</span></span>       | <span data-ttu-id="b80da-183">2</span><span class="sxs-lookup"><span data-stu-id="b80da-183">2</span></span>       | <span data-ttu-id="b80da-184">Der Schlüssel Pfad ist ein Registrierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="b80da-184">Key path is a registry value.</span></span>                                                                                                                                      |
| <span data-ttu-id="b80da-185">**msidbLocatorType64bit**</span><span class="sxs-lookup"><span data-stu-id="b80da-185">**msidbLocatorType64bit**</span></span>     | <span data-ttu-id="b80da-186">0x010</span><span class="sxs-lookup"><span data-stu-id="b80da-186">0x010</span></span>       | <span data-ttu-id="b80da-187">16</span><span class="sxs-lookup"><span data-stu-id="b80da-187">16</span></span>      | <span data-ttu-id="b80da-188">Legen Sie dieses Bit fest, damit das Installationsprogramm den 64-Bit-Teil der Registrierung durchsucht.</span><span class="sxs-lookup"><span data-stu-id="b80da-188">Set this bit to have the installer search the 64-bit portion of the registry.</span></span> <span data-ttu-id="b80da-189">Legen Sie dieses Bit nicht fest, damit das Installationsprogramm den 32-Bit-Teil der Registrierung durchsucht.</span><span class="sxs-lookup"><span data-stu-id="b80da-189">Do not set this bit to have the installer search the 32-bit portion of the registry.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b80da-190">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b80da-190">Remarks</span></span>

<span data-ttu-id="b80da-191">Beachten Sie, dass das Installationsprogramm den Wert der Eigenschaft, die im Feld "Eigenschaft" der [AppSearch](appsearch-table.md) -Tabelle angegeben ist, auf den Registrierungs Wert festlegt, wenn der Wert im type-Feld " **msidblokatortyperawvalue**" ist.</span><span class="sxs-lookup"><span data-stu-id="b80da-191">Note that if the value in the Type field is **msidbLocatorTypeRawValue**, the installer sets the value of the property specified in the Property field of the [AppSearch](appsearch-table.md) table to the registry value.</span></span> <span data-ttu-id="b80da-192">Das Installationsprogramm fügt dem Registrierungs Wert ein Präfix hinzu, das den Typ des Registrierungs Werts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b80da-192">The installer adds a prefix to the registry value that identifies the type of registry value.</span></span> <span data-ttu-id="b80da-193">Weitere Informationen zu Typen von Registrierungs Werten finden Sie unter [Registrierungs Werttypen](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="b80da-193">For more information about types of registry values, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>



| <span data-ttu-id="b80da-194">Registrierungstyp</span><span class="sxs-lookup"><span data-stu-id="b80da-194">Registry type</span></span>   | <span data-ttu-id="b80da-195">Durch Installer hinzugefügtes Präfix</span><span class="sxs-lookup"><span data-stu-id="b80da-195">Prefix added by Installer</span></span>                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b80da-196">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="b80da-196">REG\_SZ</span></span>         | <span data-ttu-id="b80da-197">Keine, aber wenn das erste Zeichen des Registrierungs Werts ist \# , schützt das Installationsprogramm das Zeichen, indem es einem anderen vorangestellt wird \# .</span><span class="sxs-lookup"><span data-stu-id="b80da-197">None, but if the first character of the registry value is \#, the installer escapes the character by prefixing a another \#.</span></span>            |
| <span data-ttu-id="b80da-198">DWORD</span><span class="sxs-lookup"><span data-stu-id="b80da-198">DWORD</span></span>           | <span data-ttu-id="b80da-199">" \# ", optional gefolgt von "+" oder "-"</span><span class="sxs-lookup"><span data-stu-id="b80da-199">"\#" optionally followed by '+' or '-'</span></span>                                                                                                  |
| <span data-ttu-id="b80da-200">REG \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="b80da-200">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="b80da-201">"\#%"</span><span class="sxs-lookup"><span data-stu-id="b80da-201">"\#%"</span></span>                                                                                                                                   |
| <span data-ttu-id="b80da-202">REG \_ \_ MultiSZ</span><span class="sxs-lookup"><span data-stu-id="b80da-202">REG\_MULTI\_SZ</span></span>  | <span data-ttu-id="b80da-203">Null.</span><span class="sxs-lookup"><span data-stu-id="b80da-203">Null.</span></span> <span data-ttu-id="b80da-204">Der Installer legt die-Eigenschaft auf einen Wert fest, der mit Null beginnt und mit einem NULL-Wert endet.</span><span class="sxs-lookup"><span data-stu-id="b80da-204">The installer sets the property to a value beginning with a null and ending with a null.</span></span>                                          |
| <span data-ttu-id="b80da-205">REG- \_ Binärdatei</span><span class="sxs-lookup"><span data-stu-id="b80da-205">REG\_BINARY</span></span>     | <span data-ttu-id="b80da-206">" \# x" im Fall von reg \_ Binary konvertiert und speichert das Installationsprogramm jede hexadezimal Ziffer (Nibble) als ASCII-Zeichen mit dem Präfix " \# x".</span><span class="sxs-lookup"><span data-stu-id="b80da-206">"\#x" In case of REG\_BINARY, the installer converts and saves each hexadecimal digit (nibble) as an ASCII character prefixed by "\#x".</span></span> |



 

<span data-ttu-id="b80da-207">In der Regel werden die Spalten in dieser Tabelle nicht lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="b80da-207">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="b80da-208">Wenn ein Autor eine Suche nach Produkten in mehreren Sprachen beschließt, muss für jede Sprache ein separater Eintrag in der Tabelle enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="b80da-208">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="b80da-209">Beachten Sie, dass es nicht möglich ist, die reglocator-Tabelle zu verwenden, um nur auf das vorhanden sein des Schlüssels zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b80da-209">Note that it is not possible to use the RegLocator table to check only for the presence of the key.</span></span> <span data-ttu-id="b80da-210">Sie können jedoch nach dem Standardwert eines Schlüssels suchen und dessen Wert abrufen, wenn er nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="b80da-210">However, you can search for the default value of a key and retrieve its value if it is not empty.</span></span>

<span data-ttu-id="b80da-211">Weitere Informationen finden Sie unter [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="b80da-211">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="b80da-212">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="b80da-212">Validation</span></span>

<dl>

[<span data-ttu-id="b80da-213">ICE03</span><span class="sxs-lookup"><span data-stu-id="b80da-213">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b80da-214">ICE06</span><span class="sxs-lookup"><span data-stu-id="b80da-214">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b80da-215">ICE46</span><span class="sxs-lookup"><span data-stu-id="b80da-215">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="b80da-216">ICE80</span><span class="sxs-lookup"><span data-stu-id="b80da-216">ICE80</span></span>](ice80.md)  
</dl>

 

 
