---
title: Inter-Object Kommunikation
description: COM ist so konzipiert, dass Clients transparent mit Objekten kommunizieren können, unabhängig davon, wo diese Objekte im gleichen Prozess, auf demselben Computer oder auf einem anderen Computer ausgeführt werden.
ms.assetid: dd4adafb-a7e4-44ba-ae4a-80585875ecb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49d3d584ba6aa25a721276559a65ca2f9f9deded76616b93ff9953affce3553
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070830"
---
# <a name="inter-object-communication"></a>Inter-Object Kommunikation

COM ist so konzipiert, dass Clients transparent mit Objekten kommunizieren können, unabhängig davon, wo diese Objekte im selben Prozess, auf demselben Computer oder auf einem anderen Computer ausgeführt werden. Dies stellt ein einzelnes Programmiermodell für alle Objekttypen sowie sowohl für Objektclients als auch für Objektserver zur Verfügung.

Aus Clientsicht wird auf alle Objekte über Schnittstellenze0er zugegriffen. Ein Zeiger muss in Bearbeitung sein. Tatsächlich erreicht jeder Aufruf einer Schnittstellenfunktion immer zuerst einen Teil des In-Process-Codes. Wenn das Objekt in Bearbeitung ist, erreicht der Aufruf es direkt, ohne dass sich der Systeminfrastrukturcode interveniert. Wenn das Objekt out-of-process ist, erreicht der Aufruf zuerst ein sogenanntes "Proxy"-Objekt, das entweder von COM oder vom -Objekt bereitgestellt wird (wenn der Implementator dies möchte). Die Proxypakete rufen Parameter (einschließlich beliebiger Schnittstellenzeder) auf und generieren den entsprechenden Remoteprozeduraufruf (oder einen anderen Kommunikationsmechanismus bei benutzerdefinierten generierten Proxys) an den anderen Prozess oder den anderen Computer, auf dem sich die Objektimplementierung befindet. Dieser Prozess der Paketierung von Zeigern für die Übertragung über Prozessgrenzen hinweg wird als *Marshalling bezeichnet.*

Aus Sicht eines Servers werden alle Aufrufe der Schnittstellenfunktionen eines Objekts über einen Zeiger auf diese Schnittstelle ausgeführt. Auch hier verfügt ein Zeiger nur über Kontext in einem einzelnen Prozess, und der Aufrufer muss immer ein Teil des In-Process-Codes sein. Wenn das Objekt in Bearbeitung ist, ist der Aufrufer der Client selbst. Andernfalls ist der Aufrufer ein "Stub"-Objekt, das entweder von COM oder vom Objekt selbst bereitgestellt wird. Der Stub empfängt den Remoteprozeduraufruf (oder einen anderen Kommunikationsmechanismus bei benutzerdefinierten generierten Proxys) vom "Proxy" im Clientprozess, entmarshalt die Parameter und ruft die entsprechende Schnittstelle für das Serverobjekt auf. Aus Sicht von Clients und Servern kommunizieren sie immer direkt mit einem anderen Prozesscode.

COM bietet eine Implementierung des Marshallings, das als *Standard-Marshalling bezeichnet wird.* Diese Implementierung funktioniert für die meisten Objekte sehr gut und reduziert die Programmieranforderungen deutlich, wodurch der Marshallingprozess effektiv transparent wird.

Die klare Trennung der Schnittstelle von der Implementierung der Prozesstransparenz von COM kann jedoch in einigen Situationen im Weg sein. Der Entwurf einer Schnittstelle, die sich aus Clientsicht auf ihre Funktion konzentriert, kann manchmal zu Entwurfsentscheidungen führen, die mit der effizienten Implementierung dieser Schnittstelle über ein Netzwerk in Konflikt stehen. In solchen Fällen ist nicht reine Prozesstransparenz erforderlich, sondern "Prozesstransparenz, es sei denn, Sie müssen sich darum kümmern". COM bietet diese Funktion, indem einem Objekt implementor ermöglicht wird, benutzerdefiniertes *Marshalling* (auch [**als IMarshal-Marshalling**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) bezeichnet) zu unterstützen. Standard-Marshalling ist tatsächlich eine Instanz des benutzerdefinierten Marshallings. Es handelt sich um die Standardimplementierung, die verwendet wird, wenn ein Objekt kein benutzerdefiniertes Marshalling erfordert.

Sie können benutzerdefiniertes Marshalling implementieren, damit ein Objekt andere Aktionen ausführen kann, wenn es über ein Netzwerk verwendet wird, als es unter lokalem Zugriff benötigt, und es ist für den Client vollständig transparent. Diese Architektur ermöglicht das Entwerfen von Client-/Objektschnittstellen ohne Hinweis auf Netzwerkleistungsprobleme und später das Beheben von Problemen mit der Netzwerkleistung, ohne den etablierten Entwurf zu unterbrechen.

COM gibt nicht an, wie Komponenten strukturiert sind. sie gibt an, wie sie interagieren. COM überlässt programmiersprachen und Entwicklungsumgebungen das Problem der internen Struktur einer Komponente. Im Gegensatz dazu haben Programmierumgebungen keine festgelegten Standards für die Arbeit mit Objekten außerhalb der unmittelbaren Anwendung. Microsoft Visual C++ funktioniert beispielsweise sehr gut zum Bearbeiten von Objekten in einer Anwendung, bietet jedoch keine Unterstützung für die Arbeit mit Objekten außerhalb der Anwendung. Im Allgemeinen sind alle anderen Programmiersprachen in dieser Hinsicht identisch. Um eine netzwerkweite Interoperabilität zu gewährleisten, wählt COM daher über sprachunabhängige Schnittstellen die Stelle aus, an der Programmiersprachen ausgeschaltet werden.

Die doppelte Dekonsensierung der vtbl-Struktur bedeutet, dass die Zeiger in der Tabelle der Funktionszeder nicht direkt auf die tatsächliche Implementierung im realen Objekt verweisen müssen. Dies ist das Kernstück der Prozesstransparenz.

Bei Prozessservern, bei denen das Objekt direkt in den Clientprozess geladen wird, zeigen die Funktionsze zeiger in der Tabelle direkt auf die tatsächliche Implementierung. In diesem Fall überträgt ein Funktionsaufruf vom Client an eine Schnittstellenmethode die Ausführungssteuerung direkt an die -Methode. Dies funktioniert jedoch nicht für lokale Objekte , geschweige denn für Remoteobjekte, da Zeiger auf den Arbeitsspeicher nicht von Prozessen gemeinsam genutzt werden können. Trotzdem muss der Client Schnittstellenmethoden aufrufen können, als ob er die tatsächliche Implementierung aufruft. Daher überträgt der Client die Steuerung einheitlich an eine Methode in einem -Objekt, indem er den -Aufruf aufruft.

Ein Client ruft immer Schnittstellenmethoden in einem In-Process-Objekt auf. Wenn das eigentliche Objekt lokal oder remote ist, erfolgt der Aufruf an ein Proxyobjekt, das dann einen Remoteprozeduraufruf an das eigentliche Objekt vor sich geht.

Welche Methode wird also tatsächlich ausgeführt? Die Antwort ist, dass bei jedem Aufruf einer Out-of-Process-Schnittstelle jede Schnittstellenmethode von einem Proxyobjekt implementiert wird. Das Proxyobjekt ist immer ein prozessin bearbeitungsbasiertes Objekt, das für das aufgerufene Objekt fungiert. Dieses Proxyobjekt weiß, dass das eigentliche Objekt auf einem lokalen oder Remoteserver ausgeführt wird.

Das Proxyobjekt packt die Funktionsparameter in einigen Datenpaketen und generiert einen RPC-Aufruf des lokalen oder Remoteobjekts. Dieses Paket wird von einem Stubobjekt im Prozess des Servers auf dem lokalen computer oder einem Remotecomputer empfangen, das die Parameter entpackt und die tatsächliche Implementierung der -Methode aufruft. Wenn diese Funktion zurückgegeben wird, packt der Stub alle out-Parameter und den Rückgabewert und sendet sie zurück an den Proxy, der sie entpackt und an den ursprünglichen Client zurückgibt.

Daher sprechen Client und Server immer miteinander, als ob alles in Bearbeitung wäre. Alle Aufrufe vom Client und alle Aufrufe an den Server sind zu einem bestimmten Zeitpunkt in Bearbeitung. Da jedoch die vtbl-Struktur es einem Agent wie COM ermöglicht, alle Funktionsaufrufe abzufangen und alle Rückgaben von Funktionen auszuführen, kann dieser Agent diese Aufrufe bei Bedarf an einen RPC-Aufruf umleiten. Obwohl In-Process-Aufrufe schneller als Out-of-Process-Aufrufe sind, sind die Prozessunterschiede für client und server vollständig transparent.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Marshallingdetails](marshaling-details.md)
-   [Proxy](proxy.md)
-   [Stub](stub.md)
-   [Kanal](channel.md)
-   [Microsoft RPC](microsoft-rpc.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und -Server](com-clients-and-servers.md)
</dt> <dt>

[Schnittstellen-Marshalling](interface-marshaling.md)
</dt> </dl>

 

 