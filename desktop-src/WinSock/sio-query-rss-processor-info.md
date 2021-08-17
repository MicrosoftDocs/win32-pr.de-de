---
description: Steuerungscode fragt die Zuordnung zwischen einem Socket und einem RSS-Prozessorkern und NUMA-Knoten ab.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: SIO_QUERY_RSS_PROCESSOR_INFO-Steuerelementcode
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 6c0f690555beb19f7d5d79a81e2cc900194f731c3acacb075ae12dc304debffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740382"
---
# <a name="sio_query_rss_processor_info-control-code"></a>SIO_QUERY_RSS_PROCESSOR_INFO-Steuerelementcode

## <a name="description"></a>Beschreibung

Der Steuerungscode **SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** fragt die Zuordnung zwischen einem Socket und einem RSS-Prozessorkern und NUMA-Knoten ab.

Rufen Sie zum Ausführen dieses Vorgangs die [**Funktion WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl** mit den folgenden Parametern auf.

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

Der Steuerelementcode für den Vorgang.
Verwenden Sie **SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** für diesen Vorgang.

### <a name="lpvinbuffer"></a>lpvInBuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cbinbuffer"></a>cbInBuffer

Die Größe des Eingabepuffers in Bytes.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter sollte auf eine [**SOCKET \_ PROCESSOR \_ AFFINITY-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) verweisen, wenn die Parameter *lpOverlapped* und *lpCompletionRoutine* **NULL** sind.

### <a name="cboutbuffer"></a>cbOutBuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter muss mindestens die Größe einer [**SOCKET \_ PROCESSOR \_ AFFINITY-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) aufweisen.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten in Bytes empfängt.

Wenn der Ausgabepuffer zu klein ist, schlägt der Aufruf fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbBytesReturned-Parameter* zeigt auf den *DWORD-Wert* 0 (null).

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

Ein Zeiger auf eine [**WSATHREADID-Struktur,**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) die vom Anbieter in einem nachfolgenden Aufruf von [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)verwendet werden soll.
Der Anbieter sollte die [**referenzierte WSATHREADID-Struktur**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) (nicht den Zeiger auf denselben) speichern, bis die [**WPUQueueApc-Funktion**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) zurückgegeben wurde.

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
| **FEHLER: \_ \_ UNZUREICHENDER PUFFER** | Der an einen Systemaufruf übergebene Datenbereich ist zu klein. Dieser Fehler wird zurückgegeben, wenn der Puffer, auf den der *lpvOutBuffer-Parameter* zeigt, mit einer im *cbOutBuffer-Parameter* übergebenen Puffergröße zu klein ist. Die erforderliche Puffergröße wird im *lpcbBytesReturned-Parameter* zurückgegeben. Dieser Fehler wird zurückgegeben, wenn der *cbOutBuffer-Parameter* kleiner als die Größe einer [**SOCKET PROCESSOR \_ \_ AFFINITY-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) ist. |
| **WSA \_ IO \_ PENDING** | Ein überlappender Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angezeigt. |
| **\_WSA-VORGANG \_ ABGEBROCHEN** | Ein überlappender Vorgang wurde aufgrund des Schließens des Sockets oder der Ausführung des **SIO \_ FLUSH** IOCTL-Befehls abgebrochen. |
| **WSAEFAULT** | Der Parameter *lpvInBuffer,* *lpvoutBuffer,* *lpcbBytesReturned,* *lpOverlapped* oder *lpCompletionRoutine* ist nicht vollständig in einem gültigen Teil des Benutzeradressbereichs enthalten. |
| **WSAEINPROGRESS** | Die Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird. |
| **WSAEINTR** | Ein Blockierungsvorgang wurde unterbrochen. |
| **WSAEINVAL** | Der *dwIoControlCode-Parameter* ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht akzeptabel, oder der Befehl gilt nicht für den angegebenen Sockettyp. Dieser Fehler wird zurückgegeben, wenn der *cbOutBuffer-Parameter* kleiner als die Größe einer [**SOCKET PROCESSOR \_ \_ AFFINITY-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) ist.
| **WSAENETDOWN** | Fehler beim Netzwerksubsystem. |
| **WSAENOPROTOOPT** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **WSAENOTCONN** | Die *Sockets sind* nicht verbunden. |
| **WSAENOTSOCK** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene IOCTL-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn die **SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** IOCTL vom Transportanbieter nicht unterstützt wird. |

## <a name="remarks"></a>Hinweise

Die **SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** IOCTL wird auf Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.

Das IOCTL für **\_ SIO QUERY \_ RSS PROCESSOR \_ \_ INFO** wird verwendet, um die Zuordnung zwischen einem Socket und einem RSS-Prozessorkern und NUMA-Knoten zu bestimmen.
Diese IOCTL gibt eine [**SOCKET \_ PROCESSOR \_ AFFINITY-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) zurück, die die [**\_ PROZESSORNUMMER**](/windows/desktop/api/winnt/ns-winnt-processor_number) und die NUMA-Knoten-ID enthält.
Die [**zurückgegebene PROCESSOR \_ NUMBER-Struktur**](/windows/desktop/api/winnt/ns-winnt-processor_number) enthält eine Gruppennummer und eine relative Prozessornummer innerhalb der Gruppe.

Wenn es sich bei dem Socket um einen UDP-Socket handelt, muss der Socket verbunden sein, damit die **SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** IOCTL ordnungsgemäß funktioniert.

## <a name="see-also"></a>Weitere Informationen

[**PROCESSOR_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number)

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOCKET_PROCESSOR_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
