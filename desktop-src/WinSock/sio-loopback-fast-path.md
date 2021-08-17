---
description: Der Steuerungscode konfiguriert einen TCP-Socket für geringere Latenz und schnellere Vorgänge auf der Loopbackschnittstelle.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: SIO_LOOPBACK_FAST_PATH-Steuerelementcode
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8650cd267d321569aca584e7195fb1bdb79c83a33d931e59e8db37521b8933a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740409"
---
# <a name="sio_loopback_fast_path-control-code"></a>SIO_LOOPBACK_FAST_PATH-Steuerelementcode

## <a name="description"></a>Beschreibung

Der **SIO \_ LOOPBACK \_ FAST PATH-Steuerungscode \_** konfiguriert einen TCP-Socket für geringere Latenz und schnellere Vorgänge auf der Loopbackschnittstelle.

**Wichtig**  **SIO \_ LOOPBACK \_ FAST \_ PATH** ist veraltet und wird nicht empfohlen, in Ihrem Code verwendet zu werden.

Rufen Sie zum Ausführen dieses Vorgangs die [**Funktion WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl** mit den folgenden Parametern auf.

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

Der Steuerelementcode für den Vorgang.
Verwenden Sie für diesen Vorgang **SIO \_ LOOPBACK \_ FAST \_ PATH.**

### <a name="lpvinbuffer"></a>lpvInBuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter enthält einen Zeiger auf einen booleschen Wert, der angibt, ob der Socket für schnelle Loopbackvorgänge konfiguriert werden soll.

### <a name="cbinbuffer"></a>cbInBuffer

Die Größe des Eingabepuffers in Bytes.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cboutbuffer"></a>cbOutBuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter muss auf 0 (null) festgelegt werden.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten in Bytes empfängt.

Wenn der Ausgabepuffer zu klein ist, schlägt der Aufruf fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbBytesReturned-Parameter* zeigt auf den **DWORD-Wert** 0 (null).

Wenn *lpOverlapped* **NULL** ist, darf der **DWORD-Wert,** auf den der *lpcbBytesReturned-Parameter* zeigt, der bei einem erfolgreichen Aufruf zurückgegeben wird, nicht 0 (null) sein.

Wenn der *lpOverlapped-Parameter* für überlappende Sockets nicht **NULL** ist, werden Vorgänge initiiert, die nicht sofort abgeschlossen werden können, und der Abschluss wird zu einem späteren Zeitpunkt angezeigt.
Der **DWORD-Wert,** auf den der *lpcbBytesReturned-Parameter* zeigt, der zurückgegeben wird, kann 0 (null) sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, nachdem der überlappende Vorgang abgeschlossen wurde.
Der endgültige Abschlussstatus kann abgerufen werden, wenn die entsprechende Vervollständigungsmethode signalisiert wird, wenn der Vorgang abgeschlossen wurde.

### <a name="lpvoverlapped"></a>lpvOverlapped

Ein Zeiger auf eine [**WSAOVERLAPPED-Struktur.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Wenn *Sockets* ohne das überlappende Attribut erstellt wurden, wird der *lpOverlapped-Parameter* ignoriert.

Wenn *s* mit dem überlappende Attribut geöffnet wurde und der *lpOverlapped-Parameter* nicht **NULL** ist, wird der Vorgang als überlappender (asynchroner) Vorgang ausgeführt.
In diesem Fall muss der *lpOverlapped-Parameter* auf eine gültige [**WSAOVERLAPPED-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) verweisen.

Für überlappende Vorgänge gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** sofort zurück, und die entsprechende Vervollständigungsmethode wird signalisiert, wenn der Vorgang abgeschlossen wurde.
Andernfalls gibt die Funktion erst dann zurück, wenn der Vorgang abgeschlossen wurde oder ein Fehler auftritt.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Ein Zeiger auf die Abschlussroutine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (wird für nicht überlappende Sockets ignoriert).

### <a name="lpthreadid"></a>lpThreadId

Ein Zeiger auf eine [**WSATHREADID-Struktur,**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) die vom Anbieter in einem nachfolgenden Aufruf von [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)verwendet werden soll.
Der Anbieter sollte die [**referenzierte WSATHREADID-Struktur**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) (nicht den Zeiger auf denselben) speichern, bis die [**WPUQueueApc-Funktion**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) zurückgegeben wurde.

**Hinweis**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**

### <a name="lperrno"></a>lpErrno

Ein Zeiger auf den Fehlercode.

**Hinweis**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** **SOCKET \_ ERROR** zurück.
Um erweiterte Fehlerinformationen abzurufen, rufen [**Sie WSAGetLastError auf.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

| Fehlercode | Bedeutung |
|------------|---------|
|**WSA \_ IO \_ PENDING** | Ein überlappender E/A-Vorgang wird ausgeführt. Dieser Wert wird zurückgegeben, wenn ein überlappender Vorgang erfolgreich initiiert wurde und der Abschluss zu einem späteren Zeitpunkt angegeben wird. |
| **\_WSA-VORGANG \_ ABGEBROCHEN** | Der E/A-Vorgang wurde aufgrund eines Threadendvorgangs oder einer Anwendungsanforderung abgebrochen. Dieser Fehler wird zurückgegeben, wenn ein überlappender Vorgang aufgrund des Schließens des Sockets oder der Ausführung des **SIO \_ FLUSH IOCTL-Befehls** abgebrochen wurde. |
| **WSAEACCES** | Es wurde versucht, auf eine Weise auf einen Socket zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist. Dieser Fehler wird unter mehreren Bedingungen für persistente Portreservierungen zurückgegeben, die Folgendes umfassen: Dem Benutzer fehlen die erforderlichen Administratorrechte auf dem lokalen Computer, oder die Anwendung wird nicht in einer erweiterten Shell als integrierter Administrator ( `RunAs administrator` ) ausgeführt. |
| **WSAEFAULT** | Das System hat beim Versuch, ein Zeigerargument in einem Aufruf zu verwenden, eine ungültige Zeigeradresse erkannt. Dieser Fehler wird zurückgegeben, wenn der *lpvInBuffer-,* *lpvoutBuffer-,* *lpcbBytesReturned-,* *lpOverlapped-* oder *lpCompletionRoutine-Parameter* nicht vollständig in einem gültigen Teil des Benutzeradressraums enthalten ist. |
| **WSAEINPROGRESS** | Ein Blockierungsvorgang wird momentan ausgeführt. Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird. |
| **WSAEINTR** | Ein Blockierungsvorgang wurde durch einen Aufruf von [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)unterbrochen. Dieser Fehler wird zurückgegeben, wenn ein Blockierungsvorgang unterbrochen wurde. |
| **WSAEINVAL** | Ein ungültiges Argument wurde angegeben. Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode-Parameter* kein gültiger Befehl ist oder ein angegebener Eingabeparameter nicht akzeptabel ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist. |
| **WSAENETDOWN** | Bei einem Socketvorgang war das Netzwerk inaktiv. Dieser Fehler wird zurückgegeben, wenn beim Netzwerksubsystem ein Fehler aufgetreten ist. |
| **WSAENOTSOCK** | Es wurde versucht, einen Vorgang für etwas zu unternehmen, das kein Socket ist. Dieser Fehler wird zurückgegeben, wenn der Deskriptor *s* kein Socket ist. |
| **WSAEOPNOTSUPP** | Der versuchsweise Vorgang wird für den Objekttyp, auf den verwiesen wird, nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der angegebene IOCTL-Befehl nicht unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn der **SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL vom Transportanbieter nicht unterstützt wird. |

## <a name="remarks"></a>Hinweise

Eine Anwendung kann die **SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL verwenden, um die Latenz zu reduzieren und die Leistung von Loopbackvorgängen für einen TCP-Socket zu verbessern.
Diese IOCTL fordert an, dass der TCP/IP-Stapel einen speziellen schnellen Pfad für Loopbackvorgänge auf diesem Socket verwendet.
**SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL kann nur mit TCP-Sockets verwendet werden.
Diese IOCTL muss auf beiden Seiten der Loopbacksitzung verwendet werden.
Der schnelle TCP-Loopbackpfad wird mithilfe der IPv4- oder IPv6-Loopbackschnittstelle unterstützt.

Der Socket, der die Verbindungsanforderung initiieren möchte, muss diese IOCTL anwenden, bevor die Verbindungsanforderung gestellt wird.
Daher muss der Socket, der von der [**Funktion connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx,**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex) [**WSAConnect,**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect) [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)oder [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) zum Initiieren der Verbindung verwendet wird, diese IOCTL anwenden, um den schnellen Pfad für Loopbackvorgänge zu verwenden.

Der Socket, der auf die Verbindungsanforderung lauscht, muss diese IOCTL anwenden, bevor die Verbindung akzeptiert wird.
Daher muss der von der Lauschfunktion verwendete Socket diese IOCTL anwenden, damit alle akzeptierten Sockets den schnellen Pfad für loopback verwenden.
Alle Sockets, die von der Listenfunktion zurückgegeben und an die [**Accept-,**](/windows/desktop/api/winsock2/nf-winsock2-accept) [**AcceptEx-**](/windows/desktop/api/winsock/nf-winsock-acceptex)oder [**WSAAccept-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) übergeben werden, werden markiert, um den speziellen schnellen Pfad für Loopbackvorgänge zu verwenden.

Sobald eine Anwendung die Verbindung auf einer Loopbackschnittstelle unter Verwendung des schnellen Pfads herstellt, müssen alle Pakete für die Lebensdauer der Verbindung den schnellen Pfad verwenden.

Das Anwenden von **SIO \_ LOOPBACK \_ FAST \_ PATH** auf einen Socket, der mit einem Nicht-Loopbackpfad verbunden wird, hat keine Auswirkungen.

Diese TCP-Loopbackoptimierung führt zu Paketen, die die Transportschicht (Transport Layer, TL) anstelle des herkömmlichen Loopbacks durch die Netzwerkebene durchlaufen.
Diese Optimierung verbessert die Latenz für Loopbackpakete.
Sobald sich eine Anwendung für eine Einstellung auf Verbindungsebene zur Verwendung des schnellen Loopbackpfads entscheidet, folgen alle Pakete dem Loopbackpfad.
Bei der Loopbackkommunikation werden Keine Überlastung und Paketverdrückung erwartet.
Das Konzept der Überlastungssteuerung und zuverlässigen Übermittlung in TCP ist nicht erforderlich.
Dies gilt jedoch nicht für die Flusssteuerung.
Ohne Flusssteuerung kann der Absender den Empfangspuffer überlasten, was zu einem fehlerhaften TCP-Loopbackverhalten führt.
Die Flusssteuerung im TCP-optimierten Loopbackpfad wird beibehalten, indem Sendeanforderungen in einer Warteschlange platziert werden.
Wenn der Empfangspuffer voll ist, garantiert der TCP/IP-Stapel, dass die Gesendeten erst abgeschlossen werden, wenn die Warteschlange mit der Ablaufsteuerung warten muss.

Tcp-Loopbackverbindungen mit schnellem Pfad bei Vorhandensein einer WFP-Rückruffunktion (Windows Filtering Platform) für Verbindungsdaten müssen den nicht optimierten langsamen Pfad für loopback verwenden.
WFP-Filter verhindern daher die Verwendung dieses neuen schnellen Loopbackpfads.
Wenn ein WFP-Filter aktiviert ist, wird das System den langsamen Pfad auch dann verwenden, wenn **der SIO \_ LOOPBACK-FAST \_ \_ PATH** IOCTL festgelegt wurde.
Dadurch wird sichergestellt, dass Anwendungen im Benutzermodus über die vollständige WFP-Sicherheitsfunktion verfügen.

Standardmäßig ist **SIO \_ LOOPBACK \_ FAST \_ PATH** deaktiviert.

Nur eine Teilmenge der TCP/IP-Socketoptionen wird unterstützt, wenn **SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL verwendet wird, um den schnellen Loopbackpfad für einen Socket zu aktivieren.
Die Liste der unterstützten Optionen umfasst Folgendes:

* **\_IP-Tl**
* **IP \_ UNICAST \_ IF**
* **IPV6 \_ \_ UNICAST-HOPS**
* **IPV6 \_ UNICAST \_ IF**
* **IPV6 \_ V6ONLY**
* **BEDINGTES \_ \_ AKZEPTIEREN ALSO**
* **SO \_ EXCLUSIVEADDRUSE**
* **\_ \_ PORTSKALIERBARKEIT**
* **SO \_ RCVBUF**
* **ALSO \_ WIEDERVERWENDENADDR**
* **TCP \_ BSDBSDENT**

## <a name="see-also"></a>Weitere Informationen

[**IPPROTO_IP Socketoptionen**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**IPPROTO_IPV6 Socketoptionen**](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[**IPPROTO_TCP Socketoptionen**](/windows/desktop/winsock/ipproto-tcp-socket-options)

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOL_SOCKET Socketoptionen**](/windows/desktop/winsock/sol-socket-socket-options)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
