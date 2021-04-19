---
description: Der Steuerungs Code konfiguriert einen TCP-Socket für eine geringere Latenz und schnellere Vorgänge an der Loopback Schnittstelle.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: SIO_LOOPBACK_FAST_PATH Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f32cba8a081d2eb268a3e93a362ccec9bf414d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360715"
---
# <a name="sio_loopback_fast_path-control-code"></a>SIO_LOOPBACK_FAST_PATH Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG

Der Code für die **\_ \_ schnelle \_ Pfad Steuerung von SIO Loopback** konfiguriert einen TCP-Socket für eine geringere Latenz und schnellere Vorgänge in der Loopback Schnittstelle.

**Wichtig**  Der **\_ \_ schnelle \_ Pfad des SIO-Loopbacks** ist veraltet und wird nicht für die Verwendung im Code empfohlen.

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>Parameter

### <a name="s"></a>s

Ein Deskriptor, der einen Socket identifiziert.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Der Steuerelement Code für den Vorgang.
Verwenden Sie für diesen Vorgang einen **\_ \_ schnellen \_ Pfad** für den hoch-Loopback.

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter enthält einen Zeiger auf einen booleschen Wert, der angibt, ob der Socket für schnelle Loopback Vorgänge konfiguriert werden soll.

### <a name="cbinbuffer"></a>cbinbuffer

Die Größe des Eingabe Puffers in Bytes.

### <a name="lpvoutbuffer"></a>lpvoutbuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cboutbuffer"></a>cboutbuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter muss auf 0 (null) festgelegt werden.

### <a name="lpcbbytesreturned"></a>lpcbbyteszurück gegeben

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.

Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).

Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.

Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.
Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.
Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.

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
|**ausstehende WSA-e/a \_ \_** | Überlappende e/a-Vorgänge werden ausgeführt. Dieser Wert wird zurückgegeben, wenn ein überlappende Vorgang erfolgreich initiiert wurde und die Beendigung zu einem späteren Zeitpunkt angegeben wird. |
| **WSA- \_ Vorgang \_ abgebrochen** | Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen. Dieser Fehler wird zurückgegeben, wenn ein über Lapp ender Vorgang aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush ioctl** " abgebrochen wurde. |
| **WSAEACCES** | Es wurde versucht, auf einen Socket auf eine Weise zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist. Dieser Fehler wird unter mehreren Bedingungen für persistente Port Reservierungen zurückgegeben, die Folgendes umfassen: dem Benutzer fehlen die erforderlichen Administratorrechte auf dem lokalen Computer, oder die Anwendung wird nicht in einer erweiterten Shell als integrierter Administrator ( `RunAs administrator` ) ausgeführt. |
| **WSAEFAULT** | Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt. Dieser Fehler wird zurückgegeben, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer*, *lpcbbytesall*, *lpoverlgetauscht* oder *lpCompletionRoutine* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist. |
| **Wsaeingabe Progress** | Ein Blockierungsvorgang wird momentan ausgeführt. Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird. |
| **Wsaeingabe** | Ein Blockierungs Vorgang wurde durch einen [**wsacancelblockingstatement**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)-Aufrufvorgang unterbrochen. Dieser Fehler wird zurückgegeben, wenn ein Blockierungs Vorgang unterbrochen wurde. |
| **Wsaabval** | Ein ungültiges Argument wurde angegeben. Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode* -Parameter kein gültiger Befehl ist oder wenn ein angegebener Eingabeparameter nicht zulässig ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist. |
| **WSAENETDOWN** | Bei einem Socketvorgang war das Netzwerk inaktiv. Dieser Fehler wird zurückgegeben, wenn das Netzwerk Subsystem fehlgeschlagen ist. |
| **Wsaumotsock** | Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist. Dieser Fehler wird zurückgegeben, wenn es sich bei den *Deskriptoren nicht* um einen Socket handelt. |
| **WSAEOPNOTSUPP** | Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der angegebene ioctl-Befehl nicht unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn der IOCTL-Pfad für die hoch- **\_ Loopback \_ \_** -Schleife vom Transportanbieter nicht unterstützt wird. |

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann die IOCTL-Schleife für den **\_ \_ schnellen \_ Loopback** Bereich verwenden, um die Latenz zu verringern und die Leistung von Loopback Vorgängen auf einem TCP-Socket zu verbessern.
Diese IOCTL fordert an, dass der TCP/IP-Stapel einen speziellen schnellen Pfad für Loopback Vorgänge in diesem Socket verwendet.
Die IOCTL-Schleife für den " **SIO \_ Loopback \_ \_** " kann nur mit TCP-Sockets verwendet werden.
Diese IOCTL muss auf beiden Seiten der Loopback Sitzung verwendet werden.
Der schnelle TCP-Loopback Pfad wird entweder über die IPv4-oder IPv6-loopback Schnittstelle unterstützt.

Der Socket, der die Verbindungsanforderung initiieren soll, muss diese IOCTL vor dem Herstellen der Verbindungsanforderung anwenden.
Der von der [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)-, [**connectex**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex)-, [**wsaconnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect)-, [**wsaconnectbylist**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)-oder [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) -Funktion verwendete Socket zum Initiieren der Verbindung muss daher diese IOCTL anwenden, um den schnellen Pfad für Loopback Vorgänge zu verwenden.

Der Socket, der die Verbindungsanforderung überwacht, muss diese IOCTL anwenden, bevor die Verbindung akzeptiert wird.
Der von der Funktion "lauschen" verwendete Socket muss daher diese IOCTL anwenden, sodass alle akzeptierten Sockets den schnellen Pfad für Loopback verwenden.
Alle Sockets, die von der Funktion "lauschen" zurückgegeben und an die Funktion " [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)", " [**Accept**](/windows/desktop/api/winsock/nf-winsock-acceptex)" oder " [**wsaaccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) " übermittelt werden, werden für die Verwendung des speziellen schnellen Pfads für Loopback Vorgänge

Sobald eine Anwendung die Verbindung über eine Loopback Schnittstelle mithilfe des schnellen Pfads herstellt, müssen alle Pakete für die Lebensdauer der Verbindung den schnellen Pfad verwenden.

Wenn Sie den **\_ \_ schnellen \_ Pfad von SIO Loopback** auf einen Socket anwenden, der mit einem nicht-Loopback Pfad verbunden wird, hat dies keine Auswirkungen.

Diese TCP-Loopback Optimierung führt zu Paketen, die über die Transport Schicht (TL) statt über das herkömmliche Loopback durch die Netzwerkschicht fließen.
Diese Optimierung erhöht die Latenz für Loopback Pakete.
Wenn sich eine Anwendung für eine Einstellung auf Verbindungs Ebene für die Verwendung des schnellen Loopbacks-Pfads entscheidet, werden alle Pakete dem Loopback Pfad folgen.
Bei der Loopback Kommunikation werden Überlastung und Paket Ablagevorgang nicht erwartet.
Das Konzept der Überlastungs Steuerung und der zuverlässigen Übermittlung in TCP ist unnötig.
Dies gilt jedoch nicht für die Fluss Steuerung.
Ohne Fluss Steuerung kann der Absender den Empfangs Puffer überlasten, was zu einem fehlerhaften TCP-Loopback Verhalten führt.
Die Fluss Steuerung im TCP-optimierten Loopback Pfad wird durch das Platzieren von Sende Anforderungen in einer Warteschlange beibehalten.
Wenn der Empfangs Puffer voll ist, gewährleistet der TCP/IP-Stapel, dass die Sende Vorgänge nicht vollständig ausgeführt werden, bis die Warteschlange gewartet hat

TCP-schnell Pfad Loopback Verbindungen bei vorhanden sein einer Windows-Filter Plattform (WFP) für Verbindungsdaten müssen den nicht optimierten langsamen Pfad für Loopback annehmen.
WFP-Filter verhindern also, dass dieser neue schnelle Pfad für Loopbacks verwendet wird.
Wenn ein WFP-Filter aktiviert ist, wird der langsame Pfad auch dann verwendet, wenn der IOCTL-Wert für den **\_ \_ schnell \_ Pfad für "sio Loopback** " festgelegt wurde.
Dadurch wird sichergestellt, dass Benutzermodus-Anwendungen über die gesamte WFP-Sicherheitsfunktion verfügen.

Standardmäßig ist **der \_ \_ schnelle \_ Pfad** für die hoch-Loopback Option deaktiviert.

Es wird nur eine Teilmenge der TCP/IP-Socketoptionen unterstützt, wenn die IOCTL-Schleife für den Schleifen-Schleifen- **\_ \_ schnell \_ Pfad** verwendet wird, um den schnellen Loopback Pfad für einen Socket zu aktivieren.
Die Liste der unterstützten Optionen umfasst Folgendes:

* **IP- \_ TTL**
* **IP- \_ Unicast \_ if**
* **IPv6- \_ \_ unicasthops**
* **IPv6- \_ Unicast, \_ Wenn**
* **IPv6- \_ V6ONLY**
* **\_bedingte \_ Annahme**
* **" \_ exclusiveaddruse"**
* **\_Port \_ Skalierbarkeit**
* **\_rcvbuf**
* **\_reuseaddr**
* **TCP- \_ bsdurgent**

## <a name="see-also"></a>Siehe auch

[**IPPROTO_IP Socketoptionen**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**IPPROTO_IPV6 Socketoptionen**](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[**IPPROTO_TCP Socketoptionen**](/windows/desktop/winsock/ipproto-tcp-socket-options)

[**Glühbirne**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOL_SOCKET Socketoptionen**](/windows/desktop/winsock/sol-socket-socket-options)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
