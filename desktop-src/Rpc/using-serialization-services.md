---
title: Verwenden von Serialisierungsdiensten
description: "\"Mittel l\" generiert einen serialisierungsstub für die Prozedur mit den Attributen \\ \"Codieren \\\" und \"\\ Decode \\\"."
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- Remote Prozedur Aufruf RPC, Tasks, mithilfe von Serialisierungsdiensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317156a2da954e001b687cca12eb0c6df23ef4ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039562"
---
# <a name="using-serialization-services"></a>Verwenden von Serialisierungsdiensten

"Mittel l" generiert einen serialisierungsstub für die Prozedur mit den Attributen \[ [**Codieren**](/windows/desktop/Midl/encode) \] und \[ [**decodieren**](/windows/desktop/Midl/decode) \] . Wenn Sie diese Routine aufrufen, führen Sie einen serialisierungsbefehl anstelle eines Remote Aufrufes aus. Die Prozedur Argumente werden auf die übliche Weise an einen Puffer gemarshallt bzw. aus diesem entfernt. Sie haben dann die komplette Kontrolle über die Puffer.

Wenn das Programm hingegen die Typserialisierung ausführt (ein Typ wird mit Serialisierungsattributen bezeichnet), generiert die Mittel l Routinen zum Anpassen, codieren und Decodieren von Objekten dieses Typs. Zum Serialisieren von Daten müssen Sie diese Routinen in geeigneter Weise aufzurufen. Die Typserialisierung ist eine Microsoft-Erweiterung und nicht verfügbar, wenn Sie im DCE-Kompatibilitätsmodus ([**/OSF**](/windows/desktop/Midl/-osf)) kompilieren. Durch die Verwendung der \[ Attribute [**Codieren**](/windows/desktop/Midl/encode) \] und \[ [**decodieren**](/windows/desktop/Midl/decode) \] als Schnittstellen Attribute wendet RPC die Codierung auf alle Typen und Routinen an, die in der IDL-Datei definiert sind.

Sie müssen bei der Verwendung von Serialisierungsdiensten ausreichend ausgerichtete Puffer angeben. Der Anfang des Puffers muss an einer Adresse ausgerichtet werden, die ein Vielfaches von 8 oder eine Ausrichtung mit 8 Bytes ist. Bei der prozedurerialisierung von Prozeduren muss jeder Prozedur Aufrufvorgang von einer Puffer Position, die 8-Byte-ausgerichtet ist, in eine marshallt Bei der Serialisierung des Typs müssen Größe, Codierung und Decodierung an einer Position beginnen, die mit 8 Bytes ausgerichtet ist.

Eine Möglichkeit für Ihre Anwendung, sicherzustellen, dass Ihre Puffer ausgerichtet sind, besteht darin, die Funktion " [**Mittell- \_ Benutzer \_ zuweisen**](/windows/desktop/Midl/midl-user-allocate-1) " so zu schreiben, dass Sie ausgerichtete Puffer erstellt. Im folgenden Codebeispiel wird veranschaulicht, wie dies durchgeführt werden kann.


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



Im folgenden Beispiel wird die entsprechende [**\_ Benutzer \_ freie Funktion "Mittel l**](/windows/desktop/Midl/midl-user-free-1) " gezeigt.


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



 

 