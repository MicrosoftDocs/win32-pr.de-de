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
# <a name="using-serialization-services"></a><span data-ttu-id="90114-104">Verwenden von Serialisierungsdiensten</span><span class="sxs-lookup"><span data-stu-id="90114-104">Using Serialization Services</span></span>

<span data-ttu-id="90114-105">"Mittel l" generiert einen serialisierungsstub für die Prozedur mit den Attributen \[ [**Codieren**](/windows/desktop/Midl/encode) \] und \[ [**decodieren**](/windows/desktop/Midl/decode) \] .</span><span class="sxs-lookup"><span data-stu-id="90114-105">MIDL generates a serialization stub for the procedure with the attributes \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\].</span></span> <span data-ttu-id="90114-106">Wenn Sie diese Routine aufrufen, führen Sie einen serialisierungsbefehl anstelle eines Remote Aufrufes aus.</span><span class="sxs-lookup"><span data-stu-id="90114-106">When you call this routine, you execute a serialization call instead of a remote call.</span></span> <span data-ttu-id="90114-107">Die Prozedur Argumente werden auf die übliche Weise an einen Puffer gemarshallt bzw. aus diesem entfernt.</span><span class="sxs-lookup"><span data-stu-id="90114-107">The procedure arguments are marshaled to or unmarshaled from a buffer in the usual way.</span></span> <span data-ttu-id="90114-108">Sie haben dann die komplette Kontrolle über die Puffer.</span><span class="sxs-lookup"><span data-stu-id="90114-108">You then have complete control of the buffers.</span></span>

<span data-ttu-id="90114-109">Wenn das Programm hingegen die Typserialisierung ausführt (ein Typ wird mit Serialisierungsattributen bezeichnet), generiert die Mittel l Routinen zum Anpassen, codieren und Decodieren von Objekten dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="90114-109">In contrast, when your program performs type serialization (a type is labeled with serialization attributes), MIDL generates routines to size, encode, and decode objects of that type.</span></span> <span data-ttu-id="90114-110">Zum Serialisieren von Daten müssen Sie diese Routinen in geeigneter Weise aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="90114-110">To serialize data, you must call these routines in the appropriate way.</span></span> <span data-ttu-id="90114-111">Die Typserialisierung ist eine Microsoft-Erweiterung und nicht verfügbar, wenn Sie im DCE-Kompatibilitätsmodus ([**/OSF**](/windows/desktop/Midl/-osf)) kompilieren.</span><span class="sxs-lookup"><span data-stu-id="90114-111">Type serialization is a Microsoft extension and, as such, is not available when you compile in DCE-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="90114-112">Durch die Verwendung der \[ Attribute [**Codieren**](/windows/desktop/Midl/encode) \] und \[ [**decodieren**](/windows/desktop/Midl/decode) \] als Schnittstellen Attribute wendet RPC die Codierung auf alle Typen und Routinen an, die in der IDL-Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="90114-112">By using the \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\] attributes as interface attributes, RPC applies encoding to all the types and routines defined in the IDL file.</span></span>

<span data-ttu-id="90114-113">Sie müssen bei der Verwendung von Serialisierungsdiensten ausreichend ausgerichtete Puffer angeben.</span><span class="sxs-lookup"><span data-stu-id="90114-113">You must supply adequately aligned buffers when using serialization services.</span></span> <span data-ttu-id="90114-114">Der Anfang des Puffers muss an einer Adresse ausgerichtet werden, die ein Vielfaches von 8 oder eine Ausrichtung mit 8 Bytes ist.</span><span class="sxs-lookup"><span data-stu-id="90114-114">The beginning of the buffer must be aligned at an address that is a multiple of 8, or 8-byte aligned.</span></span> <span data-ttu-id="90114-115">Bei der prozedurerialisierung von Prozeduren muss jeder Prozedur Aufrufvorgang von einer Puffer Position, die 8-Byte-ausgerichtet ist, in eine marshallt</span><span class="sxs-lookup"><span data-stu-id="90114-115">For procedure serialization, each procedure call must marshal into or unmarshal from a buffer position that is 8-byte aligned.</span></span> <span data-ttu-id="90114-116">Bei der Serialisierung des Typs müssen Größe, Codierung und Decodierung an einer Position beginnen, die mit 8 Bytes ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="90114-116">For type serialization, sizing, encoding, and decoding must start at a position that is 8-byte aligned.</span></span>

<span data-ttu-id="90114-117">Eine Möglichkeit für Ihre Anwendung, sicherzustellen, dass Ihre Puffer ausgerichtet sind, besteht darin, die Funktion " [**Mittell- \_ Benutzer \_ zuweisen**](/windows/desktop/Midl/midl-user-allocate-1) " so zu schreiben, dass Sie ausgerichtete Puffer erstellt.</span><span class="sxs-lookup"><span data-stu-id="90114-117">One way for your application to ensure that its buffers are aligned is to write the [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) function such that it creates aligned buffers.</span></span> <span data-ttu-id="90114-118">Im folgenden Codebeispiel wird veranschaulicht, wie dies durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="90114-118">The following code sample demonstrates how this can be done.</span></span>


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



<span data-ttu-id="90114-119">Im folgenden Beispiel wird die entsprechende [**\_ Benutzer \_ freie Funktion "Mittel l**](/windows/desktop/Midl/midl-user-free-1) " gezeigt.</span><span class="sxs-lookup"><span data-stu-id="90114-119">The following example shows the corresponding [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) function.</span></span>


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



 

 