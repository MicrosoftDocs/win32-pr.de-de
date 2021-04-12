---
description: Die ModuleConfiguration-Tabelle identifiziert die konfigurierbaren Attribute des Moduls. Diese Tabelle wird nicht in der Datenbank zusammengeführt.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: ModuleConfiguration-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa187c10b5d3376a9bec78eb897b4982445ff01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216566"
---
# <a name="moduleconfiguration-table"></a><span data-ttu-id="59dc5-104">ModuleConfiguration-Tabelle</span><span class="sxs-lookup"><span data-stu-id="59dc5-104">ModuleConfiguration Table</span></span>

<span data-ttu-id="59dc5-105">Die ModuleConfiguration-Tabelle identifiziert die konfigurierbaren Attribute des Moduls.</span><span class="sxs-lookup"><span data-stu-id="59dc5-105">The ModuleConfiguration table identifies the configurable attributes of the module.</span></span> <span data-ttu-id="59dc5-106">Diese Tabelle wird nicht in der Datenbank zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="59dc5-106">This table is not merged into the database.</span></span>

<span data-ttu-id="59dc5-107">Die ModuleConfiguration-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="59dc5-107">The ModuleConfiguration table has the following columns.</span></span>



| <span data-ttu-id="59dc5-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="59dc5-108">Column</span></span>       | <span data-ttu-id="59dc5-109">Typ</span><span class="sxs-lookup"><span data-stu-id="59dc5-109">Type</span></span>                         | <span data-ttu-id="59dc5-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="59dc5-110">Key</span></span> | <span data-ttu-id="59dc5-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="59dc5-111">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="59dc5-112">Name</span><span class="sxs-lookup"><span data-stu-id="59dc5-112">Name</span></span>         | [<span data-ttu-id="59dc5-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="59dc5-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="59dc5-114">J</span><span class="sxs-lookup"><span data-stu-id="59dc5-114">Y</span></span>   | <span data-ttu-id="59dc5-115">N</span><span class="sxs-lookup"><span data-stu-id="59dc5-115">N</span></span>        |
| <span data-ttu-id="59dc5-116">Format</span><span class="sxs-lookup"><span data-stu-id="59dc5-116">Format</span></span>       | [<span data-ttu-id="59dc5-117">Integer</span><span class="sxs-lookup"><span data-stu-id="59dc5-117">Integer</span></span>](integer.md)       | <span data-ttu-id="59dc5-118">N</span><span class="sxs-lookup"><span data-stu-id="59dc5-118">N</span></span>   | <span data-ttu-id="59dc5-119">N</span><span class="sxs-lookup"><span data-stu-id="59dc5-119">N</span></span>        |
| <span data-ttu-id="59dc5-120">type</span><span class="sxs-lookup"><span data-stu-id="59dc5-120">Type</span></span>         | [<span data-ttu-id="59dc5-121">Text</span><span class="sxs-lookup"><span data-stu-id="59dc5-121">Text</span></span>](text.md)             | <span data-ttu-id="59dc5-122">N</span><span class="sxs-lookup"><span data-stu-id="59dc5-122">N</span></span>   | <span data-ttu-id="59dc5-123">J</span><span class="sxs-lookup"><span data-stu-id="59dc5-123">Y</span></span>        |
| <span data-ttu-id="59dc5-124">ContextData</span><span class="sxs-lookup"><span data-stu-id="59dc5-124">ContextData</span></span>  | [<span data-ttu-id="59dc5-125">Text</span><span class="sxs-lookup"><span data-stu-id="59dc5-125">Text</span></span>](text.md)             | <span data-ttu-id="59dc5-126">N</span><span class="sxs-lookup"><span data-stu-id="59dc5-126">N</span></span>   | <span data-ttu-id="59dc5-127">J</span><span class="sxs-lookup"><span data-stu-id="59dc5-127">Y</span></span>        |
| <span data-ttu-id="59dc5-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="59dc5-128">DefaultValue</span></span> | [<span data-ttu-id="59dc5-129">Text</span><span class="sxs-lookup"><span data-stu-id="59dc5-129">Text</span></span>](text.md)             | <span data-ttu-id="59dc5-130">N</span><span class="sxs-lookup"><span data-stu-id="59dc5-130">N</span></span>   | <span data-ttu-id="59dc5-131">J</span><span class="sxs-lookup"><span data-stu-id="59dc5-131">Y</span></span>        |
| <span data-ttu-id="59dc5-132">Attribute</span><span class="sxs-lookup"><span data-stu-id="59dc5-132">Attributes</span></span>   | [<span data-ttu-id="59dc5-133">Integer</span><span class="sxs-lookup"><span data-stu-id="59dc5-133">Integer</span></span>](integer.md)       | <span data-ttu-id="59dc5-134">N</span><span class="sxs-lookup"><span data-stu-id="59dc5-134">N</span></span>   | <span data-ttu-id="59dc5-135">J</span><span class="sxs-lookup"><span data-stu-id="59dc5-135">Y</span></span>        |
| <span data-ttu-id="59dc5-136">DisplayName</span><span class="sxs-lookup"><span data-stu-id="59dc5-136">DisplayName</span></span>  | [<span data-ttu-id="59dc5-137">Text</span><span class="sxs-lookup"><span data-stu-id="59dc5-137">Text</span></span>](text.md)             | <span data-ttu-id="59dc5-138">N</span><span class="sxs-lookup"><span data-stu-id="59dc5-138">N</span></span>   | <span data-ttu-id="59dc5-139">J</span><span class="sxs-lookup"><span data-stu-id="59dc5-139">Y</span></span>        |
| <span data-ttu-id="59dc5-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59dc5-140">Description</span></span>  | [<span data-ttu-id="59dc5-141">Text</span><span class="sxs-lookup"><span data-stu-id="59dc5-141">Text</span></span>](text.md)             | <span data-ttu-id="59dc5-142">N</span><span class="sxs-lookup"><span data-stu-id="59dc5-142">N</span></span>   | <span data-ttu-id="59dc5-143">J</span><span class="sxs-lookup"><span data-stu-id="59dc5-143">Y</span></span>        |
| <span data-ttu-id="59dc5-144">Helplocation</span><span class="sxs-lookup"><span data-stu-id="59dc5-144">HelpLocation</span></span> | [<span data-ttu-id="59dc5-145">Text</span><span class="sxs-lookup"><span data-stu-id="59dc5-145">Text</span></span>](text.md)             | <span data-ttu-id="59dc5-146">N</span><span class="sxs-lookup"><span data-stu-id="59dc5-146">N</span></span>   | <span data-ttu-id="59dc5-147">J</span><span class="sxs-lookup"><span data-stu-id="59dc5-147">Y</span></span>        |
| <span data-ttu-id="59dc5-148">HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="59dc5-148">HelpKeyword</span></span>  | [<span data-ttu-id="59dc5-149">Text</span><span class="sxs-lookup"><span data-stu-id="59dc5-149">Text</span></span>](text.md)             | <span data-ttu-id="59dc5-150">N</span><span class="sxs-lookup"><span data-stu-id="59dc5-150">N</span></span>   | <span data-ttu-id="59dc5-151">J</span><span class="sxs-lookup"><span data-stu-id="59dc5-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="59dc5-152">Spalten</span><span class="sxs-lookup"><span data-stu-id="59dc5-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="59dc5-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="59dc5-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="59dc5-154">Dieses Feld definiert den Namen des konfigurierbaren Elements.</span><span class="sxs-lookup"><span data-stu-id="59dc5-154">This field defines the name of the configurable item.</span></span> <span data-ttu-id="59dc5-155">Auf diesen Namen wird in der Formatierungs Vorlage in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)verwiesen.</span><span class="sxs-lookup"><span data-stu-id="59dc5-155">This name is referenced in the formatting template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="59dc5-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Ges</span><span class="sxs-lookup"><span data-stu-id="59dc5-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Format</span></span>
</dt> <dd>

<span data-ttu-id="59dc5-157">Diese Spalte gibt das Format der Daten an, die geändert werden.</span><span class="sxs-lookup"><span data-stu-id="59dc5-157">This column specifies the format of the data being changed.</span></span>



| <span data-ttu-id="59dc5-158">Format</span><span class="sxs-lookup"><span data-stu-id="59dc5-158">Format</span></span>                                       | <span data-ttu-id="59dc5-159">Wert</span><span class="sxs-lookup"><span data-stu-id="59dc5-159">Value</span></span> |
|----------------------------------------------|-------|
| [<span data-ttu-id="59dc5-160">Text</span><span class="sxs-lookup"><span data-stu-id="59dc5-160">Text</span></span>](text-format-types.md)                | <span data-ttu-id="59dc5-161">0</span><span class="sxs-lookup"><span data-stu-id="59dc5-161">0</span></span>     |
| [<span data-ttu-id="59dc5-162">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="59dc5-162">Key</span></span>](key-format-types.md)                  | <span data-ttu-id="59dc5-163">1</span><span class="sxs-lookup"><span data-stu-id="59dc5-163">1</span></span>     |
| [<span data-ttu-id="59dc5-164">Integer</span><span class="sxs-lookup"><span data-stu-id="59dc5-164">Integer</span></span>](integer-format-types.md)          | <span data-ttu-id="59dc5-165">2</span><span class="sxs-lookup"><span data-stu-id="59dc5-165">2</span></span>     |
| [<span data-ttu-id="59dc5-166">Bitfield-Format</span><span class="sxs-lookup"><span data-stu-id="59dc5-166">Bitfield Format</span></span>](bitfield-format-types.md) | <span data-ttu-id="59dc5-167">3</span><span class="sxs-lookup"><span data-stu-id="59dc5-167">3</span></span>     |



 

</dd> <dt>

<span data-ttu-id="59dc5-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte</span><span class="sxs-lookup"><span data-stu-id="59dc5-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="59dc5-169">Diese Spalte gibt den Typ für die Daten an, die geändert werden.</span><span class="sxs-lookup"><span data-stu-id="59dc5-169">This column specifies the type for the data being changed.</span></span> <span data-ttu-id="59dc5-170">Dieser Typ wird verwendet, um einen Kontext für jede Benutzeroberfläche bereitzustellen, und wird im Mergeprozess nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="59dc5-170">This type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="59dc5-171">Die gültigen Werte für diese Spalte hängen von dem Wert in der Spalte Format ab.</span><span class="sxs-lookup"><span data-stu-id="59dc5-171">The valid values for this column depend on the value in the Format column.</span></span>

</dd> <dt>

<span data-ttu-id="59dc5-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span><span class="sxs-lookup"><span data-stu-id="59dc5-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span></span>
</dt> <dd>

<span data-ttu-id="59dc5-173">In dieser Spalte wird ein semantischer Kontext für die angeforderten Daten angegeben.</span><span class="sxs-lookup"><span data-stu-id="59dc5-173">This column specifies a semantic context for the requested data.</span></span> <span data-ttu-id="59dc5-174">Der-Typ wird verwendet, um einen Kontext für jede Benutzeroberfläche bereitzustellen, und wird im Mergeprozess nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="59dc5-174">The type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="59dc5-175">Die gültigen Werte für diese Spalte sind von den Werten in den Spalten Format und Typ abhängig.</span><span class="sxs-lookup"><span data-stu-id="59dc5-175">The valid values for this column depend on the values in the Format and Type columns.</span></span>

</dd> <dt>

<span data-ttu-id="59dc5-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue</span><span class="sxs-lookup"><span data-stu-id="59dc5-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue</span></span>
</dt> <dd>

<span data-ttu-id="59dc5-177">Diese Spalte gibt einen Standardwert für das Element in diesem Datensatz an, wenn das Merge-Tool einen Wert bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="59dc5-177">This column specifies a default value for the item in this record if the merge tool declines to provide a value.</span></span> <span data-ttu-id="59dc5-178">Dieser Wert muss das Format, den Typ und den Kontext des Elements aufweisen.</span><span class="sxs-lookup"><span data-stu-id="59dc5-178">This value must have the format, type, and context of the item.</span></span> <span data-ttu-id="59dc5-179">Wenn es sich um ein "Key"-Format Element handelt, muss der Fremdschlüssel ein gültiger Schlüssel in die Tabellen des Moduls sein.</span><span class="sxs-lookup"><span data-stu-id="59dc5-179">If this is a "Key" format item, the foreign key must be a valid key into the tables of the module.</span></span> <span data-ttu-id="59dc5-180">NULL ist möglicherweise ein gültiger Wert für diese Spalte, abhängig vom Element.</span><span class="sxs-lookup"><span data-stu-id="59dc5-180">Null may be a valid value for this column depending on the item.</span></span> <span data-ttu-id="59dc5-181">Bei Key-Format Elementen liegt dieser Wert im [cmsm-Sonderformat](cmsm-special-format.md)vor.</span><span class="sxs-lookup"><span data-stu-id="59dc5-181">For "Key" format items, this value is in [CMSM special format](cmsm-special-format.md).</span></span> <span data-ttu-id="59dc5-182">Für alle anderen Typen wird der Wert wörtlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="59dc5-182">For all other types, the value is treated literally.</span></span>

<span data-ttu-id="59dc5-183">Modul Autoren müssen sicherstellen, dass das Modul in seinem Standardzustand gültig ist.</span><span class="sxs-lookup"><span data-stu-id="59dc5-183">Module authors must ensure that the module is valid in its default state.</span></span> <span data-ttu-id="59dc5-184">Dadurch wird sichergestellt, dass Versionen von Mergemod.dll vor Version 2,0 das Modul weiterhin in seinem Standardzustand verwenden können.</span><span class="sxs-lookup"><span data-stu-id="59dc5-184">This ensures that versions of Mergemod.dll earlier than version 2.0 can still use the module in its default state.</span></span>

</dd> <dt>

<span data-ttu-id="59dc5-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt</span><span class="sxs-lookup"><span data-stu-id="59dc5-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="59dc5-186">Diese Spalte ist ein Bitfeld, das Attribute für dieses konfigurierbare Element enthält.</span><span class="sxs-lookup"><span data-stu-id="59dc5-186">This column is a bit field containing attributes for this configurable item.</span></span> <span data-ttu-id="59dc5-187">Null entspricht 0.</span><span class="sxs-lookup"><span data-stu-id="59dc5-187">Null is equivalent to 0.</span></span> <span data-ttu-id="59dc5-188">Alle anderen Bits in dieser Spalte sind für die zukünftige Verwendung reserviert und müssen den Wert 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="59dc5-188">All other bits in this column are reserved for future use and must be 0.</span></span>



| <span data-ttu-id="59dc5-189">Name</span><span class="sxs-lookup"><span data-stu-id="59dc5-189">Name</span></span>                             | <span data-ttu-id="59dc5-190">Decimal</span><span class="sxs-lookup"><span data-stu-id="59dc5-190">Decimal</span></span> | <span data-ttu-id="59dc5-191">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="59dc5-191">Hexadecimal</span></span> | <span data-ttu-id="59dc5-192">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59dc5-192">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59dc5-193">msmconfigurableoptionkeynoverwaiste</span><span class="sxs-lookup"><span data-stu-id="59dc5-193">msmConfigurableOptionKeyNoOrphan</span></span> | <span data-ttu-id="59dc5-194">1</span><span class="sxs-lookup"><span data-stu-id="59dc5-194">1</span></span>       | <span data-ttu-id="59dc5-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="59dc5-195">0x00000001</span></span>  | <span data-ttu-id="59dc5-196">Dieses Attribut gilt nur für Datensätze, die einen Fremdschlüssel für eine Modul Tabelle in Ihrem DefaultValue-Feld auflisten.</span><span class="sxs-lookup"><span data-stu-id="59dc5-196">This attribute only applies to records that list a foreign key to a module table in their DefaultValue field.</span></span> <span data-ttu-id="59dc5-197">Das Merge-Tool ignoriert das-Attribut für alle anderen Formate als die [Schlüssel Format Typen](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="59dc5-197">The merge tool ignores the attribute for any formats other than the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="59dc5-198">Elemente, die nicht in der [ModuleSubstitution-Tabelle](modulesubstitution-table.md) aufgeführt sind, werden von der folgenden Überprüfung ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="59dc5-198">Items not listed in the [ModuleSubstitution table](modulesubstitution-table.md) are excluded from the following check.</span></span> <span data-ttu-id="59dc5-199">Das Merge-Tool führt die Zeile, auf die in der Spalte DefaultValue verwiesen wird, nicht in die Zieldatenbank zusammen, wenn die folgenden Bedingungen erfüllt sind, nachdem alle Konfigurationsoptionen abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="59dc5-199">The merge tool does not merge the row referenced by the DefaultValue column into the target database if the following conditions are satisfied after completing all configuration options.</span></span><br/> <span data-ttu-id="59dc5-200">Für jede Zeile in der ModuleConfiguration-Tabelle mit dem gleichen DefaultValue-Wert ist msmconfigurationitemskeynowaist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="59dc5-200">Every row in the ModuleConfiguration table with the same DefaultValue has the msmConfigurationItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="59dc5-201">Keine Zeilen verwenden den DefaultValue, weil das Authoring Tool einen Wert bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="59dc5-201">No rows use the DefaultValue because the authoring tool declined to provide a value.</span></span><br/> <span data-ttu-id="59dc5-202">Das Zusammenführungs Tool führt die Zeile zusammen, wenn eine der folgenden Bedingungen erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="59dc5-202">The merge tool merges the row if any of the following conditions are satisfied.</span></span><br/> <span data-ttu-id="59dc5-203">Das Merge-Tool findet eine beliebige Zeile, für die kein msmconfigitemskeynoverwaister festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="59dc5-203">The merge tool finds any row that does not have msmConfigItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="59dc5-204">, Wenn das Merge-Tool eine Zeile mithilfe von DefaultValue findet, weil das Authoring Tool einen Wert bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="59dc5-204">If the merge tool finds any row using DefaultValue because the authoring tool declined to provide a value.</span></span><br/> |
| <span data-ttu-id="59dc5-205">msmconfigurableoptionnonnullable</span><span class="sxs-lookup"><span data-stu-id="59dc5-205">msmConfigurableOptionNonNullable</span></span> | <span data-ttu-id="59dc5-206">2</span><span class="sxs-lookup"><span data-stu-id="59dc5-206">2</span></span>       | <span data-ttu-id="59dc5-207">0x00000002</span><span class="sxs-lookup"><span data-stu-id="59dc5-207">0x00000002</span></span>  | <span data-ttu-id="59dc5-208">Wenn dieses Attribut festgelegt ist, ist NULL keine gültige Antwort für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="59dc5-208">When this attribute is set, null is not a valid response for this item.</span></span> <span data-ttu-id="59dc5-209">Dieses Attribut hat keine Auswirkung auf [ganzzahlige Format Typen](integer-format-types.md) oder [Bitfield-Format Typen](bitfield-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="59dc5-209">This attribute has no effect for [Integer Format Types](integer-format-types.md) or [Bitfield Format Types](bitfield-format-types.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="59dc5-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>Display Name</span><span class="sxs-lookup"><span data-stu-id="59dc5-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span></span>
</dt> <dd>

<span data-ttu-id="59dc5-211">Diese Spalte enthält eine kurze Beschreibung dieses Elements, das vom Authoring Tool in der Benutzeroberfläche verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="59dc5-211">This column provides a short description of this item that the authoring tool may use in the user interface.</span></span> <span data-ttu-id="59dc5-212">Diese Spalte ist möglicherweise nicht lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="59dc5-212">This column may not be localized.</span></span> <span data-ttu-id="59dc5-213">Legen Sie diese Spalte auf NULL fest, damit das Modul angefordert wird, dass das Authoring Tool diese Eigenschaft nicht in der Benutzeroberfläche verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="59dc5-213">Set this column to null to have the module is request that the authoring tool not expose this property in the UI.</span></span> <span data-ttu-id="59dc5-214">Das Tool ignoriert möglicherweise den Wert in diesem Feld.</span><span class="sxs-lookup"><span data-stu-id="59dc5-214">The tool may disregard the value in this field.</span></span>

</dd> <dt>

<span data-ttu-id="59dc5-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59dc5-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="59dc5-216">Diese Spalte enthält eine Beschreibung dieses Elements, das vom Authoring Tool in Benutzeroberflächen Elementen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="59dc5-216">This column provides a description of this item that the authoring tool may use in UI elements.</span></span> <span data-ttu-id="59dc5-217">Diese Zeichenfolge kann durch die sprach Transformation des Moduls lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="59dc5-217">This string may be localized by the module's language transform.</span></span> <span data-ttu-id="59dc5-218">Diese Spalte kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="59dc5-218">This column may be null.</span></span>

</dd> <dt>

<span data-ttu-id="59dc5-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>Helplocation</span><span class="sxs-lookup"><span data-stu-id="59dc5-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span></span>
</dt> <dd>

<span data-ttu-id="59dc5-220">Diese Spalte enthält entweder den Namen einer Hilfedatei (ohne die Erweiterung ". chm") oder eine durch Semikolons getrennte Liste der Hilfe Namespaces.</span><span class="sxs-lookup"><span data-stu-id="59dc5-220">This column provides either the name of a help file (without the .chm extension) or a semicolon delimited list of help namespaces.</span></span> <span data-ttu-id="59dc5-221">Diese Spalte kann NULL sein, wenn keine Hilfe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="59dc5-221">This column can be null if no help is available.</span></span> <span data-ttu-id="59dc5-222">Diese Spalte darf nur NULL sein, wenn die HelpKeyword-Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="59dc5-222">This column can be null only if the HelpKeyword column is null.</span></span>

</dd> <dt>

<span data-ttu-id="59dc5-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="59dc5-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span></span>
</dt> <dd>

<span data-ttu-id="59dc5-224">Diese Spalte stellt ein Schlüsselwort in der Hilfedatei oder im Namespace aus der helplocation-Spalte bereit.</span><span class="sxs-lookup"><span data-stu-id="59dc5-224">This column provides a keyword into the help file or namespace from the HelpLocation column.</span></span> <span data-ttu-id="59dc5-225">Die Interpretation dieses Schlüssel Worts hängt von der helplocation-Spalte ab.</span><span class="sxs-lookup"><span data-stu-id="59dc5-225">The interpretation of this keyword depends on the HelpLocation column.</span></span> <span data-ttu-id="59dc5-226">Diese Spalte kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="59dc5-226">This column may be null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59dc5-227">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59dc5-227">Remarks</span></span>

<span data-ttu-id="59dc5-228">Die ModuleConfiguration-Tabelle wird von [konfigurierbaren Mergemodulen](configurable-merge-modules.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="59dc5-228">The ModuleConfiguration table is used by [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="59dc5-229">Mergemod.dll 2,0 oder höher ist erforderlich, um ein konfigurierbares Mergemodul zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="59dc5-229">Mergemod.dll 2.0 or later is required to create a configurable merge module.</span></span>

<span data-ttu-id="59dc5-230">Um die Kompatibilität mit älteren Versionen von Mergemod.dll sicherzustellen, sollten die Tabelle ModuleConfiguration und die [Tabelle ModuleSubstitution](modulesubstitution-table.md) der Tabelle [moduleignoretable](moduleignoretable-table.md) jedes Moduls hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="59dc5-230">To ensure compatibility with older versions of Mergemod.dll, the ModuleConfiguration table and [ModuleSubstitution table](modulesubstitution-table.md) should be added to the [ModuleIgnoreTable table](moduleignoretable-table.md) of every module.</span></span>

## <a name="validation"></a><span data-ttu-id="59dc5-231">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="59dc5-231">Validation</span></span>

<dl>

[<span data-ttu-id="59dc5-232">ICE03</span><span class="sxs-lookup"><span data-stu-id="59dc5-232">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="59dc5-233">ICE06</span><span class="sxs-lookup"><span data-stu-id="59dc5-233">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="59dc5-234">ICE25</span><span class="sxs-lookup"><span data-stu-id="59dc5-234">ICE25</span></span>](ice25.md)  
[<span data-ttu-id="59dc5-235">ICE45</span><span class="sxs-lookup"><span data-stu-id="59dc5-235">ICE45</span></span>](ice45.md)  
</dl>

 

 




