---
description: Der Ws2 \_ -32.dll lädt die Schnittstellen-DLL des Dienstanbieters in das System, indem er die standardmäßigen Methoden zum Laden der dynamischen Microsoft Windows-Bibliothek verwendet, und initialisiert sie durch Aufrufen von WSPStartup.
ms.assetid: 6df28d93-8757-45b3-8f05-86381c3be64e
title: Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d6ef10db421ef15f2bb94eb67e96fc2cfc5924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343296"
---
# <a name="initialization"></a>Initialisierung

Der *Ws2- \_32.dll* lädt die Schnittstellen-DLL des Dienstanbieters in das System, indem er die standardmäßigen Methoden zum Laden der dynamischen Microsoft Windows-Bibliothek verwendet, und initialisiert sie durch Aufrufen von [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Dies wird in der Regel von einer Anwendung ausgelöst, die entweder [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) oder [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) aufruft, um einen neuen Socket zu erstellen, der einem Dienstanbieter zugeordnet wird, dessen Schnittstellen-DLL zurzeit nicht in den Arbeitsspeicher geladen wird. Der Pfad zur Schnittstellen-DLL jedes Dienstanbieters wird vom Ws2- *\_32.dll* zu dem Zeitpunkt gespeichert, an dem der Dienstanbieter installiert wird. Weitere Informationen finden Sie unter [Installations-und Konfigurationsfunktionen](installation-and-configuration-functions-2.md) .

Im Laufe der Zeit sind möglicherweise verschiedene Versionen für die Winsock-DLLs,-Anwendungen und-Dienstanbieter vorhanden. Neue Versionen definieren möglicherweise neue Features und neue Parameter für Datenstrukturen und bitparameter usw. Versionsnummern geben daher an, wie verschiedene Datenstrukturen interpretiert werden.

Um eine optimale Mischung und eine Übereinstimmung verschiedener Versionen von Anwendungen, Versionen der Ws2 \_32.dll und Versionen von Dienstanbietern durch unterschiedliche Anbieter zu ermöglichen, stellt der SPI einen Versions Aushandlungs Mechanismus zur Verwendung zwischen dem *Ws2- \_32.dll* und den Dienstanbietern bereit. Diese Versions Aushandlung wird von [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)behandelt. Im Grunde übergibt der *Ws2- \_32.dll* an den Dienstanbieter die höchsten Versionsnummern, mit denen er kompatibel ist. Der Dienstanbieter vergleicht diese mit einem eigenen unterstützten Bereich von Versionsnummern. Wenn sich diese Bereiche überschneiden, gibt der Dienstanbieter einen Wert im überlappenden Bereich des Bereichs als Ergebnis der Aushandlung zurück. In der Regel sollte dies der höchstmögliche Wert sein. Wenn sich die Bereiche nicht überlappen, sind die beiden Parteien nicht kompatibel, und die Funktion gibt einen Fehler zurück.

[**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) muss von jedem Client Prozess mindestens einmal aufgerufen werden und kann durch Ws2 \_32.dll oder andere Entitäten mehrmals aufgerufen werden. Für jeden erfolgreichen **WSPStartup** -Aufruf muss ein entsprechendes [**wspcleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) aufgerufen werden. Der Dienstanbieter sollte einen Verweis Zähler pro Prozess beibehalten. Bei jedem **WSPStartup** -Aufruf kann der Aufrufer eine beliebige Versionsnummer angeben, die von der SP-dll unterstützt wird.

Ein Dienstanbieter muss den Zeiger auf die upsend-Verteilungs Tabelle des Clients speichern, die als [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) -Parameter pro Prozess empfangen wird. Wenn ein bestimmter Prozess **WSPStartup** mehrmals aufruft, darf der Dienstanbieter nur den zuletzt angegebenen dispatchtabellenzeiger verwenden.

Im Rahmen des Initialisierungs Vorgangs des Dienstanbieters ruft der Ws2 \_ -32.dll die dispatchtabelle des Dienstanbieters über den *lpproctable* -Parameter ab, um Einstiegspunkte für die restlichen SPI-Funktionen zu erhalten, die in diesem Dokument angegeben sind.

Die Verwendung einer dispatchtabelle (im Gegensatz zu den üblichen dll-Mechanismen für den Zugriff auf Einstiegspunkte) dient zwei Zwecken:

-   Es ist für die Ws2- \_32.dll bequemer, da ein einzelner-Vorgang zum Ermitteln des gesamten Satzes von Einstiegspunkten durchgeführt werden kann.
-   Dadurch können mehrstufige Dienstanbieter, die in Protokoll Ketten gebildet werden, effizienter arbeiten.

## <a name="initializing-protocol-chains"></a>Protokoll Ketten werden initialisiert.

Zum Zeitpunkt der Installation der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für eine Protokoll Kette wird auch der Pfad zum ersten geschichteten Anbieter in der Kette angegeben. Wenn eine Protokoll Kette initialisiert wird, verwendet der Ws2 \_ -32.dll diesen Pfad zum Laden der Anbieter-DLL und ruft dann [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)auf. Da **WSPStartup** einen Zeiger auf die **wsaprotocol- \_ Informations** Struktur der Kette als einen seiner Parameter enthält, können überlagerte Anbieter ermitteln, in welchen Typ von Kette Sie initialisiert werden, und die Identität der nächst niedrigeren Ebene in der Kette. Ein mehrstufiger Anbieter lädt dann wiederum den nächsten Protokoll Anbieter in der Kette und initialisiert ihn mit einem **WSPStartup**-Aufrufvorgang usw. Wenn die nächste untere Ebene ein weiterer mehrstufiger Anbieter ist, muss im **WSPStartup** -Aufruf auf die **wsaprotocol- \_ Informations** Struktur der Kette verwiesen werden. Wenn es sich bei der nächsten niedrigeren Ebene um ein Basisprotokoll handelt (das das Ende der Kette bezeichnet), wird die **wsaprotocol- \_ Informations** Struktur der Kette nicht mehr nach unten weitergegeben. Stattdessen muss die aktuelle Ebene auf eine **wsaprotocol- \_ Informations** Struktur verweisen, die dem Protokoll entspricht, das der Basis Anbieter verwenden soll. Folglich hat der Basis Anbieter keine Ahnung, dass er an einer Protokoll Kette beteiligt ist.

Die Verteilungs Tabelle, die von einem bestimmten geschichteten Anbieter bereitgestellt wird, wird in vielen Fällen die Einstiegspunkte eines zugrunde liegenden Anbieters duplizieren. Der überlappende Anbieter fügt nur seine eigenen Einstiegspunkte für Funktionen ein, an die er direkt beteiligt sein musste. Beachten Sie jedoch, dass es zwingend erforderlich ist, dass ein mehrstufiger Anbieter den Inhalt der Upcall-Tabelle, die er empfangen hat, beim Aufrufen von [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) auf der nächst niedrigeren Ebene in einer Protokoll Kette nicht ändert. Diese upcalls müssen direkt an die Windows Sockets 2-dll vorgenommen werden.

 

 
