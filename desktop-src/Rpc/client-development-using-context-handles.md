---
title: Client Entwicklung mithilfe von Kontext Handles
description: Die einzige Verwendung eines Client Programms für ein Kontext Handle besteht darin, dass jedes Mal, wenn der Client einen Remote Prozedur Aufruf durchführt, an den Server übergeben wird.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c7d2dfca901085c743b25eb233ee2493b893e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515981"
---
# <a name="client-development-using-context-handles"></a>Client Entwicklung mithilfe von Kontext Handles

Die einzige Verwendung eines Client Programms für ein Kontext Handle besteht darin, dass jedes Mal, wenn der Client einen Remote Prozedur Aufruf durchführt, an den Server übergeben wird. Die Client Anwendung muss nicht auf den Inhalt des Handles zugreifen können. Es sollte nicht versucht werden, die Daten des Kontext Handles in irgendeiner Weise zu ändern. Die vom Client aufgerufenen Remote Prozeduren führen alle notwendigen Vorgänge im Kontext des Servers aus.

Vor dem Anfordern eines Kontext Handles von einem Server müssen Clients eine Bindung mit dem Server herstellen. Der Client kann ein automatisches, implizites oder explizites Bindungs Handle verwenden. Mit einem gültigen Bindungs Handle kann der Client eine Remote Prozedur auf dem Server aufrufen, die entweder ein geöffnetes Kontext Handle (nicht **null**) zurückgibt oder einen **\[ out \]** -Parameter in der Parameterliste der Remote Prozedur übergibt.

Clients können geöffnete Kontext Handles in beliebiger Weise verwenden. Sie sollten das Handle jedoch für ungültig erklären, wenn es nicht mehr benötigt wird. Hierfür gibt es zwei Möglichkeiten:

-   Um eine Remote Prozedur aufzurufen, die vom Serverprogramm bereitgestellt wird, das den Kontext freigibt und das Kontext Handle schließt (legt es auf **null** fest).
-   Wenn der Server nicht erreichbar ist, müssen Sie die [**rpcssdestroyclientcontext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) -Funktion aufzurufen.

Beim zweiten Ansatz wird nur der Client seitige Zustand bereinigt, und der serverseitige Zustand wird nicht bereinigt. er sollte daher nur verwendet werden, wenn die Netzwerk Partition vermutet wird, und der Client und der Server führen eine unabhängige Bereinigung durch. Der Server führt eine unabhängige Bereinigung durch die Lauf-Down-Routine durch, und der Client führt dies mithilfe der [**rpcssdestroyclientcontext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) -Funktion aus.

Das folgende Code Fragment zeigt ein Beispiel für die Verwendung eines Kontext Handles durch einen Client. Informationen zum Anzeigen der Definition der Schnittstelle, die in diesem Beispiel verwendet wird, finden Sie unter [Schnittstellen Entwicklung mithilfe von Kontext Handles](interface-development-using-context-handles.md). Informationen zur Server Implementierung finden [Sie unter Serverentwicklung mithilfe von Kontext Handles](server-development-using-context-handles.md).

In diesem Beispiel ruft der Client remoteopen auf, um ein Kontext Handle zu erhalten, das gültige Daten enthält. Der Client kann dann das Kontext Handle in Remote Prozedur aufrufen verwenden. Da das Bindungs Handle nicht mehr benötigt wird, kann der Client das explizite handle freigeben, das zum Erstellen des Kontext Handles verwendet wurde:


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



Die Client Anwendung in diesem Beispiel verwendet eine Prozedur namens RemoteRead, um eine Datendatei auf dem Server zu lesen, bis das Ende der Datei gefunden wird. Anschließend wird die Datei durch Aufrufen von remoteclose geschlossen. Das Kontext Handle wird als Parameter in den Funktionen RemoteRead und remoteclose wie folgt angezeigt:


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



 

 




