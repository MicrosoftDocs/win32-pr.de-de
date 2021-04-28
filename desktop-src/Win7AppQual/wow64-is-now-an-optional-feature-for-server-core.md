---
description: WoW64 ist jetzt ein optionales Feature für Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: WoW64-Status in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad947dac85707d3c9c89a2cffea38c4a4850a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084048"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a><span data-ttu-id="f4e0b-103">WoW64 ist jetzt ein optionales Feature für Server Core</span><span class="sxs-lookup"><span data-stu-id="f4e0b-103">WoW64 Is Now an Optional Feature for Server Core</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="f4e0b-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="f4e0b-104">Affected Platforms</span></span>

<span data-ttu-id="f4e0b-105">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4e0b-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="f4e0b-106">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="f4e0b-106">Feature Impact</span></span>

 <span data-ttu-id="f4e0b-107">**Schweregrad:** Niedrig</span><span class="sxs-lookup"><span data-stu-id="f4e0b-107">**Severity** - Low</span></span>  
<span data-ttu-id="f4e0b-108">**Häufigkeit** – Niedrig</span><span class="sxs-lookup"><span data-stu-id="f4e0b-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="f4e0b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4e0b-109">Description</span></span>

<span data-ttu-id="f4e0b-110">Mit der Server Core-Installationsoption für Windows Server 2008 R2 können Sie WoW64 deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="f4e0b-110">The Server Core installation option for Windows Server 2008 R2 allows you to uninstall WoW64.</span></span> <span data-ttu-id="f4e0b-111">WoW64 ist jetzt ein optionales Feature, das Sie deinstallieren können, wenn 32-Bit-Code nicht ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="f4e0b-111">WoW64 is now an optional feature that you can uninstall if it is not necessary to run 32-bit code.</span></span>

<span data-ttu-id="f4e0b-112">Darüber hinaus erfordern die Rollen Active Directory und Active Directory Lightweight Directory Services WoW64, um in Windows Server 2008 R2 ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="f4e0b-112">In addition, the Active Directory and Active Directory Lightweight Directory Services roles require WoW64 in order to run in Windows Server 2008 R2.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="f4e0b-113">Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="f4e0b-113">Manifestation of Impact</span></span>

<span data-ttu-id="f4e0b-114">Wenn Sie WoW64 deinstallieren, erhalten Administratoren, die 32-Bit-Code auf Server Core ausführen, eine Fehlermeldung, dass die Anwendung nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4e0b-114">If you uninstall WoW64, Administrators running 32-bit code on Server Core will receive an error message that the application cannot be executed.</span></span> <span data-ttu-id="f4e0b-115">Wenn Administratoren versuchen, Active Directory und Active Directory Lightweight Directory Services ausführen, erhalten sie eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="f4e0b-115">If Administrators attempt to run Active Directory and Active Directory Lightweight Directory Services, they will receive an error message.</span></span>

## <a name="mitigation"></a><span data-ttu-id="f4e0b-116">Minderung</span><span class="sxs-lookup"><span data-stu-id="f4e0b-116">Mitigation</span></span>

<span data-ttu-id="f4e0b-117">Installieren Sie WoW64.</span><span class="sxs-lookup"><span data-stu-id="f4e0b-117">Install WoW64.</span></span>

## <a name="solution"></a><span data-ttu-id="f4e0b-118">Lösung</span><span class="sxs-lookup"><span data-stu-id="f4e0b-118">Solution</span></span>

<span data-ttu-id="f4e0b-119">Die bevorzugte Lösung besteht in der Bereitstellung einer 64-Bit-Version des Codes, um die Ausführung auf Server Core ohne WoW64 zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f4e0b-119">The preferred solution is to provide a 64-bit version of the code to enable it to run on Server Core without needing WoW64.</span></span>

<span data-ttu-id="f4e0b-120">Stellen Sie zumindest eine Benutzerdokumentation zur Verfügung, in der Sie darauf hindechen, dass Zum Ausführen von 32-Bit-Code WoW64 installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="f4e0b-120">At a minimum, provide user documentation noting that to run 32-bit code they must install WoW64.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="f4e0b-121">Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Nutzbarkeitstests</span><span class="sxs-lookup"><span data-stu-id="f4e0b-121">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="f4e0b-122">Stellen Sie sicher, dass der verwendete Code 64-Bit ist.</span><span class="sxs-lookup"><span data-stu-id="f4e0b-122">Verify that all code used is 64-bit.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="f4e0b-123">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f4e0b-123">Links to Other Resources</span></span>

-   [<span data-ttu-id="f4e0b-124">WOW64-Implementierungsdetails</span><span class="sxs-lookup"><span data-stu-id="f4e0b-124">WOW64 Implementation Details</span></span>](../winprog64/wow64-implementation-details.md)
-   [<span data-ttu-id="f4e0b-125">Debuggen von WOW64</span><span class="sxs-lookup"><span data-stu-id="f4e0b-125">Debugging WOW64</span></span>](../winprog64/debugging-wow64.md)
-   <span data-ttu-id="f4e0b-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4e0b-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>

 

 
