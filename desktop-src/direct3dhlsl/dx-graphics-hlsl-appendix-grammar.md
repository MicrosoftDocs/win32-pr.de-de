---
title: Grammatik
description: HLSL-Anweisungen werden mithilfe der folgenden Regeln für die Grammatik erstellt.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2346e1ca2302f80c796558b4aa2bbdce016d494
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516520"
---
# <a name="grammar"></a><span data-ttu-id="ffaf3-103">Grammatik</span><span class="sxs-lookup"><span data-stu-id="ffaf3-103">Grammar</span></span>

<span data-ttu-id="ffaf3-104">HLSL-Anweisungen werden mithilfe der folgenden Regeln für die Grammatik erstellt.</span><span class="sxs-lookup"><span data-stu-id="ffaf3-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="ffaf3-105">Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="ffaf3-106">Gleit Komma Zahlen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="ffaf3-107">Ganze Zahlen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="ffaf3-108">Zeichen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="ffaf3-109">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="ffaf3-110">Identifiers (Bezeichner)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="ffaf3-111">Operatoren</span><span class="sxs-lookup"><span data-stu-id="ffaf3-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="ffaf3-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="ffaf3-113">Leerraum</span><span class="sxs-lookup"><span data-stu-id="ffaf3-113">Whitespace</span></span>

<span data-ttu-id="ffaf3-114">Die folgenden Zeichen werden als Leerzeichen erkannt.</span><span class="sxs-lookup"><span data-stu-id="ffaf3-114">The following characters are recognized as white space.</span></span>



|                            |
|----------------------------|
| <span data-ttu-id="ffaf3-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="ffaf3-115">SPACE</span></span>                      |
| <span data-ttu-id="ffaf3-116">TAB</span><span class="sxs-lookup"><span data-stu-id="ffaf3-116">TAB</span></span>                        |
| <span data-ttu-id="ffaf3-117">EOL</span><span class="sxs-lookup"><span data-stu-id="ffaf3-117">EOL</span></span>                        |
| <span data-ttu-id="ffaf3-118">C-Stil Kommentare (/ \* \* /)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-118">C style comments (/\* \*/)</span></span> |
| <span data-ttu-id="ffaf3-119">C++-Stil Kommentare (//)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-119">C++ style comments (//)</span></span>    |



 

## <a name="floating-point-numbers"></a><span data-ttu-id="ffaf3-120">Gleit Komma Zahlen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-120">Floating point numbers</span></span>

<span data-ttu-id="ffaf3-121">Gleit Komma Zahlen werden in HLSL wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="ffaf3-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="ffaf3-122">Bruchteil-Konstante Exponent-Part (opt) Floating-Suffix (opt)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="ffaf3-123">Exponent-Part-enumerationszeichen für Digit-Sequence (opt)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="ffaf3-124">Bruch Komma Konstante:</span><span class="sxs-lookup"><span data-stu-id="ffaf3-124">fractional-constant :</span></span>

    <span data-ttu-id="ffaf3-125">Ziffern Sequenz (opt).</span><span class="sxs-lookup"><span data-stu-id="ffaf3-125">digit-sequence(opt) .</span></span> <span data-ttu-id="ffaf3-126">Ziffern Sequenz</span><span class="sxs-lookup"><span data-stu-id="ffaf3-126">digit-sequence</span></span>

    <span data-ttu-id="ffaf3-127">Ziffern Sequenz.</span><span class="sxs-lookup"><span data-stu-id="ffaf3-127">digit-sequence .</span></span>

-   <span data-ttu-id="ffaf3-128">Exponent-Part:</span><span class="sxs-lookup"><span data-stu-id="ffaf3-128">exponent-part :</span></span>

    <span data-ttu-id="ffaf3-129">e-Sign (opt)-Ziffern Sequenz</span><span class="sxs-lookup"><span data-stu-id="ffaf3-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="ffaf3-130">E-Sign (opt)-Ziffern Sequenz</span><span class="sxs-lookup"><span data-stu-id="ffaf3-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="ffaf3-131">sign : eins der folgenden Zeichen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="ffaf3-132">Ziffern Sequenz:</span><span class="sxs-lookup"><span data-stu-id="ffaf3-132">digit-sequence :</span></span>

    <span data-ttu-id="ffaf3-133">digit</span><span class="sxs-lookup"><span data-stu-id="ffaf3-133">digit</span></span>

    <span data-ttu-id="ffaf3-134">digit-sequence-Stelle</span><span class="sxs-lookup"><span data-stu-id="ffaf3-134">digit-sequence digit</span></span>

-   <span data-ttu-id="ffaf3-135">floating-suffix : eins der folgenden Zeichen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-135">floating-suffix : one of</span></span>

    <span data-ttu-id="ffaf3-136">h h f f l l</span><span class="sxs-lookup"><span data-stu-id="ffaf3-136">h H f F l L</span></span>

    <span data-ttu-id="ffaf3-137">Verwenden Sie das Suffix "L", um ein vollständiges Gleit Komma Trennzeichen mit 64-Bit-Genauigkeit anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ffaf3-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="ffaf3-138">Standardmäßig ist ein Gleit Komma Wert von 32 Bit.</span><span class="sxs-lookup"><span data-stu-id="ffaf3-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="ffaf3-139">Der Compiler erkennt z. b. den folgenden Literalwert als Gleit Komma-Literale mit 32-Bit-Genauigkeit und ignoriert die unteren Bits:</span><span class="sxs-lookup"><span data-stu-id="ffaf3-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="ffaf3-140">Der Compiler erkennt den folgenden Literalwert als Gleit Komma-Literale mit 64-Bit-Genauigkeit:</span><span class="sxs-lookup"><span data-stu-id="ffaf3-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="ffaf3-141">Ganze Zahlen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-141">Integer numbers</span></span>

<span data-ttu-id="ffaf3-142">Ganzzahlige Zahlen werden in HLSL wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="ffaf3-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="ffaf3-143">integer-Konstante Integer-Suffix (opt)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="ffaf3-144">ganzzahlige Konstante: eine von</span><span class="sxs-lookup"><span data-stu-id="ffaf3-144">integer-constant: one of</span></span>

    <span data-ttu-id="ffaf3-145">\# (Dezimalzahl)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-145">\# (decimal number)</span></span>

    <span data-ttu-id="ffaf3-146">0 \# (oktale Zahl)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-146">0\# (octal number)</span></span>

    <span data-ttu-id="ffaf3-147">0x (hexadezimale \# Zahl)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="ffaf3-148">ganzzahliges Suffix kann eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="ffaf3-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="ffaf3-149">u u l l</span><span class="sxs-lookup"><span data-stu-id="ffaf3-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="ffaf3-150">Zeichen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-150">Characters</span></span>

<span data-ttu-id="ffaf3-151">Zeichen werden in HLSL wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="ffaf3-151">Characters are represented in HLSL as follows:</span></span>



|                                           |                                                                 |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ffaf3-152">„c“</span><span class="sxs-lookup"><span data-stu-id="ffaf3-152">'c'</span></span>                                       | <span data-ttu-id="ffaf3-153">Art</span><span class="sxs-lookup"><span data-stu-id="ffaf3-153">(character)</span></span>                                                     |
| <span data-ttu-id="ffaf3-154">' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r ' ' \\ t ' ' \\ v '</span><span class="sxs-lookup"><span data-stu-id="ffaf3-154">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="ffaf3-155">entkam</span><span class="sxs-lookup"><span data-stu-id="ffaf3-155">(escapes)</span></span>                                                       |
| <span data-ttu-id="ffaf3-156">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="ffaf3-156">'\\\#\#\#'</span></span>                                | <span data-ttu-id="ffaf3-157">(oktale Escapezeichen, jede \# ist eine oktale Ziffer)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-157">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="ffaf3-158">" \\ x \# "</span><span class="sxs-lookup"><span data-stu-id="ffaf3-158">'\\x\#'</span></span>                                   | <span data-ttu-id="ffaf3-159">(Hex-Escapezeichen, ist hexadezimal \# Zahl, beliebige Anzahl von Ziffern)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-159">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="ffaf3-160">" \\ c"</span><span class="sxs-lookup"><span data-stu-id="ffaf3-160">'\\c'</span></span>                                     | <span data-ttu-id="ffaf3-161">(c ist ein anderes Zeichen, einschließlich umgekehrter Schrägstriche und Anführungszeichen)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-161">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="ffaf3-162">Escapezeichen werden in Präprozessorausdrücken nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ffaf3-162">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="ffaf3-163">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-163">Strings</span></span>

<span data-ttu-id="ffaf3-164">Zeichen folgen werden in HLSL wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="ffaf3-164">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="ffaf3-165">"s" (s ist eine beliebige Zeichenfolge mit Escapezeichen).</span><span class="sxs-lookup"><span data-stu-id="ffaf3-165">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="ffaf3-166">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ffaf3-166">Identifiers</span></span>

<span data-ttu-id="ffaf3-167">Bezeichner werden in HLSL wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="ffaf3-167">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="ffaf3-168">Operatoren</span><span class="sxs-lookup"><span data-stu-id="ffaf3-168">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="ffaf3-169">Auch ein beliebiges anderes einzelnes Zeichen, das nicht mit einer anderen Regel identisch war.</span><span class="sxs-lookup"><span data-stu-id="ffaf3-169">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffaf3-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ffaf3-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffaf3-171">Anhang (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ffaf3-171">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




