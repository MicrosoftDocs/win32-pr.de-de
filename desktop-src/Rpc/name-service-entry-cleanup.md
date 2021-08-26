---
title: Name Service Entry Cleanup
description: Ein Namensdiensteintrag sollte Informationen enthalten, die sich nicht häufig ändern.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe7484d1c6d557899e3b661a3a616c97d3890becfad51df0e91f5a69467faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019605"
---
# <a name="name-service-entry-cleanup"></a>Name Service Entry Cleanup

Ein Namensdiensteintrag sollte Informationen enthalten, die sich nicht häufig ändern. Schließen Sie aus diesem Grund keine dynamischen Endpunkte in die exportierten Bindungshandles ein, da sie sich bei jedem Aufruf des Servers ändern und Den Namensdiensteintrag überladen. Verwenden Sie [**RpcBindingReset,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)um diese Bindungshandles zu entfernen.

Eine sinnvolle Abfolge von Servervorgängen wäre beispielsweise:

Für mehrere Transporte:

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

So platzieren Sie Bindungen in der Endpunktzuordnung:

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

So entfernen Sie Endpunkte aus Bindungen:

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

So fügen Sie dem Namensdienst Bindungen hinzu:

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




