---
description: Datenstrukturen für die Namensauflösung in Windows Sockets (Winsock).
ms.assetid: 87c54141-41e2-4eaa-ae3b-84598e8281d9
title: Datenstrukturen für die Namensauflösung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf1f76607ade81503a1057dc21890ac38d5ec265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570289"
---
# <a name="name-resolution-data-structures"></a>Datenstrukturen für die Namensauflösung

Es gibt mehrere wichtige Datenstrukturen, die in den Funktionen der Namensauflösung ausgiebig verwendet werden.

## <a name="query-related-data-structures"></a>Query-Related von Datenstrukturen

Die [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur wird zum Erstellen von Abfragen für [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)verwendet und zum Übermitteln von Abfrage Ergebnissen für [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)verwendet. Es handelt sich um eine komplexe Struktur, da Sie Zeiger auf verschiedene andere Strukturen enthält, von denen einige immer noch andere Strukturen referenzieren. Die Beziehung zwischen der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur und den Strukturen, auf die verwiesen wird, wird wie folgt veranschaulicht.

![Beziehung zwischen wsaqueryset und den zugehörigen Strukturen](images/ovrvw3-2.png)

Innerhalb der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur sind die meisten Member selbsterklärend, aber einige verdienen weitere Erläuterungen. Der **dwSize** -Member muss immer mit sizeof (**wsaqueryset**) ausgefüllt werden, da er von Namespace Anbietern verwendet wird, um unterschiedliche Versionen der **wsaqueryset** -Struktur zu erkennen und anzupassen, die möglicherweise im Laufe der Zeit angezeigt werden.

Der **dwoutputflags** -Member wird von einem Namespace Anbieter verwendet, um zusätzliche Informationen zu Abfrage Ergebnissen bereitzustellen. Weitere Informationen finden Sie unter der [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) -Funktion.

Die [**wsaecomparator**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) -Struktur, auf die vom **lpversion** -Member verwiesen wird, wird sowohl für die Abfrage Einschränkung als auch für Ergebnisse verwendet. Für Abfragen gibt der **dwVersion** -Member die gewünschte Version des Dienstanbieter an. Der **echow** -Member ist ein enumerierter Typ, der angibt, wie der Vergleich durchgeführt werden kann. Die Optionen sind comp ist \_ gleich, was erfordert, dass eine genaue Entsprechung in der Version auftritt, oder Comp \_ notless, das angibt, dass die Versionsnummer des dienstanders nicht kleiner ist als der Wert des **dwVersion** -Members.

Die Interpretation von **dwnamespace** und **lpnsproviderid** hängt davon ab, wie die Struktur verwendet wird, und wird weiter unten in den einzelnen Funktionsbeschreibungen beschrieben, die diese Struktur verwenden.

Das **lpszcontext** -Element gilt für hierarchische Namespaces und gibt den Anfangspunkt einer Abfrage oder den Speicherort in der Hierarchie an, in der sich der Dienst befindet. Allgemeine Regeln

-   Der Wert **null**, leer (""), startet die Suche im Standardkontext.
-   Der Wert " \\ " beginnt die Suche am Anfang des Namespace.
-   Bei jedem anderen Wert wird die Suche am vorgesehenen Punkt gestartet.

Anbieter, die keine Kapselung unterstützen, geben möglicherweise einen Fehler zurück, wenn etwas anderes als "" oder " \\ " angegeben ist. Anbieter, die eingeschränkte Einschluss Unterstützung (z. b. Gruppen) unterstützen, müssen "", " \\ " oder einen bestimmten Punkt akzeptieren. Kontexte sind Namespace spezifisch. Wenn der **dwnamespace** -Member \_ "NS all" ist, sollte nur "" oder " \\ " als Kontext weitergegeben werden, da diese von allen Namespaces erkannt werden.

Der **lpszquerystring** -Member wird verwendet, um zusätzliche, Namespace spezifische Abfrage Informationen bereitzustellen, z. b. eine Zeichenfolge, die einen bekannten Dienst-und Transportprotokoll Namen beschreibt, wie in "FTP/TCP".

Die [**afprotokolls**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) -Struktur, auf die durch den **lpafpprotokolls** -Member verwiesen wird, wird nur zu Abfrage Zwecken verwendet und stellt eine Liste von Protokollen bereit, um die Abfrage einzuschränken. Diese Protokolle werden als Paare von (Adressfamilie, Protokoll) dargestellt, da Protokoll Werte nur im Kontext einer Adressfamilie Bedeutung haben.

Das Array der [**csaddr- \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Informationsstruktur, auf das vom **lpcsabuffer** -Member verwiesen wird, enthält alle Informationen, die entweder für einen Dienst zum Einrichten einer Überwachung oder für einen Client zum Herstellen einer Verbindung mit dem Dienst verwendet werden müssen. Die Member **localaddr** und **remoteaddr** enthalten beide direkt eine [**socketadressstruktur \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) .

Ein Dienst erstellt einen Socket durch Aufrufen der [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -oder [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) -Funktion mit dem Tupel von *localaddr. lpsockaddr->SA- \_ Familie*, *isockettype* und *iProtocol* als Parameter. Ein Dienst bindet den Socket an eine lokale Adresse, indem er die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion mithilfe von " *localaddr. lpsockaddr* " und " *localaddr. lpsockaddrlength* " als Parameter anruft.

Ein Client erstellt seinen Socket durch Aufrufen der [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -oder [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) -Funktion mit dem Tupel von *localaddr. lpsockaddr->SA- \_ Familie*, *isockettype* und *iProtocol* als Parameter. Ein Client verwendet die Kombination aus *remoteaddr. lpsockaddr* und *remoteaddr. lpsockaddrlength* als Parameter, wenn er eine Remote Verbindung mithilfe der [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)-, [**connectex**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)-oder [**wsaconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) -Funktion herstellt.

## <a name="service-class-data-structures"></a>Dienst Klassen-Datenstrukturen

Wenn eine neue Dienstklasse installiert wird, muss eine [**wsaserviceclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) -Struktur vorbereitet und bereitgestellt werden. Diese Struktur besteht auch aus Unterstrukturen, die eine Reihe von Membern enthalten, die auf bestimmte Namespaces angewendet werden. Eine Datenstruktur der Klassen Info sieht wie folgt aus:

![Architektur der Dienst Klassen-Datenstrukturen](images/ovrvw3-3.png)

Für jede Dienstklasse gibt es eine einzelne [**wsaserviceclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) -Struktur. Innerhalb der [**wsaserviceclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) -Struktur ist der eindeutige Bezeichner der Dienstklasse im **lpserviceclassid-** Member enthalten, und auf eine zugeordnete Anzeige Zeichenfolge wird vom **lpserviceclassname** -Member verwiesen. Dies ist die Zeichenfolge, die von der [**wsagetserviceclassnamebyclassid-**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) Funktion zurückgegeben wird.

Der **lpclassinfos** -Member in der [**wsaserviceclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) -Struktur verweist auf ein Array von **wsansclassinfo** -Strukturen, von denen jedes einen benannten und typisierten Member bereitstellt, der für einen angegebenen Namespace gilt. Beispiele für Werte für den Member **lpszname** : "SAPID", "TcpPort", "UDPPort" usw. Diese Zeichen folgen sind in der Regel spezifisch für den Namespace, der im **dwnamespace** -Member identifiziert wird. Typische Werte für den **dwvaluetype** -Member sind "reg \_ DWORD", "reg \_ SZ" usw. Der **dwvaluesize** -Member gibt die Länge des Datenelements an, auf das von **lpValue** verwiesen wird.

Die gesamte Sammlung von Daten, die in einer **wsaserviceclassinfo** -Struktur dargestellt wird, wird für jeden Namespace Anbieter bereitgestellt, wenn die [**wsainstallserviceclass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) -Funktion aufgerufen wird. Jeder einzelne Namespace Anbieter durchläuft dann die Liste der **wsansclassinfo** -Strukturen und behält die für ihn anwendbaren Informationen bei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Afprotokolle**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)
</dt> <dt>

[**csaddr- \_ Informationen**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[Namens Auflösungs Modell](name-resolution-model-2.md)
</dt> <dt>

[Protokoll unabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> <dt>

[**\_Socketadresse**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)
</dt> <dt>

[Zusammenfassung der namens Auflösungs Funktionen](summary-of-name-resolution-functions-2.md)
</dt> <dt>

[**Wsaecomparator**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator)
</dt> <dt>

[**Wsagetserviceclassnamebyclassid**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**Wsainstallserviceclass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**Wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**Wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**Wsaserviceclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)
</dt> </dl>

 

 
