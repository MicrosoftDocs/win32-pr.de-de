---
description: Die msiunpublishassemblyaktion verwaltet die Ankündigung von Common Language Runtime Assemblys und Win32-Assemblys, die entfernt werden.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Msiunpublishassemblyaktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d398c66781e6e356b110828c56de6f5e616775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867468"
---
# <a name="msiunpublishassemblies-action"></a><span data-ttu-id="561a1-103">Msiunpublishassemblyaktion</span><span class="sxs-lookup"><span data-stu-id="561a1-103">MsiUnpublishAssemblies Action</span></span>

<span data-ttu-id="561a1-104">Die msiunpublishassemblyaktion verwaltet die Ankündigung von Common Language Runtime Assemblys und Win32-Assemblys, die entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="561a1-104">The MsiUnpublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies that are being removed.</span></span> <span data-ttu-id="561a1-105">Mit der-Aktion wird die [MsiAssembly-Tabelle](msiassembly-table.md) abgefragt, um zu bestimmen, welche Assemblys angekündigte oder installierte Features aus dem globalen Assemblycache entfernt haben und welche Assemblys eine angekündigte oder installierte übergeordnete Komponente von einem Speicherort entfernt wird, der für eine bestimmte</span><span class="sxs-lookup"><span data-stu-id="561a1-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have advertised or installed features being removed from the global assembly cache and which assemblies have an advertised or installed parent component being removed from a location isolated for a particular application.</span></span> <span data-ttu-id="561a1-106">Weitere Informationen finden Sie unter Installieren von Assemblys [im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md) und [Installieren von Win32](installation-of-win32-assemblies.md)-Assemblys.</span><span class="sxs-lookup"><span data-stu-id="561a1-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="561a1-107">Auf Systemen, auf denen Windows XP und höher ausgeführt wird, können Windows Installer Win32-Assemblys [als parallele](side-by-side-assemblies.md)Assemblys installieren.</span><span class="sxs-lookup"><span data-stu-id="561a1-107">On systems running Windows XP and later, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="561a1-108">Weitere Informationen finden Sie unter Informationen [zu isolierten Anwendungen und](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)parallelen Assemblys.</span><span class="sxs-lookup"><span data-stu-id="561a1-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="561a1-109">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="561a1-109">Sequence Restrictions</span></span>

<span data-ttu-id="561a1-110">Die msiunpublishassemblyaktion muss nach der [InstallInitialize-Aktion](installinitialize-action.md) in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="561a1-110">The MsiUnpublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="561a1-111">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="561a1-111">ActionData Messages</span></span>



| <span data-ttu-id="561a1-112">Feld</span><span class="sxs-lookup"><span data-stu-id="561a1-112">Field</span></span> | <span data-ttu-id="561a1-113">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="561a1-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="561a1-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="561a1-114">\[1\]</span></span> | <span data-ttu-id="561a1-115">Anwendungskontext.</span><span class="sxs-lookup"><span data-stu-id="561a1-115">Application context.</span></span>       |
| <span data-ttu-id="561a1-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="561a1-116">\[2\]</span></span> | <span data-ttu-id="561a1-117">AssemblyName.</span><span class="sxs-lookup"><span data-stu-id="561a1-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="561a1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="561a1-118">Remarks</span></span>

<span data-ttu-id="561a1-119">Die [msipublishassemblyaktion](msipublishassemblies-action.md) verwaltet die Ankündigung von Assemblys, die angekündigt oder installiert werden.</span><span class="sxs-lookup"><span data-stu-id="561a1-119">The [MsiPublishAssemblies Action](msipublishassemblies-action.md) manages the advertisement of assemblies being advertised or installed.</span></span>

 

 
