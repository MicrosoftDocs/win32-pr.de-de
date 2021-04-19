---
description: Common Language Runtime-Assemblys, die im globalen Assemblycache installiert sind, müssen in allen Vorkommen der Assembly über identische Dateien verfügen.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Neuinstallations Modi von Common Language Runtime-Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353442"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a><span data-ttu-id="30fd6-103">Neuinstallations Modi von Common Language Runtime-Assemblys</span><span class="sxs-lookup"><span data-stu-id="30fd6-103">Reinstallation Modes of Common Language Runtime Assemblies</span></span>

<span data-ttu-id="30fd6-104">Common Language Runtime-Assemblys, die im globalen Assemblycache installiert sind, müssen in allen Vorkommen der Assembly über identische Dateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="30fd6-104">Common language runtime assemblies that are installed to the global assembly cache must have identical files in all occurrences of the assembly.</span></span> <span data-ttu-id="30fd6-105">Dies bedeutet, dass die von " [**msireinstallfeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) " und " [**msireinstallproduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) " verwendeten Neuinstallations Modi für reguläre Komponenten und Common Language Runtime Assemblys unterschiedliche Bedeutungen haben müssen.</span><span class="sxs-lookup"><span data-stu-id="30fd6-105">This means that the reinstallation modes used by [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) and [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) must have different meanings for regular components and common language runtime assemblies.</span></span> <span data-ttu-id="30fd6-106">Die folgenden Definitionen der neuinstallationsmodi gelten für Common Language Runtime Assemblys.</span><span class="sxs-lookup"><span data-stu-id="30fd6-106">The following definitions of reinstall modes apply to common language runtime assemblies.</span></span>



| <span data-ttu-id="30fd6-107">Neuinstallations Modus</span><span class="sxs-lookup"><span data-stu-id="30fd6-107">Reinstall mode</span></span>                  | <span data-ttu-id="30fd6-108">Bedeutung für Microsoft .NET Komponenten</span><span class="sxs-lookup"><span data-stu-id="30fd6-108">Meaning for Microsoft .NET Components</span></span>                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fd6-109">Datei für den erneuten installmode \_ fehlt</span><span class="sxs-lookup"><span data-stu-id="30fd6-109">REINSTALLMODE\_FILEMISSING</span></span>      | <span data-ttu-id="30fd6-110">Installieren Sie die Common Language Runtime Komponente, oder installieren Sie Sie neu, falls Sie fehlt oder unvollständig ist.</span><span class="sxs-lookup"><span data-stu-id="30fd6-110">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="30fd6-111">REINSTALLMODE- \_ fileolderversion</span><span class="sxs-lookup"><span data-stu-id="30fd6-111">REINSTALLMODE\_FILEOLDERVERSION</span></span> | <span data-ttu-id="30fd6-112">Installieren Sie die Common Language Runtime Komponente, oder installieren Sie Sie neu, falls Sie fehlt oder unvollständig ist.</span><span class="sxs-lookup"><span data-stu-id="30fd6-112">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="30fd6-113">REINSTALLMODE- \_ fileequalversion</span><span class="sxs-lookup"><span data-stu-id="30fd6-113">REINSTALLMODE\_FILEEQUALVERSION</span></span> | <span data-ttu-id="30fd6-114">Installieren Sie die Common Language Runtime Komponente, oder installieren Sie Sie neu, falls Sie fehlt oder unvollständig ist.</span><span class="sxs-lookup"><span data-stu-id="30fd6-114">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="30fd6-115">REINSTALLMODE \_ File Exact</span><span class="sxs-lookup"><span data-stu-id="30fd6-115">REINSTALLMODE\_FILEEXACT</span></span>        | <span data-ttu-id="30fd6-116">Installieren Sie die Common Language Runtime Komponente, oder installieren Sie Sie neu, falls Sie fehlt oder unvollständig ist.</span><span class="sxs-lookup"><span data-stu-id="30fd6-116">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="30fd6-117">REINSTALLMODE- \_ Filter</span><span class="sxs-lookup"><span data-stu-id="30fd6-117">REINSTALLMODE\_FILEVERIFY</span></span>       | <span data-ttu-id="30fd6-118">Installieren Sie die Common Language Runtime Komponente, oder installieren Sie Sie neu, wenn Sie nicht vorhanden ist oder wenn die vorhandene Komponente unvollständig oder beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="30fd6-118">Install or reinstall the common language runtime component if it is missing or if the existing component is incomplete or corrupt.</span></span> |
| <span data-ttu-id="30fd6-119">REINSTALLMODE- \_ filereplace</span><span class="sxs-lookup"><span data-stu-id="30fd6-119">REINSTALLMODE\_FILEREPLACE</span></span>      | <span data-ttu-id="30fd6-120">Installieren Sie die Common Language Runtime Komponente immer, oder installieren Sie Sie neu.</span><span class="sxs-lookup"><span data-stu-id="30fd6-120">Always install or reinstall the common language runtime component.</span></span>                                                                 |



 

 

 



