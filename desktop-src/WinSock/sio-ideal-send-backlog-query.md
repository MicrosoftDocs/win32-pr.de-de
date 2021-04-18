---
description: Der Steuercode Ruft den idealen Wert für den Sende Rückstand für die zugrunde liegende Verbindung ab.
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: SIO_IDEAL_SEND_BACKLOG_QUERY Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351409"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a>SIO_IDEAL_SEND_BACKLOG_QUERY Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG

Der optimale Abfrage Steuerungs Code für den " **SIO- \_ \_ \_ senderückstand \_** " Ruft den idealen ISB-Wert (Send Rückstand) für die zugrunde liegende Verbindung ab.

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
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
Verwenden Sie für diesen Vorgang die **\_ optimale \_ \_ \_ Abfrage zum Senden** des sendebacklogs.

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cbinbuffer"></a>cbinbuffer

Die Größe des Eingabe Puffers in Bytes.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="lpvoutbuffer"></a>lpvoutbuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter sollte auf einen **ulong** -Datentyp zeigen, wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* **null** sind.

### <a name="cboutbuffer"></a>cboutbuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter muss mindestens die Größe eines **ulong** -Datentyps aufweisen.

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

Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.
Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.

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
| **WSA- \_ Vorgang \_ abgebrochen** | Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen. |
| **WSAEFAULT** | Der Parameter " *lpvinbuffer*", " *lpvoutbuffer*", " *lpcbbytesgab*", " *lpoverlgetauscht* " oder " *lpCompletionRoutine* " ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten. |
| **Wsaeingabe Progress** | Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird. |
| **Wsaeingabe** | Ein Blockierungs Vorgang wurde unterbrochen. |
| **Wsaabval** | Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar. Dieser Fehler wird zurückgegeben, wenn der *cboutbuffer* -Parameter kleiner als die Größe eines **ulong** -Datentyps ist.
| **WSAENETDOWN** | Das Netzwerk Subsystem ist fehlgeschlagen. |
| **Wsaumoproumopt** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **WSAENOTCONN** | Die Socket s ist nicht verbunden. |
| **Wsaumotsock** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene ioctl-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn die IOCTL- **\_ \_ \_ \_ Abfrage des optimalen** sendebacklogs nicht vom Transportanbieter unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn ein Versuch der Verwendung der " **SIO \_ ideal \_ Send \_ \_ backbackquery** ioctl" für einen Datagramm-Socket erfolgt. |

## <a name="remarks"></a>Bemerkungen

Die IOCTL- **\_ \_ \_ \_ Abfrage des optimalen** sendebacklogs wird unter Windows Server 2008, Windows Vista mit Service Pack 1 (SP1) und höheren Versionen des Betriebssystems unterstützt.

Beim Senden von Daten über eine TCP-Verbindung mithilfe von Windows Sockets ist es wichtig, dass Sie eine ausreichende Menge an ausstehenden Daten (gesendet, aber noch nicht bestätigt) in TCP aufbewahren, um den höchsten Durchsatz zu erzielen.
Der ideale Wert für die Datenmenge, die für den optimalen Durchsatz für die TCP-Verbindung aussteht, wird als ideale Größe des sendebacklogs (ISB) bezeichnet.
Der ISB-Wert ist eine Funktion des Produkts zur Bandbreiten Verzögerung der TCP-Verbindung und des angekündigten Empfangs Fensters des Empfängers (und zum Teil der Überlastung im Netzwerk).

Der ISB-Wert pro Verbindung ist über die TCP-Protokoll Implementierung in Windows Server 2008, Windows Vista mit SP1 und höheren Versionen des Betriebssystems verfügbar.
Der **\_ optimale \_ Abfrage \_ \_** -ioctl-Abfragedienst kann von einer Anwendung verwendet werden, um eine Benachrichtigung zu erhalten, wenn der ISB-Wert für eine Verbindung dynamisch geändert wird.

Unter Windows Server 2008, Windows Vista mit SP1 und höheren Versionen des Betriebssystems werden die Daten von [**der \_ optimalen \_ Sende \_ Rückstands \_ Änderung**](sio-ideal-send-backlog-change.md) und der **\_ optimalen \_ Sende \_ Rückstand \_ Abfrage** IOCTLs von der optimalen Sende Rückstands Abfrage für Stream-orientierte Sockets unterstützt, die verbunden sind.

Der Bereich für den ISB-Wert einer TCP-Verbindung kann theoretisch von 0 bis maximal 16 Megabyte abweichen.

Die typische Verwendung der " [**SIO \_ ideal \_ Send \_ \_**](sio-ideal-send-backlog-change.md) Backlogs Change" und der " **SIO \_ ideal \_ Send \_ \_ backbackquery** IOCTLs" basiert auf der Send-Methode, die von den Anwendungen verwendet wird.
Es werden zwei gängige Fälle erläutert.

Anwendungen, die eine blockierende oder nicht blockierende Sende Anforderung gleichzeitig ausführen, basieren in der Regel auf der internen Sende Pufferung durch Winsock, um einen angemessenen Durchsatz zu erzielen.
Das Sendepuffer Limit für eine bestimmte Verbindung wird durch die **\_ sndbuf** -Socketoption "so" gesteuert.
Bei der blockierenden und nicht blockierenden Sende Methode bestimmt der Grenzwert für den Sendepuffer, wie viele Daten in TCP verbleiben.
Wenn der ISB-Wert für die Verbindung größer als das Sendepuffer Limit ist, ist der Durchsatz, der für die Verbindung erreicht wird, nicht optimal.
Um einen besseren Durchsatz zu erzielen, können die Anwendungen den Grenzwert für den Sendepuffer basierend auf dem Ergebnis der ISB-Abfrage festlegen, da ISB-Änderungs Benachrichtigungen für die Verbindung auftreten.

Bei Anwendungen, die die überlappende Send-Methode mit ausstehenden ausstehenden Sende Anforderungen verwenden, wird die Menge der in TCP ausstehenden Daten durch das Sendepuffer Limit in Winsock und die Gesamtmenge der Daten, die in den ausstehenden überlappenden Sende Anforderungen enthalten sind, bestimmt.
In diesem Fall sollten Anwendungen den ISB-Wert verwenden, um zu bestimmen, wie viele ausstehende Sende Anforderungen aufbewahrt werden sollen und welche Daten für die einzelnen Sende Anforderungen verwendet werden sollen.
Im Idealfall sollte die Anwendung versuchen, die folgende Gleichung zufrieden zu halten:

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

Beachten Sie, dass die Verwendung der ISB IOCTLs über TCP-Sockets in der obigen Weise zu einer erhöhten Speicherauslastung in Exchange führen kann, um den Durchsatz bei Verbindungen mit einem Produkt mit hoher Bandbreite zu erhöhen.
Die TCP-Implementierung in Windows drosselt ISB-Werte nach Bedarf basierend auf der Gesamtauslastung des System Arbeitsspeichers.

Die IOCTL- **\_ \_ \_ \_ Abfrage des optimalen Sende** Backlogs ist nur auf einem Stream-Socket zulässig, der sich im verbundenen Zustand befindet.
Andernfalls schlägt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** mit **wsaenotconn** fehl.

Alle ioctl können unbegrenzt blockieren, abhängig von der Implementierung des Dienstanbieters.
Wenn die Anwendung die Blockierung in einem [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktions aufrufnis nicht tolerieren kann, werden überlappende e/a-Vorgänge für IOCTLs empfohlen, die besonders wahrscheinlich blockiert werden.

Die " **SIO \_ ideal Send \_ backbackquery \_ \_** ioctl" wird wahrscheinlich nicht blockiert, sodass Sie normalerweise synchron aufgerufen wird, wenn die Parameter " *lpoverlgetauscht* " und " *lpCompletionRoutine* " auf **null** festgelegt sind.

Bei der Verwendung der IOCTL- **\_ \_ \_ \_ Abfrage** für den optimalen sendebackbackioctl- **\_ Vorgang \_** **kann in den** folgenden Fällen ein Fehler auftreten.

Die TCP-Verbindung ist in der Senderichtung ordnungsgemäß getrennt.
Dies kann ein Ergebnis eines Aufrufs der Funktion zum Herunterfahren mit dem auf **SD \_ Send** festgelegten Parameter, einem Aufrufen der **disconnectex** -Funktion oder eines Aufrufs der Funktion **TransmitFile** oder **transmitpaketen** mit dem Parameter *dwFlags* , der auf **tf \_ Disconnect** oder TF- **\_ Wiederverwendung** festgelegt ist.
Die TCP-Verbindung wurde zurückgesetzt oder abgebrochen.
Die Anforderung wird vom e/a-Manager abgebrochen.

In der Header Datei " *Ws2tcpip. h* " sind zwei Inline-Wrapper Funktionen für diese IOCTLs definiert.
Es wird empfohlen, dass diese Inline Funktionen anstelle der [**\_ optimalen optimalen \_ Sende \_ Rückstands \_ Änderung**](sio-ideal-send-backlog-change.md) und der **\_ optimalen \_ Sende Rückstands Abfrage von der optimalen Sende \_ Rückstands \_ Abfrage** IOCTLs verwendet werden.

Die Funktion "Inline Wrapper" für die IOCTL-Änderung von " [**SIO \_ ideal \_ Send \_ \_**](sio-ideal-send-backlog-change.md) Backlogs" ist die Funktion " **idesendbacklognotify** ".

Die Funktion "Inline Wrapper" für die IOCTL- **\_ \_ \_ \_ Abfrage des optimalen** sendebacklogs ist die Funktion " **ideal Send backlogquery** ".

Die dynamische Sende Pufferung für TCP wurde unter Windows 7 und Windows Server 2008 R2 hinzugefügt.
Standardmäßig ist die dynamische Sende Pufferung für TCP aktiviert, es sei denn, eine Anwendung legt die **\_ sndbuf** -Socketoption für den Datenstrom Socket fest.

Die Verwendung von Netsh ist die empfohlene Methode, um die dynamische Sende Pufferung für TCP abzufragen oder festzulegen.

Der aktuelle Wert für die dynamische Sende Pufferung für TCP kann mit dem folgenden Befehl abgerufen werden:

`netsh winsock show autotuning`

Die dynamische Sende Pufferung für TCP kann mit dem folgenden Befehl deaktiviert werden:

`netsh winsock set autotuning off`

Die dynamische Sende Pufferung für TCP kann mithilfe des folgenden Befehls aktiviert werden:

`netsh winsock set autotuning on`

Obwohl es nicht empfohlen wird, kann die dynamische Sende Pufferung aus einer Anwendung deaktiviert werden, indem der folgende Registrierungs Wert auf 0 (null) festgelegt wird:

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

Wenn Sie den Wert für die dynamische Sende Pufferung mithilfe von NetSh.exe ändern oder den Registrierungs Wert ändern, muss der Computer neu gestartet werden, damit die Änderung wirksam wird.

Bei der dynamischen Sende Pufferung unter Windows 7 und Windows Server 2008 R2 werden die Anforderungen der [**\_ optimalen Sende \_ \_ Rückstands \_ Änderung**](sio-ideal-send-backlog-change.md) und **der \_ optimalen \_ Sende \_ Rückstand \_ Abfrage** IOCTLs der optimalen Sende Rückstand nur in besonderen Fällen benötigt.

## <a name="see-also"></a>Siehe auch

[**SIO_IDEAL_SEND_BACKLOG_CHANGE**](sio-ideal-send-backlog-change.md)

[**Glühbirne**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
