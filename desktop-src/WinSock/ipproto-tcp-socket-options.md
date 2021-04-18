---
description: In der folgenden Tabelle werden die ipproto \_ TCP-Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4-und IPv6-Adressfamilien (AF \_ inet und AF inet6) erstellt wurden, \_ mit dem Protokoll Parameter für die als TCP (ipproto TCP) angegebene Socketfunktion \_ .
ms.assetid: 2a10498d-0a0b-4a2d-941e-9aa45a1a4428
title: IPPROTO_TCP-Socketoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d261a639c10faa8c8ef52ba1ae88a0fbc52a16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364914"
---
# <a name="ipproto_tcp-socket-options"></a>Ipproto \_ TCP-Socketoptionen

In der folgenden Tabelle werden die **ipproto \_ TCP** -Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4-und IPv6-Adressfamilien (AF \_ inet und AF inet6) erstellt wurden, \_ mit dem *Protokoll* Parameter für die als TCP (ipproto TCP) angegebene [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) \_ . Weitere Informationen zum Ermitteln und Festlegen von Socketoptionen finden Sie auf den Referenzseiten zu den Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .

Verwenden Sie die [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)-, [**wscenumprotokolle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)-oder [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) -Funktion, um Protokolle aufzulisten und die unterstützten Eigenschaften für jedes installierte Protokoll zu ermitteln.

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
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr>
<td>TCP_BSDURGENT</td>
<td>ja</td>
<td>ja</td>
<td>DWORD (Boolean)</td>
<td><strong>True</strong>gibt an, dass der Dienstanbieter den Stil der Berkeley Software Distribution (BSD) für die Verarbeitung von beschleunigten Daten implementiert (Standard). Diese Option ist die Umkehrung der Option TCP_EXPEDITED_1122. Diese Option kann nur einmal für die Verbindung festgelegt werden. Wenn diese Option auf ON festgelegt ist, kann diese Option nicht deaktiviert werden. Diese Option muss nicht von Dienstanbietern implementiert werden. Die Option ist standardmäßig aktiviert (auf <strong>true</strong>festgelegt).</td>
</tr>
<tr>
<td>TCP_EXPEDITED_1122</td>
<td>ja</td>
<td>ja</td>
<td>DWORD (Boolean)</td>
<td><strong>True</strong>gibt an, dass der Dienstanbieter die beschleunigten Daten wie in RFC-1222 angegeben implementiert. Andernfalls wird der Stil der Berkeley Software Distribution (BSD) (Standardeinstellung) verwendet. Diese Option kann nur einmal für die Verbindung festgelegt werden. Wenn diese Option auf ON festgelegt ist, kann diese Option nicht deaktiviert werden. Diese Option muss nicht von Dienstanbietern implementiert werden.</td>
</tr>
<tr>
<td>TCP_FAIL_CONNECT_ON_ICMP_ERROR</td>
<td>ja</td>
<td>ja</td>
<td>DWORD (Boolean)</td>
<td><strong>True</strong>gibt an, dass ein Connect-API-Rückruf beim Empfang eines ICMP-Fehlers mit dem Wert "wsaehostunreach" zurückgegeben wird. Die Quelladresse des Fehlers steht dann über die TCP_ICMP_ERROR_INFO Socket-Option zur Verfügung. <strong>False</strong>gibt an, dass sich der Socket normal verhält. Der Standardwert ist deaktiviert (auf <strong>false</strong>festgelegt). Für Typsicherheit sollten Sie die Funktionen <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror">wsagetfailconnectoncmperror</a> und <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror">wsasetfailconnectoncmperror</a> verwenden, anstatt die Socketoption direkt zu verwenden.</td>
</tr>
<tr>
<td>TCP_ICMP_ERROR_INFO</td>
<td>ja</td>
<td>nein</td>
<td><a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a></td>
<td>Ruft die Informationen eines ICMP-Fehlers ab, der während eines fehlgeschlagenen Connect-Aufrufes vom TCP-Socket empfangen wurde. Nur gültig an einem TCP-Socket, bei dem bereits TCP_FAIL_CONNECT_ON_ICMP_ERROR aktiviert wurde und die <strong>Verbindung</strong> "wsaehostunreach" zurückgegeben hat. Die Abfrage ist nicht blockierend. Wenn die Abfrage erfolgreich ausgeführt wurde und der zurückgegebene optlen-Wert 0 ist, wurde seit dem letzten Connect-Befehl kein ICMP-Fehler empfangen. Wenn ein ICMP-Fehler empfangen wurde, sind seine Informationen verfügbar, bis die <strong>Verbindung</strong> erneut aufgerufen wird. Die Informationen werden als <a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a> Struktur zurückgegeben. Für die Typsicherheit sollten Sie die <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo">wsageticmperrorinfo</a> -Funktion verwenden, anstatt die Socketoption direkt zu verwenden.</td>
</tr>
<tr>
<td>TCP_KEEPCNT</td>
<td>ja</td>
<td>ja</td>
<td>DWORD</td>
<td>Ruft die Anzahl der TCP-Keep-Alive-Tests ab, die gesendet werden, bevor die Verbindung beendet wird, oder legt Sie fest. TCP_KEEPCNT kann nicht auf einen Wert größer als 255 festgelegt werden.</td>
</tr>
<tr>
<td>TCP_MAXRT</td>
<td>ja</td>
<td>ja</td>
<td>DWORD</td>
<td>Wenn dieser Wert nicht negativ ist, stellt er das gewünschte Verbindungs Timeout in Sekunden dar. Wenn der Wert-1 ist, stellt er eine Anforderung zum Deaktivieren des Verbindungs Timeouts dar (d. h., die Verbindung wird immer wieder übertragen). Wenn das Verbindungs Timeout deaktiviert ist, erhöht sich der Wert für das erneute übertragen für jede erneute Übertragung um bis zu einem Höchstwert von 60 Sek.</td>
</tr>
<tr>
<td>TCP_NODELAY</td>
<td>ja</td>
<td>ja</td>
<td>DWORD (Boolean)</td>
<td>Aktiviert oder deaktiviert den Nagle-Algorithmus für TCP-Sockets. Diese Option ist standardmäßig deaktiviert (auf false festgelegt).</td>
</tr>
<tr>
<td>TCP_TIMESTAMPS</td>
<td>ja</td>
<td>ja</td>
<td>DWORD (Boolean)</td>
<td>Aktiviert oder deaktiviert RFC 1323-Zeitstempel. Beachten Sie, dass es auch eine globale Konfiguration für Zeitstempel (standardmäßig deaktiviert), &quot; Zeitstempel &quot; in (Set/Get)-nettcpsetting gibt. Wenn Sie diese Socketoption festlegen, wird diese globale Konfigurationseinstellung überschrieben.</td>
</tr>
<tr>
<td>TCP_FASTOPEN</td>
<td>ja</td>
<td>ja</td>
<td>DWORD (Boolean)</td>
<td>Aktiviert oder deaktiviert das schnelle Öffnen von <a href="https://tools.ietf.org/html/rfc7413">RFC 7413</a> TCP, sodass Sie während der drei-Wege-Hand Shake Phase beim Öffnen einer Verbindung mit dem Senden von Daten beginnen können. Beachten Sie, dass Sie zum Verwenden der schnellen Öffnungszeiten <a href="/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex"><strong>connectex</strong></a> verwenden sollten, um die anfängliche Verbindung herzustellen, und Daten im <em>lpsendbuffer</em> -Parameter der Funktion angeben, die während des Hand Shake Vorgangs übertragen werden sollen. Einige der Daten in <em>lpsendbuffer</em> werden unter dem fast Open-Protokoll übertragen.</td>
</tr>
<tr>
<td>TCP_KEEPIDLE</td>
<td>ja</td>
<td>ja</td>
<td>DWORD</td>
<td>Ruft ab oder legt fest, wie viele Sekunden eine TCP-Verbindung im Leerlauf bleiben soll, bevor KeepAlive-Überprüfungen an den Remote Computer gesendet werden.
<blockquote>
[!Note]<br />
Diese Option ist ab Windows 10, Version 1709, verfügbar.
</blockquote>
<br/></td>
</tr>
<tr>
<td>TCP_KEEPINTVL</td>
<td>ja</td>
<td>ja</td>
<td>DWORD</td>
<td>Ruft ab oder legt fest, wie viele Sekunden eine TCP-Verbindung auf eine KeepAlive-Antwort wartet, bevor ein weiterer KeepAlive-Test gesendet wird.
<blockquote>
[!Note]<br />
Diese Option ist ab Windows 10, Version 1709, verfügbar.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>

## <a name="windows-support-for-ipproto_tcp-options"></a>Windows-Unterstützung für ipproto \_ TCP-Optionen

| Option | Windows 10 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|
| TCP- \_ bsdurgent | x | x | x | x |
| TCP \_ beschleunigt \_ 1122 | x | x | x | x |
| TCP \_ keepcnt | Ab Windows 10, Version 1703 | | | |
| TCP \_ maxrt | x | x | x | x |
| TCP- \_ nodelay | x | x | x | x |
| TCP- \_ Zeitstempel | x | x | x | x |
| TCP \_ fastopen | Ab Windows 10, Version 1607 | | | |

<br/>

 | Option | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9X/ME |
|-|-|-|-|-|-|
| TCP- \_ bsdurgent | x | x | x | x | |
| TCP \_ beschleunigt \_ 1122 | x | x | x | | |
| TCP \_ keepcnt | | | | | |
| TCP \_ maxrt | | | | | |
| TCP- \_ nodelay | x | x | x | x | |
| TCP- \_ Zeitstempel | | | | | |
| TCP \_ fastopen | | | | | |

## <a name="remarks"></a>Bemerkungen

Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Header Dateien geändert, und die **ipproto \_ TCP** -Ebene wird in der Header Datei " *Ws2def. h* " definiert, die automatisch in der Header Datei " *Winsock2. h* " enthalten ist. Die **ipproto- \_ TCP** -Socketoptionen, mit Ausnahme von **TCP- \_ bsdurgent**, sind in der Header Datei " *Ws2ipdef. h* " definiert, die automatisch in der Header Datei " *Ws2tcpip. h* " enthalten ist. Die **TCP- \_ bsdurgent** -Option ist aus historischen Gründen in der Header Datei " *mswap. h* " definiert. Die Header Dateien *Ws2def. h* und *Ws2ipdef. h* sollten niemals direkt verwendet werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | <dl> <dt>Ws2def. h (Include Winsock2. h); </dt> <dt>Winsock2. h unter Windows Server 2003, Windows XP und Windows 2000</dt> </dl> |
