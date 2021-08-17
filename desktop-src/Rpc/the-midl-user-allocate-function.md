---
title: Die midl_user_allocate-Funktion
description: Die \_ Midl-Benutzer-Zuordnungsfunktion ist eine Prozedur, die \_ von Entwicklern von RPC-Anwendungen bereitgestellt werden muss.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8e064fc16a303660be96a4a3c47aa361c4616f54a8cb825c1fce5334543fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924249"
---
# <a name="the-midl_user_allocate-function"></a>Die \_ \_ midl-Benutzer-Zuordnungsfunktion

Die **\_ Midl-Benutzer-Zuordnungsfunktion \_** ist eine Prozedur, die von Entwicklern von RPC-Anwendungen bereitgestellt werden muss. Er weist Arbeitsspeicher für die RPC-Stubs und Bibliotheksroutinen zu. Ihre **\_ Midl-Benutzer-Zuordnungsfunktion \_** muss mit dem folgenden Prototyp übereinstimmen:

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

Der *cBytes-Parameter* gibt die Anzahl der zu reservierenden Bytes an. Sowohl Clientanwendungen als auch Serveranwendungen müssen die Midl-Benutzer-Zuordnungsfunktion implementieren, es sei denn, Sie kompilieren im OSF-Kompatibilitätsmodus (/osf). **\_ \_** Anwendungen und generierte Stubs rufen **midl \_ user allocate \_ direkt** oder indirekt auf, um zugeordnete Objekte zu verwalten. Beispiel:

-   Die Client- und Serveranwendungen rufen **midl \_ user \_ allocate** auf, um Arbeitsspeicher für die Anwendung zu reservieren, z. B. beim Erstellen eines neuen Knotens in einer Struktur oder verknüpften Liste.
-   Der Serverstub ruft **midl \_ user allocate \_ auf,** wenn die Zuordnung von Daten im Serveradressenbereich entmardt wird.
-   Der Clientstub ruft **midl \_ user allocate \_ auf,** wenn daten vom Server, auf den von einem Out-Zeiger verwiesen wird, nicht imShaling \[ gespeichert \] werden. Beachten Sie, dass der Clientstub für in , out und eindeutige Zeiger nur dann midl user allocate aufruft, wenn der eindeutige Zeigerwert bei der Eingabe NULL war und sich während des Aufrufs in einen Wert ändert, der nicht \[ \] NULL \[ \] \[ \] **\_ \_** \[ \] ist. Wenn der eindeutige Zeiger bei der Eingabe nicht NULL war, schreibt der \[ \] Clientstub die zugeordneten Daten in den vorhandenen Arbeitsspeicher.

Wenn **bei der \_ Midl-Benutzerbeteilung \_** kein Arbeitsspeicher reserviert werden kann, sollte ein NULL-Zeiger zurückgegeben werden.

Die **\_ midl-Benutzerfunktion \_ allocate** sollte einen 8-Byte-ausgerichteten Zeiger zurückgeben.

Beispielsweise implementieren die mit dem Platform Software Development Kit (SDK) bereitgestellten Beispielprogramme **midl \_ user \_ allocate** in Bezug auf die C-Funktion [**malloc:**](pointers-and-memory-allocation.md)


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> Wenn das RpcSs-Paket aktiviert ist (z. B. als Ergebnis der Verwendung des Attributs \[ [**enable \_ allocate),**](/windows/desktop/Midl/enable-allocate) verwenden Sie \] [**RpcSmAllocate,**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) um Arbeitsspeicher auf der Serverseite zu reservieren. Weitere Informationen zum Aktivieren der \[ **Zuordnung finden \_ Sie** \] in der [MIDL-Referenz.](/windows/desktop/Midl/midl-language-reference)

 

 

 