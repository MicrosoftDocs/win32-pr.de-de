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
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a>Fehler Codes: errno, h \_ errno und WSAGetLastError

In Winsock-Anwendungen werden Fehlercodes mithilfe der [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) -Funktion abgerufen, der Windows Sockets-Ersatz für die Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion. Die von Windows Sockets zurückgegebenen Fehlercodes ähneln den UNIX-socketfehlercode-Konstanten, aber die Konstanten haben alle den Präfix WSA. In Winsock-Anwendungen würde der WSAEWOULDBLOCK-Fehlercode zurückgegeben werden, während in UNIX-Anwendungen der EWOULDBLOCK-Fehlercode zurückgegeben wird.

Fehlercodes, die von Windows Sockets festgelegt werden, werden nicht über die *errno* -Variable zur Verfügung gestellt. Außerdem werden Fehlercodes für die **getxbyy** -Klasse von Functions nicht durch die *h \_ errno* -Variable zur Verfügung gestellt. Die [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) -Funktion soll eine zuverlässige Methode für einen Thread in einem Multithreadprozess bereitstellen, um Fehlerinformationen pro Thread abzurufen.

Aus Kompatibilitätsgründen mit Berkeley Unix (BSD) wurden in früheren Versionen von Windows (z. b. Windows 95 mit dem Windows-Socket 2-Update und Windows 98) neudefinierte reguläre Berkeley-Fehler Konstanten normalerweise in *errno. h* auf BSD als die entsprechenden Windows Sockets WSA-Fehler festgestellt. Beispielsweise wurde "econnabgelehnte" in der Header Datei " *Winsock. h* " als " **wsaeconnabgelehnte** " definiert. In nachfolgenden Versionen von Windows (Windows NT 3,1 und höher) wurden diese Definitionen auskommentiert, um Konflikte mit *errno. h* zu vermeiden, die mit Microsoft C/C++ und Visual Studio verwendet werden.

Die Header Datei " *Winsock2. h* ", die im Microsoft Windows Software Development Kit (SDK), im Platform Software Development Kit (SDK) und in Visual Studio enthalten ist, enthält immer noch einen auskommentierten Block von Definitionen innerhalb eines \# ifdef 0-und \# EndIf-Blocks, die die BSD-Socket-Fehlercodes für die WSA-Fehler Konstanten definieren. Diese können verwendet werden, um die Kompatibilität mit der UNIX-, BSD-und Linux-Socketprogrammierung zu gewährleisten. Aus Kompatibilitätsgründen kann eine Anwendung die *Winsock2. h* ändern und die Auskommentierung dieses Blocks aufheben. Anwendungsentwickler werden jedoch dringend davon abgeraten, diesen Block aufgrund von unvermeidlichen Konflikten mit *errno. h* in den meisten Anwendungen zu entkommentieren. Außerdem werden die BSD-Socketfehler für sehr unterschiedliche Werte definiert als in UNIX-, BSD-und Linux-Programmen verwendet werden. Anwendungsentwicklern wird dringend empfohlen, die WSA-Fehler Konstanten in Socketanwendungen zu verwenden.

Diese Definitionen bleiben im " *Winsock2. h* "-Header innerhalb eines \# ifdef 0-und eines " \# SDIF"-Blocks auskommentiert. Wenn ein Anwendungsentwickler auf die Kompatibilität mit den BSD-Fehlercodes wartet, kann eine Anwendung eine Zeile in der Form einschließen:


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



Dadurch kann der Netzwerkcode, der für die Verwendung des globalen *errno* geschrieben wurde, in einer Single Thread-Umgebung ordnungsgemäß funktionieren. Es gibt einige ernsthafte Nachteile. Wenn eine Quelldatei Code enthält, der *errno* sowohl für Socketfunktionen als auch für nicht-Socket-Funktionen überprüft, kann dieser Mechanismus nicht verwendet werden. Außerdem ist es nicht möglich, dass eine Anwendung *errno* einen neuen Wert zuweist. (In Windows Sockets kann die [**wsasetlasterror**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) -Funktion zu diesem Zweck verwendet werden.)

Typischer BSD-Stil


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



Bevorzugter Stil


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



Obwohl mit Berkeley Sockets 4,3 konsistente Fehler Konstanten aus Kompatibilitätsgründen bereitgestellt werden, wird dringend empfohlen, die WSA-Fehlercode Definitionen zu verwenden. Dies liegt daran, dass Fehlercodes, die von bestimmten Windows Sockets-Funktionen zurückgegeben werden, in den Standardbereich von Fehlercodes fallen, wie von Microsoft C © definiert. Daher ist eine bessere Version des vorangehenden Quell Code Fragments:


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



Die ursprüngliche in 1995 definierte Winsock 1,1-Spezifikation hat eine Reihe von Fehlercodes empfohlen und listet die möglichen Fehler auf, die als Ergebnis der einzelnen Funktionen zurückgegeben werden können. Windows Sockets 2 hat zusätzlich zu den in der ursprünglichen Winsock-Spezifikation aufgeführten Windows Sockets-Fehlercodes Funktionen und Features hinzugefügt. Im Laufe der Zeit wurden zusätzliche Funktionen hinzugefügt, um Winsock für die Verwendung durch Entwickler zu verbessern. Beispielsweise wurden neue Namensdienst Funktionen (z. b.[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)) hinzugefügt, die sowohl IPv6 als auch IPv4 unter Windows XP und höher unterstützen. Einige der älteren reinen IPv4-Namensdienst Funktionen (z. b. die **getxbyy** -Klasse von Functions) sind veraltet.

Eine komplette Liste der möglichen Fehlercodes, die von den Windows Sockets-Funktionen zurückgegeben werden, finden Sie im Abschnitt zu [Windows Sockets-Fehlercodes](windows-sockets-error-codes-2.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Behandeln von Winsock-Fehlern](handling-winsock-errors.md)
</dt> <dt>

[Portieren von Socketanwendungen auf Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows Sockets-Fehler Codes](windows-sockets-error-codes-2.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> </dl>

 

 
