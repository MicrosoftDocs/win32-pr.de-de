---
description: Die drlocator-Tabelle enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis durchsuchen der Verzeichnisstruktur zu finden.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Drlocator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346998"
---
# <a name="drlocator-table"></a><span data-ttu-id="003e8-103">Drlocator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="003e8-103">DrLocator Table</span></span>

<span data-ttu-id="003e8-104">Die drlocator-Tabelle enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis durchsuchen der Verzeichnisstruktur zu finden.</span><span class="sxs-lookup"><span data-stu-id="003e8-104">The DrLocator table holds the information needed to find a file or directory by searching the directory tree.</span></span>

<span data-ttu-id="003e8-105">Die drlocator-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="003e8-105">The DrLocator table has the following columns.</span></span>



| <span data-ttu-id="003e8-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="003e8-106">Column</span></span>      | <span data-ttu-id="003e8-107">Typ</span><span class="sxs-lookup"><span data-stu-id="003e8-107">Type</span></span>                         | <span data-ttu-id="003e8-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="003e8-108">Key</span></span> | <span data-ttu-id="003e8-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="003e8-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="003e8-110">Signatur\_</span><span class="sxs-lookup"><span data-stu-id="003e8-110">Signature\_</span></span> | [<span data-ttu-id="003e8-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="003e8-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="003e8-112">J</span><span class="sxs-lookup"><span data-stu-id="003e8-112">Y</span></span>   | <span data-ttu-id="003e8-113">N</span><span class="sxs-lookup"><span data-stu-id="003e8-113">N</span></span>        |
| <span data-ttu-id="003e8-114">Parent</span><span class="sxs-lookup"><span data-stu-id="003e8-114">Parent</span></span>      | [<span data-ttu-id="003e8-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="003e8-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="003e8-116">J</span><span class="sxs-lookup"><span data-stu-id="003e8-116">Y</span></span>   | <span data-ttu-id="003e8-117">J</span><span class="sxs-lookup"><span data-stu-id="003e8-117">Y</span></span>        |
| <span data-ttu-id="003e8-118">Pfad</span><span class="sxs-lookup"><span data-stu-id="003e8-118">Path</span></span>        | [<span data-ttu-id="003e8-119">Anypath</span><span class="sxs-lookup"><span data-stu-id="003e8-119">AnyPath</span></span>](anypath.md)       | <span data-ttu-id="003e8-120">J</span><span class="sxs-lookup"><span data-stu-id="003e8-120">Y</span></span>   | <span data-ttu-id="003e8-121">J</span><span class="sxs-lookup"><span data-stu-id="003e8-121">Y</span></span>        |
| <span data-ttu-id="003e8-122">Tiefe</span><span class="sxs-lookup"><span data-stu-id="003e8-122">Depth</span></span>       | [<span data-ttu-id="003e8-123">Integer</span><span class="sxs-lookup"><span data-stu-id="003e8-123">Integer</span></span>](integer.md)       | <span data-ttu-id="003e8-124">N</span><span class="sxs-lookup"><span data-stu-id="003e8-124">N</span></span>   | <span data-ttu-id="003e8-125">J</span><span class="sxs-lookup"><span data-stu-id="003e8-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="003e8-126">Spalten</span><span class="sxs-lookup"><span data-stu-id="003e8-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="003e8-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_</span><span class="sxs-lookup"><span data-stu-id="003e8-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="003e8-128">Die Signatur \_ Spalte ist ein externer Schlüssel für die erste Spalte der [Signatur Tabelle](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="003e8-128">The Signature\_ column is an external key to the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="003e8-129">Dieses Feld kann eine eindeutige Datei Signatur darstellen, die in der Signatur Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="003e8-129">This field may represent a unique file signature listed in the Signature table.</span></span> <span data-ttu-id="003e8-130">Wenn der Wert in dieser Spalte in der Signatur Tabelle nicht vorhanden ist, wird angenommen, dass es sich bei der Suche um ein Verzeichnis handelt, auf das von der drlocator-Tabelle verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="003e8-130">If the value in this column is absent from the Signature table, then the search is assumed to be for a directory pointed to by the DrLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="003e8-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Übergeordneten</span><span class="sxs-lookup"><span data-stu-id="003e8-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Parent</span></span>
</dt> <dd>

<span data-ttu-id="003e8-132">Diese Spalte ist die Signatur des übergeordneten Verzeichnisses der Datei oder des Verzeichnisses in der \_ Spalte Signatur.</span><span class="sxs-lookup"><span data-stu-id="003e8-132">This column is the signature of the parent directory of the file or directory in the Signature\_ column.</span></span> <span data-ttu-id="003e8-133">Wenn dieses Feld NULL ist und die Path-Spalte nicht zu einem vollständigen Pfad erweitert wird, werden alle Festplattenlaufwerke des Benutzer Systems unter Verwendung des Pfads durchsucht.</span><span class="sxs-lookup"><span data-stu-id="003e8-133">If this field is null, and the Path column does not expand to a full path, then all the fixed drives of the user's system are searched by using the Path.</span></span>

<span data-ttu-id="003e8-134">Dieses Feld ist ein Schlüssel in einer der folgenden Tabellen: die Tabellen [reglocator](reglocator-table.md), [inilocator](inilocator-table.md), [complocator](complocator-table.md)oder drlocator.</span><span class="sxs-lookup"><span data-stu-id="003e8-134">This field is a key into one of the following tables: the [RegLocator](reglocator-table.md), the [IniLocator](inilocator-table.md), the [CompLocator](complocator-table.md), or the DrLocator tables.</span></span>

</dd> <dt>

<span data-ttu-id="003e8-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>ADS</span><span class="sxs-lookup"><span data-stu-id="003e8-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="003e8-136">Die Path-Spalte enthält den Pfad auf dem System des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="003e8-136">The Path column contains the path on the user's system.</span></span> <span data-ttu-id="003e8-137">Dies ist entweder ein vollständiger Pfad oder ein relativer unter Pfad unterhalb des Verzeichnisses, das in der übergeordneten Spalte angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="003e8-137">This is a either a full path or a relative subpath below the directory specified in the Parent column.</span></span> <span data-ttu-id="003e8-138">Weitere Informationen finden Sie unter Einschränkungen für den [anypath](anypath.md) -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="003e8-138">See the restrictions on the [AnyPath](anypath.md) data type.</span></span>

</dd> <dt>

<span data-ttu-id="003e8-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Eingeh</span><span class="sxs-lookup"><span data-stu-id="003e8-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Depth</span></span>
</dt> <dd>

<span data-ttu-id="003e8-140">Die Tiefe unterhalb des Pfads, den das Installationsprogramm nach der in der Spalte Signatur angegebenen Datei oder dem Verzeichnis durchsucht \_ .</span><span class="sxs-lookup"><span data-stu-id="003e8-140">The depth below the path that the installer searches for the file or directory specified in the Signature\_ column.</span></span> <span data-ttu-id="003e8-141">Der im Feld Tiefe verwendete Wert basiert auf 0 (null).</span><span class="sxs-lookup"><span data-stu-id="003e8-141">The value used in the Depth field is based on zero.</span></span> <span data-ttu-id="003e8-142">Wenn das Feld Pfad z. b. c:/Program Files/bin ist, muss die Spalte Tiefe auf 0 oder höher festgelegt werden, um eine Datei im Ordner bin zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="003e8-142">For example, if the Path field is c:/Program Files/bin, the Depth column must be set to 0 or greater, to detect a file located inside the folder bin.</span></span> <span data-ttu-id="003e8-143">Wenn das tiefen Feld leer ist, wird davon ausgegangen, dass die Tiefe 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="003e8-143">If the Depth field is empty, the depth is assumed to be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="003e8-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="003e8-144">Remarks</span></span>

<span data-ttu-id="003e8-145">Diese Tabelle wird mit der [AppSearch-Tabelle](appsearch-table.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="003e8-145">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="003e8-146">Die Spalten dieser Tabelle sind im Allgemeinen nicht lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="003e8-146">This table's columns are generally not localized.</span></span> <span data-ttu-id="003e8-147">Wenn ein Autor eine Suche nach Produkten in mehreren Sprachen beschließt, muss für jede Sprache ein separater Eintrag in der Tabelle enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="003e8-147">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="003e8-148">Weitere Informationen finden Sie [untersuchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="003e8-148">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="003e8-149">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="003e8-149">Validation</span></span>

<dl>

[<span data-ttu-id="003e8-150">ICE03</span><span class="sxs-lookup"><span data-stu-id="003e8-150">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="003e8-151">ICE06</span><span class="sxs-lookup"><span data-stu-id="003e8-151">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="003e8-152">ICE46</span><span class="sxs-lookup"><span data-stu-id="003e8-152">ICE46</span></span>](ice46.md)  
</dl>

 

 



