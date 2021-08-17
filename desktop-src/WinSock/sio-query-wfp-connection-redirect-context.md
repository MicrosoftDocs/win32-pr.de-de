---
description: Der Steuerungscode ruft den Umleitungskontext für einen Umleitungsdatensatz ab, der von einem Windows Filtering Platform Redirect Service verwendet wird.
ms.assetid: 87DB11BB-E08D-49DF-A211-133D813373E0
title: SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT-Steuerelementcode
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 268e1bf44c1370e49116414a367119ea8eb008a2711cbfcebdf64f6c3c1b8d62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244940"
---
# <a name="sio_query_wfp_connection_redirect_context-control-code"></a>SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT-Steuerelementcode

## <a name="description"></a>BESCHREIBUNG

Der **Steuerungscode SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT** ruft den Umleitungskontext für einen Umleitungsdatensatz ab, der von einem WFP-Umleitungsdienst (Windows Filtering Platform) verwendet wird.

Rufen Sie zum Ausführen dieses Vorgangs die [**Funktion WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl** mit den folgenden Parametern auf.

```cpp
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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
Verwenden Sie für diesen Vorgang **SIO \_ QUERY \_ WFP \_ CONNECTION REDIRECT \_ \_ CONTEXT.**

### <a name="lpvinbuffer"></a>lpvInBuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cbinbuffer"></a>cbInBuffer

Die Größe des Eingabepuffers in Bytes.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter sollte auf einen **ULONG-Datentyp** verweisen, wenn die Parameter *lpOverlapped* und *lpCompletionRoutine* **NULL** sind.

### <a name="cboutbuffer"></a>cbOutBuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter muss mindestens die Größe eines **ULONG-Datentyps** aufweisen.

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
| **WSA \_ IO \_ PENDING** | Ein überlappender Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angezeigt. |
| **\_WSA-VORGANG \_ ABGEBROCHEN** | Ein überlappender Vorgang wurde aufgrund des Schließens des Sockets oder der Ausführung des SIO_FLUSH IOCTL-Befehls abgebrochen. |
| **WSAEFAULT** | Der *Parameter lpvOutBuffer,* *lpcbBytesReturned,* *lpOverlapped* oder *lpCompletionRoutine* ist nicht vollständig in einem gültigen Teil des Benutzeradressbereichs enthalten. |
| **WSAEINPROGRESS** | Die Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird. |
| **WSAEINTR** | Ein Blockierungsvorgang wurde unterbrochen. |
| **WSAEINVAL** | Der *dwIoControlCode-Parameter* ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht akzeptabel, oder der Befehl gilt nicht für den angegebenen Sockettyp. Dieser Fehler wird zurückgegeben, wenn der *cbOutBuffer-Parameter* kleiner als die Größe eines **ULONG-Datentyps** ist. |
| **WSAENETDOWN** | Fehler beim Netzwerksubsystem. |
| **WSAENOPROTOOPT** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **WSAENOTCONN** | Die *Sockets sind* nicht verbunden. |
| **WSAENOTSOCK** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene IOCTL-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn die **SIO \_ QUERY \_ WFP \_ CONNECTION REDIRECT \_ \_ CONTEXT** IOCTL vom Transportanbieter nicht unterstützt wird. |

## <a name="remarks"></a>Hinweise

**SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT** IOCTL wird auf Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.

WFP ermöglicht den Zugriff auf den TCP/IP-Paketverarbeitungspfad, wobei ausgehende und eingehende Pakete untersucht oder geändert werden können, bevor sie weiter verarbeitet werden können.
Durch Tippen auf den TCP/IP-Verarbeitungspfad können unabhängige Softwarehersteller (INDEPENDENT Software Vendors, ISVs) leichter Firewalls, Antivirensoftware, Diagnosesoftware und andere Arten von Anwendungen und Diensten erstellen.
WFP stellt Benutzermodus- und Kernelmoduskomponenten bereit, sodass ISVs von Drittanbietern an den Filterentscheidungen teilnehmen können, die auf mehreren Ebenen im TCP/IP-Protokollstapel und im gesamten Betriebssystem erfolgen.
Mit dem WFP-Verbindungsumleitungsfeature kann ein WFP-Aufrufkerneltreiber eine Verbindung lokal an einen Benutzermodusprozess umleiten, eine Inhaltsuntersuchung im Benutzermodus durchführen und den überprüften Inhalt mithilfe einer anderen Verbindung an das ursprüngliche Ziel weiterleiten.

**SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT** IOCTL und mehrere andere zugehörige IOCTLS sind Benutzermoduskomponenten, die es mehreren WFP-basierten Verbindungsproxyanwendungen ermöglichen, denselben Datenverkehrsfluss kooperativ zu überprüfen.
Jeder Überprüfungs-Agent kann den Netzwerkdatenverkehr, der bereits von einem anderen Überprüfungs-Agent überprüft wurde, sicher erneut überprüfen.
Wenn mehrere Proxys vorhanden sind (z. B. von verschiedenen ISVs entwickelt), könnte die Verbindung, die von einem Proxy für die Kommunikation mit dem endgültigen Ziel verwendet wird, wiederum von einem zweiten Proxy umgeleitet werden, und diese neue Verbindung kann wiederum vom ursprünglichen Proxy umgeleitet werden.
Ohne Verbindungsnachverfolgung erreicht die ursprüngliche Verbindung möglicherweise nie ihr endgültiges Ziel, da sie in einer Endlosproxyschleife hängen bleibt.

Die **SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ CONTEXT-IOCTL \_** wird verwendet, um mehreren WFP-basierten Verbindungsproxyanwendungen zu ermöglichen, denselben Datenverkehrsfluss kooperativ zu überprüfen.
Jeder Überprüfungs-Agent kann den Netzwerkdatenverkehr, der bereits von einem anderen Überprüfungs-Agent überprüft wurde, sicher erneut überprüfen.
Wenn mehrere Proxys vorhanden sind (z. B. von verschiedenen ISVs entwickelt), könnte die Verbindung, die von einem Proxy für die Kommunikation mit dem endgültigen Ziel verwendet wird, wiederum von einem zweiten Proxy umgeleitet werden, und diese neue Verbindung kann wiederum vom ursprünglichen Proxy umgeleitet werden.
Ohne Verbindungsnachverfolgung erreicht die ursprüngliche Verbindung möglicherweise nie ihr endgültiges Ziel, da sie in einer Endlosproxyschleife hängen bleibt.
Die **SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ CONTEXT-IOCTL \_** wird verwendet, um die Nachverfolgung von Proxyverbindungen für umgeleitete Socketverbindungen bereitzustellen.
Dieses WFP-Feature ermöglicht die Nachverfolgung von Umleitungsdatensätzen von der ersten Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.

Die **SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ RECORDS-IOCTL \_** wird von einem WFP-basierten Umleitungsdienst verwendet, um den Umleitungsdatensatz von der akzeptierten TCP/IP-Paketverbindung (z. B. dem verbundenen Socket für einen TCP-Socket oder einem UDP-Socket) abzurufen, der von seinem begleitenden Kernelmodusaufruf, der auf **ALE CONNECT \_ \_ REDIRECT-Ebenen** in einem Kernelmodustreiber registriert ist, an ihn umgeleitet wird.
Die **SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ CONTEXT-IOCTL \_** wird von einem WFP-basierten Umleitungsdienst verwendet, um den Umleitungskontext für einen Umleitungsdatensatz von der akzeptierten TCP/IP-Paketverbindung (z. B. dem verbundenen Socket für einen TCP-Socket oder einem UDP-Socket) abzurufen, der von der begleiten Aufrufliste, die auf **ALE_CONNECT_REDIRECT** Ebenen registriert ist, an ihn umgeleitet wird.
Der Umleitungskontext ist optional und wird verwendet, wenn der aktuelle Umleitungsstatus einer Verbindung ist, dass die Verbindung vom aufrufenden Umleitungsdienst umgeleitet wurde oder die Verbindung zuvor vom aufrufenden Umleitungsdienst umgeleitet wurde, später jedoch erneut von einem anderen Umleitungsdienst umgeleitet wurde.
Der Umleitungsdienst überträgt den abgerufenen Umleitungsdatensatz an den TCP-Socket, den er verwendet, um den ursprünglichen Inhalt mithilfe der **SIO \_ SET \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS** IOCTL als Proxy zu verwenden.

Da der WFP-Umleitungskontext ein Vom Umleitungsdienst festgelegtes Datenblob variabler Länge ist, kann der Aufrufer entweder einen großen Ausgabepuffer (ein 1K-Puffer, auf den z. B. der *lpvOutBuffer-Parameter* zeigt) bereitstellen oder als Ausgabepuffergröße im *cbOutBuffer-Parameter* 0 übergeben, um die Puffergröße abzufragen, die zum Speichern des zurückgegebenen Blobs erforderlich ist.
Wenn die Größe des Ausgabepuffers die Daten nicht enthält, geben die [**Funktionen WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl** **ERROR INSUFFICIENT \_ \_ BUFFER** zurück, und die erforderliche Puffergröße wird als Wert zurückgegeben, auf den der *lpcbBytesReturned-Parameter* zeigt.

Die Anwendung, die **die SIO \_ QUERY \_ WF\P_CONNECTION \_ REDIRECT \_ RECORDS** IOCTL aufruft, muss das Blob, das die abgerufenen Umleitungsdatensätze enthält, nicht verstehen.
Dies ist ein nicht transparentes Datenblob, das die Anwendung abrufen und an den neuen Socket übergeben muss.

## <a name="see-also"></a>Weitere Informationen

[**IPPROTO_IP Socketoptionen**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**](sio-set-wfp-connection-redirect-records.md)

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
