---
title: Features des Replikations Modells für Active Directory Domain Services
description: Das in Active Directory Domain Services verwendete Replikations Modell wird als multimasterlose Konsistenz mit Konvergenz bezeichnet.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, Replikations Modell
- Features des Replikations Modells Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923c49dd648063ebd6afd086be3729f28f1e4080
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341632"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a><span data-ttu-id="191d5-105">Features des Replikations Modells für Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="191d5-105">Features of the Replication Model for Active Directory Domain Services</span></span>

<span data-ttu-id="191d5-106">Das in Active Directory Domain Services verwendete Replikations Modell wird als *multimasterlose Konsistenz mit Konvergenz* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="191d5-106">The replication model used in Active Directory Domain Services is called *multi-master loose consistency with convergence*.</span></span> <span data-ttu-id="191d5-107">In diesem Modell kann das Verzeichnis über viele Replikate verfügen. ein Replikationssystem überträgt Änderungen an einem beliebigen Replikat an alle anderen Replikate.</span><span class="sxs-lookup"><span data-stu-id="191d5-107">In this model, the directory can have many replicas; a replication system propagates changes made at any given replica to all other replicas.</span></span> <span data-ttu-id="191d5-108">Es ist nicht garantiert, dass die Replikate zu einem bestimmten Zeitpunkt konsistent sind ("lose Konsistenz"), da Änderungen jederzeit auf ein beliebiges Replikat angewendet werden können ("Multimaster").</span><span class="sxs-lookup"><span data-stu-id="191d5-108">The replicas are not guaranteed to be consistent with each other at any particular time ("loose consistency"), because changes can be applied to any replica at any time ("multi-master").</span></span> <span data-ttu-id="191d5-109">Wenn das System in der Lage ist, einen stabilen Zustand zu erreichen, in dem keine neuen Updates stattfinden und alle vorherigen Updates vollständig repliziert wurden, werden alle Replikate sicher mit dem gleichen Satz von Werten ("Konvergenz") zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="191d5-109">If the system is allowed to reach a steady state, in which no new updates are occurring and all previous updates have been completely replicated, all replicas are guaranteed to converge on the same set of values ("convergence").</span></span>

 

 




