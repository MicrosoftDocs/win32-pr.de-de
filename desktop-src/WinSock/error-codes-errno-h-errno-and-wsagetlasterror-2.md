---
description: In Winsock-Anwendungen werden Fehlercodes mithilfe der WSAGetLastError-Funktion abgerufen, wobei die Windows Sockets die Windows GetLastError-Funktion ersetzen.
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: 'Fehlercodes: errno, h_errno und WSAGetLastError'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e9c4372bd479ee4b94bd3226128737dae3d5637be94046eb013716590ac285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132633"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a>Fehlercodes: errno, h \_ errno und WSAGetLastError

In Winsock-Anwendungen werden Fehlercodes mithilfe der [**WSAGetLastError-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) abgerufen. Die Windows Sockets ersetzen die Windows [**GetLastError-Funktion.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) Die von Windows Sockets zurückgegebenen Fehlercodes ähneln UNIX Socketfehlercodekonstanten, aber allen Konstanten wird das Präfix WSA vorangestellt. In Winsock-Anwendungen würde der WSAEW DLLDBLOCK-Fehlercode zurückgegeben, während in UNIX Anwendungen der Fehlercode EWOULDBLOCK zurückgegeben würde.

Fehlercodes, die von Windows Sockets festgelegt werden, werden nicht über die *errno-Variable* verfügbar gemacht. Darüber hinaus werden fehlercodes für die **getXbyY-Klasse** von Funktionen nicht über die *h \_ errno-Variable* verfügbar gemacht. Die [**WSAGetLastError-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) soll einem Thread in einem Multithreadprozess eine zuverlässige Möglichkeit bieten, pro Thread Fehlerinformationen abzurufen.

Aus Gründen der Kompatibilität mit UNIX Windows Socket 2 Update und Windows 98 definierten frühe Versionen von Windows (Windows 95 mit Windows Socket 2 Update und Windows 98) reguläre Fehlerkonstanten in Der Regel in *errno.h* auf BSD als entsprechende Windows Sockets WSA-Fehler neu. So wurde beispielsweise ECONNREFUSED in der *Headerdatei "Winsock.h"* als **WSAECONNREFUSED** definiert. In nachfolgenden Versionen von Windows (Windows NT 3.1 und höher) wurden diese Definitionen auskommentiert, um Konflikte mit *errno.h* zu vermeiden, die mit Microsoft C/C++ und Visual Studio verwendet werden.

Die *Winsock2.h-Headerdatei,* die im Microsoft Windows Software Development Kit (SDK), Im Platform Software Development Kit (SDK) enthalten ist, und Visual Studio enthält weiterhin einen auskommentierten Block von defines in einem \# ifdef 0- und \# endif-Block, der die Fehlercodes des BSD-Sockets so definiert, dass sie mit den WSA-Fehlerkonstanten identisch sind. Diese können verwendet werden, um eine gewisse Kompatibilität mit UNIX, BSD und Linux-Socketprogrammierung bereitzustellen. Aus Gründen der Kompatibilität mit BSD kann eine Anwendung die *Winsock2.h-Datei* ändern und die Auskommentierung dieses Blocks aufheben. Anwendungsentwickler werden jedoch dringend davon abgeraten, diesen Block aufgrund von unvermeidlichen Konflikten mit *errno.h* in den meisten Anwendungen auskommentieren zu lassen. Außerdem werden die BSD-Socketfehler in sehr unterschiedlichen Werten definiert, als in UNIX-, BSD- und Linux-Programmen verwendet werden. Anwendungsentwicklern wird dringend empfohlen, die WSA-Fehlerkonstanten in Socketanwendungen zu verwenden.

Diese Definitionen bleiben im *Winsock2.h-Header* innerhalb eines \# ifdef 0- und \# endif-Blocks auskommentiert. Wenn ein Anwendungsentwickler die Verwendung der BSD-Fehlercodes aus Gründen der Kompatibilität befürchtet, kann eine Anwendung eine Zeile des Formulars einschließen:


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



Dadurch kann Netzwerkcode, der für die Verwendung des globalen *Errno* geschrieben wurde, in einer Singlethreadumgebung ordnungsgemäß funktionieren. Es gibt einige sehr schwerwiegende Nachteile. Wenn eine Quelldatei Code enthält, der *errno* sowohl für Socketfunktionen als auch für Nicht-Socketfunktionen überprüft, kann dieser Mechanismus nicht verwendet werden. Darüber hinaus ist es nicht möglich, dass eine Anwendung *errno* einen neuen Wert zuweist. (In Windows Sockets kann die Funktion [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) für diesen Zweck verwendet werden.)

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



Obwohl Fehlerkonstanten, die mit Sockets 4.3 von Sockets 4.3 konsistent sind, zu Kompatibilitätszwecken bereitgestellt werden, wird Anwendungen dringend empfohlen, die WSA-Fehlercodedefinitionen zu verwenden. Dies liegt daran, dass fehlercodes, die von bestimmten Windows Sockets-Funktionen zurückgegeben werden, in den Standardbereich von Fehlercodes fallen, wie von Microsoft C© definiert. Daher ist eine bessere Version des vorangehenden Quellcodefragments:


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



Die ursprüngliche Winsock 1.1-Spezifikation, die in 1995 definiert wurde, hat eine Reihe von Fehlercodes empfohlen und die möglichen Fehler aufgelistet, die als Ergebnis jeder Funktion zurückgegeben werden können. Windows Sockets 2 hat Funktionen und Features mit anderen Windows Sockets-Fehlercodes hinzugefügt, die zusätzlich zu den in der ursprünglichen Winsock-Spezifikation aufgeführten zurückgegeben werden. Im Laufe der Zeit wurden zusätzliche Funktionen hinzugefügt, um Winsock für die Verwendung durch Entwickler zu verbessern. Beispielsweise wurden neue Name-Dienstfunktionen (z. B.[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und [**getnameinfo)**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)hinzugefügt, die sowohl IPv6 als auch IPv4 auf Windows XP und höher unterstützen. Einige der älteren reinen IPv4-Namensdienstfunktionen (z.B. die **getXbyY-Funktionsklasse)** sind veraltet.

Eine vollständige Liste der möglichen Fehlercodes, die von Windows Sockets-Funktionen zurückgegeben werden, finden Sie im Abschnitt zu [Windows Sockets-Fehlercodes.](windows-sockets-error-codes-2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Behandeln von Winsock-Fehlern](handling-winsock-errors.md)
</dt> <dt>

[Portieren von Socketanwendungen in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows Sockets-Fehlercodes](windows-sockets-error-codes-2.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> </dl>

 

 
