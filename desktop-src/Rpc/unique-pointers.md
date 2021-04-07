---
title: Eindeutige Zeiger
description: In C-Programmen können mehr als ein Zeiger die Daten Adresse enthalten.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf9a45965c82416ec838f8598c2796ba621a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039026"
---
# <a name="unique-pointers"></a><span data-ttu-id="c103e-103">Eindeutige Zeiger</span><span class="sxs-lookup"><span data-stu-id="c103e-103">Unique Pointers</span></span>

<span data-ttu-id="c103e-104">In C-Programmen können mehr als ein Zeiger die Daten Adresse enthalten.</span><span class="sxs-lookup"><span data-stu-id="c103e-104">In C programs, more than one pointer can contain the address of data.</span></span> <span data-ttu-id="c103e-105">Die Zeiger werden als [*Alias*](a-glos.md) für die Daten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c103e-105">The pointers are said to create an [*alias*](a-glos.md) for the data.</span></span> <span data-ttu-id="c103e-106">Aliase werden auch erstellt, wenn Zeiger auf deklarierte Variablen zeigen.</span><span class="sxs-lookup"><span data-stu-id="c103e-106">Aliases are also created when pointers point at declared variables.</span></span> <span data-ttu-id="c103e-107">Das folgende Code Fragment veranschaulicht beide Methoden der Aliasing:</span><span class="sxs-lookup"><span data-stu-id="c103e-107">The following code fragment illustrates both of these methods of aliasing:</span></span>


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



<span data-ttu-id="c103e-108">In einem typischen C-Programm können Sie mithilfe der folgenden Definition eine binäre Struktur angeben:</span><span class="sxs-lookup"><span data-stu-id="c103e-108">In a typical C program, you might specify a binary tree using the following definition:</span></span>


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



<span data-ttu-id="c103e-109">Mehr als ein Zeiger kann auf den Inhalt eines Struktur Knotens zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c103e-109">More than one pointer can access the contents of a tree node.</span></span> <span data-ttu-id="c103e-110">Dies eignet sich im Allgemeinen für nicht verteilte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c103e-110">This is generally fine for nondistributed applications.</span></span> <span data-ttu-id="c103e-111">Dieser Programmierstil generiert jedoch komplizierteren RPC-Unterstützungs Code.</span><span class="sxs-lookup"><span data-stu-id="c103e-111">However, this style of programming generates more complicated RPC support code.</span></span> <span data-ttu-id="c103e-112">Die Client-und serverstubdateien erfordern zusätzlichen Code zum Verwalten der Daten und Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c103e-112">The client and server stubs require the additional code to manage the data and the pointers.</span></span> <span data-ttu-id="c103e-113">Der zugrunde liegende Stubcode muss die verschiedenen Zeiger auf die Adressen auflösen und ermitteln, welche Kopie der Daten die aktuellste Version darstellt.</span><span class="sxs-lookup"><span data-stu-id="c103e-113">The underlying stub code must resolve the various pointers to the addresses and determine which copy of the data represents the most recent version.</span></span>

<span data-ttu-id="c103e-114">Die Verarbeitungs Menge kann reduziert werden, wenn Sie sicherstellen, dass der Zeiger die einzige Möglichkeit ist, auf diesen Speicherbereich zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c103e-114">The amount of processing can be reduced if you guarantee that your pointer is the only way the application can access that area of memory.</span></span> <span data-ttu-id="c103e-115">Der Zeiger kann noch viele der Features eines C-Zeigers aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c103e-115">The pointer can still have many of the features of a C pointer.</span></span> <span data-ttu-id="c103e-116">Beispielsweise kann er zwischen **null** -Werten und nicht-**null** -Werten wechseln oder unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="c103e-116">For example, it can change between **null** and non-**null** values or stay the same.</span></span> <span data-ttu-id="c103e-117">Dies wird anhand des folgenden Beispiels veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c103e-117">The following example illustrates this.</span></span> <span data-ttu-id="c103e-118">Der Zeiger ist vor dem-Befehl **null** und zeigt auf eine gültige Zeichenfolge nach dem-Befehl:</span><span class="sxs-lookup"><span data-stu-id="c103e-118">The pointer is **null** before the call and points to a valid string after the call:</span></span>

![Zeiger Wechsel zwischen NULL-Werten und nicht-NULL-Werten](images/prog-a01.png)

<span data-ttu-id="c103e-120">Standardmäßig wendet der mittlerer l-Compiler das \[ [eindeutige](/windows/desktop/Midl/unique) \] Zeiger Attribut auf alle Zeiger an, die keine Parameter sind.</span><span class="sxs-lookup"><span data-stu-id="c103e-120">By default, the MIDL compiler applies the \[ [unique](/windows/desktop/Midl/unique)\] pointer attribute to all pointers that are not parameters.</span></span> <span data-ttu-id="c103e-121">Diese Standardeinstellung kann mit dem \[ [Zeiger \_ default](/windows/desktop/Midl/pointer-default) -Attribut geändert werden \] .</span><span class="sxs-lookup"><span data-stu-id="c103e-121">This default setting can be changed with the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] attribute.</span></span>

<span data-ttu-id="c103e-122">Ein eindeutiger Zeiger weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="c103e-122">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="c103e-123">Der Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c103e-123">It can have the value **null**.</span></span>
-   <span data-ttu-id="c103e-124">Sie kann während des-Aufrufes von **null** in ungleich **null** wechseln.</span><span class="sxs-lookup"><span data-stu-id="c103e-124">It can change from **null** to non-**null** during the call.</span></span> <span data-ttu-id="c103e-125">Wenn der Wert in einen nicht-**null**-Wert geändert wird, wird bei der Rückgabe neuer Speicher zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c103e-125">When the value changes to non-**null**, new memory is allocated on return.</span></span>
-   <span data-ttu-id="c103e-126">Sie kann während des Aufrufes von ungleich **null** zu **null** wechseln.</span><span class="sxs-lookup"><span data-stu-id="c103e-126">It can change from non-**null** to **null** during the call.</span></span> <span data-ttu-id="c103e-127">Wenn der Wert in **null** geändert wird, ist die Anwendung dafür verantwortlich, den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c103e-127">When the value changes to **NULL**, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="c103e-128">Der Wert kann von einem nicht-**null** -Wert in einen anderen Wert geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c103e-128">The value can change from one non-**null** value to another.</span></span>
-   <span data-ttu-id="c103e-129">Auf den Speicher, auf den ein eindeutiger Zeiger verweist, kann von keinem anderen Zeiger oder Namen im Vorgang zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="c103e-129">The storage that a unique pointer points to cannot be accessed by any other pointer or name in the operation.</span></span>
-   <span data-ttu-id="c103e-130">Rückgabe Daten werden in den vorhandenen Speicher geschrieben, wenn der Zeiger nicht den Wert **null** hat.</span><span class="sxs-lookup"><span data-stu-id="c103e-130">Return data is written into existing storage if the pointer does not have the value **null**.</span></span>

<span data-ttu-id="c103e-131">Im folgenden Beispiel wird veranschaulicht, wie ein eindeutiger Zeiger definiert wird.</span><span class="sxs-lookup"><span data-stu-id="c103e-131">The following example demonstrates how to define a unique pointer.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

<span data-ttu-id="c103e-132">In diesem Beispiel ist der Parameter " *Ach* " ein eindeutiger Zeiger auf Zeichendaten, die an einen Server gesendet werden, der mit der remotefn-Routine verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="c103e-132">In this example, the parameter *ach* is a unique pointer to character data that is sent to a server to be processed with the RemoteFn routine.</span></span>

 

 