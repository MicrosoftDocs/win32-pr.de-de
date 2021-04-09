---
description: Der Steuercode fragt die Transport Einstellungen für einen Socket ab.
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: SIO_QUERY_TRANSPORT_SETTING Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 592301f0fcdbbb0d3d5babba446583d2e48db086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863804"
---
# <a name="sio_query_transport_setting-control-code"></a>SIO_QUERY_TRANSPORT_SETTING Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG

Der Verwaltungs Code für die Übertragung der **\_ Abfrage- \_ Transport \_** Einstellungen fragt die Transport Einstellungen für einen Socket ab.

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
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
Verwenden Sie für diesen Vorgang die **\_ \_ Transport \_ Einstellung "sio-Abfrage** ".

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter enthält einen Zeiger auf eine-Struktur, in der der erste Member der-Struktur eine [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) Struktur ist, die bestimmt, welche Transport Einstellung abgefragt wird.

### <a name="cbinbuffer"></a>cbinbuffer

Die Größe des Eingabe Puffers in Bytes.
Dieser Parameter hängt von der abgefragten Transport Einstellung ab.

### <a name="lpvoutbuffer"></a>lpvoutbuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter hängt von der Transport Einstellung ab, die abgefragt wird, wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* **null** sind.

### <a name="cboutbuffer"></a>cboutbuffer

Die Größe des Ausgabepuffers in Bytes.

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
| **Fehler \_ beim \_ Puffer.** | Der an einen System Rückruf über gegebene Datenbereich ist zu klein. Dieser Fehler wird zurückgegeben, wenn der Puffer, auf den der *lpvoutbuffer* -Parameter verweist, eine Puffergröße hat, die im *cboutbuffer* -Parameter übergeben wurde, zu klein ist. Die erforderliche Puffergröße wird im Parameter " *lpcbbytes}* " zurückgegeben. |
| **ausstehende WSA-e/a \_ \_** | Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben. |
| **WSA- \_ Vorgang \_ abgebrochen** | Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen. |
| **WSAEFAULT** | Der Parameter " *lpvoutbuffer*", " *lpcbbytesis*", " *lpoverlgetauscht*" oder " *lpCompletionRoutine* " ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten. |
| **Wsaeingabe Progress** | Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird. |
| **Wsaeingabe** | Ein Blockierungs Vorgang wurde unterbrochen. |
| **Wsaabval** | Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar. |
| **WSAENETDOWN** | Das Netzwerk Subsystem ist fehlgeschlagen. |
| **Wsaumoproumopt** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **WSAENOTCONN** | Die Socket s ist nicht verbunden. |
| **Wsaumotsock** | Der Deskriptor s ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene ioctl-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn die IOCTL- **\_ Abfrage \_ Transport \_ Einstellung** des Transport Anbieters vom Transport Anbieter nicht unterstützt wird. |

## <a name="remarks"></a>Bemerkungen

Die IOCTL- **\_ Abfrage \_ Transport \_ Einstellung** ist unter Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.

Die IOCTL- **\_ Abfrage \_ Transport \_ Einstellung** ist eine generische IOCTL, die zum Abfragen der Transport Einstellungen eines Sockets verwendet wird.
Die abgefragte Transport Einstellung basiert auf der [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , die im *lpvinbuffer* -Parameter übergeben wird.

Die einzige Transport Einstellung, die derzeit definiert, ist die Funktion für die **echt \_ Zeit \_ Benachrichtigungs \_ Funktion** in einem TCP-Socket.

Wenn für die [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , die im *lpvinbuffer* -Parameter übergeben wurde, das GUID-Element auf **echt \_ Zeit \_ Benachrichtigungs \_ Funktion** festgelegt ist, ist dies eine Anforderung zum Abfragen der Echt Zeit Benachrichtigungseinstellungen für den TCP-Socket, der mit dem [**controlchannel-**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) Parameter verwendet wird, um Hintergrund Netzwerk Benachrichtigungen in einer Windows Store-App zu empfangen
Der *lpvinbuffer* -Parameter sollte auf eine [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) Struktur zeigen.
Der *lpvoutbuffer* -Parameter sollte auf eine **Ausgabestruktur in Echtzeit- \_ \_ Benachrichtigungs \_ Einstellungen \_** zeigen.
Diese Transport Einstellung gilt nur für TCP-Sockets.
Mit dieser Transport Einstellung kann WinInet oder ähnliche Netzwerkdienste einen bestimmten TCP-Socket Abfragen, um den Status des [**controlchannel-Auslösers**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) zu ermitteln.
Eine Windows Store-App ruft diese IOCTL nicht direkt auf.
Wenn der Aufruf von [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** erfolgreich ist, gibt diese IOCTL eine Ausgabestruktur der **echt \_ Zeit \_ Benachrichtigungs \_ Einstellung \_** mit dem aktuellen Status zurück.

Die IOCTL- **\_ Abfrage \_ Transport \_ Einstellung** ist eine Möglichkeit für WinInet oder ähnliche Netzwerkdienste, den Transport Einstellungs Status für einen bestimmten TCP-Socket abzufragen, um zu bestimmen, ob [**controlchannel-Auslösers**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) auf dem Socket aktiviert ist.
Eine Windows Store-App ruft diese IOCTL nicht direkt auf.

Diese IOCTL gilt nur für TCP-Sockets.

## <a name="see-also"></a>Siehe auch

[**CONTROL_CHANNEL_TRIGGER_STATUS**](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[**SIO_APPLY_TRANSPORT_SETTING**](sio-apply-transport-setting.md)

[Glühbirne](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
