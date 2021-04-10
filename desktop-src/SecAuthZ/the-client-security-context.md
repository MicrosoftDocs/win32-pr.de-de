---
description: Wie alle Prozesse verfügt ein geschützter Server über ein primäres Zugriffs Token, das seinen Sicherheitskontext beschreibt.
ms.assetid: 4e6393b2-4a71-49e4-b1e7-f34bf317d60d
title: Der Client Sicherheitskontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d3b4522aa90ade89e2130742346956a396f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959063"
---
# <a name="the-client-security-context"></a>Der Client Sicherheitskontext

Wie alle [*Prozesse*](/windows/desktop/SecGloss/p-gly)verfügt ein geschützter Server über ein [*Primäres Zugriffs Token*](/windows/desktop/SecGloss/p-gly) , das seinen [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly)beschreibt. Wenn ein Client eine Verbindung mit einem geschützten Server herstellt, möchte der Server möglicherweise Aktionen mithilfe des Sicherheits Kontexts des Clients anstelle des Sicherheits Kontexts des Servers ausführen. Wenn z. b. ein Client in einer DDE-Konversation (Dynamic Data Exchange) Informationen von einem DDE-Server anfordert, muss der Server überprüfen, ob der Client Zugriff auf die Informationen hat.

Es gibt zwei Möglichkeiten, wie ein Server im Sicherheitskontext des Clients agieren kann:

-   Ein Thread des Server Prozesses kann die Identität des Clients annehmen. In diesem Fall verfügt der Thread des Servers über ein Identitätswechsel- [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) , das den Client, die Gruppen des Clients und die [*Berechtigungen*](/windows/desktop/SecGloss/p-gly)des Clients identifiziert. Weitere Informationen finden Sie unter [Client](client-impersonation.md)Identitätswechsel.
-   Der Server kann die [*Anmelde*](/windows/desktop/SecGloss/c-gly) Informationen des Clients erhalten und den Client auf dem Computer des Servers anmelden. Dadurch wird eine neue Anmelde [*Sitzung*](/windows/desktop/SecGloss/s-gly) erstellt, und es wird ein primäres Zugriffs Token für den Client erzeugt. Der Server kann dann das Zugriffs Token des Clients verwenden, um die Identität des Clients anzunehmen oder einen neuen Prozess zu starten, der im Sicherheitskontext des Clients ausgeführt wird. Weitere Informationen finden Sie unter [Client Anmelde Sitzungen](client-logon-sessions.md).

In den meisten Fällen ist es ausreichend, die Identität des Clients anzunehmen. Der Identitätswechsel ermöglicht es dem Server, den Client Zugriff auf Sicherungs fähige Objekte zu überprüfen, die Berechtigungen des Clients zu überprüfen und Überwachungs Pfad Einträge zu generieren, die den Client identifizieren. In der Regel muss ein Server nur dann eine Client Anmelde Sitzung starten, wenn er den Sicherheitskontext des Clients für den Zugriff auf Netzwerkressourcen verwenden muss.

 

 
