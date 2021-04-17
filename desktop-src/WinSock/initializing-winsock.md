---
description: Alle Prozesse (Anwendungen oder DLLs), die Winsock-Funktionen aufrufen, müssen die Verwendung der Windows Sockets-DLL initialisieren, bevor andere Winsock-Funktionen aufgerufen werden. Dadurch wird auch sicherstellt, dass Winsock auf dem System unterstützt wird.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Initialisieren von Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526159"
---
# <a name="initializing-winsock"></a>Initialisieren von Winsock

Alle Prozesse (Anwendungen oder DLLs), die Winsock-Funktionen aufrufen, müssen die Verwendung der Windows Sockets-DLL initialisieren, bevor andere Winsock-Funktionen aufgerufen werden. Dadurch wird auch sicherstellt, dass Winsock auf dem System unterstützt wird.

**So initialisieren Sie Winsock**

1.  Erstellen Sie ein [**wsadata**](/windows/desktop/api/winsock/ns-winsock-wsadata) -Objekt namens wsadata.
    ```C++
    WSADATA wsaData;
    ```

    

2.  Nennen Sie [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) , und geben Sie den Wert als Ganzzahl zurück, und suchen Sie nach Fehlern.
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

Die [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Funktion wird aufgerufen, um die Verwendung von ws2-32.dll zu initiieren \_ .

Die [**wsadata**](/windows/desktop/api/winsock/ns-winsock-wsadata) -Struktur enthält Informationen über die Windows Sockets-Implementierung. Der makeword (2, 2)-Parameter von [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) stellt eine Anforderung für die Version 2,2 von Winsock im System her und legt die übergebenen Version als höchste Version der Windows Sockets-Unterstützung fest, die der Aufrufer verwenden kann.

Nächster Schritt für einen Client: [Erstellen eines Sockets für den Client](creating-a-socket-for-the-client.md)

Nächster Schritt für einen Server: [Erstellen eines Sockets für den Server](creating-a-socket-for-the-server.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Erstellen einer grundlegenden Winsock-Anwendung](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



