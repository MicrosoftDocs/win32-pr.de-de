---
title: Deklarieren asynchroner Funktionen
description: Um eine RPC-Funktion als asynchron zu deklarieren, deklarieren Sie zuerst die Funktion als Teil einer Schnittstellendefinition in einer IDL-Datei (Interface Definition Language).
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- Remoteprozeduraufruf RPC , Tasks, Deklarieren asynchroner Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc0978156fe91291b91937082690258550b7f02f1d7b6e5334dd0741a9f0211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931048"
---
# <a name="declaring-asynchronous-functions"></a>Deklarieren asynchroner Funktionen

Um eine RPC-Funktion als asynchron zu deklarieren, deklarieren Sie zuerst die Funktion als Teil einer Schnittstellendefinition in einer IDL-Datei (Interface Definition Language). Die Verwendung asynchroner RPC-Funktionen erfordert keine besonderen Änderungen an Ihrer IDL-Datei. Das folgende Beispiel zeigt eine IDL-Datei für eine Anwendung, die eine asynchrone Funktion verwendet.

``` syntax
[ 
    uuid (7f6c4340-eb67-11d1-b9d7-00c04fad9a3b),
    version(1.0),
    pointer_default(unique)
]
interface AsyncRPC
{
    const long DEFAULT_ASYNC_DELAY        = 10000;
    const short APP_ERROR                 = -1;
    const char* DEFAULT_PROTOCOL_SEQUENCE = "ncacn_ip_tcp";
    const char* DEFAULT_ENDPOINT          = "8765";
 
    void NonAsyncFunc(handle_t hBinding,
                      [in, string] unsigned char * pszMessage);
 
    void AsyncFunc(handle_t hBinding,
                   [in] unsigned long nAsychDelay);
 
    void Shutdown(handle_t hBinding);
}
```

Für alle asynchronen RPC-Funktionen, die ihre Anwendung verwendet, müssen Sie die Deklaration der asynchronen Funktionen in der ACF-Datei Ihrer Anwendung ändern. Wenden Sie das [**\[ asynchrone \]**](../midl/async.md) Attribut auf jeden asynchronen Funktionsnamen an, wie im folgenden Beispiel gezeigt:

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

Wenn Sie das **\[ asynchrone \]** Attribut in der ACF-Datei anwenden, generiert der MIDL-Compiler automatisch einen zusätzlichen asynchronen Handleparameter im Stubcode.

 

 