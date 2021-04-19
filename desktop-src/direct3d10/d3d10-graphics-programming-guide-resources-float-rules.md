---
description: Direct3D 10 unterstützt mehrere verschiedene Gleit Komma Darstellungen. Alle Gleit Komma Berechnungen arbeiten unter einer definierten Teilmenge des IEEE 754 32-Bit-Gleit Komma Verhaltens mit einfacher Genauigkeit.
ms.assetid: 57221d13-8993-4db3-b1a0-88bdcf6f0167
title: Ffloating-Point-Regeln (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6909d037b11f9098bb3e0dbad0f1846b79b513e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344828"
---
# <a name="floating-point-rules-direct3d-10"></a><span data-ttu-id="1a337-104">Gleit Komma Regeln (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1a337-104">Floating-point rules (Direct3D 10)</span></span>

<span data-ttu-id="1a337-105">Direct3D 10 unterstützt mehrere verschiedene Gleit Komma Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="1a337-105">Direct3D 10 supports several different floating-point representations.</span></span> <span data-ttu-id="1a337-106">Alle Gleit Komma Berechnungen arbeiten unter einer definierten Teilmenge des IEEE 754 32-Bit-Gleit Komma Verhaltens mit einfacher Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="1a337-106">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point behavior.</span></span>

-   [<span data-ttu-id="1a337-107">32-Bit-Floating-Point Regeln</span><span class="sxs-lookup"><span data-stu-id="1a337-107">32-bit Floating-Point Rules</span></span>](#32-bit-floating-point-rules)
    -   [<span data-ttu-id="1a337-108">IEEE-754-Regeln wurden berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="1a337-108">Honored IEEE-754 Rules</span></span>](#honored-ieee-754-rules)
    -   [<span data-ttu-id="1a337-109">Abweichungen oder zusätzliche Anforderungen von IEEE-754-Regeln</span><span class="sxs-lookup"><span data-stu-id="1a337-109">Deviations or Additional Requirements from IEEE-754 Rules</span></span>](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [<span data-ttu-id="1a337-110">Regeln für 16-Bit-Floating-Point</span><span class="sxs-lookup"><span data-stu-id="1a337-110">16-bit Floating-Point Rules</span></span>](#16-bit-floating-point-rules)
-   [<span data-ttu-id="1a337-111">11-Bit-und 10-Bit-Floating-Point Regeln</span><span class="sxs-lookup"><span data-stu-id="1a337-111">11-bit and 10-bit Floating-Point Rules</span></span>](#11-bit-and-10-bit-floating-point-rules)
-   [<span data-ttu-id="1a337-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a337-112">Related topics</span></span>](#related-topics)

## <a name="32-bit-floating-point-rules"></a><span data-ttu-id="1a337-113">32-Bit-Floating-Point Regeln</span><span class="sxs-lookup"><span data-stu-id="1a337-113">32-bit Floating-Point Rules</span></span>

<span data-ttu-id="1a337-114">Es gibt zwei Sätze von Regeln: die, die IEEE-754 entsprechen, und die Regeln, die vom Standard abweichen.</span><span class="sxs-lookup"><span data-stu-id="1a337-114">There are two sets of rules: those that conform to IEEE-754, and those that deviate from the standard.</span></span>

### <a name="honored-ieee-754-rules"></a><span data-ttu-id="1a337-115">IEEE-754-Regeln wurden berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="1a337-115">Honored IEEE-754 Rules</span></span>

<span data-ttu-id="1a337-116">Einige dieser Regeln stellen eine einzelne Option dar, bei der IEEE-754 Optionen bietet.</span><span class="sxs-lookup"><span data-stu-id="1a337-116">Some of these rules are a single option where IEEE-754 offers choices.</span></span>

-   <span data-ttu-id="1a337-117">Division durch 0 erzeugt +/-inf, mit Ausnahme von 0/0, was zu Nan führt.</span><span class="sxs-lookup"><span data-stu-id="1a337-117">Divide by 0 produces +/- INF, except 0/0 which results in NaN.</span></span>
-   <span data-ttu-id="1a337-118">das Protokoll von (+/-) 0 erzeugt-inf.</span><span class="sxs-lookup"><span data-stu-id="1a337-118">log of (+/-) 0 produces -INF.</span></span> <span data-ttu-id="1a337-119">das Protokoll eines negativen Werts (mit Ausnahme von-0) erzeugt Nan.</span><span class="sxs-lookup"><span data-stu-id="1a337-119">log of a negative value (other than -0) produces NaN.</span></span>
-   <span data-ttu-id="1a337-120">Die gegenseitige Quadratwurzel (RSQ) oder die Quadratwurzel (sqrt) einer negativen Zahl erzeugt Nan.</span><span class="sxs-lookup"><span data-stu-id="1a337-120">Reciprocal square root (rsq) or square root (sqrt) of a negative number produces NaN.</span></span> <span data-ttu-id="1a337-121">Die Ausnahme ist-0; SQRT (-0) erzeugt-0, und RSQ (-0) erzeugt-inf.</span><span class="sxs-lookup"><span data-stu-id="1a337-121">The exception is -0; sqrt(-0) produces -0, and rsq(-0) produces -INF.</span></span>
-   <span data-ttu-id="1a337-122">INF-INF = Nan</span><span class="sxs-lookup"><span data-stu-id="1a337-122">INF - INF = NaN</span></span>
-   <span data-ttu-id="1a337-123">(+/-) Inf/(+/-) INF = Nan</span><span class="sxs-lookup"><span data-stu-id="1a337-123">(+/-)INF / (+/-)INF = NaN</span></span>
-   <span data-ttu-id="1a337-124">(+/-) INF \* 0 = Nan</span><span class="sxs-lookup"><span data-stu-id="1a337-124">(+/-)INF \* 0 = NaN</span></span>
-   <span data-ttu-id="1a337-125">Nan (beliebiger OP) beliebiger Wert = NaN</span><span class="sxs-lookup"><span data-stu-id="1a337-125">NaN (any OP) any-value = NaN</span></span>
-   <span data-ttu-id="1a337-126">Die Vergleiche EQ, gt, ge, lt und Le, wenn einer oder beide Operanden NaN ist, wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1a337-126">The comparisons EQ, GT, GE, LT, and LE, when either or both operands is NaN returns **FALSE**.</span></span>
-   <span data-ttu-id="1a337-127">Vergleiche ignorieren das Vorzeichen von 0 (also + 0 ist 0).</span><span class="sxs-lookup"><span data-stu-id="1a337-127">Comparisons ignore the sign of 0 (so +0 equals -0).</span></span>
-   <span data-ttu-id="1a337-128">Der Vergleichs-ne, wenn einer oder beide Operanden NaN ist, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1a337-128">The comparison NE, when either or both operands is NaN returns **TRUE**.</span></span>
-   <span data-ttu-id="1a337-129">Vergleiche eines beliebigen nicht-NaN-Werts mit +/-INF geben das korrekte Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="1a337-129">Comparisons of any non-NaN value against +/- INF return the correct result.</span></span>

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a><span data-ttu-id="1a337-130">Abweichungen oder zusätzliche Anforderungen von IEEE-754-Regeln</span><span class="sxs-lookup"><span data-stu-id="1a337-130">Deviations or Additional Requirements from IEEE-754 Rules</span></span>

-   <span data-ttu-id="1a337-131">IEEE-754 erfordert Gleit Komma Vorgänge, um ein Ergebnis zu erhalten, das den nächstgelegenen darstellbaren Wert zu einem unendlich präzisen Ergebnis ist, das auch als "Round-to-Next-even" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1a337-131">IEEE-754 requires floating-point operations to produce a result that is the nearest representable value to an infinitely-precise result, known as round-to-nearest-even.</span></span> <span data-ttu-id="1a337-132">Direct3D 10 definiert jedoch eine lockere Anforderung: 32-Bit-Gleit Komma Operationen führen zu einem Ergebnis, das sich innerhalb einer Einheits Last Stelle (1 ULP) des unendlich präzisen Ergebnisses befindet.</span><span class="sxs-lookup"><span data-stu-id="1a337-132">Direct3D 10, however, defines a looser requirement: 32-bit floating-point operations produce a result that is within one unit-last-place (1 ULP) of the infinitely-precise result.</span></span> <span data-ttu-id="1a337-133">Dies bedeutet, dass Hardware z. b. die Ergebnisse in 32-Bit Abschneiden darf, anstatt Sie durch eine roundTo-Next-even-Methode auszuführen, da dies zu einem Fehler bei höchstens einer ULP führen würde.</span><span class="sxs-lookup"><span data-stu-id="1a337-133">This means that, for example, hardware is allowed to truncate results to 32-bit rather than perform round-to-nearest-even, as that would result in error of at most one ULP.</span></span>
-   <span data-ttu-id="1a337-134">Es gibt keine Unterstützung für Gleit Komma Ausnahmen, Status Bits oder Traps.</span><span class="sxs-lookup"><span data-stu-id="1a337-134">There is no support for floating-point exceptions, status bits or traps.</span></span>
-   <span data-ttu-id="1a337-135">Denorms werden bei einem Eingabe-und Ausgabewert einer mathematischen Gleit Komma Operation in die Signierung NULL geleert.</span><span class="sxs-lookup"><span data-stu-id="1a337-135">Denorms are flushed to sign-preserved zero on input and output of any floating-point mathematical operation.</span></span> <span data-ttu-id="1a337-136">Ausnahmen werden für alle e/a-oder Daten Verschiebungs Vorgänge ausgelöst, die die Daten nicht verändern.</span><span class="sxs-lookup"><span data-stu-id="1a337-136">Exceptions are made for any I/O or data movement operation that does not manipulate the data.</span></span>
-   <span data-ttu-id="1a337-137">Zustände, die Gleit Komma Werte enthalten, wie z. b. Viewport mintiefe/maxtiefe, BorderColor-Werte usw., werden möglicherweise als denorm-Werte angegeben und können vor der Verwendung durch die Hardware geleert werden.</span><span class="sxs-lookup"><span data-stu-id="1a337-137">States that contain floating-point values, such as Viewport MinDepth/MaxDepth, BorderColor values etc., may be provided as denorm values and may or may not be flushed before use by the hardware.</span></span>
-   <span data-ttu-id="1a337-138">Bei minimalen oder maximalen Vorgängen werden denorms zum Vergleichen geleert, das Ergebnis kann jedoch nicht mit denorm geleert werden.</span><span class="sxs-lookup"><span data-stu-id="1a337-138">Min or max operations flush denorms for comparison, but the result may or may not be denorm flushed.</span></span>
-   <span data-ttu-id="1a337-139">Die Nan-Eingabe für einen Vorgang erzeugt immer Nan in der Ausgabe, aber das genaue Bitmuster von Nan muss nicht gleich bleiben (es sei denn, der Vorgang ist eine unformatierte Move-Anweisung, die Daten überhaupt nicht ändert.)</span><span class="sxs-lookup"><span data-stu-id="1a337-139">NaN input to an operation always produces NaN on output, however the exact bit pattern of the NaN is not required to stay the same (unless the operation is a raw move instruction - which does not alter data at all.)</span></span>
-   <span data-ttu-id="1a337-140">Minimale oder maximale Vorgänge, für die nur ein Operand NaN ist, geben den anderen Operanden als Ergebnis zurück (im Gegensatz zu den obigen Vergleichs Regeln).</span><span class="sxs-lookup"><span data-stu-id="1a337-140">Min or max operations for which only one operand is NaN return the other operand as the result (contrary to comparison rules above).</span></span> <span data-ttu-id="1a337-141">Dies ist eine neue IEEE-Regel (IEEE 754r), die in Direct3D 10 erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1a337-141">This is a new IEEE rule (IEEE 754R), required in Direct3D 10.</span></span>
-   <span data-ttu-id="1a337-142">Eine weitere neue IEEE 754r-Regel ist, dass min (-0, + 0) = = min (+ 0,-0) = =-0 und Max (-0, + 0) = = Max (+ 0,-0) = = + 0, die das Vorzeichen beachten, im Gegensatz zu den Vergleichs Regeln für signed Zero (oben angegeben).</span><span class="sxs-lookup"><span data-stu-id="1a337-142">Another new IEEE 754R rule is that min(-0,+0) == min(+0,-0) == -0, and max(-0,+0) == max(+0,-0) == +0, which honor the sign, in contrast to the comparison rules for signed zero (stated above).</span></span> <span data-ttu-id="1a337-143">Direct3D 10 empfiehlt das IEEE 754r-Verhalten, wird jedoch nicht erzwungen. Es ist zulässig, dass das Ergebnis des Vergleichs von Nullen von der Reihenfolge der Parameter abhängig ist. dabei wird ein Vergleich verwendet, bei dem die Vorzeichen ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="1a337-143">Direct3D 10 recommends the IEEE 754R behavior here, but it will not be enforced; it is permissible for the result of comparing zeros to be dependent on the order of parameters, using a comparison that ignores the signs.</span></span>
-   <span data-ttu-id="1a337-144">x \* 1.0 f ergibt immer x (außer denorm geleert).</span><span class="sxs-lookup"><span data-stu-id="1a337-144">x\*1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="1a337-145">x/1.0 f ergibt immer x (außer denorm geleert).</span><span class="sxs-lookup"><span data-stu-id="1a337-145">x/1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="1a337-146">x +/-0,0 f ergibt immer x (außer denorm geleert).</span><span class="sxs-lookup"><span data-stu-id="1a337-146">x +/- 0.0f always results in x (except denorm flushed).</span></span> <span data-ttu-id="1a337-147">Aber-0 + 0 = + 0.</span><span class="sxs-lookup"><span data-stu-id="1a337-147">But -0 + 0 = +0.</span></span>
-   <span data-ttu-id="1a337-148">Beim Durchlaufen von Vorgängen (z. b. Mad, DP3) werden Ergebnisse erzeugt, die nicht weniger genau sind als die schlechtesten mögliche serielle Reihenfolge der Auswertung der nicht geschmolzenen Erweiterung des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1a337-148">Fused operations (such as mad, dp3) produce results that are no less accurate than the worst possible serial ordering of evaluation of the unfused expansion of the operation.</span></span> <span data-ttu-id="1a337-149">Beachten Sie, dass die Definition der ungünstigsten Reihenfolge für die Toleranz keine festgelegte Definition für einen bestimmten Fused-Vorgang ist. Dies hängt von den jeweiligen Werten der Eingaben ab.</span><span class="sxs-lookup"><span data-stu-id="1a337-149">Note that the definition of the worst possible ordering, for the purpose of tolerance, is not a fixed definition for a given fused operation; it depends on the particular values of the inputs.</span></span> <span data-ttu-id="1a337-150">Die einzelnen Schritte in der nicht zugezierten Erweiterung sind jeweils als 1 ULP-Toleranz zulässig (oder für alle Anweisungen Direct3D 10 Aufrufe mit einer weniger Lax-Toleranz als 1 ULP, desto weniger Lax-Toleranz ist zulässig).</span><span class="sxs-lookup"><span data-stu-id="1a337-150">The individual steps in the unfused expansion are each allowed 1 ULP tolerance (or for any instructions Direct3D 10 calls out with a more lax tolerance than 1 ULP, the more lax tolerance is allowed).</span></span>
-   <span data-ttu-id="1a337-151">Bei der durchgeführten Ausführung werden die gleichen Nan-Regeln wie nicht-Fused-Vorgänge befolgt.</span><span class="sxs-lookup"><span data-stu-id="1a337-151">Fused operations adhere to the same NaN rules as non-fused operations.</span></span>
-   <span data-ttu-id="1a337-152">Multiplizieren und Dividieren jedes Betriebs auf der 32-Bit-Gleit Komma Genauigkeit (Genauigkeit zu 1 ULP).</span><span class="sxs-lookup"><span data-stu-id="1a337-152">Multiply and divide each operate at the 32-bit floating-point precision level (accuracy to 1 ULP).</span></span>

## <a name="16-bit-floating-point-rules"></a><span data-ttu-id="1a337-153">Regeln für 16-Bit-Floating-Point</span><span class="sxs-lookup"><span data-stu-id="1a337-153">16-bit Floating-Point Rules</span></span>

<span data-ttu-id="1a337-154">Direct3D 10 unterstützt auch 16-Bit-Darstellungen von Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="1a337-154">Direct3D 10 also supports 16-bit representations of floating-point numbers.</span></span>

<span data-ttu-id="1a337-155">Format:</span><span class="sxs-lookup"><span data-stu-id="1a337-155">Format:</span></span>

-   <span data-ttu-id="1a337-156">1 Signier Bit (e) an der MSB-Bitposition</span><span class="sxs-lookup"><span data-stu-id="1a337-156">1 sign bit (s)in the MSB bit position</span></span>
-   <span data-ttu-id="1a337-157">5 Bits von unparteiischen Exponent (e)</span><span class="sxs-lookup"><span data-stu-id="1a337-157">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="1a337-158">10 Bits des Bruchteils (f) mit einem zusätzlichen ausgeblendeten Bit</span><span class="sxs-lookup"><span data-stu-id="1a337-158">10 bits of fraction (f), with an additional hidden bit</span></span>

<span data-ttu-id="1a337-159">Ein float16-Wert (v) folgt den folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="1a337-159">A float16 value (v) follows the following rules:</span></span>

-   <span data-ttu-id="1a337-160">Wenn e = = 31 und f! = 0 ist, dann ist v unabhängig von s</span><span class="sxs-lookup"><span data-stu-id="1a337-160">if e == 31 and f != 0, then v is NaN regardless of s</span></span>
-   <span data-ttu-id="1a337-161">Wenn e = = 31 und f = = 0, dann v = (-1) s \* unendlich (Vorzeichen unendlich)</span><span class="sxs-lookup"><span data-stu-id="1a337-161">if e == 31 and f == 0, then v = (-1)s\*infinity (signed infinity)</span></span>
-   <span data-ttu-id="1a337-162">Wenn e zwischen 0 und 31 liegt, dann v = (-1) s \* 2 (e-15) \* (1. f)</span><span class="sxs-lookup"><span data-stu-id="1a337-162">if e is between 0 and 31, then v = (-1)s\*2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="1a337-163">Wenn e = = 0 und f! = 0, dann v = (-1) s \* 2 (e-14) \* (0. f) (Denormalisierte Zahlen)</span><span class="sxs-lookup"><span data-stu-id="1a337-163">if e == 0 and f != 0, then v = (-1)s\*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="1a337-164">Wenn e = = 0 und f = = 0, dann v = (-1) s \* 0 (signierte null)</span><span class="sxs-lookup"><span data-stu-id="1a337-164">if e == 0 and f == 0, then v = (-1)s\*0 (signed zero)</span></span>

<span data-ttu-id="1a337-165">32-Bit-Gleit Komma Regeln enthalten auch für 16-Bit-Gleit Komma Zahlen, die für das oben beschriebene bitlayout angepasst sind.</span><span class="sxs-lookup"><span data-stu-id="1a337-165">32-bit floating-point rules also hold for 16-bit floating-point numbers, adjusted for the bit layout described above.</span></span> <span data-ttu-id="1a337-166">Ausnahmen bilden die folgenden Fälle:</span><span class="sxs-lookup"><span data-stu-id="1a337-166">Exceptions to this include:</span></span>

-   <span data-ttu-id="1a337-167">Genauigkeit: bei unfused-Vorgängen für 16-Bit-Gleit Komma Zahlen wird ein Ergebnis erzeugt, bei dem es sich um den nächstgelegenen darstellbaren Wert eines unendlich präzisen Ergebnisses handelt (abgerundet auf den nächstgelegenen Wert, auch pro IEEE-754, auf 16-Bit-Werte angewendet).</span><span class="sxs-lookup"><span data-stu-id="1a337-167">Precision: Unfused operations on 16-bit floating-point numbers produce a result that is the nearest representable value to an infinitely-precise result (round to nearest even, per IEEE-754, applied to 16-bit values).</span></span> <span data-ttu-id="1a337-168">32-Bit-Gleit Komma Regeln entsprechen 1 ULP-Toleranz, 16-Bit-Gleit Komma Regeln entsprechen 0,5 ULP für unfused-Vorgänge und 0,6 ULP für Fused-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="1a337-168">32-bit floating-point rules adhere to 1 ULP tolerance, 16-bit floating-point rules adhere to 0.5 ULP for unfused operations, and 0.6 ULP for fused operations.</span></span>
-   <span data-ttu-id="1a337-169">16-Bit-Gleit Komma Zahlen behalten denorms bei.</span><span class="sxs-lookup"><span data-stu-id="1a337-169">16-bit floating-point numbers preserve denorms.</span></span>

## <a name="11-bit-and-10-bit-floating-point-rules"></a><span data-ttu-id="1a337-170">11-Bit-und 10-Bit-Floating-Point Regeln</span><span class="sxs-lookup"><span data-stu-id="1a337-170">11-bit and 10-bit Floating-Point Rules</span></span>

<span data-ttu-id="1a337-171">Direct3D 10 unterstützt auch 11-Bit-und 10-Bit-Gleit Komma Formate.</span><span class="sxs-lookup"><span data-stu-id="1a337-171">Direct3D 10 also supports 11-bit and 10-bit floating-point formats.</span></span>

<span data-ttu-id="1a337-172">Format:</span><span class="sxs-lookup"><span data-stu-id="1a337-172">Format:</span></span>

-   <span data-ttu-id="1a337-173">Kein Signier Bit</span><span class="sxs-lookup"><span data-stu-id="1a337-173">No sign bit</span></span>
-   <span data-ttu-id="1a337-174">5 Bits von unparteiischen Exponent (e)</span><span class="sxs-lookup"><span data-stu-id="1a337-174">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="1a337-175">6 Bits des Bruchteils (f) für ein 11-Bit-Format, 5 Bits von Bruchteil (f) für ein 10-Bit-Format, mit einem zusätzlichen ausgeblendeten Bit in beiden Fällen.</span><span class="sxs-lookup"><span data-stu-id="1a337-175">6 bits of fraction (f) for an 11-bit format, 5 bits of fraction (f) for a 10-bit format, with an additional hidden bit in either case.</span></span>

<span data-ttu-id="1a337-176">Ein float11/float10-Wert (v) folgt den folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="1a337-176">A float11/float10 value (v) follows the following rules:</span></span>

-   <span data-ttu-id="1a337-177">Wenn e = = 31 und f! = 0 ist, dann ist v Nan.</span><span class="sxs-lookup"><span data-stu-id="1a337-177">if e == 31 and f != 0, then v is NaN</span></span>
-   <span data-ttu-id="1a337-178">Wenn e = = 31 und f = = 0, dann v = + unendlich</span><span class="sxs-lookup"><span data-stu-id="1a337-178">if e == 31 and f == 0, then v = +infinity</span></span>
-   <span data-ttu-id="1a337-179">Wenn e zwischen 0 und 31 liegt, dann v = 2 (e-15) \* (1. f)</span><span class="sxs-lookup"><span data-stu-id="1a337-179">if e is between 0 and 31, then v = 2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="1a337-180">Wenn e = = 0 und f! = 0, dann v = \* 2 (e-14) \* (0. f) (Denormalisierte Zahlen)</span><span class="sxs-lookup"><span data-stu-id="1a337-180">if e == 0 and f != 0, then v = \*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="1a337-181">Wenn e = = 0 und f = = 0, dann v = 0 (null)</span><span class="sxs-lookup"><span data-stu-id="1a337-181">if e == 0 and f == 0, then v = 0 (zero)</span></span>

<span data-ttu-id="1a337-182">32-Bit-Gleit Komma Regeln enthalten auch für 11-Bit-und 10-Bit-Gleit Komma Zahlen, die für das oben beschriebene bitlayout angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="1a337-182">32-bit floating-point rules also hold for 11-bit and 10-bit floating-point numbers, adjusted for the bit layout described above.</span></span> <span data-ttu-id="1a337-183">Zu den Ausnahmen zählen:</span><span class="sxs-lookup"><span data-stu-id="1a337-183">Exceptions include:</span></span>

-   <span data-ttu-id="1a337-184">Genauigkeit: 32-Bit-Gleit Komma Regeln entsprechen 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="1a337-184">Precision: 32-bit floating-point rules adhere to 0.5 ULP.</span></span>
-   <span data-ttu-id="1a337-185">10/11-Bit-Gleit Komma Zahlen behalten denorms bei.</span><span class="sxs-lookup"><span data-stu-id="1a337-185">10/11-bit floating-point numbers preserve denorms.</span></span>
-   <span data-ttu-id="1a337-186">Jeder Vorgang, der zu einer Zahl kleiner als 0 (null) führt, wird an NULL gebunden.</span><span class="sxs-lookup"><span data-stu-id="1a337-186">Any operation that would result in a number less than zero, is clamped to zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a337-187">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a337-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a337-188">Ressourcen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1a337-188">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



