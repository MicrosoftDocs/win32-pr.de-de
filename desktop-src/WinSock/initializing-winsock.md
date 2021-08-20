---
description: Alle Prozesse (Anwendungen oder DLLs), die Winsock-Funktionen aufrufen, müssen die Verwendung der Windows Sockets-DLL initialisieren, bevor andere Winsock-Funktionen aufrufen. Dadurch wird auch sicher, dass Winsock auf dem System unterstützt wird.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Initialisieren von Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aad1dc5bffb09490a963bd86c61c6cc2a857fec45251b38111ab790db8a26e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051518"
---
# <a name="initializing-winsock"></a>Initialisieren von Winsock

Alle Prozesse (Anwendungen oder DLLs), die Winsock-Funktionen aufrufen, müssen die Verwendung der Windows Sockets-DLL initialisieren, bevor andere Winsock-Funktionen aufrufen. Dadurch wird auch sicher, dass Winsock auf dem System unterstützt wird.

**So initialisieren Sie Winsock**

1.  Erstellen Sie ein [**WSADATA-Objekt**](/windows/desktop/api/winsock/ns-winsock-wsadata) mit dem Namen wsaData.
    ```C++
    WSADATA wsaData;
    ```

    

2.  Rufen [**Sie WSAStartup auf,**](/windows/desktop/api/winsock/nf-winsock-wsastartup) und geben Sie dessen Wert als ganze Zahl zurück, und überprüfen Sie auf Fehler.
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

Die [**WSAStartup-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsastartup) wird aufgerufen, um die Verwendung von WS2-32.dll. \_

Die [**WSADATA-Struktur**](/windows/desktop/api/winsock/ns-winsock-wsadata) enthält Informationen zur Windows Sockets-Implementierung. Der MAKEWORD(2,2)-Parameter von [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) stellt eine Anforderung für Version 2.2 von Winsock auf dem System und legt die übergebene Version als höchste Version der Windows Sockets-Unterstützung fest, die der Aufrufer verwenden kann.

Nächster Schritt für einen Client: [Erstellen eines Sockets für den Client](creating-a-socket-for-the-client.md)

Nächster Schritt für einen Server: [Erstellen eines Sockets für den Server](creating-a-socket-for-the-server.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Erstellen einer einfachen Winsock-Anwendung](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



