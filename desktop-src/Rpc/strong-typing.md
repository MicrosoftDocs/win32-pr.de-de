---
title: Starke Typisierung
description: C ist eine schwach typisierte Sprache, d. h. der Compiler lässt Vorgänge wie Zuweisung und Vergleich zwischen Variablen verschiedener Typen zu.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Dateneingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948058"
---
# <a name="strong-typing"></a><span data-ttu-id="a78cc-104">Starke Typisierung</span><span class="sxs-lookup"><span data-stu-id="a78cc-104">Strong Typing</span></span>

<span data-ttu-id="a78cc-105">C ist eine schwach typisierte Sprache, d. h. der Compiler lässt Vorgänge wie Zuweisung und Vergleich zwischen Variablen verschiedener Typen zu.</span><span class="sxs-lookup"><span data-stu-id="a78cc-105">C is a weakly typed language, that is, the compiler allows operations such as assignment and comparison among variables of different types.</span></span> <span data-ttu-id="a78cc-106">Beispielsweise lässt C zu, dass der Wert einer Variablen in einen anderen Typ umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="a78cc-106">For example, C allows the value of a variable to be cast to another type.</span></span> <span data-ttu-id="a78cc-107">Die Möglichkeit, Variablen unterschiedlicher Typen im gleichen Ausdruck zu verwenden, fördert Flexibilität und Effizienz.</span><span class="sxs-lookup"><span data-stu-id="a78cc-107">The ability to use variables of different types in the same expression promotes flexibility as well as efficiency.</span></span>

<span data-ttu-id="a78cc-108">Eine stark typisierte Sprache erzwingt Einschränkungen für Vorgänge zwischen Variablen unterschiedlicher Typen.</span><span class="sxs-lookup"><span data-stu-id="a78cc-108">A strongly typed language imposes restrictions on operations among variables of different types.</span></span> <span data-ttu-id="a78cc-109">In diesen Fällen gibt der Compiler einen Fehler aus, der den Vorgang untersagt.</span><span class="sxs-lookup"><span data-stu-id="a78cc-109">In those cases, the compiler issues an error prohibiting the operation.</span></span> <span data-ttu-id="a78cc-110">Diese strengen Richtlinien bezüglich der Datentypen sind darauf ausgelegt, potenzielle Fehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a78cc-110">These strict guidelines regarding data types are designed to avoid potential errors.</span></span>

<span data-ttu-id="a78cc-111">Die Schwierigkeit bei der Verwendung einer schwach typisierten Sprache wie z. b. C für Remote Prozedur Aufrufe besteht darin, dass verteilte Anwendungen auf verschiedenen Computern mit unterschiedlichen C-Compilern und verschiedenen Architekturen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="a78cc-111">The difficulty with using a weakly typed language such as C for remote procedure calls is that distributed applications can run on several different computers with different C compilers and different architectures.</span></span> <span data-ttu-id="a78cc-112">Wenn eine Anwendung nur auf einem Computer ausgeführt wird, müssen Sie sich nicht mit dem internen Datenformat beschäftigen, da die Daten konsistent verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a78cc-112">When an application runs on only one computer, you don't have to be concerned with the internal data format because the data is handled in a consistent manner.</span></span> <span data-ttu-id="a78cc-113">In einer verteilten Computerumgebung können von verschiedenen Computern jedoch unterschiedliche Definitionen für die Basis Datentypen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a78cc-113">However, in a distributed computing environment, different computers can use different definitions for their base data types.</span></span> <span data-ttu-id="a78cc-114">Einige Computer definieren z. b. den **int** -Typ, sodass die interne Darstellung 16 Bits beträgt, während andere Computer 32 Bits verwenden.</span><span class="sxs-lookup"><span data-stu-id="a78cc-114">For example, some computers define the **int** type, so its internal representation is 16 bits, while other computers use 32 bits.</span></span> <span data-ttu-id="a78cc-115">Eine Computerarchitektur, die als "Little Endian" bezeichnet wird, weist der niedrigsten Speicheradresse und dem signifikantesten der höchsten Adresse das am wenigsten signifikante Byte zu.</span><span class="sxs-lookup"><span data-stu-id="a78cc-115">One computer architecture, known as "little endian," assigns the least significant byte of data to the lowest memory address and the most significant byte to the highest address.</span></span> <span data-ttu-id="a78cc-116">Eine andere Architektur, die als "Big Endian" bezeichnet wird, weist das am wenigsten signifikante Byte der höchsten Speicheradresse zu, die diesen Daten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a78cc-116">Another architecture, known as "big endian," assigns the least significant byte to the highest memory address associated with that data.</span></span>

<span data-ttu-id="a78cc-117">Remote Prozedur Aufrufe erfordern eine strikte Kontrolle über Parametertypen.</span><span class="sxs-lookup"><span data-stu-id="a78cc-117">Remote procedure calls require strict control over parameter types.</span></span> <span data-ttu-id="a78cc-118">Um die Datenübertragung und-Konvertierung über das Netzwerk zu verarbeiten, erzwingt die Mittelwert Einschränkung Typeinschränkungen für Daten, die über das Netzwerk übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="a78cc-118">To handle data transmission and conversion over the network, MIDL strictly enforces type restrictions for data transferred over the network.</span></span> <span data-ttu-id="a78cc-119">Aus diesem Grund enthält die Mittel Menge eine Reihe von klar definierten [Basis Typen](base-types.md).</span><span class="sxs-lookup"><span data-stu-id="a78cc-119">For this reason, MIDL includes a set of well-defined [base types](base-types.md).</span></span> <span data-ttu-id="a78cc-120">Die Mittel Menge erzwingt eine starke Typisierung durch die Verwendung von Schlüsselwörtern, die die Größe und den Typ der Daten eindeutig definieren.</span><span class="sxs-lookup"><span data-stu-id="a78cc-120">MIDL enforces strong typing by mandating the use of keywords that unambiguously define the size and type of data.</span></span> <span data-ttu-id="a78cc-121">Die offensichtlichste Auswirkung der starken Typisierung besteht darin, dass die Mittel l keine Variablen vom Typ " **void \***" zulässt.</span><span class="sxs-lookup"><span data-stu-id="a78cc-121">The most visible effect of strong typing is that MIDL does not allow variables of the type **void \***.</span></span>

<span data-ttu-id="a78cc-122">In den folgenden Themen werden in diesem Abschnitt die Funktionen der mittleren Sprache erläutert, die eine starke Dateneingabe erzwingen:</span><span class="sxs-lookup"><span data-stu-id="a78cc-122">In the following topics, this section discusses the MIDL language features that enforce strong data typing:</span></span>

-   [<span data-ttu-id="a78cc-123">Basis Typen</span><span class="sxs-lookup"><span data-stu-id="a78cc-123">Base Types</span></span>](base-types.md)
-   [<span data-ttu-id="a78cc-124">Typen mit und ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="a78cc-124">Signed and Unsigned Types</span></span>](signed-and-unsigned-types.md)
-   [<span data-ttu-id="a78cc-125">Breit Zeichen Typen</span><span class="sxs-lookup"><span data-stu-id="a78cc-125">Wide-Character Types</span></span>](wide-character-types.md)
-   [<span data-ttu-id="a78cc-126">Strukturen</span><span class="sxs-lookup"><span data-stu-id="a78cc-126">Structures</span></span>](structures.md)
-   [<span data-ttu-id="a78cc-127">Unions</span><span class="sxs-lookup"><span data-stu-id="a78cc-127">Unions</span></span>](unions.md)
-   [<span data-ttu-id="a78cc-128">Enumerierte Typen</span><span class="sxs-lookup"><span data-stu-id="a78cc-128">Enumerated Types</span></span>](enumerated-types.md)
-   [<span data-ttu-id="a78cc-129">Arrays</span><span class="sxs-lookup"><span data-stu-id="a78cc-129">Arrays</span></span>](arrays.md)
-   [<span data-ttu-id="a78cc-130">Funktionsattribute</span><span class="sxs-lookup"><span data-stu-id="a78cc-130">Function Attributes</span></span>](function-attributes.md)
-   [<span data-ttu-id="a78cc-131">Feldattribute</span><span class="sxs-lookup"><span data-stu-id="a78cc-131">Field Attributes</span></span>](field-attributes.md)
-   [<span data-ttu-id="a78cc-132">Drei Zeiger Typen</span><span class="sxs-lookup"><span data-stu-id="a78cc-132">Three Pointer Types</span></span>](three-pointer-types.md)
-   [<span data-ttu-id="a78cc-133">Typattribute</span><span class="sxs-lookup"><span data-stu-id="a78cc-133">Type Attributes</span></span>](type-attributes.md)

 

 




