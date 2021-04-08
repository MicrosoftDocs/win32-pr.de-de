---
title: Empfehlungen für RPC-over-HTTP
description: In diesem Abschnitt werden bewährte Methoden und empfohlene Bereitstellungs Konfigurationen zum Erreichen von maximaler Sicherheit und Leistung bei Verwendung von RPC über HTTP dokumentiert.
ms.assetid: 83938a7d-77d0-45e8-b0a3-7b32ef768d83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8871686d1fc8b87bcd6fb7ac4314b1977252f23a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037419"
---
# <a name="rpc-over-http-deployment-recommendations"></a>Empfehlungen für RPC-over-HTTP

In diesem Abschnitt werden bewährte Methoden und empfohlene Bereitstellungs Konfigurationen zum Erreichen von maximaler Sicherheit und Leistung bei Verwendung von RPC über HTTP dokumentiert. Die verschiedenen darin gefundenen Konfigurationen gelten für verschiedene Unternehmen, die auf verschiedenen Größen, Budgets und Sicherheitsanforderungen basieren. Jede Konfiguration bietet auch Überlegungen zur Bereitstellung, die für ein bestimmtes Szenario am besten geeignet sind.

Informationen zu großen RPC-über-HTTP-Szenarios finden Sie unter [Microsoft RPC-Lastenausgleich](rpc-load-balancing.md).

Für alle Konfigurationen gelten die folgenden Empfehlungen:

-   Verwenden Sie Versionen von Windows, die RPC über HTTP v2 unterstützen.
-   Legen Sie IIS auf dem Computer ab, auf dem der RPC-Proxy im IIS 6,0-Modus ausgeführt wird.
-   Anonymen Zugriff auf das virtuelle Verzeichnis des RPC-Proxys nicht zulassen.
-   Aktivieren Sie niemals den zugewiesenen Registrierungsschlüssel.
-   Verwenden Sie zum Überprüfen, ob der RPC-Proxy, mit dem Sie eine Verbindung hergestellt haben, das **certifiaseesubjectfield** (siehe [**rpcbindingsetauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) ).
-   Konfigurieren Sie den **ValidPorts** -Registrierungsschlüssel so, dass er nur Computer enthält, mit denen die RPC über HTTP-Clients eine Verbindung herstellen.
-   Verwenden Sie keine Platzhalter im **ValidPorts** -Schlüssel. Dies kann Zeit sparen, aber ein vollständig unerwarteter Computer kann auch für den Platzhalter geeignet sein.
-   Verwenden Sie SSL auf RPC-über-HTTP-Clients. Wenn die Richtlinien befolgt werden, die in diesen Abschnitten aufgeführt sind, kann der RPC-über-HTTP-Client keine Verbindung herstellen, ohne SSL zu verwenden.
-   Konfigurieren von RPC-über-HTTP-Clients für die Verwendung der RPC-Verschlüsselung zusätzlich zur Verwendung von SSL. Wenn der RPC-über-HTTP-Client den KDC nicht erreichen kann, kann er nur aushandeln und NTLM verwenden.
-   Konfigurieren Sie Client Computer für die Verwendung von NTLMv2. Legen Sie für den Registrierungsschlüssel **LMCompatibilityLevel den Wert** 2 oder höher fest. Weitere Informationen zum Schlüssel **LMCompatibilityLevel** finden Sie unter **MSDN.Microsoft.com** .
-   Führen Sie eine Webfarm von RPC-Proxy Computern mit der oben beschriebenen Konfiguration aus.
-   Stellen Sie eine Firewall zwischen dem Internet und dem RPC-Proxy bereit.
-   Um eine optimale Leistung zu erzielen, konfigurieren Sie IIS so, dass eine kurze Antwort auf nicht erfolgreiche Fehlercodes gesendet wird. Da der Consumer der IIS-Antwort ein automatisierter Prozess ist, ist es nicht erforderlich, dass benutzerfreundliche Erläuterungen an den Client gesendet werden. Sie werden einfach vom RPC-über-HTTP-Client ignoriert.

Die grundlegenden Ziele des RPC-Proxys aus Sicht der Sicherheit, Leistung und Verwaltbarkeit lauten wie folgt:

-   Geben Sie einen einzelnen Einstiegspunkt für den RPC-über-HTTP-Datenverkehr in das Servernetzwerk an. Die Verwendung eines einzelnen Einstiegs Punkts für den RPC-über-HTTP-Datenverkehr in ein Servernetzwerk hat zwei wesentliche Vorteile. Da der RPC-Proxy mit dem Internet erreichbar ist, isolieren die meisten Organisationen solche Computer in einem speziellen Netzwerk, das als nicht vertrauenswürdiges Umkreis Netzwerk bezeichnet wird, das vom normalen Organisations Netzwerk getrennt ist. Server in einem nicht vertrauenswürdigen Umkreis Netzwerk werden sorgfältig verwaltet, konfiguriert und überwacht, um Angriffe aus dem Internet zu unterhalten. Je weniger Computer in einem nicht vertrauenswürdigen Umkreis Netzwerk, desto einfacher ist es, Sie zu konfigurieren, zu verwalten, zu überwachen und sicher zu halten. Da eine einzelne Webfarm mit installiertem RPC-Proxy eine beliebige Anzahl von RPC-über-HTTP-Servern im Unternehmensnetzwerk bedienen kann, ist es sehr sinnvoll, den RPC-Proxy vom RPC-über-HTTP-Server zu trennen und den RPC-Proxy in einem nicht vertrauenswürdigen Umkreis Netzwerk zu befinden. Wenn sich der RPC-Proxy auf dem gleichen Computer wie der RPC-über-HTTP-Server befunden hat, müssten Organisationen alle Back-End-Server in einem nicht vertrauenswürdigen Umkreis Netzwerk ablegen, wodurch es viel schwieriger wird, das nicht vertrauenswürdige Umkreis Netzwerk sicher zu halten. Durch die Trennung der Rolle des RPC-Proxys und des RPC-über-HTTP-Servers können Organisationen die Anzahl der Computer in einem nicht vertrauenswürdigen Umkreis Netzwerk verwalten und somit sicherer gestalten.
-   Dient als Sicherheits fuse für das Servernetzwerk. Der RPC-Proxy ist als expenable fuse für das Servernetzwerk konzipiert – wenn auf dem RPC-Proxy etwas schief geht, wird es einfach durchlaufen und somit den echten RPC-über-HTTP-Server schützen. Wenn die in diesem Abschnitt beschriebenen bewährten Methoden bisher befolgt wurden, wird der RPC-über-HTTP-Datenverkehr zusätzlich zu SSL mit der RPC-Verschlüsselung verschlüsselt. Die RPC-Verschlüsselung selbst erfolgt zwischen Client und Server, nicht zwischen dem Client und dem Proxy. Dies bedeutet, dass der Proxy den empfangenen RPC-Datenverkehr nicht versteht und nicht entschlüsseln kann. Sie versteht nur einige der vom Client gesendeten Steuerungs Sequenzen, die sich mit der Verbindungs Einrichtung, der Fluss Steuerung und anderen tunnelingdetails befassen. Er hat keinen Zugriff auf die Daten, die der RPC-über-HTTP-Client an den Server sendet. Darüber hinaus muss sich der RPC-über-HTTP-Client für den RPC-Proxy und den RPC-über-HTTP-Server einzeln authentifizieren. Dies ermöglicht eine gründliche Abwehr. Wenn der RPC-Proxy Computer aufgrund eines Konfigurations Fehlers oder eines Sicherheits Verstoßes in irgendeiner Art kompromittiert wird, sind die Daten, die Sie durchlaufen, immer noch sicher vor Manipulationen. Ein Angreifer, der die Kontrolle über den RPC-Proxy hätte, kann den Datenverkehr höchstens unterbrechen, ihn aber nicht lesen oder manipulieren. An dieser Stelle kommt die fuse-Rolle des RPC-Proxys ins Spiel – Sie kann nicht ausgeführt werden, ohne dass die Sicherheit des RPC-über-HTTP-Datenverkehrs gefährdet ist.
-   Verteilen einiger Zugriffs Überprüfungen und Entschlüsselungs Vorgänge auf mehreren Computern, auf denen der RPC-Proxy in einer Webfarm ausgeführt wird. Durch die ordnungsgemäße Funktionsweise in einer Webfarm können Organisationen mithilfe des RPC-Proxys die SSL-Entschlüsselung und einige der Zugriffs Überprüfungen auslagern, wodurch mehr Kapazität auf dem Back-End-Server für die Verarbeitung freigegeben wird. Die Verwendung einer Webfarm von RPC-Proxy Computern ermöglicht es einer Organisation, die Fähigkeit zu verbessern, DOS-Angriffe (Denial of Service) zu übernehmen, indem die Kapazität der Front-End-Server erhöht wird.

In den bisher aufgeführten Richtlinien haben Organisationen immer noch die Wahl. Jede Organisation hat Auswahlmöglichkeiten und Kompromisse zwischen Benutzer Unannehmlichkeiten, Sicherheit und Kosten:

-   **Verwenden Sie die Standard Authentifizierung oder die integrierte Windows-Authentifizierung, um sich beim RPC-Proxy zu authentifizieren?** RPC-über-HTTP unterstützt derzeit nur NTLM – Sie unterstützt Kerberos nicht. Außerdem kann die NTLM-Authentifizierung nicht ausgeführt werden, wenn ein HTTP-Proxy oder eine Firewall zwischen dem RPC-über-HTTP-Client und dem RPC-Proxy vorhanden ist, der das *via* -Pragma in den HTTP-Header einfügt. Wenn dies nicht der Fall ist, können Organisationen zwischen der Basic-und der NTLM-Authentifizierung wählen. Der Vorteil der Standard Authentifizierung ist, dass Sie schneller und einfacher ist und daher weniger Möglichkeiten für Denial-of-Service-Angriffe bietet. NTLM ist jedoch sicherer. Abhängig von den Prioritäten eines Unternehmens kann es "Basic", "NTLM" oder den Benutzern erlauben, zwischen beiden auszuwählen. Wenn nur eine ausgewählt wird, empfiehlt es sich, die andere vom virtuellen Verzeichnis des RPC-Proxys zu deaktivieren, um das Risiko von Angriffen zu verringern.
-   **Verwenden Sie denselben Satz von Anmelde Informationen für den RPC-Proxy und den RPC-über-HTTP-Server, oder verwenden Sie jeweils andere Anmelde Informationen?** Der Nachteil bei dieser Entscheidung liegt zwischen der benutzerfreundliche und der Sicherheit. Nur wenige Benutzer möchten mehrere Anmelde Informationen eingeben. Wenn jedoch ein Sicherheits Verstoß in einem nicht vertrauenswürdigen Umkreis Netzwerk auftritt, bietet die Verwendung separater Sätze von Anmelde Informationen für den RPC-Proxy und den RPC-über-HTTP-Server zusätzlichen Schutz. Beachten Sie Folgendes: Wenn separate Anmelde Informationen verwendet werden und eine Gruppe von Anmelde Informationen die Anmelde Informationen für die Domäne des Benutzers ist, empfiehlt es sich, die Domänen Anmelde Informationen des Benutzers für den RPC-über-HTTP-Server und nicht für den RPC-Proxy zu verwenden.

 

 




