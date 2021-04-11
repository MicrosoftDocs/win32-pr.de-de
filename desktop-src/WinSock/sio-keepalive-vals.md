---
description: Der Steuerungs Code aktiviert oder deaktiviert die Einstellung pro Verbindung der TCP-Keep-Alive-Option, die das TCP-Keep-Alive-Timeout und-Intervall angibt.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: SIO_KEEPALIVE_VALS Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131020"
---
# <a name="sio_keepalive_vals-control-code"></a>SIO_KEEPALIVE_VALS Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG

Der " **SIO \_ KeepAlive \_ Vals** -Steuerungs Code" aktiviert oder deaktiviert die Einstellung pro Verbindung der TCP-Keep-Alive-Option, die das TCP-Keep-Alive-Timeout und-Intervall angibt.

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
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
Verwenden Sie für diesen Vorgang den " **SIO \_ KeepAlive \_ Vals** ".

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter sollte auf eine **TCP \_ KeepAlive** -Struktur zeigen.

### <a name="cbinbuffer"></a>cbinbuffer

Die Größe des Eingabe Puffers in Bytes.
Dieser Parameter muss größer oder gleich der Größe der **TCP \_ KeepAlive** -Struktur sein, auf die durch den *lpvinbuffer* -Parameter verwiesen wird.

### <a name="lpvoutbuffer"></a>lpvoutbuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cboutbuffer"></a>cboutbuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter muss auf 0 (null) festgelegt werden.

### <a name="lpcbbytesreturned"></a>lpcbbyteszurück gegeben

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.
Dieser zurückgegebene Parameter verweist auf einen **DWORD** -Wert von 0 (null) für diesen Vorgang, da keine Ausgabe vorhanden ist.

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
|**ausstehende WSA-e/a \_ \_** | Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben. |
| **WSA- \_ Vorgang \_ abgebrochen** | Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des **SIO_FLUSH ioctl** -Befehls abgebrochen. |
| **WSAEFAULT** | Der *lpoverllapp* -oder *lpCompletionRoutine* -Parameter ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten. |
| **Wsaeingabe Progress** | Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird. |
| **Wsaeingabe** | Ein Blockierungs Vorgang wurde unterbrochen. |
| **Wsaabval** | Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar. |
| **WSAENETDOWN** | Das Netzwerk Subsystem ist fehlgeschlagen. |
| **Wsaumoproumopt** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. Dieser Fehler wird für einen Datagramm-Socket zurückgegeben. |
| **Wsaumotsock** | Der Deskriptor s ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene ioctl-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der " **SIO \_ KeepAlive \_ Vals** ioctl" vom Transportanbieter nicht unterstützt wird. |

## <a name="remarks"></a>Bemerkungen

Der " **SIO \_ KeepAlive \_ Vals** ioctl" wird unter Windows 2000 und höheren Versionen des Betriebssystems unterstützt.

Der " **SIO \_ KeepAlive \_ Vals** "-Steuerungs Code aktiviert oder deaktiviert die Einstellung pro Verbindung der TCP-Keep-Alive-Option, die das TCP-Keep-Alive-Timeout und das für TCP-Keep-Alive-Pakete verwendete Intervall angibt.
Weitere Informationen zur Keep-Alive-Option finden Sie im Abschnitt 4.2.3.6 zu den Anforderungen für Internet Hosts – in RFC 1122 angegebene Kommunikations Schichten auf der [IETF-Website](https://www.ietf.org/rfc/rfc1122.txt).
(Diese Ressource ist möglicherweise nur in englischer Sprache verfügbar.)

Der *lpvinbuffer* -Parameter sollte auf eine **TCP- \_ KeepAlive** -Struktur verweisen, die in der Header Datei " *MSTCPIP. h* " definiert ist.
Diese Struktur ist wie folgt definiert:

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

Der im **ToggleMicrophoneOnOff** -Member angegebene Wert bestimmt, ob TCP Keep-Alive aktiviert oder deaktiviert ist.
Wenn der **ToggleMicrophoneOnOff** -Member auf einen Wert ungleich 0 (null) festgelegt ist, wird TCP Keep-Alive aktiviert, und die anderen Elemente in der Struktur werden verwendet.
Der **"KeepAliveTime"** -Member gibt das Timeout (in Millisekunden) ohne Aktivität an, bis das erste Keep-Alive-Paket gesendet wird.
Der **"KeepAliveInterval"** -Member gibt das Intervall (in Millisekunden) zwischen dem Senden von Keep-Alive-Paketen an, wenn keine Bestätigung empfangen wird.

Die Option [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , die eine der [**SOL_SOCKET Socketoptionen**](/windows/desktop/winsock/sol-socket-socket-options)ist, kann auch verwendet werden, um den TCP-Keep-Alive-Vorgang für eine Verbindung zu aktivieren oder zu deaktivieren und den aktuellen Status dieser Option abzufragen.
Um abzufragen, ob TCP Keep-Alive für einen Socket aktiviert ist, kann die getsockopt-Funktion mit der [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) -Option aufgerufen werden.
Um TCP Keep-Alive zu aktivieren oder zu deaktivieren, kann die Funktion **setsockopt** mit der Option [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) aufgerufen werden.
Wenn TCP Keep-Alive mit [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)aktiviert ist, werden die standardmäßigen TCP-Einstellungen für Keep-Alive-Timeout und-Intervall verwendet, es sei denn, diese Werte wurden mithilfe von " **SIO \_ KeepAlive \_ Vals**" geändert.

Der standardmäßige systemweite Wert des Keep-Alive-Timeouts ist über die [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) -Registrierungs Einstellung steuerbar, die einen Wert in Millisekunden annimmt. Wenn der Schlüssel nicht festgelegt ist, beträgt der Standardwert für Keep-Alive-Timeout 2 Stunden.
Der standardmäßige systemweite Wert des Keep-Alive-Intervalls kann durch die [**keepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) -Registrierungs Einstellung gesteuert werden, die einen Wert in Millisekunden annimmt. Wenn der Schlüssel nicht festgelegt ist, beträgt das standardmäßige Keep-Alive-Intervall 1 Sekunde.

Unter Windows Vista und höher wird die Anzahl von Keep-Alive-Tests (Neuübertragungen von Daten) auf 10 festgelegt und kann nicht geändert werden.

Unter Windows Server 2003, Windows XP und Windows 2000 ist die Standardeinstellung für die Anzahl von Keep-Alive-Tests 5.
Die Anzahl der Keep-Alive-Tests ist über die Registrierungs Einstellungen **TcpMaxDataRetransmissions** und [**pptptcpmaxdataretransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) steuerbar.
Die Anzahl der Keep-Alive-Tests wird auf den größeren der beiden Registrierungsschlüssel Werte festgelegt.
Wenn diese Zahl 0 ist, werden Keep-Alive-Tests nicht gesendet.
Wenn diese Zahl über 255 liegt, wird Sie an 255 angepasst.

## <a name="see-also"></a>Siehe auch

[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))

[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))

[**Pptptcpmaxdataretransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))

[Glühbirne](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
