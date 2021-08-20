---
description: In der folgenden Tabelle werden die IPPROTO-TCP-Socketoptionen beschrieben, die für Sockets gelten, die für die \_ IPv4- und IPv6-Adressfamilien (AF INET und AF INET6) mit dem Protokollparameter für die als \_ \_ TCP (IPPROTO TCP) angegebene Socketfunktion erstellt \_ wurden.
ms.assetid: 2a10498d-0a0b-4a2d-941e-9aa45a1a4428
title: IPPROTO_TCP-Socketoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153f3bdf2cbfa3cbdbc50214722c62b4ad2f75d65136f2f7370b73bdfa3bfc1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927578"
---
# <a name="ipproto_tcp-socket-options"></a>\_IPPROTO-TCP-Socketoptionen

In der folgenden Tabelle werden **die IPPROTO-TCP-Socketoptionen \_** beschrieben, die für Sockets gelten, die für die IPv4- und IPv6-Adressfamilien (AF INET und AF INET6) mit dem Protokollparameter für die als \_ TCP \_ (IPPROTO TCP)  [](/windows/desktop/api/Winsock2/nf-winsock2-socket) angegebene Socketfunktion erstellt \_ wurden. Weitere Informationen zum Abrufen und Festlegen von Socketoptionen finden Sie auf den Referenzseiten der [**getsockopt-**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt-Funktion.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Um Protokolle aufzählen und unterstützte Eigenschaften für jedes installierte Protokoll zu finden, verwenden Sie die [**WSAEnumProtocols-,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols-**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)oder [**WSCEnumProtocols32-Funktion.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

## <a name="options"></a>Optionen

<table>
<colgroup>
<col/>
<col/>
<col/>
<col/>
<col/>
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Herunterladen</th>
<th>Set</th>
<th>Optval-Typ</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr>
<td>TCP_BSDURGENT</td>
<td>Ja</td>
<td>Ja</td>
<td>DWORD (boolean)</td>
<td>True <strong>gibt</strong>an, dass der Dienstanbieter den BSD-Stil (California Software Distribution) (Standard) für die Verarbeitung beschleunigter Daten implementiert. Diese Option ist die Umkehrung der TCP_EXPEDITED_1122 Option. Diese Option kann für die Verbindung nur einmal festgelegt werden. Sobald diese Option aktiviert ist, kann diese Option nicht mehr deaktiviert werden. Diese Option muss nicht von Dienstanbietern implementiert werden. Die Option ist standardmäßig aktiviert (auf <strong>TRUE</strong>festgelegt).</td>
</tr>
<tr>
<td>TCP_EXPEDITED_1122</td>
<td>Ja</td>
<td>Ja</td>
<td>DWORD (boolean)</td>
<td>True <strong>gibt</strong>an, dass der Dienstanbieter die beschleunigten Daten gemäß RFC-1222 implementiert. Andernfalls wird der BSD-Stil (California Software Distribution, Softwareverteilung) (Standard) verwendet. Diese Option kann für die Verbindung nur einmal festgelegt werden. Sobald diese Option aktiviert ist, kann diese Option nicht mehr deaktiviert werden. Diese Option muss nicht von Dienstanbietern implementiert werden.</td>
</tr>
<tr>
<td>TCP_FAIL_CONNECT_ON_ICMP_ERROR</td>
<td>Ja</td>
<td>Ja</td>
<td>DWORD (boolean)</td>
<td>True <strong>gibt einen</strong>Connect-API-Aufruf zurück, wenn ein ICMP-Fehler mit dem Wert WSAEHOSTUNREACH empfangen wird. Die Quelladresse des Fehlers ist dann über die Socketoption TCP_ICMP_ERROR_INFO verfügbar. False <strong>gibt an,</strong>dass sich der Socket normal verhält. Der Standardwert ist deaktiviert (auf <strong>FALSE festgelegt).</strong> Zur Typsicherheit sollten Sie die <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror">Funktionen WSAGetFailConnectOnIcmpError</a> und <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror">WSASetFailConnectOnIcmpError</a> verwenden, anstatt die Socketoption direkt zu verwenden.</td>
</tr>
<tr>
<td>TCP_ICMP_ERROR_INFO</td>
<td>Ja</td>
<td>Nein</td>
<td><a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a></td>
<td>Ruft die Informationen zu einem ICMP-Fehler ab, der vom TCP-Socket während eines fehlerhaften Verbindungsaufrufs empfangen wurde. Nur gültig für einen TCP-Socket, TCP_FAIL_CONNECT_ON_ICMP_ERROR zuvor aktiviert wurde und <strong>connect</strong> WSAEHOSTUNREACH zurückgegeben hat. Die Abfrage ist nicht blockierend. Wenn die Abfrage erfolgreich war und der zurückgegebene optlen-Wert 0 ist, wurde seit dem letzten Verbindungsaufruf kein ICMP-Fehler empfangen. Wenn ein ICMP-Fehler empfangen wurde, sind seine Informationen verfügbar, bis <strong>die Verbindung</strong> erneut aufgerufen wird. Die Informationen werden als <a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a> zurückgegeben. Zur Typsicherheit sollten Sie die <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo">WSAGetIcmpErrorInfo-Funktion</a> verwenden, anstatt die Socketoption direkt zu verwenden.</td>
</tr>
<tr>
<td>TCP_KEEPCNT</td>
<td>Ja</td>
<td>Ja</td>
<td>DWORD</td>
<td>Ruft die Anzahl der TCP-Keep-Alive-Tests ab, die gesendet werden, bevor die Verbindung beendet wird, oder legt diese fest. Es ist unzulässig, TCP_KEEPCNT auf einen Wert größer als 255 zu setzen.</td>
</tr>
<tr>
<td>TCP_MAXRT</td>
<td>Ja</td>
<td>Ja</td>
<td>DWORD</td>
<td>Wenn dieser Wert nicht negativ ist, stellt er das gewünschte Verbindungs-Timeout in Sekunden dar. Wenn er -1 ist, stellt er eine Anforderung zum Deaktivieren des Verbindungszeitüberschreitungs dar (d. h., die Verbindung wird für immer neu übertragen). Wenn das Verbindungs-Timeout deaktiviert ist, erhöht sich das Timeout für die Neuübertragung für jede Neuübertragung exponentiell bis zu seinem maximalen Wert von 60 s und bleibt dort.</td>
</tr>
<tr>
<td>TCP_NODELAY</td>
<td>Ja</td>
<td>Ja</td>
<td>DWORD (boolean)</td>
<td>Aktiviert oder deaktiviert den Nagle-Algorithmus für TCP-Sockets. Diese Option ist standardmäßig deaktiviert (auf FALSE festgelegt).</td>
</tr>
<tr>
<td>TCP_TIMESTAMPS</td>
<td>Ja</td>
<td>Ja</td>
<td>DWORD (boolean)</td>
<td>Aktiviert oder deaktiviert RFC 1323-Zeitstempel. Beachten Sie, dass es auch eine globale Konfiguration für Zeitstempel (Standardwert ist deaktiviert) und &quot; Zeitstempel &quot; in (set/get)-nettcpsetting gibt. Wenn Sie diese Socketoption festlegen, wird diese globale Konfigurationseinstellung überschrieben.</td>
</tr>
<tr>
<td>TCP_FASTOPEN</td>
<td>Ja</td>
<td>Ja</td>
<td>DWORD (boolean)</td>
<td>Aktiviert oder deaktiviert <a href="https://tools.ietf.org/html/rfc7413">RFC 7413</a> TCP Fast Open, wodurch Sie während der Drei-Wege-Handshakephase beim Öffnen einer Verbindung mit dem Senden von Daten beginnen können. Beachten Sie, dass Sie <a href="/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex"><strong>connectEx</strong></a> verwenden sollten, um die erste Verbindung herzustellen und Daten im <em>lpSendBuffer-Parameter</em> dieser Funktion anzugeben, die während des Handshakeprozesses übertragen werden sollen, um schnelles Öffnen zu verwenden. Einige der Daten in <em>lpSendBuffer</em> werden unter dem Fast Open-Protokoll übertragen.</td>
</tr>
<tr>
<td>TCP_KEEPIDLE</td>
<td>Ja</td>
<td>Ja</td>
<td>DWORD</td>
<td>Ruft die Anzahl der Sekunden ab, die eine TCP-Verbindung im Leerlauf verbleibt, bevor Keepalive-Tests an die Remoteverbindung gesendet werden, oder legt diese fest.
<blockquote>
[!Note]<br />
Diese Option ist ab Windows 10 Version 1709 verfügbar.
</blockquote>
<br/></td>
</tr>
<tr>
<td>TCP_KEEPINTVL</td>
<td>Ja</td>
<td>Ja</td>
<td>DWORD</td>
<td>Ruft die Anzahl der Sekunden ab, die eine TCP-Verbindung auf eine Keepalive-Antwort wartet, bevor ein weiterer Keepalive-Test gesendet wird, oder legt diese fest.
<blockquote>
[!Note]<br />
Diese Option ist ab Windows 10 Version 1709 verfügbar.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>

## <a name="windows-support-for-ipproto_tcp-options"></a>Windows für \_ IPPROTO-TCP-Optionen

| Option | Windows 10 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|
| \_TCP-BSD WRAPPENT | x | x | x | x |
| TCP \_ EXPEDITED \_ 1122 | x | x | x | x |
| TCP \_ KEEPCNT | Ab Windows 10 Version 1703 | | | |
| TCP \_ MAXRT | x | x | x | x |
| TCP \_ NODELAY | x | x | x | x |
| \_TCP-ZEITSTEMPEL | x | x | x | x |
| TCP \_ FASTOPEN | Ab Windows 10 Version 1607 | | | |

<br/>

 | Option | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-|-|-|-|-|-|
| \_TCP-BSD WRAPPENT | x | x | x | x | |
| TCP \_ EXPEDITED \_ 1122 | x | x | x | | |
| TCP \_ KEEPCNT | | | | | |
| TCP \_ MAXRT | | | | | |
| TCP \_ NODELAY | x | x | x | x | |
| \_TCP-ZEITSTEMPEL | | | | | |
| TCP \_ FASTOPEN | | | | | |

## <a name="remarks"></a>Hinweise

Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Headerdateien geändert, und die **\_ IPPROTO-TCP-Ebene** wird in der *Headerdatei Ws2def.h* definiert, die automatisch in der *Winsock2.h-Headerdatei* enthalten ist. Die **IPPROTO-TCP-Socketoptionen, \_** mit Ausnahme von **TCP \_ BSD ADRENT,** werden in der *Headerdatei Ws2ipdef.h* definiert, die automatisch in der *Headerdatei Ws2tcpip.h* enthalten ist. Die **\_ TCP-Option BSD AUS** historischen Gründen wird in der *Headerdatei "Mswsock.h"* definiert. Die *Headerdateien "Ws2def.h"* und *"Ws2ipdef.h"* sollten nie direkt verwendet werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | <dl> <dt>Ws2def.h (einschließlich Winsock2.h);</dt> <dt>Winsock2.h auf Windows Server 2003, Windows XP und Windows 2000</dt> </dl> |
