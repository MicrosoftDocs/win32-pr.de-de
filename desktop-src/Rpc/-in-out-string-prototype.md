---
title: " in, out, Zeichen folgen Prototyp"
description: Der folgende Funktionsprototyp verwendet einen einzelnen \ in-, out-, String \-Parameter für die Eingabe-und Ausgabe Zeichenfolgen.
ms.assetid: 5a652b79-11ca-4780-aac1-60a22f96b4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed8ed47c02ea3e08672d529bf7ce9f627925518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948846"
---
# <a name="in-out-string-prototype"></a><span data-ttu-id="fe7b7-103">\[in, out, Zeichen folgen \] Prototyp</span><span class="sxs-lookup"><span data-stu-id="fe7b7-103">\[in, out, string\] Prototype</span></span>

<span data-ttu-id="fe7b7-104">Der folgende Funktionsprototyp verwendet einen einzelnen \[ [**in**](/windows/desktop/Midl/in)-, [**out**](/windows/desktop/Midl/out-idl)-und Zeichen folgen Parameter für die Eingabe-und Ausgabe [**Zeichenfolgen**](/windows/desktop/Midl/string) \] .</span><span class="sxs-lookup"><span data-stu-id="fe7b7-104">The following function prototype uses a single \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), [**string**](/windows/desktop/Midl/string)\] parameter for both the input and output strings.</span></span> <span data-ttu-id="fe7b7-105">Die Zeichenfolge enthält zunächst Patienten Eingaben und wird dann mit der Antwort des Arztes überschrieben, wie im folgenden gezeigt:</span><span class="sxs-lookup"><span data-stu-id="fe7b7-105">The string first contains patient input and is then overwritten with the doctor response as shown:</span></span>

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

<span data-ttu-id="fe7b7-106">Dieses Beispiel ähnelt dem Beispiel, in dem eine Zeichenfolge mit einem Zeichen sowohl für die Eingabe als auch für die Ausgabe verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fe7b7-106">This example is similar to the one that employed a single-counted string for both input and output.</span></span> <span data-ttu-id="fe7b7-107">Wie bei diesem Beispiel bestimmt die \[ [**Größe \_**](/windows/desktop/Midl/size-is) " \] Attribute" die Anzahl der Elemente, die auf dem Server zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fe7b7-107">As with that example, the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute determines the number of elements allocated on the server.</span></span> <span data-ttu-id="fe7b7-108">Das \[ [**String**](/windows/desktop/Midl/string) - \] Attribut weist den Stub an, " **strinlen** " aufzurufen, um die Anzahl der übertragenen Elemente zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="fe7b7-108">The \[[**string**](/windows/desktop/Midl/string)\] attribute directs the stub to call **strlen** to determine the number of transmitted elements.</span></span>

<span data-ttu-id="fe7b7-109">Der Client ordnet den gesamten Arbeitsspeicher vor dem-Rückruf zu:</span><span class="sxs-lookup"><span data-stu-id="fe7b7-109">The client allocates all memory before the call as:</span></span>

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

<span data-ttu-id="fe7b7-110">Beachten Sie, dass die Funktion analysieren nicht mehr die Länge der Rückgabe Zeichenfolge berechnen muss, wie dies im Beispiel für eine gezählte Zeichenfolge geschehen ist, in dem das **\[ Zeichen \]** folgen Attribut nicht verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fe7b7-110">Note that the Analyze function no longer must calculate the length of the return string as it did in the counted-string example where the **\[string\]** attribute was not used.</span></span> <span data-ttu-id="fe7b7-111">Die stubzeichen berechnen nun die Länge wie gezeigt:</span><span class="sxs-lookup"><span data-stu-id="fe7b7-111">Now the stubs calculate the length as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 