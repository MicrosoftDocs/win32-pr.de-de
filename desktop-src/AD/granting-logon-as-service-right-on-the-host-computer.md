---
title: Gewähren von Berechtigung "Anmelden als Dienst" auf dem Host Computer
description: Bei der Installation eines Diensts für die unter Verwendung eines Domänen Benutzerkontos muss das Konto über die Berechtigung zum Anmelden als Dienst auf dem lokalen Computer verfügen.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef2bb87c3cf461e67cb7da20f36d9ac07fb362
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707613"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a><span data-ttu-id="c6ef5-103">Gewähren von Berechtigung "Anmelden als Dienst" auf dem Host Computer</span><span class="sxs-lookup"><span data-stu-id="c6ef5-103">Granting Logon as Service Right on the Host Computer</span></span>

<span data-ttu-id="c6ef5-104">Bei der Installation eines Diensts für die unter Verwendung eines Domänen Benutzerkontos muss das Konto über die Berechtigung zum Anmelden als Dienst auf dem lokalen Computer verfügen.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-104">When installing a service to run under a domain user account, the account must have the right to logon as a service on the local computer.</span></span> <span data-ttu-id="c6ef5-105">Beachten Sie, dass sich dieses Anmelde Recht nur auf den lokalen Computer bezieht und in der lokalen LSA-Richtlinie jedes Host Computers erteilt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-105">Be aware that this logon right applies only to the local computer and must be granted in the local LSA policy of each host computer.</span></span> <span data-ttu-id="c6ef5-106">Dieser Schritt ist nicht erforderlich, wenn der Dienst als "LocalSystem" ausgeführt wird, dem standardmäßig dieses Recht erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-106">This step is not required if your service runs as LocalSystem, which, by default, is granted this right.</span></span>

<span data-ttu-id="c6ef5-107">Weitere Informationen zum programmgesteuerten gewähren der Berechtigung "Anmelden als Dienst" finden Sie im [lsaprivs-Beispielcode](https://www.google.com/#q=LSAPrivs).</span><span class="sxs-lookup"><span data-stu-id="c6ef5-107">For more information on how to programmatically grant logon as a service right, see the [LSAPrivs sample code](https://www.google.com/#q=LSAPrivs).</span></span>

 

 




