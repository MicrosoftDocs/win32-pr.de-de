---
title: Gewähren der Anmeldung als Dienstrecht auf dem Hostcomputer
description: Wenn Sie einen Dienst installieren, der unter einem Domänenbenutzerkonto ausgeführt werden soll, muss das Konto über das Recht verfügen, sich als Dienst auf dem lokalen Computer zu anmelden.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef53e68feb9312bb8efdca285716aa5b6ea077e2e85f6c5538eb13532b51a8ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188954"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a>Gewähren der Anmeldung als Dienstrecht auf dem Hostcomputer

Wenn Sie einen Dienst installieren, der unter einem Domänenbenutzerkonto ausgeführt werden soll, muss das Konto über das Recht verfügen, sich als Dienst auf dem lokalen Computer zu anmelden. Beachten Sie, dass dieses Anmelderecht nur für den lokalen Computer gilt und in der lokalen LSA-Richtlinie jedes Hostcomputers gewährt werden muss. Dieser Schritt ist nicht erforderlich, wenn Ihr Dienst als LocalSystem ausgeführt wird, dem standardmäßig dieses Recht gewährt wird.

Weitere Informationen zum programmgesteuerten Gewähren von Anmelde-as-a-Service-Rechten finden Sie im [LSAPrivs-Beispielcode](https://www.google.com/#q=LSAPrivs).

 

 




