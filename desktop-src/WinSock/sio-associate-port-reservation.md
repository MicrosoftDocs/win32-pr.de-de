---
description: Der Steuercode verknüpft einen Socket mit einer permanenten oder Lauf Zeit Reservierung für einen TCP-oder UDP-Block, der durch das Port Reservierungs Token identifiziert wird.
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: SIO_ASSOCIATE_PORT_RESERVATION Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 69af4f396fabd32f948d7e43cbf348aa34fb1a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217287"
---
# <a name="sio_associate_port_reservation-control-code"></a>SIO_ASSOCIATE_PORT_RESERVATION Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG

Der Port für die Zuordnung von **\_ Port- \_ \_ Reservierungs** Codes ordnet einen Socket einer permanenten oder Lauf Zeit Reservierung für einen TCP-oder UDP-Block zu, der durch das Port Reservierungs Token identifiziert wird.
Diese IOCTL muss ausgegeben werden, bevor der Socket gebunden ist.
Wenn und wenn der Socket gebunden ist, wird der zugewiesene Port aus der durch das angegebene Token identifizierten Port Reservierung ausgewählt.
Wenn keine Ports aus der angegebenen Reservierung verfügbar sind, schlägt der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktionsaufrufe fehl.

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
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
Verwenden Sie für diesen Vorgang die **\_ \_ Port \_ Reservierung für "sio zuordnen** ".

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter enthält einen Zeiger auf eine [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) Struktur mit dem Token für die TCP-oder UDP-Port Reservierung, die dem Socket zugeordnet werden soll.

### <a name="cbinbuffer"></a>cbinbuffer

Die Größe des Eingabe Puffers in Bytes.
Dieser Parameter muss mindestens die Größe der [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) Struktur aufweisen.

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
|**ausstehende WSA-e/a \_ \_** | Überlappende e/a-Vorgänge werden ausgeführt. Dieser Wert wird zurückgegeben, wenn ein überlappende Vorgang erfolgreich initiiert wurde und die Beendigung zu einem späteren Zeitpunkt angegeben wird. |
| **WSA- \_ Vorgang \_ abgebrochen** | Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen. Dieser Fehler wird zurückgegeben, wenn ein über Lapp ender Vorgang aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush ioctl** " abgebrochen wurde. |
| **WSAEACCES** | Es wurde versucht, auf einen Socket auf eine Weise zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist. Dieser Fehler wird unter mehreren Bedingungen für persistente Port Reservierungen zurückgegeben, die Folgendes umfassen: dem Benutzer fehlen die erforderlichen Administratorrechte auf dem lokalen Computer, oder die Anwendung wird nicht in einer erweiterten Shell als integrierter Administrator ( `RunAs administrator` ) ausgeführt. |
| **WSAEFAULT** | Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt. Dieser Fehler wird zurückgegeben, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer*, *lpcbbytesall*, *lpoverlgetauscht* oder *lpCompletionRoutine* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist. |
| **Wsaeingabe Progress** | Ein Blockierungsvorgang wird momentan ausgeführt. Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird. |
| **Wsaeingabe** | Ein Blockierungs Vorgang wurde durch einen [**wsacancelblockingstatement**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)-Aufrufvorgang unterbrochen. Dieser Fehler wird zurückgegeben, wenn ein Blockierungs Vorgang unterbrochen wurde. |
| **Wsaabval** | Ein ungültiges Argument wurde angegeben. Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode* -Parameter kein gültiger Befehl ist oder wenn ein angegebener Eingabeparameter nicht zulässig ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist. |
| **WSAENETDOWN** | Bei einem Socketvorgang war das Netzwerk inaktiv. Dieser Fehler wird zurückgegeben, wenn das Netzwerk Subsystem fehlgeschlagen ist. |
| **Wsaumotsock** | Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist. Dieser Fehler wird zurückgegeben, wenn es sich bei den *Deskriptoren nicht* um einen Socket handelt. |
| **WSAEOPNOTSUPP** | Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der angegebene ioctl-Befehl nicht unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn die **\_ \_ Port \_ Reservierungs** -ioctl des Zertifikat Anschlusses vom Transportanbieter nicht unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn bei dem Versuch, die IOCTL-ioctl für die **\_ Port- \_ \_ Reservierung** zu verwenden, ein anderer Socket als UDP oder TCP verwendet wird. |

## <a name="remarks"></a>Bemerkungen

Die IOCTL-ioctl für die **\_ Port- \_ \_ Reservierung** wird unter Windows Vista und höheren Versionen des Betriebssystems unterstützt.

Anwendungen und Dienste, die Ports reservieren müssen, lassen sich in zwei Kategorien unterteilen.
Die erste Kategorie umfasst Komponenten, die einen bestimmten Port als Teil Ihres Vorgangs benötigen.
Diese Komponenten bevorzugen in der Regel die Angabe Ihres erforderlichen Ports zur Installationszeit (z. b. in einem Anwendungs Manifest).
Die zweite Kategorie umfasst Komponenten, die zur Laufzeit einen beliebigen verfügbaren Port oder einen beliebigen Port Block benötigen.
Diese beiden Kategorien entsprechen bestimmten Port Reservierungs Anforderungen für und Platzhalter.
Bestimmte Reservierungs Anforderungen sind möglicherweise persistent oder Laufzeit, während reservierte Port Reservierungs Anforderungen nur zur Laufzeit unterstützt werden.

Mithilfe der IOCTL-ioctl-zuordnende **\_ \_ Port \_ Reservierung** wird eine TCP-oder UDP-Port Reservierung entweder mit einer permanenten oder einer Lauf Zeit Reservierung verknüpft.

Die Funktion " [**kreatepersistenttcpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) " oder " [**kreatepersistentudpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) " bietet einer Anwendung oder einem Dienst die Möglichkeit, einen permanenten Block von TCP-oder UDP-Ports zu reservieren.
Persistente Port Reservierungen werden in einem permanenten Speicher für das TCP-oder UDP-Modul in Windows aufgezeichnet.
Beachten Sie, dass sich das Token für eine bestimmte persistente Port Reservierung bei jedem Neustart des Systems ändern kann.

Nachdem eine permanente TCP-oder UDP-Port Reservierung abgerufen wurde, kann eine Anwendung Port Zuweisungen von der Port Reservierung anfordern, indem Sie einen TCP-oder UDP-Socket öffnet und anschließend die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -Funktion aufruft, indem Sie die IOCTL-ioctl für die Port **\_ \_ \_ Reservierung** der Zertifizierungsstelle angibt und das Reservierungs Token vor dem Ausgeben eines Aufrufs an die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion

Der [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl kann verwendet werden, um eine Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports anzufordern.
Bei Lauf Zeit Port Reservierungen erfordert der Port Pool, dass Reservierungen von dem Prozess verarbeitet werden, dessen Socket die Reservierung gewährt wurde.
Lauf Zeit Port Reservierungen dauern nur so lange, wie die Lebensdauer des Sockets, auf dem die [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl aufgerufen wurde.
Im Gegensatz dazu können persistente Port Reservierungen, die mithilfe der Funktion " [**kreatepersistenttcpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) " oder " [**kreatepersistentudpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) " erstellt wurden, von jedem Prozess genutzt werden, der über die Möglichkeit zum Abrufen dauerhafter Reservierungen verfügt.

Sobald eine TCP-oder UDP-Port Reservierung für die Laufzeit abgerufen wurde, kann eine Anwendung Port Zuweisungen von der Port Reservierung anfordern, indem Sie einen TCP-oder UDP-Socket öffnet und anschließend die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -Funktion aufruft, die die IOCTL-ioctl-IOCTL- **\_ \_ \_ typreservierung** angibt und vor dem Ausgeben eines Aufrufs an die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion des Sockets

Wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* NULL sind, wird der Socket in dieser Funktion als nicht überlappenden Socket behandelt.
Bei einem nicht überlappenden Socket werden die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* ignoriert, mit der Ausnahme, dass die Funktion blockiert werden kann, wenn sich Socket *s* im Blockierungs Modus befindet.
Wenn sich Socket *s* im nicht blockierenden Modus befindet, wird diese Funktion immer noch blockiert, da diese spezielle ioctl den nicht blockierenden Modus nicht unterstützt.

Bei überlappenden Sockets werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.

Alle ioctl können unbegrenzt blockieren, abhängig von der Implementierung des Dienstanbieters.
Wenn die Anwendung die Blockierung in einem [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktions aufrufnis nicht tolerieren kann, werden überlappende e/a-Vorgänge für IOCTLs empfohlen, die besonders wahrscheinlich blockiert werden.

In den folgenden Fällen kann die IOCTL-ioctl für die Karte " **\_ \_ Port \_ Reservierung** " mit **WSAEINTR** oder **WSA_OPERATION_ABORTED** fehlschlagen:

* Die Anforderung wird vom e/a-Manager abgebrochen.
* Der Socket ist geschlossen.

Die für eine permanente Port Reservierung an die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** weiter gegebene **\_ \_ Port \_ Reservierungs** -ioctl kann nur in einer Anwendung verwendet werden, wenn der Benutzer als Mitglied der Gruppe "Administratoren" angemeldet ist.
Wenn in einer Anwendung eine IOCTL- **\_ \_ Port \_ Reservierung** verwendet wird, wenn der Benutzer kein Mitglied der Gruppe "Administratoren" ist, schlägt der Funktionsaufrufe fehl, und es wird **WSAEACCES** zurückgegeben.
Die Verwendung der IOCTL-ioctl-zuordnende **\_ \_ Port \_ Reservierung** kann auch aufgrund der Benutzerkontensteuerung (User Account Control, UAC) unter Windows Vista und höher fehlschlagen.
Wenn eine Anwendung, die diese IOCTL mit einer permanenten Port Reservierung verwendet, von einem Benutzer ausgeführt wird, der nicht als integrierter Administrator, sondern als Mitglied der Gruppe "Administratoren" angemeldet ist, schlägt dieser Vorgang fehl, es sei denn, die Anwendung wurde in der Manifest-Datei mit einem **requestedExecutionLevel** auf " *requisorministrator*" festgelegt.
Wenn in der Anwendung diese Manifestressource fehlt, muss ein Benutzer, der als Mitglied der Gruppe "Administratoren" angemeldet ist, nicht der integrierte Administrator, sondern die Anwendung in einer erweiterten Shell als integrierter Administrator () ausführen, damit `RunAs administrator` Diese Funktion erfolgreich ausgeführt werden kann.

## <a name="see-also"></a>Siehe auch

[**Zwick**](/windows/desktop/api/winsock/nf-winsock-bind)

[**"Kreatepersistenttcpportreservation"**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**"Kreatepersistentudpportreservation"**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**Deletepersistenttcpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**Deletepersistentudpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[**Lookuppersistenttcpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**Lookuppersistentudpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md)

[**SIO_RELEASE_PORT_RESERVATION**](sio-release-port-reservation.md)

[Glühbirne](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
