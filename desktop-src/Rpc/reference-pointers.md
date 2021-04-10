---
title: Verweis Zeiger
description: Verweis Zeiger sind die einfachsten Zeiger und erfordern die geringste Menge an Verarbeitung durch den Clientstub.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039490"
---
# <a name="reference-pointers"></a><span data-ttu-id="170b2-103">Verweis Zeiger</span><span class="sxs-lookup"><span data-stu-id="170b2-103">Reference Pointers</span></span>

<span data-ttu-id="170b2-104">Verweis Zeiger sind die einfachsten Zeiger und erfordern die geringste Menge an Verarbeitung durch den Clientstub.</span><span class="sxs-lookup"><span data-stu-id="170b2-104">Reference pointers are the simplest pointers and require the least amount of processing by the client stub.</span></span> <span data-ttu-id="170b2-105">Wenn ein Client Programm einen Verweis Zeiger an eine Remote Prozedur übergibt, enthält der Verweis Zeiger immer die Adresse eines gültigen Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="170b2-105">When a client program passes a reference pointer to a remote procedure, the reference pointer always contains the address of a valid block of memory.</span></span> <span data-ttu-id="170b2-106">Es wird immer noch auf denselben Speicherblock verwiesen, wenn die Remote Prozedur abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="170b2-106">It will still be pointing to the same memory block when the remote procedure completes.</span></span> <span data-ttu-id="170b2-107">Diese Zeiger werden hauptsächlich verwendet, um Verweis Semantik zu implementieren und \[ [**out**](/windows/desktop/Midl/out-idl) - \] Parameter in C zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="170b2-107">These pointers are mainly used to implement reference semantics, and to allow for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters in C.</span></span>

<span data-ttu-id="170b2-108">Im folgenden Beispiel ändert sich der Wert des-Zeigers während des-Aufrufes nicht, obwohl sich der Inhalt der Daten an der durch den Zeiger gekennzeichneten Adresse ändern kann.</span><span class="sxs-lookup"><span data-stu-id="170b2-108">In the following example, the value of the pointer does not change during the call, although the contents of the data at the address indicated by the pointer can change.</span></span>

![Daten, die sich an einer statischen Verweis Zeiger Adresse ändern](images/prog-a07.png)

<span data-ttu-id="170b2-110">Ein Verweis Zeiger hat die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="170b2-110">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="170b2-111">Er verweist immer auf einen gültigen Speicher und hat nie den Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="170b2-111">It always points to valid storage and never has the value **NULL**.</span></span>
-   <span data-ttu-id="170b2-112">Sie ändert sich nie während eines Aufrufes und zeigt immer auf denselben Speicher vor und nach dem-Befehl.</span><span class="sxs-lookup"><span data-stu-id="170b2-112">It never changes during a call and always points to the same storage before and after the call.</span></span>
-   <span data-ttu-id="170b2-113">Daten, die von der Remote Prozedur zurückgegeben werden, werden in den vorhandenen Speicher geschrieben.</span><span class="sxs-lookup"><span data-stu-id="170b2-113">Data returned from the remote procedure is written into the existing storage.</span></span>
-   <span data-ttu-id="170b2-114">Auf den Speicher, auf den von einem Verweis Zeiger verwiesen wird, kann nicht von einem anderen Zeiger oder einem anderen Namen in der Funktion zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="170b2-114">The storage pointed to by a reference pointer cannot be accessed by any other pointer or any other name in the function.</span></span>

<span data-ttu-id="170b2-115">Verwenden Sie das \[ [**ref**](/windows/desktop/Midl/ref) - \] Attribut, um Verweis Zeiger in Schnittstellendefinitionen anzugeben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="170b2-115">Use the \[[**ref**](/windows/desktop/Midl/ref)\] attribute to specify reference pointers in interface definitions, as shown in the following example.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

<span data-ttu-id="170b2-116">In diesem Beispiel wird der Parameter *PChar* als Zeiger auf ein einzelnes Zeichen, nicht auf ein Array von Zeichen definiert.</span><span class="sxs-lookup"><span data-stu-id="170b2-116">This example defines the parameter *pChar* as a pointer to a single character, not an array of characters.</span></span> <span data-ttu-id="170b2-117">Dabei handelt es sich um einen \[ **out** \] -Parameter und einen Verweis Zeiger, der auf den Arbeitsspeicher verweist, der von der Server Routine remotefn mit Daten aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="170b2-117">It is an \[**out**\] parameter and a reference pointer that points to memory that the server routine RemoteFn will fill with data.</span></span>

 

 