---
description: Die Verwendung von Kommas und Semikolons kann das komplexeste Syntax Problem im Dateiformat sein, und diese Verwendung ist sehr streng. Kommas werden verwendet, um Array Elemente voneinander zu trennen. die einzelnen Datenelemente werden durch Semikolons beendet.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Verwendung von Kommas und Semikolons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba238d50ff5d0dace017f16b75547df6b016e14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125570"
---
# <a name="use-of-commas-and-semicolons"></a><span data-ttu-id="bc199-104">Verwendung von Kommas und Semikolons</span><span class="sxs-lookup"><span data-stu-id="bc199-104">Use of Commas and Semicolons</span></span>

<span data-ttu-id="bc199-105">Die Verwendung von Kommas und Semikolons kann das komplexeste Syntax Problem im Dateiformat sein, und diese Verwendung ist sehr streng.</span><span class="sxs-lookup"><span data-stu-id="bc199-105">Using commas and semicolons can be the most complex syntax issue in the file format, and this usage is very strict.</span></span> <span data-ttu-id="bc199-106">Kommas werden verwendet, um Array Elemente voneinander zu trennen. die einzelnen Datenelemente werden durch Semikolons beendet.</span><span class="sxs-lookup"><span data-stu-id="bc199-106">Commas are used to separate array members; semicolons terminate each data item.</span></span>

<span data-ttu-id="bc199-107">Wenn eine Vorlage beispielsweise folgendermaßen definiert wird:</span><span class="sxs-lookup"><span data-stu-id="bc199-107">For example, if a template is defined in the following manner:</span></span>


```
template mytemp {
DWORD myvar;
}
```



<span data-ttu-id="bc199-108">Eine Instanz dieser Vorlage sieht dann wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="bc199-108">Then an instance of this template looks like the following:</span></span>


```
mytemp dataTemp {
1;
}
```



<span data-ttu-id="bc199-109">Wenn eine Vorlage, die eine andere Vorlage enthält, folgendermaßen definiert ist:</span><span class="sxs-lookup"><span data-stu-id="bc199-109">If a template containing another template is defined in the following manner;</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



<span data-ttu-id="bc199-110">Eine Instanz dieser Vorlage sieht dann wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="bc199-110">Then an instance of this template looks like the following:</span></span>


```
container dataContainer {
1.1;
2; 
3;;
}
```



<span data-ttu-id="bc199-111">Beachten Sie, dass die zweite Zeile, die den Wert von mytemp innerhalb des Containers darstellt, zwei Semikolons am Ende der Zeile enthält.</span><span class="sxs-lookup"><span data-stu-id="bc199-111">Note that the second line that represents the mytemp inside container has two semicolons at the end of the line.</span></span> <span data-ttu-id="bc199-112">Das erste Semikolon gibt das Ende des Datenelements an, aTemp (innerhalb des Containers) und das zweite Semikolon das Ende des Containers.</span><span class="sxs-lookup"><span data-stu-id="bc199-112">The first semicolon indicates the end of the data item, aTemp (inside container), and the second semicolon indicates the end of the container.</span></span>

<span data-ttu-id="bc199-113">Wenn ein Array wie folgt definiert wird:</span><span class="sxs-lookup"><span data-stu-id="bc199-113">If an array is defined in the following manner:</span></span>


```
Template mytemp {

array DWORD myvar[3];

}
```



<span data-ttu-id="bc199-114">Dann sieht eine Instanz von wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="bc199-114">Then an instance of this looks like the following:</span></span>


```
mytemp aTemp {
1, 2, 3;
}
```



<span data-ttu-id="bc199-115">Im Array Beispiel ist es nicht erforderlich, dass die Datenelemente durch Semikolons getrennt werden, da Sie durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="bc199-115">In the array example, there is no need for the data items to be separated by semicolons because they are delineated by commas.</span></span> <span data-ttu-id="bc199-116">Das Semikolon am Ende markiert das Ende des Arrays.</span><span class="sxs-lookup"><span data-stu-id="bc199-116">The semicolon at the end marks the end of the array.</span></span>

<span data-ttu-id="bc199-117">Stellen Sie sich eine Vorlage vor, die ein Array von Datenelementen enthält, die durch eine Vorlage definiert werden.</span><span class="sxs-lookup"><span data-stu-id="bc199-117">Consider a template that contains an array of data items defined by a template.</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



<span data-ttu-id="bc199-118">Eine Instanz dieses Beispiels würde wie im folgenden Beispiel aussehen.</span><span class="sxs-lookup"><span data-stu-id="bc199-118">An instance of this would look like the following example.</span></span>


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a><span data-ttu-id="bc199-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc199-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc199-120">Text Codierung</span><span class="sxs-lookup"><span data-stu-id="bc199-120">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



