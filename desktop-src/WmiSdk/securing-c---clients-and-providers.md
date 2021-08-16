---
description: Sowohl C++-Anbieter als auch Clientanwendungen müssen viele der gleichen Vorgänge ausführen, um die WMI-Sicherheit zu gewährleisten.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Sichern von C++-Clients und -Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4151440f9e85f7cd9e6590842ffd3d103242410b38f52287dba83ba3bb3faec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316159"
---
# <a name="securing-c-clients-and-providers"></a>Sichern von C++-Clients und -Anbietern

Sowohl C++-Anbieter als auch Clientanwendungen müssen viele der gleichen Vorgänge ausführen, um die WMI-Sicherheit zu gewährleisten.

Clientanwendungen müssen beim Herstellen einer [](setting-authentication-in-wmi.md) Verbindung [mit](setting-the-default-process-security-level-using-c-.md) WMI den DCOM-Identitätswechsel und die Authentifizierungsebenen ordnungsgemäß festlegen. Rückrufe von [asynchronen Aufrufen](setting-security-on-an-asynchronous-call.md) haben Sicherheitsrisiken, sodass Clientanwendungen Zugriffsüberprüfungen durchführen müssen, um sicherzustellen, dass der Rückruf von einer vertrauenswürdigen Quelle stammt. [](performing-access-checks.md) Clients müssen sowohl temporäre als [auch permanente Ereignisverbraucher schützen.](securing-wmi-events.md)

Ein Anbieter kann [Zugriffsüberprüfungen durchführen,](performing-access-checks.md) um sicherzustellen, dass auf die erstellten Ressourcen nur von den entsprechenden Clients zugegriffen wird.

Sowohl Anbieter als auch Clients können die Sicherheit für eine bestimmte [Proxyverbindung](setting-the-security-on-iwbemservices-and-other-proxies.md) festlegen. Beide können auch Berechtigungen [aktivieren.](executing-privileged-operations.md) Ein Ereignisanbieter muss sicherstellen, dass der Clientverbraucher über Berechtigungen zum Empfangen [eines angeforderten Ereignisses verfügt.](providing-events-securely.md)

Ein Client oder Anbieter muss möglicherweise eine Remoteverbindung herstellen, die einen anderen Authentifizierungsdienst erfordert, z. B. NTLM anstelle von Kerberos.

 

 



