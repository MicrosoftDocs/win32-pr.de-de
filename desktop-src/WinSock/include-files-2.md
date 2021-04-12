---
description: Die ursprüngliche Includedatei für die Verwendung mit Windows Sockets 1,1 war die Header Datei "Winsock. h".
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: Includedateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf7a4edcd70e6a6280b26f7b6ab9f0f1dab674e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343499"
---
# <a name="include-files"></a>Includedateien

Die ursprüngliche Includedatei für die Verwendung mit Windows Sockets 1,1 war die Header Datei " *Winsock. h* ". Zum Vereinfachen der Portierung von vorhandenem Quellcode auf der Grundlage von Berkeley-socketsockets auf Windows Sockets wurde empfohlen, dass Windows Sockets Development Kits für Winsock 1,1 mit mehreren Includedateien mit denselben Namen wie standardmäßige UNIX-Includedateien (z. b. *sys/Socket. h* -und ARPA/inet. h-Header Dateien) bereitgestellt werden. Diese Winsock-Header Dateien mit ähnlichen Namen enthielten jedoch lediglich eine-Direktive, um die Header Datei " *Winsock2. h* " einzuschließen.

Wenn Windows Sockets 2 freigegeben wurde, wurde die primäre Includedatei für die Verwendung mit Windows Sockets in *Winsock2. h* umbenannt. Die ältere Original- *Winsock. h* -Header Datei für Winsock 1,1 wurde ebenfalls für die Kompatibilität mit älteren Anwendungen beibehalten. Die Entwicklung von mit Winsock 1,1 kompatiblen Anwendungen wurde seit der Veröffentlichung von Windows 2000 als veraltet markiert. Alle Anwendungen sollten jetzt die include *Winsock2. h* -Direktive in Winsock-Anwendungs Quelldateien verwenden.

Die Header Datei " *Winsock2. h* " enthält die meisten WinSock-Funktionen,-Strukturen und-Definitionen. Die Header Datei " *Ws2tcpip. h* " enthält Definitionen, die im Winsock 2-Protocol-Specific Anhang-Dokument für TCP/IP eingeführt wurden und neuere Funktionen und Strukturen enthalten, die zum Abrufen von IP-Adressen verwendet werden. Hierzu gehören die [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -und die [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) -Familie von Funktionen, die die Namensauflösung für IPv4-oder IPv6-Adressen bereitstellen. Die Header Datei " *Ws2tcpip. h* " ist nur erforderlich, wenn diese IP-agnostischen Benennungs Funktionen von der Anwendung benötigt werden.

Die Header Datei " *mtausock. h* " enthält Definitionen für Microsoft-spezifische Erweiterungen für Windows Sockets 2 (z. b.[**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**Accept tex**](/windows/win32/api/mswsock/nf-mswsock-acceptex)und [**connectex**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)). Die Header Datei " *mswap. h* " ist normalerweise nicht erforderlich, es sei denn, diese Microsoft-spezifischen Erweiterungen werden von der Anwendung verwendet.

Die Header Datei " *Winsock2. h* " enthält intern Kernelemente aus der Header Datei " *Windows. h* ", sodass \# in Winsock-Anwendungen normalerweise keine Include-Zeile für die Header Datei " *Windows. h* " vorhanden ist. Wenn eine \# Include-Zeile für die Header Datei " *Windows. h* " erforderlich ist, sollte diesem das \# Win32 \_ \_ -und Mean-Makro definiert werden \_ . Aus historischen Gründen hat der *Windows. h* -Header standardmäßig die *Winsock. h* -Header Datei für Windows Sockets 1,1. Die Deklarationen in der Header Datei " *Winsock. h* " verursachen einen Konflikt mit den Deklarationen in der *Winsock2. h* -Header Datei, die von Windows Sockets 2 benötigt wird. Das Win32 \_ \_ -und \_ Mean-Makro verhindert, dass die *Winsock. h* -Datei vom *Windows. h* -Header eingeschlossen wird. Im folgenden wird ein Beispiel gezeigt, das dies veranschaulicht.


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

[Erstellen einer grundlegenden Winsock-Anwendung](creating-a-basic-winsock-application.md)
</dt> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Portieren von Socketanwendungen auf Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> </dl>

 

 
