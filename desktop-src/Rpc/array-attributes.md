---
title: Arrayattribute
description: Es gibt eine enge Beziehung zwischen Arrays und Zeigern in der Programmiersprache C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed669a2a81528afa84b41a1be25a0c84f70fbe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729433"
---
# <a name="array-attributes"></a><span data-ttu-id="d8048-103">Arrayattribute</span><span class="sxs-lookup"><span data-stu-id="d8048-103">Array Attributes</span></span>

<span data-ttu-id="d8048-104">Es gibt eine enge Beziehung zwischen Arrays und Zeigern in der Programmiersprache C.</span><span class="sxs-lookup"><span data-stu-id="d8048-104">There is a close relationship between arrays and pointers in the C language.</span></span> <span data-ttu-id="d8048-105">Wenn ein Array Name als Parameter an eine Funktion übergeben wird, wird er als Zeiger auf das erste Element des Arrays behandelt, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d8048-105">When passed as a parameter to a function, an array name is treated as a pointer to the first element of the array, as shown in the following example:</span></span>


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



<span data-ttu-id="d8048-106">In einem lokalen-Befehl können Sie den Zeiger Parameter verwenden, um den Arbeitsspeicher zu durchsuchen und den Inhalt anderer Adressen zu untersuchen:</span><span class="sxs-lookup"><span data-stu-id="d8048-106">In a local call, you can use the pointer parameter to march through memory and examine the contents of other addresses:</span></span>


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



<span data-ttu-id="d8048-107">Wenn ein Client einen Zeiger an eine Remote Prozedur übergibt, überträgt der Clientstub den Zeiger und die Daten, auf die er verweist.</span><span class="sxs-lookup"><span data-stu-id="d8048-107">When a client passes a pointer to a remote procedure, the client stub transmits both the pointer and the data it points to.</span></span> <span data-ttu-id="d8048-108">Wenn der Zeiger nicht auf seine entsprechenden Daten beschränkt ist, muss der gesamte Arbeitsspeicher des Clients mit jedem Remote-Befehl übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="d8048-108">Unless the pointer is restricted to its corresponding data, all the client's memory must be transmitted with every remote call.</span></span> <span data-ttu-id="d8048-109">Durch erzwingen der starken Typisierung in der Schnittstellen Definition schränkt die Client-Stub-Verarbeitung von der Mittell auf die Daten ein, die dem angegebenen Zeiger entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d8048-109">By enforcing strong typing in the interface definition, MIDL limits client-stub processing to the data that corresponds to the specified pointer.</span></span>

<span data-ttu-id="d8048-110">Die Größe des Arrays und der Bereich der Array Elemente, die an den Remote Computer übertragen werden, können konstant oder variabel sein.</span><span class="sxs-lookup"><span data-stu-id="d8048-110">The size of the array and the range of array elements transmitted to the remote computer can be constant or variable.</span></span> <span data-ttu-id="d8048-111">Wenn diese Werte variabel sind und daher zur Laufzeit bestimmt werden, müssen Sie Attribute in der IDL-Datei verwenden, um anzugeben, wie viele Array Elemente übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8048-111">When these values are variable, and thus determined at run time, you must use attributes in the IDL file to specify how many array elements to transmit.</span></span> <span data-ttu-id="d8048-112">Die folgenden Mittell-Attribute unterstützen Array Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="d8048-112">The following MIDL attributes support array bounds.</span></span>



| <span data-ttu-id="d8048-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="d8048-113">Attribute</span></span>                             | <span data-ttu-id="d8048-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8048-114">Description</span></span>                                             | <span data-ttu-id="d8048-115">Standard</span><span class="sxs-lookup"><span data-stu-id="d8048-115">Default</span></span> |
|---------------------------------------|---------------------------------------------------------|---------|
| <span data-ttu-id="d8048-116">\[der [ **erste \_ ist**](/windows/desktop/Midl/first-is)\]</span><span class="sxs-lookup"><span data-stu-id="d8048-116">\[ [**first\_is**](/windows/desktop/Midl/first-is)\]</span></span>   | <span data-ttu-id="d8048-117">Der Index des ersten übertragenen Array Elements.</span><span class="sxs-lookup"><span data-stu-id="d8048-117">Index of the first array element transmitted.</span></span>           | <span data-ttu-id="d8048-118">0</span><span class="sxs-lookup"><span data-stu-id="d8048-118">0</span></span>       |
| <span data-ttu-id="d8048-119">\[[ **Letzter \_ ist**](/windows/desktop/Midl/last-is)\]</span><span class="sxs-lookup"><span data-stu-id="d8048-119">\[ [**last\_is**](/windows/desktop/Midl/last-is)\]</span></span>     | <span data-ttu-id="d8048-120">Der Index des letzten übertragenen Array Elements.</span><span class="sxs-lookup"><span data-stu-id="d8048-120">Index of the last array element transmitted.</span></span>            | \-      |
| <span data-ttu-id="d8048-121">\[[ **Länge \_ ist**](/windows/desktop/Midl/length-is)\]</span><span class="sxs-lookup"><span data-stu-id="d8048-121">\[ [**length\_is**](/windows/desktop/Midl/length-is)\]</span></span> | <span data-ttu-id="d8048-122">Gesamtanzahl der übertragenen Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="d8048-122">Total number of array elements transmitted.</span></span>             | \-      |
| <span data-ttu-id="d8048-123">\[[ **Max \_ ist**](/windows/desktop/Midl/max-is)\]</span><span class="sxs-lookup"><span data-stu-id="d8048-123">\[ [**max\_is**](/windows/desktop/Midl/max-is)\]</span></span>       | <span data-ttu-id="d8048-124">Höchster gültiger Array Indexwert.</span><span class="sxs-lookup"><span data-stu-id="d8048-124">Highest valid array index value.</span></span>                        | \-      |
| <span data-ttu-id="d8048-125">\[[ **Min \_ ist**](/windows/desktop/Midl/min-is)\]</span><span class="sxs-lookup"><span data-stu-id="d8048-125">\[ [**min\_is**](/windows/desktop/Midl/min-is)\]</span></span>       | <span data-ttu-id="d8048-126">Niedrigster gültiger Array Indexwert.</span><span class="sxs-lookup"><span data-stu-id="d8048-126">Lowest valid array index value.</span></span>                         | <span data-ttu-id="d8048-127">0</span><span class="sxs-lookup"><span data-stu-id="d8048-127">0</span></span>       |
| <span data-ttu-id="d8048-128">\[[ **Größe \_** :](/windows/desktop/Midl/size-is)\]</span><span class="sxs-lookup"><span data-stu-id="d8048-128">\[ [**size\_is**](/windows/desktop/Midl/size-is)\]</span></span>     | <span data-ttu-id="d8048-129">Die Gesamtanzahl der für das Array zugeordneten Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="d8048-129">Total number of array elements allocated for the array.</span></span> | \-      |



 

> [!Note]  
> <span data-ttu-id="d8048-130">Das **Min \_ is** -Attribut ist in RPC nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d8048-130">The **min\_is** attribute is not implemented in RPC.</span></span> <span data-ttu-id="d8048-131">Der minimale Array Index wird immer als 0 (null) behandelt.</span><span class="sxs-lookup"><span data-stu-id="d8048-131">The minimum array index is always treated as zero.</span></span>

 

 

 