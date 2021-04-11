---
description: Der Fehler "Manifest-konstantensocket" \_ wird zur Überprüfung des Funktions Fehlers bereitgestellt Obwohl die Verwendung dieser Konstante nicht obligatorisch ist, wird empfohlen. Im folgenden Beispiel wird die Verwendung der \_ socketfehlerkonstante veranschaulicht.
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Rückgabewerte bei Funktions Fehlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94280d47d705833528c03c0d98a4a31232a0c6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215347"
---
# <a name="return-values-on-function-failure"></a>Rückgabewerte bei Funktions Fehlern

Der **\_ Fehler** "Manifest-konstantensocket" wird zur Überprüfung des Funktions Fehlers bereitgestellt Obwohl die Verwendung dieser Konstante nicht obligatorisch ist, wird empfohlen. Im folgenden Beispiel wird die Verwendung der **\_ socketfehlerkonstante** veranschaulicht.

Typischer BSD-Stil (funktioniert nicht unter Windows)


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



Windows-Stil


```C++
        iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (iResult == SOCKET_ERROR ) {
            iError = WSAGetLastError();
            if (iError == WSAEWOULDBLOCK)
                printf("recv failed with error: WSAEWOULDBLOCK\n");
            else
                printf("recv failed with error: %ld\n", iError);

            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }    
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehler Codes: errno, h \_ errno und WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Behandeln von Winsock-Fehlern](handling-winsock-errors.md)
</dt> <dt>

[Portieren von Socketanwendungen auf Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> <dt>

[Windows Sockets-Fehler Codes](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



