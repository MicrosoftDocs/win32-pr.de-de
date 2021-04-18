---
description: Beim Hinzufügen der Unterstützung für IPv6 müssen Sie sicherstellen, dass Ihre Anwendung Datenstrukturen mit ordnungsgemäßer Größen Definition definiert.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Ändern von Datenstrukturen für IPv6-Winsock-Appications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c91e19ed733d111bd4e12d824da6ee1a988e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343300"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a><span data-ttu-id="20e67-103">Ändern von Datenstrukturen für IPv6-Winsock-Appications</span><span class="sxs-lookup"><span data-stu-id="20e67-103">Changing Data Structures for IPv6 Winsock Appications</span></span>

<span data-ttu-id="20e67-104">Beim Hinzufügen der Unterstützung für IPv6 müssen Sie sicherstellen, dass Ihre Anwendung Datenstrukturen mit ordnungsgemäßer Größen Definition definiert.</span><span class="sxs-lookup"><span data-stu-id="20e67-104">When adding support for IPv6, you must ensure that your application defines properly sized data structures.</span></span> <span data-ttu-id="20e67-105">Die Größe einer IPv6-Adresse ist weitaus größer als eine IPv4-Adresse.</span><span class="sxs-lookup"><span data-stu-id="20e67-105">The size of an IPv6 address is much larger than an IPv4 address.</span></span> <span data-ttu-id="20e67-106">Strukturen, die hart codiert sind, um die Größe einer IPv4-Adresse beim Speichern einer IP-Adresse zu verarbeiten, verursachen Probleme in der Anwendung und müssen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="20e67-106">Structures that are hard-coded to handle the size of an IPv4 address when storing an IP address will cause problems in your application, and must be modified.</span></span>

<span data-ttu-id="20e67-107">Bewährte Methode</span><span class="sxs-lookup"><span data-stu-id="20e67-107">Best Practice</span></span>

<span data-ttu-id="20e67-108">Der beste Ansatz, um sicherzustellen, dass ihre Strukturen ordnungsgemäß skaliert sind, ist die Verwendung der [**sockaddr- \_ Speicher**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) Struktur.</span><span class="sxs-lookup"><span data-stu-id="20e67-108">The best approach to ensuring that your structures are properly sized is to use the [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure.</span></span> <span data-ttu-id="20e67-109">Die **sockaddr- \_ Speicher** Struktur ist für die IP-Adress Version agnostisch.</span><span class="sxs-lookup"><span data-stu-id="20e67-109">The **SOCKADDR\_STORAGE** structure is agnostic to IP address version.</span></span> <span data-ttu-id="20e67-110">Wenn die **sockaddr- \_ Speicher** Struktur zum Speichern von IP-Adressen verwendet wird, können IPv4-und IPv6-Adressen ordnungsgemäß mit einer Codebasis behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="20e67-110">When the **SOCKADDR\_STORAGE** structure is used to store IP addresses, IPv4 and IPv6 addresses can be properly handled with one code base.</span></span>

<span data-ttu-id="20e67-111">Das folgende Beispiel, bei dem es sich um einen Auszug aus der Datei "Server. c" in Anhang B handelt, identifiziert eine angemessene Verwendung der **sockaddr- \_ Speicher** Struktur.</span><span class="sxs-lookup"><span data-stu-id="20e67-111">The following example, which is an excerpt taken from the Server.c file found in Appendix B, identifies an appropriate use of the **SOCKADDR\_STORAGE** structure.</span></span> <span data-ttu-id="20e67-112">Beachten Sie, dass die-Struktur, die in diesem Beispiel ordnungsgemäß verwendet wird, entweder eine IPv4-oder eine IPv6-Adresse ordnungsgemäß verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="20e67-112">Notice that the structure, when used properly as this example shows, gracefully handles either an IPv4 or IPv6 address.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

#define BUFFER_SIZE 512
#define DEFAULT_PORT "27015"

int main(int argc, char **argv)
{
    char Buffer[BUFFER_SIZE] = {0};
    char *Hostname;
    int Family = AF_UNSPEC;
    int SocketType = SOCK_STREAM;
    char *Port = DEFAULT_PORT;
    char *Address = NULL;
    int i = 0;
    DWORD dwRetval = 0;
    int iResult = 0;
    int FromLen = 0;
    int AmountRead = 0;

    SOCKADDR_STORAGE From;

    WSADATA wsaData;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;

    // Parse arguments
    if (argc >= 1) {
        Hostname = argv[1];
    }    

   // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    From.ss_family = (ADDRESS_FAMILY) Family;
    
    //...
        
        return 0;
}
```



> [!Note]  
> <span data-ttu-id="20e67-113">Die [**sockaddr- \_ Speicher**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) Struktur ist neu für Windows XP.</span><span class="sxs-lookup"><span data-stu-id="20e67-113">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure is new for Windows XP.</span></span>

 

<span data-ttu-id="20e67-114">Zu Vermeider Code</span><span class="sxs-lookup"><span data-stu-id="20e67-114">Code To Avoid</span></span>

<span data-ttu-id="20e67-115">In der Regel haben viele Anwendungen die [**sockaddr**](sockaddr-2.md) -Struktur verwendet, um Protokoll unabhängige Adressen zu speichern, oder die **sockaddr \_ in** der Struktur für IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="20e67-115">Typically, many applications used the [**sockaddr**](sockaddr-2.md) structure to store protocol-independent addresses, or the **sockaddr\_in** structure for IP addresses.</span></span> <span data-ttu-id="20e67-116">Weder die sockaddr-Struktur noch die **sockaddr \_ in** -Struktur ist groß genug, um IPv6-Adressen aufzunehmen. beide sind nicht ausreichend, wenn Ihre Anwendung IPv6-kompatibel sein soll.</span><span class="sxs-lookup"><span data-stu-id="20e67-116">Neither the sockaddr structure nor the **sockaddr\_in** structure is large enough to hold IPv6 addresses, and therefore both are insufficient if your application is to be IPv6 compatible.</span></span>

<span data-ttu-id="20e67-117">Codierungs Aufgabe</span><span class="sxs-lookup"><span data-stu-id="20e67-117">Coding Task</span></span>

<span data-ttu-id="20e67-118">**So ändern Sie die vorhandene Codebasis von IPv4 zu IPv4-und IPv6-Interoperabilität**</span><span class="sxs-lookup"><span data-stu-id="20e67-118">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="20e67-119">Erwerben Sie das Checkv4.exe-Hilfsprogramm.</span><span class="sxs-lookup"><span data-stu-id="20e67-119">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="20e67-120">Das-Hilfsprogramm ist im Microsoft Windows Software Development Kit (SDK) enthalten, das über Ihr MSDN-Abonnement oder über das Internet als Download verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="20e67-120">The utility is included with the Microsoft Windows Software Development Kit (SDK) which is made available through your MSDN subscription, or from the web as a download.</span></span>
2.  <span data-ttu-id="20e67-121">Führen Sie das Checkv4.exe-Hilfsprogramm für den Code aus.</span><span class="sxs-lookup"><span data-stu-id="20e67-121">Run the Checkv4.exe utility against your code.</span></span> <span data-ttu-id="20e67-122">Erfahren Sie, wie Sie das Checkv4.exe-Hilfsprogramm für Ihre Dateien ausführen, [indem Sie das Checkv4.exe-Hilfsprogramm verwenden](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="20e67-122">Learn about how to run the Checkv4.exe utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="20e67-123">Das Hilfsprogramm warnt Sie bei der Verwendung von **sockaddr** oder **sockaddr \_ in** Strukturen und bietet Empfehlungen darüber, wie Sie entweder durch die IPv6-kompatible Struktur [**sockaddr- \_ Speicher**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="20e67-123">The utility alerts you to usage of **sockaddr** or **sockaddr\_in** structures, and provides recommendations on how to replace either with the IPv6 compatible structure [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).</span></span>
4.  <span data-ttu-id="20e67-124">Ersetzen Sie alle diese Instanzen und den zugehörigen Code nach Bedarf, um die **sockaddr- \_ Speicher** Struktur zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="20e67-124">Replace any such instances, and associated code as appropriate, to use the **SOCKADDR\_STORAGE** structure.</span></span>

<span data-ttu-id="20e67-125">Alternativ dazu können Sie Ihre Codebasis nach Instanzen von **sockaddr** und **sockaddr \_ in** Strukturen durchsuchen und die gesamte Verwendung (und ggf. einen anderen zugeordneten Code) in die **sockaddr- \_ Speicher** Struktur ändern.</span><span class="sxs-lookup"><span data-stu-id="20e67-125">Alternatively, you can search your code base for instances of the **sockaddr** and **sockaddr\_in** structures, and change all such usage (and other associated code, as appropriate) to the **SOCKADDR\_STORAGE** structure.</span></span>

> [!Note]  
> <span data-ttu-id="20e67-126">Die Speicherstrukturen **addrinfo** und **\_ sockaddr** umfassen Protokoll-und Adress familienmember (**AI- \_ Familie** bzw. **SS- \_ Familie**).</span><span class="sxs-lookup"><span data-stu-id="20e67-126">The **addrinfo** and **SOCKADDR\_STORAGE** structures include protocol and address family members (**ai\_family** and **ss\_family**), respectively.</span></span> <span data-ttu-id="20e67-127">RFC 2553 gibt das **AI- \_ Familienmitglied** von [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) als int an, während die **SS- \_ Familie** kurz angegeben wird. Daher führt eine direkte Kopie zwischen diesen Membern zu einem Compilerfehler.</span><span class="sxs-lookup"><span data-stu-id="20e67-127">RFC 2553 specifies the **ai\_family** member of [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) as an int, while **ss\_family** is specified as a short; as such, a direct copy between those members results in a compiler error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="20e67-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20e67-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20e67-129">IPv6-Handbuch für Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20e67-129">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="20e67-130">Dual-Stack-Sockets für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20e67-130">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="20e67-131">Funktionsaufrufe für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20e67-131">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="20e67-132">Verwendung von hart codierten IPv4-Adressen</span><span class="sxs-lookup"><span data-stu-id="20e67-132">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="20e67-133">Probleme mit der Benutzeroberfläche für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20e67-133">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="20e67-134">Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20e67-134">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
