---
description: Steuerungs Code fragt die Zuordnung zwischen einem Socket und einem RSS-Prozessor Core und einem NUMA-Knoten ab.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: SIO_QUERY_RSS_PROCESSOR_INFO Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a2d251fa4fee996adaec51599e7b1d140a296b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958921"
---
# <a name="sio_query_rss_processor_info-control-code"></a>SIO_QUERY_RSS_PROCESSOR_INFO Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG

Der Code der **\_ RSS-Abfrage-RSS- \_ \_ Prozessor \_ Info-Abfrage** steuert die Zuordnung zwischen einem Socket und einem RSS-Prozessor Core und einem NUMA-Knoten.

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
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
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
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
Verwenden Sie für diesen Vorgang die RSS-Abfrage für die **\_ \_ RSS- \_ \_ Abfrage** .

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cbinbuffer"></a>cbinbuffer

Die Größe des Eingabe Puffers in Bytes.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="lpvoutbuffer"></a>lpvoutbuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter sollte auf eine [**Affinitäts Struktur des \_ socketprozessors \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) zeigen, wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* **null** sind.

### <a name="cboutbuffer"></a>cboutbuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter muss mindestens die Größe einer [**\_ socketprozessoraffinitäts \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) -Struktur aufweisen.

### <a name="lpcbbytesreturned"></a>lpcbbyteszurück gegeben

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.

Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den *DWORD* -Wert 0 (null).

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
| **Fehler \_ beim \_ Puffer.** | Der an einen System Rückruf über gegebene Datenbereich ist zu klein. Dieser Fehler wird zurückgegeben, wenn der Puffer, auf den der *lpvoutbuffer* -Parameter verweist, eine Puffergröße hat, die im *cboutbuffer* -Parameter übergeben wurde, zu klein ist. Die erforderliche Puffergröße wird im Parameter " *lpcbbytes}* " zurückgegeben. Dieser Fehler wird zurückgegeben, wenn der *cboutbuffer* -Parameter kleiner als die Größe [**einer \_ socketprozessoraffinitäts \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) -Struktur ist. |
| **ausstehende WSA-e/a \_ \_** | Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben. |
| **WSA- \_ Vorgang \_ abgebrochen** | Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen. |
| **WSAEFAULT** | Der Parameter " *lpvinbuffer*", " *lpvoutbuffer*", " *lpcbbytesgab*", " *lpoverlgetauscht* " oder " *lpCompletionRoutine* " ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten. |
| **Wsaeingabe Progress** | Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird. |
| **Wsaeingabe** | Ein Blockierungs Vorgang wurde unterbrochen. |
| **Wsaabval** | Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar. Dieser Fehler wird zurückgegeben, wenn der *cboutbuffer* -Parameter kleiner als die Größe [**einer \_ socketprozessoraffinitäts \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) -Struktur ist.
| **WSAENETDOWN** | Das Netzwerk Subsystem ist fehlgeschlagen. |
| **Wsaumoproumopt** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **WSAENOTCONN** | Die Socket *s* ist nicht verbunden. |
| **Wsaumotsock** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene ioctl-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn die vom Transportanbieter nicht unterstützte ioctl-Abfrage für die **\_ RSS-Abfrage-RSS- \_ \_ \_ Verarbeitung** von der |

## <a name="remarks"></a>Bemerkungen

Die Konfigurations-ioctl für die **\_ RSS-Abfrage \_ RSS \_ \_ -Abfrage** wird unter Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.

Die Informationen ioctl der **\_ Prozessor-Abfrage \_ RSS \_ \_ -Abfrage** wird verwendet, um die Zuordnung zwischen einem Socket und einem RSS-Prozessor Core und einem NUMA-Knoten zu bestimmen.
Diese IOCTL gibt eine [**\_ socketprozessoraffinitäts \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) -Struktur zurück, die die [**Prozessor \_ Nummer**](/windows/desktop/api/winnt/ns-winnt-processor_number) und die NUMA-Knoten-ID enthält.
Die zurückgegebene [**Prozessor \_ Zahlen**](/windows/desktop/api/winnt/ns-winnt-processor_number) Struktur enthält eine Gruppennummer und eine relative Prozessornummer in der Gruppe.

Wenn es sich bei dem Socket um einen UDP-Socket handelt, muss der Socket verbunden sein, damit die IOCTL- **Abfrage "RSS-Abfrage-RSS- \_ \_ \_ Prozessor \_ Informationen** "

## <a name="see-also"></a>Siehe auch

[**PROCESSOR_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number)

[**Glühbirne**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOCKET_PROCESSOR_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
