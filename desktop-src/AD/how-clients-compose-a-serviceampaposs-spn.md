---
title: Funktionsweise eines Dienst-SPN durch Clients
description: Um einen Dienst zu authentifizieren, stellt eine Client Anwendung einen SPN für die Dienst Instanz dar, mit der eine Verbindung hergestellt werden muss.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Zusammenstellen eines Dienst-SPN-AD durch Clients
- Dienst Prinzipal Name AD, wie Clients den SPN eines Dienstanbieter verfassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd8aa599b6d8238017897c9383bab188ce144e0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947385"
---
# <a name="how-clients-compose-a-services-spn"></a>Funktionsweise eines Dienst-SPN durch Clients

Um einen Dienst zu authentifizieren, stellt eine Client Anwendung einen SPN für die Dienst Instanz dar, mit der eine Verbindung hergestellt werden muss. Die Client Anwendung kann die [**dsmakespn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) -Funktion verwenden, um einen SPN zu erstellen. Der Client gibt die Komponenten des SPN mit bekannten Daten oder Daten an, die aus anderen Quellen als dem Dienst selbst abgerufen wurden.

Die Form eines SPN ist wie in der folgenden Form dargestellt:


```C++
<service class>/<host>:<port>/<service name>
```



In dieser Form sind " &lt; Service Class &gt; " und " &lt; Host &gt; " erforderlich. " &lt; Port &gt; " und " &lt; Dienst Name &gt; " sind optional.

In der Regel erkennt der Client den &lt; &gt; Teil des Namens "Service Class" und erkennt, welche der optionalen Komponenten in den SPN eingeschlossen werden sollen. Der Client kann die Komponenten des SPN von Quellen abrufen, z. b. einem Dienst Verbindungspunkt (Service Connection Point, SCP) oder Benutzereingaben. Beispielsweise kann der Client das **servicednsname** -Attribut des Dienst Verbindungs Punkts eines Diensts lesen, um die " &lt; Host"-Komponente zu erhalten &gt; . Das **servicednsname** -Attribut enthält entweder den DNS-Namen des Servers, auf dem die Dienst Instanz ausgeführt wird, oder den DNS-Namen von SRV-Datensätzen, die die Hostdaten für Dienst Replikate enthalten. Die " &lt; Service Name &gt; "-Komponente, die nur für replizierungsdienste verwendet wird, kann der Distinguished Name des Dienst Verbindungs Diensts, der DNS-Name der Domäne, die vom Dienst bereitgestellt wird, oder der DNS-Name der SRV-oder MX-Einträge sein.

Weitere Informationen und ein Codebeispiel zum Erstellen eines SPN für einen Dienst finden Sie unter [How a Client authenticates a SCP-based Windows Sockets Service](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).

Weitere Informationen und eine Beschreibung der SPN-Komponenten finden Sie unter [namens Formate für eindeutige SPNs](name-formats-for-unique-spns.md).

 

 




