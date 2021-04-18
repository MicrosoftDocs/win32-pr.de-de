---
description: Windows Installer können Win32-Assemblys und Assemblys, die vom Common Language Runtime des Microsoft .NET Frameworks verwendet werden, installieren, entfernen und aktualisieren.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347958"
---
# <a name="assemblies"></a><span data-ttu-id="e9339-103">Assemblys</span><span class="sxs-lookup"><span data-stu-id="e9339-103">Assemblies</span></span>

<span data-ttu-id="e9339-104">Windows Installer können Win32-Assemblys und Assemblys, die vom Common Language Runtime des Microsoft .NET Frameworks verwendet werden, installieren, entfernen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e9339-104">Windows Installer can install, remove, and update Win32 assemblies and assemblies used by the common language runtime of the Microsoft .NET Framework.</span></span> <span data-ttu-id="e9339-105">Eine Assembly wird vom Windows Installer als einzelne installerkomponente behandelt.</span><span class="sxs-lookup"><span data-stu-id="e9339-105">An assembly is handled by the Windows Installer as a single installer component.</span></span> <span data-ttu-id="e9339-106">Alle Dateien, die eine Assembly bilden, müssen in einer einzelnen installerkomponente enthalten sein, die in der [Komponenten](component-table.md) Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="e9339-106">All of the files that constitute an assembly must be contained by a single installer component that is listed in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="e9339-107">Windows Installer, die unter Windows Vista und Windows XP ausgeführt werden, können parallele Assemblys installiert werden.</span><span class="sxs-lookup"><span data-stu-id="e9339-107">Windows Installer running on Windows Vista and Windows XP can install side-by-side assemblies.</span></span> <span data-ttu-id="e9339-108">Parallele Assemblys können Assemblys auf sichere Weise für mehrere Anwendungen freigeben und die negativen Auswirkungen der assemblyfreigabe, wie z. b. dll-Konflikte, ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="e9339-108">Side-by-side assemblies can safely share assemblies among multiple applications and can offset the negative effects of assembly sharing, such as DLL conflicts.</span></span> <span data-ttu-id="e9339-109">Anstelle einer einzelnen Version einer Assembly, die die Abwärtskompatibilität mit allen Anwendungen annimmt, ermöglicht die parallele assemblyfreigabe, dass mehrere Versionen einer com-oder Win32-Assembly gleichzeitig auf dem System ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e9339-109">Instead of a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a COM or Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="e9339-110">Diese verbesserte Funktion zum Isolieren von Anwendungen ist ein wichtiger Bestandteil des Microsoft .NET-Frameworks.</span><span class="sxs-lookup"><span data-stu-id="e9339-110">This improved capability to isolate applications is an important part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="e9339-111">Weitere Informationen finden Sie unter [isolierte Anwendungen und](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)parallele Assemblys.</span><span class="sxs-lookup"><span data-stu-id="e9339-111">For more information, see [Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span></span>

<span data-ttu-id="e9339-112">In den folgenden Abschnitten wird die Verwendung von Assemblys mit dem-Windows Installer beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e9339-112">The following sections describe the use of assemblies with the Windows Installer.</span></span>

-   [<span data-ttu-id="e9339-113">Hinzufügen von Assemblys zu Paketen</span><span class="sxs-lookup"><span data-stu-id="e9339-113">Adding Assemblies to a Package</span></span>](adding-assemblies-to-a-package.md)
-   [<span data-ttu-id="e9339-114">Installieren und Entfernen von Assemblys</span><span class="sxs-lookup"><span data-stu-id="e9339-114">Installing and Removing Assemblies</span></span>](installing-and-removing-assemblies.md)
-   [<span data-ttu-id="e9339-115">Aktualisieren von Assemblys</span><span class="sxs-lookup"><span data-stu-id="e9339-115">Updating Assemblies</span></span>](updating-assemblies.md)
-   [<span data-ttu-id="e9339-116">Neuinstallations Modi von Common Language Runtime-Assemblys</span><span class="sxs-lookup"><span data-stu-id="e9339-116">Reinstallation Modes of Common Language Runtime Assemblies</span></span>](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [<span data-ttu-id="e9339-117">Von Windows Installer geschriebene assemblyregistrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="e9339-117">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)

<span data-ttu-id="e9339-118">Informationen zum Installieren von com-und com+ 1,0-Anwendungen finden Sie unter [Installieren einer COM+-Anwendung mit dem Windows Installer](installing-a-com--application-with-the-windows-installer.md), [Installieren einer COM-Komponente an einem privaten Speicherort](installing-a-com-component-to-a-private-location.md)und [Erstellen einer COM-Komponente in einem vorhandenen Paket](make-a-com-component-in-an-existing-package-private.md).</span><span class="sxs-lookup"><span data-stu-id="e9339-118">For information about installing COM and COM+ 1.0 applications, see [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md), [Installing a COM Component to a Private Location](installing-a-com-component-to-a-private-location.md), and [Make a COM Component in an Existing Package Private](make-a-com-component-in-an-existing-package-private.md).</span></span>

 

 
