---
description: Steuerungscode gibt eine Laufzeitreservierung für einen Block von TCP- oder UDP-Ports frei.
ms.assetid: 24D67A40-8CE9-4AF1-90BF-599D19C87B89
title: SIO_RELEASE_PORT_RESERVATION-Steuerelementcode
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8d949e325292210ec7126da5ddf65c6ff30c5aa151cfaf85331fb7ebf3e5b346
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097490"
---
# <a name="sio_release_port_reservation-control-code"></a>SIO_RELEASE_PORT_RESERVATION-Steuerelementcode

## <a name="description"></a>BESCHREIBUNG

Der **SIO \_ RELEASE PORT \_ \_ RESERVATION-Steuerungscode** gibt eine Laufzeitreservierung für einen Block von TCP- oder UDP-Ports frei.
Die laufzeitreservierung, die freigegeben werden soll, muss [](sio-acquire-port-reservation.md) vom ausstellenden Prozess mithilfe der SIO_ACQUIRE_PORT_RESERVATION IOCTL erhalten worden sein.

Um diesen Vorgang durchzuführen, rufen Sie die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** mit den folgenden Parametern auf.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
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
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
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

Der Steuerungscode für den Vorgang.
Verwenden **Sie SIO \_ RELEASE PORT \_ \_ RESERVATION** für diesen Vorgang.

### <a name="lpvinbuffer"></a>lpvInBuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter enthält einen [](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) Zeiger auf eine INET_PORT_RESERVATION_TOKEN-Struktur mit dem Token für die Freigabe der TCP- oder UDP-Portreservierung.

### <a name="cbinbuffer"></a>cbInBuffer

Die Größe des Eingabepuffers in Bytes.
Dieser Parameter muss mindestens die Größe der [**-Struktur**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) INET_PORT_RESERVATION_TOKEN haben.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cboutbuffer"></a>cbOutBuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter muss auf 0 (null) festgelegt werden.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten in Bytes empfängt.

Wenn der Ausgabepuffer zu klein ist, schlägt der Aufruf fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbBytesReturned-Parameter* zeigt auf den **DWORD-Wert** 0 (null).

Wenn *lpOverlapped* **NULL ist,** darf der **DWORD-Wert,** auf den der *lpcbBytesReturned-Parameter* verweist, der bei einem erfolgreichen Aufruf zurückgegeben wird, nicht 0 (null) sein.

Wenn der *lpOverlapped-Parameter* für überlappende Sockets nicht **NULL** ist, werden Vorgänge initiiert, die nicht sofort abgeschlossen werden können, und der Abschluss wird zu einem späteren Zeitpunkt angezeigt.
Der **DWORD-Wert,** auf den der *zurückgegebene lpcbBytesReturned-Parameter* verweist, kann 0 (null) sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen ist.
Der endgültige Abschlussstatus kann abgerufen werden, wenn die entsprechende Abschlussmethode signalisiert wird, wenn der Vorgang abgeschlossen wurde.

### <a name="lpvoverlapped"></a>lpvOverlapped

Ein Zeiger auf eine [**WSAOVERLAPPED-Struktur.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Wenn *Sockets ohne* das überlappende Attribut erstellt wurden, wird *der lpOverlapped-Parameter* ignoriert.

Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpOverlapped-Parameter* nicht **NULL** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.
In diesem Fall muss *der lpOverlapped-Parameter* auf eine gültige [**WSAOVERLAPPED-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) verweisen.

Bei überlappenden Vorgängen wird die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** sofort zurückgegeben, und die entsprechende Abschlussmethode wird signalisiert, wenn der Vorgang abgeschlossen wurde.
Andernfalls gibt die Funktion erst dann zurück, wenn der Vorgang abgeschlossen wurde oder ein Fehler auftritt.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Ein Zeiger auf die Abschlussroutine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).

### <a name="lpthreadid"></a>lpThreadId

Ein Zeiger auf eine [**WSATHREADID-Struktur,**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) die vom Anbieter in einem nachfolgenden Aufruf von [**WPUQueueApc verwendet werden soll.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)
Der Anbieter sollte die [**referenzierte WSATHREADID-Struktur**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) (nicht den Zeiger auf dieselbe) speichern, bis die [**WPUQueueApc-Funktion**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) zurückgegeben wurde.

**Hinweis:**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**

### <a name="lperrno"></a>lpErrno

Ein Zeiger auf den Fehlercode.

**Hinweis:**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** **SOCKET ERROR \_ zurück.**
Um erweiterte Fehlerinformationen zu erhalten, rufen [**Sie WSAGetLastError auf.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

| Fehlercode | Bedeutung |
|------------|---------|
| **AUSSTEHENDE \_ \_ WSA-E/A** | Überlappende E/A-Operation wird durchgeführt. Dieser Wert wird zurückgegeben, wenn ein überlappende Vorgang erfolgreich initiiert wurde und der Abschluss zu einem späteren Zeitpunkt angezeigt wird. |
| **\_WSA-VORGANG \_ ABGEBROCHEN** | Der E/A-Vorgang wurde aufgrund eines Thread-Exits oder einer Anwendungsanforderung abgebrochen. Dieser Fehler wird zurückgegeben, wenn ein überlappende Vorgang aufgrund des Schließens des Sockets oder der Ausführung des IOCTL-Befehls SIO_FLUSH **abgebrochen** wurde. |
| **WSAEFAULT** | Das System hat beim Versuch, ein Zeigerargument in einem Aufruf zu verwenden, eine ungültige Zeigeradresse erkannt. Dieser Fehler wird zurückgegeben, wenn der *lpOverlapped-* oder *lpCompletionRoutine-Parameter* nicht vollständig in einem gültigen Teil des Benutzeradrenraums enthalten ist. |
| **WSAEINPROGRESS** | Ein Blockierungsvorgang wird momentan ausgeführt. Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf in Bearbeitung ist. |
| **WSAEINTR** | Ein blockierende Vorgang wurde durch einen Aufruf von **WSACancelBlockingCall unterbrochen.** Dieser Fehler wird zurückgegeben, wenn ein blockierende Vorgang unterbrochen wurde. |
| **WSAEINVAL** | Ein ungültiges Argument wurde angegeben. Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode-Parameter* kein gültiger Befehl ist, ein angegebener Eingabeparameter nicht akzeptabel ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist. |
| **WSAENETDOWN** | Bei einem Socketvorgang war das Netzwerk inaktiv. Dieser Fehler wird zurückgegeben, wenn beim Netzwerksubsystem ein Fehler aufgetreten ist. |
| **WSAENOTSOCK** | Es wurde versucht, einen Vorgang für etwas zu unternehmen, das kein Socket ist. Dieser Fehler wird zurückgegeben, wenn der Deskriptor *s* kein Socket ist. |
| **WSAEOPNOTSUPP** | Der versuchte Vorgang wird für den Objekttyp, auf den verwiesen wird, nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der angegebene IOCTL-Befehl nicht unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn **die SIO \_ RELEASE PORT \_ \_ RESERVATION** IOCTL vom Transportanbieter nicht unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn versucht wird, die **SIO \_ RELEASE PORT \_ \_ RESERVATION** IOCTL auf einem anderen Socket als UDP oder TCP zu verwenden. |

## <a name="remarks"></a>Hinweise

Die **SIO \_ RELEASE PORT \_ \_ RESERVATION** IOCTL wird auf Windows Vista und neueren Versionen des Betriebssystems unterstützt.

Anwendungen und Dienste, die Ports reservieren müssen, sind in zwei Kategorien unterteilt.
Die erste Kategorie enthält Komponenten, die einen bestimmten Port als Teil ihres Vorgangs benötigen.
Solche Komponenten bevorzugen in der Regel die Angabe ihres erforderlichen Ports zur Installationszeit (z. B. in einem Anwendungsmanifest).
Die zweite Kategorie umfasst Komponenten, die zur Laufzeit einen verfügbaren Port oder Block von Ports benötigen.
Diese beiden Kategorien entsprechen bestimmten Reservierungsanforderungen und Platzhalterportreservierungsanforderungen.
Bestimmte Reservierungsanforderungen können dauerhaft oder zur Laufzeit sein, während Reservierungsanforderungen für Platzhalterports nur zur Laufzeit unterstützt werden.

Die [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL wird verwendet, um eine Laufzeitreservierung für einen Block von TCP- oder UDP-Ports an fordern.
Für Laufzeitportreservierungen erfordert der Portpool, dass Reservierungen aus dem Prozess verwendet werden, auf dessen Socket die Reservierung gewährt wurde.
Laufzeitportreservierungen dauern nur so lange wie die Lebensdauer des Sockets, auf dem [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL aufgerufen wurde.
Im Gegensatz dazu können persistente Portreservierungen, die mit der [**CreatePersistentTcpPortReservation-**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) oder [**CreatePersistentUdpPortReservation-Funktion**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) erstellt wurden, von jedem Prozess mit der Möglichkeit zum Abrufen persistenter Reservierungen verwendet werden.

Die **SIO \_ RELEASE PORT \_ \_ RESERVATION** IOCTL wird verwendet, um eine Laufzeitreservierung für einen Block von TCP- oder UDP-Ports frei zu geben.

Wenn sowohl *der lpOverlapped-* als auch der *lpCompletionRoutine-Parameter* **NULL sind,** wird der Socket in dieser Funktion als nicht überlappende Socket behandelt.
Bei einem nicht überlappenden Socket werden die Parameter *lpOverlapped* und *lpCompletionRoutine* ignoriert, mit der Ausnahme, dass die Funktion blockieren kann, wenn sich *Sockets* im Blockierungsmodus befinden.
Wenn sich *Sockets* im nicht blockierenden Modus befinden, wird diese Funktion weiterhin blockiert, da diese bestimmte IOCTL den nicht blockierenden Modus nicht unterstützt.

Bei überlappenden Sockets werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.

Jede IOCTL kann je nach Implementierung des Dienstanbieters unbegrenzt blockiert werden.
Wenn die Anwendung das Blockieren in einem [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktionsaufruf** nicht tolerieren kann, wird empfohlen, überlappende E/A-Blöcke für IOCTLs zuzulassen, die besonders wahrscheinlich blockiert werden.

Die **SIO \_ RELEASE PORT \_ \_ RESERVATION** IOCTL kann in den folgenden Fällen mit **WSAEINTR** oder **WSA OPERATION \_ \_ ABORTED** fehlschlagen:

* Die Anforderung wird vom E/A-Manager abgebrochen.
* Der Socket ist geschlossen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Laufzeitportreservierung erworben und dann die Laufzeitportreservierung veröffentlicht.

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

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**DeletePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**DeletePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[**LookupPersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**LookupPersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md)

[**SIO_ASSOCIATE_PORT_RESERVATION**](sio-associate-port-reservation.md)

[Socket](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
