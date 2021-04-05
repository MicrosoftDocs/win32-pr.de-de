---
description: Durch die Aktion RemoveDuplicateFiles werden Dateien gelöscht, die von der duplicatefiles-Aktion installiert wurden.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: RemoveDuplicateFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751121"
---
# <a name="removeduplicatefiles-action"></a><span data-ttu-id="9524a-103">RemoveDuplicateFiles-Aktion</span><span class="sxs-lookup"><span data-stu-id="9524a-103">RemoveDuplicateFiles Action</span></span>

<span data-ttu-id="9524a-104">Durch die Aktion RemoveDuplicateFiles werden Dateien gelöscht, die von der [duplicatefiles](duplicatefiles-action.md) -Aktion installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9524a-104">The RemoveDuplicateFiles action deletes files installed by the [DuplicateFiles](duplicatefiles-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9524a-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="9524a-105">Sequence Restrictions</span></span>

<span data-ttu-id="9524a-106">Die Aktion RemoveDuplicateFiles muss nach der [InstallValidate](installvalidate-action.md) -Aktion und vor der [InstallFiles](installfiles-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="9524a-106">The RemoveDuplicateFiles action must occur after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9524a-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="9524a-107">ActionData Messages</span></span>



| <span data-ttu-id="9524a-108">Feld</span><span class="sxs-lookup"><span data-stu-id="9524a-108">Field</span></span> | <span data-ttu-id="9524a-109">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="9524a-109">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="9524a-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9524a-110">\[1\]</span></span> | <span data-ttu-id="9524a-111">Bezeichner der entfernten Datei.</span><span class="sxs-lookup"><span data-stu-id="9524a-111">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="9524a-112">\[9\]</span><span class="sxs-lookup"><span data-stu-id="9524a-112">\[9\]</span></span> | <span data-ttu-id="9524a-113">Der Bezeichner des Verzeichnisses, das die entfernte Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="9524a-113">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9524a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9524a-114">Remarks</span></span>

<span data-ttu-id="9524a-115">Zum Löschen einer Datei, die mit der [Aktion "duplicatefiles](duplicatefiles-action.md) " mithilfe der Aktion "RemoveDuplicateFiles" dupliziert wurde, muss die Komponente, die dem Eintrag der Datei in der duplicatefile-Tabelle zugeordnet ist, zum Entfernen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="9524a-115">To delete a file duplicated with the [DuplicateFiles action](duplicatefiles-action.md) using the RemoveDuplicateFiles action, the component associated with the file's entry in the DuplicateFile table must be selected for removal.</span></span>

<span data-ttu-id="9524a-116">Verwenden Sie die Spalte destfolder der [duplicatefile-Tabelle](duplicatefile-table.md) , um den Eigenschaftsnamen anzugeben, dessen Wert den Zielordner angibt.</span><span class="sxs-lookup"><span data-stu-id="9524a-116">Use the DestFolder column of the [DuplicateFile table](duplicatefile-table.md) to specify the property name whose value identifies the destination folder.</span></span>

 

 



