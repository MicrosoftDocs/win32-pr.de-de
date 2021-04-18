---
description: Um sowohl IPv4 als auch IPv6 unter Windows XP mit Service Pack 1 (SP1) und Windows Server 2003 zu unterstützen, muss eine Anwendung zwei Sockets erstellen, einen Socket für die Verwendung mit IPv4 und einen Socket für die Verwendung mit IPv6.
ms.assetid: 7ae49081-ffb5-4eee-b488-2541398e7acc
title: Dual-Stack Sockets für IPv6-Winsock-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943d8150586bcf14a905ab32dcacaea63b7d6982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347170"
---
# <a name="dual-stack-sockets-for-ipv6-winsock-applications"></a>Dual-Stack Sockets für IPv6-Winsock-Anwendungen

Um sowohl IPv4 als auch IPv6 unter Windows XP mit Service Pack 1 (SP1) und Windows Server 2003 zu unterstützen, muss eine Anwendung zwei Sockets erstellen, einen Socket für die Verwendung mit IPv4 und einen Socket für die Verwendung mit IPv6. Diese beiden Sockets müssen separat von der Anwendung behandelt werden.

Windows Vista und höher bieten die Möglichkeit, einen einzelnen IPv6-Socket zu erstellen, der sowohl IPv6-als auch IPv4-Datenverkehr verarbeiten kann. Beispielsweise wird ein TCP-lausch-Socket für IPv6 erstellt, in den Dual Stack-Modus versetzt und an Port 5001 gebunden. Dieser Dual-Stack-Socket kann Verbindungen von IPv6-TCP-Clients akzeptieren, die Verbindungen mit Port 5001 herstellen, sowie IPv4-TCP-Clients, die eine Verbindung mit 5001 Port Diese Funktion ermöglicht einen stark vereinfachten Anwendungs Entwurf und reduziert den Ressourcen Aufwand, der für die Bereitstellung von Vorgängen auf zwei separaten Sockets erforderlich ist.

## <a name="creating-a-dual-stack-socket"></a>Erstellen eines Dual-Stack Sockets

Standardmäßig funktioniert ein IPv6-Socket, der unter Windows Vista und höher erstellt wurde, nur über das IPv6-Protokoll. Um einen IPv6-Socket in einem Dual-Stack-Socket zu erstellen, muss die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion mit der **IPv6- \_ V6ONLY** -Socketoption aufgerufen werden, um diesen Wert auf 0 (null) festzulegen, bevor der Socket an eine IP-Adresse gebunden wird. Wenn die **IPv6 \_ V6ONLY** Socket-Option auf 0 (null) festgelegt ist, kann ein für die **AF \_ inet6** Address-Familie erstellter Socket zum Senden und empfangen von Paketen an eine oder von einer IPv6-Adresse oder einer zugeordneten IPv4-Adresse verwendet werden.

## <a name="ip-addresses-with-a-dual-stack-socket"></a>IP-Adressen mit einem Dual-Stack Socket

Dual-Stack-Sockets erfordern immer IPv6-Adressen. Die Möglichkeit der Interaktion mit einer IPv4-Adresse erfordert die Verwendung des IPv4-zugeordneten IPv6-Adress Formats. Alle IPv4-Adressen müssen im IPv4-zugeordneten IPv6-Adressformat dargestellt werden, das einer reinen IPv6-Anwendung die Kommunikation mit einem IPv4-Knoten ermöglicht. Das IPv4-zugeordnete IPv6-Adressformat ermöglicht die Darstellung der IPv4-Adresse eines IPv4-Knotens als IPv6-Adresse. Die IPv4-Adresse wird in die 32 Bits der IPv6-Adresse mit niedriger Reihenfolge codiert, und die höherwertigen 96 Bits enthalten das feste Präfix 0:0: 0:0: 0: FFFF. Das IPv4-zugeordnete IPv6-Adressformat wird in RFC 4291 angegeben. Weitere Informationen finden Sie unter [www.ietf.org/RFC/rfc4291.txt](https://tools.ietf.org/html/rfc4291). Das IN6ADDR \_ SETV4MAPPED-Makro in *MSTCPIP. h* kann verwendet werden, um eine IPv4-Adresse in das erforderliche IPv4-zugeordnete IPv6-Adressformat zu konvertieren.

Wenn das zugrunde liegende Protokoll tatsächlich IPv4 ist, wird die IPv4-Adresse einem IPv4-zugeordneten IPv6-Adressformat zugeordnet. Das heißt, das Familien Feld in der [sockaddr](sockaddr-2.md) -Struktur zeigt AF \_ inet6 an, aber eine IPv4-zugeordnete IPv6-Adresse wird in der IPv6-Adressstruktur codiert. Bei einem Dual-Stack-Socket im Empfangsmodus bedeutet dies, dass alle akzeptierten IPv4-Verbindungen eine IPv4-zugeordnete IPv6-Adresse zurückgeben. Bei einem Dual-Stack-Socket, der eine Verbindung mit einem IPv4-Ziel herstellt, muss die an Connect über gegebene sockaddr-Struktur eine IPv4-zugeordnete IPv6-Adresse sein. Anwendungen müssen diese IPv4-zugeordneten IPv6-Adressen entsprechend verarbeiten und nur mit Dual Stack Sockets verwenden. Wenn eine IP-Adresse an einen regulären IPv4-Socket übermittelt werden soll, muss die Adresse eine reguläre IPv4-Adresse und keine IPv4-zugeordnete IPv6-Adresse sein.

## <a name="potential-issues-using-a-dual-stack-socket"></a>Mögliche Probleme bei der Verwendung eines Dual-Stack Sockets

Ein potenzieller Fall für Anwendungen besteht darin, eine IPv4-zugeordnete IPv6-Adresse in einem Dual-Stack-Socket zu erhalten und dann zu versuchen, die zurückgegebene IP-Adresse in einem anderen reinen IPv6-Socket zu verwenden. Beispielsweise kann die Funktionen [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) oder [**getPeer Name**](/windows/desktop/api/winsock/nf-winsock-getpeername) eine IPv4-zugeordnete IPv6-Adresse zurückgeben, wenn Sie in einem Dual-Stack-Socket verwendet wird. Wenn die zurückgegebene IPv4-zugeordnete IPv6-Adresse anschließend in einem anderen Socket verwendet wird, der nicht auf Dual-Stack festgelegt wurde (ein reines IPv6-Socket, das beim Erstellen eines Sockets das Standardverhalten ist), schlägt die Verwendung dieses reinen IPv6-Sockets mit einer IPv4-zugeordneten IPv6-Adresse fehl. Das IPv4-zugeordnete IPv6-Adressformat kann nur in einem Dual-Stack-Socket verwendet werden.

Wenn in einem Dual-Stack-Datagramm-Socket eine Anwendung erfordert, dass die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion Paketinformationen in einer [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur für über IPv4 Empfangene Datagramme zurückgibt, muss die [IP \_ pktinfo-](ip-pktinfo.md) Socketoption für den Socket auf true festgelegt werden. Wenn nur die [IPv6- \_ pktinfo](ipv6-pktinfo.md) -Option im Socket auf true festgelegt ist, werden Paketinformationen für über IPv6 Empfangene Datagramme bereitgestellt, jedoch nicht für Datagramme, die über IPv4 empfangen werden.

Wenn eine Anwendung versucht, die [IP- \_ pktinfo-](ip-pktinfo.md) Socketoption auf einem Dual-Stack-Datagramm-Socket festzulegen, und IPv4 auf dem System deaktiviert ist, schlägt die Funktion " [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) " fehl, und " [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) " wird mit dem Fehler " [WSAEINVAL](windows-sockets-error-codes-2.md)" zurückgegeben. Dieser Fehler wird auch durch die Funktion " **setsockopt** " aufgrund anderer Fehler zurückgegeben. Wenn eine Anwendung versucht, eine \_ Socketoption auf ipproto-IP-Ebene in einem Dual-Stack-Socket festzulegen, und Sie mit [WSAEINVAL](windows-sockets-error-codes-2.md)fehlschlägt, sollte die Anwendung ermitteln, ob IPv4 auf dem lokalen Computer deaktiviert ist. Eine Methode, die verwendet werden kann, um zu ermitteln, ob IPv4 aktiviert oder deaktiviert ist, besteht darin, die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) mit dem auf AF inet festgelegten *AF* -Parameter aufzurufen, \_ um einen IPv4-Socket zu erstellen. Wenn die **Socketfunktion** ausfällt und **WSAGetLastError** einen Fehler von [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md)zurückgibt, bedeutet dies, dass IPv4 nicht aktiviert ist. In diesem Fall kann ein **setsockopt** -Funktionsfehler auftreten, wenn versucht wird, die IP \_ pktinfo-Socketoption festzulegen, kann die Anwendung ignoriert werden. Andernfalls sollte bei dem Versuch, die \_ Socketoption IP pktinfo festzulegen, ein unerwarteter Fehler behandelt werden.

Bei einem Dual-Stack-Socket beim Senden von Datagrammen mit der [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Funktion und einer Anwendung, die eine bestimmte lokale IP-Quelladresse für die Verwendung angeben möchte, hängt die Methode, die diese behandelt, von der Ziel-IP-Adresse ab. Beim Senden an eine IPv4-Zieladresse oder an eine IPv4-zugeordnete IPv6-Zieladresse sollte eines der Steuerungsdaten Objekte, das in der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur übergeben wird, auf die durch den *lpmsg* -Parameter verwiesen wird, eine [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) -Struktur mit der lokalen IPv4-Quelladresse enthalten, die zum Senden verwendet wird. Beim Senden an eine IPv6-Zieladresse, die keine IPv4-zugeordnete IPv6-Adresse ist, sollte eines der Steuerungsdaten Objekte, das in der **wsamsg** -Struktur, auf die durch den *lpmsg* -Parameter verwiesen wird, eine [**IN6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) -Struktur mit der lokalen IPv6-Quelladresse enthalten, die zum Senden verwendet werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Handbuch für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Ändern von Datenstrukturen für IPv6-Winsock-Appications](changing-data-structures-2.md)
</dt> <dt>

[Funktionsaufrufe für IPv6-Winsock-Anwendungen](function-calls-2.md)
</dt> <dt>

[Verwendung von hart codierten IPv4-Adressen](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Probleme mit der Benutzeroberfläche für IPv6-Winsock-Anwendungen](user-interface-issues-2.md)
</dt> <dt>

[Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen](underlying-protocols-2.md)
</dt> <dt>

[**getPeer Name**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname)
</dt> <dt>

[**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**IN6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[IP- \_ pktinfo](ip-pktinfo.md)
</dt> <dt>

[IPv6- \_ pktinfo](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> <dt>

[**Wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
</dt> </dl>

 

 
