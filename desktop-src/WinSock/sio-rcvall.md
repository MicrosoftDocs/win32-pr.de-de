---
description: Steuerungscode ermöglicht es einem Socket, alle IPv4- oder IPv6-Pakete zu empfangen, die über eine Netzwerkschnittstelle übergeben werden.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: SIO_RCVALL-Steuerelementcode
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: d545bcdf8f3cc01159b3afbc86a686fb2bf8e83493784d2197353f19ff01e576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993430"
---
# <a name="sio_rcvall-control-code"></a>SIO_RCVALL-Steuerelementcode

## <a name="description"></a>Beschreibung
Mit **dem SIO RC COD-Steuerungscode \_** kann ein Socket alle IPv4- oder IPv6-Pakete empfangen, die über eine Netzwerkschnittstelle übergeben werden.

Um diesen Vorgang durchzuführen, rufen Sie die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** mit den folgenden Parametern auf.

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a>Parameter

### <a name="s"></a>s

Ein Deskriptor, der einen Socket identifiziert.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Der Steuerungscode für den Vorgang.
Verwenden **Sie SIO \_ RCIO** für diesen Vorgang.

### <a name="lpvinbuffer"></a>lpvInBuffer

Ein Zeiger auf den Eingabepuffer, der den Optionswert enthalten soll.
Die möglichen Werte für die **SIO \_ RC HK** IOCTL-Option werden in der RCVALL_VALUE-Enumeration  angegeben, die in der *Headerdatei Mstcpip.h* definiert ist.

Die möglichen Werte **für SIO \_ RC WIE** FOLGT:

| Wert | Bedeutung |
|-------|---------|
| **RC RC \_ OFF** | Deaktivieren Sie diese Option, damit ein Socket nicht alle IPv4- oder IPv6-Pakete erhält, die über eine Netzwerkschnittstelle übergeben werden. |
| **RC RC \_ RC ON** | Aktivieren Sie diese Option, damit ein Socket alle IPv4- oder IPv6-Pakete empfängt, die über eine Netzwerkschnittstelle übergeben werden. Diese Option aktiviert den promiscuous-Modus auf der Netzwerkschnittstellenkarte (NIC), wenn die NIC den promiscuous-Modus unterstützt. In einem LAN-Segment mit einem Netzwerkhub erfasst eine NIC, die den promiscuous-Modus unterstützt, den sämtlichen IPv4- oder IPv6-Datenverkehr im LAN, einschließlich des Datenverkehrs zwischen anderen Computern im selben LAN-Segment. Alle erfassten Pakete (IPv4 oder IPv6, je nach Socket) werden an den unformatierten Socket übermittelt. Diese Option erfasst keine anderen Pakete (z. B. ARP-, IPX- und NetBEUI-Pakete) auf der Schnittstelle. Netmon verwendet den gleichen Modus für die Netzwerkschnittstelle, aber nicht diese Option, um Datenverkehr zu erfassen. |
| **RCBUCH \_ SOCKETLEVELONLY** | Dieses Feature ist derzeit nicht implementiert, sodass das Festlegen dieser Option keine Auswirkungen hat. |
| **RC GOVERNANCE \_ IPLEVEL** | Aktivieren Sie diese Option, damit ein IPv4- oder IPv6-Socket alle Pakete auf IP-Ebene empfängt, die über eine Netzwerkschnittstelle übergeben werden. Mit dieser Option wird der promiscuous-Modus auf der Netzwerkschnittstellenkarte nicht aktiviert. Diese Option wirkt sich nur auf die Paketverarbeitung auf IP-Ebene aus. Die NIC empfängt weiterhin nur Pakete, die an die konfigurierten Unicast- und Multicastadressen geleitet werden. Ein Socket mit aktivierter Option empfängt jedoch nicht nur Pakete, die an bestimmte IP-Adressen geleitet werden, sondern auch alle IPv4- oder IPv6-Pakete, die die NIC empfängt. Diese Option erfasst keine anderen Pakete (z. B. ARP-, IPX- und NetBEUI-Pakete), die auf der Schnittstelle empfangen werden. |

### <a name="cbinbuffer"></a>cbInBuffer

Die Größe des Eingabepuffers in Bytes.
Dieser Parameter sollte gleich oder größer als  die Größe des RCVALL_VALUE-Enumerationswerts sein, auf den der *lpvInBuffer-Parameter* verweist.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cboutbuffer"></a>cbOutBuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten in Bytes empfängt.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="lpvoverlapped"></a>lpvOverlapped

Ein Zeiger auf eine [**WSAOVERLAPPED-Struktur.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Wenn *Sockets ohne* das überlappende Attribut erstellt wurden, wird *der lpOverlapped-Parameter* ignoriert.

Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpOverlapped-Parameter* nicht **NULL** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.
In diesem Fall muss *der lpOverlapped-Parameter* auf eine gültige [**WSAOVERLAPPED-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) verweisen.

Bei überlappenden Vorgängen wird die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** sofort zurückgegeben, und die entsprechende Abschlussmethode wird signalisiert, wenn der Vorgang abgeschlossen wurde.
Andernfalls gibt die Funktion erst dann zurück, wenn der Vorgang abgeschlossen wurde oder ein Fehler auftritt.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Ein Zeiger auf die Abschlussroutine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).

### <a name="lpthreadid"></a>lpThreadId

Ein Zeiger auf eine [**WSATHREADID-Struktur,**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) die vom Anbieter in einem nachfolgenden Aufruf von [**WPUQueueApc verwendet werden soll.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)
Der Anbieter sollte die [**referenzierte WSATHREADID-Struktur**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) (nicht den Zeiger auf dieselbe) speichern, bis die [**WPUQueueApc-Funktion**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) zurückgegeben wurde.

**Hinweis:**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**

### <a name="lperrno"></a>lpErrno

Ein Zeiger auf den Fehlercode.

**Hinweis:**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** **SOCKET ERROR \_ zurück.**
Um erweiterte Fehlerinformationen zu erhalten, rufen [**Sie WSAGetLastError auf.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

| Fehlercode | Bedeutung |
|------------|---------|
| **AUSSTEHENDE \_ \_ WSA-E/A** | Ein überlappende Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angezeigt. |
| **\_WSA-VORGANG \_ ABGEBROCHEN** | Ein überlappende Vorgang wurde aufgrund des Schließens des  Sockets oder der Ausführung des SIO_FLUSH IOCTL-Befehls abgebrochen. |
| **WSAEFAULT** | Der *lpOverlapped-* oder *lpCompletionRoutine-Parameter* ist nicht vollständig in einem gültigen Teil des Benutzeradrenraums enthalten. |
| **WSAEINPROGRESS** | Die Funktion wird aufgerufen, wenn ein Rückruf in Bearbeitung ist. |
| **WSAEINTR** | Ein blockierende Vorgang wurde unterbrochen. |
| **WSAEINVAL** | Der *dwIoControlCode-Parameter* ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht akzeptabel, oder der Befehl gilt nicht für den angegebenen Sockettyp. Dieser Fehler wird auch zurückgegeben, wenn der *cbInBuffer-Parameter* kleiner als der ist oder der `sizeof(UCHAR)` *lpvInBuffer-Parameter* auf einen Wert verweist, der kein RCVALL_VALUE ist.  Dieser Fehler kann auch zurückgegeben werden, wenn die dem Socket zugeordnete Netzwerkschnittstelle nicht gefunden werden kann. Dies kann auftreten, wenn die dem Socket zugeordnete Netzwerkschnittstelle gelöscht oder entfernt wird (z. B. ein PCMCIA- oder USB-Netzwerkgerät entfernen). |
| **WSAENETDOWN** | Fehler beim Netzwerksubsystem. |
| **WSAENOBUFS** | Kein Pufferspeicherplatz verfügbar. |
| **WSAENOPROTOOPT** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **WSAENOTSOCK** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene IOCTL-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn **die SIO \_ RCIO IOCTL** vom Transportanbieter nicht unterstützt wird. |

## <a name="remarks"></a>Hinweise

Die **SIO \_ RCIO** IOCTL wird auf Windows 2000 und höher des Betriebssystems unterstützt.

Mit **der SIO RCFÜHRUNGS-IOCTL \_** kann ein Socket alle IPv4- oder IPv6-Pakete auf einer Netzwerkschnittstelle empfangen.
Das socket-Handle, das an [**die WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** übergeben wird, muss eine der folgenden Sein:

* Ein IPv4-Socket, der erstellt wurde, bei dem die Adressfamilie auf AF_INET, der Sockettyp auf SOCK_RAW und das Protokoll auf IPPROTO_IP.
* Ein IPv6-Socket, der erstellt wurde, bei dem die Adressfamilie auf AF_INET6, der Sockettyp auf SOCK_RAW und das Protokoll auf IPPROTO_IPV6.

Weitere Informationen zu unformatiert Sockets finden Sie unter [**TCP/IP Raw Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).

Der Socket muss auch an eine explizite lokale IPv4- oder IPv6-Schnittstelle gebunden werden, was bedeutet, dass Sie keine Bindung an **INADDR \_ ANY** oder **in6addr \_ beliebiger -Schnittstelle erstellen können.**

Sobald der Socket gebunden ist und die IOCTL erfolgreich abgeschlossen wurde, geben Aufrufe der [**WSARecv-**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) oder [**recv-Funktionen**](/windows/desktop/api/winsock/nf-winsock-recv) IPv4-Datagramme zurück, die die gegebene IPv4-Schnittstelle oder IPv6-Datagramme über die gegebene IPv6-Schnittstelle übergeben.
Beachten Sie, dass Sie einen ausreichend großen Puffer liefern müssen.
Durch festlegen dieser IOCTL werden nur IPv4- oder IPv6-Pakete auf einer bestimmten Schnittstelle erfasst.
Diese IOCTL erfasst keine anderen Pakete (z. B. ARP-, IPX- und NetBEUI-Pakete) auf der Schnittstelle.

Ein Socket, der an eine bestimmte lokale Schnittstelle mit **der SIO \_ RC RC IOCTL** gebunden ist, erhält nur Pakete, die diese Schnittstelle passieren.
Es werden keine Pakete empfangen, die auf einer anderen Schnittstelle empfangen und an eine andere Schnittstelle weitergeleitet werden, die sich von der Socketgrenze mit **SIO \_ RC RC RCIO** IOCTL unterscheiden.

Auf Windows Server 2008 und früher erfasste die **SIO \_ RCIO** IOCTL-Einstellung keine lokalen Pakete, die von einer Netzwerkschnittstelle gesendet wurden.
Dies umfasste Pakete, die auf einer anderen Schnittstelle empfangen und die netzwerkschnittstelle weitergeleitet wurden, die für **die SIO \_ RCIO** IOCTL angegeben ist.

In Windows 7 und Windows Server 2008 R2 wurde dies geändert, sodass lokale Pakete, die von einer Netzwerkschnittstelle gesendet werden, ebenfalls erfasst werden.
Dies schließt Pakete ein, die auf einer anderen Schnittstelle empfangen und dann die netzwerkgebundene Netzwerkschnittstelle an den Socket mit **SIO \_ RCIO** IOCTL weitergeleitet wurden.

Zum Festlegen dieser IOCTL ist die Administratorberechtigung auf dem lokalen Computer erforderlich.

Dieses Feature wird manchmal auch als promiscuous-Modus bezeichnet.
Jede direkte Änderung von der Anwendung dieser Option auf eine Schnittstelle und dann auf eine andere Schnittstelle mit einem einzelnen Aufruf mithilfe dieser IOCTL wird nicht unterstützt.
Eine Anwendung muss diese IOCTL zuerst verwenden, um das Verhalten auf der ersten Schnittstelle zu deaktivieren, und dann diese IOCTL verwenden, um das Verhalten auf einer neuen Schnittstelle zu aktivieren.

## <a name="see-also"></a>Siehe auch

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Unformatiert TCP/IP-Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
