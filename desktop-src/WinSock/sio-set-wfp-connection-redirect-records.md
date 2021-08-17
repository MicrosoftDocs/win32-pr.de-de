---
description: Der Steuerungscode legt den Umleitungsdatensatz auf den neuen TCP-Socket fest, der zum Herstellen einer Verbindung mit dem Umleitungsdienst verwendet wird.
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS-Steuerungscode
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 5d8617f679907e46d8fc194bb75b9e5c2dac267a1c4781fc7cc0f1bf47d49d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993360"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a>SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS-Steuerungscode

## <a name="description"></a>BESCHREIBUNG

Der **Steuerungscode SIO \_ SET \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS** legt den Umleitungsdatensatz auf den neuen TCP-Socket fest, der zum Herstellen einer Verbindung mit dem endgültigen Ziel für die Verwendung durch einen Windows WFP-Umleitungsdienst (Filtering Platform) verwendet wird.

Rufen Sie zum Ausführen dieses Vorgangs die [**Funktion WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl** mit den folgenden Parametern auf.

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a>Parameter

### <a name="s"></a>s

Ein Deskriptor, der einen Socket identifiziert.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Der Steuerelementcode für den Vorgang.
Verwenden Sie **SIO \_ SET \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS** für diesen Vorgang.

### <a name="lpvinbuffer"></a>lpvInBuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter enthält einen Zeiger auf den WFP-Umleitungsdatensatz, der dem Socket zugeordnet ist.

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
| **WSA \_ IO \_ PENDING** | Ein überlappender E/A-Vorgang wird ausgeführt. Dieser Wert wird zurückgegeben, wenn ein überlappender Vorgang erfolgreich initiiert wurde und der Abschluss zu einem späteren Zeitpunkt angegeben wird. |
| **\_WSA-VORGANG \_ ABGEBROCHEN** | Der E/A-Vorgang wurde aufgrund eines Threadendvorgangs oder einer Anwendungsanforderung abgebrochen. Dieser Fehler wird zurückgegeben, wenn ein überlappender Vorgang aufgrund des Schließens des Sockets oder der Ausführung des **SIO_FLUSH** IOCTL-Befehls abgebrochen wurde. |
| **WSAEACCES** | Es wurde versucht, auf eine Weise auf einen Socket zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist. Dieser Fehler wird unter folgenden Bedingungen zurückgegeben: Dem Benutzer fehlen die erforderlichen Administratorrechte auf dem lokalen Computer, oder die Anwendung wird nicht in einer erweiterten Shell als integrierter Administrator ( `RunAs administrator` ) ausgeführt. |
| **WSAEFAULT** | Das System hat beim Versuch, ein Zeigerargument in einem Aufruf zu verwenden, eine ungültige Zeigeradresse erkannt. Dieser Fehler wird zurückgegeben, wenn der *lpvInBuffer-,* *lpvoutBuffer-,* *lpcbBytesReturned-,* *lpOverlapped-* oder *lpCompletionRoutine-Parameter* nicht vollständig in einem gültigen Teil des Benutzeradressraums enthalten ist. |
| **WSAEINPROGRESS** | Ein Blockierungsvorgang wird momentan ausgeführt. Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird. |
| **WSAEINTR** | Ein Blockierungsvorgang wurde durch einen Aufruf von **WSACancelBlockingCall** unterbrochen. Dieser Fehler wird zurückgegeben, wenn ein Blockierungsvorgang unterbrochen wurde. |
| **WSAEINVAL** | Ein ungültiges Argument wurde angegeben. Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode-Parameter* kein gültiger Befehl ist oder ein angegebener Eingabeparameter nicht akzeptabel ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist. |
| **WSAENETDOWN** | Bei einem Socketvorgang war das Netzwerk inaktiv. Dieser Fehler wird zurückgegeben, wenn beim Netzwerksubsystem ein Fehler aufgetreten ist. |
| **WSAENOTSOCK** | Es wurde versucht, einen Vorgang für etwas zu unternehmen, das kein Socket ist. Dieser Fehler wird zurückgegeben, wenn der Deskriptor *s* kein Socket ist. |
| **WSAEOPNOTSUPP** | Der versuchsweise Vorgang wird für den Objekttyp, auf den verwiesen wird, nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der angegebene IOCTL-Befehl nicht unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn die **SIO \_ SET \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS** IOCTL vom Transportanbieter nicht unterstützt wird. |

## <a name="remarks"></a>Hinweise

**SIO \_ SET \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS** IOCTL wird auf Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.

WFP ermöglicht den Zugriff auf den TCP/IP-Paketverarbeitungspfad, wobei ausgehende und eingehende Pakete untersucht oder geändert werden können, bevor sie weiter verarbeitet werden können.
Durch Tippen auf den TCP/IP-Verarbeitungspfad können unabhängige Softwarehersteller (INDEPENDENT Software Vendors, ISVs) leichter Firewalls, Antivirensoftware, Diagnosesoftware und andere Arten von Anwendungen und Diensten erstellen.
WFP stellt Benutzermodus- und Kernelmoduskomponenten bereit, sodass ISVs von Drittanbietern an den Filterentscheidungen teilnehmen können, die auf mehreren Ebenen im TCP/IP-Protokollstapel und im gesamten Betriebssystem erfolgen.
Mit dem WFP-Verbindungsumleitungsfeature kann ein WFP-Aufrufkerneltreiber eine Verbindung lokal an einen Benutzermodusprozess umleiten, eine Inhaltsuntersuchung im Benutzermodus durchführen und den überprüften Inhalt mithilfe einer anderen Verbindung an das ursprüngliche Ziel weiterleiten.

**SIO \_ SET \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS** IOCTL und mehrere andere zugehörige IOCTLS sind Benutzermoduskomponenten, die es mehreren WFP-basierten Verbindungsproxyanwendungen ermöglichen, denselben Datenverkehrsfluss kooperativ zu überprüfen.
Jeder Überprüfungs-Agent kann den Netzwerkdatenverkehr, der bereits von einem anderen Überprüfungs-Agent überprüft wurde, sicher erneut überprüfen.
Wenn mehrere Proxys vorhanden sind (z. B. von verschiedenen ISVs entwickelt), könnte die Verbindung, die von einem Proxy für die Kommunikation mit dem endgültigen Ziel verwendet wird, wiederum von einem zweiten Proxy umgeleitet werden, und diese neue Verbindung kann wiederum vom ursprünglichen Proxy umgeleitet werden.
Ohne Verbindungsnachverfolgung erreicht die ursprüngliche Verbindung möglicherweise nie ihr endgültiges Ziel, da sie in einer Endlosproxyschleife hängen bleibt.

**SIO \_ SET \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS** IOCTL wird verwendet, um eine Proxyverbindungsnachverfolgung für umgeleitete Socketverbindungen bereitzustellen.
Dieses WFP-Feature ermöglicht die Nachverfolgung von Umleitungsdatensätzen von der ersten Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.

Die [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL wird von einem WFP-basierten Umleitungsdienst verwendet, um den Umleitungsdatensatz von der akzeptierten TCP/IP-Paketverbindung (z.B. dem verbundenen Socket für einen TCP-Socket oder einem UDP-Socket) abzurufen, der von seiner begleitenden Kernelmodus-Callout, die auf  **ALE CONNECT \_ \_ REDIRECT-Ebenen** in einem Kernelmodustreiber registriert ist, umgeleitet wird.
Der [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL ruft den Umleitungskontext für einen Umleitungsdatensatz ab, der verwendet wird.
Der Umleitungskontext ist optional und wird verwendet, wenn der aktuelle Umleitungsstatus einer Verbindung ist, dass die Verbindung vom aufrufenden Umleitungsdienst umgeleitet wurde oder die Verbindung zuvor vom aufrufenden Umleitungsdienst umgeleitet wurde, später jedoch erneut von einem anderen Umleitungsdienst umgeleitet wurde. Der Umleitungsdienst überträgt den abgerufenen Umleitungsdatensatz an den TCP-Socket, den er verwendet, um den ursprünglichen Inhalt mithilfe der **SIO \_ SET \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS** IOCTL als Proxy zu verwenden.

Die Anwendung, die die **SIO \_ SET \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS** IOCTL aufruft, muss das Blob, das den festzulegenden Umleitungsdatensatz enthält, nicht verstehen.
Dies ist ein nicht transparentes Datenblob, das die Anwendung an den neuen Socket übergeben muss.

## <a name="see-also"></a>Weitere Informationen

[**IPPROTO_IP Socketoptionen**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
