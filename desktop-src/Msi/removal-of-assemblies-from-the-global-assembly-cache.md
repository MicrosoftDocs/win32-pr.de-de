---
description: Der Windows Installer bestimmt, ob das Entfernen einer Common Language Runtime Assembly basierend auf einer Client Liste zulässig ist, die unabhängig von der Assembly gespeichert wird.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Entfernen von Assemblys aus dem globalen Assemblycache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216033"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a><span data-ttu-id="baf82-103">Entfernen von Assemblys aus dem globalen Assemblycache</span><span class="sxs-lookup"><span data-stu-id="baf82-103">Removal of Assemblies from the Global Assembly Cache</span></span>

<span data-ttu-id="baf82-104">Der Windows Installer bestimmt, ob das Entfernen einer Common Language Runtime Assembly basierend auf einer Client Liste zulässig ist, die unabhängig von der Assembly gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="baf82-104">The Windows Installer determines whether to allow the removal of a common language runtime assembly based upon a client list it keeps independently of the assembly.</span></span> <span data-ttu-id="baf82-105">Der Windows Installer behält ein Pin-Bit bei, das Windows Installer Clients der Assembly repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="baf82-105">The Windows Installer keeps one pin bit to represent Windows Installer clients of the assembly.</span></span> <span data-ttu-id="baf82-106">Das Installationsprogramm heftet die Assembly für den ersten Windows Installer Client an und entheftet Sie, wenn der letzte Windows Installer Client entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="baf82-106">The installer pins the assembly for the first Windows Installer client and unpins it when the last Windows Installer client is removed.</span></span> <span data-ttu-id="baf82-107">Die Assembly verwaltet ein Pin-Bit für jeden Client einer Assembly.</span><span class="sxs-lookup"><span data-stu-id="baf82-107">The assembly maintains a pin bit for every client of an assembly.</span></span>

<span data-ttu-id="baf82-108">Der Windows Installer ist nicht direkt verantwortlich für das physische Entfernen von Common Language Runtime Assemblys vom Computer.</span><span class="sxs-lookup"><span data-stu-id="baf82-108">The Windows Installer is not directly responsible for the physical removal of common language runtime assemblies from the computer.</span></span> <span data-ttu-id="baf82-109">Der Installer entfernt die Assembly, wenn der letzte Windows Installer Client entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="baf82-109">The installer unpins the assembly when the last Windows Installer client is removed.</span></span> <span data-ttu-id="baf82-110">Wenn die Windows Installer der letzte Client der Assembly ist, stellt die Common Language Runtime die Option bereit, eine synchrone Bereinigung der Assembly zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="baf82-110">If the Windows Installer is the last client of the assembly, the common language runtime provides the option to force a synchronous cleanup of the assembly.</span></span> <span data-ttu-id="baf82-111">Der Bereinigungs Prozess ist atomarisch, und an dieser Stelle wird kein "Rollback" bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="baf82-111">The cleanup process is atomic and there is no provision for a "rollback" at this point.</span></span> <span data-ttu-id="baf82-112">Alle Assemblys von Common Language Runtime Assemblys müssen auftreten, nachdem der Benutzer die Installation oder Entfernung abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="baf82-112">All unpinning of common language runtime assemblies must occur after the user has had a chance to cancel the installation or removal.</span></span>

 

 



