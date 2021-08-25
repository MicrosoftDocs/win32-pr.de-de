---
description: Wie alle Prozesse verfügt ein geschützter Server über ein primäres Zugriffstoken, das seinen Sicherheitskontext beschreibt.
ms.assetid: 4e6393b2-4a71-49e4-b1e7-f34bf317d60d
title: Der Clientsicherheitskontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af57c11c7b0452003498b88b0be24c880e2875fec459fb80e3cd87ef01bdd493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907120"
---
# <a name="the-client-security-context"></a>Der Clientsicherheitskontext

Wie alle [*Prozesse verfügt*](/windows/desktop/SecGloss/p-gly)ein geschützter Server über ein [*primäres Zugriffstoken,*](/windows/desktop/SecGloss/p-gly) das seinen [*Sicherheitskontext beschreibt.*](/windows/desktop/SecGloss/s-gly) Wenn ein Client eine Verbindung mit einem geschützten Server herstellt, möchte der Server möglicherweise Aktionen mithilfe des Sicherheitskontexts des Clients anstelle des Sicherheitskontexts des Servers ausführen. Wenn beispielsweise ein Client in einer DDE-Konversation (Dynamic Data Exchange) Informationen von einem DDE-Server an fordert, muss der Server überprüfen, ob der Client Zugriff auf die Informationen hat.

Es gibt zwei Möglichkeiten, wie ein Server im Sicherheitskontext des Clients agieren kann:

-   Ein Thread des Serverprozesses kann die Identität des Clients imitieren. In diesem Fall verfügt der Thread des [](/windows/desktop/SecGloss/a-gly) Servers über ein Identitätswechsel-Zugriffstoken, das den Client, die Gruppen des Clients und die Berechtigungen des [*Clients identifiziert.*](/windows/desktop/SecGloss/p-gly) Weitere Informationen finden Sie unter [Clientpersonation](client-impersonation.md).
-   Der Server kann die Anmeldeinformationen des Clients [*erhalten und*](/windows/desktop/SecGloss/c-gly) den Client beim Computer des Servers anmelden. Dadurch wird eine neue Anmeldesitzung [*erstellt*](/windows/desktop/SecGloss/s-gly) und ein primäres Zugriffstoken für den Client erzeugt. Der Server kann dann das Zugriffstoken des Clients verwenden, um die Identität des Clients zu angenommen oder einen neuen Prozess zu starten, der im Sicherheitskontext des Clients ausgeführt wird. Weitere Informationen finden Sie unter [Clientanmeldungssitzungen](client-logon-sessions.md).

In den meisten Fällen reicht der Identitätswechsel des Clients aus. Der Identitätswechsel ermöglicht es dem Server, den Zugriff des Clients auf sicherungsfähige Objekte zu überprüfen, die Berechtigungen des Clients zu überprüfen und Überwachungspfadeinträge zu generieren, die den Client identifizieren. In der Regel muss ein Server eine Clientanmeldungssitzung nur starten, wenn er den Sicherheitskontext des Clients für den Zugriff auf Netzwerkressourcen verwenden muss.

 

 
