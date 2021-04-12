---
description: Die msipatcholdassemblyname-Tabelle gibt den alten Namen für eine Assembly an.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Msipatcholdassemblyname-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347348"
---
# <a name="msipatcholdassemblyname-table"></a><span data-ttu-id="84608-103">Msipatcholdassemblyname-Tabelle</span><span class="sxs-lookup"><span data-stu-id="84608-103">MsiPatchOldAssemblyName Table</span></span>

<span data-ttu-id="84608-104">Die msipatcholdassemblyname-Tabelle gibt den alten Namen für eine Assembly an.</span><span class="sxs-lookup"><span data-stu-id="84608-104">The MsiPatchOldAssemblyName table specifies the old name for an assembly.</span></span>

<span data-ttu-id="84608-105">Die msipatcholdassemblyname-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="84608-105">The MsiPatchOldAssemblyName table has the following columns.</span></span>



| <span data-ttu-id="84608-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="84608-106">Column</span></span>   | <span data-ttu-id="84608-107">Typ</span><span class="sxs-lookup"><span data-stu-id="84608-107">Type</span></span>                         | <span data-ttu-id="84608-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="84608-108">Key</span></span> | <span data-ttu-id="84608-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="84608-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="84608-110">Assembly</span><span class="sxs-lookup"><span data-stu-id="84608-110">Assembly</span></span> | [<span data-ttu-id="84608-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="84608-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="84608-112">J</span><span class="sxs-lookup"><span data-stu-id="84608-112">Y</span></span>   | <span data-ttu-id="84608-113">N</span><span class="sxs-lookup"><span data-stu-id="84608-113">N</span></span>        |
| <span data-ttu-id="84608-114">Name</span><span class="sxs-lookup"><span data-stu-id="84608-114">Name</span></span>     | [<span data-ttu-id="84608-115">Text</span><span class="sxs-lookup"><span data-stu-id="84608-115">Text</span></span>](text.md)             | <span data-ttu-id="84608-116">J</span><span class="sxs-lookup"><span data-stu-id="84608-116">Y</span></span>   | <span data-ttu-id="84608-117">N</span><span class="sxs-lookup"><span data-stu-id="84608-117">N</span></span>        |
| <span data-ttu-id="84608-118">Wert</span><span class="sxs-lookup"><span data-stu-id="84608-118">Value</span></span>    | [<span data-ttu-id="84608-119">Text</span><span class="sxs-lookup"><span data-stu-id="84608-119">Text</span></span>](text.md)             | <span data-ttu-id="84608-120">N</span><span class="sxs-lookup"><span data-stu-id="84608-120">N</span></span>   | <span data-ttu-id="84608-121">N</span><span class="sxs-lookup"><span data-stu-id="84608-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="84608-122">Spalten</span><span class="sxs-lookup"><span data-stu-id="84608-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="84608-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Stadtverordneten</span><span class="sxs-lookup"><span data-stu-id="84608-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Assembly</span></span>
</dt> <dd>

<span data-ttu-id="84608-124">Eindeutiger Bezeichner für den alten Assemblynamen.</span><span class="sxs-lookup"><span data-stu-id="84608-124">Unique identifier for the old assembly name.</span></span> <span data-ttu-id="84608-125">Dieser Schlüssel wird als Zuordnung zwischen dieser und der Tabelle " [msipatcholdassemblyfile](msipatcholdassemblyfile-table.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="84608-125">This key is used as a mapping between this and the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="84608-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="84608-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="84608-127">Der Name des Attributs, das dem in der Spalte Wert angegebenen Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="84608-127">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="84608-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="84608-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="84608-129">Der Wert, der dem in der Spalte Name angegebenen Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="84608-129">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84608-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84608-130">Remarks</span></span>

<span data-ttu-id="84608-131">Beim Patchen von Assemblys, die im globalen Assemblycache (GAC) installiert sind, verwendet Windows Installer die Tabelle [msipatcholdassemblyfile](msipatcholdassemblyfile-table.md) und die Tabelle msipatcholdassemblyname.</span><span class="sxs-lookup"><span data-stu-id="84608-131">Windows Installer uses the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="84608-132">Wenn eine neuere Version einer Assembly freigegeben wird, wird der starke Name der Assembly geändert.</span><span class="sxs-lookup"><span data-stu-id="84608-132">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="84608-133">Die beiden Tabellen identifizieren den alten Assemblynamen für eine aktualisierte Assembly.</span><span class="sxs-lookup"><span data-stu-id="84608-133">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="84608-134">Dadurch kann der Installer den alten Assemblynamen verwenden, um die ursprüngliche Datei im GAC zu suchen und einen binären Patch anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="84608-134">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="84608-135">Ohne diese Informationen muss das Installationsprogramm möglicherweise auf die ursprüngliche Installationsquelle zugreifen, um eine im GAC installierte Assembly zu patchen.</span><span class="sxs-lookup"><span data-stu-id="84608-135">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="84608-136">Die [msipatcholdassemblyfile-Tabelle](msipatcholdassemblyfile-table.md) und die msipatcholdassemblyname-Tabelle werden nicht automatisch von [patchwiz](patchwiz-dll.md)generiert.</span><span class="sxs-lookup"><span data-stu-id="84608-136">The [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="84608-137">Das Update Paket, das in der [Tabelle "UpgradedImages](upgradedimages-table-patchwiz-dll-.md) " angegeben ist, muss diese Tabellen enthalten, damit der Patch diese Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="84608-137">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="84608-138">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="84608-138">Validation</span></span>

<dl>

[<span data-ttu-id="84608-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="84608-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="84608-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="84608-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="84608-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="84608-141">ICE32</span></span>](ice32.md)  
</dl>

 

 



