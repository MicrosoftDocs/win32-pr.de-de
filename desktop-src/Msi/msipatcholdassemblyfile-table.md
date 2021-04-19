---
description: Die msipatcholdassemblyfile-Tabelle verknüpft eine Datei in der Dateitabelle mit einem Assemblynamen in der msipatcholdassemblyname-Tabelle. Mehrere alte Assemblynamen können einer einzelnen Datei zugeordnet werden.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Msipatcholdassemblyfile-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357074"
---
# <a name="msipatcholdassemblyfile-table"></a><span data-ttu-id="8c1ce-104">Msipatcholdassemblyfile-Tabelle</span><span class="sxs-lookup"><span data-stu-id="8c1ce-104">MsiPatchOldAssemblyFile Table</span></span>

<span data-ttu-id="8c1ce-105">Die msipatcholdassemblyfile-Tabelle verknüpft eine Datei in der [Dateitabelle](file-table.md) mit einem [Assemblynamen in der msipatcholdassemblyname-Tabelle](msipatcholdassemblyname-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c1ce-105">The MsiPatchOldAssemblyFile table relates a file in the [File table](file-table.md) to an assembly name in the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md).</span></span> <span data-ttu-id="8c1ce-106">Mehrere alte Assemblynamen können einer einzelnen Datei zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-106">Multiple old assembly names can be associated with a single file.</span></span>

<span data-ttu-id="8c1ce-107">Die msipatcholdassemblyfile-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-107">The MsiPatchOldAssemblyFile table has the following columns.</span></span>



| <span data-ttu-id="8c1ce-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="8c1ce-108">Column</span></span>     | <span data-ttu-id="8c1ce-109">Typ</span><span class="sxs-lookup"><span data-stu-id="8c1ce-109">Type</span></span>                         | <span data-ttu-id="8c1ce-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="8c1ce-110">Key</span></span> | <span data-ttu-id="8c1ce-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="8c1ce-111">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="8c1ce-112">Datei\_</span><span class="sxs-lookup"><span data-stu-id="8c1ce-112">File\_</span></span>     | [<span data-ttu-id="8c1ce-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8c1ce-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="8c1ce-114">J</span><span class="sxs-lookup"><span data-stu-id="8c1ce-114">Y</span></span>   | <span data-ttu-id="8c1ce-115">N</span><span class="sxs-lookup"><span data-stu-id="8c1ce-115">N</span></span>        |
| <span data-ttu-id="8c1ce-116">Assembly\_</span><span class="sxs-lookup"><span data-stu-id="8c1ce-116">Assembly\_</span></span> | [<span data-ttu-id="8c1ce-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8c1ce-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="8c1ce-118">J</span><span class="sxs-lookup"><span data-stu-id="8c1ce-118">Y</span></span>   | <span data-ttu-id="8c1ce-119">N</span><span class="sxs-lookup"><span data-stu-id="8c1ce-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8c1ce-120">Spalten</span><span class="sxs-lookup"><span data-stu-id="8c1ce-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8c1ce-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_</span><span class="sxs-lookup"><span data-stu-id="8c1ce-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="8c1ce-122">Fremdschlüssel für die [Dateitabelle](file-table.md) , der die zu patchen Assembly angibt.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-122">Foreign key to the [File table](file-table.md) that specifies the assembly to be patched.</span></span> <span data-ttu-id="8c1ce-123">Diese Spalte ist Teil des Primärschlüssels.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-123">This column is part of the primary key.</span></span>

</dd> <dt>

<span data-ttu-id="8c1ce-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Stadtverordneten\_</span><span class="sxs-lookup"><span data-stu-id="8c1ce-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assembly\_</span></span>
</dt> <dd>

<span data-ttu-id="8c1ce-125">Der Fremdschlüssel für die [msipatcholdassemblyname-Tabelle](msipatcholdassemblyname-table.md) , der einen der alten Assemblynamen für die Assembly identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-125">Foreign key to the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) that identifies one of the old assembly names for the assembly.</span></span> <span data-ttu-id="8c1ce-126">Diese Spalte ist Teil des Primärschlüssels.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-126">This column is part of the primary key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c1ce-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c1ce-127">Remarks</span></span>

<span data-ttu-id="8c1ce-128">Beim Patchen von Assemblys, die im globalen Assemblycache (GAC) installiert sind, verwendet Windows Installer die Tabelle msipatcholdassemblyfile und die [Tabelle msipatcholdassemblyname](msipatcholdassemblyname-table.md) .</span><span class="sxs-lookup"><span data-stu-id="8c1ce-128">Windows Installer uses the MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="8c1ce-129">Wenn eine neuere Version einer Assembly freigegeben wird, wird der starke Name der Assembly geändert.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-129">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="8c1ce-130">Die beiden Tabellen identifizieren den alten Assemblynamen für eine aktualisierte Assembly.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-130">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="8c1ce-131">Dadurch kann der Installer den alten Assemblynamen verwenden, um die ursprüngliche Datei im GAC zu suchen und einen binären Patch anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-131">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="8c1ce-132">Ohne diese Informationen muss das Installationsprogramm möglicherweise auf die ursprüngliche Installationsquelle zugreifen, um eine im GAC installierte Assembly zu patchen.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-132">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="8c1ce-133">Die msipatcholdassemblyfile-Tabelle und die [msipatcholdassemblyname-Tabelle](msipatcholdassemblyname-table.md) werden nicht automatisch von [patchwiz](patchwiz-dll.md)generiert.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-133">The MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="8c1ce-134">Das Update Paket, das in der [Tabelle "UpgradedImages](upgradedimages-table-patchwiz-dll-.md) " angegeben ist, muss diese Tabellen enthalten, damit der Patch diese Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="8c1ce-134">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="8c1ce-135">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="8c1ce-135">Validation</span></span>

<dl>

[<span data-ttu-id="8c1ce-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="8c1ce-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8c1ce-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="8c1ce-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8c1ce-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="8c1ce-138">ICE32</span></span>](ice32.md)  
</dl>

 

 



