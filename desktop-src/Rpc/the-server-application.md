---
title: Die Serveranwendung
description: Zeigen Sie den Serveranwendungsteil eines RPC-Beispiels (Remote Procedure Call) an. Das Beispiel stammt aus der Anwendung "Hallo Welt" im Plattform-SDK.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c393e16a4c26b39efb95d23a2745f75cbeb984cac466c869046f9775f94c80c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923989"
---
# <a name="the-server-application"></a>Die Serveranwendung

Das folgende Beispiel stammt aus der Anwendung "Hallo Welt" im VERZEICHNIS RPC \\ Hello des Platform Software Development Kit (SDK). Die Serverseite der verteilten Anwendung informiert das System darüber, dass seine Dienste verfügbar sind. Anschließend wird auf Clientanforderungen gewartet. Der MIDL-Compiler muss mit dem folgenden Beispiel verwendet werden.

Abhängig von der Größe Ihrer Anwendung und Ihren Codierungseinstellungen können Sie Remoteprozeduren in einer oder mehreren separaten Dateien implementieren. In diesem Tutorialprogramm enthält die Quelldatei Hellos.c die Hauptserverroutine. Die Datei Hellop.c enthält die Remoteprozedur.

Der Vorteil der Organisation der Remoteprozeduren in separaten Dateien besteht darin, dass die Prozeduren mit einem eigenständigen Programm verknüpft werden können, um den Code zu debuggen, bevor er in eine verteilte Anwendung konvertiert wird. Nachdem die Prozeduren im eigenständigen Programm funktionieren, können Sie die Quelldateien, die die Remoteprozeduren enthalten, kompilieren und mit der Serveranwendung verknüpfen. Wie bei der Clientanwendungsquelldatei muss die Quelldatei der Serveranwendung die Headerdatei Hello.h enthalten.

Der Server ruft die RPC-Laufzeitfunktionen [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) und [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) auf, um dem Client Bindungsinformationen zur Verfügung zu stellen. Dieses Beispielprogramm übergibt den Schnittstellenhandlenamen an **RpcServerRegisterIf.** Die anderen Parameter werden auf **NULL** festgelegt. Der Server ruft dann die [**RpcServerListen-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) auf, um anzugeben, dass auf Clientanforderungen gewartet wird.

Die Serveranwendung muss auch die beiden Speicherverwaltungsfunktionen enthalten, die der Serverstub aufruft: [**midl \_ user \_ allocate**](the-midl-user-allocate-function.md) und [**midl \_ user \_ free**](the-midl-user-free-function.md). Diese Funktionen belegen Und freigeben Arbeitsspeicher auf dem Server, wenn eine Remoteprozedur Parameter an den Server übergibt. In diesem Beispielprogramm sind **midl \_ user \_ allocate** und **midl \_ user \_ free** einfach Wrapper für die C-Bibliotheksfunktionen [**malloc**](pointers-and-memory-allocation.md) und **free.** (Beachten Sie, dass "MIDL" in den vom MIDL-Compiler generierten Vorwärtsdeklarationen groß geschrieben ist. Die Headerdatei Rpcndr.h definiert midl \_ user \_ free und midl user allocate als \_ \_ MIDL user free \_ \_ bzw. MIDL \_ user \_ allocate.)


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



 

 




