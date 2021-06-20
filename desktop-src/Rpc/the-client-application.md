---
title: Die Clientanwendung
description: Zeigen Sie den Clientanwendungsteil eines RPC-Beispiels (Remote Procedure Call) an. Das folgende Beispiel ist aus der Anwendung "Hallo Welt" im Platform SDK.
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e0b798543cd70e61f3ff1161503fa64710e53e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405013"
---
# <a name="the-client-application"></a>Die Clientanwendung

Das folgende Beispiel ist aus der Anwendung "Hallo Welt" im RPC \\ Hello-Verzeichnis des Platform Software Development Kit (SDK) enthalten. Die Helloc.c-Quelldatei enthält eine -Direktive, die die von MIDL generierte Headerdatei Hello.h enthält. In Hello.h sind -Anweisungen enthalten, die Rpc.h und rpcndr.h enthalten, die die Definitionen für die RPC-Laufzeitroutinen, **HelloProc** und **Shutdown** sowie die Datentypen enthalten, die die Client- und Serveranwendungen verwenden. Der MIDL-Compiler muss mit dem folgenden Beispiel verwendet werden.

Da der Client seine Verbindung mit dem Server verwalten soll, ruft die Clientanwendung Laufzeitfunktionen auf, um ein Handle für den Server herzustellen und dieses Handle frei zu geben, nachdem die Remoteprozeduraufrufe abgeschlossen sind. Die [**Funktion RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) kombiniert die Komponenten des Bindungshandpunkts in einer Zeichenfolgendarstellung dieses Handle und ordnet Arbeitsspeicher für die Zeichenfolgenbindung zu. Die Funktion [**RpcBindingFromStringBinding erstellt**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) aus dieser Zeichenfolgendarstellung das Serverbindungshandle **hello \_ ClientIfHandle** für die Clientanwendung.

Beim Aufruf von [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose)geben die Parameter die UUID nicht an, da in diesem Tutorial davon ausgegangen wird, dass es nur eine Implementierung der Schnittstelle "hello" gibt. Darüber hinaus gibt der Aufruf keine Netzwerkadresse an, da die Anwendung die Standardeinstellung verwendet, bei der es sich um den lokalen Hostcomputer handelt. Die Protokollsequenz ist eine Zeichenfolge, die den zugrunde liegenden Netzwerktransport darstellt. Der Endpunkt ist ein Name, der für die Protokollsequenz spezifisch ist. In diesem Beispiel werden Named Pipes für den Netzwerktransport verwendet, sodass die Protokollsequenz "ncacn \_ np" ist. Der Endpunktname ist \\ "pipe \\ hello".

Die tatsächlichen Remoteprozeduraufrufe **HelloProc** und **Shutdown** erfolgen innerhalb des RPC-Ausnahmehandlers– einer Reihe von Makros, mit denen Sie Ausnahmen steuern können, die außerhalb des Anwendungscodes auftreten. Wenn das RPC-Laufzeitmodul eine Ausnahme meldet, wird die Steuerung an den [**RpcExcept-Block**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) übergibt. Hier fügen Sie Code ein, um alle erforderlichen Bereinigungen zu ausführen und dann ordnungsgemäß zu beenden. Dieses Beispielprogramm informiert den Benutzer lediglich darüber, dass eine Ausnahme aufgetreten ist. Wenn Sie keine Ausnahmen verwenden möchten, können Sie die ACF-Attribute [comm \_ status](/windows/desktop/Midl/comm-status) und [fault \_ status](/windows/desktop/Midl/fault-status) verwenden, um Fehler zu melden.

Nachdem die Remoteprozeduraufrufe abgeschlossen sind, ruft der Client zuerst [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) auf, um den Arbeitsspeicher frei zu geben, der für die Zeichenfolgenbindung zugeordnet wurde. Beachten Sie, dass ein Clientprogramm nach dem Erstellen des Bindungshandpunkts jederzeit eine Zeichenfolgenbindung freigibt. Der Client ruft als Nächstes [**RpcBindingFree auf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) um das Handle frei zu geben.


```C++
/* file: helloc.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h" 
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszUuid             = NULL;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszNetworkAddress   = NULL;
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned char * pszOptions          = NULL;
    unsigned char * pszStringBinding    = NULL;
    unsigned char * pszString           = "hello, world";
    unsigned long ulCode;
 
    status = RpcStringBindingCompose(pszUuid,
                                     pszProtocolSequence,
                                     pszNetworkAddress,
                                     pszEndpoint,
                                     pszOptions,
                                     &pszStringBinding);
    if (status) exit(status);

    status = RpcBindingFromStringBinding(pszStringBinding, &hello_ClientIfHandle);
 
    if (status) exit(status);
 
    RpcTryExcept  
    {
        HelloProc(pszString);
        Shutdown();
    }
    RpcExcept(1) 
    {
        ulCode = RpcExceptionCode();
        printf("Runtime reported exception 0x%lx = %ld\n", ulCode, ulCode);
    }
    RpcEndExcept
 
    status = RpcStringFree(&pszStringBinding); 
 
    if (status) exit(status);
 
    status = RpcBindingFree(&hello_IfHandle);
 
    if (status) exit(status);

    exit(0);
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



 

 