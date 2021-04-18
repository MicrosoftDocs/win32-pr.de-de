---
description: Die sockaddr-Struktur variiert je nach ausgewähltem Protokoll.
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
ms.openlocfilehash: ccd4b98efc987630ab625e5c9788f0be16018e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343820"
---
# <a name="sockaddr"></a>sockaddr

Die sockaddr-Struktur variiert je nach ausgewähltem Protokoll. Mit Ausnahme des Parameters der *Sin- \* \_ Familie* werden sockaddr-Inhalte in der Netzwerk-Byte Reihenfolge ausgedrückt.

Winsock-Funktionen, die sockaddr verwenden, werden nicht streng als Zeiger auf eine sockaddr-Struktur interpretiert. Die Struktur wird im Kontext verschiedener Adressfamilien anders interpretiert. Die einzige Anforderung ist, dass die erste **u \_ Short** die Adressfamilie und die Gesamtgröße des Arbeitsspeicher Puffers in Bytes *namge* ist.

Die [**sockaddr- \_ Speicher**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) Struktur speichert auch socketadressinformationen, und die Struktur ist ausreichend groß, um IPv4-oder IPv6-Adressinformationen zu speichern. Die Verwendung der **sockaddr- \_ Speicher** Struktur fördert die Unabhängigkeit von Protokoll Familien und Protokoll Versionen und vereinfacht die Entwicklung. Es wird empfohlen, die **sockaddr- \_ Speicher** Struktur anstelle der sockaddr-Struktur zu verwenden. Die **sockaddr- \_ Speicher** Struktur wird unter Windows Server 2003 und höher unterstützt.

Die sockaddr-Struktur und sockaddr \_ in den folgenden Strukturen werden mit IPv4 verwendet. Andere Protokolle verwenden ähnliche Strukturen.

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

Die folgenden sockaddr \_ -IN6 und sockaddr \_ IN6 \_ alte Strukturen werden mit IPv6 verwendet.

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

Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, werden **sockaddr** -und **sockaddr-Tags \_ in** typedef-Tags wie folgt für sockaddr und sockaddr \_ in Strukturen definiert:

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

Auf der Windows SDK, die für Windows Vista und höher veröffentlicht wurden, hat sich die Organisation der Header Dateien geändert, und die sockaddr-und sockaddr- \_ Struktur in Strukturen sind in der Header Datei " *Ws2def. h* " und nicht in der Header Datei " *Winsock2. h* " definiert. Die Header Datei " *Ws2def. h* " wird automatisch von der *Winsock2. h* -Header Datei eingeschlossen. Die sockaddr \_ IN6-Struktur wird in der *Ws2ipdef. h* -Header Datei definiert, nicht in der Header Datei *Ws2tcpip. h* . Die Header Datei " *Ws2ipdef. h* " wird automatisch von der *Ws2tcpip. h* -Header Datei eingeschlossen. Die Header Dateien *Ws2def. h* und *Ws2ipdef. h* sollten niemals direkt verwendet werden.

## <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird die Verwendung der **sockaddr** -Struktur veranschaulicht.


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

[**sockaddr- \_ Speicher**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))


 

 
