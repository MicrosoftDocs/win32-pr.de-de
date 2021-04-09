---
description: Erstellen einer grundlegenden Windows Sockets (Winsock)-Anwendung
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Erstellen einer grundlegenden Winsock-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d5b5695ddb3b329bb4f81da6149fcf740a4240
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129208"
---
# <a name="creating-a-basic-winsock-application"></a>Erstellen einer grundlegenden Winsock-Anwendung

**So erstellen Sie eine Winsock-Basisanwendung**

1.  Erstellen Sie ein neues leeres Projekt.
2.  Fügen Sie dem Projekt eine leere C++-Quelldatei hinzu.
3.  Stellen Sie sicher, dass sich die Buildumgebung auf das include-, lib-und src-Verzeichnis des Microsoft Windows Software Development Kit (SDK) oder auf dem früheren Platform Software Development Kit (SDK) bezieht.
4.  Stellen Sie sicher, dass die Buildumgebung mit der Winsock-Bibliotheksdatei Ws2 \_ 32. lib verknüpft ist. Anwendungen, die Winsock verwenden, müssen mit der \_ Bibliotheksdatei Ws2 32. lib verknüpft werden. Der \# pragma-Kommentar weist den Linker an, dass die Datei *Ws2 \_ 32. lib* benötigt wird.
5.  Beginnen Sie mit dem Programmieren der Winsock-Anwendung. Verwenden Sie die Winsock-API, indem Sie die Winsock 2-Header Dateien einschließen. Die Header Datei " *Winsock2. h* " enthält die meisten WinSock-Funktionen,-Strukturen und-Definitionen. Die Header Datei " *Ws2tcpip. h* " enthält Definitionen, die im Winsock 2-Protocol-Specific Anhang-Dokument für TCP/IP eingeführt wurden und neuere Funktionen und Strukturen enthalten, die zum Abrufen von IP-Adressen verwendet werden.
    > [!Note]  
    > Stdio. h wird für die Standardeingabe und-Ausgabe verwendet, insbesondere die **printf ()** -Funktion.

     


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
> Die Header Datei " *iphlpapi. h* " ist erforderlich, wenn eine Anwendung die IP-hilfsprogrammapis verwendet. Wenn die Header Datei " *iphlpapi. h* " erforderlich ist, \# sollte die includezeile für die Header Datei " *Winsock2. h* " vor der \# Include-Zeile für die Header Datei " *iphlpapi. h* " platziert werden.
>
> Die Header Datei " *Winsock2. h* " enthält intern Kernelemente aus der Header Datei " *Windows. h* ", sodass \# in Winsock-Anwendungen normalerweise keine Include-Zeile für die Header Datei " *Windows. h* " vorhanden ist. Wenn eine \# Include-Zeile für die Header Datei " *Windows. h* " erforderlich ist, sollte diesem das \# Win32 \_ \_ -und Mean-Makro definiert werden \_ . Aus historischen Gründen hat der *Windows. h* -Header standardmäßig die *Winsock. h* -Header Datei für Windows Sockets 1,1. Die Deklarationen in der Header Datei " *Winsock. h* " verursachen einen Konflikt mit den Deklarationen in der *Winsock2. h* -Header Datei, die von Windows Sockets 2,0 benötigt wird. Das Win32 \_ \_ -und \_ Mean-Makro verhindert, dass die *Winsock. h* -Datei vom *Windows. h* -Header eingeschlossen wird. Im folgenden wird ein Beispiel gezeigt, das dies veranschaulicht.

 


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

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Informationen zu Servern und Clients](about-clients-and-servers.md)
</dt> </dl>

 

 



