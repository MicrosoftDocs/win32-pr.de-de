---
title: Replikation und Datenintegrität
description: Active Directory Domain Services eine Multimasteraktualisierung bereitstellen.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, Verwendung, Replikation und Datenintegrität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341419"
---
# <a name="replication-and-data-integrity"></a><span data-ttu-id="13e4d-104">Replikation und Datenintegrität</span><span class="sxs-lookup"><span data-stu-id="13e4d-104">Replication and Data Integrity</span></span>

<span data-ttu-id="13e4d-105">Active Directory Domain Services eine *Multimasteraktualisierung* bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="13e4d-105">Active Directory Domain Services provide *multi-master update*.</span></span> <span data-ttu-id="13e4d-106">Das Multi-Master-Update bedeutet, dass alle vollständigen Replikate einer bestimmten Partition beschreibbar sind (die partiellen Replikate auf globalen Katalog Servern sind nicht beschreibbar). Das Multi-Master-Update bedeutet, dass Updates nicht blockiert werden, auch wenn einige Replikate nicht funktionsfähig sind.</span><span class="sxs-lookup"><span data-stu-id="13e4d-106">Multi-master update means that all full replicas of a given partition are writable (the partial replicas on global catalog servers are not writable.) Multi-master update means that updates are not blocked even when some replicas are inoperable.</span></span> <span data-ttu-id="13e4d-107">Der Active Directory Server überträgt die Änderungen vom aktualisierten Replikat an alle anderen Replikate.</span><span class="sxs-lookup"><span data-stu-id="13e4d-107">The Active Directory server propagates the changes from the updated replica to all other replicas.</span></span> <span data-ttu-id="13e4d-108">Die Replikation erfolgt automatisch und transparent.</span><span class="sxs-lookup"><span data-stu-id="13e4d-108">Replication is automatic and transparent.</span></span>

<span data-ttu-id="13e4d-109">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="13e4d-109">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="13e4d-110">Das Replikations Modell in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="13e4d-110">The Replication Model in Active Directory Domain Services</span></span>](replication-model-in-active-directory-domain-services.md)
-   [<span data-ttu-id="13e4d-111">Replikations Verhalten in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="13e4d-111">Replication Behavior in Active Directory Domain Services</span></span>](replication-behavior-in-active-directory-domain-services.md)
-   [<span data-ttu-id="13e4d-112">Erkennen und vermeiden von Replikations Latenz</span><span class="sxs-lookup"><span data-stu-id="13e4d-112">Detecting and Avoiding Replication Latency</span></span>](detecting-and-avoiding-replication-latency.md)

 

 




