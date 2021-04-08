---
description: Jede parallele Assembly muss eine Version aufweisen.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Assemblyversionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757315"
---
# <a name="assembly-versions"></a><span data-ttu-id="722ec-103">Assemblyversionen</span><span class="sxs-lookup"><span data-stu-id="722ec-103">Assembly Versions</span></span>

<span data-ttu-id="722ec-104">Jede parallele Assembly muss eine Version aufweisen.</span><span class="sxs-lookup"><span data-stu-id="722ec-104">Every side-by-side assembly must have a version.</span></span> <span data-ttu-id="722ec-105">Jede Assemblyversion ist einer Versionsnummer zugeordnet, die vier Teile durch Punkte trennt: *Major. Minor. Build. Revision*.</span><span class="sxs-lookup"><span data-stu-id="722ec-105">Each assembly version is associated with a version number having four parts separated by periods: *major.minor.build.revision*.</span></span> <span data-ttu-id="722ec-106">Wenn eine Assembly geändert wird, sodass Sie mit den vorhandenen Versionen nicht kompatibel ist, müssen die *Haupt* -oder *nebenteile* der Versionsnummer geändert werden.</span><span class="sxs-lookup"><span data-stu-id="722ec-106">If a change is made to an assembly making it incompatible with existing versions, the *major* or *minor* parts of the version number must be changed.</span></span> <span data-ttu-id="722ec-107">Eine Versionsnummer, die nur in den *Build* -oder *Revisions* Teilen geändert wird, gibt an, dass die Assembly abwärts kompatibel mit früheren Versionen ist.</span><span class="sxs-lookup"><span data-stu-id="722ec-107">A version number that changes only in the *build* or *revision* parts indicates that the assembly is backward compatible with prior versions.</span></span>

<span data-ttu-id="722ec-108">Die Version muss in **assemblyIdentity** -Elementen der [Manifeste](manifests.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="722ec-108">The version must be specified in **assemblyIdentity** elements of [manifests](manifests.md).</span></span> <span data-ttu-id="722ec-109">Verwenden Sie das vierteilige Versions Format: mmmmm. nnnnn. Ooooo. ppppp.</span><span class="sxs-lookup"><span data-stu-id="722ec-109">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="722ec-110">Alle durch Zeiträume getrennten Teile können 0-65535 einschließlich sein.</span><span class="sxs-lookup"><span data-stu-id="722ec-110">Each of the parts separated by periods can be 0-65535 inclusive.</span></span>

 

 



