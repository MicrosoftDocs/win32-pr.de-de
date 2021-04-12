---
title: " in-, out-, size_is-Prototyp"
description: '\ in, out, size \_ ist \ Prototype verwendet ein Array mit nur einem zählenden Zeichen, das vom Client an den Server und vom Server an den Client übermittelt wird.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315374"
---
# <a name="in-out-size_is-prototype"></a><span data-ttu-id="8c92a-103">\[in, out, size \_ ist \] Prototype</span><span class="sxs-lookup"><span data-stu-id="8c92a-103">\[in, out, size\_is\] Prototype</span></span>

<span data-ttu-id="8c92a-104">Der folgende Funktionsprototyp verwendet ein Array mit einzelnen Zeichen, das auf beide Arten übermittelt wird: vom Client zum Server und von Server zu Client:</span><span class="sxs-lookup"><span data-stu-id="8c92a-104">The following function prototype uses a single-counted character array that is passed both ways: from client to server and from server to client:</span></span>

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

<span data-ttu-id="8c92a-105">Als \[ [**in**](/windows/desktop/Midl/in) - \] Parameter muss " *achinout* " auf der Clientseite auf einen gültigen Speicher zeigen.</span><span class="sxs-lookup"><span data-stu-id="8c92a-105">As an \[[**in**](/windows/desktop/Midl/in)\] parameter, *achInOut* must point to valid storage on the client side.</span></span> <span data-ttu-id="8c92a-106">Der Entwickler ordnet dem Array auf der Clientseite Arbeitsspeicher zu, bevor der Remote Prozedur Aufrufe durchführen wird.</span><span class="sxs-lookup"><span data-stu-id="8c92a-106">The developer allocates memory associated with the array on the client side before making the remote procedure call.</span></span>

<span data-ttu-id="8c92a-107">Die Stub verwenden die \[ [**Größe \_**](/windows/desktop/Midl/size-is) des \] para  meters "-Parameter", um Arbeitsspeicher auf dem Server zuzuweisen, und verwenden dann die \[ [**Länge \_**](/windows/desktop/Midl/length-is) des \] Parameters " *pcbSize* ", um die Array Elemente in diesen Speicher zu übertragen</span><span class="sxs-lookup"><span data-stu-id="8c92a-107">The stubs use the \[[**size\_is**](/windows/desktop/Midl/size-is)\] parameter *strsize* to allocate memory on the server and then use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] parameter *pcbSize* to transmit the array elements into this memory.</span></span> <span data-ttu-id="8c92a-108">Der Entwickler muss sicherstellen, dass der Client Code die **\[ Länge \_ ist \]** variabel festlegt, bevor die Remote Prozedur aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8c92a-108">The developer must make sure the client code sets the **\[length\_is\]** variable before calling the remote procedure.</span></span>

<span data-ttu-id="8c92a-109">In einigen Fällen ist die Verwendung von separaten Parametern anstelle einer einzelnen Zeichenfolge für die Eingabe und Ausgabe effizienter und bietet Flexibilität.</span><span class="sxs-lookup"><span data-stu-id="8c92a-109">In some situations, using separate parameters instead of a single string for the input and output is more efficient and provides flexibility.</span></span> <span data-ttu-id="8c92a-110">Dies wird im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="8c92a-110">This is demonstrated in the next example:</span></span>

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

<span data-ttu-id="8c92a-111">Im vorherigen Beispiel wird das Zeichen Array "achinout" auch als out- \[ [](/windows/desktop/Midl/out-idl) \] Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c92a-111">In the previous example, the character array achInOut is also used as an \[[**out**](/windows/desktop/Midl/out-idl)\] parameter.</span></span> <span data-ttu-id="8c92a-112">In C entspricht der Name des Arrays der Verwendung eines Zeigers.</span><span class="sxs-lookup"><span data-stu-id="8c92a-112">In C, the name of the array is equivalent to the use of a pointer.</span></span> <span data-ttu-id="8c92a-113">Standardmäßig handelt es sich bei allen Zeigern auf oberster Ebene um Verweis Zeiger – Sie ändern nicht den Wert und zeigen auf den gleichen Arbeitsspeicher Bereich auf dem Client vor und nach dem-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="8c92a-113">By default, all top-level pointers are reference pointers — they do not change in value and they point to the same area of memory on the client before and after the call.</span></span> <span data-ttu-id="8c92a-114">Der gesamte Arbeitsspeicher, auf den die Remote Prozedur zugreift, muss der Größe entsprechen, die der Client vor dem-Befehl angibt, oder die stubweise generiert eine Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="8c92a-114">All memory that the remote procedure accesses must fit the size that the client specifies before the call, or the stubs will generate an exception.</span></span>

<span data-ttu-id="8c92a-115">Vor der Rückgabe muss die Funktion "analysieren" auf dem Server den *pcbSize* -Parameter zurücksetzen, um die Anzahl der Elemente anzugeben, die der Server wie dargestellt an den Client übertragen wird:</span><span class="sxs-lookup"><span data-stu-id="8c92a-115">Before returning, the Analyze function on the server must reset the *pcbSize* parameter to indicate the number of elements that the server will transmit to the client as shown:</span></span>

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 