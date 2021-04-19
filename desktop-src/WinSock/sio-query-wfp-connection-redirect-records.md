---
description: Der Steuerungs Code Ruft den Umleitungs Daten Satz für die akzeptierte TCP/IP-Verbindung für die Verwendung durch einen Windows-Filter Plattform-Umleitungs Dienst ab.
ms.assetid: E0D7CC1A-8F93-45A0-9543-3F2ACAF352F5
title: SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 2389914d29bd403a33e23065c29f549a01adbb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347895"
---
# <a name="sio_query_wfp_connection_redirect_records-control-code"></a>SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG

Der Verwaltungs Code für die **\_ \_ WFP- \_ \_ verbindungsumleitungs- \_ Datensätze** der zentrale Abfrage ruft den Umleitungs Daten Satz für die akzeptierte TCP/IP-Verbindung für die Verwendung durch einen WFP-Umleitungs Dienst (Windows Filtering Platform

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
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
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a>Parameter

### <a name="s"></a>s

Ein Deskriptor, der einen Socket identifiziert.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Der Steuerelement Code für den Vorgang.
Verwenden Sie für diesen Vorgang die **\_ \_ WFP- \_ Verbindungs \_ \_ Einträge für die WFP-Abfrage** .

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
| **WSA_IO_PENDING** | Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben. |
| **WSA_OPERATION_ABORTED** | Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des **SIO_FLUSH** ioctl-Befehls abgebrochen. |
| **WSAEFAULT** | Der Parameter " *lpvoutbuffer*", " *lpcbbytesis*", " *lpoverlgetauscht*" oder " *lpCompletionRoutine* " ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten. |
| **Wsaeingabe Progress** | Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird. |
| **Wsaeingabe** | Ein Blockierungs Vorgang wurde unterbrochen. |
| **Wsaabval** | Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar. Dieser Fehler wird zurückgegeben, wenn der *cboutbuffer* -Parameter kleiner als die Größe eines **ulong** -Datentyps ist. |
| **WSAENETDOWN** | Das Netzwerk Subsystem ist fehlgeschlagen. |
| **Wsaumoproumopt** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **WSAENOTCONN** | Die Socket *s* ist nicht verbunden. |
| **Wsaumotsock** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene ioctl-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn die **\_ Abfrage der \_ WFP-Verbindungs Umleitung für den \_ \_ \_ Daten bankverbindungs** -Datensatz ioctl vom Transportanbieter nicht unterstützt wird. |

## <a name="remarks"></a>Bemerkungen

Die **Konfigurations \_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung** werden von Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.

WFP ermöglicht den Zugriff auf den TCP/IP-Paket Verarbeitungs Pfad, in dem ausgehende und eingehende Pakete überprüft oder geändert werden können, bevor Sie weiterverarbeitet werden können.
Durch das Tippen auf den TCP/IP-Verarbeitungs Pfad können unabhängige Softwarehersteller (ISVs) leichter Firewalls, Antivirussoftware, Diagnosesoftware und andere Arten von Anwendungen und Diensten erstellen.
WFP stellt Komponenten im Benutzermodus und im Kernel Modus bereit, sodass Drittanbieter-ISVs an den Filter Entscheidungen teilnehmen können, die auf mehreren Ebenen im TCP/IP-Protokollstapel und im gesamten Betriebssystem stattfinden.
Mithilfe des WFP-Verbindungs Umleitungs Features kann ein WFP-Legenden-Kernel-Treiber eine Verbindung lokal an einen Benutzermodusprozess umleiten, eine Inhalts Untersuchung im Benutzermodus durchführen und den überprüften Inhalt mithilfe einer anderen Verbindung zum ursprünglichen Ziel weiterleiten.

Bei der Verbindung mit der **\_ \_ WFP-Verbindungs \_ Umleitung \_ \_** für die zentral Abfrage werden ioctl und mehrere andere verwandte IOCTLs-Datensätze im benutzermodusbereich verwendet, damit mehrere WFP-basierte Verbindungs Proxy Anwendungen den gleichen Daten Verkehrsfluss auf kooperative Weise überprüfen können.
Jeder Inspektions Agent kann den Netzwerk Datenverkehr, der bereits von einem anderen Inspektions Agent überprüft wurde, sicher erneut überprüfen.
Durch das vorhanden sein mehrerer Proxys (z. b. durch verschiedene ISVs) kann die Verbindung, die von einem Proxy für die Kommunikation mit dem endgültigen Ziel verwendet wird, wiederum von einem zweiten Proxy umgeleitet werden, und diese neue Verbindung kann erneut vom ursprünglichen Proxy umgeleitet werden.
Ohne Verbindungs Nachverfolgung erreicht die ursprüngliche Verbindung möglicherweise nie das endgültige Ziel, weil Sie in einer unendlichen Proxy Schleife hängen bleibt.

Die **\_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung** mit der Datenbank ". ioctl" werden verwendet, um eine Proxy Verbindung für umgeleitete Socketverbindungen herzustellen.
Diese WFP-Funktion ermöglicht das Nachverfolgen von Umleitungs Datensätzen von der anfänglichen Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.

Die **\_ Abfrage Datensätze für die WFP-Verbindung mit der Leistungs \_ \_ \_ \_ Datensätze** ". ioctl" wird von einem WFP-basierten Umleitungs Dienst verwendet, um den Umleitungs Daten Satz von der akzeptierten TCP/IP-Paket Verbindung (z. b. den verbundenen Socket für einen TCP-Socket oder einen UDP-Socket **ALE_CONNECT_REDIRECT** ) abzurufen
Der **\_ \_ \_ Verbindungs \_ Umleitungs \_ Kontext** ioctl für die WFP-Abfrage wird von einem WFP-basierten Umleitungs Dienst verwendet, um den Umleitungs Kontext für einen Umleitungs Daten Satz von der akzeptierten TCP/IP-Paket Verbindung (z. b. den verbundenen Socket für einen TCP-Socket oder einen UDP-Socket **) \_ \_** abzurufen
Der Umleitungs Kontext ist ein optionaler vom Treiber zugewiesener Kontext, der verwendet wird, wenn der aktuelle Umleitungs Status einer Verbindung darin besteht, dass die Verbindung vom aufrufenden Umleitungs Dienst umgeleitet wurde oder die Verbindung zuvor durch den aufrufenden Umleitungs Dienst umgeleitet, aber später von einem anderen Umleitungs Dienst umgeleitet wurde.
Bei einer TCP-Proxy Verbindung überträgt der Umleitungs Dienst den abgerufenen Umleitungs Daten Satz an den TCP-Socket, der zum Proxy des ursprünglichen Inhalts verwendet wird, indem er die IOCTL- **\_ \_ \_ Verbindungs \_ \_ Datensätze der WFP-Verbindung** verwendet.

Wenn der Umleitungs Dienst einen nicht-TCP-Socket umleitet (z. b. UDP), wird durch die von der Leistungsindikator- **\_ \_ WFP- \_ Verbindungs \_ Umleitung \_** zurückgegebenen Umleitungs Datensätze ioctl darauf hingewiesen, dass die [**wsamsg**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) -Struktur mit der Funktion [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) verwendet wird.
Das Steuerelementmember der [**wsamsg**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) -Struktur hätte eine cmsg_type in der **wsacmsghdr** -Struktur, die auf den **\_ \_ Umleitungs \_ Daten Satz der IP-Verbindung** festgelegt ist.
Der [**LPFN_WSARECVMSG Parameter (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) muss vom Umleitungs Dienst bereitgestellt werden, wenn nicht-TCP-Umleitungen akzeptiert werden.

Bei nicht-TCP-Datenverkehr wird der Umleitungs Daten Satz mithilfe der [**wsamsg**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) -Struktur mit der [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Funktion weitergeleitet.

Beachten Sie, dass für nicht-TCP-Datenverkehr nur das Flow-Erfassungs Paket den **Datensatz der IP- \_ Verbindungs \_ Umleitung \_** enthält.
Folglich muss nur das erste Proxy Paket diese Informationen mithilfe der [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion einschließen.

Da der WFP-Umleitungs Daten Satz ein Daten-BLOB mit variabler Länge ist, kann der Aufrufer entweder einen großen Ausgabepuffer (z. b. einen 1.024-Byte-Puffer, auf den der *lpvoutbuffer* -Parameter zeigt) bereitstellen oder eine Ausgabepuffergröße im *cboutbuffer* -Parameter von 0 übergeben, um die Puffergröße abzufragen, die für das
Wenn die Ausgabepuffergröße nicht ausreichend ist, um die Daten zu speichern, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion den **Fehler "Fehler \_ unzureichend \_** " zurück, und die erforderliche Puffergröße wird als Wert zurückgegeben, auf den der *lpcbbytesreturn* -Parameter verweist.

Die Anwendung, die den [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) aufrufen, muss das BLOB, das den abgerufenen Umleitungs Kontext enthält, nicht verstehen.
Dies ist ein undurchsichtiges BLOB von Daten, das die Anwendung abrufen und an den neuen Socket zurückgeben muss.

## <a name="see-also"></a>Siehe auch

[**IPPROTO_IP Socketoptionen**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**Glühbirne**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsamsg**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

[**Wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
