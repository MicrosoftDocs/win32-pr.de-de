---
title: RpcSs-Speicherverwaltungspaket
description: Das standarde Zuweisungs-/Zuordnungspaar, das von den Stubs und der Laufzeit beim Zuweisen von Arbeitsspeicher im Auftrag der Anwendung verwendet wird, ist midl \_ user \_ allocate/midl \_ user \_ free.
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93648b56ed47eb98a83b27a39b606fa2a51de9bf5791ad1b732e7169ef5dfa63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018180"
---
# <a name="rpcss-memory-management-package"></a>RpcSs-Speicherverwaltungspaket

Das standarde Zuweisungs-/Zuordnungspaar, das von den Stubs und der Laufzeit beim Zuweisen von Arbeitsspeicher im Auftrag der Anwendung verwendet wird, ist **midl \_ user \_ allocate** / **midl \_ user \_ free**. Sie können jedoch das RpcSs-Paket anstelle des Standardpakets auswählen, indem Sie das ACF-Attribut **\[ enable \_ allocate \] verwenden.** Das RpcSs-Paket besteht aus RPC-Funktionen, die mit dem Präfix **RpcSs** oder **RpcSm** beginnen. Das RpcSs-Paket wird für Windows Anwendungen nicht empfohlen.

> [!Note]  
> Das Rpcss-Speicherverwaltungspaket ist veraltet. Es wird empfohlen, [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) und [**midl \_ user \_ free**](/windows/desktop/Midl/midl-user-free-1) an seiner Stelle zu verwenden.

 

Im **Modus /osf** wird das RpcSs-Paket automatisch für MIDL-generierte Stubs aktiviert, wenn vollständige Zeiger verwendet werden, wenn die Argumente eine Speicherbelegung erfordern oder das **\[ Attribut enable \_ allocate \]** verwendet wird. Im Standardmodus (Erweitert von Microsoft) ist das RpcSs-Paket nur aktiviert, wenn das **\[ Attribut enable \_ allocate \]** verwendet wird. Das **\[ Attribut enable \_ allocate \]** aktiviert die RpcSs-Umgebung durch die serverseitigen Stubs. Die Clientseite wird über die Möglichkeit benachrichtigt, dass das RpcSs-Paket aktiviert werden kann. Im **Modus /osf** ist die Clientseite nicht betroffen.

Wenn das RpcSs-Paket aktiviert ist, wird die Speicherbelegung auf serverseitiger Seite mit dem privaten RpcSs-Speicherverwaltungszuordnungs- und -Zuordnungspaar erreicht. Sie können Arbeitsspeicher mit demselben Mechanismus zuordnen, indem [**Sie RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (oder [**RpcSsAllocate)**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)aufrufen. Nach der Rückgabe vom Serverstub wird der gesamte vom RpcSs-Paket belegte Arbeitsspeicher automatisch freigegeben. Das folgende Beispiel zeigt, wie das RpcSs-Paket aktiviert wird:

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

Ihre Anwendung kann explizit Arbeitsspeicher freigeben, indem sie die [**RpcSsFree-**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) oder [**RpcSmFree-Funktion**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) aufruft. Beachten Sie, dass diese Funktionen nicht tatsächlich Arbeitsspeicher freigeben. Sie markieren sie zum Löschen. Die RPC-Bibliothek gibt den Arbeitsspeicher frei, wenn Ihr Programm [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) oder [**RpcSsDisableAllocate aufruft.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate)

Sie können auch die Speicherverwaltungsumgebung für Ihre Anwendung aktivieren, indem Sie die [**RpcSmEnableAllocate-Routine**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) aufrufen (und sie deaktivieren, indem Sie die [**RpcSmDisableAllocate-Routine**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) aufrufen). Nach der Aktivierung kann der Anwendungscode Arbeitsspeicher zuweisen und die Zuordnung wieder aufteilen, indem Funktionen aus dem RpcSs-Paket aufgerufen werden.

 

 