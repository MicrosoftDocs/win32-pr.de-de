---
description: Installieren Sie Win32-Assemblys, indem Sie Sie zu einer Komponente Microsoft Windows Installer Pakets, das die Anwendung installiert oder aktualisiert.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Installation von Win32-Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348254"
---
# <a name="installation-of-win32-assemblies"></a><span data-ttu-id="cdfcb-103">Installation von Win32-Assemblys</span><span class="sxs-lookup"><span data-stu-id="cdfcb-103">Installation of Win32 Assemblies</span></span>

<span data-ttu-id="cdfcb-104">Installieren Sie Win32-Assemblys, indem Sie Sie zu einer Komponente Microsoft Windows Installer Pakets, das die Anwendung installiert oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cdfcb-104">Install Win32 assemblies by making them a component of Microsoft Windows Installer package that installs or updates your application.</span></span> <span data-ttu-id="cdfcb-105">Wenn Sie die [MsiAssembly-Tabelle](msiassembly-table.md) und die [MsiAssemblyName-Tabelle](msiassemblyname-table.md)erstellen, wird die Komponente in der Component- \_ Spalte als Assembly identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cdfcb-105">When you author the [MsiAssembly table](msiassembly-table.md) and [MsiAssemblyName table](msiassemblyname-table.md), this identifies the component in the Component\_ column as an assembly.</span></span> <span data-ttu-id="cdfcb-106">Das Installationsprogramm legt die [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) -Eigenschaft auf die Dateiversion von Sxs.dll unter Betriebssystemen fest, die Win32-Assemblys unterstützen und andernfalls diese Eigenschaft nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="cdfcb-106">The installer will set the [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) property to the file version of Sxs.dll on operating systems that can support Win32 assemblies and not set this property otherwise.</span></span>

<span data-ttu-id="cdfcb-107">In Windows Vista und Windows XP werden von Windows Installer keine Assemblyinformationen in die Registrierung geschrieben.</span><span class="sxs-lookup"><span data-stu-id="cdfcb-107">In Windows Vista and Windows XP, Windows Installer does not write assembly information into the registry.</span></span> <span data-ttu-id="cdfcb-108">Außerdem können freigegebene Assemblys, private Assemblys und parallele Assemblys verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cdfcb-108">In addition, shared assemblies, private assemblies, and side-by-side assemblies can be used.</span></span> <span data-ttu-id="cdfcb-109">Weitere Informationen finden Sie unter [frei](side-by-side-assemblies.md) [gegebene](shared-assemblies.md)Assemblys, [private](private-assemblies.md)Assemblys und parallele Assemblys.</span><span class="sxs-lookup"><span data-stu-id="cdfcb-109">For information, see [Shared Assemblies](shared-assemblies.md), [Private Assemblies](private-assemblies.md), and [Side-by-Side Assemblies](side-by-side-assemblies.md).</span></span>

<span data-ttu-id="cdfcb-110">In den folgenden Abschnitten wird beschrieben, wie ein Windows Installer Paket zum Installieren von Win32-Assemblys als freigegeben, privat oder nebeneinander auf verschiedenen Windows-Betriebssystemen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cdfcb-110">The following sections describe how to author a Windows Installer package to install Win32 assemblies as shared, private, or side-by-side on different Windows operating systems.</span></span>

-   [<span data-ttu-id="cdfcb-111">Installieren von Win32-Assemblys für die parallele Freigabe unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="cdfcb-111">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="cdfcb-112">Installieren von Win32-Assemblys für die private Verwendung einer Anwendung unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="cdfcb-112">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



