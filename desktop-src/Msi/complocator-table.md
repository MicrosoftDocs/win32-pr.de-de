---
description: Die complocator-Tabelle enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis zu finden, das die installerkonfigurationsdaten verwendet.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Complocator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530239"
---
# <a name="complocator-table"></a><span data-ttu-id="9e9c5-103">Complocator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="9e9c5-103">CompLocator Table</span></span>

<span data-ttu-id="9e9c5-104">Die complocator-Tabelle enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis zu finden, das die installerkonfigurationsdaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-104">The CompLocator Table contains the information needed to find a file or directory that is using the installer configuration data.</span></span>

<span data-ttu-id="9e9c5-105">Die complocator-Tabelle enthält die folgenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-105">The CompLocator table contains the following information.</span></span>



| <span data-ttu-id="9e9c5-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="9e9c5-106">Column</span></span>      | <span data-ttu-id="9e9c5-107">Typ</span><span class="sxs-lookup"><span data-stu-id="9e9c5-107">Type</span></span>                         | <span data-ttu-id="9e9c5-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="9e9c5-108">Key</span></span> | <span data-ttu-id="9e9c5-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="9e9c5-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="9e9c5-110">Signatur\_</span><span class="sxs-lookup"><span data-stu-id="9e9c5-110">Signature\_</span></span> | [<span data-ttu-id="9e9c5-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="9e9c5-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="9e9c5-112">J</span><span class="sxs-lookup"><span data-stu-id="9e9c5-112">Y</span></span>   | <span data-ttu-id="9e9c5-113">N</span><span class="sxs-lookup"><span data-stu-id="9e9c5-113">N</span></span>        |
| <span data-ttu-id="9e9c5-114">ComponentID</span><span class="sxs-lookup"><span data-stu-id="9e9c5-114">ComponentId</span></span> | [<span data-ttu-id="9e9c5-115">GUID</span><span class="sxs-lookup"><span data-stu-id="9e9c5-115">GUID</span></span>](guid.md)             | <span data-ttu-id="9e9c5-116">N</span><span class="sxs-lookup"><span data-stu-id="9e9c5-116">N</span></span>   | <span data-ttu-id="9e9c5-117">N</span><span class="sxs-lookup"><span data-stu-id="9e9c5-117">N</span></span>        |
| <span data-ttu-id="9e9c5-118">type</span><span class="sxs-lookup"><span data-stu-id="9e9c5-118">Type</span></span>        | [<span data-ttu-id="9e9c5-119">Integer</span><span class="sxs-lookup"><span data-stu-id="9e9c5-119">Integer</span></span>](integer.md)       | <span data-ttu-id="9e9c5-120">N</span><span class="sxs-lookup"><span data-stu-id="9e9c5-120">N</span></span>   | <span data-ttu-id="9e9c5-121">J</span><span class="sxs-lookup"><span data-stu-id="9e9c5-121">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="9e9c5-122">Spalten Informationen</span><span class="sxs-lookup"><span data-stu-id="9e9c5-122">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="9e9c5-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_</span><span class="sxs-lookup"><span data-stu-id="9e9c5-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="9e9c5-124">Diese Spalte stellt eine eindeutige Datei Signatur dar und ist auch der externe Schlüssel in der [Signatur Tabelle](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="9e9c5-124">This column represents a unique file signature and is also the external key into the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="9e9c5-125">Wenn der Schlüssel in der Signatur Tabelle nicht vorhanden ist, wird davon ausgegangen, dass es sich bei der Suche um das vorhanden sein eines Verzeichnisses handelt, auf das von der complocator-Tabelle verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-125">If the key is absent from the Signature Table, the search is assumed to be for the presence of a directory pointed to by the CompLocator Table.</span></span>

</dd> <dt>

<span data-ttu-id="9e9c5-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentID</span><span class="sxs-lookup"><span data-stu-id="9e9c5-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="9e9c5-127">Die Komponenten-ID der Komponente, deren Schlüssel Pfad für die Suche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-127">The component ID of the component whose key path is to be used for the search.</span></span> <span data-ttu-id="9e9c5-128">Dies sollte die GUID einer Komponente sein, die im Feld "ComponentId" der [Komponenten Tabelle](component-table.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-128">This should be the GUID of a component that appears in the ComponentId field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="9e9c5-129">Dies kann die Komponenten-ID einer Komponente sein, die zu einem anderen Produkt gehört, das auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-129">It may be the component ID of a component belonging to another product installed on the computer.</span></span> <span data-ttu-id="9e9c5-130">Dies sollte nicht der GUID einer veröffentlichten Komponente sein, die im Feld "ComponentId" der [Tabelle "PublishComponent](publishcomponent-table.md)" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-130">It should not be the GUID of a published component appearing in the ComponentId field of the [PublishComponent Table](publishcomponent-table.md).</span></span>

<span data-ttu-id="9e9c5-131">Wechseln Sie zum Installationspaket des Produkts, um den GUID-Wert der Komponenten-ID für eine Datei zu ermitteln, die von einem anderen Produkt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-131">To find the component ID GUID value for a file installed by another product, go to the installation package of the product.</span></span> <span data-ttu-id="9e9c5-132">Wechseln Sie zur [Dateitabelle](file-table.md) , und suchen Sie die Zeile, die den Datei Bezeichner für die Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-132">Go to the [File Table](file-table.md) and find the row that contains the file identifier for the file.</span></span> <span data-ttu-id="9e9c5-133">Die Komponenten \_ Spalte dieser Zeile enthält den Komponenten Bezeichner für die Komponente, mit der die Datei gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-133">The Component\_ column of this row contains the component identifier for the component that controls the file.</span></span> <span data-ttu-id="9e9c5-134">Wechseln Sie zur [Komponenten Tabelle](component-table.md) , und suchen Sie die Zeile, die diesen Komponenten Bezeichner enthält, in der Spalte Komponente.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-134">Go to the [Component table](component-table.md) and find the row that contains this component identifier in the Component column.</span></span> <span data-ttu-id="9e9c5-135">Die Spalte ComponentID dieser Zeile enthält die Komponenten-ID-GUID.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-135">The ComponentId column of this row contains the component ID GUID.</span></span>

</dd> <dt>

<span data-ttu-id="9e9c5-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte</span><span class="sxs-lookup"><span data-stu-id="9e9c5-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="9e9c5-137">Ein boolescher Wert, der bestimmt, ob der Schlüssel Pfad der Komponente ein Dateiname oder ein Verzeichnis Speicherort ist.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-137">A Boolean value that determines if the key path of the component is a file name or a directory location.</span></span>

<span data-ttu-id="9e9c5-138">In der folgenden Tabelle sind gültige Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-138">The following table lists valid values.</span></span> <span data-ttu-id="9e9c5-139">Wenn nicht vorhanden, wird Type auf 1 (eins) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-139">If absent, Type is set to be 1 (one).</span></span>



| <span data-ttu-id="9e9c5-140">Konstante</span><span class="sxs-lookup"><span data-stu-id="9e9c5-140">Constant</span></span>                      | <span data-ttu-id="9e9c5-141">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="9e9c5-141">Hexadecimal</span></span> | <span data-ttu-id="9e9c5-142">Decimal</span><span class="sxs-lookup"><span data-stu-id="9e9c5-142">Decimal</span></span> | <span data-ttu-id="9e9c5-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e9c5-143">Description</span></span>              |
|-------------------------------|-------------|---------|--------------------------|
| <span data-ttu-id="9e9c5-144">**msidbloprojekttypedirectory**</span><span class="sxs-lookup"><span data-stu-id="9e9c5-144">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="9e9c5-145">0x000</span><span class="sxs-lookup"><span data-stu-id="9e9c5-145">0x000</span></span>       | <span data-ttu-id="9e9c5-146">0</span><span class="sxs-lookup"><span data-stu-id="9e9c5-146">0</span></span>       | <span data-ttu-id="9e9c5-147">Der Schlüssel Pfad ist ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-147">Key path is a directory.</span></span> |
| <span data-ttu-id="9e9c5-148">**msidblo-typefilename**</span><span class="sxs-lookup"><span data-stu-id="9e9c5-148">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="9e9c5-149">0x001</span><span class="sxs-lookup"><span data-stu-id="9e9c5-149">0x001</span></span>       | <span data-ttu-id="9e9c5-150">1</span><span class="sxs-lookup"><span data-stu-id="9e9c5-150">1</span></span>       | <span data-ttu-id="9e9c5-151">Der Schlüssel Pfad ist ein Dateiname.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-151">Key path is a file name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e9c5-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e9c5-152">Remarks</span></span>

<span data-ttu-id="9e9c5-153">Diese Tabelle wird mit der [AppSearch-Tabelle](appsearch-table.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-153">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="9e9c5-154">In der Regel werden die Spalten in dieser Tabelle nicht lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-154">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="9e9c5-155">Wenn ein Autor eine Suche nach Produkten in mehreren Sprachen beschließt, kann in der Tabelle für jede Sprache ein separater Eintrag enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-155">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="9e9c5-156">Weitere Informationen finden Sie unter [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="9e9c5-156">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="9e9c5-157">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="9e9c5-157">Validation</span></span>

<dl>

[<span data-ttu-id="9e9c5-158">ICE03</span><span class="sxs-lookup"><span data-stu-id="9e9c5-158">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9e9c5-159">ICE06</span><span class="sxs-lookup"><span data-stu-id="9e9c5-159">ICE06</span></span>](ice06.md)  
</dl>

 

 



