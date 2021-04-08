---
description: Windows Installer können das Patchen optimieren, um die für die Anwendung von Patches auf installierte Anwendungen erforderliche Zeit zu verkürzen.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Patch-Optimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864079"
---
# <a name="patch-optimization"></a><span data-ttu-id="8dc90-103">Patch-Optimierung</span><span class="sxs-lookup"><span data-stu-id="8dc90-103">Patch Optimization</span></span>

<span data-ttu-id="8dc90-104">Windows Installer können das Patchen optimieren, um die für die Anwendung von Patches auf installierte Anwendungen erforderliche Zeit zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="8dc90-104">Windows Installer can optimize patching to reduce the time that is required to apply patches to installed applications.</span></span>

<span data-ttu-id="8dc90-105">**Windows Installer 2,0:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8dc90-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="8dc90-106">Für Versionen von Windows Installer, die vor Windows Installer 3,0 veröffentlicht wurden, führt das Patchen eine komplette Reparatur Installation der Anwendung durch, die erheblich mehr Zeit in Anspruch nehmen kann.</span><span class="sxs-lookup"><span data-stu-id="8dc90-106">For versions of Windows Installer released before Windows Installer 3.0, patching runs a complete repair installation of the application, which can take significantly more time.</span></span>

<span data-ttu-id="8dc90-107">**Windows Installer 3,0 und höher:** Beim Patchen werden nur die Teile einer Anwendung geändert, die durch einen Patch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8dc90-107">**Windows Installer 3.0 and later:** The patching process only changes the parts of an application that are modified by a patch.</span></span>

<span data-ttu-id="8dc90-108">**Windows Installer 3,1 und höher:** Ab Windows Installer 3,1 erfordert die patchoptimierung, dass für alle Patches in der Transaktion die OptimizedInstallMode-Eigenschaft in der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md)auf 1 (eins) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8dc90-108">**Windows Installer 3.1 and later:** Beginning with Windows Installer 3.1, patch optimization requires that all patches in the transaction have the OptimizedInstallMode property set to 1 (one) in the [MsiPatchMetadata Table](msipatchmetadata-table.md).</span></span>

<span data-ttu-id="8dc90-109">Wenn in einem Patch nur die folgenden Tabellen geändert werden, werden die mit allen anderen Tabellen verbundenen Aktionen von Windows Installer 3,0 oder höher überspringt, auch wenn diese Aktionen in den Sequenz Tabellen des ursprünglichen Anwendungsinstallations Pakets (MSI-Datei) aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="8dc90-109">If a patch only modifies the following tables, Windows Installer 3.0 or later skips the actions that are associated with all the other tables, even if those actions are listed in the sequence tables of the original application installation package (.msi file).</span></span>

-   [<span data-ttu-id="8dc90-110">"AdminExecuteSequence"</span><span class="sxs-lookup"><span data-stu-id="8dc90-110">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="8dc90-111">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="8dc90-111">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="8dc90-112">Condition</span><span class="sxs-lookup"><span data-stu-id="8dc90-112">Condition</span></span>](condition-table.md)
-   [<span data-ttu-id="8dc90-113">CustomAction</span><span class="sxs-lookup"><span data-stu-id="8dc90-113">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="8dc90-114">File</span><span class="sxs-lookup"><span data-stu-id="8dc90-114">File</span></span>](file-table.md)
-   [<span data-ttu-id="8dc90-115">Filesfpcatalog</span><span class="sxs-lookup"><span data-stu-id="8dc90-115">FileSFPCatalog</span></span>](filesfpcatalog-table.md)
-   [<span data-ttu-id="8dc90-116">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="8dc90-116">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="8dc90-117">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="8dc90-117">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="8dc90-118">Medien</span><span class="sxs-lookup"><span data-stu-id="8dc90-118">Media</span></span>](media-table.md)
-   [<span data-ttu-id="8dc90-119">MoveFile</span><span class="sxs-lookup"><span data-stu-id="8dc90-119">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="8dc90-120">MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="8dc90-120">MsiAssembly</span></span>](msiassembly-table.md)
-   [<span data-ttu-id="8dc90-121">Msidigitalcertificate</span><span class="sxs-lookup"><span data-stu-id="8dc90-121">MsiDigitalCertificate</span></span>](msidigitalcertificate-table.md)
-   [<span data-ttu-id="8dc90-122">Msidigitalsignature</span><span class="sxs-lookup"><span data-stu-id="8dc90-122">MsiDigitalSignature</span></span>](msidigitalsignature-table.md)
-   [<span data-ttu-id="8dc90-123">Msiflehash</span><span class="sxs-lookup"><span data-stu-id="8dc90-123">MsiFileHash</span></span>](msifilehash-table.md)
-   [<span data-ttu-id="8dc90-124">Msipatchheader</span><span class="sxs-lookup"><span data-stu-id="8dc90-124">MsiPatchHeaders</span></span>](msipatchheaders-table.md)
-   [<span data-ttu-id="8dc90-125">Patch</span><span class="sxs-lookup"><span data-stu-id="8dc90-125">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="8dc90-126">Patchpaket</span><span class="sxs-lookup"><span data-stu-id="8dc90-126">PatchPackage</span></span>](patchpackage-table.md)
-   [<span data-ttu-id="8dc90-127">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8dc90-127">Property</span></span>](property-table.md)
-   [<span data-ttu-id="8dc90-128">Registrierung</span><span class="sxs-lookup"><span data-stu-id="8dc90-128">Registry</span></span>](registry-table.md)
-   [<span data-ttu-id="8dc90-129">Sfpcatalog</span><span class="sxs-lookup"><span data-stu-id="8dc90-129">SFPCatalog</span></span>](sfpcatalog-table.md)
-   [<span data-ttu-id="8dc90-130">Export der Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8dc90-130">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="8dc90-131">\_Spalten</span><span class="sxs-lookup"><span data-stu-id="8dc90-131">\_Columns</span></span>](-columns-table.md)
-   [<span data-ttu-id="8dc90-132">\_Speicher</span><span class="sxs-lookup"><span data-stu-id="8dc90-132">\_Storages</span></span>](-storages-table.md)
-   [<span data-ttu-id="8dc90-133">\_Datenströme</span><span class="sxs-lookup"><span data-stu-id="8dc90-133">\_Streams</span></span>](-streams-table.md)
-   [<span data-ttu-id="8dc90-134">\_Tabellen</span><span class="sxs-lookup"><span data-stu-id="8dc90-134">\_Tables</span></span>](-tables-table.md)
-   [<span data-ttu-id="8dc90-135">\_Transformview-Tabelle</span><span class="sxs-lookup"><span data-stu-id="8dc90-135">\_TransformView Table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="8dc90-136">\_Überprüfen</span><span class="sxs-lookup"><span data-stu-id="8dc90-136">\_Validation</span></span>](-validation-table.md)

<span data-ttu-id="8dc90-137">Verwenden Sie die Richtlinie [disableflyweightpatching](disableflyweightpatching.md) , um die patchoptimierungs Option zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8dc90-137">To turn off the patch optimization option, use the [DisableFlyWeightPatching](disableflyweightpatching.md) policy.</span></span>

 

 



