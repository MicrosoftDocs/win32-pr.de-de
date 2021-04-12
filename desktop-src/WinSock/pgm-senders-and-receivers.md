---
description: Das Einrichten einer PGM-Sitzung ähnelt der Verbindung, die mit einer TCP-Sitzung verknüpft ist.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: PGM-Absender und-Empfänger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e300a0c9de199e1f836e71407caf6487812cf7b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526120"
---
# <a name="pgm-senders-and-receivers"></a>PGM-Absender und-Empfänger

Das Einrichten einer PGM-Sitzung ähnelt der Verbindung, die mit einer TCP-Sitzung verknüpft ist. Der bedeutende Abbruch von einer TCP-Sitzung ist jedoch, dass die Client-und Server Semantik umgekehrt ist. der Server (der PGM-Sender) stellt eine Verbindung mit einer Multicast Gruppe her, während der Client (der PGM-Empfänger) darauf wartet, eine Verbindung zu akzeptieren. In den folgenden Abschnitten werden die programmgesteuerten Schritte erläutert, die zum Erstellen eines PGM-Senders und eines PGM-Empfängers erforderlich sind Auf dieser Seite werden auch die verfügbaren Daten Modi für PGM-Sitzungen beschrieben.

## <a name="pgm-sender"></a>PGM-Absender

**Führen Sie die folgenden Schritte aus, um einen PGM-Sender zu erstellen:**

1.  Erstellen Sie einen PGM-Socket.
2.  [**binden**](/windows/desktop/api/winsock/nf-winsock-bind) Sie den Socket an inaddr \_ any.
3.  Stellen Sie eine [**Verbindung**](/windows/desktop/api/Winsock2/nf-winsock2-connect) mit der Multicast Gruppen-Übertragungs Adresse her.

Es werden keine formellen Sitzungs Handler für Clients ausgeführt. Der Verbindungsprozess ähnelt einer UDP- [**Verbindung**](/windows/desktop/api/Winsock2/nf-winsock2-connect), da er eine Endpunkt Adresse (die Multicast Gruppe) dem Socket zuordnet. Nach Abschluss des Vorgangs können Daten auf dem Socket gesendet werden.

Wenn ein Absender einen PGM-Socket erstellt und ihn mit einer Multicast Adresse verbindet, wird eine PGM-Sitzung erstellt. Eine zuverlässige Multicast Sitzung wird durch eine Kombination aus dem Globally Unique Identifier (GUID) und dem Quellport definiert. Die GUID wird vom Transport generiert. Der sSource-Port wird vom Transport festgelegt, und es wird kein Steuerelement bereitgestellt, über den der Quellport verwendet wird.

> [!Note]  
> Das Empfangen von Daten auf einem Absender Socket ist nicht zulässig und führt zu einem Fehler.

 

Der folgende Code Ausschnitt veranschaulicht das Einrichten eines PGM-Senders:


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
2.  [**binden**](/windows/desktop/api/winsock/nf-winsock-bind) Sie den Socket an die Multicast Gruppen Adresse, über die der Absender überträgt.
3.  Ruft die Funktion " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) " im Socket auf, um den Socket in den Empfangsmodus zu versetzen. Die Funktion "lauschen" gibt zurück, wenn eine PGM-Sitzung für die angegebene Multicast Gruppen Adresse und den Port erkannt wird.
4.  Rufen Sie die [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) -Funktion auf, um ein neues Sockethandle zu erhalten, das der Sitzung entspricht.

Nur ursprüngliche PGM-Daten (odata) lösen die Annahme einer neuen Sitzung aus. Daher kann ein anderer PGM-Datenverkehr (z. b. SPM-oder rdata-Pakete) vom Transport empfangen werden, dies führt jedoch nicht dazu, dass die Funktion " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) " zurückgibt.

Nachdem eine Sitzung akzeptiert wurde, wird das zurückgegebene Sockethandle zum Empfangen von Daten verwendet.

> [!Note]  
> Das Senden von Daten in einem Empfangs Socket ist nicht zulässig und führt zu einem Fehler.

 

Der folgende Code Ausschnitt veranschaulicht das Einrichten eines PGM-Empfängers:


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



## <a name="data-modes"></a>Daten Modi

PGM-Sitzungen verfügen über zwei Optionen für Daten Modi: Nachrichten Modus und Streammodus.

Der Nachrichten Modus ist für Anwendungen geeignet, die diskrete Nachrichten senden müssen, und wird durch den Sockettyp Sock \_ RDM angegeben. Der Streammodus eignet sich für Anwendungen, die Streamingdaten an Empfänger (z. b. Video-oder Sprachanwendungen) senden müssen, und die durch einen Sockettyp von Sock Stream angegeben werden \_ . Die Auswahl des Modus hat Auswirkungen auf die Verarbeitung von Daten durch Winsock.

Sehen Sie sich das folgende Beispiel an: ein PGM-Absender im Nachrichten Modus führt drei Aufrufe an die [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) -Funktion mit jeweils einem 100-Byte-Puffer aus. Dieser Vorgang wird im Netzwerk als drei diskrete PGM-Pakete angezeigt. Auf der Empfängerseite gibt jeder Aufrufe der [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) -Funktion nur 100 Bytes zurück, auch wenn ein größerer Empfangs Puffer bereitgestellt wird. Im Gegensatz dazu können bei einem PGM-Absender im Streammodus diese 3 100-Byte-Übertragungen in weniger als drei physische Pakete übertragen werden (oder in ein BLOB von Daten auf der Empfängerseite zusammen geschrieben werden). Wenn der Empfänger z. b. eine der Windows Sockets-Empfangsfunktionen aufruft, kann jede Menge von Daten, die vom PGM-Transport empfangen wurde, an die Anwendung zurückgegeben werden, ohne dass dabei berücksichtigt wird, wie die Daten physisch übertragen oder empfangen werden.

 

 



