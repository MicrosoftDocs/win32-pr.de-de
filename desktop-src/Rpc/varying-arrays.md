---
title: Variierende Arrays
description: In der mittleren l sind unterschiedliche Arrays in der Größe fester Größe. Sie ermöglichen es Clients, verschiedene Teile von Arrays von Clients an Server zu übergeben. Die Größe des Array Teils kann vom Aufruf zum Aufruf abweichen. Allerdings ist die Größe des gesamten Arrays korrigiert.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b2d79ee37f3e366bbf232b362306f78ca6ada4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473877"
---
# <a name="varying-arrays"></a><span data-ttu-id="11487-106">Variierende Arrays</span><span class="sxs-lookup"><span data-stu-id="11487-106">Varying Arrays</span></span>

<span data-ttu-id="11487-107">In der mittleren l sind unterschiedliche Arrays in der Größe fester Größe.</span><span class="sxs-lookup"><span data-stu-id="11487-107">In MIDL, varying arrays are fixed in size.</span></span> <span data-ttu-id="11487-108">Sie ermöglichen es Clients, verschiedene Teile von Arrays von Clients an Server zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="11487-108">They allow clients to pass different portions of arrays from clients to servers.</span></span> <span data-ttu-id="11487-109">Die Größe des Array Teils kann vom Aufruf zum Aufruf abweichen.</span><span class="sxs-lookup"><span data-stu-id="11487-109">The size of the array portion can vary from invocation to invocation.</span></span> <span data-ttu-id="11487-110">Allerdings ist die Größe des gesamten Arrays korrigiert.</span><span class="sxs-lookup"><span data-stu-id="11487-110">However, the size of the overall array is fixed.</span></span>

<span data-ttu-id="11487-111">Das folgende Beispiel zeigt beispielsweise die Definition einer Remote Prozedur in einer Schnittstelle in einer Mittel l-Datei.</span><span class="sxs-lookup"><span data-stu-id="11487-111">For instance, the following example shows the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="11487-112">Die Größe des Arrays, das der Client an den Server übergibt, wird durch die Konstante Array \_ Größe festgesetzt.</span><span class="sxs-lookup"><span data-stu-id="11487-112">The size of the array that the client passes to the server is fixed by the constant ARRAY\_SIZE.</span></span> <span data-ttu-id="11487-113">Die-Schnittstelle gibt den Teil des Arrays an, den der Client in den Parametern firstelement und ChunkSize an den Server übergibt.</span><span class="sxs-lookup"><span data-stu-id="11487-113">The interface specifies the portion of the array that the client passes to the server in the parameters firstElement and chunkSize.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(
        [in] long lFirstElement,
        [in] long lChunkSize,
        [in, first_is(lFirstElement), 
          length_is(lChunkSize)] char achArray[ARRAY_SIZE]
    );

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="11487-114">Die Schnittstellen Definition verwendet zuerst das Attribut "Mittel" \[ [**\_**](/windows/desktop/Midl/first-is) \] , um die Indexnummer des ersten Elements in dem Array anzugeben, das der Client an den Server übergibt.</span><span class="sxs-lookup"><span data-stu-id="11487-114">The interface definition uses the MIDL attribute \[[**first\_is**](/windows/desktop/Midl/first-is)\] to specify the index number of the first element in the portion of the array that the client passes to the server.</span></span> <span data-ttu-id="11487-115">Das \[ [**length \_ is**](/windows/desktop/Midl/length-is) - \] Attribut gibt die Gesamtanzahl der Array Elemente an, die der Client übergibt.</span><span class="sxs-lookup"><span data-stu-id="11487-115">The \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute specifies the total number of array elements that the client passes.</span></span> <span data-ttu-id="11487-116">Weitere Informationen zu diesen Mittelwert Attributen finden Sie unter [Array Attribute](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="11487-116">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="11487-117">Das folgende Code Fragment veranschaulicht, wie ein Client möglicherweise die in der vorhergehenden-Datei definierte Remote Prozedur aufruft.</span><span class="sxs-lookup"><span data-stu-id="11487-117">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


```C++
long lFirstArrayElementNumber = 20;
long lTotalElementsPassed = 100;
char achCharArray[ARRAY_SIZE];

// Code to store chars in the array goes here.

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);

firstArrayElementNumber = 120;
totalElementsPassed = 200;

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);
```



<span data-ttu-id="11487-118">Dieses Fragment Ruft die Remote Prozedur myremoteproc zweimal auf.</span><span class="sxs-lookup"><span data-stu-id="11487-118">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="11487-119">Beim ersten Aufruf übergibt Sie die Array Elemente mit der Nummerierung 20 bis 119, wie durch die Werte in den Variablen firstarrayelementnumber und totalelementsp; angegeben.</span><span class="sxs-lookup"><span data-stu-id="11487-119">On the first invocation it passes the array elements numbered 20 through 119, as indicated by the values in the variables firstArrayElementNumber and totalElementsPassed.</span></span> <span data-ttu-id="11487-120">Beim zweiten-Befehl übergibt der Client die Array Elemente mit der Nummerierung 120 bis 319.</span><span class="sxs-lookup"><span data-stu-id="11487-120">On the second call, the client passes the array elements numbered 120 through 319.</span></span>

 

 