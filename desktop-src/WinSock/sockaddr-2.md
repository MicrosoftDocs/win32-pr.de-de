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
# <a name="sockaddr"></a><span data-ttu-id="d1443-103">sockaddr</span><span class="sxs-lookup"><span data-stu-id="d1443-103">sockaddr</span></span>

<span data-ttu-id="d1443-104">Die sockaddr-Struktur variiert je nach ausgewähltem Protokoll.</span><span class="sxs-lookup"><span data-stu-id="d1443-104">The sockaddr structure varies depending on the protocol selected.</span></span> <span data-ttu-id="d1443-105">Mit Ausnahme des Parameters der *Sin- \* \_ Familie* werden sockaddr-Inhalte in der Netzwerk-Byte Reihenfolge ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="d1443-105">Except for the *sin\*\_family* parameter, sockaddr contents are expressed in network byte order.</span></span>

<span data-ttu-id="d1443-106">Winsock-Funktionen, die sockaddr verwenden, werden nicht streng als Zeiger auf eine sockaddr-Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="d1443-106">Winsock functions using sockaddr are not strictly interpreted to be pointers to a sockaddr structure.</span></span> <span data-ttu-id="d1443-107">Die Struktur wird im Kontext verschiedener Adressfamilien anders interpretiert.</span><span class="sxs-lookup"><span data-stu-id="d1443-107">The structure is interpreted differently in the context of different address families.</span></span> <span data-ttu-id="d1443-108">Die einzige Anforderung ist, dass die erste **u \_ Short** die Adressfamilie und die Gesamtgröße des Arbeitsspeicher Puffers in Bytes *namge* ist.</span><span class="sxs-lookup"><span data-stu-id="d1443-108">The only requirements are that the first **u\_short** is the address family and the total size of the memory buffer in bytes is *namelen*.</span></span>

<span data-ttu-id="d1443-109">Die [**sockaddr- \_ Speicher**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) Struktur speichert auch socketadressinformationen, und die Struktur ist ausreichend groß, um IPv4-oder IPv6-Adressinformationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d1443-109">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure also stores socket address information and the structure is sufficiently large to store IPv4 or IPv6 address information.</span></span> <span data-ttu-id="d1443-110">Die Verwendung der **sockaddr- \_ Speicher** Struktur fördert die Unabhängigkeit von Protokoll Familien und Protokoll Versionen und vereinfacht die Entwicklung.</span><span class="sxs-lookup"><span data-stu-id="d1443-110">The use of the **SOCKADDR\_STORAGE** structure promotes protocol-family and protocol-version independence, and simplifies development.</span></span> <span data-ttu-id="d1443-111">Es wird empfohlen, die **sockaddr- \_ Speicher** Struktur anstelle der sockaddr-Struktur zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1443-111">It is recommended that the **SOCKADDR\_STORAGE** structure be used in place of the sockaddr structure.</span></span> <span data-ttu-id="d1443-112">Die **sockaddr- \_ Speicher** Struktur wird unter Windows Server 2003 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1443-112">The **SOCKADDR\_STORAGE** structure is supported on Windows Server 2003 and later.</span></span>

<span data-ttu-id="d1443-113">Die sockaddr-Struktur und sockaddr \_ in den folgenden Strukturen werden mit IPv4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1443-113">The sockaddr structure and sockaddr\_in structures below are used with IPv4.</span></span> <span data-ttu-id="d1443-114">Andere Protokolle verwenden ähnliche Strukturen.</span><span class="sxs-lookup"><span data-stu-id="d1443-114">Other protocols use similar structures.</span></span>

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

<span data-ttu-id="d1443-115">Die folgenden sockaddr \_ -IN6 und sockaddr \_ IN6 \_ alte Strukturen werden mit IPv6 verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1443-115">The sockaddr\_in6 and sockaddr\_in6\_old structures below are used with IPv6.</span></span>

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

<span data-ttu-id="d1443-116">Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, werden **sockaddr** -und **sockaddr-Tags \_ in** typedef-Tags wie folgt für sockaddr und sockaddr \_ in Strukturen definiert:</span><span class="sxs-lookup"><span data-stu-id="d1443-116">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, **SOCKADDR** and **SOCKADDR\_IN** typedef tags are defined for sockaddr and sockaddr\_in structures as follows:</span></span>

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

<span data-ttu-id="d1443-117">Auf der Windows SDK, die für Windows Vista und höher veröffentlicht wurden, hat sich die Organisation der Header Dateien geändert, und die sockaddr-und sockaddr- \_ Struktur in Strukturen sind in der Header Datei " *Ws2def. h* " und nicht in der Header Datei " *Winsock2. h* " definiert.</span><span class="sxs-lookup"><span data-stu-id="d1443-117">On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the sockaddr and sockaddr\_in structures are defined in the *Ws2def.h* header file, not the *Winsock2.h* header file.</span></span> <span data-ttu-id="d1443-118">Die Header Datei " *Ws2def. h* " wird automatisch von der *Winsock2. h* -Header Datei eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d1443-118">The *Ws2def.h* header file is automatically included by the *Winsock2.h* header file.</span></span> <span data-ttu-id="d1443-119">Die sockaddr \_ IN6-Struktur wird in der *Ws2ipdef. h* -Header Datei definiert, nicht in der Header Datei *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="d1443-119">The sockaddr\_in6 structure is defined in the *Ws2ipdef.h* header file, not the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="d1443-120">Die Header Datei " *Ws2ipdef. h* " wird automatisch von der *Ws2tcpip. h* -Header Datei eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d1443-120">The *Ws2ipdef.h* header file is automatically included by the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="d1443-121">Die Header Dateien *Ws2def. h* und *Ws2ipdef. h* sollten niemals direkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1443-121">The *Ws2def.h* and *Ws2ipdef.h* header files should never be used directly.</span></span>

## <a name="example-code"></a><span data-ttu-id="d1443-122">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="d1443-122">Example Code</span></span>

<span data-ttu-id="d1443-123">Im folgenden Beispiel wird die Verwendung der **sockaddr** -Struktur veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d1443-123">The following example demonstrates the use of the **sockaddr** structure.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="d1443-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d1443-124">See Also</span></span>

<span data-ttu-id="d1443-125">[**sockaddr- \_ Speicher**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1443-125">[**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span></span>


 

 
