---
title: Mehrdimensionale Arrays
description: Array Attribute können auch mit mehrdimensionalen Arrays verwendet werden.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948959"
---
# <a name="multidimensional-arrays"></a><span data-ttu-id="e6605-103">Mehrdimensionale Arrays</span><span class="sxs-lookup"><span data-stu-id="e6605-103">Multidimensional Arrays</span></span>

<span data-ttu-id="e6605-104">Array Attribute können auch mit mehrdimensionalen Arrays verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6605-104">Array attributes can also be used with multidimensional arrays.</span></span> <span data-ttu-id="e6605-105">Achten Sie jedoch darauf, sicherzustellen, dass jede Dimension des Arrays über ein entsprechendes-Attribut verfügt.</span><span class="sxs-lookup"><span data-stu-id="e6605-105">However, be careful to ensure that every dimension of the array has a corresponding attribute.</span></span> <span data-ttu-id="e6605-106">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e6605-106">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

<span data-ttu-id="e6605-107">Das vorangehende Array ist ein konformes Array (der Größe d1size) von 30 Element Arrays (mit d2len-Elementen, die für jedes Element ausgeliefert werden).</span><span class="sxs-lookup"><span data-stu-id="e6605-107">The preceding array is a conformant array (of size d1size ) of 30 element arrays (with d2len elements shipped for each).</span></span> <span data-ttu-id="e6605-108">Das Komma in den Klammern des \[ [**size \_ is**](/windows/desktop/Midl/size-is) - \] Attributs gibt an, dass der Wert in d1size auf die erste Dimension des Arrays angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6605-108">The comma in the parentheses of the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute specifies that value in d1size is applied to the first dimension of the array.</span></span> <span data-ttu-id="e6605-109">Entsprechend gibt der-Befehl in den Klammern der \[ [**Länge \_**](/windows/desktop/Midl/length-is) \] Attribute an, dass der Wert in d2len auf die zweite Dimension des Arrays angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6605-109">Likewise, the command in the parentheses of the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute indicates that the value in d2len is applied to the second dimension of the array.</span></span>

<span data-ttu-id="e6605-110">Der Compiler für die Mittel l 2,0 stellt zwei Methoden zum Mars Hallen von Parametern bereit: gemischter Modus (/**OS**) und vollständig interpretiert (/**OIF** oder/**Oicf**).</span><span class="sxs-lookup"><span data-stu-id="e6605-110">The MIDL 2.0 compiler provides two methods for marshaling parameters: mixed-mode (/**Os**) and fully-interpreted (/**Oif** or /**Oicf**).</span></span> <span data-ttu-id="e6605-111">Standardmäßig kompiliert der Mittell-Compiler Schnittstellen im gemischten Modus.</span><span class="sxs-lookup"><span data-stu-id="e6605-111">By default, the MIDL compiler compiles interfaces in mixed mode.</span></span> <span data-ttu-id="e6605-112">Sie müssen nicht explizit den [**/OS**](/windows/desktop/Midl/-os) -Schalter angeben, um das Marshalling im gemischten Modus zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e6605-112">You do not need to explicitly specify the [**/Os**](/windows/desktop/Midl/-os) switch to get mixed-mode marshaling.</span></span>

<span data-ttu-id="e6605-113">Die vollständig interpretierte Methode Marshalls Daten vollständig offline.</span><span class="sxs-lookup"><span data-stu-id="e6605-113">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="e6605-114">Dadurch wird die Größe des stubcodes beträchtlich reduziert, dies führt jedoch auch zu einer geringeren Leistung.</span><span class="sxs-lookup"><span data-stu-id="e6605-114">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span> <span data-ttu-id="e6605-115">Beim Marshalling im gemischten Modus marshallt die stubweise einige Parameter online.</span><span class="sxs-lookup"><span data-stu-id="e6605-115">In mixed-mode marshaling, the stubs marshals some parameters online.</span></span> <span data-ttu-id="e6605-116">Dies führt zwar zu einer größeren stubgröße, bietet aber auch eine höhere Leistung.</span><span class="sxs-lookup"><span data-stu-id="e6605-116">While this results in a larger stub size, it also offers increased performance.</span></span>

> [!Caution]  
> <span data-ttu-id="e6605-117">Bei der Kompilierung von IDL-Dateien in diesem Modus ist Vorsicht geboten.</span><span class="sxs-lookup"><span data-stu-id="e6605-117">Exercise caution when compiling IDL files in this mode.</span></span> <span data-ttu-id="e6605-118">Die Verwendung von mehrdimensionalen Arrays im gemischten Modus kann zu Parametern führen, die nicht ordnungsgemäß gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="e6605-118">Using multidimensional arrays in mixed mode can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="e6605-119">Der [**/Oicf**](/windows/desktop/Midl/-oi) -Befehls Zeilenschalter wird empfohlen, wenn Ihre Schnittstelle Parameter definiert, die mehrdimensionale Arrays sind.</span><span class="sxs-lookup"><span data-stu-id="e6605-119">The [**/Oicf**](/windows/desktop/Midl/-oi) command line switch is recommended when your interface defines parameters that are multidimensional arrays.</span></span>

 

<span data-ttu-id="e6605-120">Das \[ [**String**](/windows/desktop/Midl/string) - \] Attribut kann auch mit mehrdimensionalen Arrays verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6605-120">The \[[**string**](/windows/desktop/Midl/string)\] attribute can also be used with multidimensional arrays.</span></span> <span data-ttu-id="e6605-121">Das-Attribut gilt für die am wenigsten bedeutende Dimension, z. b. ein konformes Array von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="e6605-121">The attribute applies to the least significant dimension, such as a conformant array of strings.</span></span> <span data-ttu-id="e6605-122">Sie können auch mehrdimensionale Zeiger Attribute verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6605-122">You can also use multidimensional pointer attributes.</span></span> <span data-ttu-id="e6605-123">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e6605-123">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

<span data-ttu-id="e6605-124">Im vorherigen Beispiel ist die Variable ptr2d ein Zeiger auf einen d1len-Zeiger, der jeweils auf d2len-Zeiger auf **Long** zeigt.</span><span class="sxs-lookup"><span data-stu-id="e6605-124">In the preceding example, the variable ptr2d is a pointer to a d1len-sized block of pointers, each of which points to d2len pointers to **long**.</span></span>

<span data-ttu-id="e6605-125">Mehrdimensionale Arrays entsprechen nicht den Arrays von Zeigern.</span><span class="sxs-lookup"><span data-stu-id="e6605-125">Multidimensional arrays are not equivalent to arrays of pointers.</span></span> <span data-ttu-id="e6605-126">Bei einem mehrdimensionalen Array handelt es sich um einen einzelnen großen Block von Daten im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e6605-126">A multidimensional array is a single, large block of data in memory.</span></span> <span data-ttu-id="e6605-127">Ein Array von Zeigern enthält nur einen Zeiger Block im Array.</span><span class="sxs-lookup"><span data-stu-id="e6605-127">An array of pointers only contains a block of pointers in the array.</span></span> <span data-ttu-id="e6605-128">Die Daten, auf die die Zeiger zeigen, können sich an einer beliebigen Stelle im Speicher befinden.</span><span class="sxs-lookup"><span data-stu-id="e6605-128">The data that the pointers point to can be anywhere in memory.</span></span> <span data-ttu-id="e6605-129">Außerdem ermöglicht die ANSI C-Syntax, dass nur die signifikanteste (äußteste) Array Dimension in einem mehrdimensionalen Array nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e6605-129">Also, ANSI C syntax allows only the most significant (leftmost) array dimension to be unspecified in a multidimensional array.</span></span> <span data-ttu-id="e6605-130">Daher ist Folgendes eine gültige-Anweisung:</span><span class="sxs-lookup"><span data-stu-id="e6605-130">Therefore, the following is a valid statement:</span></span>

`long a1[] [20]`

<span data-ttu-id="e6605-131">Vergleichen Sie dies mit der folgenden ungültigen Anweisung:</span><span class="sxs-lookup"><span data-stu-id="e6605-131">Compare this to the following invalid statement:</span></span>

`long a1[20] []`

 

 