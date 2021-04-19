---
description: Dieser Abschnitt enthält eine Übersicht über die Division der Zuständigkeit zwischen den Ws2 \_ -32.dll und Transport Dienstanbietern.
ms.assetid: e1ea1e99-a2bc-4e76-91f6-e388c39dfbbb
title: Transport Division von Zuständigkeiten zwischen dll-und Dienstanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142ac98c95e95c310c2eefb7bfdaf1f70a03bf28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363272"
---
# <a name="transport-division-of-responsibilities-between-dll-and-service-providers"></a>Transport Division von Zuständigkeiten zwischen dll-und Dienstanbietern

Dieser Abschnitt enthält eine Übersicht über die Division der Zuständigkeit zwischen den Ws2 \_ -32.dll und Transport Dienstanbietern.

## <a name="ws2_32dll-functionality-for-transport"></a>Ws2 \_32.dll-Funktionalität für Transport

Die Hauptaufgabe des Datentransport Teils der Ws2 \_ -32.dll besteht darin, als Traffic Manager zwischen Dienstanbietern und Anwendungen zu fungieren. Wenn verschiedene Dienstanbieter mit derselben Anwendung interagieren, interagiert jeder Dienstanbieter strikt mit dem Ws2- \_32.dll. Die DLL übernimmt Folgendes:

-   Auswählen eines geeigneten Dienstanbieters zum Erstellen von Sockets basierend auf einer Protokoll Beschreibung.
-   Weiterleiten von Anwendungs Prozedur aufrufen mit einem Socket an den entsprechenden Dienstanbieter, der den Socket erstellt oder steuert. Dienstanbieter wissen nicht, dass diese Vorgänge auftreten.

Sie müssen sich nicht um die Details der Zusammenarbeit mit einem anderen oder sogar über das vorhanden sein anderer Dienstanbieter kümmern. Durch die Abstraktion der Dienstanbieter in eine konsistente DLL-Schnittstelle und durch das Ausführen dieser automatischen Datenverkehrs Routing Funktion ermöglicht die Ws2- \_32.dll Anwendungen die Interaktion mit einer Vielzahl von Anbietern, ohne dass die Anwendungen die Unterschiede zwischen den Anbietern kennen müssen, in denen verschiedene Anbieter installiert sind.

Die Ws2 \_ -32.dll basiert auf den Parametern der API-socketerstellungs-Funktionen ( [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) und [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)), um zu bestimmen, welcher Dienstanbieter verwendet werden soll. Der ausgewählte Transport Dienstanbieter wird über die [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) -Funktion aufgerufen. Im Fall der **Socket** -Funktion findet der Ws2- \_32.dll den ersten Eintrag im Satz installierter [**wsaprotocol- \_ Info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Strukturen, der den Werten entspricht, die im Tupel mit den Parametern (*Adressfamilie*, *socketyp*, *Protokoll*) angegeben sind. Um die Abwärtskompatibilität zu erhalten, behandelt der Ws2- \_32.dll den Wert 0 (null) entweder für die *Adressfamilie* oder den *Sockettyp* als Platzhalter Wert. Der Wert 0 (null) für das Protokoll wird vom Ws2-32.dll nicht als Platzhalter Wert betrachtet, \_ es sei denn, für ein bestimmtes Protokoll ist ein solches Verhalten festgelegt, indem das Pfl- \_ \_ Flag für Protokoll \_ 0 in der **wsaprotocol- \_ Informations** Struktur festgelegt

Wenn für die [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) -Funktion der Wert NULL für *lpprotocolinfo* angegeben wird, ist das Verhalten genau so, wie es nur für [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)beschrieben wird. Wenn jedoch auf eine [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur verwiesen wird, führt der Ws2- \_32.dll keine übereinstimmende Funktion aus, sondern leitet die socketerstellungs-Anforderung sofort an den Transport Dienstanbieter weiter, der der angeordneten **wsaprotocol- \_ Informations** Struktur zugeordnet ist. Die Werte für das Tupel (*Adressfamilie,* *socketyp*) werden für den Dienstanbieter in der [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) -Funktion intakt bereitgestellt. Dienstanbieter können die Werte der Parameter (*Adressfamilie,* *Sockettyp*) nach Bedarf ignorieren oder darauf achten. Sie dürfen jedoch nicht auf eine Fehlerbedingung hinweisen, wenn der Wert von *Adressfamilie* oder *Sockettyp* gleich NULL ist. Außerdem dürfen Dienstanbieter keine Fehlerbedingung angeben, wenn die Manifest-Konstante von \_ Protokoll \_ Informationen in einem der Parameter (*Adressfamilie,* *socketyp*) enthalten ist. Dieser Wert gibt lediglich an, dass die Anwendung die Werte verwenden möchte, die in den entsprechenden Parametern der **wsaprotocol- \_ Informations** Struktur gefunden werden: (**iaddressfamily**, **isockettype**, **iProtocol**).

Im Rahmen der Socketerstellung informiert ein Dienstanbieter den Ws2 \_32.dll über die Zuordnung zwischen sich selbst und dem neuen Socket mithilfe von Parametern, die an [**wpukreatesockethandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) oder [**wpumodifyifshandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle)übergeben werden. Der Ws2 \_ -32.dll verfolgt diese Zuordnung zwischen Sockethandles und bestimmten Dienstanbietern nach. Wenn eine Anwendungsschnittstellen Funktion aufgerufen wird, die auf ein Sockethandle verweist, \_ sucht der Ws2-32.dll nach der Zuordnung und ruft die entsprechende Funktion der Dienstanbieter Schnittstelle des entsprechenden Dienstanbieters auf.

Neben dem umfangreichen Datenverkehrs Routing Dienst bietet die Ws2- \_32.dll eine Reihe von anderen Diensten, z. b. protokollenumeration, socketdeskriptorverwaltung (Zuordnung, Aufhebung der Zuordnung und Zuordnung von Kontext Werten für nicht-Dateisystem Dienstanbieter, Blockieren der hookverwaltung auf Thread Basis, Byte Austausch-Hilfsprogramme, Warteschlangen von asynchronen Prozedur aufrufen (APCs) zum Vereinfachen des Aufrufs von e/a-Abschluss Routinen und Versions Aushandlung zwischen Anwendungen und der Ws2- \_32.dll sowie zwischen den Ws2 \_ -32.dll und-Dienstanbietern.

## <a name="transport-service-provider-functionality"></a>Funktionen des Transport Dienstanbieters

Dienstanbieter implementieren das eigentliche Transportprotokoll, das Funktionen wie das Einrichten von Verbindungen, das Übertragen von Daten, das Üben der Fluss Steuerung und die Fehler Steuerung usw. umfasst. Der Ws2- \_32.dll hat keine Kenntnis darüber, wie Anforderungen an Dienstanbieter realisiert werden. Dies liegt an der Implementierung des Dienstanbieters. Die Implementierung solcher Funktionen kann sich stark von einem Anbieter zu einem anderen unterscheiden. Dienstanbieter verbergen die Implementierungs spezifischen Details der Art und Weise, wie Netzwerk Vorgänge ausgeführt werden.

Transport Dienstanbieter können weitgehend in zwei Kategorien unterteilt werden: bei den socketdeskriptoren handelt es sich um echte Dateisystem Handles (und werden im folgenden als "Installable File System"-Anbieter (IFS) bezeichnet. der Rest wird als nicht-IFS-Anbieter bezeichnet. Der Ws2 \_ -32.dll übergibt den socketdeskriptor des Transport Dienstanbieters immer an die Windows Sockets-Anwendung, sodass Anwendungen die Vorteile von socketdeskriptoren nutzen können, bei denen es sich um Dateisystem Handles handelt.

Zusammenfassend: Dienstanbieter implementieren die Netzwerk spezifischen Protokolle auf niedriger Ebene. Der Ws2- \_32.dll bietet die mittlere Datenverkehrs Verwaltung, die diese Transportprotokolle mit Anwendungen verbindet. Anwendungen stellen wiederum die Richtlinie dafür bereit, wie diese Daten Verkehrsströme und Netzwerk spezifischen Vorgänge verwendet werden, um die vom Benutzer gewünschten Funktionen zu erfüllen.

 

 
