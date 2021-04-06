---
title: Out-of-Band-Signalisierung
description: Bei der Zusammenarbeit von Anwendungen, die gemeinsame Daten mit dem Verzeichnis gemeinsam nutzen, kann die Out-of-Band-Signalisierung verwendet werden
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036351"
---
# <a name="out-of-band-signaling"></a><span data-ttu-id="e0c4b-103">Out-of-Band-Signalisierung</span><span class="sxs-lookup"><span data-stu-id="e0c4b-103">Out-of-Band Signaling</span></span>

<span data-ttu-id="e0c4b-104">Bei der Zusammenarbeit von Anwendungen, die gemeinsame Daten mit dem Verzeichnis gemeinsam nutzen, kann die Out-of-Band-Signalisierung verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e0c4b-104">Cooperating applications that share common data using the directory can use out-of-band signaling to avoid both version skew and partial updates.</span></span> <span data-ttu-id="e0c4b-105">Einfach ausgedrückt: die kooperierenden Anwendungen verwenden einen Mechanismus, der von der Verzeichnisreplikation getrennt ist, um einander über Änderungen in den gemeinsam genutzten allgemeinen Daten zu informieren.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-105">Put simply, the cooperating applications use a mechanism separate from directory replication to inform each other of changes in the shared common data.</span></span> <span data-ttu-id="e0c4b-106">Die Out-of-Band-Signalisierung ist am effektivsten, wenn Sie in Kombination mit einem Versionsmechanismus verwendet wird – dies ermöglicht dem Partner, die Änderungen zu erkennen, um Remote Partner zu benachrichtigen, auf welche Version der freigegebenen Daten gewartet werden</span><span class="sxs-lookup"><span data-stu-id="e0c4b-106">Out-of-band signaling is most effective when used in combination with a versioning mechanism—this allows the partner detecting the change to notify remote partners what version of the shared data to wait for.</span></span>

<span data-ttu-id="e0c4b-107">Wenn Sie zum RPC-Beispiel zurückkehren, das im Abschnitt "Versions Schiefe" des [Replikations Verhaltens in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md)angegeben ist, könnte der RPC-Server einen Rückruf an verbundene Clients durchführen, um Sie über den Umstieg auf einen neuen Server zu informieren: "Ich werde das verschieben.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-107">Returning to the RPC example given in the "Version Skew" section of [Replication Behavior in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), the RPC server could call back into connected clients to inform them of the move to a new server: "I am going to move.</span></span> <span data-ttu-id="e0c4b-108">Bitte stellen Sie sich vor, die Replikation bringt Ihnen die neue Adresse in Kürze, damit der Client den Übergangszeitraum verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-108">Please stand by, replication will bring you the new address shortly" so that the client can handle the transition period.</span></span>

<span data-ttu-id="e0c4b-109">Anwendungen, für die identische Richtlinien erforderlich sind, um miteinander zu kommunizieren, können Out-of-Band-Signalisierung verwenden, um sicherzustellen, dass eine neue Richtlinie erst verwendet wird, wenn Sie von allen beteiligten Parteien empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-109">Applications that require identical policies to be in force in order to communicate with each other can use out-of-band signaling to ensure that a new policy is not employed until all involved parties have received it.</span></span> <span data-ttu-id="e0c4b-110">Wenn beispielsweise die IPSec-Richtlinie (Internet Protocol Security, Internet Protokoll Sicherheit) zwischen zwei Computern geändert wird, kann ein Agent auf dem Quellcomputer einen Agent auf dem Zielcomputer kontaktieren, um die Anwendung der geänderten Richtlinie zu aushandeln, wobei der Quellcomputer die Anwendung verzögert, bis der Zielcomputer ebenfalls die neue Richtlinie empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-110">For example, if the Internet Protocol security (IPsec) policy between two machines is changed, an agent on the source machine could contact an agent on the destination machine to negotiate the application of the changed policy, with the source machine delaying application until the destination machine has received the new policy as well.</span></span>

 

 




