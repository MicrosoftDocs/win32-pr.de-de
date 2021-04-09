---
title: Direktionale Attribute (Parameter)
description: Direktionale Attribute beschreiben, ob die Daten vom Client an den Server, den Server an den Client oder beides übertragen werden.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, direktionale Attribute
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec37dbf65919f5aae9e7674cf7102eddcdf5170
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101990"
---
# <a name="directional-parameter-attributes"></a><span data-ttu-id="6b1e3-106">Direktionale Attribute (Parameter)</span><span class="sxs-lookup"><span data-stu-id="6b1e3-106">Directional (Parameter) Attributes</span></span>

<span data-ttu-id="6b1e3-107">Direktionale Attribute beschreiben, ob die Daten vom Client an den Server, den Server an den Client oder beides übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-107">Directional attributes describe whether the data is transmitted from client to server, server to client, or both.</span></span> <span data-ttu-id="6b1e3-108">Alle Parameter im Funktionsprototyp müssen direktionalen Attributen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-108">All parameters in the function prototype must be associated with directional attributes.</span></span> <span data-ttu-id="6b1e3-109">Die drei möglichen Kombinationen von direktionalen Attributen lauten: 1) \[ [**in**](/windows/desktop/Midl/in) \] , 2) ausgehend \[ [](/windows/desktop/Midl/out-idl) \] und 3) \[ **in**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="6b1e3-109">The three possible combinations of directional attributes are: 1) \[[**in**](/windows/desktop/Midl/in)\], 2) \[[**out**](/windows/desktop/Midl/out-idl)\], and 3) \[**in**, **out**\].</span></span> <span data-ttu-id="6b1e3-110">Diese beschreiben, wie Parameter zwischen aufrufenden und aufgerufenen Prozeduren übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-110">These describe the way parameters are passed between calling and called procedures.</span></span> <span data-ttu-id="6b1e3-111">Wenn Sie im Standardmodus (Microsoft-erweiterter Modus) kompilieren und ein direktionales Attribut für einen Parameter weglassen, nimmt der Mittelwert Compiler den Standardwert \[ **in an** \] .</span><span class="sxs-lookup"><span data-stu-id="6b1e3-111">When you compile in the default (Microsoft-extended mode) and you omit a directional attribute for a parameter, the MIDL compiler assumes a default value of \[**in**\].</span></span>

<span data-ttu-id="6b1e3-112">Ein \[ [**out**](/windows/desktop/Midl/out-idl) - \] Parameter muss ein Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-112">An \[[**out**](/windows/desktop/Midl/out-idl)\] parameter must be a pointer.</span></span> <span data-ttu-id="6b1e3-113">Tatsächlich ist das \[ **out** - \] Attribut nicht sinnvoll, wenn es auf Parameter angewendet wird, die nicht als Zeiger fungieren, da C-Funktionsparameter als Wert übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-113">In fact, the \[**out**\] attribute is not meaningful when applied to parameters that do not act as pointers because C function parameters are passed by value.</span></span> <span data-ttu-id="6b1e3-114">In C empfängt die aufgerufene Funktion eine private Kopie des Parameter Werts. der Wert der aufrufenden Funktion für diesen Parameter kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-114">In C, the called function receives a private copy of the parameter value; it cannot change the calling function's value for that parameter.</span></span> <span data-ttu-id="6b1e3-115">Wenn der Parameter jedoch als Zeiger fungiert, kann er verwendet werden, um auf den Speicher zuzugreifen und ihn zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-115">If the parameter acts as a pointer, however, it can be used to access and modify memory.</span></span> <span data-ttu-id="6b1e3-116">Das \[ **out** \] -Attribut gibt an, dass die Server Funktion den Wert an die aufrufende Funktion des Clients zurückgeben soll und dass der dem Zeiger zugeordnete Arbeitsspeicher in Übereinstimmung mit den Attributen zurückgegeben werden soll, die dem Zeiger zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-116">The \[**out**\] attribute indicates that the server function should return the value to the client's calling function, and that memory associated with the pointer should be returned in accordance with the attributes assigned to the pointer.</span></span>

<span data-ttu-id="6b1e3-117">Die folgende Schnittstelle veranschaulicht die drei möglichen Kombinationen direktionaler Attribute, die auf einen Parameter angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-117">The following interface demonstrates the three possible combinations of directional attributes that can be applied to a parameter.</span></span> <span data-ttu-id="6b1e3-118">Die **inoutproc** -Funktion ist in der IDL-Datei wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="6b1e3-118">The function **InOutProc** is defined in the IDL file as:</span></span>

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

<span data-ttu-id="6b1e3-119">Der erste Parameter ( *S1*) ist \[ nur [**in**](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="6b1e3-119">The first parameter, *s1*, is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="6b1e3-120">Der Wert wird an den Remote Computer übertragen, aber nicht an die aufrufenden Prozeduren zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-120">Its value is transmitted to the remote computer, but is not returned to the calling procedure.</span></span> <span data-ttu-id="6b1e3-121">Obwohl die Serveranwendung ihren Wert für *S1* ändern kann, ist der Wert von *S1* auf dem Client vor und nach dem-Befehl identisch.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-121">Although the server application can change its value for *s1*, the value of *s1* on the client is the same before and after the call.</span></span>

<span data-ttu-id="6b1e3-122">Der zweite Parameter, " *PS2*", wird im Funktionsprototyp als Zeiger mit den Attributen " \[ [**in**](/windows/desktop/Midl/in) " \] und " \[ [**out**](/windows/desktop/Midl/out-idl) " definiert \] .</span><span class="sxs-lookup"><span data-stu-id="6b1e3-122">The second parameter, *ps2*, is defined in the function prototype as a pointer with both \[[**in**](/windows/desktop/Midl/in)\] and \[[**out**](/windows/desktop/Midl/out-idl)\] attributes.</span></span> <span data-ttu-id="6b1e3-123">Das \[ **in** - \] Attribut gibt an, dass der Wert des-Parameters vom Client an den Server übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-123">The \[**in**\] attribute indicates that the value of the parameter is passed from the client to the server.</span></span> <span data-ttu-id="6b1e3-124">Das \[ **out** - \] Attribut gibt an, dass der Wert, auf den von *PS2* verwiesen wird, dem Client zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-124">The \[**out**\] attribute indicates that the value pointed to by *ps2* is returned to the client.</span></span>

<span data-ttu-id="6b1e3-125">Der dritte Parameter ist \[ nur [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="6b1e3-125">The third parameter is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="6b1e3-126">Für den Parameter auf dem Server ist Speicherplatz zugeordnet, aber der Wert ist beim Eintrag nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-126">Space is allocated for the parameter on the server, but the value is undefined on entry.</span></span> <span data-ttu-id="6b1e3-127">Wie bereits erwähnt, müssen alle \[ **out** - \] Parameter Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-127">As mentioned above, all \[**out**\] parameters must be pointers.</span></span>

<span data-ttu-id="6b1e3-128">Die Remote Prozedur ändert den Wert aller drei Parameter, aber nur die neuen Werte der \[ [](/windows/desktop/Midl/out-idl) \] Parameter out und \[ [**in**](/windows/desktop/Midl/in) stehen \] dem Client zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-128">The remote procedure changes the value of all three parameters, but only the new values of the \[[**out**](/windows/desktop/Midl/out-idl)\] and \[[**in**](/windows/desktop/Midl/in)\] parameters are available to the client.</span></span>


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



<span data-ttu-id="6b1e3-129">Bei der Rückgabe des Aufrufes **inoutproc** werden der zweite und der dritte Parameter geändert.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-129">On return from the call to **InOutProc**, the second and third parameters are modified.</span></span> <span data-ttu-id="6b1e3-130">Der erste Parameter, der nur \[ [**in**](/windows/desktop/Midl/in) ist \] , ist unverändert.</span><span class="sxs-lookup"><span data-stu-id="6b1e3-130">The first parameter, which is \[[**in**](/windows/desktop/Midl/in)\] only, is unchanged.</span></span>

![in-Parameter](images/prog-a22.png)

![out-Parameter](images/prog-a23.png)

![in-out-Parameter](images/prog-a21.png)

 

 