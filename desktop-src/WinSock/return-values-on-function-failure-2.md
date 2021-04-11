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
# <a name="return-values-on-function-failure"></a><span data-ttu-id="6439d-105">Rückgabewerte bei Funktions Fehlern</span><span class="sxs-lookup"><span data-stu-id="6439d-105">Return Values on Function Failure</span></span>

<span data-ttu-id="6439d-106">Der **\_ Fehler** "Manifest-konstantensocket" wird zur Überprüfung des Funktions Fehlers bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="6439d-106">The manifest constant **SOCKET\_ERROR** is provided for checking function failure.</span></span> <span data-ttu-id="6439d-107">Obwohl die Verwendung dieser Konstante nicht obligatorisch ist, wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="6439d-107">Although use of this constant is not mandatory, it is recommended.</span></span> <span data-ttu-id="6439d-108">Im folgenden Beispiel wird die Verwendung der **\_ socketfehlerkonstante** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6439d-108">The following example illustrates the use of the **SOCKET\_ERROR** constant.</span></span>

<span data-ttu-id="6439d-109">Typischer BSD-Stil (funktioniert nicht unter Windows)</span><span class="sxs-lookup"><span data-stu-id="6439d-109">Typical BSD Style (will not work on Windows)</span></span>


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



<span data-ttu-id="6439d-110">Windows-Stil</span><span class="sxs-lookup"><span data-stu-id="6439d-110">Windows Style</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6439d-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6439d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6439d-112">Fehler Codes: errno, h \_ errno und WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="6439d-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[<span data-ttu-id="6439d-113">Behandeln von Winsock-Fehlern</span><span class="sxs-lookup"><span data-stu-id="6439d-113">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="6439d-114">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="6439d-114">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="6439d-115">Überlegungen zur Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="6439d-115">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="6439d-116">Windows Sockets-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="6439d-116">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



