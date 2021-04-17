---
title: Die midl_user_free-Funktion
description: Die mittlere \_ Benutzer \_ freie Funktion muss von RPC-Entwicklern bereitgestellt werden.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713ed05173b709780b6496f233051fa3adddff8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390927"
---
# <a name="the-midl_user_free-function"></a>Die mittlere \_ Benutzer \_ freie Funktion

Die **mittlere \_ Benutzer \_ freie** Funktion muss von RPC-Entwicklern bereitgestellt werden. Dadurch wird Arbeitsspeicher für die RPC-stubspeicher und Bibliotheks Routinen zugewiesen. Ihre **mittlere \_ Benutzer \_ freie** Funktion muss dem folgenden Prototyp entsprechen:

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

Der *pbuffer* -Parameter gibt einen Zeiger auf den Speicher an, der freigegeben werden soll. Sowohl die Client Anwendung als auch die Serveranwendung müssen die **\_ \_ Free** -Funktion von "Mittel l" implementieren, es sei denn, Sie Kompilieren im OSF-Kompatibilitätsmodus ([**/OSF**](/windows/desktop/Midl/-osf)). Die **mittlere \_ Benutzer \_ freie** Funktion muss in der Lage sein, den gesamten Speicher freizugeben, der von der [**\_ Benutzer \_ Zuordnung**](the-midl-user-allocate-function.md)für den Benutzer zugeordnet wird.

Anwendungen und stufstufs wenden beim Umgang mit zugeordneten Objekten einen **mittleren \_ Benutzer \_ frei** an:

-   Die Serveranwendung sollte den **\_ Benutzer freien Benutzer \_ kostenlos** anrufen, um von der Anwendung zugeordnete Arbeitsspeicher freizugeben, z. b. beim Löschen eines dynamisch zugeordneten Daten Knotens.
-   Der Serverstub Ruft den **\_ Benutzer \_ kostenlos** auf, um Arbeitsspeicher auf dem Server freizugeben, nachdem alle \[ Argumente, \] \[ in \] , \[ out \] -Argumente und der Funktionsrückgabewert gemarshallert wurden.

Beispielsweise implementiert das RPC Windows-Beispielprogramm, das "Hello, World" anzeigt, in Bezug auf die C-Funktion kostenlos den **mittleren \_ Benutzer \_ Free** :


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> Wenn das RPCSS-Paket aktiviert ist (z. b. als Ergebnis der Verwendung des \[ Attributs " [**\_ zuordnen**](/windows/desktop/Midl/enable-allocate) " \] ), sollte das Serverprogramm [**rpcsmfree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) verwenden, um Arbeitsspeicher freizugeben. Weitere Informationen finden Sie unter [RPCSS-Speicher Verwaltungspaket](rpcss-memory-management-package.md).

 

 

 