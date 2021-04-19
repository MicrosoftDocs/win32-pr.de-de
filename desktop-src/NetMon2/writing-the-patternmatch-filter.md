---
description: Der Filter für die Muster Übereinstimmung benachrichtigt den Treiber, dass Frames mit einem bestimmten Muster an einem bestimmten Offset akzeptiert werden.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Schreiben des patternmatch-Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372992"
---
# <a name="writing-the-patternmatch-filter"></a><span data-ttu-id="37741-103">Schreiben des patternmatch-Filters</span><span class="sxs-lookup"><span data-stu-id="37741-103">Writing the PATTERNMATCH Filter</span></span>

<span data-ttu-id="37741-104">Der Filter für die Muster Übereinstimmung benachrichtigt den Treiber, dass Frames mit einem bestimmten Muster an einem bestimmten Offset akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="37741-104">The pattern match filter notifies the driver to accept frames that have a specific pattern at a specific offset.</span></span> <span data-ttu-id="37741-105">Sie können maximal vier ausführliche Muster Übereinstimmungen angeben, die in logischen and-oder or-Anweisungen für die Auswertung Netzwerkmonitor Treibers kombiniert werden können.</span><span class="sxs-lookup"><span data-stu-id="37741-105">You can specify a maximum of four detailed pattern matches, which can be combined in logical AND or OR statements for Network Monitor driver evaluation.</span></span>

<span data-ttu-id="37741-106">Verwenden Sie die folgenden Netzwerkmonitor Strukturen, um Muster Übereinstimmungen zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="37741-106">To implement pattern matches, use the following Network Monitor structures:</span></span>

-   [<span data-ttu-id="37741-107">**Begriff**</span><span class="sxs-lookup"><span data-stu-id="37741-107">**EXPRESSION**</span></span>](expression.md)
-   [<span data-ttu-id="37741-108">**Andexp**</span><span class="sxs-lookup"><span data-stu-id="37741-108">**ANDEXP**</span></span>](andexp.md)
-   [<span data-ttu-id="37741-109">**Patternmatch**</span><span class="sxs-lookup"><span data-stu-id="37741-109">**PATTERNMATCH**</span></span>](patternmatch.md)

<span data-ttu-id="37741-110">Um eine- **oder** -Anweisung auszuwerten, kombinieren Sie zwei bis vier Muster mit einer [**andexp**](andexp.md) -Struktur (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3).</span><span class="sxs-lookup"><span data-stu-id="37741-110">To evaluate an **OR** statement, combine two to four pattern matches an [**ANDEXP**](andexp.md) structure (PatternMatch1 \|\| PatternMatch2 \|\| PatternMatch3).</span></span> <span data-ttu-id="37741-111">Um eine-Anweisung und eine-Anweisung auszuwerten, kombinieren Sie eine zu vier **andexp** -Strukturen und eine [**Ausdrucks**](expression.md) Struktur (AndExp1 && AndExp2).</span><span class="sxs-lookup"><span data-stu-id="37741-111">To evaluate an AND statement, combine one to four **ANDEXP** structures and an [**EXPRESSION**](expression.md) structure (AndExp1 && AndExp2).</span></span>

## <a name="pattern-match-definitions"></a><span data-ttu-id="37741-112">Muster Übereinstimmungs Definitionen</span><span class="sxs-lookup"><span data-stu-id="37741-112">Pattern Match Definitions</span></span>

<span data-ttu-id="37741-113">Eine einzelne Muster Übereinstimmung wird durch die [**patternmatch**](patternmatch.md) -Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="37741-113">A single pattern match is defined by the [**PATTERNMATCH**](patternmatch.md) structure.</span></span> <span data-ttu-id="37741-114">Eine individuelle Übereinstimmung kann auf zwei Arten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="37741-114">An individual match can operate in one of two ways.</span></span>

<span data-ttu-id="37741-115">Normalerweise nimmt der Treiber den Offset auf (der auf der Basis von Frame, Offset-Basis in Bezug auf das \_ \_ \_ effektive Protokoll, die Offset-Basis in Bezug auf \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ IPX oder \_ die Offset Basis \_ \_ in Bezug auf die \_ IP-Adresse sein kann) und beginnt mit der Zählung.</span><span class="sxs-lookup"><span data-stu-id="37741-115">Normally, the driver will take the offset basis (which can be OFFSET\_BASIS\_RELATIVE\_TO\_FRAME, OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL, OFFSET\_BASIS\_RELATIVE\_TO\_IPX, or OFFSET\_BASIS\_RELATIVE\_TO\_IP) and start counting there.</span></span> <span data-ttu-id="37741-116">Der Treiber zählt Offset Bytes von dort und passt dann die gefundenen Daten mit den ersten Längen Bytes in **patterntomatch** an.</span><span class="sxs-lookup"><span data-stu-id="37741-116">The driver will count offset bytes from there and then match the data it finds with the first length bytes in **PatternToMatch**.</span></span> <span data-ttu-id="37741-117">Wenn Sie identisch sind und die Übereinstimmungs \_ Kennzeichen \_ \_ nicht-Flag nicht festgelegt ist, wird dieses Muster weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="37741-117">If they are the same, and the PATTERN\_MATCH\_FLAGS\_NOT flag is not set, then this pattern passes.</span></span> <span data-ttu-id="37741-118">Wenn Sie unterschiedlich sind und die Übereinstimmungs Flags für Muster \_ \_ \_ nicht festgelegt wurden, wird das Muster weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="37741-118">If they are different and the PATTERN\_MATCH\_FLAGS\_NOT has been set, the pattern passes.</span></span> <span data-ttu-id="37741-119">Andernfalls schlägt dieses Muster fehl.</span><span class="sxs-lookup"><span data-stu-id="37741-119">Otherwise this pattern fails.</span></span>

<span data-ttu-id="37741-120">Oder:</span><span class="sxs-lookup"><span data-stu-id="37741-120">Or:</span></span>

<span data-ttu-id="37741-121">Wenn das angegebene Flag für das Übereinstimmungs Kennzeichen des Musters \_ \_ festgelegt \_ \_ ist und die Basis auf den Wert "Offset" \_ \_ relativ \_ zu \_ IPX oder "Offset" \_ relativ zu IP festgelegt ist \_ \_ \_ , ist der Vergleich komplexer.</span><span class="sxs-lookup"><span data-stu-id="37741-121">If the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag is set, and the basis is set to OFFSET\_BASIS\_RELATIVE\_TO\_IPX or OFFSET\_BASIS\_RELATIVE\_TO\_IP, the comparison is more complex.</span></span> <span data-ttu-id="37741-122">Zuerst stellt der Treiber sicher, dass das Protokoll für die Offset Basis vorhanden ist, dann überprüft der Treiber, ob der angegebene Port mit dem Port im Frame übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="37741-122">First, the driver ensures that the offset basis protocol is there, then the driver verifies that the specified port matches the port in the frame.</span></span> <span data-ttu-id="37741-123">Schließlich stellt der Treiber sicher, dass der **patterntomatch** -Member wie zuvor übereinstimmt, mit der Ausnahme, dass der Offset vom Ende von IP oder IPX abweicht.</span><span class="sxs-lookup"><span data-stu-id="37741-123">Finally the driver ensures that the **PatternToMatch** member matches as before, with the exception that the offset is from the end of IP or IPX.</span></span> <span data-ttu-id="37741-124">Beachten Sie Folgendes: Wenn es sich bei der Basis nicht um eine dieser beiden handelt, wird das Flag für den Übereinstimmungs Kennzeichen \_ \_ \_ \_ -Port festgelegt, und das Muster wird wie oben ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="37741-124">Note that if the basis is not one of these two, then the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag will be ignored, and the pattern will be evaluated as above.</span></span>

<span data-ttu-id="37741-125">Zum Auswerten einer einzelnen Muster Übereinstimmung muss eine [**Ausdrucks**](expression.md) Struktur einen " **andexp** "-Member aufweisen, der eine einzelne Muster Übereinstimmung enthält.</span><span class="sxs-lookup"><span data-stu-id="37741-125">To evaluate a single pattern match, an [**EXPRESSION**](expression.md) structure must have one **AndExp** member containing a single pattern match.</span></span>

<span data-ttu-id="37741-126">Das Erstellen des Muster Übereinstimmungs Filters umfasst das Erstellen von [**patternmatch**](patternmatch.md) -Strukturen und das logische kombinieren mit den Strukturen [**Expression**](expression.md) und [**andexp**](andexp.md) .</span><span class="sxs-lookup"><span data-stu-id="37741-126">Building the pattern match filter involves creating [**PATTERNMATCH**](patternmatch.md) structures and logically combining them with [**EXPRESSION**](expression.md) and [**ANDEXP**](andexp.md) structures.</span></span>

<span data-ttu-id="37741-127">**So schreiben Sie einen patternmatch-Filter**</span><span class="sxs-lookup"><span data-stu-id="37741-127">**To write a PATTERNMATCH filter**</span></span>

1.  <span data-ttu-id="37741-128">Füllen Sie in der [**andexp**](andexp.md) -Struktur das Array mit Muster Übereinstimmungen auf.</span><span class="sxs-lookup"><span data-stu-id="37741-128">In the [**ANDEXP**](andexp.md) structure, populate the array with pattern matches.</span></span>
2.  <span data-ttu-id="37741-129">Füllt die [**Ausdrucks**](expression.md) Struktur mit einem Array von **andexp** -Membern auf.</span><span class="sxs-lookup"><span data-stu-id="37741-129">Populate the [**EXPRESSION**](expression.md) structure with an array of **AndExp** members.</span></span>
3.  <span data-ttu-id="37741-130">Die Summe von vier Muster Übereinstimmungen für den Erfassungs Filter darf nicht überschritten werden.</span><span class="sxs-lookup"><span data-stu-id="37741-130">Do not exceed a total of four pattern matches for the capture filter.</span></span>
4.  <span data-ttu-id="37741-131">Wählen Sie in der [**patternmatch**](patternmatch.md) -Struktur einen flagtyp aus.</span><span class="sxs-lookup"><span data-stu-id="37741-131">In the [**PATTERNMATCH**](patternmatch.md) structure, select a flag type.</span></span>
5.  <span data-ttu-id="37741-132">Wählen Sie einen Offset aus.</span><span class="sxs-lookup"><span data-stu-id="37741-132">Select an offset basis.</span></span>
6.  <span data-ttu-id="37741-133">Enumerieren Sie einen Portwert.</span><span class="sxs-lookup"><span data-stu-id="37741-133">Enumerate a port value.</span></span>
7.  <span data-ttu-id="37741-134">Legen Sie den Offset Wert fest.</span><span class="sxs-lookup"><span data-stu-id="37741-134">Define offset value.</span></span>
8.  <span data-ttu-id="37741-135">Definieren Sie die Muster Länge.</span><span class="sxs-lookup"><span data-stu-id="37741-135">Define the pattern length.</span></span>
9.  <span data-ttu-id="37741-136">Listet den Pattern-Wert auf.</span><span class="sxs-lookup"><span data-stu-id="37741-136">Enumerate the pattern value.</span></span>

## <a name="patternmatch-examples"></a><span data-ttu-id="37741-137">Patternmatch-Beispiele</span><span class="sxs-lookup"><span data-stu-id="37741-137">PATTERNMATCH Examples</span></span>

<span data-ttu-id="37741-138">Dieser Frame stellt einen Standard Offset dar.</span><span class="sxs-lookup"><span data-stu-id="37741-138">This frame represents a standard offset.</span></span>

![Standard Offset Rahmen](images/offs-pat.png)

<span data-ttu-id="37741-140">Das Code Fragment wird wie folgt implementiert:</span><span class="sxs-lookup"><span data-stu-id="37741-140">The code fragment is implemented as:</span></span>

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

<span data-ttu-id="37741-141">Dieser Frame stellt einen Port spezifischen Offset (gegen IPX) dar.</span><span class="sxs-lookup"><span data-stu-id="37741-141">This frame depicts a port-specified offset (against IPX).</span></span>

![vom Port angegebener Offset Rahmen](images/stan-pat.png)

<span data-ttu-id="37741-143">Der Beispielcode wird wie folgt implementiert:</span><span class="sxs-lookup"><span data-stu-id="37741-143">The example code is implemented as:</span></span>

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



