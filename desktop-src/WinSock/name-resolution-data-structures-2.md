---
description: Namensauflösungsdatenstrukturen in Windows Sockets (Winsock).
ms.assetid: 87c54141-41e2-4eaa-ae3b-84598e8281d9
title: Namensauflösungsdatenstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e6f3b889d295241bb0cdb9c0182babf0c5b8115e7eff7e86c27b65c992c452
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794790"
---
# <a name="name-resolution-data-structures"></a>Namensauflösungsdatenstrukturen

Es gibt mehrere wichtige Datenstrukturen, die in den Namensauflösungsfunktionen umfassend verwendet werden.

## <a name="query-related-data-structures"></a>Query-Related Datenstrukturen

Die [**WSAQUERYSET-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) wird verwendet, um Abfragen für [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)zu erstellen, und verwendet, um Abfrageergebnisse für [**WSALookupServiceNext zu liefern.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) Es handelt sich um eine komplexe Struktur, da sie Zeiger auf mehrere andere Strukturen enthält, von denen einige auf andere Strukturen verweisen. Die Beziehung zwischen der [**WSAQUERYSET-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) und den Strukturen, auf die verwiesen wird, wird wie folgt veranschaulicht.

![Beziehung zwischen wsaqueryset und den zugehörigen Strukturen](images/ovrvw3-2.png)

Innerhalb der [**WSAQUERYSET-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) sind die meisten Member selbsterklärend, aber einige sind eine zusätzliche Erklärung. Der **dwSize-Member** muss immer mit sizeof(**WSAQUERYSET)** gefüllt werden, da dies von Namespaceanbietern verwendet wird, um verschiedene Versionen der **WSAQUERYSET-Struktur** zu erkennen und sich an diese anzupassen, die im Laufe der Zeit auftreten können.

Der **dwOutputFlags-Member** wird von einem Namespaceanbieter verwendet, um zusätzliche Informationen zu Abfrageergebnissen zur Verfügung zu stellen. Weitere Informationen finden Sie in der [**WSALookupServiceNext-Funktion.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)

Die [**WSAECOMPARATOR-Struktur,**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) auf die vom **lpversion-Member** verwiesen wird, wird sowohl für Abfrageeinschränkungen als auch für Ergebnisse verwendet. Bei Abfragen gibt das **dwVersion-Mitglied** die gewünschte Version des Diensts an. Der **ecHow-Member** ist ein aufzählter Typ, der angibt, wie der Vergleich vorgenommen werden kann. Die Optionen sind COMP EQUALS, was erfordert, dass eine genaue Übereinstimmung in der Version auftritt, oder COMP NOTLESS, die angibt, dass die Versionsnummer des Diensts nicht kleiner als der Wert des \_ \_ **dwVersion-Mitglieds** ist.

Die Interpretation von **dwNameSpace** und **lpNSProviderId** hängt davon ab, wie die Struktur verwendet wird, und wird in den einzelnen Funktionsbeschreibungen, die diese Struktur verwenden, weiter beschrieben.

Das **lpszContext-Element** gilt für hierarchische Namespaces und gibt den Ausgangspunkt einer Abfrage oder den Speicherort innerhalb der Hierarchie an, in der sich der Dienst befindet. Allgemeine Regeln

-   Der Wert **NULL**, leer ("") startet die Suche im Standardkontext.
-   Der Wert " \\ " startet die Suche am Anfang des Namespace.
-   Jeder andere Wert startet die Suche am angegebenen Punkt.

Anbieter, die keine Stützung unterstützen, geben möglicherweise einen Fehler zurück, wenn etwas anderes als "" oder " \\ " " angegeben ist. Anbieter, die eine eingeschränkte Stützung unterstützen, z. B. Gruppen, sollten "", " " oder einen \\ angegebenen Punkt akzeptieren. Kontexte sind namespacespezifisch. Wenn der **dwNameSpace-Member** NS ALL ist, sollte nur "" oder " " " als Kontext übergeben werden, da diese von allen \_ \\ Namespaces erkannt werden.

Der **lpszQueryString-Member** wird verwendet, um zusätzliche namespacespezifische Abfrageinformationen wie eine Zeichenfolge zur Beschreibung eines bekannten Dienst- und Transportprotokollnamens wie in "FTP/TCP" zu liefern.

Die [**AFPROTOCOLS-Struktur,**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) auf die das **lpafpProtocols-Member** verweist, wird nur zu Abfragezwecken verwendet und stellt eine Liste von Protokollen zur Einschränkung der Abfrage zur Verfügung. Diese Protokolle werden als Paare (Adressfamilie, Protokoll) dargestellt, da Protokollwerte nur innerhalb des Kontexts einer Adressfamilie eine Bedeutung haben.

Das Array der [**CSADDR \_ INFO-Struktur,**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) auf die vom **lpcsaBuffer-Member** verwiesen wird, enthält alle Informationen, die für einen Dienst zum Einrichten eines Lauschens oder für einen Client zum Herstellen einer Verbindung mit dem Dienst erforderlich sind. Die **Member LocalAddr** **und RemoteAddr** enthalten beide direkt eine [**SOCKET \_ ADDRESS-Struktur.**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)

Ein Dienst würde einen Socket [](/windows/desktop/api/Winsock2/nf-winsock2-socket) erstellen, indem er die Socket- oder [**WSASocket-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) mithilfe des Tupels *von LocalAddr.lpSockaddr->sa \_ family,* *iSocketType* und *iProtocol* als Parameter aufruft. Ein Dienst würde den Socket an eine lokale Adresse binden, indem er die [**bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) mit *localAddr.lpSockaddr* und *LocalAddr.lpSockaddrLength* als Parameter aufruft.

Ein Client erstellt seinen [](/windows/desktop/api/Winsock2/nf-winsock2-socket) Socket, indem er die Socket- oder [**WSASocket-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) mithilfe des Tupels *von LocalAddr.lpSockaddr->sa \_ family,* *iSocketType* und *iProtocol* als Parameter aufruft. Ein Client verwendet die Kombination aus *RemoteAddr.lpSockaddr* und *RemoteAddr.lpSockaddrLength* als Parameter, wenn eine Remoteverbindung mithilfe der Connect-, [](/windows/desktop/api/Winsock2/nf-winsock2-connect) [**ConnectEx-**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)oder [**WSAConnect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) hergestellt wird.

## <a name="service-class-data-structures"></a>Datenstrukturen der Dienstklasse

Wenn eine neue Dienstklasse installiert wird, muss eine [**WSASERVICECLASSINFO-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) vorbereitet und bereitgestellt werden. Diese Struktur besteht auch aus Unterstrukturen, die eine Reihe von Membern enthalten, die für bestimmte Namespaces gelten. Eine Klasseninformationsdatenstruktur ist wie folgt:

![Architektur von Dienstklassendatenstrukturen](images/ovrvw3-3.png)

Für jede Dienstklasse gibt es eine einzelne [**WSASERVICECLASSINFO-Struktur.**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) Innerhalb der [**WSASERVICECLASSINFO-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) ist der eindeutige Bezeichner der Dienstklasse im **lpServiceClassId-Member** enthalten, und auf eine zugeordnete Anzeigezeichenfolge wird vom **lpServiceClassName-Member** verwiesen. Dies ist die Zeichenfolge, die von der [**WSAGetServiceClassNameByClassId-Funktion zurückgegeben**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) wird.

Der **lpClassInfos-Member** in der [**WSASERVICECLASSINFO-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) verweist auf ein Array von **WSANSCLASSINFO-Strukturen,** von denen jedes einen benannten und typierten Member liefert, der für einen angegebenen Namespace gilt. Beispiele für Werte für **den lpszName-Member** sind: "SapId", "TcpPort", "UdpPort" usw. Diese Zeichenfolgen sind im Allgemeinen spezifisch für den Namespace, der im **dwNameSpace-Member identifiziert** wird. Typische Werte für das **dwValueType-Member** können REG \_ DWORD, REG \_ SZ usw. sein. Das **dwValueSize-Element** gibt die Länge des Datenelements an, auf das **lpValue zeigt.**

Die gesamte Auflistung von Daten, die in einer **WSASERVICECLASSINFO-Struktur** dargestellt werden, wird für jeden Namespaceanbieter bereitgestellt, wenn die [**WSAInstallServiceClass-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) aufgerufen wird. Jeder einzelne Namespaceanbieter durchsingt dann die Liste der **WSANSCLASSINFO-Strukturen** und behält die entsprechenden Informationen bei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)
</dt> <dt>

[**\_CSADDR-INFORMATIONEN**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[Namensauflösungsmodell](name-resolution-model-2.md)
</dt> <dt>

[Protokollunabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> <dt>

[**\_SOCKETADRESSE**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)
</dt> <dt>

[Zusammenfassung der Namensauflösungsfunktionen](summary-of-name-resolution-functions-2.md)
</dt> <dt>

[**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator)
</dt> <dt>

[**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)
</dt> </dl>

 

 
