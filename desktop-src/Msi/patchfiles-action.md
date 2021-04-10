---
description: Mit der Aktion PATCHFILES wird die patchtabelle abgefragt, um zu bestimmen, welche Patches angewendet werden sollen. Die Aktion "PATCHFILES" führt auch das Byte Weise Patchen der Dateien aus.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Aktion "PATCHFILES"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865212"
---
# <a name="patchfiles-action"></a><span data-ttu-id="a07c5-104">Aktion "PATCHFILES"</span><span class="sxs-lookup"><span data-stu-id="a07c5-104">PatchFiles Action</span></span>

<span data-ttu-id="a07c5-105">Mit der Aktion PATCHFILES wird die [patchtabelle](patch-table.md) abgefragt, um zu bestimmen, welche Patches angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a07c5-105">The PatchFiles action queries the [Patch table](patch-table.md) to determine which patches are to be applied.</span></span> <span data-ttu-id="a07c5-106">Die Aktion "PATCHFILES" führt auch das Byte Weise Patchen der Dateien aus.</span><span class="sxs-lookup"><span data-stu-id="a07c5-106">The PatchFiles action also performs the byte-wise patching of the files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a07c5-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="a07c5-107">Sequence Restrictions</span></span>

<span data-ttu-id="a07c5-108">Wenn die Datei, die gepatcht werden soll, nicht installiert ist, muss die PATCHFILES-Aktion nach der [InstallFiles-Aktion](installfiles-action.md) erfolgen, mit der die Datei installiert wird.</span><span class="sxs-lookup"><span data-stu-id="a07c5-108">If the file that is to be patched is not installed, the PatchFiles action must come after the [InstallFiles action](installfiles-action.md) that installs the file.</span></span> <span data-ttu-id="a07c5-109">Zuvor installierte Dateien können an einem beliebigen Punkt in der Aktions Sequenz gepatcht werden.</span><span class="sxs-lookup"><span data-stu-id="a07c5-109">Previously installed files may be patched at any point in the action sequence.</span></span> <span data-ttu-id="a07c5-110">Die [duplicatefiles-Aktion](duplicatefiles-action.md) muss nach der PATCHFILES-Aktion erfolgen, um zu verhindern, dass die nicht gepatchte Version der Datei duplizieren.</span><span class="sxs-lookup"><span data-stu-id="a07c5-110">The [DuplicateFiles Action](duplicatefiles-action.md) must come after the PatchFiles action to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a07c5-111">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="a07c5-111">ActionData Messages</span></span>



| <span data-ttu-id="a07c5-112">Feld</span><span class="sxs-lookup"><span data-stu-id="a07c5-112">Field</span></span> | <span data-ttu-id="a07c5-113">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="a07c5-113">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="a07c5-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a07c5-114">\[1\]</span></span> | <span data-ttu-id="a07c5-115">Bezeichner der gepatchten Datei.</span><span class="sxs-lookup"><span data-stu-id="a07c5-115">Identifier of patched file.</span></span>                   |
| <span data-ttu-id="a07c5-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a07c5-116">\[2\]</span></span> | <span data-ttu-id="a07c5-117">Der Bezeichner des Verzeichnisses mit gepatchten Datei.</span><span class="sxs-lookup"><span data-stu-id="a07c5-117">Identifier of directory holding patched file.</span></span> |
| <span data-ttu-id="a07c5-118">\[3\]</span><span class="sxs-lookup"><span data-stu-id="a07c5-118">\[3\]</span></span> | <span data-ttu-id="a07c5-119">Größe des Patches in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a07c5-119">Size of patch in bytes.</span></span>                       |



 

 

 



