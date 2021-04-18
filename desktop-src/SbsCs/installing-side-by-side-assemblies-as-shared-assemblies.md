---
description: Im folgenden Verfahren wird beschrieben, wie parallele Assemblys als freigegebene Assemblys installiert werden.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Installieren paralleler Assemblys als freigegebene Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484643"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a><span data-ttu-id="6e6e9-103">Installieren paralleler Assemblys als freigegebene Assemblys</span><span class="sxs-lookup"><span data-stu-id="6e6e9-103">Installing Side-by-side Assemblies as Shared Assemblies</span></span>

<span data-ttu-id="6e6e9-104">Im folgenden Verfahren wird beschrieben, wie parallele Assemblys als [frei](about-side-by-side-assemblies-.md) [gegebene](/windows/desktop/Msi/shared-assemblies)Assemblys installiert werden.</span><span class="sxs-lookup"><span data-stu-id="6e6e9-104">The following procedure describes how to install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [shared assemblies](/windows/desktop/Msi/shared-assemblies).</span></span>

<span data-ttu-id="6e6e9-105">**So installieren Sie eine parallele Assembly als freigegebene Assembly**</span><span class="sxs-lookup"><span data-stu-id="6e6e9-105">**To install a side-by-side assembly as a shared assembly**</span></span>

1.  <span data-ttu-id="6e6e9-106">Signieren Sie einen Katalog für die Dateien in der Assembly, und erstellen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="6e6e9-106">Sign and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="6e6e9-107">Dateien müssen signiert werden, damit Sie als parallele Assemblys installiert werden.</span><span class="sxs-lookup"><span data-stu-id="6e6e9-107">Files must be signed to install them as side-by-side assemblies.</span></span> <span data-ttu-id="6e6e9-108">Weitere Informationen finden Sie [unter Erstellen signierter Dateien und Kataloge](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="6e6e9-108">For more information, see [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

2.  <span data-ttu-id="6e6e9-109">Sie sollten freigegebene parallele Assemblys als Komponenten eines Windows Installer Pakets installieren.</span><span class="sxs-lookup"><span data-stu-id="6e6e9-109">You should install shared side-by-side assemblies as components of a Windows Installer package.</span></span> <span data-ttu-id="6e6e9-110">Dabei kann es sich um das Installationspaket handeln, mit dem die Anwendung installiert oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6e6e9-110">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="6e6e9-111">Wenn die freigegebene Assembly als Teil mehrerer Anwendungen ausgeliefert wird, sollten Sie ein Mergemodul bereitstellen, das in die Installationspakete dieser Anwendungen eingebunden werden kann, und einen Katalog für die Dateien in der Assembly erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e6e9-111">If the shared assembly is shipped as part of multiple applications, you should provide a merge module that can be incorporated into these applications' installation packages and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="6e6e9-112">Zum Installieren von Assemblys ist Windows Installer Version 2,0 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6e6e9-112">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="6e6e9-113">Weitere Informationen finden Sie im [Windows Installer](../msi/windows-installer-portal.md) SDK und in den Abschnitten unter [Installieren von Win32](../msi/installation-of-win32-assemblies.md)-Assemblys.</span><span class="sxs-lookup"><span data-stu-id="6e6e9-113">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

 

 
