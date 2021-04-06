---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 5591218A-3212-46D0-A40F-C0788B459545
title: S (isolierte Anwendungen und parallele Assemblys)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9727db4c2db522b0bbb88eccf89481a61a75d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759042"
---
# <a name="s-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="adb63-103">S (isolierte Anwendungen und parallele Assemblys)</span><span class="sxs-lookup"><span data-stu-id="adb63-103">S (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="adb63-104">[a](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="adb63-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="adb63-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**freigegebene parallele Assembly**</span><span class="sxs-lookup"><span data-stu-id="adb63-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**shared side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="adb63-106">Eine freigegebene parallele Assembly ist für die Verwendung durch mehrere Anwendungen auf dem Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="adb63-106">A shared side-by-side assembly is available for use by multiple applications on the computer.</span></span> <span data-ttu-id="adb63-107">Es wird im Ordner WinSxS des Windows-Verzeichnisses installiert.</span><span class="sxs-lookup"><span data-stu-id="adb63-107">It is installed in the Winsxs folder of the Windows directory.</span></span> <span data-ttu-id="adb63-108">Anwendungen und Administratoren können die Version einer freigegebenen Assembly verwalten, die Sie verwenden möchten, indem Sie die Anwendungskonfiguration angeben.</span><span class="sxs-lookup"><span data-stu-id="adb63-108">Applications and administrators can manage the version of a shared assembly to be used by specifying the application configuration.</span></span> <span data-ttu-id="adb63-109">Parallele Assemblys werden immer von Manifest-Dateien begleitet, die Informationen über die Assembly für das Betriebssystem bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="adb63-109">Side-by-side assemblies are always accompanied by manifest files that provide information about the assembly to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="adb63-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**parallele Assembly**</span><span class="sxs-lookup"><span data-stu-id="adb63-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="adb63-111">Eine parallele Assembly ist eine Win32-Assembly, die von Manifests begleitet wird.</span><span class="sxs-lookup"><span data-stu-id="adb63-111">A side-by-side assembly is a Win32 assembly accompanied by manifests.</span></span> <span data-ttu-id="adb63-112">Eine parallele Assembly enthält eine Sammlung von Ressourcen – eine Gruppe von DLLs, Windows-Klassen, com-Servern, Typbibliotheken oder Schnittstellen –, die für Anwendungen immer zusammen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="adb63-112">A side-by-side assembly contains a collection of resources—a group of DLLs, windows classes, COM servers, type libraries, or interfaces—that are always provided to applications together.</span></span>

</dd> <dt>

<span data-ttu-id="adb63-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**parallele assemblyfreigabe**</span><span class="sxs-lookup"><span data-stu-id="adb63-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**side-by-side assembly sharing**</span></span>
</dt> <dd>

<span data-ttu-id="adb63-114">Verwendung von parallelen Assemblys, um Assemblys sicher für mehrere Anwendungen freizugeben und die negativen Auswirkungen der Freigabe auszugleichen, wie z. b. dll-Konflikte.</span><span class="sxs-lookup"><span data-stu-id="adb63-114">Use of side-by-side assemblies to safely share assemblies among multiple applications and to offset the negative effects of sharing, such as DLL conflicts.</span></span> <span data-ttu-id="adb63-115">Anstatt eine einzige Version einer Assembly zu verwenden, die die Abwärtskompatibilität mit allen Anwendungen annimmt, ermöglicht die parallele assemblyfreigabe, dass mehrere Versionen einer Win32-Assembly gleichzeitig auf dem System ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="adb63-115">Instead of having a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="adb63-116">Parallele Assemblys werden immer von assemblymanierdateien begleitet, die Informationen über die Assembly für das Betriebssystem bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="adb63-116">Side-by-side assemblies are always accompanied by assembly manifest files that provide information about the assembly to the operating system.</span></span> <span data-ttu-id="adb63-117">Anwendungen und Administratoren können die parallele assemblyfreigabe nach der Bereitstellung verwalten, indem Sie die Anwendungskonfiguration entweder global oder pro Anwendung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="adb63-117">Applications and administrators can manage side-by-side assembly sharing after deployment by updating the application configuration on either a global or per-application basis.</span></span>

</dd> </dl>

 

 



