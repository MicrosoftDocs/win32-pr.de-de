---
description: Mithilfe von Steuerungs Code kann ein Socket alle IPv4-oder IPv6-Pakete empfangen, die über eine Netzwerkschnittstelle übergeben werden.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: SIO_RCVALL Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343676"
---
# <a name="sio_rcvall-control-code"></a>SIO_RCVALL Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG
Der " **SIO \_ rcvall** "-Steuerungs Code ermöglicht einem Socket, alle IPv4-oder IPv6-Pakete zu empfangen, die über eine Netzwerkschnittstelle übergeben werden.

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

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

Der Steuerelement Code für den Vorgang.
Verwenden Sie für diesen Vorgang " **SIO \_ rcvall** ".

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer, der den Optionswert enthalten soll.
Die möglichen Werte für die Option " **SIO \_ rcvall** ioctl" werden in der **RCVALL_VALUE** Enumeration angegeben, die in der Header Datei " *MSTCPIP. h* " definiert ist.

Die möglichen Werte für " **SIO \_ rcvall** " lauten wie folgt:

| Wert | Bedeutung |
|-------|---------|
| **rcvall \_ aus** | Deaktivieren Sie diese Option, damit ein Socket nicht alle IPv4-oder IPv6-Pakete empfängt, die über eine Netzwerkschnittstelle übergeben werden. |
| **rcvall \_ on** | Aktivieren Sie diese Option, damit ein Socket alle IPv4-oder IPv6-Pakete empfängt, die über eine Netzwerkschnittstelle übergeben werden. Diese Option aktiviert den gemischten-Modus auf der Netzwerkschnittstellenkarte (NIC), wenn die NIC den gemischten-Modus unterstützt. In einem LAN-Segment mit einem Netzwerkhub erfasst eine NIC, die den gemischten-Modus unterstützt, den gesamten IPv4-oder IPv6-Datenverkehr im LAN, einschließlich des Datenverkehrs zwischen anderen Computern desselben LAN-Segments. Alle aufgezeichneten Pakete (IPv4 oder IPv6, abhängig vom Socket) werden an den Rohdaten Socket übermittelt. Mit dieser Option werden nicht andere Pakete (z. b. ARP-, IPX-und NetBEUI-Pakete) auf der-Schnittstelle erfasst. NetMon verwendet den gleichen Modus für die Netzwerkschnittstelle, verwendet diese Option jedoch nicht zum Erfassen von Datenverkehr. |
| **rcvall \_ socketlevelonly** | Diese Funktion ist zurzeit nicht implementiert, sodass das Festlegen dieser Option keine Auswirkung hat. |
| **rcvall \_ iplevel** | Aktivieren Sie diese Option, damit ein IPv4-oder IPv6-Socket alle Pakete auf IP-Ebene empfängt, die über eine Netzwerkschnittstelle übergeben werden. Diese Option aktiviert nicht den gemischten-Modus auf der Netzwerkschnittstellenkarte. Diese Option wirkt sich nur auf die Paketverarbeitung auf IP-Ebene aus. Die NIC empfängt weiterhin nur Pakete, die an die konfigurierten Unicast-und Multicast Adressen weitergeleitet werden. Ein Socket, für den diese Option aktiviert ist, empfängt jedoch nicht nur Pakete, die an bestimmte IP-Adressen weitergeleitet werden, sondern empfängt alle IPv4-oder IPv6-Pakete, die die NIC empfängt. Mit dieser Option werden keine anderen Pakete (z. b. ARP-, IPX-und NetBEUI-Pakete) erfasst, die über die Schnittstelle empfangen werden. |

### <a name="cbinbuffer"></a>cbinbuffer

Die Größe des Eingabe Puffers in Bytes.
Dieser Parameter muss größer oder gleich der Größe des **RCVALL_VALUE** Enumerationswerts sein, auf den der *lpvinbuffer* -Parameter verweist.

### <a name="lpvoutbuffer"></a>lpvoutbuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cboutbuffer"></a>cboutbuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="lpcbbytesreturned"></a>lpcbbyteszurück gegeben

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="lpvoverlapped"></a>lpvoverlgetauscht

Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.

Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.

Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.
In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.

Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.
Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).

### <a name="lpthreadid"></a>lpthreadid

Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.
Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.

**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.

### <a name="lperrno"></a>lperrno

Ein Zeiger auf den Fehlercode.

**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.
Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Fehlercode | Bedeutung |
|------------|---------|
| **ausstehende WSA-e/a \_ \_** | Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben. |
| **WSA- \_ Vorgang \_ abgebrochen** | Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des **SIO_FLUSH** ioctl-Befehls abgebrochen. |
| **WSAEFAULT** | Der *lpoverllapp* -oder *lpCompletionRoutine* -Parameter ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten. |
| **Wsaeingabe Progress** | Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird. |
| **Wsaeingabe** | Ein Blockierungs Vorgang wurde unterbrochen. |
| **Wsaabval** | Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar. Dieser Fehler wird auch zurückgegeben, wenn der *cbinbuffer* -Parameter kleiner als `sizeof(UCHAR)` oder der *lpvinbuffer* -Parameter auf einen Wert verweist, der kein **RCVALL_VALUE** Enumerationswert ist. Dieser Fehler kann auch zurückgegeben werden, wenn die dem Socket zugeordnete Netzwerkschnittstelle nicht gefunden wurde. Dies kann vorkommen, wenn die Netzwerkschnittstelle, die dem Socket zugeordnet ist, gelöscht oder entfernt wird (z. b. ein Entfernen von PCMCIA oder ein USB-Netzwerkgerät). |
| **WSAENETDOWN** | Das Netzwerk Subsystem ist fehlgeschlagen. |
| **WSAENOBUFS** | Es ist kein Pufferspeicher verfügbar. |
| **Wsaumoproumopt** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **Wsaumotsock** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene ioctl-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn die " **SIO \_ rcvall** "-ioctl vom Transportanbieter nicht unterstützt wird. |

## <a name="remarks"></a>Bemerkungen

Die IOCTL " **SIO \_ rcvall** " wird unter Windows 2000 und höheren Versionen des Betriebssystems unterstützt.

Mit der " **SIO \_ rcvall** "-ioctl kann ein Socket alle IPv4-oder IPv6-Pakete an einer Netzwerkschnittstelle empfangen.
Das an die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** über gegebene Sockethandle muss einer der folgenden sein:

* Ein IPv4-Socket, der erstellt wurde, wobei die Adressfamilie auf AF_INET festgelegt ist, der socketyp auf SOCK_RAW und das Protokoll auf IPPROTO_IP festgelegt wurde.
* Ein IPv6-Socket, der erstellt wurde, wobei die Adressfamilie auf AF_INET6 festgelegt ist, der socketyp auf SOCK_RAW und das Protokoll auf IPPROTO_IPV6 festgelegt wurde.

Weitere Informationen zu rohsockets finden Sie unter [**TCP/IP-rohsockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).

Der Socket muss auch an eine explizite lokale IPv4-oder IPv6-Schnittstelle gebunden werden, was bedeutet, dass Sie keine Bindung an **inaddr \_ any** oder **in6addr \_ any** herstellen können.

Nachdem der Socket gebunden und die IOCTL erfolgreich abgeschlossen wurde, geben Aufrufe der [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) -oder der [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -Funktion IPv4-Datagramme zurück, die die angegebene IPv4-Schnittstelle übergeben, oder geben IPv6-Datagramme zurück, die die angegebene IPv6-Schnittstelle übergeben.
Beachten Sie, dass Sie einen ausreichend großen Puffer angeben müssen.
Durch Festlegen dieser ioctl werden nur IPv4-oder IPv6-Pakete für eine bestimmte Schnittstelle erfasst.
Mit dieser ioctl werden z. b. keine anderen Pakete (z. b. ARP-, IPX-und NetBEUI-Pakete) auf der-Schnittstelle erfasst.

Ein an eine bestimmte lokale Schnittstelle mit der " **SIO \_ rcvall** ioctl" gebundener Socket empfängt nur Pakete, die diese Schnittstelle passieren.
Er empfängt keine Pakete, die auf einer anderen Schnittstelle empfangen werden, und wird an eine andere Schnittstelle weitergeleitet, die sich von der mit der " **SIO \_ rcvall** ioctl" gebundenen

Unter Windows Server 2008 und früheren Versionen werden von der IOCTL-Einstellung " **SIO \_ rcvall** " keine lokalen Pakete erfasst, die von einer Netzwerkschnittstelle gesendet werden.
Diese enthielten Pakete, die auf einer anderen Schnittstelle empfangen wurden, und haben die für die IOCTL " **SIO \_ rcvall** " angegebene Netzwerkschnittstelle weitergeleitet.

Unter Windows 7 und Windows Server 2008 R2 wurde dies geändert, sodass lokale Pakete, die von einer Netzwerkschnittstelle gesendet werden, ebenfalls aufgezeichnet werden.
Dies schließt Pakete ein, die auf einer anderen Schnittstelle empfangen werden, und leitet dann die Netzwerkschnittstelle, die an den Socket gebunden ist, mit der " **SIO \_ rcvall** "

Das Festlegen dieser ioctl erfordert Administrator Rechte auf dem lokalen Computer.

Diese Funktion wird manchmal als gemischten-Modus bezeichnet.
Jede direkte Änderung von der Anwendung dieser Option auf eine Schnittstelle und dann auf eine andere Schnittstelle mit einem einzigen-Befehl, der diese IOCTL verwendet, wird nicht unterstützt.
Eine Anwendung muss zuerst dieses ioctl-Element verwenden, um das Verhalten auf der ersten Schnittstelle zu deaktivieren, und dann diese IOCTL verwenden, um das Verhalten für eine neue Schnittstelle zu aktivieren.

## <a name="see-also"></a>Siehe auch

[**Glühbirne**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**TCP/IP-Rohdaten Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
