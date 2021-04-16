---
description: Die wsaqueryset-Struktur wird verwendet, um Abfragen für die nsplookupservicebegin-Funktion zu erstellen und zum Übermitteln von Abfrage Ergebnissen für die nsplookupservicenext-Funktion zu verwenden.
ms.assetid: 017b5828-bc6e-42b7-aba7-21648b2dd707
title: Query-Related von Datenstrukturen in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ce5a7016bd2ad96f464137177036b470c64a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565959"
---
# <a name="query-related-data-structures-in-the-spi"></a>Query-Related von Datenstrukturen in der SPI

Die [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur wird zum Erstellen von Abfragen für [**nsplookupservicebegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)verwendet und zum Übermitteln von Abfrage Ergebnissen für [**nsplookupservicenext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)verwendet. Es handelt sich um eine komplexe Struktur, da Sie Zeiger auf verschiedene andere Strukturen enthält, von denen einige immer noch andere Strukturen referenzieren. Die Beziehung zwischen **wsaqueryset** und den Strukturen, auf die verwiesen wird, ist wie folgt dargestellt:

![wsaqueryset-Strukturen](images/ovrvw3-2.png)

Innerhalb der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur sind die meisten Member selbsterklärend, aber einige verdienen weitere Erläuterungen. Die **dwSize** wird mit sizeof ( **wsaqueryset**) gefüllt und kann von Namespace Anbietern verwendet werden, um unterschiedliche Versionen der möglicherweise angezeigten **wsaqueryset** -Struktur zu erkennen und anzupassen.

Der **dwoutputflags** -Member wird von einem Namespace Anbieter verwendet, um zusätzliche Daten über Abfrageergebnisse bereitzustellen. Weitere Informationen finden Sie unter [**nsplookupservicenext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext).

Die von **lpversion** referenzierte [**wsaecomparator**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) -Struktur wird sowohl für die Abfrage Einschränkung als auch für Ergebnisse verwendet. Für Abfragen gibt der **dwVersion** -Member die gewünschte Version des Dienstanbieter an. Der **echow** -Member ist ein enumerierter Typ, der angibt, wie der Vergleich durchgeführt wird. Die Optionen sind "Comp gleich", \_ was erfordert, dass eine genaue Entsprechung in der Version auftritt, oder Comp \_ notless, das angibt, dass die Versionsnummer des diensnicht kleiner ist als der Wert von " **dwVersion**".

Die Interpretation von **dwnamespace** und **lpnsproviderid** hängt davon ab, wie die Struktur verwendet wird, und wird weiter unten in den einzelnen Funktionsbeschreibungen beschrieben, die diese Struktur verwenden.

Das **lpszcontext** -Element gilt für hierarchische Namespaces und gibt den Anfangspunkt einer Abfrage oder den Speicherort in der Hierarchie an, in der sich der Dienst befindet. Allgemeine Regeln

-   Mit dem Wert **null**(leer) wird die Suche im Standardkontext gestartet.
-   Der Wert " \\ " beginnt die Suche am Anfang des Namespace.
-   Bei jedem anderen Wert wird die Suche am vorgesehenen Punkt gestartet.

Anbieter, die keine Kapselung unterstützen, geben möglicherweise einen Fehler zurück, wenn etwas anderes als "" oder " \\ " angegeben ist. Anbieter, die eingeschränkte Einschluss Unterstützung (z. b. Gruppen) unterstützen, müssen "", " \\ " oder einen bestimmten Punkt akzeptieren. Kontexte sind Namespace spezifisch. Wenn **dwnamespace** den Wert NS \_ all hat, sollte nur "" oder " \\ " als Kontext weitergegeben werden, da diese von allen Namespaces erkannt werden.

Der **lpszquerystring** -Member wird verwendet, um zusätzliche, Namespace spezifische Abfrage Informationen bereitzustellen, z. b. eine Zeichenfolge, die einen bekannten Dienst-und Transportprotokoll Namen beschreibt, wie in "FTP/TCP".

Die [**afprotokolls**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) -Struktur, auf die von **lpafpprotokolle** verwiesen wird, wird nur zu Abfrage Zwecken verwendet und stellt eine Liste von Protokollen bereit, um die Abfrage einzuschränken. Diese Protokolle werden als (Adressfamilie, Protokoll Paare) dargestellt, da Protokoll Werte nur im Kontext einer Adressfamilie Bedeutung haben.

Das Array der [**csaddr \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) -Informationsstruktur, auf das von **lpcsabuffer** verwiesen wird, enthält alle Informationen, die erforderlich sind, damit ein Dienst zum Einrichten einer Überwachung verwendet werden kann, oder ein Client, der beim Herstellen einer Verbindung mit dem Dienst verwendet werden soll. Die Member **localaddr** und **remoteaddr** enthalten beide direkt eine [**socketadressstruktur \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) . Ein Dienst erstellt einen Socket mithilfe des Tupels (localaddr. lpsockaddr->SA- \_ Familie, isockettype, iProtocol). Er bindet den Socket mithilfe von "localaddr. lpsockaddr" und "localaddr. lpsockaddrlength" an eine lokale Adresse. Der Client erstellt seinen Socket mit dem Tupel (remoteaddr. lpsockaddr->SA- \_ Familie, isockettype, iProtocol) und verwendet die Kombination aus remoteaddr. lpsockaddr und remoteaddr. lpsockaddrlength beim Herstellen einer Remote Verbindung.

 

 
