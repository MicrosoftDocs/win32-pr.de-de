---
description: Die Tabelle "| atefolder" enthält Verweise auf Ordner, die für eine bestimmte Komponente explizit erstellt werden müssen.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: Tabelle "Buildordner"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217177"
---
# <a name="createfolder-table"></a><span data-ttu-id="ed600-103">Tabelle "Buildordner"</span><span class="sxs-lookup"><span data-stu-id="ed600-103">CreateFolder Table</span></span>

<span data-ttu-id="ed600-104">Die Tabelle "| atefolder" enthält Verweise auf Ordner, die für eine bestimmte Komponente explizit erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ed600-104">The CreateFolder table contains references to folders that need to be created explicitly for a particular component.</span></span>

<span data-ttu-id="ed600-105">Die Tabelle "| atefolder" weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="ed600-105">The CreateFolder table has the following columns.</span></span>



| <span data-ttu-id="ed600-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="ed600-106">Column</span></span>      | <span data-ttu-id="ed600-107">Typ</span><span class="sxs-lookup"><span data-stu-id="ed600-107">Type</span></span>                         | <span data-ttu-id="ed600-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="ed600-108">Key</span></span> | <span data-ttu-id="ed600-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="ed600-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="ed600-110">Verzeichnis\_</span><span class="sxs-lookup"><span data-stu-id="ed600-110">Directory\_</span></span> | [<span data-ttu-id="ed600-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ed600-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="ed600-112">J</span><span class="sxs-lookup"><span data-stu-id="ed600-112">Y</span></span>   | <span data-ttu-id="ed600-113">N</span><span class="sxs-lookup"><span data-stu-id="ed600-113">N</span></span>        |
| <span data-ttu-id="ed600-114">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="ed600-114">Component\_</span></span> | [<span data-ttu-id="ed600-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ed600-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="ed600-116">J</span><span class="sxs-lookup"><span data-stu-id="ed600-116">Y</span></span>   | <span data-ttu-id="ed600-117">N</span><span class="sxs-lookup"><span data-stu-id="ed600-117">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ed600-118">Spalten</span><span class="sxs-lookup"><span data-stu-id="ed600-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ed600-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Befinden\_</span><span class="sxs-lookup"><span data-stu-id="ed600-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="ed600-120">Externer Schlüssel in der ersten Spalte der [Verzeichnis Tabelle](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="ed600-120">External key into the first column of the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed600-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="ed600-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="ed600-122">Externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ed600-122">External key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed600-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed600-123">Remarks</span></span>

<span data-ttu-id="ed600-124">Die Ordner in dieser Tabelle werden bei der Installation der Komponente erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed600-124">The folders in this table are created when the component is installed.</span></span> <span data-ttu-id="ed600-125">Es wurde versucht, diese Ordner nur zu entfernen, wenn die Komponente deinstalliert oder in "Run-From-Source" verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="ed600-125">An attempt is made to remove these folders only when the component is uninstalled or moved to run-from-source.</span></span> <span data-ttu-id="ed600-126">Wenn die Ordner leer werden, wird keine automatische Entfernung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ed600-126">No automatic removal is triggered if the folders become empty.</span></span> <span data-ttu-id="ed600-127">Im Gegensatz dazu werden Ordner, die vom Installer erstellt, aber nicht in dieser Tabelle aufgelistet werden, entfernt, wenn Sie leer sind.</span><span class="sxs-lookup"><span data-stu-id="ed600-127">In contrast, folders created by the installer but not listed in this table are removed when they become empty.</span></span>

<span data-ttu-id="ed600-128">Da Ordner, die vom Installationsprogramm erstellt werden, gelöscht werden, wenn Sie leer sind, müssen Sie einen Eintrag in der Tabelle "| atefolder" erstellen, um eine Komponente zu installieren, die aus einem leeren Ordner besteht.</span><span class="sxs-lookup"><span data-stu-id="ed600-128">Because folders created by the installer are deleted when they become empty, you must author an entry into the CreateFolder table to install a component that consists of an empty folder.</span></span>

<span data-ttu-id="ed600-129">Auf diese Tabelle wird verwiesen, wenn [die Aktion "die Aktion"](createfolders-action.md) oder " [RemoveFolders](removefolders-action.md) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ed600-129">This table is referred to when the [CreateFolders](createfolders-action.md) action or the [RemoveFolders](removefolders-action.md) action is called.</span></span>

<span data-ttu-id="ed600-130">Informationen zum Sichern eines Ordners finden Sie in der Tabelle " [msilockpermissionsex](msilockpermissionsex-table.md) " und der [Tabelle "lockberechtigungs](lockpermissions-table.md)Tabelle".</span><span class="sxs-lookup"><span data-stu-id="ed600-130">For information on how to secure a folder see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="ed600-131">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="ed600-131">Validation</span></span>

<dl>

[<span data-ttu-id="ed600-132">ICE03</span><span class="sxs-lookup"><span data-stu-id="ed600-132">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ed600-133">ICE06</span><span class="sxs-lookup"><span data-stu-id="ed600-133">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ed600-134">ICE18</span><span class="sxs-lookup"><span data-stu-id="ed600-134">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="ed600-135">ICE32</span><span class="sxs-lookup"><span data-stu-id="ed600-135">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ed600-136">ICE55</span><span class="sxs-lookup"><span data-stu-id="ed600-136">ICE55</span></span>](ice55.md)  
</dl>

 

 



