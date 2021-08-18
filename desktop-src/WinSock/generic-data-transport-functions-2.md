---
description: Die Datentransportfunktionen, die von Ws2spi.h verfügbar gemacht werden.
ms.assetid: 6900faa3-79bb-4ed8-b83e-148eb10425a0
title: Generische Datentransportfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d13b067713fe6a2600d6667ebe7eac058c5fcae87fc5bfd14311b3a263b862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132353"
---
# <a name="generic-data-transport-functions"></a>Generische Datentransportfunktionen

In diesem Abschnitt werden die Datentransportfunktionen aufgelistet, die von Ws2spi.h verfügbar gemacht werden.



| Funktion                                                   | Beschreibung                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)                           | Eine eingehende Verbindung wird bestätigt und einem sofort erstellten Socket zugeordnet. Der ursprüngliche Socket wird in den Überwachungszustand zurückgegeben. Diese Funktion ermöglicht auch die bedingte Akzeptanz. |
| [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))                 | Führt eine asynchrone Version von [**WSPSelect aus.**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                                                                                                                                      |
| [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))                               | Weist einem unbenannten Socket einen lokalen Namen zu.                                                                                                                                                              |
| [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85))   | Bricht einen ausstehenden blockierenden Windows Sockets-Aufruf ab.                                                                                                                                                   |
| [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))                         | Meldet sich vom zugrunde liegenden Windows Sockets-Dienstanbieter ab.                                                                                                                                         |
| [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                 | Entfernt einen Socket aus der Pro-Prozess-Objektverweistabelle. Blockiert nur, wenn SO \_ LINGER mit einem Time out ungleich 0 (null) für einen blockierenden Socket festgelegt ist.                                                            |
| [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                         | Initiiert eine Verbindung für den angegebenen Socket. Diese Funktion ermöglicht auch den Austausch von Verbindungsdaten und QoS-Spezifikationen.                                                                           |
| [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85))         | Gibt eine [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) zurück, die zum Erstellen eines neuen Socketdeskriptors für einen freigegebenen Socket verwendet werden kann.                                                             |
| [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85))     | Ermittelt Vorkommen von Netzwerkereignissen.                                                                                                                                                                |
| [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))                 | Ordnet Einem Ereignisobjekt Netzwerkereignisse zu.                                                                                                                                                         |
| [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) | Ruft den Abschlussstatus eines überlappende Vorgangs ab.                                                                                                                                                         |
| [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85))                 | Ruft den Namen des Peers ab, der mit dem angegebenen Socket verbunden ist.                                                                                                                                       |
| [**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85))                 | Ruft die lokale Adresse ab, an die der angegebene Socket gebunden ist.                                                                                                                                     |
| [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))                   | Ruft optionen ab, die dem angegebenen Socket zugeordnet sind.                                                                                                                                                 |
| [**WSPGetQOSByName**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetqosbyname)               | Stellt QoS-Parameter basierend auf einem bekannten Dienstnamen zur Verfügung.                                                                                                                                             |
| [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))                             | Stellt die Steuerung für Sockets bereit.                                                                                                                                                                           |
| [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)                       | Verbindet einen Blattknoten mit einer Multipointsitzung.                                                                                                                                                            |
| [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))                           | Lauscht auf eingehende Verbindungen an einem angegebenen Socket.                                                                                                                                                 |
| [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))                               | Empfängt Daten von einem verbundenen oder nicht verbundenen Socket. Diese Funktion unterstützt Punkt-/Erfassungs-E/A, überlappende Sockets und stellt den Flags-Parameter als IN/OUT bereit.                                    |
| [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85))           | Beendet den Empfang für einen Socket und ruft die Daten ab, wenn der Socket verbindungsorientiert ist.                                                                                                |
| [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))                       | Empfängt Daten von einem verbundenen oder nicht verbundenen Socket. Diese Funktion unterstützt Punkt-/Erfassungs-E/A, überlappende Sockets und stellt den Flags-Parameter als IN/OUT bereit.                              |
| [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                           | Führt synchrones E/A-Multiplexing aus.                                                                                                                                                                  |
| [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))                               | Sendet Daten an einen verbundenen Socket. Diese Funktion unterstützt auch Punkt-/Erfassungs-E/A und überlappende Sockets.                                                                                            |
| [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))           | Initiiert das Beenden einer Socketverbindung und optional das Senden von Daten zum Trennen der Verbindung.                                                                                                                       |
| [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                           | Sendet Daten an einen verbundenen oder nicht verbundenen Socket. Diese Funktion unterstützt auch Punkt-/Erfassungs-E/A und überlappende Sockets.                                                                      |
| [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))                   | Speichert Optionen, die dem angegebenen Socket zugeordnet sind.                                                                                                                                                    |
| [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))                       | Beendet einen Teil einer Vollduplexverbindung.                                                                                                                                                            |
| [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)                           | Eine Socketerstellungsfunktion, die eine [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) als Eingabe annimmt und das Erstellen überlappender Sockets ermöglicht.                                                |
| [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)                         | Initialisiert den zugrunde liegenden Windows Sockets-Dienstanbieter.                                                                                                                                            |



 

 

 
