---
title: Cliententwicklung mitHilfe von Kontexthandles
description: Die einzige Verwendung eines Clientprogramms für ein Kontexthand handle besteht in der Übergeben dieses An den Server bei jedem Aufruf einer Remoteprozedur durch den Client.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ff599bebdf042bc2021d53538cff1c0203d2de875bdc52c50a72675b73a47f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931841"
---
# <a name="client-development-using-context-handles"></a>Cliententwicklung mitHilfe von Kontexthandles

Die einzige Verwendung eines Clientprogramms für ein Kontexthand handle besteht in der Übergeben dieses An den Server bei jedem Aufruf einer Remoteprozedur durch den Client. Die Clientanwendung muss nicht auf den Inhalt des Handle zugreifen. Es sollte nicht versucht werden, die Kontexthand handle-Daten in irgendeiner Weise zu ändern. Die Remoteverfahren, die der Client aufruft, führen alle erforderlichen Vorgänge im Kontext des Servers aus.

Vor dem Anfordern eines Kontexthandpunkts von einem Server müssen Clients eine Bindung mit dem Server herstellen. Der Client kann ein automatisches, implizites oder explizites Bindungshand handle verwenden. Mit einem gültigen Bindungshand handle kann der Client eine Remoteprozedur auf dem Server aufrufen, die entweder ein geöffnetes Kontexthand handle (nicht **NULL)** zurückgibt oder eines über einen **\[ out-Parameter \]** in der Parameterliste der Remoteprozedur übergibt.

Clients können geöffnete Kontexthandles auf jede Weise verwenden, die sie benötigen. Sie sollten das Handle jedoch für ungültig erklären, wenn es nicht mehr benötigt wird. Es gibt zwei Wege, dies zu tun:

-   So rufen Sie eine Remoteprozedur auf, die vom Serverprogramm angeboten wird, das den Kontext freigibt und das Kontexthand handle schließt (legt es auf **NULL fest).**
-   Wenn der Server nicht erreichbar ist, rufen Sie die [**RpcSsDestroyClientContext-Funktion**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) auf.

Der zweite Ansatz bereinigt nur den clientseitigen Zustand und nicht den serverseitigen Zustand. Daher sollte er nur verwendet werden, wenn eine Netzwerkpartition vermutet wird, und der Client und der Server werden eine unabhängige Bereinigung ausführen. Der Server führt eine unabhängige Bereinigung durch die Run-Down-Routine durch. Der Client verwendet dazu die [**RpcSsDestroyClientContext-Funktion.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext)

Das folgende Codefragment zeigt ein Beispiel dafür, wie ein Client ein Kontexthand handle verwenden kann. Informationen zum Anzeigen der Definition der Schnittstelle, die in diesem Beispiel verwendet wird, finden Sie unter [Schnittstellenentwicklung mithilfe von Kontexthandles.](interface-development-using-context-handles.md) Informationen zur Serverimplementierung finden Sie unter [Serverentwicklung mithilfe von Kontexthandles.](server-development-using-context-handles.md)

In diesem Beispiel ruft der Client RemoteOpen auf, um ein Kontexthand handle zu erhalten, das gültige Daten enthält. Der Client kann dann das Kontexthand handle in Remoteprozeduraufrufen verwenden. Da das Bindungshand handle nicht mehr benötigt wird, kann der Client das explizite Handle, das er zum Erstellen des Kontexthandpunkts verwendet hat, frei verwenden:


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



Die Clientanwendung in diesem Beispiel verwendet eine Prozedur namens RemoteRead, um eine Datendatei auf dem Server zu lesen, bis ein Dateiende vorgelegen hat. Anschließend wird die Datei durch Aufrufen von RemoteClose geschlossen. Das Kontexthandles wird als Parameter in den Funktionen RemoteRead und RemoteClose angezeigt:


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




