---
title: Deklarieren von asynchronen Funktionen
description: Um eine RPC-Funktion als asynchron zu deklarieren, deklarieren Sie zuerst die Funktion als Teil einer Schnittstellen Definition in einer IDL-Datei (Interface Definition Language).
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- Remote Prozedur Aufruf RPC, Tasks, deklarieren von asynchronen Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fafc1208d53763835d72f527723d00816f38db9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103949189"
---
# <a name="declaring-asynchronous-functions"></a>Deklarieren von asynchronen Funktionen

Um eine RPC-Funktion als asynchron zu deklarieren, deklarieren Sie zuerst die Funktion als Teil einer Schnittstellen Definition in einer IDL-Datei (Interface Definition Language). Die Verwendung von asynchronen RPC-Funktionen erfordert keine besonderen Änderungen an ihrer IDL-Datei. Das folgende Beispiel zeigt eine IDL-Datei für eine Anwendung, die eine asynchrone Funktion verwendet.

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

Für alle asynchronen RPC-Funktionen, die von der Anwendung verwendet werden, müssen Sie die Deklaration der asynchronen Funktionen in der ACF-Datei der Anwendung ändern. Wenden Sie das [**\[ Async \]**](../midl/async.md) -Attribut auf die einzelnen asynchronen Funktionsnamen an, wie im folgenden Beispiel gezeigt:

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

Wenn Sie das **\[ Async \]** -Attribut in der ACF-Datei anwenden, generiert der mittlerer l-Compiler automatisch einen zusätzlichen asynchronen handle-Parameter im Stubcode.

 

 