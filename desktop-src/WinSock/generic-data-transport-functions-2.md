---
description: Die von Ws2spi. h verfügbar gemachten Datentransport Funktionen.
ms.assetid: 6900faa3-79bb-4ed8-b83e-148eb10425a0
title: Allgemeine Daten Transport Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63de41b90148210ea8a99d5271b62c5d8bc0c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526174"
---
# <a name="generic-data-transport-functions"></a>Allgemeine Daten Transport Funktionen

In diesem Abschnitt werden die Datentransport Funktionen aufgelistet, die von Ws2spi. h verfügbar gemacht werden.



| Funktion                                                   | BESCHREIBUNG                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wspaccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)                           | Eine eingehende Verbindung wird bestätigt und einem sofort erstellten Socket zugeordnet. Der ursprüngliche Socket wird in den Abhör Zustand zurückversetzt. Diese Funktion ermöglicht außerdem die bedingte Annahme. |
| [**Wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))                 | Führt eine asynchrone Version von [**wspselect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))aus.                                                                                                                                      |
| [**Wspbind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))                               | Weist einem unbenannten Socket einen lokalen Namen zu.                                                                                                                                                              |
| [**Wspcancelblockingcall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85))   | Bricht einen ausstehenden blockierenden Windows Sockets-Befehl ab.                                                                                                                                                   |
| [**Wspcleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))                         | Meldet sich vom zugrunde liegenden Windows Sockets-Dienstanbieter ab.                                                                                                                                         |
| [**Wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                 | Entfernt einen Socket aus der Objekt Verweis Tabelle pro Prozess. Blockiert nur, wenn so \_ LINGER für einen blockierenden Socket mit einem Timeout ungleich NULL festgelegt ist.                                                            |
| [**Wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                         | Initiiert eine Verbindung auf dem angegebenen Socket. Diese Funktion ermöglicht auch den Austausch von Connect-Daten und QoS-Spezifikationen.                                                                           |
| [**Wspduplialisiesocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85))         | Gibt eine [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur zurück, die zum Erstellen eines neuen socketdeskriptors für einen freigegebenen Socket verwendet werden kann.                                                             |
| [**Wspenum networkevents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85))     | Erkennt Vorkommen von Netzwerk Ereignissen.                                                                                                                                                                |
| [**Wspeventselect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))                 | Ordnet Netzwerkereignisse einem Ereignis Objekt zu.                                                                                                                                                         |
| [**Wspgedienst verlappedresult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) | Ruft den Abschluss Status des überlappenden Vorgangs ab.                                                                                                                                                         |
| [**Wspgetpeer Name**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85))                 | Ruft den Namen des Peers ab, der mit dem angegebenen Socket verbunden ist.                                                                                                                                       |
| [**Wspgetsockname**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85))                 | Ruft die lokale Adresse ab, an die der angegebene Socket gebunden ist.                                                                                                                                     |
| [**Wspgetsockopt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))                   | Ruft die dem angegebenen Socket zugeordneten Optionen ab.                                                                                                                                                 |
| [**Wspgetqosbyname**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetqosbyname)               | Liefert QoS-Parameter auf der Grundlage eines bekannten Dienst namens.                                                                                                                                             |
| [**Wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))                             | Stellt das Steuerelement für Sockets bereit.                                                                                                                                                                           |
| [**Wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)                       | Fügt einen Blattknoten in eine Multipoint-Sitzung ein.                                                                                                                                                            |
| [**Wsplauschen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))                           | Lauscht auf eingehende Verbindungen für einen angegebenen Socket.                                                                                                                                                 |
| [**Wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))                               | Empfängt Daten von einem verbundenen oder nicht verbundenen Socket. Diese Funktion kann Punkt-/Sammler-e/a, überlappende Sockets und den flags-Parameter als in/out-Parameter bereitstellen.                                    |
| [**Wsprecvdisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85))           | Beendet den Empfang für einen Socket und ruft die Trenn Daten ab, wenn der Socket verbindungsorientiert ist.                                                                                                |
| [**Wsprecvfrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))                       | Empfängt Daten von einem verbundenen oder nicht verbundenen Socket. Diese Funktion kann Punkt-/Sammler-e/a, überlappende Sockets und den flags-Parameter als in/out-Parameter bereitstellen.                              |
| [**Wspselect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                           | Führt synchrone e/a-Multiplexing aus.                                                                                                                                                                  |
| [**Wspsend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))                               | Sendet Daten an einen verbundenen Socket. Diese Funktion bietet auch eine Punkt-/Sammler-e/a und überlappende Sockets.                                                                                            |
| [**Wspsenddisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))           | Initiiert die Beendigung einer Socketverbindung und sendet optional Trennungs Daten.                                                                                                                       |
| [**Wspsendto**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                           | Sendet Daten an einen verbundenen oder nicht verbundenen Socket. Diese Funktion bietet auch eine Punkt-/Sammler-e/a und überlappende Sockets.                                                                      |
| [**Wspsetsockopt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))                   | Speichert Optionen, die dem angegebenen Socket zugeordnet sind.                                                                                                                                                    |
| [**Wspshutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))                       | Beendet einen Teil einer Vollduplex Verbindung.                                                                                                                                                            |
| [**Wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)                           | Eine socketerstellungs-Funktion, die eine [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur als Eingabe annimmt und ermöglicht, dass überlappende Sockets erstellt werden.                                                |
| [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)                         | Initialisiert den zugrunde liegenden Windows Sockets-Dienstanbieter.                                                                                                                                            |



 

 

 
