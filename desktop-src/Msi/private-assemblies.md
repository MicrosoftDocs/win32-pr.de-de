---
description: Eine Win32-Assembly kann als private Assembly installiert und exklusiv für eine Anwendung verwendet werden. Private Assemblys sollten von einem Windows Installer Paket installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Private Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1073426e080cc4b8b30358ce26feb99515abb185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216356"
---
# <a name="private-assemblies"></a><span data-ttu-id="be786-104">Private Assemblys</span><span class="sxs-lookup"><span data-stu-id="be786-104">Private Assemblies</span></span>

<span data-ttu-id="be786-105">Eine Win32-Assembly kann als private Assembly installiert und exklusiv für eine Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be786-105">A Win32 assembly can be installed as a private assembly and be exclusively available for use by one application.</span></span> <span data-ttu-id="be786-106">Private Assemblys sollten von einem Windows Installer Paket installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be786-106">Private assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="be786-107">Unter Windows XP werden private Assemblys als [parallele](side-by-side-assemblies.md)Assemblys installiert.</span><span class="sxs-lookup"><span data-stu-id="be786-107">On Windows XP, private assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="be786-108">Der Windows Installer installiert private parallele Assemblys in einem Ordner, der für die Anwendung privat ist.</span><span class="sxs-lookup"><span data-stu-id="be786-108">The Windows Installer installs private side-by-side assemblies in a folder private to the application.</span></span> <span data-ttu-id="be786-109">Üblicherweise der Ordner, der die ausführbare Datei der Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="be786-109">Commonly the folder that contains the applications executable file.</span></span> <span data-ttu-id="be786-110">Die Abhängigkeit der Anwendung auf dem private Assembly wird in einer Anwendungs Manifest-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="be786-110">The dependency of the application on the private assembly is specified in an application manifest file.</span></span> <span data-ttu-id="be786-111">Weitere Informationen finden Sie unter [isolierte Anwendungen und](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)parallele Assemblys.</span><span class="sxs-lookup"><span data-stu-id="be786-111">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="be786-112">Auf älteren Betriebssystemen als Windows XP wird eine Kopie der private Assembly und einer lokalen Datei in einem privaten Ordner installiert, um die Anwendung exklusiv zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="be786-112">On operating systems earlier than Windows XP, a copy of the private assembly and a .local file is installed into a private folder for the exclusive use of the application.</span></span> <span data-ttu-id="be786-113">Eine Version der Assembly wird auch global auf dem System registriert und steht für jede Anwendung zur Verfügung, die Sie bindet.</span><span class="sxs-lookup"><span data-stu-id="be786-113">A version of the assembly is also globally registered on the system and available for any application that binds to it.</span></span> <span data-ttu-id="be786-114">Die globale Version der Assembly kann die Version sein, die mit der Anwendung installiert wird, oder eine frühere Version.</span><span class="sxs-lookup"><span data-stu-id="be786-114">The global version of the assembly may be the version installed with the application or an earlier version.</span></span> <span data-ttu-id="be786-115">Die globale Version wird durch die gleichen Regeln festgelegt, die von [isolierten Komponenten](isolated-components.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be786-115">The global version is determined by the same rules use by [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="be786-116">Beachten Sie, dass die Windows Installer eine private Assembly nicht an einem Speicherort mit einem Pfad mit mehr als 234 Zeichen installieren kann, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="be786-116">Note that the Windows Installer cannot install a private assembly in a location having a path that contains more than 234 characters, including the terminating null character.</span></span>

 

 
