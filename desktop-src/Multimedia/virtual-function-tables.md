---
title: Virtuelle Funktionstabellen
description: Virtuelle Funktionstabellen
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341841"
---
# <a name="virtual-function-tables"></a><span data-ttu-id="e54d3-103">Virtuelle Funktionstabellen</span><span class="sxs-lookup"><span data-stu-id="e54d3-103">Virtual Function Tables</span></span>

<span data-ttu-id="e54d3-104">Eine virtuelle Funktions Tabelle ist ein Array von Zeigern auf die Methoden, die von einem Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e54d3-104">A virtual function table is an array of pointers to the methods an object supports.</span></span> <span data-ttu-id="e54d3-105">Wenn Sie C verwenden, wird ein Objekt als Struktur angezeigt, deren erstes Element ein Zeiger auf die virtuelle Funktions Tabelle (**lpvtbl**) ist. Das heißt, das erste Element verweist auf ein Array mit Funktions Zeigern.</span><span class="sxs-lookup"><span data-stu-id="e54d3-105">If you're using C, an object appears as a structure whose first member is a pointer to the virtual function table (**lpVtbl**); that is, the first member points to an array containing function pointers.</span></span> <span data-ttu-id="e54d3-106">Die Methoden übernehmen einen Zeiger auf die Funktions Tabelle als ersten Parameter.</span><span class="sxs-lookup"><span data-stu-id="e54d3-106">The methods all take a pointer to the function table as the first parameter.</span></span> <span data-ttu-id="e54d3-107">Daher wird im folgenden Beispiel die **Read** -Methode eines **pStream** -Objekts aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="e54d3-107">Thus, the following example calls the **Read** method of a **pStream** object:</span></span>


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



<span data-ttu-id="e54d3-108">In C + + ist der Zeiger auf die virtuelle Funktions Tabelle, der *this* -Zeiger, implizit.</span><span class="sxs-lookup"><span data-stu-id="e54d3-108">In C+ +, the pointer to the virtual function table, the *this* pointer, is implicit.</span></span> <span data-ttu-id="e54d3-109">Das folgende Beispiel entspricht dem vorherigen Beispiel bei Verwendung von C + +:</span><span class="sxs-lookup"><span data-stu-id="e54d3-109">The following is equivalent to the previous example when using C+ +:</span></span>


```C++
pStream->Read(parameters) 
 
```



 

 




