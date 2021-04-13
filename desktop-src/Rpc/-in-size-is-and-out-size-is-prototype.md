---
title: " in, size_is und Out, size_is Prototyp"
description: Der folgende Funktionsprototyp verwendet zwei gezählte Zeichen folgen. Der Entwickler muss Code sowohl auf dem Client als auch auf dem Server schreiben, um die Zeichen Array Längen und Pass Parameter zu verfolgen, die die stubwerte angeben, wie viele Array Elemente übertragen werden sollen.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03dbb4dd65d44122bea7ff086013295e0bf616d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390896"
---
# <a name="in-size_is-and-out-size_is-prototype"></a><span data-ttu-id="a5618-104">\[in, Größe \_ ist \] und ausgehend \[ , Größe \_ ist \] Prototyp</span><span class="sxs-lookup"><span data-stu-id="a5618-104">\[in, size\_is\] and \[out, size\_is\] Prototype</span></span>

<span data-ttu-id="a5618-105">Der folgende Funktionsprototyp verwendet zwei gezählte Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="a5618-105">The following function prototype uses two counted strings.</span></span> <span data-ttu-id="a5618-106">Der Entwickler muss Code sowohl auf dem Client als auch auf dem Server schreiben, um die Zeichen Array Längen und Pass Parameter zu verfolgen, die die stubwerte angeben, wie viele Array Elemente übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a5618-106">The developer must write code on both client and server to keep track of the character array lengths and pass parameters that tell the stubs how many array elements to transmit.</span></span>

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

<span data-ttu-id="a5618-107">Beachten Sie, dass die Parameter, die die Array Länge beschreiben, in der gleichen Richtung wie die Arrays übertragen werden: *cbin* und *Achin* sind \[ [](/windows/desktop/Midl/in) \] Parameter, während *PCBout* und *achout* \[ [](/windows/desktop/Midl/out-idl) \] Parameter sind.</span><span class="sxs-lookup"><span data-stu-id="a5618-107">Note the parameters that describe the array length are transmitted in the same direction as the arrays: *cbIn* and *achIn* are \[[**in**](/windows/desktop/Midl/in)\] parameters while *pcbOut* and *achOut* are \[[**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="a5618-108">Als **\[ out \]** -Parameter muss der Parameter *PCBout* der C-Konvention folgen und als Zeiger deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="a5618-108">As an **\[out\]** parameter, the parameter *pcbOut* must follow C convention and be declared as a pointer.</span></span>

<span data-ttu-id="a5618-109">Der Client Code zählt die Anzahl der Zeichen in der Zeichenfolge, einschließlich der nachfolgenden NULL, vor dem Aufrufen der Remote Prozedur, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="a5618-109">The client code counts the number of characters in the string, including the trailing zero, before calling the remote procedure as shown:</span></span>

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

<span data-ttu-id="a5618-110">Die Remote Prozedur auf dem Server liefert die Länge des Rückgabe Puffers in *cbout* , wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="a5618-110">The remote procedure on the server supplies the length of the return buffer in *cbOut* as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchIn,
             long cbIn,
             char *pchOut,
             long *pcbOut)
{
   ...
   *pcbOut = strlen(pchOut) + 1; // transmitted elements
   return;
}
```

<span data-ttu-id="a5618-111">Das \[ **String** - \] Attribut kann verwendet werden, wenn ein Parameter bekanntermaßen eine Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="a5618-111">The \[**string**\] attribute can be utilized when a parameter is known to be a string.</span></span> <span data-ttu-id="a5618-112">Dieses Attribut weist den Stub an, die Zeichen folgen Größe zu berechnen. Dadurch entfällt der Aufwand, der der \[ [**Länge der Länge**](/windows/desktop/Midl/size-is) von \] Parametern zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a5618-112">This attribute directs the stub to calculate the string size, thus eliminating the overhead associated with the \[[**length is**](/windows/desktop/Midl/size-is)\] parameters.</span></span> <span data-ttu-id="a5618-113">Außerdem wird der Stub angewiesen, zu überprüfen, ob die Zeichenfolge **null** endet, bevor der Parameter an die Anwendung übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a5618-113">Additionally, it will direct the stub to verify the string is **NULL** terminated before passing the parameter to the application.</span></span>

 

 