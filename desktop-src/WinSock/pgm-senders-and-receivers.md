---
description: Das Einrichten einer PGM-Sitzung ähnelt der Verbindungseinrichtungsroutine, die einer TCP-Sitzung zugeordnet ist.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: PGM-Absender und -Empfänger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559ac30ace4374b48c86efeb579e1426cc455b00adb803e97244a37d8df7fda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741067"
---
# <a name="pgm-senders-and-receivers"></a>PGM-Absender und -Empfänger

Das Einrichten einer PGM-Sitzung ähnelt der Verbindungseinrichtungsroutine, die einer TCP-Sitzung zugeordnet ist. Die wesentliche Abweichung von einer TCP-Sitzung besteht jedoch darin, dass die Client- und Serversemantik umgekehrt wird. Der Server (der PGM-Absender) stellt eine Verbindung mit einer Multicastgruppe her, während der Client (der PGM-Empfänger) auf die Annahme einer Verbindung wartet. In den folgenden Absätzen werden die programmgesteuerten Schritte beschrieben, die zum Erstellen eines PGM-Absenders und eines PGM-Empfängers erforderlich sind. Auf dieser Seite werden auch die verfügbaren Datenmodi für PGM-Sitzungen beschrieben.

## <a name="pgm-sender"></a>PGM-Absender

**Führen Sie die folgenden Schritte aus, um einen PGM-Absender zu erstellen.**

1.  Erstellen Sie einen PGM-Socket.
2.  [**Binden Sie**](/windows/desktop/api/winsock/nf-winsock-bind) den Socket an INADDR \_ ANY.
3.  [**Stellen Sie eine Verbindung mit**](/windows/desktop/api/Winsock2/nf-winsock2-connect) der Multicastgruppenübertragungsadresse her.

Für Clients wird kein formaler Sitzungshandshake ausgeführt. Der Verbindungsprozess ähnelt einer [**UDP-Verbindung,**](/windows/desktop/api/Winsock2/nf-winsock2-connect)da dem Socket eine Endpunktadresse (die Multicastgruppe) zugeordnet wird. Nach Abschluss des Abschlusses können Daten an den Socket gesendet werden.

Wenn ein Absender einen PGM-Socket erstellt und mit einer Multicastadresse verbindet, wird eine PGM-Sitzung erstellt. Eine zuverlässige Multicastsitzung wird durch eine Kombination aus GUID (Globally Unique Identifier) und Quellport definiert. Die GUID wird vom Transport generiert. Der sSource-Port wird vom Transport angegeben, und es wird keine Kontrolle darüber bereitgestellt, welcher Quellport verwendet wird.

> [!Note]  
> Das Empfangen von Daten auf einem Absendersocket ist nicht zulässig und führt zu einem Fehler.

 

Der folgende Codeausschnitt veranschaulicht das Einrichten eines PGM-Absenders:


```C++

SOCKET        s;
SOCKADDR_IN   salocal, sasession;
int           dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

salocal.sin_family = AF_INET;
salocal.sin_port   = htons (0);    // Port is ignored here
salocal.sin_addr.s_addr = htonl (INADDR_ANY);

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant sender socket options here
//

//
// Now, connect <entity type="hellip"/>
// Setting the connection port (dwSessionPort) has relevance, and
// can be used to multiplex multiple sessions to the same
// multicast group address over different ports
//
dwSessionPort = 0;
sasession.sin_family = AF_INET;
sasession.sin_port   = htons (dwSessionPort);
sasession.sin_addr.s_addr = inet_addr ("234.5.6.7");

connect (s, (SOCKADDR *)&sasession, sizeof(sasession));

//
// We're now ready to send data!
//



```



## <a name="pgm-receiver"></a>PGM-Empfänger

**Führen Sie die folgenden Schritte aus, um einen PGM-Empfänger zu erstellen.**

1.  Erstellen Sie einen PGM-Socket.
2.  [**Binden Sie**](/windows/desktop/api/winsock/nf-winsock-bind) den Socket an die Multicastgruppenadresse, an die der Absender übermittelt.
3.  Rufen Sie die [**Lauschenfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-listen) für den Socket auf, um den Socket in den Überwachungsmodus zu versetzen. Die listen-Funktion gibt zurück, wenn eine PGM-Sitzung an der angegebenen Multicastgruppenadresse und dem angegebenen Port erkannt wird.
4.  Rufen Sie die [**accept-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-accept) auf, um ein neues Sockethandle zu erhalten, das der Sitzung entspricht.

Nur ursprüngliche PGM-Daten (ODATA) lösen die Annahme einer neuen Sitzung aus. Daher kann anderer PGM-Datenverkehr (z. B. SPM- oder RDATA-Pakete) vom Transport empfangen werden, führt jedoch nicht dazu, dass die [**Lauschenfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-listen) zurückgibt.

Sobald eine Sitzung akzeptiert wird, wird das zurückgegebene Sockethandle zum Empfangen von Daten verwendet.

> [!Note]  
> Das Senden von Daten an einen Empfangssocket ist nicht zulässig und führt zu einem Fehler.

 

Der folgende Codeausschnitt veranschaulicht das Einrichten eines PGM-Empfängers:


```C++

SOCKET        s,
              sclient;
SOCKADDR_IN   salocal,
              sasession;
int           sasessionsz, dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

//
// The bind port (dwSessionPort) specified should match that
// which the sender specified in the connect call
//
dwSessionPort = 0;
salocal.sin_family = AF_INET;
salocal.sin_port   = htons (dwSessionPort);    
salocal.sin_addr.s_addr = inet_addr ("234.5.6.7");

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant receiver socket options here
//

listen (s, 10);

sasessionsz = sizeof(sasession);
sclient = accept (s, (SOCKADDR *)&sasession, &sasessionsz);

//
// accept will return the client socket and we are now ready
// to receive data on the new socket!
//



```



## <a name="data-modes"></a>Datenmodi

PGM-Sitzungen haben zwei Optionen für Datenmodi: Nachrichtenmodus und Streammodus.

Der Nachrichtenmodus eignet sich für Anwendungen, die diskrete Nachrichten senden müssen, und wird durch einen Sockettyp von SOCK \_ RDM angegeben. Der Streammodus eignet sich für Anwendungen, die Streamingdaten an Empfänger senden müssen, z. B. Video- oder Sprachanwendungen, und wird durch einen Sockettyp von SOCK \_ STREAM angegeben. Die Wahl des Modus wirkt sich darauf aus, wie Winsock Daten verarbeitet.

Betrachten Sie das folgende Beispiel: Ein PGM-Absender im Nachrichtenmodus führt drei Aufrufe an die [**WSASend-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) aus, die jeweils einen 100-Byte-Puffer haben. Dieser Vorgang wird als drei diskrete PGM-Pakete angezeigt. Auf empfängerseitiger Seite gibt jeder Aufruf der [**WSARecv-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) nur 100 Bytes zurück, auch wenn ein größerer Empfangspuffer bereitgestellt wird. Im Gegensatz dazu können diese drei 100-Byte-Übertragungen bei einem PGM-Sender im Streammodus in weniger als drei physische Pakete im Netzwerk zusammengeknüpft werden (oder in einem Datenblob auf empfängerseitiger Seite zusammengeführt). Wenn der Empfänger also eine der Windows Sockets-Empfangsfunktionen aufruft, kann jede Datenmenge, die vom PGM-Transport empfangen wurde, an die Anwendung zurückgegeben werden, unabhängig davon, wie die Daten physisch übertragen oder empfangen wurden.

 

 



