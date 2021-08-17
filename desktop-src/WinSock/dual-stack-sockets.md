---
description: 'Um sowohl IPv4 als auch IPv6 auf Windows XP mit Service Pack 1 (SP1) und auf Windows Server 2003 zu unterstützen, muss eine Anwendung zwei Sockets erstellen: einen Socket für die Verwendung mit IPv4 und einen Socket für die Verwendung mit IPv6.'
ms.assetid: 7ae49081-ffb5-4eee-b488-2541398e7acc
title: Dual-Stack Sockets für IPv6-Winsockanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424580569fb3bed5e81c6232cb99dc2d53a30af1ab2c23c9b4afa6945c0a6eb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132663"
---
# <a name="dual-stack-sockets-for-ipv6-winsock-applications"></a>Dual-Stack Sockets für IPv6-Winsockanwendungen

Um sowohl IPv4 als auch IPv6 auf Windows XP mit Service Pack 1 (SP1) und auf Windows Server 2003 zu unterstützen, muss eine Anwendung zwei Sockets erstellen: einen Socket für die Verwendung mit IPv4 und einen Socket für die Verwendung mit IPv6. Diese beiden Sockets müssen von der Anwendung separat behandelt werden.

Windows Vista und höher bieten die Möglichkeit, einen einzelnen IPv6-Socket zu erstellen, der sowohl IPv6- als auch IPv4-Datenverkehr verarbeiten kann. Beispielsweise wird ein TCP-Lauschendocket für IPv6 erstellt, in den Dual Stack-Modus versetzt und an Port 5001 gebunden. Dieser Dual Stack-Socket kann Verbindungen von IPv6-TCP-Clients akzeptieren, die eine Verbindung mit Port 5001 herstellen, und von IPv4-TCP-Clients, die eine Verbindung mit Port 5001 herstellen. Dieses Feature ermöglicht einen erheblich vereinfachten Anwendungsentwurf und reduziert den Ressourcenaufwand, der für das Bereitstellen von Vorgängen an zwei separaten Sockets erforderlich ist.

## <a name="creating-a-dual-stack-socket"></a>Erstellen eines Dual-Stack Sockets

Standardmäßig wird ein IPv6-Socket, der auf Windows Vista und höher erstellt wurde, nur über das IPv6-Protokoll betrieben. Um einen IPv6-Socket in einen Doppelstapelsocket zu verwandeln, muss die [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit der **IPV6 \_ V6ONLY-Socketoption** aufgerufen werden, um diesen Wert auf 0 festzulegen, bevor der Socket an eine IP-Adresse gebunden wird. Wenn die **IpV6 \_ V6ONLY-Socketoption** auf 0 (null) festgelegt ist, kann ein für die **AF \_ INET6-Adressfamilie** erstellter Socket verwendet werden, um Pakete an eine IPv6-Adresse oder eine IPv4-zugeordnete Adresse zu senden und zu empfangen.

## <a name="ip-addresses-with-a-dual-stack-socket"></a>IP-Adressen mit einem Dual-Stack Socket

Dual-Stack-Sockets erfordern immer IPv6-Adressen. Für die Interaktion mit einer IPv4-Adresse muss das IPv4-zugeordnete IPv6-Adressformat verwendet werden. Alle IPv4-Adressen müssen im IPv4-zugeordneten IPv6-Adressformat dargestellt werden, wodurch eine IPv6-Anwendung nur mit einem IPv4-Knoten kommunizieren kann. Das IPv4-zugeordnete IPv6-Adressformat ermöglicht die Darstellung der IPv4-Adresse eines IPv4-Knotens als IPv6-Adresse. Die IPv4-Adresse wird in die 32 Bits der IPv6-Adresse mit niedriger Ordnung codiert, und die 96 Bits mit hoher Ordnung enthalten das feste Präfix 0:0:0:0:0:FFFF. Das IPv4-zugeordnete IPv6-Adressformat wird in RFC 4291 angegeben. Weitere Informationen finden Sie unter [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). Das IN6ADDR \_ SETV4MAPPED-Makro in *Mstcpip.h* kann verwendet werden, um eine IPv4-Adresse in das erforderliche IPv4-zugeordnete IPv6-Adressformat zu konvertieren.

Wenn das zugrunde liegende Protokoll tatsächlich IPv4 ist, wird die IPv4-Adresse einem IPv4-zugeordneten IPv6-Adressformat zugeordnet. Das heißt, das Familienfeld in der [SOCKADDR-Struktur](sockaddr-2.md) gibt AF \_ INET6 an, aber eine IPv4-zugeordnete IPv6-Adresse wird in der IPv6-Adressstruktur codiert. Für einen Dual-Stack-Socket im Überwachungsmodus bedeutet dies, dass alle akzeptierten IPv4-Verbindungen eine IPv4-zugeordnete IPv6-Adresse zurückgeben. Bei einem Dual-Stack-Socket, der eine Verbindung mit einem IPv4-Ziel herstellt, muss die sockaddr-Struktur, die für die Verbindung übergeben wird, eine IPv4-zugeordnete IPv6-Adresse sein. Anwendungen müssen darauf achten, diese IPv4-zugeordneten IPv6-Adressen angemessen zu behandeln und nur mit dualen Stapelsockets zu verwenden. Wenn eine IP-Adresse an einen regulären IPv4-Socket übergeben werden soll, muss es sich bei der Adresse um eine reguläre IPv4-Adresse und nicht um eine IPv4-zugeordnete IPv6-Adresse handelt.

## <a name="potential-issues-using-a-dual-stack-socket"></a>Potenzielle Probleme bei der Verwendung eines Dual-Stack Sockets

Ein potenzieller Fehler für Anwendungen besteht darin, eine IPv4-zugeordnete IPv6-Adresse auf einem Dual-Stack-Socket zu erhalten und dann zu versuchen, die zurückgegebene IP-Adresse auf einem anderen IPv6-Socket zu verwenden. Beispielsweise können die Funktionen [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) oder [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) eine IPv4-zugeordnete IPv6-Adresse zurückgeben, wenn sie auf einem Dual-Stack-Socket verwendet werden. Wenn die zurückgegebene IPv4-zugeordnete IPv6-Adresse anschließend auf einem anderen Socket verwendet wird, der nicht auf dualen Stapel festgelegt wurde (ein IPv6-Socket, der beim Erstellen eines Sockets das Standardverhalten darstellt), schlägt jede Verwendung dieses IPv6-Sockets mit einer IPv4-zugeordneten IPv6-Adresse fehl. Das IPv4-zugeordnete IPv6-Adressformat kann nur für einen Doppelstapelsocket verwendet werden.

Wenn eine Anwendung für einen Dual-Stack-Datagrammsocket die [**funktion LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) zum Zurückgeben von Paketinformationen in einer [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) für über IPv4 empfangene Datagramme benötigt, muss die [ \_ IP-PKTINFO-Socketoption](ip-pktinfo.md) für den Socket auf TRUE festgelegt werden. Wenn nur die [ \_ IPV6 PKTINFO-Option](ipv6-pktinfo.md) für den Socket auf TRUE festgelegt ist, werden Paketinformationen für Datagramme bereitgestellt, die über IPv6 empfangen werden, aber möglicherweise nicht für Datagramme, die über IPv4 empfangen werden.

Wenn eine Anwendung versucht, die [ \_ IP-PKTINFO-Socketoption](ip-pktinfo.md) für einen Dual-Stack-Datagrammsocket festzulegen, und IPv4 auf dem System deaktiviert ist, schlägt die [**Setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) fehl, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt den Fehler [WSAEINVAL](windows-sockets-error-codes-2.md)zurück. Dieser Fehler wird auch von der **setsockopt-Funktion** als Ergebnis anderer Fehler zurückgegeben. Wenn eine Anwendung versucht, eine \_ IPPROTO-Socketoption auf IP-Ebene für einen Socket mit zwei Stapeln festzulegen, und ein Fehler mit [WSAEINVAL](windows-sockets-error-codes-2.md)auftritt, sollte die Anwendung bestimmen, ob IPv4 auf dem lokalen Computer deaktiviert ist. Eine Methode, mit der ermittelt werden kann, ob IPv4 aktiviert oder deaktiviert ist, ist das Aufrufen der [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) mit *dem* af-Parameter, der auf AF INET festgelegt \_ ist, um zu versuchen, einen IPv4-Socket zu erstellen. Wenn die **Socketfunktion** fehlschlägt und **WSAGetLastError** den Fehler [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md)zurückgibt, bedeutet dies, dass IPv4 nicht aktiviert ist. In diesem Fall kann ein **Setsockopt-Funktionsfehler** beim Festlegen der IP-PKTINFO-Socketoption \_ von der Anwendung ignoriert werden. Andernfalls sollte ein Fehler beim Festlegen der \_ IP-PKTINFO-Socketoption als unerwarteter Fehler behandelt werden.

Bei einem Dual-Stack-Socket beim Senden von Datagrammen mit der [**WSASendMsg-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) und einer Anwendung, die eine bestimmte lokale IP-Quelladresse angeben möchte, hängt die Methode zur Behandlung dieser Daten von der Ziel-IP-Adresse ab. Beim Senden an eine IPv4-Zieladresse oder eine IPv4-zugeordnete IPv6-Zieladresse sollte eines der Steuerdatenobjekte, die in der [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) übergeben werden, auf die der *lpMsg-Parameter* zeigt, eine [**in \_ pktinfo-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) enthalten, die die lokale IPv4-Quelladresse enthält, die zum Senden verwendet werden soll. Beim Senden an eine IPv6-Zieladresse, bei der es sich nicht um eine IPv4-zugeordnete IPv6-Adresse handelt, sollte eines der Steuerelementdatenobjekte, die in der **WSAMSG-Struktur** übergeben werden, auf die der *lpMsg-Parameter* zeigt, eine [**in6 \_ pktinfo-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) enthalten, die die lokale IPv6-Quelladresse enthält, die zum Senden verwendet werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Leitfaden für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Ändern von Datenstrukturen für IPv6-Winsock-Appications](changing-data-structures-2.md)
</dt> <dt>

[Funktionsaufrufe für IPv6-Winsock-Anwendungen](function-calls-2.md)
</dt> <dt>

[Verwenden von hartcodierten IPv4-Adressen](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Benutzeroberfläche Probleme bei IPv6-Winsock-Anwendungen](user-interface-issues-2.md)
</dt> <dt>

[Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen](underlying-protocols-2.md)
</dt> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname)
</dt> <dt>

[**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[IP \_ PKTINFO](ip-pktinfo.md)
</dt> <dt>

[IPV6 \_ PKTINFO](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> <dt>

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
</dt> </dl>

 

 
