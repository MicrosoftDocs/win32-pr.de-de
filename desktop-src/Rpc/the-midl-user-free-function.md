---
title: Die midl_user_free-Funktion
description: Die \_ kostenlose \_ Midl-Benutzerfunktion muss von RPC-Entwicklern bereitgestellt werden.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6ca52635da5bedb60fdc7f94165ad9c888c030d5fe3340c53dfc970a90ff49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080820"
---
# <a name="the-midl_user_free-function"></a>Die \_ kostenlose \_ Midl-Benutzerfunktion

Die **kostenlose Midl-Benutzerfunktion \_ \_** muss von RPC-Entwicklern bereitgestellt werden. Es belegt Arbeitsspeicher für die RPC-Stubs und Bibliotheksroutinen. Ihre **\_ \_ kostenlose Midl-Benutzerfunktion** muss mit dem folgenden Prototyp übereinstimmen:

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

Der *pBuffer-Parameter* gibt einen Zeiger auf den Speicher an, der freigegeben werden soll. Sowohl die Clientanwendung als auch die Serveranwendung müssen die **kostenlose Midl-Funktion für \_ Benutzer \_** implementieren, es sei denn, Sie kompilieren im OSF-Kompatibilitätsmodus ([**/osf**](/windows/desktop/Midl/-osf)). Die **\_ funktion \_ "midl user free"** muss in der Lage sein, den gesamten Speicher frei zu geben, der vom [**midl-Benutzer \_ \_ belegt**](the-midl-user-allocate-function.md)wird.

Anwendungen und Stubs rufen **midl \_ user \_ free** auf, wenn es um zugeordnete Objekte geht:

-   Die Serveranwendung sollte **midl \_ user \_ free** aufrufen, um von der Anwendung belegten Arbeitsspeicher freizugeben, z. B. beim Löschen eines dynamisch zugeordneten Datenknotens.
-   Der Serverstub ruft **midl \_ user \_ free** auf, um Arbeitsspeicher auf dem Server freizugeben, nachdem alle \[ \] out-Argumente, \[ in , \] \[ \] out-Argumente und der Funktionsrückgabewert gemarshallt wurden.

Beispielsweise implementiert das RPC-Windows-Beispielprogramm, das "Hello, world" anzeigt, **midl \_ user \_ free** im Hinblick auf die kostenlose C-Funktion:


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> Wenn das RpcSs-Paket aktiviert ist (z. B. aufgrund der Verwendung des \[ [**Attributs enable \_ allocate),**](/windows/desktop/Midl/enable-allocate) \] sollte Ihr Serverprogramm [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) verwenden, um Arbeitsspeicher freizugeben. Weitere Informationen finden Sie unter [RpcSs-Speicherverwaltungspaket.](rpcss-memory-management-package.md)

 

 

 