---
description: Ein unformatierte Socket ist ein Typ von Socket, der den Zugriff auf den zugrunde liegenden Transportanbieter ermöglicht.
ms.assetid: 4cbe5505-75e7-454f-9e6b-f38bdc60bf6d
title: TCP/IP-Rohdaten Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25cc08d59d80089a4e655f363e4a899edac8d2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345880"
---
# <a name="tcpip-raw-sockets"></a>TCP/IP-Rohdaten Sockets

Ein unformatierte Socket ist ein Typ von Socket, der den Zugriff auf den zugrunde liegenden Transportanbieter ermöglicht. In diesem Thema geht es nur um RAW-Sockets und IPv4-und IPv6-Protokolle. Dies liegt daran, dass die meisten anderen Protokolle mit Ausnahme von ATM keine Rohdaten Sockets unterstützen. Um Unformatierte Sockets zu verwenden, benötigt eine Anwendung ausführliche Informationen über das zugrunde liegende Protokoll, das verwendet wird.

Winsock-Dienstanbieter für das IP-Protokoll unterstützen möglicherweise einen *Sockettyp* von **Sock- \_ RAW**. Der in Windows enthaltene Windows Sockets 2-Anbieter für TCP/IP unterstützt diesen Sockettyp mit **\_ socketrohdaten** .

Es gibt zwei grundlegende Arten von rohsockets:

-   Der erste Typ verwendet einen bekannten Protokolltyp, der im IP-Header geschrieben ist, der von einem Winsock-Dienstanbieter erkannt wird. Ein Beispiel für den ersten Sockettyp ist ein Socket für das ICMP-Protokoll (IP-Protokolltyp = 1) oder das ICMPv6-Protokoll (IP Procotol Type = 58).
-   Der zweite Typ ermöglicht das Angeben eines beliebigen Protokoll Typs. Ein Beispiel für den zweiten Typ wäre ein experimentelles Protokoll, das nicht direkt vom Winsock-Dienstanbieter, wie z. b. dem Stream Control Transmission Protocol (SCTP), unterstützt wird.

## <a name="determining-if-raw-sockets-are-supported"></a>Ermitteln, ob RAW-Sockets unterstützt werden

Wenn ein Winsock-Dienstanbieter **Sock- \_ RAW** -Sockets für die AF- \_ oder AF \_ inet6-Adressfamilien unterstützt, sollte der socketyp von **Sock \_ RAW** in der von der [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) -Funktion für einen oder mehrere der verfügbaren Transportanbieter zurückgegebenen [**\_ wsaenumprotokolle**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) -Struktur enthalten sein.

Der Member " **iaddressfamily** " in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur sollte "AF inet" oder "AF inet6" angeben, \_ \_ und der Member " **isockettype** " der **wsaprotocol- \_ Informations** Struktur sollte " **Sock \_ RAW** " für einen der Transportanbieter angeben.

Der **iProtocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur kann auf **iproto \_ IP** festgelegt werden. Der **iProtocol** -Member der **wsaprotocol- \_ Informations** Struktur kann auch auf 0 (null) festgelegt werden, wenn der Dienstanbieter es einer Anwendung ermöglicht, einen Socket- **\_ rohsocketyp** für andere Netzwerkprotokolle als das Internet Protokoll für die Adressfamilie zu verwenden.

Die anderen Elemente in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur geben andere Eigenschaften der Protokoll Unterstützung für **Sock \_ RAW** an und geben an, wie ein Socket von **Sock- \_ RAW** behandelt werden soll. Diese anderen **Member der wsaprotocol- \_ Informationen** für **Sock \_ RAW** geben normalerweise an, dass das Protokoll verbindungslose und Nachrichten orientiert ist, unterstützt Broadcast/Multicast (die XP1 \_ Connectionless, XP1 \_ Message \_ Oriented, XP1 \_ Support \_ Broadcast und XP1 \_ Support \_ Multipoint Bits werden im dwServiceFlags1-Member festgelegt) und kann eine maximale Nachrichtengröße von 65.467 Bytes aufweisen.

Unter Windows XP und höher kann der *NetSh.exe* -Befehl verwendet werden, um zu bestimmen, ob RAW-Sockets unterstützt werden. Der folgende Befehl, der in einem cmd-Fenster ausgeführt wird, zeigt Daten aus dem Winsock-Katalog auf der Konsole an:

**netsh Winsock Show Catalog**

Die Ausgabe enthält eine Liste mit einigen der Daten aus den [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Strukturen, die auf dem lokalen Computer unterstützt werden. Suchen Sie im Feld Beschreibung nach dem Begriff Raw/IP oder RAW/IPv6, um die Protokolle zu suchen, die unformatierte Sockets unterstützen.

## <a name="creating-a-raw-socket"></a>Erstellen eines RAW-Sockets

Um einen Socket des Typs **Sock \_ RAW** zu erstellen, rufen Sie die [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -oder [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) -Funktion mit dem *AF* -Parameter (Adressfamilie) auf, der auf AF \_ inet oder AF inet6 festgelegt ist, und legen Sie den Parameter "Type" auf " \_ **Sock \_ RAW**" und  den *Protokoll* Parameter auf die erforderliche Protokollnummer fest Der *Protokoll* Parameter wird zum Protokoll Wert im IP-Header (z. b. SCTP ist 132).

> [!Note]  
> Eine Anwendung darf nicht NULL (0) als *Protokoll* Parameter für die Funktionen [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket), [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)und [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) angeben, wenn der *Typparameter* auf **Sock \_ RAW** festgelegt ist.

 

Rohsockets bieten die Möglichkeit, den zugrunde liegenden Transport zu manipulieren, sodass Sie für schädliche Zwecke verwendet werden können, die eine Sicherheitsbedrohung darstellen. Daher können nur Mitglieder der Gruppe "Administratoren" Sockets vom Typ "Sock \_ RAW" unter Windows 2000 und höher erstellen.

## <a name="send-and-receive-operations"></a>Sende-und Empfangs Vorgänge

Sobald eine Anwendung einen Socket vom Typ **Sock \_ RAW** erstellt, kann dieser Socket zum Senden und empfangen von Daten verwendet werden. Alle an einen Socket vom Typ " **Sock \_ RAW** " gesendeten oder empfangenen Pakete werden als Datagramme auf einem nicht verbundenen Socket behandelt.

Die folgenden Regeln gelten für die Vorgänge über **\_ socketrohsockets** :

-   Die [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) -oder [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) -Funktion wird normalerweise zum Senden von Daten an einen Socket vom Typ " **Sock \_ RAW**" verwendet. Die Zieladresse kann eine beliebige gültige Adresse in der Adressfamilie des Sockets sein, einschließlich einer Broadcast-oder Multicast Adresse. Damit eine Anwendung an eine Broadcast Adresse gesendet werden kann, muss [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit \_ aktiviertem Broadcast verwendet werden. Andernfalls schlägt ' **SendTo** ' oder ' **WSASendTo** ' mit dem Fehlercode ' [WSAEACCES](windows-sockets-error-codes-2.md)' fehl. Bei IP kann eine Anwendung an eine beliebige Multicast Adresse (ohne Gruppenmitglied) senden.
-   Beim Senden von IPv4-Daten kann eine Anwendung entscheiden, ob der IPv4-Header an der Vorderseite des ausgehenden Datagramms für das Paket angegeben werden soll. Wenn die Option **IP \_ hdrincl** Socket für einen IPv4-Socket (Adressfamilie von AF inet) auf true festgelegt ist \_ , muss die Anwendung den IPv4-Header in den ausgehenden Daten für Sende Vorgänge bereitstellen. Wenn diese Socketoption auf false festgelegt ist (Standardeinstellung), sollte der IPv4-Header nicht in den ausgehenden Daten für Sende Vorgänge enthalten sein.
-   Beim Senden von IPv6-Daten kann eine Anwendung auswählen, ob der IPv6-Header an der Vorderseite des ausgehenden Datagramms für das Paket angegeben werden soll. Wenn die **IPv6- \_ hdrincl** -Socketoption für einen IPv6-Socket (Adressfamilie von AF inet6) auf true festgelegt ist \_ , muss die Anwendung den IPv6-Header in den ausgehenden Daten für Sende Vorgänge bereitstellen. Die Standardeinstellung für diese Option ist false. Wenn diese Socketoption auf false festgelegt ist (Standardeinstellung), sollte der IPv6-Header nicht in den ausgehenden Daten für Sende Vorgänge enthalten sein. Für IPv6 sollte es nicht erforderlich sein, den IPv6-Header einzuschließen. Wenn Informationen mithilfe von Socketfunktionen verfügbar sind, sollte der IPv6-Header nicht eingeschlossen werden, um in Zukunft Kompatibilitätsprobleme zu vermeiden. Diese Probleme werden in RFC 3542 erläutert, die vom IETF veröffentlicht werden. Die Verwendung der **IPv6- \_ hdrincl** -Socketoption wird nicht empfohlen und ist in Zukunft möglicherweise veraltet.
-   Die Funktion " [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) " oder " [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) " wird normalerweise verwendet, um Daten für einen Socket vom Typ " **Sock \_ RAW**" zu empfangen. Beide Funktionen verfügen über eine Option zum Zurückgeben der Quell-IP-Adresse, von der das Paket gesendet wurde. Die empfangenen Daten sind ein Datagramm von einem nicht verbundenen Socket.
-   Für IPv4 (Adressfamilie von AF \_ inet) empfängt eine Anwendung unabhängig von der **IP \_ hdrincl-** Socketoption den IP-Header an der Vorderseite jedes empfangenen Datagramms.
-   Für IPv6 (Adressfamilie von AF \_ inet6) empfängt eine Anwendung alle Elemente, die sich nach dem letzten IPv6-Header in jedem empfangenen Datagramm befinden, unabhängig von der **IPv6- \_ hdrincl** -Socketoption. Die Anwendung empfängt keine IPv6-Header mithilfe eines RAW-Sockets.
-   Empfangene Datagramme werden in alle **\_ socketrohsockets** kopiert, die die folgenden Bedingungen erfüllen:

    -   Die im *Protokoll* Parameter angegebene Protokollnummer, als der Socket erstellt wurde, sollte der Protokollnummer im IP-Header des empfangenen Datagramms entsprechen.
    -   Wenn eine lokale IP-Adresse für den Socket definiert ist, sollte Sie der Zieladresse entsprechen, wie im IP-Header des empfangenen Datagramms angegeben. Eine Anwendung kann die lokale IP-Adresse durch Aufrufen der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion angeben. Wenn für den Socket keine lokale IP-Adresse angegeben ist, werden die Datagramme unabhängig von der Ziel-IP-Adresse im IP-Header des empfangenen Datagramms in das Socket kopiert.
    -   Wenn eine fremd Adresse für den Socket definiert ist, sollte Sie der Quelladresse entsprechen, wie im IP-Header des empfangenen Datagramms angegeben. Eine Anwendung kann die fremde IP-Adresse durch Aufrufen der [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) -oder [**wsaconnetct**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) -Funktion angeben. Wenn für den Socket keine fremde IP-Adresse angegeben wird, werden die Datagramme unabhängig von der Quell-IP-Adresse im IP-Header des empfangenen Datagramms in das Socket kopiert.

Es ist wichtig zu verstehen, dass einige Sockets des Typs **Sock \_ RAW** viele unerwartete Datagramme erhalten. Beispielsweise kann ein Ping-Programm einen Socket vom Typ " **Sock \_ RAW** " erstellen, um ICMP-Echo Anforderungen zu senden und Antworten zu empfangen. Obwohl die Anwendung ICMP-Echo Antworten erwartet, können alle anderen ICMP-Nachrichten (z. b. der ICMP-Host \_ nicht erreichbar) auch an diese Anwendung übermittelt werden. Wenn darüber hinaus mehrere **\_ socketrohsockets** gleichzeitig auf einem Computer geöffnet sind, werden möglicherweise dieselben Datagramme an alle geöffneten Sockets übermittelt. Eine Anwendung muss über einen Mechanismus verfügen, um die von Interesse betroffenen Datagramme zu erkennen und alle anderen zu ignorieren. Bei einem Ping-Programm kann ein solcher Mechanismus die Überprüfung des empfangenen IP-Headers auf eindeutige Bezeichner im ICMP-Header (z. b. die Prozess-ID der Anwendung) beinhalten.

> [!Note]  
> Um einen Socket des Typs " **Sock \_ RAW** " verwenden zu können, sind Administratorrechte erforderlich. Benutzer, die Winsock-Anwendungen ausführen, die unformatierte Sockets verwenden, müssen ein Mitglied der Gruppe "Administratoren" auf dem lokalen Computer sein. andernfalls schlagen unformatierte Socket-Aufrufe mit dem Fehlercode " [WSAEACCES](windows-sockets-error-codes-2.md)" fehl. Unter Windows Vista und höher wird der Zugriff für RAW-Sockets bei der Socket-Erstellung erzwungen. In früheren Versionen von Windows wird der Zugriff auf unformatierte Sockets bei anderen Socketvorgängen erzwungen.

 

## <a name="common-uses-of-raw-sockets"></a>Häufige Verwendungsmöglichkeiten von rohsockets

Eine häufige Verwendung von rohsockets ist die Problembehandlung bei Anwendungen, bei denen IP-Pakete und Header ausführlich untersucht werden müssen. Beispielsweise kann ein RAW-Socket mit der "sio \_ rcvall"-IOCTL verwendet werden, damit ein Socket alle IPv4-oder IPv6-Pakete empfangen kann, die über eine Netzwerkschnittstelle übergeben werden. Weitere Informationen finden Sie in der Referenz zu " [**SIO \_ rcvall**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) ".

## <a name="limitations-on-raw-sockets"></a>Einschränkungen bei rohsockets

Unter Windows 7, Windows Vista, Windows XP mit Service Pack 2 (SP2) und Windows XP mit Service Pack 3 (SP3) wurde die Möglichkeit zum Senden von Datenverkehr über Raw Sockets auf verschiedene Weise eingeschränkt:

-   TCP-Daten können nicht über Unformatierte Sockets gesendet werden.
-   UDP-Datagramme mit einer ungültigen Quelladresse können nicht über Unformatierte Sockets gesendet werden. Die IP-Quelladresse für alle ausgehenden UDP-Datagramm muss in einer Netzwerkschnittstelle vorhanden sein, oder das Datagramm wird gelöscht. Diese Änderung wurde vorgenommen, um die Fähigkeit von schädlichem Code zum Erstellen verteilter Denial-of-Service-Angriffe einzuschränken und die Möglichkeit einzuschränken, gefälschte Pakete (TCP/IP-Pakete mit einer gefälschten Quell-IP-Adresse) zu senden.
-   Ein Aufrufe der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion mit einem unformatierten Socket für das ipproto \_ TCP-Protokoll ist nicht zulässig.
    > [!Note]  
    > Die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion mit einem RAW-Socket ist beispielsweise für andere Protokolle zulässig ( \_ z. b. ipproto IP, ipproto \_ UDP oder ipproto \_ SCTP).

     

Diese Einschränkungen gelten nicht für Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 oder Versionen des Betriebssystems vor Windows XP mit SP2.

> [!Note]  
> Die Microsoft-Implementierung von TCP/IP unter Windows ist in der Lage, einen unformatierten UDP-oder TCP-Socket basierend auf den oben genannten Einschränkungen zu öffnen. Andere Winsock-Anbieter unterstützen möglicherweise nicht die Verwendung von rohsockets.

 

Für Anwendungen, die einen Socket vom Typ " **Sock \_ RAW**" verwenden, gibt es weitere Einschränkungen. Beispielsweise erhalten alle Anwendungen, die ein bestimmtes Protokoll überwachen, alle Pakete, die für dieses Protokoll empfangen werden. Dies ist möglicherweise nicht das, was für mehrere Anwendungen mit einem Protokoll gewünscht ist. Dies ist auch für Hochleistungsanwendungen nicht geeignet. Um diese Probleme zu umgehen, kann es erforderlich sein, einen Windows-Netzwerkprotokoll Treiber (Gerätetreiber) für das jeweilige Netzwerkprotokoll zu schreiben. Unter Windows Vista und höher, Winsock Kernel (WSK), kann eine neue Transport unabhängige kernelmodusschnittstelle zum Schreiben eines Netzwerkprotokoll Treibers verwendet werden. Unter Windows Server 2003 und früheren Versionen können ein Transport Driver Interface (TDI)-Anbieter und eine Winsock Helper-DLL geschrieben werden, um das Netzwerkprotokoll zu unterstützen. Das Netzwerkprotokoll wird dann dem Winsock-Katalog als unterstütztes Protokoll hinzugefügt. Dadurch können mehrere Anwendungen Sockets für dieses bestimmte Protokoll öffnen, und der Gerätetreiber kann verfolgen, welcher Socket bestimmte Pakete und Fehler empfängt. Weitere Informationen zum Schreiben eines Netzwerkprotokoll Anbieters finden Sie in den Abschnitten zu WSK und TDI im Windows-Treiberkit (WDK).

Anwendungen müssen auch wissen, welche Auswirkungen Firewalleinstellungen auf das Senden und empfangen von Paketen mithilfe von rohsockets haben können.

 

 
