---
description: In Winsock-Anwendungen werden Fehlercodes mithilfe der WSAGetLastError-Funktion abgerufen, der Windows Sockets-Ersatz für die Windows GetLastError-Funktion.
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: 'Fehler Codes: errno, h_errno und WSAGetLastError'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b547e0b580599aaec27a0b77bfad0ffaa8966e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344440"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a><span data-ttu-id="cc4d2-103">Fehler Codes: errno, h \_ errno und WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="cc4d2-103">Error Codes - errno, h\_errno and WSAGetLastError</span></span>

<span data-ttu-id="cc4d2-104">In Winsock-Anwendungen werden Fehlercodes mithilfe der [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) -Funktion abgerufen, der Windows Sockets-Ersatz für die Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-104">In Winsock applications, error codes are retrieved using the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function, the Windows Sockets substitute for the Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span> <span data-ttu-id="cc4d2-105">Die von Windows Sockets zurückgegebenen Fehlercodes ähneln den UNIX-socketfehlercode-Konstanten, aber die Konstanten haben alle den Präfix WSA.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-105">The error codes returned by Windows Sockets are similar to UNIX socket error code constants, but the constants are all prefixed with WSA.</span></span> <span data-ttu-id="cc4d2-106">In Winsock-Anwendungen würde der WSAEWOULDBLOCK-Fehlercode zurückgegeben werden, während in UNIX-Anwendungen der EWOULDBLOCK-Fehlercode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-106">So in Winsock applications the WSAEWOULDBLOCK error code would be returned, while in UNIX applications the EWOULDBLOCK error code would be returned.</span></span>

<span data-ttu-id="cc4d2-107">Fehlercodes, die von Windows Sockets festgelegt werden, werden nicht über die *errno* -Variable zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-107">Error codes set by Windows Sockets are not made available through the *errno* variable.</span></span> <span data-ttu-id="cc4d2-108">Außerdem werden Fehlercodes für die **getxbyy** -Klasse von Functions nicht durch die *h \_ errno* -Variable zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-108">Additionally, for the **getXbyY** class of functions, error codes are not made available through the *h\_errno* variable.</span></span> <span data-ttu-id="cc4d2-109">Die [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) -Funktion soll eine zuverlässige Methode für einen Thread in einem Multithreadprozess bereitstellen, um Fehlerinformationen pro Thread abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-109">The [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function is intended to provide a reliable way for a thread in a multithreaded process to obtain per-thread error information.</span></span>

<span data-ttu-id="cc4d2-110">Aus Kompatibilitätsgründen mit Berkeley Unix (BSD) wurden in früheren Versionen von Windows (z. b. Windows 95 mit dem Windows-Socket 2-Update und Windows 98) neudefinierte reguläre Berkeley-Fehler Konstanten normalerweise in *errno. h* auf BSD als die entsprechenden Windows Sockets WSA-Fehler festgestellt.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-110">For compatibility with Berkeley UNIX (BSD), early versions of Windows (Windows 95 with the Windows Socket 2 Update and Windows 98, for example) redefined regular Berkeley error constants typically found in *errno.h* on BSD as the equivalent Windows Sockets WSA errors.</span></span> <span data-ttu-id="cc4d2-111">Beispielsweise wurde "econnabgelehnte" in der Header Datei " *Winsock. h* " als " **wsaeconnabgelehnte** " definiert.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-111">So for example, ECONNREFUSED was defined as **WSAECONNREFUSED** in the *Winsock.h* header file.</span></span> <span data-ttu-id="cc4d2-112">In nachfolgenden Versionen von Windows (Windows NT 3,1 und höher) wurden diese Definitionen auskommentiert, um Konflikte mit *errno. h* zu vermeiden, die mit Microsoft C/C++ und Visual Studio verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-112">In subsequent versions of Windows (Windows NT 3.1 and later) these defines were commented out to avoid conflicts with *errno.h* used with Microsoft C/C++ and Visual Studio.</span></span>

<span data-ttu-id="cc4d2-113">Die Header Datei " *Winsock2. h* ", die im Microsoft Windows Software Development Kit (SDK), im Platform Software Development Kit (SDK) und in Visual Studio enthalten ist, enthält immer noch einen auskommentierten Block von Definitionen innerhalb eines \# ifdef 0-und \# EndIf-Blocks, die die BSD-Socket-Fehlercodes für die WSA-Fehler Konstanten definieren.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-113">The *Winsock2.h* header file included with the Microsoft Windows Software Development Kit (SDK), Platform Software Development Kit (SDK), and Visual Studio still contains a commented out block of defines within an \#ifdef 0 and \#endif block that define the BSD socket error codes to be the same as the WSA error constants.</span></span> <span data-ttu-id="cc4d2-114">Diese können verwendet werden, um die Kompatibilität mit der UNIX-, BSD-und Linux-Socketprogrammierung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-114">These can be used to provide some compatibility with UNIX, BSD, and Linux socket programming.</span></span> <span data-ttu-id="cc4d2-115">Aus Kompatibilitätsgründen kann eine Anwendung die *Winsock2. h* ändern und die Auskommentierung dieses Blocks aufheben.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-115">For compatibility with BSD, an application may choose to change the *Winsock2.h* and uncomment this block.</span></span> <span data-ttu-id="cc4d2-116">Anwendungsentwickler werden jedoch dringend davon abgeraten, diesen Block aufgrund von unvermeidlichen Konflikten mit *errno. h* in den meisten Anwendungen zu entkommentieren.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-116">However, application developers are strongly discouraged from uncommenting this block because of inevitable conflicts with *errno.h* in most applications.</span></span> <span data-ttu-id="cc4d2-117">Außerdem werden die BSD-Socketfehler für sehr unterschiedliche Werte definiert als in UNIX-, BSD-und Linux-Programmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-117">Also, the BSD socket errors are defined to very different values than are used in UNIX, BSD, and Linux programs.</span></span> <span data-ttu-id="cc4d2-118">Anwendungsentwicklern wird dringend empfohlen, die WSA-Fehler Konstanten in Socketanwendungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-118">Application developers are very strongly encouraged to use the WSA error constants in socket applications.</span></span>

<span data-ttu-id="cc4d2-119">Diese Definitionen bleiben im " *Winsock2. h* "-Header innerhalb eines \# ifdef 0-und eines " \# SDIF"-Blocks auskommentiert.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-119">These defines remain commented out in the *Winsock2.h* header within an \#ifdef 0 and \#endif block.</span></span> <span data-ttu-id="cc4d2-120">Wenn ein Anwendungsentwickler auf die Kompatibilität mit den BSD-Fehlercodes wartet, kann eine Anwendung eine Zeile in der Form einschließen:</span><span class="sxs-lookup"><span data-stu-id="cc4d2-120">If an application developer insists on using the BSD error codes for compatibility, then an application may choose to include a line of the form:</span></span>


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



<span data-ttu-id="cc4d2-121">Dadurch kann der Netzwerkcode, der für die Verwendung des globalen *errno* geschrieben wurde, in einer Single Thread-Umgebung ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-121">This allows networking code which was written to use the global *errno* to work correctly in a single-threaded environment.</span></span> <span data-ttu-id="cc4d2-122">Es gibt einige ernsthafte Nachteile.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-122">There are some very serious drawbacks.</span></span> <span data-ttu-id="cc4d2-123">Wenn eine Quelldatei Code enthält, der *errno* sowohl für Socketfunktionen als auch für nicht-Socket-Funktionen überprüft, kann dieser Mechanismus nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-123">If a source file includes code which inspects *errno* for both socket and non-socket functions, this mechanism cannot be used.</span></span> <span data-ttu-id="cc4d2-124">Außerdem ist es nicht möglich, dass eine Anwendung *errno* einen neuen Wert zuweist.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-124">Furthermore, it is not possible for an application to assign a new value to *errno*.</span></span> <span data-ttu-id="cc4d2-125">(In Windows Sockets kann die [**wsasetlasterror**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) -Funktion zu diesem Zweck verwendet werden.)</span><span class="sxs-lookup"><span data-stu-id="cc4d2-125">(In Windows Sockets, the function [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) may be used for this purpose.)</span></span>

<span data-ttu-id="cc4d2-126">Typischer BSD-Stil</span><span class="sxs-lookup"><span data-stu-id="cc4d2-126">Typical BSD Style</span></span>


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="cc4d2-127">Bevorzugter Stil</span><span class="sxs-lookup"><span data-stu-id="cc4d2-127">Preferred Style</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="cc4d2-128">Obwohl mit Berkeley Sockets 4,3 konsistente Fehler Konstanten aus Kompatibilitätsgründen bereitgestellt werden, wird dringend empfohlen, die WSA-Fehlercode Definitionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-128">Although error constants consistent with Berkeley Sockets 4.3 are provided for compatibility purposes, applications are strongly encouraged to use the WSA error code definitions.</span></span> <span data-ttu-id="cc4d2-129">Dies liegt daran, dass Fehlercodes, die von bestimmten Windows Sockets-Funktionen zurückgegeben werden, in den Standardbereich von Fehlercodes fallen, wie von Microsoft C © definiert.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-129">This is because error codes returned by certain Windows Sockets functions fall into the standard range of error codes as defined by Microsoft C©.</span></span> <span data-ttu-id="cc4d2-130">Daher ist eine bessere Version des vorangehenden Quell Code Fragments:</span><span class="sxs-lookup"><span data-stu-id="cc4d2-130">Thus, a better version of the preceding source code fragment is:</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



<span data-ttu-id="cc4d2-131">Die ursprüngliche in 1995 definierte Winsock 1,1-Spezifikation hat eine Reihe von Fehlercodes empfohlen und listet die möglichen Fehler auf, die als Ergebnis der einzelnen Funktionen zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-131">The original Winsock 1.1 specification defined in 1995 recommended a set of error codes, and listed the possible errors that can be returned as a result of each function.</span></span> <span data-ttu-id="cc4d2-132">Windows Sockets 2 hat zusätzlich zu den in der ursprünglichen Winsock-Spezifikation aufgeführten Windows Sockets-Fehlercodes Funktionen und Features hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-132">Windows Sockets 2 added functions and features with other Windows Sockets error codes returned in addition to those listed in the original Winsock specification.</span></span> <span data-ttu-id="cc4d2-133">Im Laufe der Zeit wurden zusätzliche Funktionen hinzugefügt, um Winsock für die Verwendung durch Entwickler zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-133">Additional functions have been added over time to enhance Winsock for use by developers.</span></span> <span data-ttu-id="cc4d2-134">Beispielsweise wurden neue Namensdienst Funktionen (z. b.[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)) hinzugefügt, die sowohl IPv6 als auch IPv4 unter Windows XP und höher unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-134">For example, new name service functions ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), for example) were added that support both IPv6 and IPv4 on Windows XP and later.</span></span> <span data-ttu-id="cc4d2-135">Einige der älteren reinen IPv4-Namensdienst Funktionen (z. b. die **getxbyy** -Klasse von Functions) sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-135">Some of the older IPv4-only name service functions (the **getXbyY** class of functions, for example) have been deprecated.</span></span>

<span data-ttu-id="cc4d2-136">Eine komplette Liste der möglichen Fehlercodes, die von den Windows Sockets-Funktionen zurückgegeben werden, finden Sie im Abschnitt zu [Windows Sockets-Fehlercodes](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="cc4d2-136">A complete list of possible error codes returned by Windows Sockets functions is given in the section on [Windows Sockets Error Codes](windows-sockets-error-codes-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc4d2-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc4d2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc4d2-138">Behandeln von Winsock-Fehlern</span><span class="sxs-lookup"><span data-stu-id="cc4d2-138">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="cc4d2-139">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="cc4d2-139">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="cc4d2-140">Windows Sockets-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="cc4d2-140">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="cc4d2-141">Überlegungen zur Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="cc4d2-141">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
