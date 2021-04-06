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
# <a name="granting-logon-as-service-right-on-the-host-computer"></a>Gewähren von Berechtigung "Anmelden als Dienst" auf dem Host Computer

Bei der Installation eines Diensts für die unter Verwendung eines Domänen Benutzerkontos muss das Konto über die Berechtigung zum Anmelden als Dienst auf dem lokalen Computer verfügen. Beachten Sie, dass sich dieses Anmelde Recht nur auf den lokalen Computer bezieht und in der lokalen LSA-Richtlinie jedes Host Computers erteilt werden muss. Dieser Schritt ist nicht erforderlich, wenn der Dienst als "LocalSystem" ausgeführt wird, dem standardmäßig dieses Recht erteilt wird.

Weitere Informationen zum programmgesteuerten gewähren der Berechtigung "Anmelden als Dienst" finden Sie im [lsaprivs-Beispielcode](https://www.google.com/#q=LSAPrivs).

 

 




