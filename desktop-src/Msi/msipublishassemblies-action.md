---
description: Die msipublishassemblyaktion verwaltet die Ankündigung von Common Language Runtime Assemblys und Win32-Assemblys.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Msipublishassemblyaktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24e1787aeb87cf00eb82aefab375771c7c1ddc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350137"
---
# <a name="msipublishassemblies-action"></a><span data-ttu-id="f9825-103">Msipublishassemblyaktion</span><span class="sxs-lookup"><span data-stu-id="f9825-103">MsiPublishAssemblies Action</span></span>

<span data-ttu-id="f9825-104">Die msipublishassemblyaktion verwaltet die Ankündigung von Common Language Runtime Assemblys und Win32-Assemblys.</span><span class="sxs-lookup"><span data-stu-id="f9825-104">The MsiPublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="f9825-105">Mit der-Aktion wird die [MsiAssembly-Tabelle](msiassembly-table.md) abgefragt, um zu bestimmen, welche Assemblys im globalen Assemblycache angekündigt oder installiert werden und welche Assemblys über eine übergeordnete Komponente verfügen, die für eine bestimmte Anwendung isoliert ist.</span><span class="sxs-lookup"><span data-stu-id="f9825-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have features being advertised or installed to the global assembly cache and which assemblies have a parent component being advertised or installed to a location isolated for a particular application.</span></span> <span data-ttu-id="f9825-106">Weitere Informationen finden Sie unter Installieren von Assemblys [im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md) und [Installieren von Win32](installation-of-win32-assemblies.md)-Assemblys.</span><span class="sxs-lookup"><span data-stu-id="f9825-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="f9825-107">Auf [Systemen mit Microsoft](side-by-side-assemblies.md)Windows XP und höher können Windows Installer Win32-Assemblys als parallele Assemblys installieren.</span><span class="sxs-lookup"><span data-stu-id="f9825-107">On Microsoft Windows XP and later systems, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="f9825-108">Weitere Informationen finden Sie unter Informationen [zu isolierten Anwendungen und](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)parallelen Assemblys.</span><span class="sxs-lookup"><span data-stu-id="f9825-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f9825-109">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="f9825-109">Sequence Restrictions</span></span>

<span data-ttu-id="f9825-110">Die msipublishassemblyaktion muss nach der [InstallInitialize-Aktion](installinitialize-action.md) in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) oder der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f9825-110">The MsiPublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md) or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f9825-111">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="f9825-111">ActionData Messages</span></span>



| <span data-ttu-id="f9825-112">Feld</span><span class="sxs-lookup"><span data-stu-id="f9825-112">Field</span></span> | <span data-ttu-id="f9825-113">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="f9825-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="f9825-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f9825-114">\[1\]</span></span> | <span data-ttu-id="f9825-115">Anwendungskontext.</span><span class="sxs-lookup"><span data-stu-id="f9825-115">Application context.</span></span>       |
| <span data-ttu-id="f9825-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="f9825-116">\[2\]</span></span> | <span data-ttu-id="f9825-117">AssemblyName.</span><span class="sxs-lookup"><span data-stu-id="f9825-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="f9825-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9825-118">Remarks</span></span>

<span data-ttu-id="f9825-119">Weitere Informationen finden Sie unter [](assemblies.md)Assemblys.</span><span class="sxs-lookup"><span data-stu-id="f9825-119">For more information, see [Assemblies](assemblies.md).</span></span>

<span data-ttu-id="f9825-120">Die [msiunpublishassemblyaktion](msiunpublishassemblies-action.md) verwaltet die Ankündigung der zu entfernenden Assemblys.</span><span class="sxs-lookup"><span data-stu-id="f9825-120">The [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md) manages the advertisement of assemblies being removed.</span></span>

 

 
