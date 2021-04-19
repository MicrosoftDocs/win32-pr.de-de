---
description: Um parallele Assemblys als private Assemblys zu installieren, können Sie die Assembly als Komponente eines Installer-Pakets installieren.
ms.assetid: 1cfd836f-a1b9-4339-8756-5488c88b3c2b
title: Parallele Assemblys als private Assemblys installieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7719a9887f9e92d81e2ad65fe2e75424f0b6957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348150"
---
# <a name="installing-side-by-side-assemblies-as-private-assemblies"></a><span data-ttu-id="60b68-103">Parallele Assemblys als private Assemblys installieren</span><span class="sxs-lookup"><span data-stu-id="60b68-103">Installing Side-by-side Assemblies as Private Assemblies</span></span>

<span data-ttu-id="60b68-104">Um parallele Assemblys als [private](/windows/desktop/Msi/private-assemblies)Assemblys zu installieren, können Sie die Assembly als Komponente eines Installer- [Pakets installieren.](about-side-by-side-assemblies-.md)</span><span class="sxs-lookup"><span data-stu-id="60b68-104">To install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [private assemblies](/windows/desktop/Msi/private-assemblies), you can install the assembly as a component of an installer package.</span></span> <span data-ttu-id="60b68-105">Dabei kann es sich um das Installationspaket handeln, mit dem die Anwendung installiert oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="60b68-105">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="60b68-106">Zum Installieren von Assemblys ist Windows Installer Version 2,0 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="60b68-106">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="60b68-107">Weitere Informationen finden Sie im [Windows Installer](../msi/windows-installer-portal.md) SDK und in den Abschnitten unter [Installieren von Win32](../msi/installation-of-win32-assemblies.md)-Assemblys.</span><span class="sxs-lookup"><span data-stu-id="60b68-107">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="60b68-108">Als Alternative können Sie das Installationsprogramm verwenden, um eine private Assembly und ein Manifest in denselben Ordner wie die ausführbare Datei der Anwendung zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="60b68-108">As an alternative, you can use the installer to copy a private assembly and manifest into the same folder as the application's executable file.</span></span>

 

 
