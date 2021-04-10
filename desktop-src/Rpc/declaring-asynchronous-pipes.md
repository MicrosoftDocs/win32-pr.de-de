---
title: Deklarieren von asynchronen Pipes
description: Die folgende Beispiel-IDL-Datei definiert eine typische Pipe-Struktur und eine asynchrone RPC-Funktion mit Pipes.
ms.assetid: ddd20212-18f5-41f6-9f6e-0edbe5e517a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f8fb11d89d92bcee5b2b8b052a381077aeb82c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309607"
---
# <a name="declaring-asynchronous-pipes"></a><span data-ttu-id="5cbba-103">Deklarieren von asynchronen Pipes</span><span class="sxs-lookup"><span data-stu-id="5cbba-103">Declaring Asynchronous Pipes</span></span>

<span data-ttu-id="5cbba-104">Die folgende Beispiel-IDL-Datei definiert eine typische Pipe-Struktur und eine asynchrone RPC-Funktion mit Pipes.</span><span class="sxs-lookup"><span data-stu-id="5cbba-104">The following example IDL file defines a typical pipe structure, and an asynchronous RPC function with pipes.</span></span>

## <a name="example"></a><span data-ttu-id="5cbba-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5cbba-105">Example</span></span>

``` syntax
//file: Xasyncpipe.idl:
//
interface IMyAsyncPipe 
{
    //define the pipe type
    typedef pipe int aysnc_intpipe ;
 
    //then use it as a parameter
    int MyAsyncPipe(
        handle_t hBinding, 
        [in] a,
        [in] ASYNC_INTPIPE *inpipe, 
        [out] ASYNC_INTPIPE *outpipe, 
        [out] int *b) ;
};
//other function declarations
 
//other interface definitions
//end Xasyncpipe.idl
 
//file:Xasyncpipe.acf:
//file: Xasyncpipe.acf:
interface IMyAsyncPipe
{
    [async] MyAsyncPipe () ;
} ;
//
//end Xasyncpipe.acf
```

<span data-ttu-id="5cbba-106">Das folgende Code Fragment zeigt eine typische Pipe-Struktur Definition.</span><span class="sxs-lookup"><span data-stu-id="5cbba-106">The following code fragment shows a typical pipe structure definition.</span></span> <span data-ttu-id="5cbba-107">Sie enthält Zeiger auf Push-und Pull-Prozeduren, einen Puffer zum Speichern der pipedaten und eine Zustands Variable zum Koordinieren der Prozeduren:</span><span class="sxs-lookup"><span data-stu-id="5cbba-107">It contains pointers to push and pull procedures, a buffer to hold the pipe data, and a state variable to coordinate the procedures:</span></span>

``` syntax
//
typedef struct ASYNC_MYPIPE
{
    RPC_STATUS (__RPC_FAR * pull) (
        char __RPC_FAR * state,
        small __RPC_FAR * buf,
        unsigned long esize,
        unsigned long __RPC_FAR * ecount );
    RPC_STATUS (__RPC_FAR * push) (
        char __RPC_FAR * state,
        small __RPC_FAR * buf,
        unsigned long ecount );
    void *Reserved;
    char __RPC_FAR * state;
}ASYNC_INTPIPE;
```

 

 




