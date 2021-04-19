---
description: Mit der "so \_ exclusiveaddruse"-Socketoption wird verhindert, dass andere Sockets an dieselbe Adresse und denselben Port gebunden werden.
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: SO_EXCLUSIVEADDRUSE Socket-Option (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348772"
---
# <a name="so_exclusiveaddruse-socket-option"></a>" \_ Exclusiveaddruse"-Socketoption

Mit der "so \_ exclusiveaddruse"-Socketoption wird verhindert, dass andere Sockets an dieselbe Adresse und denselben Port gebunden werden.

## <a name="syntax"></a>Syntax

Die Option "so \_ exclusiveaddruse" verhindert, dass andere Sockets zwangsweise an dieselbe Adresse und denselben Port gebunden werden, eine Übung, die von der so \_ reuseaddr-Socketoption aktiviert wird. Eine solche Wiederverwendung kann von böswilligen Anwendungen ausgeführt werden, um die Anwendung zu unterbrechen. Die Option "so \_ exclusiveaddruse" ist sehr nützlich für Systemdienste, die Hochverfügbarkeit erfordern.

Im folgenden Codebeispiel wird das Festlegen dieser Option veranschaulicht.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



Um einen Effekt zu haben, muss die Option "so \_ exclusivaddruse" festgelegt werden, bevor die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion aufgerufen wird (Dies gilt auch für die \_ Option "reuseaddr"). In Tabelle 1 werden die Auswirkungen der Einstellung der \_ Option "so exclusiveaddruse" aufgeführt. Platzhalter gibt eine Bindung an die Platzhalter Adresse an, z. b. 0.0.0.0 für IPv4 und:: für IPv6. Spezifisch gibt eine Bindung an eine bestimmte Schnittstelle an, z. b. das Binden einer einem Adapter zugewiesenen IP-Adresse. Specific2 gibt an, dass die Bindung an eine bestimmte Adresse nicht an die Adresse gebunden ist, die im speziellen Fall an gebunden ist

> [!Note]  
> Der Specific2-Fall ist nur anwendbar, wenn die erste Bindung mit einer bestimmten Adresse ausgeführt wird. für den Fall, in dem der erste Socket an den Platzhalter gebunden ist, deckt der Eintrag für "spezifisch" alle speziellen Adress Fälle ab.

 

Nehmen Sie beispielsweise einen Computer mit zwei IP-Schnittstellen an: 10.0.0.1 und 10.99.99.99. Wenn die erste Bindung an 10.0.0.1 und Port 5150 mit der "so \_ exclusiveaddruse"-Option festgelegt ist, wird die zweite Bindung an 10.99.99.99 und Port 5150 mit einer oder ohne Optionen erfolgreich festgelegt. Wenn der erste Socket jedoch an die Platzhalter Adresse (0.0.0.0) und Port 5150 gebunden ist, wobei " \_ exclusiveaddruse" festgelegt ist, schlagen alle nachfolgenden Bindungen an denselben Port – unabhängig von der IP-Adresse – entweder mit WSAEADDRINUSE (10048) oder wsaeaccess (10013) fehl

### <a name="bind-behavior-with-various-options-set"></a>Bindungsverhalten mit verschiedenen festgelegten Optionen



Zweite Bindung

Erste Bindung

*" \_ exclusiveaddruse"*

*Keine Optionen* oder *so \_ reuseaddr*

*Platzhalter*

*Zugeschnitten*

*Platzhalter*

*Zugeschnitten*

$ {ROWSPAN3} $*so \_ exclusiveaddruse*$ {Remove} $  

*Platzhalter*

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

*Zugeschnitten*

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

*Specific2*

–

Erfolg

–

Erfolg

$ {ROWSPAN3} $*keine Optionen*$ {Remove} $  

*Platzhalter*

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

*Zugeschnitten*

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

Fehlgeschlagen (10048)

*Specific2*

–

Erfolg

–

Erfolg

$ {ROWSPAN3} $*so \_ reuseaddr*$ {Remove} $  

*Platzhalter*

Fehlgeschlagen (10013)

Fehlgeschlagen (10013)

Erfolgreich\*

Erfolg

*Zugeschnitten*

Fehlgeschlagen (10013)

Fehlgeschlagen (10013)

Erfolg

Erfolgreich\*

*Specific2*

–

Erfolg

–

Erfolg

\* Das Verhalten ist nicht definiert, in welchem Socket Pakete empfangen werden.



 

Wenn die erste Bindung keine Optionen oder " \_ reuseaddr" festlegt und die zweite Bindung eine so \_ reuseaddr ausführt, hat der zweite Socket den Port und das Verhalten überholt, wenn der Socket, der die Pakete empfängt, nicht bestimmt wird. Daher \_ wurde exclusiveaddruse eingeführt, um dieser Situation gerecht zu werden.

Ein Socket mit der " \_ exclusiveaddruse"-Menge kann nicht immer sofort nach dem Socket-Abschluss wieder verwendet werden. Wenn ein lausch ender Socket mit dem exklusiven Flagsatz z. b. eine Verbindung akzeptiert, nach der der lausch Ende Socket geschlossen wird, kann ein anderer Socket nicht an denselben Port wie der erste Abhör Socket mit dem exklusiven Flag gebunden werden, bis die akzeptierte Verbindung nicht mehr aktiv ist.

Diese Situation kann recht kompliziert sein. Obwohl der Socket geschlossen wurde, kann der zugrunde liegende Transport seine Verbindung möglicherweise nicht beenden. Auch nachdem der Socket geschlossen wurde, muss das System alle gepufferten Daten senden, eine ordnungsgemäße Verbindung mit dem Peer übertragen und auf eine ordnungsgemäße Trennung vom Peer warten. Daher ist es möglich, dass der zugrunde liegende Transport die Verbindung niemals freigibt, z. b. wenn der Peer ein Fenster der Größe 0 (null) oder andere derartige Angriffe anweist. Im vorherigen Beispiel wurde der Abhör Socket geschlossen, nachdem eine Client Verbindung akzeptiert wurde. Auch wenn die Client Verbindung geschlossen ist, wird der Port möglicherweise noch nicht wieder verwendet, wenn die Client Verbindung aufgrund nicht bestätigter Daten in einem aktiven Zustand bleibt usw.

Um diese Situation zu vermeiden, sollten Anwendungen ein ordnungsgemäßes herunter [](/windows/desktop/api/winsock/nf-winsock-shutdown) fahren sicherstellen: fahren Sie mit dem SD- \_ sendeflag herunter, und warten Sie dann in einer [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -Schleife, bis null Bytes zurückgegeben werden Dadurch wird das Problem im Zusammenhang mit der Port Wiederverwendung vermieden, es wird sichergestellt, dass alle Daten vom Peer empfangen wurden, und der Peer wird sichergestellt, dass alle Daten erfolgreich empfangen wurden.

Die Option "so \_ LINGER" kann für einen Socket festgelegt werden, um zu verhindern, dass der Port in einen der aktiven warte Zustände geht. Dies wird jedoch nicht empfohlen, da dies zu unerwünschten Effekten führen kann, da dies dazu führen kann, dass die Verbindung zurückgesetzt wird. Wenn z. b. Daten empfangen, aber noch nicht vom Peer bestätigt wurden und der lokale Computer den Socket mit dem sogenannten \_ LINGER-Satz schließt, wird die Verbindung zurückgesetzt, und der Peer verwirft die nicht bestätigten Daten. Außerdem ist es schwierig, eine passende Zeit für den Linger auszuwählen. Wenn ein Wert zu klein ist, werden viele abgebrochene Verbindungen erzielt, während ein großes Timeout das System anfällig für Denial-of-Service-Angriffe ist, indem viele Verbindungen hergestellt werden und dadurch zahlreiche Anwendungsthreads blockiert werden.

> [!Note]  
> Ein Socket, der die Option "so \_ exclusiveaddruse" verwendet, muss vor dem Schließen ordnungsgemäß heruntergefahren werden. Andernfalls kann dies zu einem Denial-of-Service-Angriff führen, wenn der zugeordnete Dienst neu gestartet werden muss.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winsock2. h</dt> </dl> |



 

 




