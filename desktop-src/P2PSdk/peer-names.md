---
description: Peernamen werden vom Peer Name Resolution Protocol (PNRP), vom Peer Identity Manager und von der Peer Gruppierungs Infrastruktur verwendet.
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: Peernamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18774939d5e0e9bad208999fbc6ca1e5f624300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351686"
---
# <a name="peer-names"></a>Peernamen

Peernamen werden vom Peer Name Resolution Protocol (PNRP), vom Peer Identity Manager und von der Peer Gruppierungs Infrastruktur verwendet. Peernamen sind stabile Namen für Ressourcen, z. b. Computer, Benutzer, Gruppen oder Dienste. PNRP verwendet Peernamen, um Knoten in einem Peer Netzwerk zu identifizieren.

> [!Note]  
> Ein Endpunkt, der von der Peer Infrastruktur verwendet wird, ist tatsächlich ein Tupel, das aus einer IPv4-oder IPv6-Adresse, einem Port und einem Protokoll (TCP oder UDP) besteht. Ein PeerName kann mehr als ein Tupel enthalten.

 

Ein PeerName ist eine Text Zeichenfolge, die das folgende Format aufweist:

-   "Authority. Classifier"

Der Wert einer Autorität hängt davon ab, ob der Name sicher oder unsicher ist. Der Klassifizierer eines Peer namens ist eine Zeichenfolge. Ein Klassifizierer kann ein beliebiger Name sein, der 150 oder weniger Unicode-Zeichen enthält. Bei Peernamen wird die Groß-/Kleinschreibung beachtet, und Sie können als sicher oder unsicher registriert werden In der folgenden Liste sind einige Beispiele für Peer Namen aufgeführt:

-   "0. myunsecuredpeer Name"
-   "0. JohnDoe. Games"
-   "6520c005f 63fc1864b7d8f 3cabebd4916ae7f-ID. JohnDoe

## <a name="secure-peer-names"></a>Sichere Peernamen

Bei einem sicheren Namen ist die Autorität der SHA-Hash (Secure Hash Algorithmus) des öffentlichen Schlüssels des Peer namens und führt zu einer hexadezimalen Zeichenfolge von 40 Zeichen. Ein sicherer PeerName kann nur vom Besitzer oder Delegaten des Peer Namen Besitzers in PNRP registriert werden. Ein gesicherter Peername muss erstellt werden, indem [**peercreatepeername**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)aufgerufen wird.

## <a name="unsecured-peer-names"></a>Unsichere Peernamen

Für einen ungesicherten Namen ist die Autorität NULL (0), und der Klassifizierer ist der einzige bedeutende Teil des Peer namens, der einen ungesicherten Peernamen ohne zugehörige [Identität](identity-manager-api.md)erstellt. Nicht gesicherte Peernamen werden in der PNRP-namens Registrierung und-Auflösung verwendet. Unsichere Peernamen bieten eine nützliche Möglichkeit zum Registrieren und Auflösen von Ressourcen, für die keine sichere Namensauflösung erforderlich ist. Allerdings kann jeder beliebige Knoten den nicht gesicherten Namen veröffentlichen. Anwendungen, die die Sicherheit betreffen, müssen sicherstellen, dass Sie robust und sicher sind, wenn Sie ungesicherte Peernamen nutzen.

> [!Note]  
> Jeder kann einen ungesicherten Peernamen bei PNRP registrieren.

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a>PNRP und die nächste Peer Namen Instanz

Es können mehrere Instanzen eines Peer namens vorhanden sein. Wenn [PNRP](pnrp-namespace-provider-api.md) zum Auflösen eines Peer namens verwendet wird, gibt es ein Konzept einer **nächsten** Peer Namen Instanz. Dies bedeutet, dass der Name einen Dienst Speicherort aufweist, der dem in [**pnrpinfo \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) oder [**pnrpinfo \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))am nächsten liegenden **sahint** -Member entspricht. , Wenn kein Hinweis angegeben wird, der am nächsten bei einer der lokalen IP-Adressen liegt.

 

 
