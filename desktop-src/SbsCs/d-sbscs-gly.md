---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3A4C5579-7543-4E0B-921D-BED42C2583D9
title: D (isolierte Anwendungen und parallele Assemblys)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c8912f24478f79be8aa00c963dc27cb46ec756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042386"
---
# <a name="d-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="8c415-103">D (isolierte Anwendungen und parallele Assemblys)</span><span class="sxs-lookup"><span data-stu-id="8c415-103">D (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="8c415-104">[a](a-sbscs-gly.md) B C D E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="8c415-104">[A](a-sbscs-gly.md) B C D E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="8c415-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**DEF-Kontext assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="8c415-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**DEF-context assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="8c415-106">Ein **assemblyIdentity** -Unterelement, das die parallele Assembly definiert, die durch das Manifest beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8c415-106">An **assemblyIdentity** subelement defining the side-by-side assembly described by the manifest.</span></span> <span data-ttu-id="8c415-107">Das unter **geordnete Element "** DEF-Context assemblyIdentity" ist immer das erste Unterelement eines **Assemblyelements** .</span><span class="sxs-lookup"><span data-stu-id="8c415-107">A DEF-context **assemblyIdentity** subelement is always the first subelement of an **assembly** element.</span></span>

</dd> <dt>

<span data-ttu-id="8c415-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**DLL-Versions Verwaltungs Konflikt**</span><span class="sxs-lookup"><span data-stu-id="8c415-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**DLL versioning conflict**</span></span>
</dt> <dd>

<span data-ttu-id="8c415-109">Kompatibilitätsproblem.</span><span class="sxs-lookup"><span data-stu-id="8c415-109">Compatibility problem.</span></span> <span data-ttu-id="8c415-110">Assemblyfreigabe-Probleme treten auf, wenn eine Anwendung eine Version einer freigegebenen Assembly installiert, die nicht abwärts kompatibel mit der zuvor installierten Version ist.</span><span class="sxs-lookup"><span data-stu-id="8c415-110">Assembly sharing problems occur when an application installs a version of a shared assembly that is not backward compatible with the previously installed version.</span></span> <span data-ttu-id="8c415-111">Eine Lösung für Konflikte bei der dll-Versionsverwaltung besteht darin, eine parallele assemblyfreigabe und isolierte Anwendungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c415-111">A solution to DLL versioning conflicts is to use side-by-side assembly sharing and isolated applications.</span></span> <span data-ttu-id="8c415-112">Bei der parallelen assemblyfreigabe können mehrere Versionen derselben Windows-Assembly gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8c415-112">With side-by-side assembly sharing, multiple versions of the same Windows assembly can run simultaneously.</span></span> <span data-ttu-id="8c415-113">Entwickler können auswählen, welche parallele Assembly verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c415-113">Developers can choose which side-by-side assembly to use.</span></span>

</dd> </dl>

 

 



