---
description: Ein unformatiertes Socket ist ein Sockettyp, der den Zugriff auf den zugrunde liegenden Transportanbieter ermöglicht.
ms.assetid: 4cbe5505-75e7-454f-9e6b-f38bdc60bf6d
title: UNFORMATIERTE TCP/IP-Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef8600c7b1a6c1bc5b2f7b5b210ca2d56f90069b0afce88c83ca45e9cfad8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733390"
---
# <a name="tcpip-raw-sockets"></a>UNFORMATIERTE TCP/IP-Sockets

Ein unformatiertes Socket ist ein Sockettyp, der den Zugriff auf den zugrunde liegenden Transportanbieter ermöglicht. In diesem Thema geht es nur um unformatierte Sockets und die Protokolle IPv4 und IPv6. Dies liegt daran, dass die meisten anderen Protokolle mit Ausnahme von ATM keine unformatierten Sockets unterstützen. Um rohe Sockets verwenden zu können, benötigt eine Anwendung ausführliche Informationen zum zugrunde liegenden Protokoll, das verwendet wird.

Winsock-Dienstanbieter für das IP-Protokoll unterstützen möglicherweise den *Sockettyp* **SOCK \_ RAW**. Der in Windows enthaltene Windows Sockets 2-Anbieter für TCP/IP unterstützt diesen **SOCK \_ RAW-Sockettyp.**

Es gibt zwei grundlegende Typen solcher unformatierten Sockets:

-   Der erste Typ verwendet einen bekannten Protokolltyp, der in den IP-Header geschrieben ist und von einem Winsock-Dienstanbieter erkannt wird. Ein Beispiel für den ersten Sockettyp ist ein Socket für das ICMP-Protokoll (IP-Protokolltyp = 1) oder das ICMPv6-Protokoll (IP-Procotol-Typ = 58).
-   Mit dem zweiten Typ kann ein beliebiger Protokolltyp angegeben werden. Ein Beispiel für den zweiten Typ wäre ein experimentelles Protokoll, das nicht direkt vom Winsock-Dienstanbieter wie dem Stream Control Transmission Protocol (SCTP) unterstützt wird.

## <a name="determining-if-raw-sockets-are-supported"></a>Bestimmen, ob Rohdatensockets unterstützt werden

Wenn ein Winsock-Dienstanbieter **SOCK \_ RAW-Sockets** für die AF \_ INET- oder AF \_ INET6-Adressfamilien unterstützt, sollte der **Sockettyp VON SOCK \_ RAW** in der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) enthalten sein, die von der [**WSAEnumProtocols-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) für einen oder mehrere der verfügbaren Transportanbieter zurückgegeben wird.

Das **iAddressFamily-Element** in der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) sollte AF \_ INET oder AF \_ INET6 angeben, und der **iSocketType-Member** der **WSAPROTOCOL \_ INFO-Struktur** sollte **SOCK \_ RAW** für einen der Transportanbieter angeben.

Der **iProtocol-Member** der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) kann auf **IPROTO \_ IP** festgelegt werden. Der **iProtocol-Member** der **WSAPROTOCOL \_ INFO-Struktur** kann auch auf 0 (null) festgelegt werden, wenn der Dienstanbieter einer Anwendung die Verwendung eines **SOCK RAW-Sockettyps \_** für andere Netzwerkprotokolle als das Internetprotokoll für die Adressfamilie erlaubt.

Die anderen Member in der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) geben andere Eigenschaften der Protokollunterstützung für **SOCK \_ RAW** an und geben an, wie ein Socket von **SOCK \_ RAW** behandelt werden soll. Diese anderen Member von **WSAPROTOCOL \_ INFO** für **SOCK \_ RAW** geben normalerweise an, dass das Protokoll verbindungslos und nachrichtenorientiert ist, Broadcast/Multicast unterstützt (die \_ MULTIPOINT-Bits XP1 CONNECTIONLESS, XP1 \_ MESSAGE \_ \_ \_ ORIENTED, XP1 SUPPORT BROADCAST und XP1 \_ SUPPORT sind im \_ DwServiceFlags1-Member festgelegt und können eine maximale Nachrichtengröße von 65.467 Bytes aufweisen.

Auf Windows XP und höher kann der *befehlNetSh.exe* verwendet werden, um zu bestimmen, ob Unformatierte Sockets unterstützt werden. Der folgende Befehl, der in einem CMD-Fenster ausgeführt wird, zeigt Daten aus dem Winsock-Katalog in der Konsole an:

**netsh winsock show catalog**

Die Ausgabe enthält eine Liste, die einige der Daten aus den [**WSAPROTOCOL \_ INFO-Strukturen**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) enthält, die auf dem lokalen Computer unterstützt werden. Suchen Sie im Feld Beschreibung nach dem Begriff RAW/IP oder RAW/IPv6, um die Protokolle zu finden, die Unformatierte Sockets unterstützen.

## <a name="creating-a-raw-socket"></a>Erstellen eines Unformatierten Sockets

Um einen Socket vom Typ **SOCK \_ RAW** zu erstellen, rufen Sie die [**Socket-**](/windows/desktop/api/Winsock2/nf-winsock2-socket) oder [**WSASocket-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) auf, wobei der *af-Parameter* (Adressfamilie) auf AF \_ INET oder AF \_ INET6, der *Typparameter* auf **SOCK \_ RAW** und der *Protokollparameter* auf die erforderliche Protokollnummer festgelegt ist. Der *-Protokollparameter* wird zum Protokollwert im IP-Header (SCTP ist z.B. 132).

> [!Note]  
> Eine Anwendung darf null (0) nicht als *Protokollparameter* für die [**Socket-,**](/windows/desktop/api/Winsock2/nf-winsock2-socket) [**WSASocket-**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)und [**WSPSocket-Funktionen**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) angeben, wenn der *Typparameter* auf **SOCK \_ RAW** festgelegt ist.

 

Unformatierte Sockets bieten die Möglichkeit, den zugrunde liegenden Transport zu manipulieren, sodass sie für böswillige Zwecke verwendet werden können, die eine Sicherheitsbedrohung darstellen. Daher können nur Mitglieder der Gruppe Administratoren Sockets vom Typ SOCK \_ RAW auf Windows 2000 und höher erstellen.

## <a name="send-and-receive-operations"></a>Sende- und Empfangsvorgänge

Nachdem eine Anwendung einen Socket vom Typ **SOCK \_ RAW** erstellt hat, kann dieser Socket zum Senden und Empfangen von Daten verwendet werden. Alle Pakete, die an einen Socket vom Typ **SOCK \_ RAW** gesendet oder empfangen werden, werden als Datagramme in einem nicht verbundenen Socket behandelt.

Die folgenden Regeln gelten für vorgänge über **SOCK \_ RAW-Sockets:**

-   Die [**sendto-**](/windows/desktop/api/winsock/nf-winsock-sendto) oder [**WSASendTo-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) wird normalerweise verwendet, um Daten an einen Socket vom Typ **SOCK \_ RAW** zu senden. Die Zieladresse kann eine beliebige gültige Adresse in der Adressfamilie des Sockets sein, einschließlich einer Broadcast- oder Multicastadresse. Zum Senden an eine Broadcastadresse muss eine Anwendung [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit aktivierter SO BROADCAST-Funktion verwendet \_ haben. Andernfalls schlägt **sendto** oder **WSASendTo** mit dem Fehlercode [WSAEACCES](windows-sockets-error-codes-2.md)fehl. Bei IP-Adressen kann eine Anwendung an eine beliebige Multicastadresse senden (ohne Mitglied einer Gruppe zu werden).
-   Beim Senden von IPv4-Daten hat eine Anwendung die Wahl, ob der IPv4-Header am Anfang des ausgehenden Datagramms für das Paket angegeben werden soll. Wenn die **\_ IP-HDRINCL-Socketoption** für einen IPv4-Socket (Adressfamilie von AF INET) auf TRUE festgelegt \_ ist, muss die Anwendung den IPv4-Header in den ausgehenden Daten für Sendevorgänge bereitstellen. Wenn diese Socketoption false ist (Standardeinstellung), sollte der IPv4-Header nicht in die ausgehenden Daten für Sendevorgänge eingeschlossen werden.
-   Beim Senden von IPv6-Daten hat eine Anwendung die Wahl, ob der IPv6-Header am Anfang des ausgehenden Datagramms für das Paket angegeben werden soll. Wenn die **IPV6 \_ HDRINCL-Socketoption** für einen IPv6-Socket (Adressfamilie von AF INET6) auf TRUE festgelegt \_ ist, muss die Anwendung den IPv6-Header in den ausgehenden Daten für Sendevorgänge bereitstellen. Die Standardeinstellung für diese Option ist FALSE. Wenn diese Socketoption false (Standardeinstellung) ist, sollte der IPv6-Header nicht in die ausgehenden Daten für Sendevorgänge eingeschlossen werden. Für IPv6 sollte der IPv6-Header nicht enthalten sein. Wenn Informationen mithilfe von Socketfunktionen verfügbar sind, sollte der IPv6-Header nicht enthalten sein, um Kompatibilitätsprobleme in Zukunft zu vermeiden. Diese Probleme werden in RFC 3542 erläutert, das von der IETF veröffentlicht wird. Die Verwendung der **\_ IPV6 HDRINCL-Socketoption** wird nicht empfohlen und ist in Zukunft möglicherweise veraltet.
-   Die [**recvfrom-**](/windows/desktop/api/winsock/nf-winsock-recvfrom) oder [**WSARecvFrom-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) wird normalerweise verwendet, um Daten in einem Socket vom Typ **SOCK \_ RAW** zu empfangen. Beide Funktionen haben die Möglichkeit, die Quell-IP-Adresse zurückzugeben, von der das Paket gesendet wurde. Die empfangenen Daten sind ein Datagramm von einem nicht verbundenen Socket.
-   Für IPv4 (Adressfamilie von AF \_ INET) empfängt eine Anwendung den IP-Header am Anfang jedes empfangenen Datagramms, unabhängig von der **\_ IP-HDRINCL-Socketoption.**
-   Für IPv6 (Adressfamilie von AF \_ INET6) empfängt eine Anwendung alles nach dem letzten IPv6-Header in jedem empfangenen Datagramm, unabhängig von der **IPV6 \_ HDRINCL-Socketoption.** Die Anwendung empfängt keine IPv6-Header, die einen unformatierten Socket verwenden.
-   Empfangene Datagramme werden in alle **SOCK \_ RAW-Sockets** kopiert, die die folgenden Bedingungen erfüllen:

    -   Die Protokollnummer, die beim Erstellen des Sockets im *Protokollparameter* angegeben wurde, sollte mit der Protokollnummer im IP-Header des empfangenen Datagramms übereinstimmen.
    -   Wenn eine lokale IP-Adresse für den Socket definiert ist, sollte sie der Zieladresse entsprechen, wie im IP-Header des empfangenen Datagramms angegeben. Eine Anwendung kann die lokale IP-Adresse angeben, indem sie die [**Bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) aufruft. Wenn keine lokale IP-Adresse für den Socket angegeben ist, werden die Datagramme unabhängig von der Ziel-IP-Adresse im IP-Header des empfangenen Datagramms in den Socket kopiert.
    -   Wenn eine Fremdadresse für den Socket definiert ist, sollte sie der Quelladresse entsprechen, wie im IP-Header des empfangenen Datagramms angegeben. Eine Anwendung kann die Fremd-IP-Adresse angeben, indem sie die [**Connect-**](/windows/desktop/api/Winsock2/nf-winsock2-connect) oder [**WSAConnect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) aufruft. Wenn keine Fremd-IP-Adresse für den Socket angegeben wird, werden die Datagramme unabhängig von der Quell-IP-Adresse im IP-Header des empfangenen Datagramms in den Socket kopiert.

Es ist wichtig zu verstehen, dass einige Sockets vom Typ **SOCK \_ RAW** viele unerwartete Datagramme erhalten können. Beispielsweise kann ein PING-Programm einen Socket vom Typ **SOCK \_ RAW** erstellen, um ICMP-Echoanforderungen zu senden und Antworten zu empfangen. Während die Anwendung ICMP-Echoantworten erwartet, können alle anderen ICMP-Nachrichten (z. B. ICMP HOST \_ UNREACHABLE) auch an diese Anwendung übermittelt werden. Wenn außerdem mehrere **SOCK \_ RAW-Sockets** gleichzeitig auf einem Computer geöffnet sind, können die gleichen Datagramme an alle offenen Sockets übermittelt werden. Eine Anwendung muss über einen Mechanismus verfügen, um die für Sie interessanten Datagramme zu erkennen und alle anderen zu ignorieren. Bei einem PING-Programm kann ein solcher Mechanismus die Überprüfung des empfangenen IP-Headers auf eindeutige Bezeichner im ICMP-Header (z. B. die Prozess-ID der Anwendung) umfassen.

> [!Note]  
> Für die Verwendung eines Sockets vom Typ **SOCK \_ RAW** sind Administratorrechte erforderlich. Benutzer, die Winsock-Anwendungen ausführen, die unformatierte Sockets verwenden, müssen Mitglied der Gruppe "Administratoren" auf dem lokalen Computer sein. Andernfalls schlagen Unformatierte Socketaufrufe mit dem Fehlercode [WSAEACCES](windows-sockets-error-codes-2.md)fehl. Auf Windows Vista und höher wird der Zugriff für Unformatierte Sockets bei der Socketerstellung erzwungen. In früheren Versionen von Windows wird der Zugriff für Unformatierte Sockets während anderer Socketvorgänge erzwungen.

 

## <a name="common-uses-of-raw-sockets"></a>Häufige Verwendungsmöglichkeiten von Rohsockets

Eine häufige Verwendung von Unformatierungssockets ist die Problembehandlung von Anwendungen, die IP-Pakete und -Header im Detail untersuchen müssen. Beispielsweise kann ein unformatiertes Socket mit dem SIO RCVALL IOCTL verwendet werden, \_ damit ein Socket alle IPv4- oder IPv6-Pakete empfangen kann, die über eine Netzwerkschnittstelle übergeben werden. Weitere Informationen finden Sie in der [**SIO \_ RCVALL-Referenz.**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85))

## <a name="limitations-on-raw-sockets"></a>Einschränkungen für Unformatierte Sockets

Auf Windows 7, Windows Vista, Windows XP mit Service Pack 2 (SP2) und Windows XP mit Service Pack 3 (SP3) wurde die Möglichkeit zum Senden von Datenverkehr über Unformatierte Sockets auf verschiedene Weise eingeschränkt:

-   TCP-Daten können nicht über Unformatierte Sockets gesendet werden.
-   UDP-Datagramme mit einer ungültigen Quelladresse können nicht über Unformatierte Sockets gesendet werden. Die IP-Quelladresse für alle ausgehenden UDP-Datagramme muss auf einer Netzwerkschnittstelle vorhanden sein, oder das Datagramm wird gelöscht. Diese Änderung wurde vorgenommen, um die Fähigkeit von schädlichem Code zum Erstellen verteilter Denial-of-Service-Angriffe einzuschränken und die Möglichkeit zum Senden von gefälschten Paketen (TCP/IP-Pakete mit einer gefälschten Quell-IP-Adresse) einzuschränken.
-   Ein Aufruf der [**Bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) mit einem unformatierten Socket für das IPPROTO-TCP-Protokoll \_ ist nicht zulässig.
    > [!Note]  
    > Die [**Bindungsfunktion**](/windows/desktop/api/winsock/nf-winsock-bind) mit einem unformatierten Socket ist für andere Protokolle zulässig \_ (z.B. IPPROTO IP, IPPROTO \_ UDP oder IPPROTO \_ SCTP).

     

Diese oben genannten Einschränkungen gelten nicht für Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 oder für Versionen des Betriebssystems vor Windows XP mit SP2.

> [!Note]  
> Die Microsoft-Implementierung von TCP/IP auf Windows kann einen unformatierten UDP- oder TCP-Socket basierend auf den oben genannten Einschränkungen öffnen. Andere Winsock-Anbieter unterstützen die Verwendung von Rohsockets möglicherweise nicht.

 

Es gibt weitere Einschränkungen für Anwendungen, die einen Socket vom Typ **SOCK \_ RAW** verwenden. Beispielsweise empfangen alle Anwendungen, die auf ein bestimmtes Protokoll lauschen, alle Pakete, die für dieses Protokoll empfangen wurden. Dies ist möglicherweise nicht das gewünschte Ergebnis für mehrere Anwendungen, die ein Protokoll verwenden. Dies ist auch nicht für Hochleistungsanwendungen geeignet. Um diese Probleme zu umgehen, ist es möglicherweise erforderlich, einen Windows Netzwerkprotokolltreiber (Gerätetreiber) für das spezifische Netzwerkprotokoll zu schreiben. Auf Windows Vista und höher, Winsock Kernel (WSK), kann eine neue transportunabhängige Kernelmodus-Netzwerkprogrammierschnittstelle verwendet werden, um einen Netzwerkprotokolltreiber zu schreiben. Auf Windows Server 2003 und früheren Versionen können ein Transport Driver Interface-Anbieter (TDI) und eine Winsock-Hilfs-DLL geschrieben werden, um das Netzwerkprotokoll zu unterstützen. Das Netzwerkprotokoll wird dann dem Winsock-Katalog als unterstütztes Protokoll hinzugefügt. Dadurch können mehrere Anwendungen Sockets für dieses spezifische Protokoll öffnen, und der Gerätetreiber kann nachverfolgen, welcher Socket bestimmte Pakete und Fehler empfängt. Informationen zum Schreiben eines Netzwerkprotokollanbieters finden Sie in den Abschnitten zu WSK und TDI im Windows Driver Kit (WDK).

Anwendungen müssen auch die Auswirkungen beachten, die Firewalleinstellungen auf das Senden und Empfangen von Paketen mit unformatiert Sockets haben können.

 

 
