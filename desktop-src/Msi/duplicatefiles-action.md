---
description: Die duplicatefiles-Aktion dupliziert Dateien, die von der InstallFiles-Aktion installiert wurden. Die doppelten Dateien können in dasselbe Verzeichnis mit einem anderen Namen oder in ein anderes Verzeichnis mit dem ursprünglichen Namen kopiert werden.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Duplicatefiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f6bbd4716beb227dea348826bc302e2f4ba2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360604"
---
# <a name="duplicatefiles-action"></a><span data-ttu-id="d9225-104">Duplicatefiles-Aktion</span><span class="sxs-lookup"><span data-stu-id="d9225-104">DuplicateFiles Action</span></span>

<span data-ttu-id="d9225-105">Die duplicatefiles-Aktion dupliziert Dateien, die von der [InstallFiles](installfiles-action.md) -Aktion installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d9225-105">The DuplicateFiles action duplicates files installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="d9225-106">Die doppelten Dateien können in dasselbe Verzeichnis mit einem anderen Namen oder in ein anderes Verzeichnis mit dem ursprünglichen Namen kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="d9225-106">The duplicate files can be copied to the same directory with a different name or to a different directory with the original name.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d9225-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d9225-107">Sequence Restrictions</span></span>

<span data-ttu-id="d9225-108">Die Aktion "duplicatefiles" muss nach der [Aktion "InstallFiles](installfiles-action.md)" erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d9225-108">The DuplicateFiles action must come after the [InstallFiles action](installfiles-action.md).</span></span> <span data-ttu-id="d9225-109">Die duplicatefiles-Aktion muss auch nach der [PATCHFILES-Aktion](patchfiles-action.md) erfolgen, um zu verhindern, dass die nicht gepatchte Version der Datei duplizieren.</span><span class="sxs-lookup"><span data-stu-id="d9225-109">The DuplicateFiles Action must also come after the [PatchFiles action](patchfiles-action.md) to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d9225-110">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="d9225-110">ActionData Messages</span></span>



| <span data-ttu-id="d9225-111">Feld</span><span class="sxs-lookup"><span data-stu-id="d9225-111">Field</span></span> | <span data-ttu-id="d9225-112">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="d9225-112">Description of action data</span></span>                       |
|-------|--------------------------------------------------|
| <span data-ttu-id="d9225-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d9225-113">\[1\]</span></span> | <span data-ttu-id="d9225-114">Bezeichner der duplizierten Datei.</span><span class="sxs-lookup"><span data-stu-id="d9225-114">Identifier of duplicated file.</span></span>                   |
| <span data-ttu-id="d9225-115">\[6\]</span><span class="sxs-lookup"><span data-stu-id="d9225-115">\[6\]</span></span> | <span data-ttu-id="d9225-116">Größe der duplizierten Datei.</span><span class="sxs-lookup"><span data-stu-id="d9225-116">Size of duplicated file.</span></span>                         |
| <span data-ttu-id="d9225-117">\[9\]</span><span class="sxs-lookup"><span data-stu-id="d9225-117">\[9\]</span></span> | <span data-ttu-id="d9225-118">Der Bezeichner des Verzeichnisses, das die doppelte Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="d9225-118">Identifier of directory holding duplicated file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d9225-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9225-119">Remarks</span></span>

<span data-ttu-id="d9225-120">Die duplicatefiles-Aktion verarbeitet einen [duplicatefile-Tabellen](duplicatefile-table.md) Eintrag nur dann, wenn die mit diesem Eintrag verknüpfte Komponente lokal installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d9225-120">The DuplicateFiles action processes a [DuplicateFile table](duplicatefile-table.md) entry only if the component linked to that entry is being installed locally.</span></span> <span data-ttu-id="d9225-121">Weitere Informationen finden Sie unter [Component Table](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d9225-121">For more information, see [Component table](component-table.md).</span></span>

<span data-ttu-id="d9225-122">Die Zeichenfolge im Feld "destfolder" ist ein Eigenschaftsname, dessen Wert in einen voll qualifizierten Pfad aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9225-122">The string in the DestFolder field is a property name whose value is expected to resolve to a fully qualified path.</span></span> <span data-ttu-id="d9225-123">Diese Eigenschaft kann entweder ein beliebiger Verzeichniseintrag in der [Verzeichnis](directory-table.md) Tabelle, eine vordefinierte Ordner Eigenschaft (z. b.[**CommonFilesFolder**](commonfilesfolder.md)) oder eine Eigenschaft sein, die von einem beliebigen Eintrag in der [AppSearch](appsearch-table.md) -Tabelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d9225-123">This property can either be any of the directory entries in the [Directory](directory-table.md) table, any pre-defined folder property ([**CommonFilesFolder**](commonfilesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="d9225-124">Wenn die **destfolder** -Eigenschaft nicht als gültiger Pfad ausgewertet wird, führt die duplicatefiles-Aktion für diesen Eintrag keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="d9225-124">If the **DestFolder** property does not evaluate to a valid path the DuplicateFiles action does nothing for that entry.</span></span>

<span data-ttu-id="d9225-125">Wenn der Name der Zieldatei in der Spalte destname der duplicatefile-Tabelle leer bleibt, entspricht der Name der Ziel Datei dem ursprünglichen Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="d9225-125">If the name of the destination file in the DestName column of the DuplicateFile table is left blank, the destination file name will be the same as the original file name.</span></span>

<span data-ttu-id="d9225-126">Dateien, die von der duplicatefiles-Aktion installiert werden, werden bei Bedarf von der Aktion " [RemoveDuplicateFiles](removeduplicatefiles-action.md) " entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9225-126">Files installed by the DuplicateFiles action are removed by the [RemoveDuplicateFiles](removeduplicatefiles-action.md) action when appropriate.</span></span>

 

 



