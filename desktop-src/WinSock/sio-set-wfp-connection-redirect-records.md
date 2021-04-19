---
description: Steuerungs Code legt den Umleitungs Daten Satz auf den neuen TCP-Socket fest, der zum Verbinden des Umleitungs dienstan
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS-Steuerungscode
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364108"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a>SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS-Steuerungscode

## <a name="description"></a>BESCHREIBUNG

Der Code für die **\_ \_ WFP- \_ \_ verbindungsumleitungs- \_ Datensätze der WFP-Verbindung** legt den Umleitungs Daten Satz auf den neuen TCP-Socket fest, der zum Herstellen der Verbindung mit dem endgültigen Ziel verwendet wird, um von einem Windows-Filter Plattform

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

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

Der Steuerelement Code für den Vorgang.
Verwenden Sie für diesen Vorgang die **\_ \_ \_ Verbindungs \_ \_ Datensätze der WFP-Verbindung** mit der

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter enthält einen Zeiger auf den dem Socket zugeordneten WFP-Umleitungs Daten Satz.

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
| **ausstehende WSA-e/a \_ \_** | Überlappende e/a-Vorgänge werden ausgeführt. Dieser Wert wird zurückgegeben, wenn ein überlappende Vorgang erfolgreich initiiert wurde und die Beendigung zu einem späteren Zeitpunkt angegeben wird. |
| **WSA- \_ Vorgang \_ abgebrochen** | Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen. Dieser Fehler wird zurückgegeben, wenn ein über Lapp ender Vorgang aufgrund der Schließung des Sockets oder der Ausführung des **SIO_FLUSH** ioctl-Befehls abgebrochen wurde. |
| **WSAEACCES** | Es wurde versucht, auf einen Socket auf eine Weise zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist. Dieser Fehler wird unter mehreren Bedingungen zurückgegeben, die Folgendes umfassen: dem Benutzer fehlen die erforderlichen Administratorrechte auf dem lokalen Computer, oder die Anwendung wird nicht in einer erweiterten Shell als integrierter Administrator () ausgeführt `RunAs administrator` . |
| **WSAEFAULT** | Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt. Dieser Fehler wird zurückgegeben, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer*, *lpcbbytesall*, *lpoverlgetauscht* oder *lpCompletionRoutine* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist. |
| **Wsaeingabe Progress** | Ein Blockierungsvorgang wird momentan ausgeführt. Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird. |
| **Wsaeingabe** | Ein Blockierungs Vorgang wurde durch einen **wsacancelblockingstatement**-Aufrufvorgang unterbrochen. Dieser Fehler wird zurückgegeben, wenn ein Blockierungs Vorgang unterbrochen wurde. |
| **Wsaabval** | Ein ungültiges Argument wurde angegeben. Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode* -Parameter kein gültiger Befehl ist oder wenn ein angegebener Eingabeparameter nicht zulässig ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist. |
| **WSAENETDOWN** | Bei einem Socketvorgang war das Netzwerk inaktiv. Dieser Fehler wird zurückgegeben, wenn das Netzwerk Subsystem fehlgeschlagen ist. |
| **Wsaumotsock** | Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist. Dieser Fehler wird zurückgegeben, wenn es sich bei den *Deskriptoren nicht* um einen Socket handelt. |
| **WSAEOPNOTSUPP** | Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der angegebene ioctl-Befehl nicht unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn die **\_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung** von der Gruppe "ioctl" vom Transportanbieter nicht unterstützt werden. |

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung** werden von Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.

WFP ermöglicht den Zugriff auf den TCP/IP-Paket Verarbeitungs Pfad, in dem ausgehende und eingehende Pakete überprüft oder geändert werden können, bevor Sie weiterverarbeitet werden können.
Durch das Tippen auf den TCP/IP-Verarbeitungs Pfad können unabhängige Softwarehersteller (ISVs) leichter Firewalls, Antivirussoftware, Diagnosesoftware und andere Arten von Anwendungen und Diensten erstellen.
WFP stellt Komponenten im Benutzermodus und im Kernel Modus bereit, sodass Drittanbieter-ISVs an den Filter Entscheidungen teilnehmen können, die auf mehreren Ebenen im TCP/IP-Protokollstapel und im gesamten Betriebssystem stattfinden.
Mithilfe des WFP-Verbindungs Umleitungs Features kann ein WFP-Legenden-Kernel-Treiber eine Verbindung lokal an einen Benutzermodusprozess umleiten, eine Inhalts Untersuchung im Benutzermodus durchführen und den überprüften Inhalt mithilfe einer anderen Verbindung zum ursprünglichen Ziel weiterleiten.

Die **Datensätze der WFP-Verbindungs Umleitung werden von der Datei "ioctl" und mehrere andere verwandte IOCTLs- \_ \_ \_ \_ \_ Datensätze erfasst** . Diese werden verwendet, um mehreren WFP-basierten Verbindungs Proxy Anwendungen zu ermöglichen, denselben Daten Verkehrsfluss auf kooperative Weise zu überprüfen.
Jeder Inspektions Agent kann den Netzwerk Datenverkehr, der bereits von einem anderen Inspektions Agent überprüft wurde, sicher erneut überprüfen.
Durch das vorhanden sein mehrerer Proxys (z. b. durch verschiedene ISVs) kann die Verbindung, die von einem Proxy für die Kommunikation mit dem endgültigen Ziel verwendet wird, wiederum von einem zweiten Proxy umgeleitet werden, und diese neue Verbindung kann erneut vom ursprünglichen Proxy umgeleitet werden.
Ohne Verbindungs Nachverfolgung erreicht die ursprüngliche Verbindung möglicherweise nie das endgültige Ziel, weil Sie in einer unendlichen Proxy Schleife hängen bleibt.

Die **\_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung** in der Gruppe "ioctl" werden mithilfe von "ioctl" für die Verbindungs Protokollierung über umgeleitet
Diese WFP-Funktion ermöglicht das Nachverfolgen von Umleitungs Datensätzen von der anfänglichen Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.

Der [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL wird von einem WFP-basierten Umleitungs Dienst verwendet, um den Umleitungs Daten Satz von der akzeptierten TCP/IP-Paket Verbindung abzurufen (z. b. den verbundenen Socket für einen TCP-Socket oder einen UDP-Socket), der durch seine begleitende kernelmoduslegende, die bei der  **ALE \_ Connect- \_ Umleitungs** Schicht in einem Kernelmodustreiber
Der [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) ioctl Ruft den Umleitungs Kontext für einen Umleitungs Daten Satz ab, der verwendet wird.
Der Umleitungs Kontext ist optional und wird verwendet, wenn der aktuelle Umleitungs Status einer Verbindung darin besteht, dass die Verbindung vom aufrufenden Umleitungs Dienst umgeleitet wurde oder die Verbindung zuvor vom aufrufenden Umleitungs Dienst umgeleitet, aber später von einem anderen Umleitungs Dienst umgeleitet wurde. Der Umleitungs Dienst überträgt den abgerufenen Umleitungs Daten Satz an den TCP-Socket, den er zum Proxy des ursprünglichen Inhalts verwendet, indem er die IOCTL- **\_ \_ \_ Verbindungs \_ \_ Datensätze der WFP-Verbindung** verwendet

Die Anwendung, die **die \_ \_ \_ \_ \_ Datensätze für die WFP-Verbindungs Umleitung des Daten** Satzes "moctl" aufrufen, muss das BLOB mit dem festgelegten Umleitungs Daten Satz nicht verstehen.
Hierbei handelt es sich um ein nicht transparentes BLOB von Daten, die die Anwendung an den neuen Socket zurückgeben muss.

## <a name="see-also"></a>Siehe auch

[**IPPROTO_IP Socketoptionen**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**Glühbirne**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
