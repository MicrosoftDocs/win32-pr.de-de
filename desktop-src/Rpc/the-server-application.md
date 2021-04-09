---
title: Die Server Anwendung
description: Das folgende Beispiel ist aus der "Hallo Welt"-Anwendung im Verzeichnis "RPC \\ Hello" des Platform Software Development Kit (SDK).
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6f13e2c8fecdcff820c62f3076dd2a8edd1a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856196"
---
# <a name="the-server-application"></a>Die Server Anwendung

Das folgende Beispiel ist aus der "Hallo Welt"-Anwendung im Verzeichnis "RPC \\ Hello" des Platform Software Development Kit (SDK). Die Serverseite der verteilten Anwendung informiert das System darüber, dass die zugehörigen Dienste verfügbar sind. Dann wartet er auf Client Anforderungen. Der mittlerer l-Compiler muss mit dem folgenden Beispiel verwendet werden.

Abhängig von der Größe Ihrer Anwendung und ihren Codierungs Einstellungen können Sie auswählen, dass Remote Prozeduren in einer oder mehreren separaten Dateien implementiert werden. In diesem Tutorial-Programm enthält die Quelldatei hellos. c die Hauptserver Routine. Die Datei hellop. c enthält die Remote Prozedur.

Der Vorteil der Organisation der Remote Prozeduren in separaten Dateien besteht darin, dass die Prozeduren mit einem eigenständigen Programm verknüpft werden können, um den Code vor der Konvertierung in eine verteilte Anwendung zu debuggen. Wenn die Prozeduren im eigenständigen Programm funktionieren, können Sie die Quelldateien, die die Remote Prozeduren enthalten, mit der Serveranwendung kompilieren und verknüpfen. Wie bei der Quelldatei der Client Anwendung muss die Quelldatei für die Serveranwendung die Header Datei "Hello. h" enthalten.

Der Server Ruft die RPC-Lauf Zeitfunktionen [**rpcserveruseprotabqep**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) und [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) auf, um dem Client Bindungs Informationen zur Verfügung zu stellen. Dieses Beispielprogramm übergibt den Namen des Schnittstellen Handles an **RpcServerRegisterIf**. Die anderen Parameter werden auf **null** festgelegt. Der Server ruft dann die [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) -Funktion auf, um anzugeben, dass Sie auf Client Anforderungen wartet.

Die Serveranwendung muss auch die beiden Speicherverwaltungsfunktionen enthalten, die der Serverstub aufruft: [**mittlere \_ Benutzer \_**](the-midl-user-allocate-function.md) Zuordnungen und [**mittlerer l- \_ Benutzer \_ kostenlos**](the-midl-user-free-function.md). Diese Funktionen weisen Arbeitsspeicher auf dem Server zu und verteilen ihn frei, wenn eine Remote Prozedur Parameter an den Server übergibt. In diesem Beispielprogramm sind die **Mittel l- \_ Benutzer \_** Zuordnungen und die **\_ Benutzer \_ Freihand für mittlere Benutzer** einfach Wrapper für die C-Bibliotheksfunktionen [**malloc**](pointers-and-memory-allocation.md) und **Free**. (Beachten Sie, dass in der vom Compiler generierten Forward-Deklarationen "Mittel l" in Großbuchstaben vorliegt. Die Header Datei Rpcndr. h definiert mittlere \_ Benutzer freie und mittlere Benutzer Zuordnungen, \_ die als \_ \_ mittlere \_ Benutzer \_ kostenfrei \_ \_ sind, bzw. Benutzer Zuordnungen.


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
 }

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 




