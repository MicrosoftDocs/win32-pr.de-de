---
title: Inter-Object Kommunikation
description: COM ist so konzipiert, dass Clients transparent mit Objekten kommunizieren können, unabhängig davon, wo diese Objekte im gleichen Prozess, auf demselben Computer oder auf einem anderen Computer ausgeführt werden.
ms.assetid: dd4adafb-a7e4-44ba-ae4a-80585875ecb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9356ba2bcb9dd3a6a56ac16c354f3abcb752d717
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102386"
---
# <a name="inter-object-communication"></a>Inter-Object Kommunikation

COM ist so konzipiert, dass Clients transparent mit Objekten kommunizieren können, unabhängig davon, wo diese Objekte in demselben Prozess, auf demselben Computer oder auf einem anderen Computer durchlaufen werden. Dadurch wird ein einzelnes Programmiermodell für alle Objekttypen und für Objekt Clients und Objekt Server bereitstellt.

Aus Sicht eines Clients erfolgt der Zugriff auf alle Objekte über Schnittstellen Zeiger. Ein Zeiger muss in Verarbeitung sein. Tatsächlich erreicht jeder Aufrufe einer Schnittstellenfunktion immer zuerst ein Teil des in-Process-Codes. Wenn das Objekt in Bearbeitung ist, erreicht der-Befehl es direkt und ohne dazwischenliegenden Systeminfrastruktur Code. Wenn das Objekt außerhalb des Prozesses ist, erreicht der Aufruf zuerst das, was als "Proxy"-Objekt bezeichnet wird, das entweder durch com oder durch das-Objekt bereitgestellt wird (wenn der Implementierungs Vorgang wünscht). Die Proxy Pakete rufen Parameter (einschließlich der Schnittstellen Zeiger) auf und generieren den entsprechenden Remote Prozedur Aufrufe (oder einen anderen Kommunikationsmechanismus im Fall von benutzerdefinierten Proxys) für den anderen Prozess oder den anderen Computer, auf dem sich die Objekt Implementierung befindet. Dieser Prozess zum Packen von Zeigern für die Übertragung über Prozess Grenzen hinweg *wird als* Marshalling bezeichnet.

Aus Sicht eines Servers werden alle Aufrufe der Schnittstellen Funktionen eines Objekts über einen Zeiger auf diese Schnittstelle durchgeführt. Auch hier hat ein Zeiger nur Kontext in einem einzelnen Prozess, und der Aufrufer muss immer ein Teil des in-Process-Codes sein. Wenn das Objekt in Bearbeitung ist, ist der Aufrufer der Client selbst. Andernfalls ist der Aufrufer ein "Stub"-Objekt, das entweder durch com oder das Objekt selbst bereitgestellt wird. Der Stub empfängt den Remote Prozedur Aufruf (oder einen anderen Kommunikationsmechanismus im Fall von benutzerdefinierten generierten Proxys) vom "Proxy" im Client Prozess, entmarsheitet die Parameter und ruft die entsprechende Schnittstelle für das Server Objekt auf. Aus Sicht der Sicht von Clients und Servern kommunizieren Sie immer direkt mit einem anderen Prozess internen Code.

COM stellt eine Marshalling-Implementierung dar, die als *Standardmarshalling* bezeichnet wird. Diese Implementierung funktioniert sehr gut für die meisten Objekte und reduziert die Programmier Anforderungen erheblich, sodass der Marshallingprozess effektiv transparent wird.

Die klare Trennung der-Schnittstelle von der Implementierung der Prozesstransparenz von com kann jedoch in einigen Situationen sinnvoll sein. Der Entwurf einer Schnittstelle, die sich auf die Funktion aus der Sicht des Clients konzentriert, kann manchmal zu Entwurfsentscheidungen führen, die mit einer effizienten Implementierung dieser Schnittstelle in einem Netzwerk in Konflikt stehen. In solchen Fällen ist es erforderlich, dass es sich nicht um reine Prozesstransparenz, sondern um die Prozesstransparenz handelt, es sei denn, Sie müssen sich kümmern. COM bietet diese Funktion, indem es einem Objekt Implementierer ermöglicht, ein *benutzerdefiniertes* Marshalling (auch als " [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) Marshalling" bezeichnet) zu unterstützen. Standard mäßiges Marshalling ist tatsächlich eine Instanz von benutzerdefiniertem Marshalling; Dies ist die Standard Implementierung, die verwendet wird, wenn für ein Objekt kein benutzerdefiniertes Marshalling erforderlich ist.

Sie können das benutzerdefinierte Marshalling implementieren, damit ein Objekt verschiedene Aktionen durchführen kann, wenn es in einem Netzwerk verwendet wird, das in einem Netzwerk verwendet wird, und es für den Client vollständig transparent ist. Diese Architektur ermöglicht das Entwerfen von Client-/Objekt-Schnittstellen ohne Berücksichtigung von Netzwerk Leistungsproblemen und später, um Netzwerk Leistungsprobleme zu beheben, ohne den eingerichteten Entwurf zu unterbrechen.

COM gibt nicht an, wie Komponenten strukturiert werden. Gibt an, wie Sie interagieren. COM unterscheidet sich von der internen Struktur einer Komponente für Programmiersprachen und Entwicklungsumgebungen. Im Gegensatz dazu haben Programmierumgebungen keine festgelegten Standards zum Arbeiten mit Objekten außerhalb der unmittelbaren Anwendung. Microsoft Visual C++ z. b. sehr gut für die Bearbeitung von Objekten in einer Anwendung, aber keine Unterstützung für das Arbeiten mit Objekten außerhalb der Anwendung. Im Allgemeinen sind alle anderen Programmiersprachen in dieser Hinsicht identisch. Daher wird für die Bereitstellung von networkwide Interoperabilität, com, über sprachunabhängige Schnittstellen ausgewählt, wo die Programmiersprachen verlassen werden.

Die doppelte Dereferenzierung der VTBL-Struktur bedeutet, dass die Zeiger in der Tabelle der Funktionszeiger nicht direkt auf die tatsächliche Implementierung im echten-Objekt verweisen müssen. Dies ist das Herzstück der Prozesstransparenz.

Bei Prozess internen Servern, bei denen das Objekt direkt in den Client Prozess geladen wird, werden die Funktionszeiger in der Tabelle direkt auf die tatsächliche Implementierung festgelegt. In diesem Fall überträgt ein Funktionsaufrufe vom Client an eine Schnittstellen Methode direkt die Ausführungs Steuerung an die-Methode. Dies funktioniert jedoch nicht für lokale, nicht-Remote Objekte, da Zeiger auf den Arbeitsspeicher nicht von Prozessen gemeinsam verwendet werden können. Dennoch muss der Client in der Lage sein, Schnittstellen Methoden aufzurufen, als ob er die tatsächliche Implementierung aufruft. Folglich überträgt der Client die Steuerung gleichmäßig an eine Methode in einem Objekt, indem er den-Befehl aufruft.

Ein Client ruft immer Schnittstellen Methoden in einem in-Process-Objekt auf. Wenn das eigentliche Objekt lokal oder Remote ist, wird der-Vorgang an ein Proxy Objekt gerichtet, das dann einen Remote Prozedur Aufrufvorgang an das tatsächliche-Objekt sendet.

Welche Methode wird tatsächlich ausgeführt? Die Antwort besteht darin, dass jede Schnittstellen Methode bei einem Aufruf einer Out-of-Process-Schnittstelle von einem Proxy Objekt implementiert wird. Das Proxy Objekt ist immer ein Prozess interner Objekt, das im Namen des aufgerufenen Objekts fungiert. Dieses Proxy Objekt weiß, dass das tatsächliche-Objekt auf einem lokalen Server oder Remote Server ausgeführt wird.

Das Proxy Objekt verpackt die Funktionsparameter in einigen Datenpaketen und generiert einen RPC-Aufruf an das lokale oder Remote Objekt. Dieses Paket wird von einem Stub-Objekt im Server Prozess auf dem lokalen Computer oder einem Remote Computer übernommen, der die Parameter entpackt und die tatsächliche Implementierung der Methode aufruft. Wenn diese Funktion zurückgibt, verpackt der Stub alle out-Parameter und den Rückgabewert und sendet Sie zurück an den Proxy, der Sie entpackt und an den ursprünglichen Client zurückgibt.

Daher kommunizieren Client und Server immer miteinander, als ob alles in Verarbeitung wäre. Alle Aufrufe vom Client und alle Aufrufe an den Server werden zu einem bestimmten Zeitpunkt in den Prozess verarbeitet. Da die VTBL-Struktur es jedoch ermöglicht, dass ein Agent (z. b. com) alle Funktionsaufrufe abfängt und alle Rückgabe Vorgänge von Funktionen durchführt, kann dieser Agent diese Aufrufe nach Bedarf an einen RPC-Aufruf umleiten. Obwohl Prozess interne Aufrufe schneller als prozessübergreifende Aufrufe sind, sind die Prozess Unterschiede für Client und Server vollständig transparent.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Marshalling von Details](marshaling-details.md)
-   [Proxy](proxy.md)
-   [Stub](stub.md)
-   [Kanal](channel.md)
-   [Microsoft RPC](microsoft-rpc.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und-Server](com-clients-and-servers.md)
</dt> <dt>

[Schnittstellenmarshalling](interface-marshaling.md)
</dt> </dl>

 

 