---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (isolierte Anwendungen und parallele Assemblys)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347989"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="47d12-103">A (isolierte Anwendungen und parallele Assemblys)</span><span class="sxs-lookup"><span data-stu-id="47d12-103">A (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="47d12-104">a B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="47d12-104">A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="47d12-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**Aktivierungs Kontext**</span><span class="sxs-lookup"><span data-stu-id="47d12-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**activation context**</span></span>
</dt> <dd>

<span data-ttu-id="47d12-106">Eine Datenstruktur im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="47d12-106">A data structure in memory.</span></span> <span data-ttu-id="47d12-107">Jeder Abschnitt dieser Struktur enthält Metadaten für parallele API-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="47d12-107">Each section of this structure contains metadata for side-by-side-aware API functions.</span></span> <span data-ttu-id="47d12-108">Ein Abschnitt kann z. b. dll-Umleitungs Daten enthalten, die vom dll-Lade Modul verwendet werden, und ein anderer Abschnitt kann über com-Serverdaten verfügen.</span><span class="sxs-lookup"><span data-stu-id="47d12-108">For example, one section may have DLL redirection data, which is used by the DLL loader, and another may have COM server data.</span></span> <span data-ttu-id="47d12-109">Diese Daten können verwendet werden, um das Laden einer DLL an eine bestimmte Version, die Erstellung eines COM-Objekts oder die Erstellung eines Fensters an eine Version umzuleiten, die für die Anwendung am meisten kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="47d12-109">This data may be used to redirect the loading of a DLL to a specific version, the creation of a COM object, or the creation of a window to a version that is most compatible for the application.</span></span>

</dd> <dt>

<span data-ttu-id="47d12-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**Anwendungskonfiguration**</span><span class="sxs-lookup"><span data-stu-id="47d12-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="47d12-111">Namen und Versionen paralleler Assemblys, die zum Ausführen einer Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="47d12-111">Names and versions of side-by-side assemblies required to run an application.</span></span> <span data-ttu-id="47d12-112">Wenn eine Anwendung mit einem Manifest bereitgestellt wird, werden Abhängigkeiten von bestimmten Versionen von freigegebenen parallelen Assemblys explizit definiert.</span><span class="sxs-lookup"><span data-stu-id="47d12-112">When an application is deployed with a manifest, dependencies on specific versions of shared side-by-side assemblies are explicitly defined.</span></span> <span data-ttu-id="47d12-113">Standardmäßig ist die Version der Assembly, die im Manifest angegeben ist, die Version, die bei der Aktivierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47d12-113">By default, the version of the assembly specified in the manifest is the version that is used upon activation.</span></span> <span data-ttu-id="47d12-114">Mit der globalen Anwendungskonfiguration wird die Konfiguration aller Anwendungen auf dem System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="47d12-114">Global application configuration specifies the configuration of all applications on the system.</span></span> <span data-ttu-id="47d12-115">Die Konfiguration pro Anwendung kann die globale Anwendungskonfiguration auf Anwendungs Basis außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="47d12-115">Per-application configuration can override the global application configuration on a per-application basis.</span></span>

</dd> <dt>

<span data-ttu-id="47d12-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**Anwendungs Konfigurations Manifest**</span><span class="sxs-lookup"><span data-stu-id="47d12-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**application configuration manifest**</span></span>
</dt> <dd>

<span data-ttu-id="47d12-117">Eine Datei, die parallele Assemblys angibt, die von einer vollständig oder teilweise isolierten Anwendung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47d12-117">File that specifies side-by-side assemblies to be used by a fully or partially isolated application.</span></span> <span data-ttu-id="47d12-118">Dateien des Anwendungs konfigurationsmanifests werden im selben Ordner wie die ausführbare Datei der Anwendung installiert.</span><span class="sxs-lookup"><span data-stu-id="47d12-118">Application configuration manifest files are installed in the same folder as the application's executable file.</span></span>

</dd> <dt>

<span data-ttu-id="47d12-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**Anwendungs Manifest**</span><span class="sxs-lookup"><span data-stu-id="47d12-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**application manifest**</span></span>
</dt> <dd>

<span data-ttu-id="47d12-120">Datei, in der eine isolierte Anwendung beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="47d12-120">File that describes an isolated application.</span></span> <span data-ttu-id="47d12-121">Sie gibt die für die Ausführung der Anwendung erforderlichen Informationen an, einschließlich Abhängigkeiten von privaten Assemblys, bestimmte Versionen von freigegebenen Assemblys und Metadaten für private Assemblys.</span><span class="sxs-lookup"><span data-stu-id="47d12-121">It specifies the information required to run the application, including dependencies on private assemblies, specific versions of shared assemblies and metadata for private assemblies.</span></span> <span data-ttu-id="47d12-122">Der Name einer Anwendungs Manifest-Datei ist der Name der ausführbaren Datei der Anwendung, gefolgt von der Erweiterung ". Manifest".</span><span class="sxs-lookup"><span data-stu-id="47d12-122">The name of an application manifest file is the name of the application executable followed by the extension .manifest.</span></span> <span data-ttu-id="47d12-123">Beispielsweise wäre die Manifest-Datei für MySampleApp.exe MySampleApp.exe. manifest.</span><span class="sxs-lookup"><span data-stu-id="47d12-123">For example, for MySampleApp.exe, the manifest file would be MySampleApp.exe.manifest.</span></span>

</dd> <dt>

<span data-ttu-id="47d12-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**Stadtverordneten**</span><span class="sxs-lookup"><span data-stu-id="47d12-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="47d12-125">Grundlegende Einheit für das benennen, binden, Versionieren, bereitstellen oder Konfigurieren eines Blocks von Programmiercode.</span><span class="sxs-lookup"><span data-stu-id="47d12-125">Fundamental unit for naming, binding, versioning, deploying, or configuring a block of programming code.</span></span> <span data-ttu-id="47d12-126">Diese Codeassemblys können in DLLs oder COM-Assemblys abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="47d12-126">These code assemblies may be placed in DLLs or COM assemblies.</span></span> <span data-ttu-id="47d12-127">Anwendungen mit allgemeiner Funktionalität können freigegebene Blöcke von Programmiercode ausführen, die als Module oder Codeassemblys bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="47d12-127">Applications with common functionality may run shared blocks of programming code which are referred to as modules or code assemblies.</span></span> <span data-ttu-id="47d12-128">Die Infrastruktur für die sichere Freigabe von Assemblys wird als parallele assemblyfreigabe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="47d12-128">The infrastructure for the safe sharing of assemblies is referred to as side-by-side assembly sharing.</span></span>

</dd> <dt>

<span data-ttu-id="47d12-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**Assemblymanifest**</span><span class="sxs-lookup"><span data-stu-id="47d12-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="47d12-130">Beschreibung einer parallelen Assembly.</span><span class="sxs-lookup"><span data-stu-id="47d12-130">Description of a side-by-side assembly.</span></span> <span data-ttu-id="47d12-131">Er gibt den Namen, die Version, die Dateien, die Ressourcen der Assembly, die Bindungs Daten für die Elemente der Assembly sowie Abhängigkeiten von anderen parallelen Assemblys an.</span><span class="sxs-lookup"><span data-stu-id="47d12-131">It specifies the name, version, files, resources of the assembly, binding data for items of the assembly, and dependencies on other side-by-side assemblies.</span></span> <span data-ttu-id="47d12-132">Eine Assemblymanifest-Datei kann einen beliebigen gültigen Dateinamen aufweisen, solange die Erweiterung. Manifest folgt.</span><span class="sxs-lookup"><span data-stu-id="47d12-132">An assembly manifest file can have any valid file name, as long as it is followed by the extension .manifest.</span></span>

</dd> </dl>

 

 



