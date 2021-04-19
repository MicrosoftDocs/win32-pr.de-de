---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 904FE2AB-9E94-47E4-88BA-DB215775797B
title: G (isolierte Anwendungen und parallele Assemblys)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4488c03da1c4c1f568db039a8b0e0a05d60ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346092"
---
# <a name="g-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="0d385-103">G (isolierte Anwendungen und parallele Assemblys)</span><span class="sxs-lookup"><span data-stu-id="0d385-103">G (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="0d385-104">[a](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F G H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="0d385-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F G H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="0d385-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**globale Anwendungskonfiguration**</span><span class="sxs-lookup"><span data-stu-id="0d385-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**global application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="0d385-106">Angabe, dass für alle Anwendungen im System dieselbe Assemblyversion der gleichen Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d385-106">Specification that all applications on the system use the same side-by-side assembly version.</span></span> <span data-ttu-id="0d385-107">Die globale Konfiguration wird auf assemblybasis in einer globalen Assemblymanifest-Datei angegeben, die im Ordner WinSxS installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0d385-107">Global configuration is specified on a per-assembly basis in a global assembly manifest file installed in the Winsxs folder.</span></span> <span data-ttu-id="0d385-108">Die globale Konfiguration kann verwendet werden, wenn ein Assemblyentwickler oder-Administrator alle Anwendungen auf dem System für die Verwendung einer neueren Assemblyversion konfigurieren muss.</span><span class="sxs-lookup"><span data-stu-id="0d385-108">Global configuration might be used when an assembly developer or administrator needs to configure all applications on the system to use a newer assembly version.</span></span> <span data-ttu-id="0d385-109">In diesem Fall muss die neue Assembly abwärts kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="0d385-109">In this case, the new assembly needs to be backward compatible.</span></span> <span data-ttu-id="0d385-110">Eine Konfiguration pro Anwendung überschreibt die standardmäßige oder globale Anwendungskonfiguration für bestimmte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="0d385-110">A per-application configuration overrides the default or global application configuration for specific applications.</span></span>

</dd> <dt>

<span data-ttu-id="0d385-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**globales Assemblymanifest**</span><span class="sxs-lookup"><span data-stu-id="0d385-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**global assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="0d385-112">Datei, die die globale Anwendungskonfiguration einer parallelen Assembly definiert.</span><span class="sxs-lookup"><span data-stu-id="0d385-112">File that defines the global application configuration of a side-by-side assembly.</span></span> <span data-ttu-id="0d385-113">Globale Assemblymanifestressourcen werden im System-Assemblyspeicher im Ordner WinSxS installiert.</span><span class="sxs-lookup"><span data-stu-id="0d385-113">Global assembly manifest files are installed into the system assembly store in the Winsxs folder.</span></span>

</dd> </dl>

 

 



