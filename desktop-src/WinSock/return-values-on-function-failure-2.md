---
description: Die Manifestkonstante SOCKET \_ ERROR wird zum Überprüfen des Funktionsfehlers bereitgestellt. Obwohl die Verwendung dieser Konstante nicht obligatorisch ist, wird sie empfohlen. Das folgende Beispiel veranschaulicht die Verwendung der SOCKET \_ ERROR-Konstante.
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Rückgabewerte bei Funktionsfehlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b277da114c8c86c53339590eeff3e831cbaf2a4277765bf53047b3d07991b026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740932"
---
# <a name="return-values-on-function-failure"></a>Rückgabewerte bei Funktionsfehlern

Die Manifestkonstante **SOCKET \_ ERROR** wird zum Überprüfen des Funktionsfehlers bereitgestellt. Obwohl die Verwendung dieser Konstante nicht obligatorisch ist, wird sie empfohlen. Das folgende Beispiel veranschaulicht die Verwendung der **SOCKET \_ ERROR-Konstante.**

Typischer BSD-Stil (funktioniert nicht auf Windows)


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



Windows Stil


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

[Fehlercodes: errno, h \_ errno und WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Behandeln von Winsock-Fehlern](handling-winsock-errors.md)
</dt> <dt>

[Portieren von Socketanwendungen in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> <dt>

[Windows Sockets-Fehlercodes](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



