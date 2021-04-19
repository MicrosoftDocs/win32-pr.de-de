---
description: Der Steuerungs Code erhält eine Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports.
ms.assetid: 1A2E3920-88D2-4109-B7EF-E66BD4AB6153
title: SIO_ACQUIRE_PORT_RESERVATION Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8eab53aeb945837b55c70560294b2fc295160a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347917"
---
# <a name="sio_acquire_port_reservation-control-code"></a>SIO_ACQUIRE_PORT_RESERVATION Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG

Der Konfigurations Code für die **\_ Port- \_ \_ Reservierungs** Steuerung von SIO erhält eine Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports.

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to an INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to a INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
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
Verwenden Sie für diesen Vorgang die **\_ \_ Port \_ Reservierung**  von "sio abrufen".

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter enthält einen Zeiger auf eine [**inet- \_ Port \_ Bereichs**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) Struktur, die die Startpunkt Nummer und die Anzahl der zu reservierenden Ports angibt.

### <a name="cbinbuffer"></a>cbinbuffer

Die Größe des Eingabe Puffers in Bytes.
Dieser Parameter sollte die Größe der inet- [**\_ Port \_ Bereichs**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) Struktur sein.

### <a name="lpvoutbuffer"></a>lpvoutbuffer

Ein Zeiger auf den Ausgabepuffer.
Bei erfolgreicher Ausgabe enthält dieser Parameter einen Zeiger auf eine [**inet- \_ Port- \_ Reservierungs \_ Instanzstruktur**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .

### <a name="cboutbuffer"></a>cboutbuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter muss mindestens die Größe der [**inet \_ Port- \_ Reservierungs \_ Instanzstruktur**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) aufweisen.

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

Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden **wpuqueueapc**-Rückruf verwendet werden soll.
Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die **wpuqueueapc** -Funktion zurückgibt.

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
| **WSA- \_ Vorgang \_ abgebrochen** | Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen. Dieser Fehler wird zurückgegeben, wenn ein über Lapp ender Vorgang aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen wurde. |
| **WSAEFAULT** | Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt. Dieser Fehler wird zurückgegeben, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer*, *lpcbbytesall*, *lpoverlgetauscht* oder *lpCompletionRoutine* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist. |
| **Wsaeingabe Progress** | Ein Blockierungsvorgang wird momentan ausgeführt. Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird. |
| **Wsaeingabe** | Ein Blockierungs Vorgang wurde durch einen [**wsacancelblockingstatement**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)-Aufrufvorgang unterbrochen. Dieser Fehler wird zurückgegeben, wenn ein Blockierungs Vorgang unterbrochen wurde. |
| **Wsaabval** | Ein ungültiges Argument wurde angegeben. Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode* -Parameter kein gültiger Befehl ist oder wenn ein angegebener Eingabeparameter nicht zulässig ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist. |
| **WSAENETDOWN** | Bei einem Socketvorgang war das Netzwerk inaktiv. Dieser Fehler wird zurückgegeben, wenn das Netzwerk Subsystem fehlgeschlagen ist. |
| **Wsaumotsock** | Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist. Dieser Fehler wird zurückgegeben, wenn es sich bei den *Deskriptoren nicht* um einen Socket handelt. |
| **WSAEOPNOTSUPP** | Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der angegebene ioctl-Befehl nicht unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn die IOCTL-ioctl zum Abrufen des Zertifikat **\_ \_ Anschlusses \_** vom Transportanbieter nicht unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn bei dem Versuch, die IOCTL für den Zertifikat **\_ \_ erstellungsport \_** zu verwenden, ein anderer Socket als UDP oder TCP verwendet wird. |

## <a name="remarks"></a>Bemerkungen

Die IOCTL- **\_ \_ \_ reservierte**  ioctl des Zertifikat Erstellungs Ports wird unter Windows Vista und höheren Versionen des Betriebssystems unterstützt.

Anwendungen und Dienste, die Ports reservieren müssen, lassen sich in zwei Kategorien unterteilen.
Die erste Kategorie umfasst Komponenten, die einen bestimmten Port als Teil Ihres Vorgangs benötigen.
Diese Komponenten bevorzugen in der Regel die Angabe Ihres erforderlichen Ports zur Installationszeit (z. b. in einem Anwendungs Manifest).
Die zweite Kategorie umfasst Komponenten, die zur Laufzeit einen beliebigen verfügbaren Port oder einen beliebigen Port Block benötigen.
Diese beiden Kategorien entsprechen bestimmten Port Reservierungs Anforderungen für und Platzhalter.
Bestimmte Reservierungs Anforderungen sind möglicherweise persistent oder Laufzeit, während reservierte Port Reservierungs Anforderungen nur zur Laufzeit unterstützt werden.

Die IOCTL- **\_ \_ \_ reservierte**  ioctl-Anforderung zum Abrufen einer Lauf Zeit Reservierung wird für einen Block von TCP-oder UDP-Ports verwendet.
Bei Lauf Zeit Port Reservierungen erfordert der Port Pool, dass Reservierungen von dem Prozess verarbeitet werden, dessen Socket die Reservierung gewährt wurde.
Lauf Zeit Port Reservierungen dauern nur so lange, wie die Lebensdauer des Sockets, auf dem die IOCTL-ioctl-Reservierung für den Zertifikat Abruf **\_ \_ \_ reserviert**  wurde.
Im Gegensatz dazu können persistente Port Reservierungen, die mithilfe der Funktion " [**kreatepersistenttcpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) " oder " [**kreatepersistentudpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) " erstellt wurden, von jedem Prozess genutzt werden, der über die Möglichkeit zum Abrufen dauerhafter Reservierungen verfügt.

Sobald eine TCP-oder UDP-Port Reservierung für die Laufzeit abgerufen wurde, kann eine Anwendung Port Zuweisungen von der Port Reservierung anfordern, indem Sie einen TCP-oder UDP-Socket öffnet und anschließend die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -Funktion aufruft, die die IOCTL-ioctl-IOCTL- [**\_ \_ \_ typreservierung**](sio-associate-port-reservation.md) angibt und vor dem Ausgeben eines Aufrufs an die Bind-Funktion des Sockets

Wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* **null** sind, wird der Socket in dieser Funktion als nicht überlappenden Socket behandelt.
Bei einem nicht überlappenden Socket werden die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* ignoriert, mit der Ausnahme, dass die Funktion blockiert werden kann, wenn sich Socket *s* im Blockierungs Modus befindet.
Wenn sich Socket *s* im nicht blockierenden Modus befindet, wird diese Funktion immer noch blockiert, da diese spezielle ioctl den nicht blockierenden Modus nicht unterstützt.

Bei überlappenden Sockets werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.

Alle ioctl können unbegrenzt blockieren, abhängig von der Implementierung des Dienstanbieters.
Wenn die Anwendung die Blockierung in einem WSAIoctl-oder **wspioctl** -Funktions aufrufnis nicht tolerieren kann, werden überlappende e/a-Vorgänge für IOCTLs empfohlen, die besonders wahrscheinlich blockiert werden.

**In den** folgenden Fällen kann die IOCTL- **\_ \_ \_ Reservierungs** -ioctl für die RSA-Abruf Vorgänge fehlschlagen: **\_ \_**

* Die Anforderung wird vom e/a-Manager abgebrochen.
* Der Socket ist geschlossen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Lauf Zeit Port Reservierung angefordert, anschließend wird ein Socket erstellt und ein Port aus der Lauf Zeit Port Reservierung für den Socket zugewiesen. Anschließend wird der Socket geschlossen, und die Lauf Zeit Port Reservierung wird aufgehoben.

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Note that the sockaddr_in struct works only with AF_INET not AF_INET6
    // An application needs to use the sockaddr_in6 for AF_INET6
    sockaddr_in service;
    sockaddr_in sockName;
    int nameLen = sizeof (sockName);

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            sockRes = socket(iFamily, iType, iProtocol);
            if (sockRes == INVALID_SOCKET) {
                wprintf(L"socket function for second socket failed with error = %d\n",
                        WSAGetLastError());
                closesocket(sock);
                WSACleanup();
                return 1;
            } else {
                wprintf(L"socket function for second socket succeeded\n");

                iResult =
                    WSAIoctl(sock, SIO_ASSOCIATE_PORT_RESERVATION,
                             (LPVOID) & portRes.Token, sizeof (ULONG64), NULL, 0,
                             &bytesReturned, NULL, NULL);
                if (iResult != 0) {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) failed with error = %d\n",
                         WSAGetLastError());
                } else {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                         bytesReturned);

                    service.sin_family = (ADDRESS_FAMILY) iFamily;
                    service.sin_addr.s_addr = INADDR_ANY;
                    service.sin_port = 0;

                    iResult = bind(sock, (SOCKADDR *) & service, sizeof (service));
                    if (iResult == SOCKET_ERROR)
                        wprintf(L"bind failed with error = %d\n", WSAGetLastError());
                    else {
                        wprintf(L"bind succeeded\n");
                        iResult = getsockname(sock, (SOCKADDR *) & sockName, &nameLen);
                        if (iResult == SOCKET_ERROR)
                            wprintf(L"getsockname failed with error = %d\n",
                                    WSAGetLastError());
                        else {
                            wprintf(L"getsockname succeeded\n");
                            wprintf(L"Port number allocated = %u\n",
                                    ntohs(sockName.sin_port));
                        }
                    }
                }
            }

            // comment out this block of code if you don't want to delete the reservation just created
            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sockRes != INVALID_SOCKET) {
            iResult = closesocket(sockRes);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for second socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a>Siehe auch

[**erst**](/windows/desktop/api/winsock2/nf-winsock2-accept)

[**Zwick**](/windows/desktop/api/winsock/nf-winsock-bind)

[**"Kreatepersistenttcpportreservation"**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**"Kreatepersistentudpportreservation"**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**Deletepersistenttcpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**Deletepersistentudpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET- \_ Port \_ Bereich**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range)

[**INET- \_ Port \_ Reservierungs \_ Instanz**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance)

[**Lookuppersistenttcpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**Lookuppersistentudpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**\_Zuordnen der \_ Port \_ Reservierung**](sio-associate-port-reservation.md)

[**\_ \_ Port \_ Reservierung für den SIO-Release**](sio-release-port-reservation.md)

[**Glühbirne**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
