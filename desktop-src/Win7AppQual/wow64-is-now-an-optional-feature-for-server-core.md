---
description: .
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: WOW64-Status in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a121c6bb9c4fb2cd052825bb4c2d5e3dbd0183c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366282"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a><span data-ttu-id="aa947-103">WOW64 ist jetzt ein optionales Feature für Server Core.</span><span class="sxs-lookup"><span data-stu-id="aa947-103">WoW64 Is Now an Optional Feature for Server Core</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="aa947-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="aa947-104">Affected Platforms</span></span>

<span data-ttu-id="aa947-105">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa947-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="aa947-106">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="aa947-106">Feature Impact</span></span>

 <span data-ttu-id="aa947-107">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="aa947-107">**Severity** - Low</span></span>  
<span data-ttu-id="aa947-108">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="aa947-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="aa947-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa947-109">Description</span></span>

<span data-ttu-id="aa947-110">Mit der Server Core-Installationsoption für Windows Server 2008 R2 können Sie WOW64 deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="aa947-110">The Server Core installation option for Windows Server 2008 R2 allows you to uninstall WoW64.</span></span> <span data-ttu-id="aa947-111">WOW64 ist jetzt ein optionales Feature, das Sie deinstallieren können, wenn es nicht erforderlich ist, 32-Bit-Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="aa947-111">WoW64 is now an optional feature that you can uninstall if it is not necessary to run 32-bit code.</span></span>

<span data-ttu-id="aa947-112">Außerdem ist für die Active Directory-und Active Directory Lightweight Directory Services Rollen WOW64 erforderlich, um unter Windows Server 2008 R2 ausgeführt werden zu können.</span><span class="sxs-lookup"><span data-stu-id="aa947-112">In addition, the Active Directory and Active Directory Lightweight Directory Services roles require WoW64 in order to run in Windows Server 2008 R2.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="aa947-113">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="aa947-113">Manifestation of Impact</span></span>

<span data-ttu-id="aa947-114">Wenn Sie WOW64 deinstallieren, erhalten Administratoren, die 32-Bit-Code auf Server Core ausführen, eine Fehlermeldung, dass die Anwendung nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="aa947-114">If you uninstall WoW64, Administrators running 32-bit code on Server Core will receive an error message that the application cannot be executed.</span></span> <span data-ttu-id="aa947-115">Wenn Administratoren versuchen, Active Directory und Active Directory Lightweight Directory Services auszuführen, erhalten Sie eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="aa947-115">If Administrators attempt to run Active Directory and Active Directory Lightweight Directory Services, they will receive an error message.</span></span>

## <a name="mitigation"></a><span data-ttu-id="aa947-116">Minderung</span><span class="sxs-lookup"><span data-stu-id="aa947-116">Mitigation</span></span>

<span data-ttu-id="aa947-117">Installieren Sie WOW64.</span><span class="sxs-lookup"><span data-stu-id="aa947-117">Install WoW64.</span></span>

## <a name="solution"></a><span data-ttu-id="aa947-118">Lösung</span><span class="sxs-lookup"><span data-stu-id="aa947-118">Solution</span></span>

<span data-ttu-id="aa947-119">Die bevorzugte Lösung besteht darin, eine 64-Bit-Version des Codes bereitzustellen, damit Sie auf Server Core ausgeführt werden kann, ohne dass WOW64 erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="aa947-119">The preferred solution is to provide a 64-bit version of the code to enable it to run on Server Core without needing WoW64.</span></span>

<span data-ttu-id="aa947-120">Geben Sie mindestens eine Benutzerdokumentation an, die darauf hinweist, dass zum Ausführen von 32-Bit-Code WOW64 installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="aa947-120">At a minimum, provide user documentation noting that to run 32-bit code they must install WoW64.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="aa947-121">Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="aa947-121">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="aa947-122">Vergewissern Sie sich, dass der gesamte verwendete Code 64-Bit ist.</span><span class="sxs-lookup"><span data-stu-id="aa947-122">Verify that all code used is 64-bit.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="aa947-123">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aa947-123">Links to Other Resources</span></span>

-   [<span data-ttu-id="aa947-124">WOW64-Implementierungs Details</span><span class="sxs-lookup"><span data-stu-id="aa947-124">WOW64 Implementation Details</span></span>](../winprog64/wow64-implementation-details.md)
-   [<span data-ttu-id="aa947-125">Debuggen WOW64</span><span class="sxs-lookup"><span data-stu-id="aa947-125">Debugging WOW64</span></span>](../winprog64/debugging-wow64.md)
-   <span data-ttu-id="aa947-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa947-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>

 

 
