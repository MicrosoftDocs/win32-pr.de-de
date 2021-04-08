---
title: Zeiger Layout
description: Das Zeiger Layout beschreibt Zeiger einer Struktur oder eines Arrays.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856639"
---
# <a name="pointer-layout"></a><span data-ttu-id="58cec-103">Zeiger Layout</span><span class="sxs-lookup"><span data-stu-id="58cec-103">Pointer Layout</span></span>

<span data-ttu-id="58cec-104">Das Zeiger Layout beschreibt Zeiger einer Struktur oder eines Arrays.</span><span class="sxs-lookup"><span data-stu-id="58cec-104">Pointer layout describes pointers of a structure or an array.</span></span>

## <a name="pointer_layout"></a><span data-ttu-id="58cec-105">Zeiger \_ Layout<></span><span class="sxs-lookup"><span data-stu-id="58cec-105">pointer\_layout<></span></span>

<span data-ttu-id="58cec-106">Ein Zeiger \_ Layout<> Feld besteht aus der Format \_ \_ Zeichenfolge FC FC, gefolgt von einer oder mehreren Zeiger Beschreibungen, die später beschrieben werden, und endet mit einem FC- \_ endformatzeichen:</span><span class="sxs-lookup"><span data-stu-id="58cec-106">A pointer\_layout<> field consists of the format characters FC\_PP FC\_PAD followed by one or more pointer descriptions, as described later, and terminating with an FC\_END format character:</span></span>

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

<span data-ttu-id="58cec-107">Ein \_ zeigerinstanzlayout \_<> Feld ist eine Format Zeichenfolge, die einzelne oder mehrere Instanzen von Zeigern beschreibt.</span><span class="sxs-lookup"><span data-stu-id="58cec-107">A pointer\_instance\_layout<> field is a format string describing single or multiple instances of pointers.</span></span> <span data-ttu-id="58cec-108">Die folgenden Felder werden in diesen Deskriptoren verwendet:</span><span class="sxs-lookup"><span data-stu-id="58cec-108">The following fields are used in these descriptors:</span></span>

-   <span data-ttu-id="58cec-109">Offset \_ im \_ Speicher</span><span class="sxs-lookup"><span data-stu-id="58cec-109">offset\_in\_memory</span></span>

    <span data-ttu-id="58cec-110">Der Offset mit Vorzeichen für die Position des Zeigers im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="58cec-110">The signed offset to the pointer's location in memory.</span></span> <span data-ttu-id="58cec-111">Bei einem Zeiger in einer Struktur ist dieser Offset ein negativer Offset vom Ende der Struktur (das Ende des nicht konformen Teils der konformen Strukturen). für Arrays erfolgt der Offset vom Anfang des Arrays.</span><span class="sxs-lookup"><span data-stu-id="58cec-111">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures); for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="58cec-112">Offset \_ im \_ Puffer</span><span class="sxs-lookup"><span data-stu-id="58cec-112">offset\_in\_buffer</span></span>

    <span data-ttu-id="58cec-113">Der Offset mit Vorzeichen an der Position des Zeigers im Puffer.</span><span class="sxs-lookup"><span data-stu-id="58cec-113">The signed offset to the pointer's location in the buffer.</span></span> <span data-ttu-id="58cec-114">Bei einem Zeiger in einer Struktur ist dieser Offset ein negativer Offset vom Ende der Struktur (das Ende des nicht konformen Teils der konformen Strukturen): bei Arrays erfolgt der Offset vom Anfang des Arrays.</span><span class="sxs-lookup"><span data-stu-id="58cec-114">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures): for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="58cec-115">Offset \_ zu \_ Array</span><span class="sxs-lookup"><span data-stu-id="58cec-115">offset\_to\_array</span></span>

    <span data-ttu-id="58cec-116">Offset von einer einschließenden Struktur zum eingebetteten Array, dessen Zeiger behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="58cec-116">Offset from an enclosing structure to the embedded array whose pointers are being handled.</span></span> <span data-ttu-id="58cec-117">Bei Arrays der obersten Ebene ist dieses Feld immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="58cec-117">For top-level arrays, this field will always be zero.</span></span>

-   <span data-ttu-id="58cec-118">Iterationen</span><span class="sxs-lookup"><span data-stu-id="58cec-118">iterations</span></span>

    <span data-ttu-id="58cec-119">Die Gesamtanzahl von Zeigern, die das gleiche Layout aufweisen<> beschrieben.</span><span class="sxs-lookup"><span data-stu-id="58cec-119">Total number of pointers that have the same layout<> described.</span></span>

-   <span data-ttu-id="58cec-120">increment</span><span class="sxs-lookup"><span data-stu-id="58cec-120">increment</span></span>

    <span data-ttu-id="58cec-121">Inkrement zwischen aufeinander folgenden Zeigern während einer Wiederholung.</span><span class="sxs-lookup"><span data-stu-id="58cec-121">Increment between successive pointers during a REPEAT.</span></span>

-   <span data-ttu-id="58cec-122">Anzahl \_ von \_ Zeigern</span><span class="sxs-lookup"><span data-stu-id="58cec-122">number\_of\_pointers</span></span>

    <span data-ttu-id="58cec-123">Die Anzahl der unterschiedlichen Zeiger in einer Wiederholungs Instanz.</span><span class="sxs-lookup"><span data-stu-id="58cec-123">Number of different pointers in a repeat instance.</span></span>

-   <span data-ttu-id="58cec-124">Zeiger \_ Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58cec-124">pointer\_description</span></span>

    <span data-ttu-id="58cec-125">Zeiger Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="58cec-125">Pointer description.</span></span>

<span data-ttu-id="58cec-126">Alle Zeiger instanzlayouts verwenden die folgende einzelne Zeiger \_ Instanz<8>:</span><span class="sxs-lookup"><span data-stu-id="58cec-126">All pointer instance layouts use the following single pointer\_instance<8>:</span></span>

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

<span data-ttu-id="58cec-127">Die folgenden Instanzdeskriptoren sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="58cec-127">The following are instance descriptors:</span></span>

<span data-ttu-id="58cec-128">**Einzelne Instanz eines Zeigers auf einen einfachen Typ:**</span><span class="sxs-lookup"><span data-stu-id="58cec-128">**Single instance of a pointer to a simple type:**</span></span>

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

<span data-ttu-id="58cec-129">**Wiederholungs Zeiger korrigiert:**</span><span class="sxs-lookup"><span data-stu-id="58cec-129">**Fixed repeat pointer:**</span></span>

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

<span data-ttu-id="58cec-130">**Variabler Wiederholungs Zeiger:**</span><span class="sxs-lookup"><span data-stu-id="58cec-130">**Variable repeat pointer:**</span></span>

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

<span data-ttu-id="58cec-131">Für die wiederholten Wiederholungs-und Wiederholungs Zeiger Instanzen gibt es einen Satz von Offset-und Zeiger Beschreibungen für jeden Zeiger in der Wiederholungs Instanz.</span><span class="sxs-lookup"><span data-stu-id="58cec-131">For fixed repeat and variable repeat pointer instances there is a set of offset and pointer descriptions for each pointer in the repeat instance.</span></span>

## <a name="pointers-layout-design-issues"></a><span data-ttu-id="58cec-132">Entwurfs Probleme beim Layout von Zeigern</span><span class="sxs-lookup"><span data-stu-id="58cec-132">Pointers Layout Design Issues</span></span>

<span data-ttu-id="58cec-133">In diesem Abschnitt werden Probleme im Zusammenhang mit der Verarbeitung von kompatiblen Strukturen und eingebetteten Zeigern behandelt.</span><span class="sxs-lookup"><span data-stu-id="58cec-133">This section addresses issues related to processing conformant structures and embedded pointers.</span></span> <span data-ttu-id="58cec-134">Das Problem besteht darin, dass der Compiler Zeiger Layouts für Strukturen und Arrays mit einiger Redundanz generiert.</span><span class="sxs-lookup"><span data-stu-id="58cec-134">The issue is that the compiler generates pointer layouts for structures and arrays with some redundancy.</span></span> <span data-ttu-id="58cec-135">Dies ist von Vorteil, da die Informationen hilfreich sind. eine konforme Struktur kann z. b. ein Zeiger Layout durchlaufen, um alle Zeiger aus der Struktur zu bedienen, und aus dem konformen Array, das Teil der konformen Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="58cec-135">This is beneficial, because the information is useful and as such, for example, a conformant structure can walk one pointer layout to service all the pointers from the structure and from the conformant array being part of the conformant structure.</span></span> <span data-ttu-id="58cec-136">Es gibt jedoch einige eingebettete Situationen, bei denen die NDR-Engine zusätzliche Aufgaben ausführen muss, um alle Zeiger Layouts in der richtigen Reihenfolge zu verarbeiten, wobei jeder Zeiger genau einmal verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="58cec-136">However, some embedded situations exist that require the NDR engine to perform additional work to process all the pointer layouts in the proper sequence, processing each pointer exactly once.</span></span>

## <a name="what-the-compiler-generates"></a><span data-ttu-id="58cec-137">Was der Compiler generiert</span><span class="sxs-lookup"><span data-stu-id="58cec-137">What the Compiler Generates</span></span>

<span data-ttu-id="58cec-138">Jedes in diesem Abschnitt erörterte Objekt verfügt über Zeiger, z. b. enthält eine konforme Struktur Zeiger sowohl im Struktur Teil als auch in den Array Elementen.</span><span class="sxs-lookup"><span data-stu-id="58cec-138">Every object discussed in this section has pointers, so for example, a conformant structure has pointers in the structure part as well as in the array elements.</span></span> <span data-ttu-id="58cec-139">Das-Element ist eine einfache Struktur mit einem-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="58cec-139">The element is a simple structure with a pointer.</span></span>

1.  <span data-ttu-id="58cec-140">Konforme Struktur, einzelne Ebene</span><span class="sxs-lookup"><span data-stu-id="58cec-140">Conformant structure, single level</span></span>

    <span data-ttu-id="58cec-141">Der konforme Deskriptor verfügt über einen PP-Teil, in dem alle Zeiger sowohl aus der Struktur als auch aus dem Array beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="58cec-141">The conformant descriptor has a PP part where all the pointers are described, both from the structure and from the array.</span></span> <span data-ttu-id="58cec-142">Die Elementliste enthält den FC " \_ Long" an Stelle eines Zeigers.</span><span class="sxs-lookup"><span data-stu-id="58cec-142">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="58cec-143">Die Beschreibung des caretzarararrays hat Elemente, die einen eingebetteten \_ komplexen und keinen Zeiger Deskriptoren verwenden.</span><span class="sxs-lookup"><span data-stu-id="58cec-143">The CARRAY array descriptor has elements through the use of an embedded\_complex and no pointer descriptors at all.</span></span> <span data-ttu-id="58cec-144">Das Element hat immer noch seinen einzelnen Zeiger Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="58cec-144">The element still has its single pointer descriptor.</span></span> <span data-ttu-id="58cec-145">Das Zeiger Layout liegt vor dem Element Layout in einer konformen Struktur und einfachen Struktur Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="58cec-145">Pointer layout precedes the member layout in a conformant structure and simple structure descriptors.</span></span>

2.  <span data-ttu-id="58cec-146">Konforme Struktur, mindestens zwei Ebenen</span><span class="sxs-lookup"><span data-stu-id="58cec-146">Conformant structure, two or more levels</span></span>

    <span data-ttu-id="58cec-147">Die PP-Beschreibung enthält Zeiger von allen Ebenen.</span><span class="sxs-lookup"><span data-stu-id="58cec-147">The PP description has pointers from all levels.</span></span> <span data-ttu-id="58cec-148">Die gleiche Array Beschreibung wird wieder verwendet wie die interne konforme Struktur.</span><span class="sxs-lookup"><span data-stu-id="58cec-148">It reuses the same array description as the internal conformant structure.</span></span> <span data-ttu-id="58cec-149">Die Elementliste enthält den FC " \_ Long" an Stelle eines Zeigers.</span><span class="sxs-lookup"><span data-stu-id="58cec-149">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="58cec-150">Eine eingebettete Struktur kommt durch die Verwendung eines eingebetteten komplexen.</span><span class="sxs-lookup"><span data-stu-id="58cec-150">An embedded structure comes through the use of an embedded complex.</span></span> <span data-ttu-id="58cec-151">Der konforme Struktur Deskriptor wird unverändert wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="58cec-151">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="58cec-152">Die Größe des flachen Teils der Struktur wird ebenfalls vervollständigt, was bedeutet, dass die Struktur Größe der obersten Ebene die flache Größe der eingebetteten Struktur einschließt.</span><span class="sxs-lookup"><span data-stu-id="58cec-152">The size of the flat portion of the structure comes out complete as well, meaning that the top-level structure size would include embedded structure's flat size.</span></span>

3.  <span data-ttu-id="58cec-153">Komplexe Struktur, einzelne Ebene</span><span class="sxs-lookup"><span data-stu-id="58cec-153">Complex structure, single level</span></span>

    <span data-ttu-id="58cec-154">Zeiger Elemente werden durch einen FC- \_ Zeiger gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="58cec-154">Pointer members are marked by FC\_POINTER.</span></span> <span data-ttu-id="58cec-155">Das Zeiger Layout ist so vereinfacht, dass für jeden FC- \_ Zeiger Eintrag in der Liste ein Zeiger Deskriptor (4 Bytes) vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="58cec-155">Pointer layout is simplified such that there is a pointer descriptor (4 bytes) for each FC\_POINTER entry on the list.</span></span> <span data-ttu-id="58cec-156">Das Zeiger Layout wird parallel zu einem Element Durchlauf durchlaufen, d. h. ein FC- \_ Zeiger bewirkt, dass die nächste Zeiger Beschreibung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="58cec-156">Pointer layout is walked in parallel with a member walk, that is, an FC\_POINTER causes the next pointer description to be processed.</span></span> <span data-ttu-id="58cec-157">Das CArray-Array weist das Zeiger Layout mit allen Deskriptoren des Arrays und dann das-Element durch die Verwendung eines eingebetteten komplexen auf.</span><span class="sxs-lookup"><span data-stu-id="58cec-157">The CARRAY array has pointer layout with all the descriptors of the array, and then element, through the use of an embedded complex.</span></span> <span data-ttu-id="58cec-158">Der Element Deskriptor wird wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="58cec-158">The element descriptor is reused.</span></span> <span data-ttu-id="58cec-159">Die Größe des flachen Teils der Struktur wird beendet. Das heißt, die flache Größe der Struktur der obersten Ebene enthält die flache Größe der eingebetteten Struktur.</span><span class="sxs-lookup"><span data-stu-id="58cec-159">The size of the flat portion of the structure comes out complete; in other words, the top-level structure's flat size includes the embedded structure's flat size.</span></span> <span data-ttu-id="58cec-160">Das Element Layout liegt vor dem Zeiger Layout für komplexe Strukturen.</span><span class="sxs-lookup"><span data-stu-id="58cec-160">The member layout precedes the pointer layout for complex structures.</span></span>

    <span data-ttu-id="58cec-161">Daher unterscheidet sich die Beschreibung des konformen Arrays in Abhängigkeit davon, ob es sich um ein Array innerhalb einer konformen Struktur oder innerhalb einer komplexen Struktur handelt.</span><span class="sxs-lookup"><span data-stu-id="58cec-161">Hence, the conformant array description generation is different depending on whether it is an array inside of a conformant structure or inside a complex structure.</span></span>

4.  <span data-ttu-id="58cec-162">Komplexe Struktur, mindestens zwei Ebenen, Komplex in Komplex</span><span class="sxs-lookup"><span data-stu-id="58cec-162">Complex structure, 2 or more levels, complex in complex</span></span>

    <span data-ttu-id="58cec-163">Die komplexe Struktur der obersten Ebene verfügt über die Member-Zeiger, die eingebettete komplexe Struktur hat ihre Member-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="58cec-163">Top-level complex structure has its member pointers, embedded complex structure has its member pointers.</span></span> <span data-ttu-id="58cec-164">Der konforme Struktur Deskriptor wird wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="58cec-164">The conformant structure descriptor is reused.</span></span> <span data-ttu-id="58cec-165">Der Array Deskriptor von oben ist das wiederverwendete Array aus der eingebetteten-Struktur.</span><span class="sxs-lookup"><span data-stu-id="58cec-165">The array descriptor from the top is the reused array from the embedded structure.</span></span>

5.  <span data-ttu-id="58cec-166">Komplexe Struktur mit einer eingebetteten konformen Struktur</span><span class="sxs-lookup"><span data-stu-id="58cec-166">Complex structure with an embedded conformant structure</span></span>

    <span data-ttu-id="58cec-167">Die oberste = ebenenkonforme Struktur verfügt über die Member-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="58cec-167">Top=level conformant structure has its member pointers.</span></span> <span data-ttu-id="58cec-168">Der konforme Struktur Deskriptor wird unverändert wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="58cec-168">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="58cec-169">Der Array Deskriptor wird aus der eingebetteten konformen Struktur wieder verwendet. Das heißt, es enthält keine Zeiger auf den Array Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="58cec-169">The array descriptor is reused from the embedded conformant structure; in other words, it does not have any pointers at the array descriptor.</span></span> <span data-ttu-id="58cec-170">Das-Element hat seinen Zeiger Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="58cec-170">The element has its pointer descriptor.</span></span>

6.  <span data-ttu-id="58cec-171">Arrays von Strukturen mit Zeigern</span><span class="sxs-lookup"><span data-stu-id="58cec-171">Arrays of structures with pointers</span></span>

    <span data-ttu-id="58cec-172">Ein Array von einfachen Strukturen mit Zeigern wird als smfarray oder CArray generiert, abhängig davon, ob die Größe des Arrays groß ist. in beiden Fällen weist es jedoch ein gezeichtes Zeiger Layout auf (eine \_ wiederholte Wiederholung oder eine \_ wiederholte Variable).</span><span class="sxs-lookup"><span data-stu-id="58cec-172">An array of simple structures with pointers is generated as an SMFARRAY or CARRAY depending whether the array is sized, but in both cases it has a pointer layout that is complete (FIXED\_REPEAT or VARIABLE\_REPEAT).</span></span> <span data-ttu-id="58cec-173">Das Zeiger Layout ist vor dem Element Layout.</span><span class="sxs-lookup"><span data-stu-id="58cec-173">The pointer layout comes before the member layout.</span></span>

    <span data-ttu-id="58cec-174">Ein Array komplexer Strukturen mit Zeigern wird \_ unabhängig davon, ob es sich um ein fester oder eine Größe handelt, als falsch Array generiert, und in beiden Fällen ist kein Zeiger Layout vorhanden.</span><span class="sxs-lookup"><span data-stu-id="58cec-174">An array of complex structures with pointers is generated as BOGUS\_ARRAY regardless whether it is fixed or sized, and in both cases, does not have any pointer layout.</span></span>

## <a name="what-the-ndr-engine-does"></a><span data-ttu-id="58cec-175">Funktionsweise der NDR-Engine</span><span class="sxs-lookup"><span data-stu-id="58cec-175">What the NDR Engine Does</span></span>

<span data-ttu-id="58cec-176">In diesem Abschnitt wird das Verhalten der NDR-Engine beschrieben.</span><span class="sxs-lookup"><span data-stu-id="58cec-176">This section describes the NDR engine behavior.</span></span>

<span data-ttu-id="58cec-177">**Der marshallingdurchlauf**</span><span class="sxs-lookup"><span data-stu-id="58cec-177">**The marshaling pass**</span></span>

1.  <span data-ttu-id="58cec-178">Konforme Strukturen und eingebettete konforme Struktur.</span><span class="sxs-lookup"><span data-stu-id="58cec-178">Conformant structures and embedded conformant structure.</span></span>

    <span data-ttu-id="58cec-179">Die Struktur der obersten Ebene verhält sich wie eine Struktur mit einer Ebene.</span><span class="sxs-lookup"><span data-stu-id="58cec-179">The top-level structure behaves like a single-level structure.</span></span>

2.  <span data-ttu-id="58cec-180">Eingebettete komplexe Struktur mit konformem Array</span><span class="sxs-lookup"><span data-stu-id="58cec-180">Embedded complex structure with conformant array</span></span>

    <span data-ttu-id="58cec-181">Jede komplexe Struktur erzwingt, dass die äußere Struktur eine komplexe Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="58cec-181">Any complex structure forces the outer structure to be a complex structure.</span></span> <span data-ttu-id="58cec-182">Die eingebettete Struktur Marshalls nie das Array.</span><span class="sxs-lookup"><span data-stu-id="58cec-182">Embedded structure never marshals its array.</span></span> <span data-ttu-id="58cec-183">Jede Struktur durchläuft immer eingebettete Zeiger, indem Member einfach gemarshallert werden und ein Member, der als FC- \_ Zeiger auftritt.</span><span class="sxs-lookup"><span data-stu-id="58cec-183">Every structure always goes through embedded pointers by simply marshaling members and a member happening to be an FC\_POINTER.</span></span>

3.  <span data-ttu-id="58cec-184">Komplexe Struktur mit konformen Struktur</span><span class="sxs-lookup"><span data-stu-id="58cec-184">Complex structure with conformant structure</span></span>

    <span data-ttu-id="58cec-185">Die am meisten eingebettete konforme Struktur marshallziert das konforme Array und alle pointierten.</span><span class="sxs-lookup"><span data-stu-id="58cec-185">The top-most embedded conformant structure marshals the conformant array and all the pointees.</span></span> <span data-ttu-id="58cec-186">Die NDR-Engine wird nicht zu tieferen, in die Struktur eingefügten Strukturen herab laufen, wenn vorhanden. Dadurch wird die Lösung vereinfacht, da eine konforme Struktur ein Blatt Objekt ist, so weit das Marshalling von eingebetteten Objekten betrifft.</span><span class="sxs-lookup"><span data-stu-id="58cec-186">The NDR engine never descends to deeper nested conformant structures if there are any; this simplifies the solution, as a conformant structure is a leaf object as far as the marshaling of embedded objects is concerned.</span></span> <span data-ttu-id="58cec-187">Die komplexe Struktur der obersten Ebene überspringt das Marshalling von Arrays.</span><span class="sxs-lookup"><span data-stu-id="58cec-187">The top-level complex structure skips the array marshaling.</span></span>

<span data-ttu-id="58cec-188">**Nicht Marshalling, übertragen und Freigeben von Durchläufen**</span><span class="sxs-lookup"><span data-stu-id="58cec-188">**Unmarshaling, bufsizing and freeing passes**</span></span>

<span data-ttu-id="58cec-189">Das Marshalling ist symmetrisch zum Marshalling. der erste Vorgang, der für komplexe Strukturen durchführt, besteht darin, die Position des poinrats im Puffer zu ermitteln, indem die Funktion **ndrcomplexstructbuffersize** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="58cec-189">Unmarshaling is symmetrical to marshaling; the first operation it performs for complex structures is to find out the pointees' location in the buffer by means of calling the **NdrComplexStructBufferSize** function.</span></span> <span data-ttu-id="58cec-190">Anschließend werden die pointees parallel entfernt. Dadurch wird das gleiche Schema zum ordnungsgemäßen Marshalling der pointierten für die Verwendung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="58cec-190">It then unmarshals pointees in parallel, enabling the same scheme for unmarshaling the pointees correctly to be used.</span></span> <span data-ttu-id="58cec-191">Es sollte keine Verwirrung bezüglich der großen Objekte und Unions bestehen. das Speicher Abbild sollte nicht für Größen Objekte und Unions verwendet werden, sondern nur für den Pufferinhalt.</span><span class="sxs-lookup"><span data-stu-id="58cec-191">There should be no confusion about sized objects and unions; the memory image should not be used for sized objects and unions, just for the buffer contents.</span></span>

<span data-ttu-id="58cec-192">Die Flags, die verwendet werden, um das Marshalling und das Marshalling ordnungsgemäß durchzuführen, werden auf die gleiche Weise wie bei der Überprüfung und Freigabe verwendet, um sicherzustellen, dass pointierten genau einmal durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="58cec-192">The flags used to perform marshaling and unmarshaling correctly are used in the same way in bufsizing and freeing to make sure that pointees are walked exactly once.</span></span>

<span data-ttu-id="58cec-193">**Erfolgs Übergabe**</span><span class="sxs-lookup"><span data-stu-id="58cec-193">**Endianess pass**</span></span>

<span data-ttu-id="58cec-194">Zunächst ähnelt der gegen übergebene Pass einem Marshalling/Unmarshalling. zum Verarbeiten komplexer Strukturen sind zwei Durchgänge erforderlich.</span><span class="sxs-lookup"><span data-stu-id="58cec-194">At first, the endianess pass is somewhat similar to marshaling/unmarshaling; two passes are required to process complex structures.</span></span> <span data-ttu-id="58cec-195">First Pass konvertiert den flachen Teil und findet die Position des pointierten im Puffer ähnlich der Art, wie bufsizing diesen Vorgang für das Marshalling durchführt.</span><span class="sxs-lookup"><span data-stu-id="58cec-195">First pass converts the flat part and finds the pointees' location in the buffer similar to how bufsizing performs this operation for unmarshaling.</span></span> <span data-ttu-id="58cec-196">Der zweite Durchlauf konvertiert dann die pointierten.</span><span class="sxs-lookup"><span data-stu-id="58cec-196">The second pass then converts the pointees.</span></span>

<span data-ttu-id="58cec-197">Endianess-Pässe unterscheiden sich wie folgt: jede Struktur und jeder Member muss abgestuft werden, bis das Blatt Element oder Element ein einfacher Typ ist.</span><span class="sxs-lookup"><span data-stu-id="58cec-197">Endianess passes differ in the following manner: every structure and every member has to be stepped until the leaf member or element is a simple type.</span></span> <span data-ttu-id="58cec-198">Dies unterscheidet sich vom nicht Mars Hallen. beim nicht Marshalling gibt es z. b. nie eine Notwendigkeit, konforme Strukturen zu verarbeiten, die in konforme Strukturen eingebettet sind, oder ein beliebiges Member der konformen Struktur.</span><span class="sxs-lookup"><span data-stu-id="58cec-198">This is different from unmarshaling; in unmarshaling, for example, there is never a need to process conformant structures embedded in conformant structures, or any member of the conformant structure, for that matter.</span></span> <span data-ttu-id="58cec-199">Ein weiteres Problem ist, dass es sich bei der Konvertierung nicht um einen idempotenten Vorgang handelt – daher könnte der Unmarshalling-Durchlauf das rückgängig machen einiger Teile ohne Schaden wiederholen, während die Konvertierung für eine strikte einmal pro einfachen Typ durchgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="58cec-199">Another issue is that the conversion is not an idempotent operation—hence the unmarshaling pass could redo unmarshaling of some pieces without harm, while conversion has to be performed on a strictly once-per-any-simple-type basis.</span></span>

<span data-ttu-id="58cec-200">Daher kann der-Algorithmus für die erneute Anmeldung wie folgt zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="58cec-200">Hence, the endianess algorithm can be summarized as the following.</span></span> <span data-ttu-id="58cec-201">Der NDR hat eine Vorstellung von der Konzept Struktur der obersten Ebene und ein Flag, um dies nach Bedarf zu markieren.</span><span class="sxs-lookup"><span data-stu-id="58cec-201">NDR has a notion of the top-level conformant structure and a flag to mark that, as appropriate.</span></span> <span data-ttu-id="58cec-202">Wenn Sie das erste Mal durchlaufen, z. b. zum Konvertieren des flachen Teils und zum Abrufen der Position der poindanten, wird dieser Begriff nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="58cec-202">When walking the first time, such as to convert the flat portion and to obtain the location of the pointees, this notion would not be used.</span></span> <span data-ttu-id="58cec-203">Der NDR würde die flachen Teile aller Ebenen von Strukturen durchlaufen und nie die Zeiger Verarbeitung Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="58cec-203">NDR would descend through the flat parts of all levels of structures and never venture into pointer processing.</span></span> <span data-ttu-id="58cec-204">Schließlich würde der NDR das Array auf der obersten Ebene in eine flache Konvertierung konvertieren.</span><span class="sxs-lookup"><span data-stu-id="58cec-204">Finally, NDR would flat convert the array at the top-level.</span></span>

<span data-ttu-id="58cec-205">Wenn Sie das zweite Mal durchlaufen, wird das-Flag verwendet, um die Übergabe des eingebetteten Zeigers zu markieren, um zu vermeiden, dass tiefere Ebenen der konformen Strukturen eingegeben werden, und dann die oberste konforme Struktur.</span><span class="sxs-lookup"><span data-stu-id="58cec-205">When walking the second time, the flag would be used to mark the embedded pointer's pass to avoid entering deeper levels of the conformant structures, then the top-most conformant structure.</span></span> <span data-ttu-id="58cec-206">Auf diese Weise würde das-Flag das gängige Marshalling/Unmarshalling-Verhalten erzwingen, um zu vermeiden, dass es zu tieferen Ebenen von konformen Strukturen absteigend wird.</span><span class="sxs-lookup"><span data-stu-id="58cec-206">In this way, the flag would force the common marshaling/unmarshaling behavior, which is to avoid descending into deeper levels of conformant structures.</span></span>

<span data-ttu-id="58cec-207">Der zweite Durchlauf für komplexe Strukturen mit konformen Arrays funktioniert wie folgt: die komplexen Strukturen funktionieren in der üblichen Weise. Dies bedeutet, dass tiefere Ebenen nie Ihre konformen Größe oder Ihre konformen Arrays untersuchen oder überspringen und stattdessen einfach Ihre Member durchlaufen, ohne das Array zu berühren.</span><span class="sxs-lookup"><span data-stu-id="58cec-207">The second pass for complex structures with conformant arrays works as follows: the complex structures work the common way; which means deeper levels would never look at or skip their conformant size or their conformant arrays, and would rather simply walk their members without touching the array.</span></span>

<span data-ttu-id="58cec-208">Bei komplexen Strukturen mit konformen Strukturen muss die konforme Struktur beachten, ob Sie die oberste Ebene ist und ob Sie sich in einer komplexen Struktur befindet.</span><span class="sxs-lookup"><span data-stu-id="58cec-208">For complex structures with conformant structures, the conformant structure must be aware whether it is top level, and whether it is in a complex structure.</span></span> <span data-ttu-id="58cec-209">Der flache Teil des Arrays wird von der obersten konformen Struktur verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="58cec-209">The flat portion of the array is processed by the top-most conformant structure.</span></span> <span data-ttu-id="58cec-210">Beim zweiten Durchlauf würde die am meisten übergebene Struktur den flachen Teil überspringen und das Zeiger Layout durchlaufen und zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="58cec-210">On the second pass, the top-most conformant structure would skip the flat portion and go through the pointer layout and return.</span></span> <span data-ttu-id="58cec-211">Die oberste komplexe Struktur würde den flachen Teil überspringen und auch das Zeiger Layout überspringen.</span><span class="sxs-lookup"><span data-stu-id="58cec-211">The top-most complex structure would skip its flat portion, and would also skip the pointer layout.</span></span>

<span data-ttu-id="58cec-212">**Der robuste Aspekt der nicht Umwahl enden Exemplarische Vorgehensweise**</span><span class="sxs-lookup"><span data-stu-id="58cec-212">**The robust aspect of the endianess walks**</span></span>

<span data-ttu-id="58cec-213">Der einstufige Durchlauf prüft auf die üblichen nicht korrelierten Bedingungen und führt andere Prüfungen in einer nicht korrelierten Art aus.</span><span class="sxs-lookup"><span data-stu-id="58cec-213">The endianess walk checks for the usual out-of-the-buffer conditions and performs other checks of an uncorrelated nature.</span></span> <span data-ttu-id="58cec-214">Die Überprüfungen, die auf korrelierte Werte abzielen (z. b. das Größen Anpassungs Argument und die konformen Größe), können nicht mit diesem Schritt ausgeführt werden. Sie werden später, wenn das Marshalling erfolgt, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58cec-214">The checks aimed at correlated values (such as the sizing argument versus the conformant size) cannot be performed using this step; they are performed later, when unmarshaling.</span></span>

 

 




