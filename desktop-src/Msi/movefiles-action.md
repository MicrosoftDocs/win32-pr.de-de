---
description: Durch die Aktion "Aktion" werden vorhandene Dateien auf dem Computer des Benutzers lokalisiert und an einen neuen Speicherort verschoben oder kopiert.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Aktion "muvefiles"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868864"
---
# <a name="movefiles-action"></a><span data-ttu-id="3ff74-103">Aktion "muvefiles"</span><span class="sxs-lookup"><span data-stu-id="3ff74-103">MoveFiles Action</span></span>

<span data-ttu-id="3ff74-104">Durch die Aktion "Aktion" werden vorhandene Dateien auf dem Computer des Benutzers lokalisiert und an einen neuen Speicherort verschoben oder kopiert.</span><span class="sxs-lookup"><span data-stu-id="3ff74-104">The MoveFiles action locates existing files on the user's computer and moves or copies those files to a new location.</span></span> <span data-ttu-id="3ff74-105">Mit der Aktion "muvefiles" wird die [Tabelle "muvefile](movefile-table.md) " abgefragt und die dort angegebenen Dateien verschoben, wenn die mit den Einträgen verknüpfte Komponente für die lokale Installation angegeben ist oder von der Quelle ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ff74-105">The MoveFiles action queries the [MoveFile table](movefile-table.md) and moves files specified there if the component linked to the entries is specified to be install locally or is being run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3ff74-106">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="3ff74-106">Sequence Restrictions</span></span>

<span data-ttu-id="3ff74-107">Die Aktion "muvefiles" muss nach der [InstallValidate](installvalidate-action.md) -Aktion und vor der [InstallFiles](installfiles-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="3ff74-107">The MoveFiles action must come after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3ff74-108">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="3ff74-108">ActionData Messages</span></span>



| <span data-ttu-id="3ff74-109">Feld</span><span class="sxs-lookup"><span data-stu-id="3ff74-109">Field</span></span> | <span data-ttu-id="3ff74-110">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="3ff74-110">Description of action data</span></span>                  |
|-------|---------------------------------------------|
| <span data-ttu-id="3ff74-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="3ff74-111">\[1\]</span></span> | <span data-ttu-id="3ff74-112">Der Bezeichner der verschoden Datei.</span><span class="sxs-lookup"><span data-stu-id="3ff74-112">Identifier of moved file.</span></span>                   |
| <span data-ttu-id="3ff74-113">\[6\]</span><span class="sxs-lookup"><span data-stu-id="3ff74-113">\[6\]</span></span> | <span data-ttu-id="3ff74-114">Größe der installierten Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3ff74-114">Size of installed file in bytes.</span></span>            |
| <span data-ttu-id="3ff74-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="3ff74-115">\[9\]</span></span> | <span data-ttu-id="3ff74-116">Bezeichner des Verzeichnisses, das die verschoderte Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="3ff74-116">Identifier of directory holding moved file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3ff74-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ff74-117">Remarks</span></span>

<span data-ttu-id="3ff74-118">Die Tabelle "muvefiles" enthält eine Spalte mit dem Namen "Options", die die zu verschiebenden oder zu kopierenden Quelldateien angibt.</span><span class="sxs-lookup"><span data-stu-id="3ff74-118">The MoveFiles table contain a column named "options" which specifies the source files to be moved or copied.</span></span> <span data-ttu-id="3ff74-119">Eine verschoderte Quelldatei wird gelöscht, nachdem Sie an einen neuen Speicherort kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3ff74-119">A moved source file is deleted after it has been copied to a new location.</span></span> <span data-ttu-id="3ff74-120">Die genaue Syntax finden Sie in der [Tabelle "muvefile](movefile-table.md)".</span><span class="sxs-lookup"><span data-stu-id="3ff74-120">For the exact syntax, see the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="3ff74-121">Die Spalten sourcefolder und destfolder der Tabelle "muvefile" sind Eigenschaftsnamen, deren Werte in voll qualifizierte Pfade aufgelöst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3ff74-121">The SourceFolder and DestFolder columns of the MoveFile table are property names whose values are expected to resolve to fully qualified paths.</span></span> <span data-ttu-id="3ff74-122">Diese Eigenschaften können alle Verzeichniseinträge in der [Verzeichnis](directory-table.md) Tabelle, jede vordefinierte Ordner Eigenschaft (z. b.[**FavoritesFolder**](favoritesfolder.md)) oder eine Eigenschaft sein, die von einem beliebigen Eintrag in der [AppSearch](appsearch-table.md) -Tabelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3ff74-122">These properties can be any of the directory entries in the [Directory](directory-table.md) table, any predefined folder property ([**FavoritesFolder**](favoritesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="3ff74-123">Diese Eigenschaften können einen vollständigen Pfad enthalten, der den Dateinamen für eine bestimmte Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="3ff74-123">These properties may contain a full path containing the file name to a specific file.</span></span> <span data-ttu-id="3ff74-124">Beispielsweise kann die Tabelle "AppSearch" erstellt werden, um nach einer bestimmten Datei zu suchen und eine Eigenschaft auf den vollständigen Pfad zu dieser Datei festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3ff74-124">For example, the AppSearch table can be authored to search for a particular file and set a property to the full path to that file.</span></span> <span data-ttu-id="3ff74-125">In diesem Beispiel kann die Spalte SourceName in der Tabelle "muvefile" leer gelassen werden, um anzugeben, dass der Wert in der sourcefolder-Eigenschaft einen vollständigen Dateipfad enthält.</span><span class="sxs-lookup"><span data-stu-id="3ff74-125">In this example, the SourceName column in the MoveFile table can be left blank to indicate that the value in the SourceFolder property contains a full file path.</span></span> <span data-ttu-id="3ff74-126">Das Semikolon ist das Listen Trennzeichen für Transformationen, Quellen und Patches und sollte nicht in Dateinamen oder Pfaden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ff74-126">The semicolon is the list delimiter for transforms, sources, and patches and should not be used in file names or paths.</span></span>

<span data-ttu-id="3ff74-127">Die Aktion "muvefiles" wirkt sich nicht auf Einträge in der "muvefile"-Tabelle aus, in der die Eigenschaft "sourcefolder" oder "destfolder" nicht zu einem vollständigen Pfad ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="3ff74-127">The MoveFiles action does not act on entries in the MoveFile table in which either the SourceFolder or DestFolder property does not evaluate to a full path.</span></span>

<span data-ttu-id="3ff74-128">Die Aktion movefiles versucht, alle Dateien im Quellverzeichnis zu verschieben oder zu kopieren, die dem in der Spalte SourceName der Tabelle movefiles angegebenen Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3ff74-128">The MoveFiles action attempts to move or copy all files in the source directory that match the name given in the SourceName column of the MoveFiles table.</span></span> <span data-ttu-id="3ff74-129">Der Name in der Spalte SourceName kann entweder oder enthalten \* ?</span><span class="sxs-lookup"><span data-stu-id="3ff74-129">The name in the SourceName column can include either the \* or ?</span></span> <span data-ttu-id="3ff74-130">Platzhalter, die es ermöglichen, eine Gruppe von Dateien zu verschieben oder zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="3ff74-130">wildcards which allow a group of files to be moved or copied.</span></span> <span data-ttu-id="3ff74-131">Beispielsweise kann die Spalte SourceName einen Eintrag von " \* . xls" enthalten, und mit der Aktion "muvefiles" wird jede Microsoft Excel-Arbeitsmappe aus dem Quellverzeichnis in das Ziel verschoben oder kopiert.</span><span class="sxs-lookup"><span data-stu-id="3ff74-131">For example, the SourceName column may contain an entry of "\*.xls" and the MoveFiles action moves or copies every Microsoft Excel workbook from the source directory to the destination.</span></span>

<span data-ttu-id="3ff74-132">Der Name, der an die Zieldatei übergeben werden soll, kann in der Spalte "destname" der Tabelle "muvefile" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3ff74-132">The name to be given to the destination file can be specified in the DestName column of the MoveFile table.</span></span> <span data-ttu-id="3ff74-133">Der Name der Ziel Datei behält den Quell Dateinamen bei, wenn diese Spalte leer bleibt.</span><span class="sxs-lookup"><span data-stu-id="3ff74-133">The destination file name retains the source file name if this column is left blank.</span></span>

<span data-ttu-id="3ff74-134">Wenn ein " \* "-Platzhalter in die Spalte "SourceName" der [Tabelle "muvefile](movefile-table.md) " eingegeben wird und in der Spalte "destname" ein Ziel Dateiname angegeben ist, behalten alle verschobener oder kopierten Dateien die Namen in den Quellen bei.</span><span class="sxs-lookup"><span data-stu-id="3ff74-134">If a "\*" wildcard is entered in the SourceName column of the [MoveFile table](movefile-table.md) and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="3ff74-135">Dateien, die von der Aktion "muvefiles" verschoben oder kopiert werden, werden bei der Installation des Produkts nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3ff74-135">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

 

 



