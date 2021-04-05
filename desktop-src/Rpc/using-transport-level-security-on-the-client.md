---
title: Verwenden von Transport-Level Sicherheit auf dem Client
description: Der Client gibt an, wie der Server die Identität des Clients annimmt, wenn der Client die Zeichen folgen Bindung herstellt.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- Remote Prozedur Aufruf RPC, Tasks, mit Sicherheit auf Transport Ebene auf dem Client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949037"
---
# <a name="using-transport-level-security-on-the-client"></a>Verwenden von Transport-Level Sicherheit auf dem Client

Der Client gibt an, wie der Server die Identität des Clients annimmt, wenn der Client die Zeichen folgen Bindung herstellt. Diese QoS-Informationen werden als Endpunkt Option in der Zeichen folgen Bindung bereitgestellt. Der Client kann die Ebene des Identitäts Wechsels, die dynamische oder statische Nachverfolgung und das Flag für die effektive Festlegung angeben.

**So stellen Sie Quality of Service-Informationen für den Server bereit**

1.  Der Client ruft [**rpcstringbindingcompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) auf, um die Komponenten Zeichenfolgen (einschließlich Endpunkt Optionen) im richtigen Zeichen folgen Bindungs Kontext zu erstellen.
2.  Der Client ruft [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) auf, um ein neues Bindungs Handle zu erhalten und die Quality of Service-Informationen für den Client anzuwenden.
3.  Der Client führt Remote Prozedur Aufrufe mit dem Handle aus.

Microsoft RPC unterstützt Windows-Sicherheitsfeatures nur auf [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) und [**Ncalrpc**](/windows/desktop/Midl/ncalrpc). Sicherheitsoptionen für andere Transporte werden ignoriert.

Der Client kann die folgenden Sicherheitsparameter der Bindung für den Named Pipe-Transport [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) oder [**Ncalrpc**](/windows/desktop/Midl/ncalrpc)zuordnen:

-   Identifizierung, Identitätswechsel oder anonym. Gibt den verwendeten Sicherheitstyp an. Der Standardwert ist der Identitätswechsel.
-   Dynamisch oder statisch. Bestimmt, ob einem Thread zugeordnete Sicherheitsinformationen eine Kopie der Sicherheitsinformationen sind, die zu dem Zeitpunkt erstellt werden, zu dem der Remote Prozedur Aufruf erfolgt (statisch), oder ein Zeiger auf die Sicherheitsinformationen (dynamisch).

    Statische Sicherheitsinformationen werden nicht geändert. Die dynamische Einstellung gibt die aktuellen Sicherheitseinstellungen an, einschließlich der Änderungen, die nach dem Ausführen des Remote Prozedur Aufrufes vorgenommen wurden. Bei [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)ist die Standardeinstellung für Remote Named Pipe Verbindungen statisch, für lokale Named Pipe Verbindungen der Standardwert Dynamic.

-   **True** oder **false**. Gibt den Wert des Flag für die effektive Gültigkeit an. Der Wert **true** gibt an, dass nur tokenprivilegien, die zum Zeitpunkt des Aufrufes auf ON festgelegt sind, wirksam sind. Der Wert **false** gibt an, dass alle Berechtigungen verfügbar sind und dass Sie von der Anwendung geändert werden können.

Eine beliebige Kombination dieser Einstellungen kann der Bindung zugewiesen werden, wie im folgenden Beispiel gezeigt:

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

Standardeinstellungen für Sicherheitsparameter variieren je nach Transportprotokoll.

Weitere Informationen zur Syntax der Endpunkt Optionen finden Sie unter [EndPoint](/windows/desktop/Midl/endpoint).

 

 