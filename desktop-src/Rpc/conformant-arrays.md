---
title: Konforme Arrays
description: Die Größe eines konformen Arrays kann je nachdem, wann der Client es an eine Remote Prozedur auf dem Server übergibt.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f1491354f9cd26ef6100ab8d21f2ace3133f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039441"
---
# <a name="conformant-arrays"></a><span data-ttu-id="5831f-103">Konforme Arrays</span><span class="sxs-lookup"><span data-stu-id="5831f-103">Conformant Arrays</span></span>

<span data-ttu-id="5831f-104">Die Größe eines konformen Arrays kann je nachdem, wann der Client es an eine Remote Prozedur auf dem Server übergibt.</span><span class="sxs-lookup"><span data-stu-id="5831f-104">The size of a conformant array can vary or conform each time the client passes it to a remote procedure on the server.</span></span> <span data-ttu-id="5831f-105">Die Schnittstellen Definition in der mittleren l-Datei der Anwendung ermöglicht es dem Client, die Größe des Arrays jedes Mal anzugeben, wenn die Remote Prozedur aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5831f-105">The interface definition in the application's MIDL file enables the client to specify the size of the array each time it invokes the remote procedure.</span></span> <span data-ttu-id="5831f-106">Verwenden \[ \] Sie in der Array Definition leere eckige Klammern () oder ein Sternchen in den eckigen Klammern ( \[ \* \] ), um ein konformes Array anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5831f-106">Use empty square brackets (\[ \]) or an asterisk in the square brackets (\[\*\]) in the array definition to indicate a conformant array.</span></span>

<span data-ttu-id="5831f-107">Das folgende Beispiel enthält die Definition einer Remote Prozedur in einer Schnittstelle in einer Mittel l-Datei.</span><span class="sxs-lookup"><span data-stu-id="5831f-107">The following sample contains the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="5831f-108">Der Client gibt die Größe des Arrays an, das durch den Parameter *arraySize* an den Server übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5831f-108">The client specifies the size of the array that it passes to the server by the parameter *arraySize*.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    MyRemoteProc(
         long lArraySize,
         [size_is(lArraySize)] char achArray[*]
    );

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="5831f-109">Die Schnittstellen Definition verwendet die mittlere Attribut \[ [**Größe \_**](/windows/desktop/Midl/size-is) \] , um die Größe des Arrays anzugeben, das der Client an den Server übergibt.</span><span class="sxs-lookup"><span data-stu-id="5831f-109">The interface definition uses the MIDL attribute \[[**size\_is**](/windows/desktop/Midl/size-is)\] to specify the size of the array that the client passes to the server.</span></span> <span data-ttu-id="5831f-110">Wenn Sie den maximalen Wert für die Indexnummern des Arrays angeben möchten, verwenden Sie stattdessen das \[ [**Maximum \_ is**](/windows/desktop/Midl/max-is) - \] Attribut.</span><span class="sxs-lookup"><span data-stu-id="5831f-110">If you would rather indicate the maximum value of the array's index numbers, use the \[[**max\_is**](/windows/desktop/Midl/max-is)\] attribute instead.</span></span> <span data-ttu-id="5831f-111">Weitere Informationen zu diesen Mittelwert Attributen finden Sie unter [Array Attribute](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="5831f-111">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="5831f-112">Das folgende Code Fragment veranschaulicht, wie ein Client möglicherweise die in der vorhergehenden-Datei definierte Remote Prozedur aufruft.</span><span class="sxs-lookup"><span data-stu-id="5831f-112">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


```C++
long lArrayLength = 20;
char achCharArray[20], achAnotherCharArray[200];

// Code to store 20 chars in achCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achCharArray);

lArrayLength = 200;

// Code to store 200 chars in achAnotherCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achAnotherCharArray);
```



<span data-ttu-id="5831f-113">Dieses Fragment Ruft die Remote Prozedur myremoteproc zweimal auf.</span><span class="sxs-lookup"><span data-stu-id="5831f-113">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="5831f-114">Beim ersten Aufruf übergibt Sie ein Array von 20 Elementen.</span><span class="sxs-lookup"><span data-stu-id="5831f-114">On the first invocation it passes an array of 20 elements.</span></span> <span data-ttu-id="5831f-115">Beim zweiten-Befehl übergibt der Client ein Array aus 200 Elementen.</span><span class="sxs-lookup"><span data-stu-id="5831f-115">On the second call, the client passes an array of 200 elements.</span></span>

 

 