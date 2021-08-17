---
description: Die Sockaddr-Struktur variiert je nach ausgewähltem Protokoll.
ms.assetid: d1392e1c-2b20-425a-8adf-38e665fb6275
title: sockaddr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sockaddr
api_type:
- NA
api_location: ''
ms.openlocfilehash: afdacd0b4579bcb73bfaaa2da0b3714c7d597d94c0d25020e7353e3afd168d71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927321"
---
# <a name="sockaddr"></a>sockaddr

Die Sockaddr-Struktur variiert je nach ausgewähltem Protokoll. Mit Ausnahme des *\* \_ Sin-Family-Parameters* werden sockaddr-Inhalte in Netzwerk-Bytereihenfolge ausgedrückt.

Winsock-Funktionen, die sockaddr verwenden, werden nicht streng als Zeiger auf eine Sockaddr-Struktur interpretiert. Die Struktur wird im Kontext verschiedener Adressfamilien unterschiedlich interpretiert. Die einzige Anforderung besteht darin, dass das erste **u \_ short** die Adressfamilie und die Gesamtgröße des Arbeitsspeicherpuffers in Bytes *namelen* ist.

Die [**SOCKADDR \_ STORAGE-Struktur**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) speichert auch Socketadresseninformationen, und die Struktur ist ausreichend groß, um IPv4- oder IPv6-Adressinformationen zu speichern. Die Verwendung der **SOCKADDR \_ STORAGE-Struktur** fördert die Unabhängigkeit von Protokollfamilie und Protokollversion und vereinfacht die Entwicklung. Es wird empfohlen, die **SOCKADDR \_ STORAGE-Struktur** anstelle der sockaddr-Struktur zu verwenden. Die **SOCKADDR \_ STORAGE-Struktur** wird auf Windows Server 2003 und höher unterstützt.

Die Struktur "sockaddr" und "sockaddr" \_ in den folgenden Strukturen werden mit IPv4 verwendet. Andere Protokolle verwenden ähnliche Strukturen.

``` syntax
struct sockaddr {
        ushort  sa_family;
        char    sa_data[14];
};

struct sockaddr_in {
        short   sin_family;
        u_short sin_port;
        struct  in_addr sin_addr;
        char    sin_zero[8];
};
```

Der sockaddr \_ in6 und der sockaddr \_ in6 \_ alten Strukturen unten werden mit IPv6 verwendet.

``` syntax
struct sockaddr_in6 {
        short   sin6_family;
        u_short sin6_port;
        u_long  sin6_flowinfo;
        struct  in6_addr sin6_addr;
        u_long  sin6_scope_id;
};

typedef struct sockaddr_in6 SOCKADDR_IN6;
typedef struct sockaddr_in6 *PSOCKADDR_IN6;
typedef struct sockaddr_in6 FAR *LPSOCKADDR_IN6;


struct sockaddr_in6_old {
        short   sin6_family;        
        u_short sin6_port;          
        u_long  sin6_flowinfo;      
        struct  in6_addr sin6_addr;  
};
```

Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, werden **SOCKADDR-** und **SOCKADDR IN-Typdefinitionstags \_** wie folgt für sockaddr und sockaddr \_ in Strukturen definiert:

``` syntax
typedef struct sockaddr {
#if (_WIN32_WINNT < 0x0600)
    u_short sa_family;
#else 
    ADDRESS_FAMILY sa_family;
#endif //(_WIN32_WINNT < 0x0600)
    CHAR sa_data[14];
} SOCKADDR, *PSOCKADDR, FAR *LPSOCKADDR;


typedef struct sockaddr_in {
#if(_WIN32_WINNT < 0x0600)
    short   sin_family;    
#else //(_WIN32_WINNT < 0x0600)
    ADDRESS_FAMILY sin_family;
#endif //(_WIN32_WINNT < 0x0600)
    USHORT sin_port;
    IN_ADDR sin_addr;
    CHAR sin_zero[8];
} SOCKADDR_IN, *PSOCKADDR_IN;
```

Auf dem Windows SDK, das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Headerdateien geändert, und die Sockaddr und sockaddr \_ in Strukturen werden in der *Headerdatei Ws2def.h* definiert, nicht in der *Winsock2.h-Headerdatei.* Die *Headerdatei Ws2def.h* wird automatisch in die *Winsock2.h-Headerdatei* eingefügt. Die sockaddr \_ in6-Struktur wird in der *Headerdatei Ws2ipdef.h* und nicht in der *Headerdatei Ws2tcpip.h* definiert. Die *Headerdatei Ws2ipdef.h* wird automatisch in die *Headerdatei Ws2tcpip.h* eingefügt. Die *Headerdateien "Ws2def.h"* und *"Ws2ipdef.h"* sollten nie direkt verwendet werden.

## <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird die Verwendung der **Sockaddr-Struktur** veranschaulicht.


```C++

// Declare variables
SOCKET ListenSocket;
struct sockaddr_in saServer;
hostent* localHost;
char* localIP;

// Create a listening socket
ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);

// Get the local host information
localHost = gethostbyname("");
localIP = inet_ntoa (*(struct in_addr *)*localHost->h_addr_list);

// Set up the sockaddr structure
saServer.sin_family = AF_INET;
saServer.sin_addr.s_addr = inet_addr(localIP);
saServer.sin_port = htons(5150);

// Bind the listening socket using the
// information in the sockaddr structure
bind( ListenSocket,(SOCKADDR*) &saServer, sizeof(saServer) );


```



## <a name="see-also"></a>Weitere Informationen

[**SOCKADDR-SPEICHER \_**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))


 

 
