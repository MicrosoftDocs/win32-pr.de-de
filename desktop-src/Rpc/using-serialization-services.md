---
title: Verwenden von Serialisierungsdiensten
description: MIDL generiert einen Serialisierungsstub für die Prozedur mit den Attributen \encode\ und \ decode\ .
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- REMOTE PROCEDURE Call RPC , Tasks, using serialization services (Rpc-Aufruf von Remoteprozeduren, Tasks mitHilfe von Serialisierungsdiensten)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be20d513bdb74eca316b022dd8536e8988e32e93099981cc77830035048e55e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010628"
---
# <a name="using-serialization-services"></a>Verwenden von Serialisierungsdiensten

MIDL generiert einen Serialisierungsstub für die Prozedur, bei dem die Attribute \[ [**codiert**](/windows/desktop/Midl/encode) \] und \[ [**decodiert werden.**](/windows/desktop/Midl/decode) \] Wenn Sie diese Routine aufrufen, führen Sie einen Serialisierungsaufruf anstelle eines Remoteaufrufs aus. Die Prozedurargumente werden auf die übliche Weise an einen Puffer gemarshallt oder aus einem Puffer nicht gemarshallt. Anschließend haben Sie die vollständige Kontrolle über die Puffer.

Wenn das Programm dagegen die Typserialisierung ausführt (ein Typ ist mit Serialisierungsattributen bezeichnet), generiert MIDL Routinen zur Größe, Codierung und Decodierung von Objekten dieses Typs. Um Daten zu serialisieren, müssen Sie diese Routinen auf die entsprechende Weise aufrufen. Die Typserialisierung ist eine Microsoft-Erweiterung und daher nicht verfügbar, wenn Sie im DCE-Kompatibilitätsmodus [**(/osf)**](/windows/desktop/Midl/-osf)kompilieren. Indem die \[ [**Codierungs-**](/windows/desktop/Midl/encode) und Decodierungsattribute als Schnittstellenattribute verwendet werden, wendet RPC die Codierung auf alle Typen und Routinen an, die \] in der \[ [](/windows/desktop/Midl/decode) \] IDL-Datei definiert sind.

Sie müssen angemessen ausgerichtete Puffer bei der Verwendung von Serialisierungsdiensten zur Verfügung stellen. Der Anfang des Puffers muss an einer Adresse ausgerichtet werden, die ein Vielfaches von 8 oder 8 Byte ist. Für die Prozedurserialisierung muss jeder Prozeduraufruf an einer 8-Byte-ausgerichteten Pufferposition marshallen oder das Marshallen von einer Pufferposition aus unmarshalieren. Für die Typserialisierung müssen Größe, Codierung und Decodierung an einer 8-Byte-ausgerichteten Position beginnen.

Eine Möglichkeit für Ihre Anwendung, sicherzustellen, dass ihre Puffer ausgerichtet sind, besteht im Schreiben der Midl-Benutzer-Zuordnungsfunktion, damit sie ausgerichtete Puffer erstellt. [**\_ \_**](/windows/desktop/Midl/midl-user-allocate-1) Im folgenden Codebeispiel wird veranschaulicht, wie dies möglich ist.


```C++
#include <windows.h>

#define ALIGN_TO8(p)   (char *)((unsigned long)((char *)p + 7) & ~7)

void __RPC_FAR *__RPC_USER  MIDL_user_allocate(size_t sizeInBytes)
{
    unsigned char *pcAllocated;
    unsigned char *pcUserPtr;

    pcAllocated = (unsigned char *) malloc( sizeInBytes + 15 );
    pcUserPtr =  ALIGN_TO8( pcAllocated );
    if ( pcUserPtr == pcAllocated )
        pcUserPtr = pcAllocated + 8;

    *(pcUserPtr - 1) = pcUserPtr - pcAllocated;

    return( pcUserPtr );
}
```



Das folgende Beispiel zeigt die entsprechende [**funktion midl \_ user \_ free.**](/windows/desktop/Midl/midl-user-free-1)


```C++
void __RPC_USER  MIDL_user_free(void __RPC_FAR *f)
{
    unsigned char * pcAllocated;
    unsigned char * pcUserPtr;

    pcUserPtr = (unsigned char *) f;
    pcAllocated = pcUserPtr - *(pcUserPtr - 1);

    free( pcAllocated );
}
```



 

 