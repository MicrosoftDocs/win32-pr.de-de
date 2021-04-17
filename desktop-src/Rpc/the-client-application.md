---
title: Die Clientanwendung
description: Das folgende Beispiel ist aus der "Hallo Welt"-Anwendung im Verzeichnis "RPC \\ Hello" des Platform Software Development Kit (SDK).
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f97c7c35e00d3f36c645bfad2825dbada5e3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474037"
---
# <a name="the-client-application"></a>Die Clientanwendung

Das folgende Beispiel ist aus der "Hallo Welt"-Anwendung im Verzeichnis "RPC \\ Hello" des Platform Software Development Kit (SDK). Die Quelldatei helloc. c enthält eine Direktive, die die von der Mittel l generierte Header Datei Hello. h einschließt. In "Hello. h" sind Direktiven zum Einschließen von RPC. h und Rpcndr. h enthalten, die die Definitionen für die RPC-Lauf Zeit Routinen, **helloproc** und **Shutdown** sowie die Datentypen enthalten, die von den Client-und Server Anwendungen verwendet werden. Der mittlerer l-Compiler muss mit dem folgenden Beispiel verwendet werden.

Da der Client seine Verbindung mit dem Server verwaltet, ruft die Client Anwendung Lauf Zeitfunktionen auf, um ein Handle für den Server einzurichten und dieses Handle freizugeben, nachdem die Remote Prozedur Aufrufe beendet wurden. Die Funktion [**rpcstringbindingcompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) kombiniert die Komponenten des Bindungs Handles zu einer Zeichen folgen Darstellung des Handles und ordnet Speicher für die Zeichen folgen Bindung zu. Die Funktion [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) erstellt ein Server Bindungs handle, **Hello \_ clientibhandle**, für die Client Anwendung aus dieser Zeichen folgen Darstellung.

Beim Aufrufen von [**rpcstringbindingcompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose)geben die Parameter nicht die UUID an, da in diesem Tutorial davon ausgegangen wird, dass es nur eine Implementierung der Schnittstelle "Hello" gibt. Außerdem gibt der-Befehl keine Netzwerkadresse an, da die Anwendung den Standardwert verwendet, bei dem es sich um den lokalen Host Computer handelt. Die Protokoll Sequenz ist eine Zeichenfolge, die den zugrunde liegenden Netzwerk Transport darstellt. Der Endpunkt ist ein Name, der spezifisch für die Protokoll Sequenz ist. In diesem Beispiel werden Named Pipes für den Netzwerk Transport verwendet, sodass die Protokoll Sequenz "ncacn \_ NP" lautet. Der Endpunkt Name ist " \\ Pipe \\ Hello".

Die eigentlichen Remote Prozedur Aufrufe, **helloproc** und **Shutdown**, erfolgen innerhalb des RPC-Ausnahme Handlers – mit einem Satz von Makros, mit denen Sie Ausnahmen steuern können, die außerhalb des Anwendungs Codes auftreten. Wenn das RPC-Lauf Zeit Modul eine Ausnahme meldet, wird die Steuerung an den [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) -Block weitergeleitet. Hier fügen Sie Code ein, um alle benötigten Bereinigungs Vorgänge durchzuführen und dann ordnungsgemäß zu beenden. Dieses Beispielprogramm informiert den Benutzer einfach darüber, dass eine Ausnahme aufgetreten ist. Wenn Sie keine Ausnahmen verwenden möchten, können Sie die ACF-Attribute " [comm- \_ Status](/windows/desktop/Midl/comm-status) " und " [Fehler \_ Status](/windows/desktop/Midl/fault-status) " verwenden, um Fehler zu melden.

Nachdem die Remote Prozedur Aufrufe abgeschlossen sind, ruft der Client zuerst [**rpcstringfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) auf, um den Arbeitsspeicher freizugeben, der für die Zeichen folgen Bindung reserviert wurde. Beachten Sie, dass ein Client Programm eine Zeichen folgen Bindung jederzeit freigeben kann, sobald das Bindungs Handle erstellt wurde. Der Client ruft dann [**rpcbindingfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) auf, um das Handle freizugeben.


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



 

 