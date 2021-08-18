---
title: Verwenden Transport-Level Sicherheit auf dem Client
description: Der Client gibt an, wie der Server die Identität des Clients angibt, wenn der Client die Zeichenfolgenbindung eingibt.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- Rpc für Remoteprozeduraufrufe , Aufgaben mit Sicherheit auf Transportebene auf dem Client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ee610da50d34711c9ec40f93c29ed08d2bb97ba83c02bc4e8c297b08f859c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010598"
---
# <a name="using-transport-level-security-on-the-client"></a>Verwenden Transport-Level Sicherheit auf dem Client

Der Client gibt an, wie der Server die Identität des Clients angibt, wenn der Client die Zeichenfolgenbindung eingibt. Diese QOS-Informationen werden als Endpunktoption in der Zeichenfolgenbindung bereitgestellt. Der Client kann die Ebene des Identitätswechsels, die dynamische oder statische Nachverfolgung und das Flag effective-only angeben.

**So stellen Sie Quality-of-Service-Informationen für den Server zur Verfügung**

1.  Der Client ruft [**RpcStringBindingCompose auf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) um die Komponentenzeichenfolgen, einschließlich Endpunktoptionen, im richtigen Zeichenfolgenbindungskontext zu erstellen.
2.  Der Client ruft [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) auf, um ein neues Bindungshand handle zu erhalten und die Quality-of-Service-Informationen für den Client anzuwenden.
3.  Der Client ruft Remoteprozeduren mithilfe des -Handles auf.

Microsoft RPC unterstützt Windows Sicherheitsfeatures nur unter [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) und [**ncalrpc.**](/windows/desktop/Midl/ncalrpc) Sicherheitsoptionen für andere Transporte werden ignoriert.

Der Client kann der Bindung für den Named Pipe-Transport [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) oder [**ncalrpc die folgenden Sicherheitsparameter zuordnen:**](/windows/desktop/Midl/ncalrpc)

-   Identifikation, Identitätswechsel oder Anonym. Gibt den verwendeten Sicherheitstyp an. Der Standardwert ist Identitätswechsel.
-   Dynamisch oder Statisch. Bestimmt, ob einem Thread zugeordnete Sicherheitsinformationen eine Kopie der Sicherheitsinformationen sind, die zum Zeitpunkt des Remoteprozeduraufrufs erstellt wurden (statisch) oder ein Zeiger auf die Sicherheitsinformationen (dynamisch).

    Statische Sicherheitsinformationen ändern sich nicht. Die dynamische Einstellung spiegelt die aktuellen Sicherheitseinstellungen wider, einschließlich der Änderungen, die nach dem Remoteprozeduraufruf vorgenommen wurden. Für [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)ist der Standardwert für Named Pipe-Remoteverbindungen statisch, für lokale Named Pipe-Verbindungen ist der Standardwert dynamisch.

-   **TRUE** oder **FALSE**. Gibt den Wert des Flags effective-only an. Der Wert **TRUE gibt an,** dass nur Tokenberechtigungen, die zum Zeitpunkt des Aufrufs auf festgelegt sind, wirksam sind. Der Wert **FALSE gibt an,** dass alle Berechtigungen verfügbar sind und von der Anwendung geändert werden können.

Eine beliebige Kombination dieser Einstellungen kann der Bindung zugewiesen werden, wie im folgenden Beispiel gezeigt:

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

Die Standardeinstellungen für Sicherheitsparameter variieren je nach Transportprotokoll.

Weitere Informationen zur Syntax der Endpunktoptionen finden Sie unter [Endpunkt](/windows/desktop/Midl/endpoint).

 

 