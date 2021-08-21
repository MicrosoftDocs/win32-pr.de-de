---
description: Die ursprüngliche Includedatei für die Verwendung mit Windows Sockets 1.1 war die Winsock.h-Headerdatei.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: Includedateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740bde9fae96aa3088a4317c66479bcc75176ee3b9ca9f5e390365c5ef481109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051528"
---
# <a name="include-files"></a>Includedateien

Die ursprüngliche Includedatei für die Verwendung mit Windows Sockets 1.1 war die *Winsock.h-Headerdatei.* Um das Portieren von vorhandenem Quellcode basierend auf Sockets von UNIX in Windows Sockets zu vereinfachen, wurde Windows Sockets Development Kits für Winsock 1.1 empfohlen, mehrere Includedateien mit den gleichen Namen wie Standard-UNIX Includedateien (z. B. *sys/socket.h* und arpa/inet.h) zu erhalten. Diese Winsock-Headerdateien mit ähnlichem Namen enthielten jedoch lediglich eine -Anweisung, um die *Winsock2.h-Headerdatei* einzuschließen.

Als Windows Sockets 2 freigegeben wurde, wurde die primäre Includedatei für die Verwendung mit Windows Sockets in *Winsock2.h* umbenannt. Die ältere ursprüngliche *Winsock.h-Headerdatei* für Winsock 1.1 wurde aus Gründen der Kompatibilität mit älteren Anwendungen ebenfalls beibehalten. Die Entwicklung von Winsock 1.1-kompatiblen Anwendungen ist seit der Veröffentlichung von Windows 2000 veraltet. Alle Anwendungen sollten jetzt die Include *Winsock2.h-Direktive* in Winsock-Anwendungsquelldateien verwenden.

Die *Headerdatei Winsock2.h* enthält die meisten Winsock-Funktionen, -Strukturen und -Definitionen. Die *Headerdatei Ws2tcpip.h* enthält Definitionen, die im Dokument WinSock 2 Protocol-Specific Anhang für TCP/IP eingeführt wurden und neuere Funktionen und Strukturen zum Abrufen von IP-Adressen enthalten. Dazu gehören die Funktionen [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und [**getnameinfo,**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) die eine Namensauflösung für IPv4- oder IPv6-Adressen bereitstellen. Die Headerdatei *Ws2tcpip.h* ist nur erforderlich, wenn diese IP-agnostischen Benennungsfunktionen von der Anwendung benötigt werden.

Die *Headerdatei Mswsock.h* enthält Definitionen für Microsoft-spezifische Erweiterungen für die Windows Sockets 2 (z.B.[**TransmitFile,**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)und [**ConnectEx).**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) Die *Headerdatei Mswsock.h* wird normalerweise nur benötigt, wenn diese Microsoft-spezifischen Erweiterungen von der Anwendung verwendet werden.

Die *Winsock2.h-Headerdatei* enthält intern Kernelemente aus der *Headerdatei Windows.h,* sodass in Winsock-Anwendungen normalerweise keine \# Includezeile für die *Headerdatei Windows.h* vorhanden ist. Wenn \# für die *Headerdatei Windows.h* eine Includezeile erforderlich ist, sollte diesem das \# \_ Win32 LEAN AND \_ MEAN-Makro vorangestellt \_ werden. Aus historischen Gründen schließt der *Windows.h-Header* standardmäßig die *Winsock.h-Headerdatei* für Windows Sockets 1.1 ein. Die Deklarationen in der *Headerdatei "Winsock.h"* stehen in Konflikt mit den Deklarationen in der *Winsock2.h-Headerdatei,* die für Windows Sockets 2 erforderlich sind. Das WIN32 \_ LEAN \_ AND \_ MEAN-Makro verhindert, dass *winsock.h* in den *header Windows.h* eingeschlossen wird. Ein Beispiel, das dies veranschaulicht, ist unten dargestellt.


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer einfachen Winsock-Anwendung](creating-a-basic-winsock-application.md)
</dt> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Portieren von Socketanwendungen in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> </dl>

 

 
