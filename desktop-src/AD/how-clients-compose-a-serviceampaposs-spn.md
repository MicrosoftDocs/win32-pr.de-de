---
title: Erstellen eines Dienst-SPN durch Clients
description: Zum Authentifizieren eines Diensts erstellt eine Clientanwendung einen SPN für die Dienstinstanz, mit der eine Verbindung hergestellt werden muss.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Erstellen des SPN-AD eines Diensts durch Clients
- Dienstprinzipalname AD , wie Clients den SPN eines Diensts erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06c3531ac329af1a4c4fa7721b5d575ce762d86f15767278ad9a348e7956cfa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188185"
---
# <a name="how-clients-compose-a-services-spn"></a>Erstellen eines Dienst-SPN durch Clients

Zum Authentifizieren eines Diensts erstellt eine Clientanwendung einen SPN für die Dienstinstanz, mit der eine Verbindung hergestellt werden muss. Die Clientanwendung kann die [**DsMakeSpn-Funktion**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) verwenden, um einen SPN zu erstellen. Der Client gibt die Komponenten des SPN mithilfe bekannter Daten oder Daten an, die aus anderen Quellen als dem Dienst selbst abgerufen wurden.

Die Form eines SPN ist wie im folgenden Format dargestellt:


```C++
<service class>/<host>:<port>/<service name>
```



In dieser Form sind " &lt; Dienstklasse &gt; " und " Host " &lt; &gt; erforderlich. " &lt; port " und " &gt; &lt; dienstname " &gt; optional.

In der Regel erkennt der Client den &lt; Teil "Dienstklasse" &gt; des Namens und erkennt, welche der optionalen Komponenten in den SPN aufgenommen werden sollen. Der Client kann Komponenten des SPN aus Quellen wie einem Dienstverbindungspunkt (Service Connection Point, SCP) oder benutzereingaben abrufen. Beispielsweise kann der Client das **serviceDNSName-Attribut** des SCP eines Diensts lesen, um die &lt; Komponente &gt; "host" abzurufen. Das **attribut serviceDNSName** enthält entweder den DNS-Namen des Servers, auf dem die Dienstinstanz ausgeführt wird, oder den DNS-Namen von SRV-Einträgen, die die Hostdaten für Dienstreplikate enthalten. Die &lt; Komponente "Dienstname", die &gt; nur für replizierbare Dienste verwendet wird, kann der Distinguished Name des Dienst-SCP, der DNS-Name der vom Dienst bedienten Domäne oder der DNS-Name von SRV- oder MX-Einträgen sein.

Weitere Informationen und ein Codebeispiel zum Erstellen eines SPN für einen Dienst finden Sie unter [Authentifizieren eines SCP-basierten Windows Sockets Service](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)durch einen Client.

Weitere Informationen und eine Beschreibung der SPN-Komponenten finden Sie unter [Namensformate für eindeutige SPNs.](name-formats-for-unique-spns.md)

 

 




