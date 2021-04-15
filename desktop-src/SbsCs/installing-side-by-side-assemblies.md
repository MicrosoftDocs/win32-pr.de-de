---
description: Parallele Assemblys können als freigegebene Assemblys oder als private Assemblys installiert werden. Weitere Informationen finden Sie unter Installieren paralleler Assemblys als private Assemblys und Installieren paralleler Assemblys als freigegebene Assemblys.
ms.assetid: 36f271ff-be0c-4162-8e1c-86088ebddbcc
title: Parallele Assemblys werden installiert.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be68580c7f0e3890c2e53b148daec92fbad18ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484638"
---
# <a name="installing-side-by-side-assemblies"></a><span data-ttu-id="fc91f-104">Parallele Assemblys werden installiert.</span><span class="sxs-lookup"><span data-stu-id="fc91f-104">Installing Side-by-side Assemblies</span></span>

<span data-ttu-id="fc91f-105">Parallele Assemblys können als frei [gegebene](/windows/desktop/Msi/shared-assemblies) Assemblys oder als [private](/windows/desktop/Msi/private-assemblies)Assemblys installiert werden.</span><span class="sxs-lookup"><span data-stu-id="fc91f-105">You may install side-by-side assemblies as [shared assemblies](/windows/desktop/Msi/shared-assemblies) or as [private assemblies](/windows/desktop/Msi/private-assemblies).</span></span> <span data-ttu-id="fc91f-106">Weitere Informationen finden Sie unter Installieren paralleler Assemblys [als private](installing-side-by-side-assemblies-as-private-assemblies.md) Assemblys und Installieren paralleler Assemblys [als freigegebene](installing-side-by-side-assemblies-as-shared-assemblies.md)Assemblys.</span><span class="sxs-lookup"><span data-stu-id="fc91f-106">For more information, see [Installing Side-by-Side Assemblies as Private Assemblies](installing-side-by-side-assemblies-as-private-assemblies.md) and [Installing Side-by-side Assemblies as Shared Assemblies](installing-side-by-side-assemblies-as-shared-assemblies.md).</span></span>

<span data-ttu-id="fc91f-107">Beachten Sie dabei Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fc91f-107">Note that:</span></span>

-   <span data-ttu-id="fc91f-108">Assemblys, die im globalen Assemblycache durch eine Installation mithilfe des [Installations Kontexts](/windows/desktop/Msi/installation-context) pro Benutzer installiert werden, werden nicht durch den Windows-Datei Schutz geschützt.</span><span class="sxs-lookup"><span data-stu-id="fc91f-108">Assemblies installed to the global assembly cache by an installation using the per-user [installation context](/windows/desktop/Msi/installation-context) are not protected by Windows File Protection.</span></span>
-   <span data-ttu-id="fc91f-109">Assemblys, die durch eine Installation im globalen Assemblycache mithilfe des [Installations Kontexts](/windows/desktop/Msi/installation-context) pro Computer installiert werden, werden durch den Windows-Datei Schutz geschützt.</span><span class="sxs-lookup"><span data-stu-id="fc91f-109">Assemblies that are installed to the global assembly cache by an installation using the per-machine [installation context](/windows/desktop/Msi/installation-context) are protected by Windows File Protection.</span></span>

 

 
