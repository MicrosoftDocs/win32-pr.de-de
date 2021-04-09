---
description: Comrepl ist ein Hilfsprogramm, mit dem der com+-Katalog von einem bestimmten Quellcomputer auf einem oder mehreren Ziel Computern repliziert wird.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: Das Hilfsprogramm zur Comrepl-Replikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958531"
---
# <a name="the-comrepl-replication-utility"></a><span data-ttu-id="49c72-103">Das Hilfsprogramm zur Comrepl-Replikation</span><span class="sxs-lookup"><span data-stu-id="49c72-103">The COMREPL Replication Utility</span></span>

<span data-ttu-id="49c72-104">Comrepl ist ein Hilfsprogramm, mit dem der com+-Katalog von einem bestimmten Quellcomputer auf einem oder mehreren Ziel Computern repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="49c72-104">COMREPL is a utility that will replicate the COM+ catalog from a given source computer to one or more target computers.</span></span> <span data-ttu-id="49c72-105">Stellen Sie sich den Quellcomputer vor, der eine "Master Konfiguration" darstellt.</span><span class="sxs-lookup"><span data-stu-id="49c72-105">Think of the source computer representing a "master configuration."</span></span> <span data-ttu-id="49c72-106">Mit Comrepl wird diese Master Konfiguration repliziert, um einen Satz identisch konfigurierter Computer beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="49c72-106">COMREPL is used to replicate this master configuration to maintain a set of identically configured computers.</span></span>

<span data-ttu-id="49c72-107">Die Replikations Einheit ist die gesamte com+-Konfiguration auf dem Master Computer.</span><span class="sxs-lookup"><span data-stu-id="49c72-107">The unit of replication is the entire COM+ configuration on the master computer.</span></span> <span data-ttu-id="49c72-108">Alle com+-Anwendungen auf dem Master werden auf den Ziel Computern repliziert. Alles oder nichts.</span><span class="sxs-lookup"><span data-stu-id="49c72-108">All COM+ applications on the master are replicated to the target computers; it's all or nothing.</span></span> <span data-ttu-id="49c72-109">Außerdem werden alle com+-Anwendungen, die zuvor auf den Ziel Computern installiert wurden, mit Ausnahme der vorinstallierten com+-Anwendungen, im Rahmen des Replikations Prozesses gelöscht.</span><span class="sxs-lookup"><span data-stu-id="49c72-109">In addition, all COM+ applications previously installed on the target computers, with the exception of the COM+ preinstalled applications, will be deleted as part of the replication process.</span></span>

<span data-ttu-id="49c72-110">Comrepl repliziert nur com+-Konfigurationsdaten.</span><span class="sxs-lookup"><span data-stu-id="49c72-110">COMREPL replicates only COM+ configuration data.</span></span> <span data-ttu-id="49c72-111">Dies schließt com+-Anwendungen und com+-spezifische Computereinstellungen ein.</span><span class="sxs-lookup"><span data-stu-id="49c72-111">This includes COM+ applications and COM+ specific computer settings.</span></span> <span data-ttu-id="49c72-112">Microsoft Internetinformationsdienste (IIS) verfügt über ein ähnliches Dienstprogramm (Iissync), das Comrepl zum Replizieren von IIS-und com+-Konfigurationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="49c72-112">Microsoft Internet Information Services (IIS) has a similar utility (IISSync), which makes use of COMREPL to replicate IIS and COM+ configuration.</span></span>

<span data-ttu-id="49c72-113">Ausführliche Informationen zum Starten und Verwenden von Comrepl finden Sie in den folgenden Themen in diesem Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="49c72-113">For detailed information on launching and using COMREPL, see the following topics in this section:</span></span>

-   [<span data-ttu-id="49c72-114">Verwenden von Comrepl</span><span class="sxs-lookup"><span data-stu-id="49c72-114">Using COMREPL</span></span>](using-comrepl.md)
-   [<span data-ttu-id="49c72-115">Was wird repliziert?</span><span class="sxs-lookup"><span data-stu-id="49c72-115">What Gets Replicated</span></span>](what-gets-replicated.md)
-   [<span data-ttu-id="49c72-116">Replikations Phasen</span><span class="sxs-lookup"><span data-stu-id="49c72-116">Replication Phases</span></span>](replication-phases.md)
-   [<span data-ttu-id="49c72-117">Dateiverwaltung</span><span class="sxs-lookup"><span data-stu-id="49c72-117">File Management</span></span>](file-management.md)
-   [<span data-ttu-id="49c72-118">Protokollierung und Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="49c72-118">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)

## <a name="related-topics"></a><span data-ttu-id="49c72-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49c72-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49c72-120">Installationspakete für COM+-Anwendungen werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="49c72-120">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="49c72-121">Anwendungs Proxys</span><span class="sxs-lookup"><span data-stu-id="49c72-121">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="49c72-122">Der com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="49c72-122">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 



