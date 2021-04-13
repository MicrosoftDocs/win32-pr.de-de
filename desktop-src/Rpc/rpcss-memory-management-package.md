---
title: RPCSS-Speicher Verwaltungspaket
description: Das standardmäßige Zuweisungs-/zuordnerpaar, das von den Stub-und Laufzeit-Speicherplatz für die Speicher Belegung im Auftrag der Anwendung verwendet wird, ist die mittlere \_ Benutzer \_ Zuordnung/mittlere \_ Benutzer Freigabe \_ .
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473900"
---
# <a name="rpcss-memory-management-package"></a>RPCSS-Speicher Verwaltungspaket

Das standardmäßige Allocator-/zuordnerpaar, das von den Stub-und Lauf Zeit Elementen verwendet wird, wenn Speicher im Auftrag der Anwendung **belegt wird \_ \_** / **\_ \_** Allerdings können Sie das RPCSS-Paket anstelle der Standardeinstellung mithilfe des ACF-Attributs " **\[ \_ zuordnen \]**" auswählen. Das RPCSS-Paket besteht aus RPC-Funktionen, die mit dem Präfix **RPCSS** oder **rpcsm** beginnen. Das RPCSS-Paket wird für Windows-Anwendungen nicht empfohlen.

> [!Note]  
> Das RPCSS-Speicher Verwaltungspaket ist veraltet. Es wird empfohlen, dass die [**\_ Benutzer \_**](/windows/desktop/Midl/midl-user-allocate-1) Namen-und [**Mittel \_ \_ lose Benutzerzuordnungen**](/windows/desktop/Midl/midl-user-free-1) an dieser Stelle verwendet werden.

 

Im **/OSF** -Modus wird das RPCSS-Paket automatisch für die von der Mitte generierten Stub aktiviert, wenn vollständige Zeiger verwendet werden, wenn die Argumente eine Speicher Belegung erfordern oder wenn das Attribut " **\[ \_ \] zuordnen** " verwendet wird. Im Standardmodus (Microsoft Extended) ist das RPCSS-Paket nur aktiviert, wenn das Attribut " **\[ \_ zuordnen \]** " verwendet wird. Das Attribut " **\[ \_ zuordnen \]** " ermöglicht die RPCSS-Umgebung durch die serverseitigen Stub. Die Clientseite wird mit der Möglichkeit benachrichtigt, dass das RPCSS-Paket aktiviert werden kann. Im **/OSF** -Modus ist die Clientseite nicht betroffen.

Wenn das RPCSS-Paket aktiviert ist, wird die Speicher Belegung auf der Serverseite mit den privaten RPCSS-Speicher Verwaltungs Zuordnungen und dem deallokator-paar erreicht. Sie können Speicher mithilfe desselben Mechanismus zuweisen, indem Sie [**rpcsmallo(**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) oder [**rpcsszuordnen**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)) aufrufen. Bei der Rückgabe vom Serverstub wird der gesamte vom RPCSS-Paket zugewiesene Arbeitsspeicher automatisch freigegeben. Das folgende Beispiel zeigt, wie Sie das RPCSS-Paket aktivieren:

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

Die Anwendung kann durch Aufrufen der Funktion [**rpcssfree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) oder [**rpcsmfree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) explizit Arbeitsspeicher freigeben. Beachten Sie, dass diese Funktionen keinen Speicherplatz freigeben. Sie markieren Sie zum Löschen. Die RPC-Bibliothek gibt den Arbeitsspeicher frei, wenn das Programm " [**rpcssdisableallolealloleallolealloleallolealloleallole**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) [](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate)

Sie können auch die Speicher Verwaltungs Umgebung für Ihre Anwendung aktivieren, indem Sie die [**rpcsmenableallo-**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) Routine aufrufen (und Sie können Sie deaktivieren, indem Sie die Routine [**rpcsmdisablebelegungs**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) Vorgang aufrufen). Nachdem die Funktion aktiviert wurde, kann der Anwendungscode Arbeitsspeicher zuordnen und seine Freigabe durch Aufrufen von Funktionen aus dem RPCSS-Paket verringern.

 

 