---
title: /cstruct_out Schalter
description: Der Schalter/cstruct_out ändert die C-Definition einer COM-Schnittstelle, die Strukturen zurückgibt, die mit der von a C++ Implementierer bereitgestellten ABI zu vergleichen sind.
keywords:
- /cstruct_out-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 535e1630046b424493e2211c29248c18bf1ed798
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859361"
---
# <a name="cstruct_out-switch"></a><span data-ttu-id="67110-104">/cstruct \_ out-Schalter</span><span class="sxs-lookup"><span data-stu-id="67110-104">/cstruct\_out switch</span></span>

<span data-ttu-id="67110-105">Dieser Schalter ändert die C-Definition einer COM-Schnittstelle, die Strukturen zurückgibt, die mit der von a C++ Implementierer bereitgestellten ABI identisch sind.</span><span class="sxs-lookup"><span data-stu-id="67110-105">This switch modifies the C definition of a COM interface which returns structures to match the ABI a C++ implementer would provide.</span></span>

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a><span data-ttu-id="67110-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="67110-106">Switch Options</span></span>

<span data-ttu-id="67110-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="67110-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="67110-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67110-108">Remarks</span></span>

<span data-ttu-id="67110-109">Einige Schnittstellendefinitionen (insbesondere in `d3d12.idl` ) enthalten `__stdcall` Methoden, die Strukturen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="67110-109">Some interface definitions (notably those in `d3d12.idl`) contain `__stdcall` methods that return structures.</span></span> <span data-ttu-id="67110-110">C und C++ ABIS from MSVC unterscheiden sich in der Implementierung solcher Funktionen:</span><span class="sxs-lookup"><span data-stu-id="67110-110">The C and C++ ABIs from MSVC differ in how they implement such functions:</span></span>

* <span data-ttu-id="67110-111">C behandelt Sie als einfache Funktionen, die einen verborgenen `this` Zeiger als ersten Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="67110-111">C treats them as plain functions that take a hidden `this` pointer as the first parameter.</span></span> <span data-ttu-id="67110-112">Der Compiler wendet eine kleine Strukturoptimierung an, die Strukturen zulässt, die kleiner sind als 8 Bytes (oder größer, wenn alle Werte Gleit Komma sind), die in Registern zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="67110-112">The complier applies a small struct optimization that allows structs smaller than 8 bytes (or larger if all values are floating point) to be returned in registers.</span></span> <span data-ttu-id="67110-113">Nur größere Strukturen werden herauf gestuft, um einen ausgeblendeten und vom Aufrufer zugewiesenen Rückgabewert zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="67110-113">Only larger structures are promoted to use a hidden parameter and caller-allocated return value.</span></span>
* <span data-ttu-id="67110-114">C++ behandelt diese als Element Funktionen.</span><span class="sxs-lookup"><span data-stu-id="67110-114">C++ treats them as member functions.</span></span> <span data-ttu-id="67110-115">Der Compiler führt dies *immer* durch Einfügen eines ausgeblendeten Parameters (einen Zeiger auf einen vom Aufrufer zugeordneten Rückgabewert) als zweiten Parameter hinter dem- `this` Zeiger.</span><span class="sxs-lookup"><span data-stu-id="67110-115">The compiler *always* does so by inserting a hidden parameter (a pointer to a caller-allocated return value) as the second parameter, after the `this` pointer.</span></span> <span data-ttu-id="67110-116">Außerdem wird derselbe Zeiger zurückgegeben wie der Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="67110-116">It also returns that same pointer as its return value.</span></span>

<span data-ttu-id="67110-117">Dieser Schalter zwingt die c-Definition der Schnittstellen im resultierenden Header dazu, dass der Implementierer C++ verwendet hat, und dass der c-Code stattdessen explizit die C++ ABI verwenden sollte.</span><span class="sxs-lookup"><span data-stu-id="67110-117">This switch forces the C definition of interfaces in the resulting header to assume that the implementer was using C++, and that the C code should instead explicitly use the C++ ABI.</span></span> <span data-ttu-id="67110-118">Dies impliziert, dass die Funktion einen ausgeblendeten Parameter für den Rückgabewert Zeiger enthält und diesen Zeiger anstelle der Struktur direkt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="67110-118">This implies that the function includes a hidden parameter for the return value pointer and returns that pointer instead of the structure directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="67110-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67110-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67110-120">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="67110-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>
