---
description: Erstellen einer einfachen Windows Sockets (Winsock)-Anwendung.
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Erstellen einer einfachen Winsock-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67b13acc0ae80242fb747415d457e6809895c38cd81878224cad2ffe130b2536
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860950"
---
# <a name="creating-a-basic-winsock-application"></a>Erstellen einer einfachen Winsock-Anwendung

**So erstellen Sie eine einfache Winsock-Anwendung**

1.  Erstellen Sie ein neues leeres Projekt.
2.  Fügen Sie dem Projekt eine leere C++-Quelldatei hinzu.
3.  Stellen Sie sicher, dass die Buildumgebung auf die Verzeichnisse Include, Lib und Src des Microsoft Windows Software Development Kit (SDK) oder des früheren Platform Software Development Kit (SDK) verweist.
4.  Stellen Sie sicher, dass die Buildumgebung mit der Winsock Library-Datei Ws2 \_ 32.lib verknüpft ist. Anwendungen, die Winsock verwenden, müssen mit der Bibliotheksdatei Ws2 \_ 32.lib verknüpft werden. Der \# Pragmakommentar zeigt dem Linker an, dass die *Datei Ws2 \_ 32.lib* benötigt wird.
5.  Beginnen Sie mit dem Programmieren der Winsock-Anwendung. Verwenden Sie die Winsock-API, indem Sie die Winsock 2-Headerdateien hinzufügen. Die *Winsock2.h-Headerdatei* enthält die meisten Winsock-Funktionen, -Strukturen und -Definitionen. Die *Ws2tcpip.h-Headerdatei* enthält Definitionen, die im WinSock 2 Protocol-Specific-Anhang für TCP/IP eingeführt wurden und neuere Funktionen und Strukturen zum Abrufen von IP-Adressen enthalten.
    > [!Note]  
    > Stdio.h wird für die Standardeingabe und -ausgabe verwendet, insbesondere für **die printf()-Funktion.**

     


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



> [!Note]
>
> Die *Headerdatei Iphlpapi.h* ist erforderlich, wenn eine Anwendung die IP-Hilfs-APIs verwendet. Wenn die *Headerdatei Iphlpapi.h* erforderlich ist, sollte die Includezeile für die \# *Headerdatei "Winsock2.h"* vor der Includezeile für die \# *Headerdatei "Iphlpapi.h"* platziert werden.
>
> Die *Winsock2.h-Headerdatei* enthält intern Kernelemente aus der *Headerdatei "Windows.h",* sodass es in Winsock-Anwendungen in der Regel keine Includezeile für die \# *Headerdatei "Windows.h"* gibt. Wenn eine \# Includezeile für die *Headerdatei Windows.h* erforderlich ist, sollte diesem das \# WIN32 LEAN AND MEAN-Makro definieren \_ \_ \_ voranstehen. Aus historischen Gründen wird für *Windows.h-Header* standardmäßig die *Headerdatei Winsock.h* für Windows Sockets 1.1 verwendet. Die Deklarationen in der *Winsock.h-Headerdatei* stehen in Konflikt mit den Deklarationen in der *Winsock2.h-Headerdatei,* die für Windows Sockets 2.0 erforderlich sind. Das WIN32 \_ LEAN \_ AND \_ MEAN-Makro verhindert, dass *winsock.h* im Header *Windows.h enthalten* ist. Ein Beispiel, das dies veranschaulicht, ist unten dargestellt.

 


```C++
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



Nächster Schritt: [Initialisieren von Winsock](initializing-winsock.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Informationen zu Servern und Clients](about-clients-and-servers.md)
</dt> </dl>

 

 



