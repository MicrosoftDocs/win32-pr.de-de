---
title: Grammatik
description: HLSL-Anweisungen werden mit den folgenden Grammatikregeln erstellt.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b77f1050beaee2b269d12e69704018e3c5abee6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129848"
---
# <a name="grammar"></a><span data-ttu-id="0aa49-103">Grammatik</span><span class="sxs-lookup"><span data-stu-id="0aa49-103">Grammar</span></span>

<span data-ttu-id="0aa49-104">HLSL-Anweisungen werden mit den folgenden Grammatikregeln erstellt.</span><span class="sxs-lookup"><span data-stu-id="0aa49-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="0aa49-105">Leerraum</span><span class="sxs-lookup"><span data-stu-id="0aa49-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="0aa49-106">Gleitkommazahlen</span><span class="sxs-lookup"><span data-stu-id="0aa49-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="0aa49-107">Ganze Zahlen</span><span class="sxs-lookup"><span data-stu-id="0aa49-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="0aa49-108">Zeichen</span><span class="sxs-lookup"><span data-stu-id="0aa49-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="0aa49-109">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="0aa49-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="0aa49-110">Identifiers (Bezeichner)</span><span class="sxs-lookup"><span data-stu-id="0aa49-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="0aa49-111">Operatoren</span><span class="sxs-lookup"><span data-stu-id="0aa49-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="0aa49-112">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0aa49-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="0aa49-113">Leerraum</span><span class="sxs-lookup"><span data-stu-id="0aa49-113">Whitespace</span></span>

<span data-ttu-id="0aa49-114">Die folgenden Zeichen werden als Leerzeichen erkannt.</span><span class="sxs-lookup"><span data-stu-id="0aa49-114">The following characters are recognized as white space.</span></span>

- <span data-ttu-id="0aa49-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="0aa49-115">SPACE</span></span>
- <span data-ttu-id="0aa49-116">TAB</span><span class="sxs-lookup"><span data-stu-id="0aa49-116">TAB</span></span>
- <span data-ttu-id="0aa49-117">Eol</span><span class="sxs-lookup"><span data-stu-id="0aa49-117">EOL</span></span>
- <span data-ttu-id="0aa49-118">C-Stilkommentare (/ \* \* /)</span><span class="sxs-lookup"><span data-stu-id="0aa49-118">C style comments (/\* \*/)</span></span>
- <span data-ttu-id="0aa49-119">C++-Stilkommentare (/)</span><span class="sxs-lookup"><span data-stu-id="0aa49-119">C++ style comments (//)</span></span>

## <a name="floating-point-numbers"></a><span data-ttu-id="0aa49-120">Gleitkommazahlen</span><span class="sxs-lookup"><span data-stu-id="0aa49-120">Floating point numbers</span></span>

<span data-ttu-id="0aa49-121">Gleitkommazahlen werden in HLSL wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="0aa49-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="0aa49-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span><span class="sxs-lookup"><span data-stu-id="0aa49-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="0aa49-123">digit-sequence exponent-part floating-suffix(opt)</span><span class="sxs-lookup"><span data-stu-id="0aa49-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="0aa49-124">fractional-constant :</span><span class="sxs-lookup"><span data-stu-id="0aa49-124">fractional-constant :</span></span>

    <span data-ttu-id="0aa49-125">digit-sequence(opt) .</span><span class="sxs-lookup"><span data-stu-id="0aa49-125">digit-sequence(opt) .</span></span> <span data-ttu-id="0aa49-126">Ziffernsequenz</span><span class="sxs-lookup"><span data-stu-id="0aa49-126">digit-sequence</span></span>

    <span data-ttu-id="0aa49-127">digit-sequence .</span><span class="sxs-lookup"><span data-stu-id="0aa49-127">digit-sequence .</span></span>

-   <span data-ttu-id="0aa49-128">exponent-part :</span><span class="sxs-lookup"><span data-stu-id="0aa49-128">exponent-part :</span></span>

    <span data-ttu-id="0aa49-129">e sign(opt) digit-sequence</span><span class="sxs-lookup"><span data-stu-id="0aa49-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="0aa49-130">E sign(opt) digit-sequence</span><span class="sxs-lookup"><span data-stu-id="0aa49-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="0aa49-131">sign : eins der folgenden Zeichen</span><span class="sxs-lookup"><span data-stu-id="0aa49-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="0aa49-132">digit-sequence :</span><span class="sxs-lookup"><span data-stu-id="0aa49-132">digit-sequence :</span></span>

    <span data-ttu-id="0aa49-133">digit</span><span class="sxs-lookup"><span data-stu-id="0aa49-133">digit</span></span>

    <span data-ttu-id="0aa49-134">digit-sequence-Stelle</span><span class="sxs-lookup"><span data-stu-id="0aa49-134">digit-sequence digit</span></span>

-   <span data-ttu-id="0aa49-135">floating-suffix : eins der folgenden Zeichen</span><span class="sxs-lookup"><span data-stu-id="0aa49-135">floating-suffix : one of</span></span>

    <span data-ttu-id="0aa49-136">h H f F l L</span><span class="sxs-lookup"><span data-stu-id="0aa49-136">h H f F l L</span></span>

    <span data-ttu-id="0aa49-137">Verwenden Sie das Suffix "L", um ein vollständiges Gleitkommaliteral mit 64-Bit-Genauigkeit anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0aa49-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="0aa49-138">Ein 32-Bit-Floatliteral ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="0aa49-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="0aa49-139">Beispielsweise erkennt der Compiler den folgenden Literalwert als Gleitkommaliteral mit 32-Bit-Genauigkeit und ignoriert die unteren Bits:</span><span class="sxs-lookup"><span data-stu-id="0aa49-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="0aa49-140">Der Compiler erkennt den folgenden Literalwert als Gleitkommaliteral mit 64-Bit-Genauigkeit:</span><span class="sxs-lookup"><span data-stu-id="0aa49-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="0aa49-141">Ganze Zahlen</span><span class="sxs-lookup"><span data-stu-id="0aa49-141">Integer numbers</span></span>

<span data-ttu-id="0aa49-142">Ganzzahlige Zahlen werden in HLSL wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="0aa49-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="0aa49-143">integer-constant integer-suffix(opt)</span><span class="sxs-lookup"><span data-stu-id="0aa49-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="0aa49-144">integer-constant: eine von</span><span class="sxs-lookup"><span data-stu-id="0aa49-144">integer-constant: one of</span></span>

    <span data-ttu-id="0aa49-145">\# (Dezimalzahl)</span><span class="sxs-lookup"><span data-stu-id="0aa49-145">\# (decimal number)</span></span>

    <span data-ttu-id="0aa49-146">0 \# (oktale Zahl)</span><span class="sxs-lookup"><span data-stu-id="0aa49-146">0\# (octal number)</span></span>

    <span data-ttu-id="0aa49-147">0x \# (Hexadezimalzahl)</span><span class="sxs-lookup"><span data-stu-id="0aa49-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="0aa49-148">Integer-Suffix kann eines der folgenden Sein:</span><span class="sxs-lookup"><span data-stu-id="0aa49-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="0aa49-149">u U l L</span><span class="sxs-lookup"><span data-stu-id="0aa49-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="0aa49-150">Zeichen</span><span class="sxs-lookup"><span data-stu-id="0aa49-150">Characters</span></span>

<span data-ttu-id="0aa49-151">Zeichen werden in HLSL wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="0aa49-151">Characters are represented in HLSL as follows:</span></span>



| <span data-ttu-id="0aa49-152">Zeichen</span><span class="sxs-lookup"><span data-stu-id="0aa49-152">Character</span></span>                                          | <span data-ttu-id="0aa49-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0aa49-153">Description</span></span>                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="0aa49-154">„c“</span><span class="sxs-lookup"><span data-stu-id="0aa49-154">'c'</span></span>                                       | <span data-ttu-id="0aa49-155">(Zeichen)</span><span class="sxs-lookup"><span data-stu-id="0aa49-155">(character)</span></span>                                                     |
| <span data-ttu-id="0aa49-156">\\'a' ' \\ b' ' f ' \\ \\ b' ' \\ r' ' t ' ' \\ \\ v'</span><span class="sxs-lookup"><span data-stu-id="0aa49-156">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="0aa49-157">(Escapes)</span><span class="sxs-lookup"><span data-stu-id="0aa49-157">(escapes)</span></span>                                                       |
| <span data-ttu-id="0aa49-158">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="0aa49-158">'\\\#\#\#'</span></span>                                | <span data-ttu-id="0aa49-159">(oktales Escapezeichen, jedes \# ist eine oktale Ziffer)</span><span class="sxs-lookup"><span data-stu-id="0aa49-159">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="0aa49-160">' \\ x \# '</span><span class="sxs-lookup"><span data-stu-id="0aa49-160">'\\x\#'</span></span>                                   | <span data-ttu-id="0aa49-161">(hexadezimales Escapezeichen, \# ist eine hexadezimale Zahl, eine beliebige Anzahl von Ziffern)</span><span class="sxs-lookup"><span data-stu-id="0aa49-161">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="0aa49-162">' \\ c'</span><span class="sxs-lookup"><span data-stu-id="0aa49-162">'\\c'</span></span>                                     | <span data-ttu-id="0aa49-163">(c ist ein anderes Zeichen, einschließlich umgekehrter Schrägstriche und Anführungszeichen)</span><span class="sxs-lookup"><span data-stu-id="0aa49-163">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="0aa49-164">Escapen werden in Präprozessorausdrücken nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0aa49-164">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="0aa49-165">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="0aa49-165">Strings</span></span>

<span data-ttu-id="0aa49-166">Zeichenfolgen werden in HLSL wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="0aa49-166">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="0aa49-167">"s" (s ist eine beliebige Zeichenfolge mit Escapezeichen).</span><span class="sxs-lookup"><span data-stu-id="0aa49-167">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="0aa49-168">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0aa49-168">Identifiers</span></span>

<span data-ttu-id="0aa49-169">Bezeichner werden in HLSL wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="0aa49-169">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="0aa49-170">Operatoren</span><span class="sxs-lookup"><span data-stu-id="0aa49-170">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="0aa49-171">Außerdem jedes andere einzelne Zeichen, das keiner anderen Regel entspricht.</span><span class="sxs-lookup"><span data-stu-id="0aa49-171">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aa49-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0aa49-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aa49-173">Anhang (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0aa49-173">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




