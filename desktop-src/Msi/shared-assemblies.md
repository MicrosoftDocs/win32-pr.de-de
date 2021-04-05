---
description: Eine Win32-Assembly kann als freigegebene Assembly installiert werden und steht für die Verwendung durch mehrere Anwendungen auf dem Computer zur Verfügung. Freigegebene Assemblys sollten von einem Windows Installer Paket installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Freigegebene Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757812"
---
# <a name="shared-assemblies"></a><span data-ttu-id="06e45-104">Freigegebene Assemblys</span><span class="sxs-lookup"><span data-stu-id="06e45-104">Shared Assemblies</span></span>

<span data-ttu-id="06e45-105">Eine Win32-Assembly kann als freigegebene Assembly installiert werden und steht für die Verwendung durch mehrere Anwendungen auf dem Computer zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="06e45-105">A Win32 assembly can be installed as a shared assembly and be available for use by multiple applications on the computer.</span></span> <span data-ttu-id="06e45-106">Freigegebene Assemblys sollten von einem Windows Installer Paket installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06e45-106">Shared assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="06e45-107">Freigegebene Assemblys [werden als parallele](side-by-side-assemblies.md)Assemblys installiert.</span><span class="sxs-lookup"><span data-stu-id="06e45-107">Shared assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="06e45-108">Der-Windows Installer installiert freigegebene parallele Assemblys im Ordner WinSxS.</span><span class="sxs-lookup"><span data-stu-id="06e45-108">The Windows Installer installs shared side-by-side assemblies into the Winsxs folder.</span></span> <span data-ttu-id="06e45-109">Die Assemblys sind nicht global auf dem System registriert, aber Sie sind global für jede Anwendung verfügbar, die eine Abhängigkeit von der Assembly in einer Manifest-Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="06e45-109">The assemblies are not registered globally on the system, but they are globally available to any application that specifies a dependency on the assembly in a manifest file.</span></span> <span data-ttu-id="06e45-110">Weitere Informationen finden Sie unter [isolierte Anwendungen und](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)parallele Assemblys.</span><span class="sxs-lookup"><span data-stu-id="06e45-110">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="06e45-111">Auf älteren Betriebssystemen als Windows XP werden freigegebene Assemblys normalerweise im Windows-Systemordner installiert und Global registriert.</span><span class="sxs-lookup"><span data-stu-id="06e45-111">On operating systems earlier than Windows XP, shared assemblies are usually installed in the Windows system folder and registered globally.</span></span> <span data-ttu-id="06e45-112">Die neueste installierte Version ist für jede Anwendung verfügbar, die Sie bindet.</span><span class="sxs-lookup"><span data-stu-id="06e45-112">The latest installed version is available to any application that binds to it.</span></span>

<span data-ttu-id="06e45-113">Informationen zum Erstellen eines Windows Installer Pakets für die Installation einer freigegebenen Assembly finden Sie in den folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="06e45-113">For information on how to author a Windows Installer package to install a shared assembly, see the following:</span></span>

-   [<span data-ttu-id="06e45-114">Installieren von Win32-Assemblys für die parallele Freigabe unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="06e45-114">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="06e45-115">Installieren von Win32-Assemblys für die private Verwendung einer Anwendung unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="06e45-115">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
