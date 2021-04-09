---
title: Strukturen (RPC)
description: Beschreibung verschiedener Typen von Strukturen im Remote Prozedur Aufruf (RPC).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039335"
---
# <a name="structures-rpc"></a><span data-ttu-id="c3e90-103">Strukturen (RPC)</span><span class="sxs-lookup"><span data-stu-id="c3e90-103">Structures (RPC)</span></span>

<span data-ttu-id="c3e90-104">Es gibt mehrere Kategorien von Strukturen, die in Bezug auf die für das Marshalling erforderlichen Aktionen progressiv komplizierter sind.</span><span class="sxs-lookup"><span data-stu-id="c3e90-104">There are several categories of structures, progressively more complicated in terms of actions required for marshaling.</span></span> <span data-ttu-id="c3e90-105">Sie beginnen mit einer einfachen Struktur, die als Ganzes blockiert werden kann, und fahren mit einer komplexen Struktur fort, bei der das Feld nach außen gewartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c3e90-105">They begin with a simple structure that can be block-copied as a whole, and continue to a complex structure that has to be serviced field by field.</span></span>

-   [<span data-ttu-id="c3e90-106">Einfache Struktur</span><span class="sxs-lookup"><span data-stu-id="c3e90-106">Simple Structure</span></span>](#simple-structure)
-   [<span data-ttu-id="c3e90-107">Einfache Struktur mit Zeigern</span><span class="sxs-lookup"><span data-stu-id="c3e90-107">Simple Structure with Pointers</span></span>](#simple-structure-with-pointers)
-   [<span data-ttu-id="c3e90-108">Konforme Struktur</span><span class="sxs-lookup"><span data-stu-id="c3e90-108">Conformant Structure</span></span>](#conformant-structure)
-   [<span data-ttu-id="c3e90-109">Konforme Struktur mit Zeigern</span><span class="sxs-lookup"><span data-stu-id="c3e90-109">Conformant Structure with Pointers</span></span>](#conformant-structure-with-pointers)
-   [<span data-ttu-id="c3e90-110">Konforme unterschiedliche Struktur (mit oder ohne Zeiger)</span><span class="sxs-lookup"><span data-stu-id="c3e90-110">Conformant Varying Structure (with or without Pointers)</span></span>](#conformant-varying-structure-with-or-without-pointers)
-   [<span data-ttu-id="c3e90-111">Harte Struktur</span><span class="sxs-lookup"><span data-stu-id="c3e90-111">Hard Structure</span></span>](#hard-structure)
-   [<span data-ttu-id="c3e90-112">Komplexe Struktur</span><span class="sxs-lookup"><span data-stu-id="c3e90-112">Complex Structure</span></span>](#complex-structure)
-   [<span data-ttu-id="c3e90-113">Beschreibung des Strukturmember-Layouts</span><span class="sxs-lookup"><span data-stu-id="c3e90-113">Structure Member Layout Description</span></span>](#structure-member-layout-description)

> [!Note]  
> <span data-ttu-id="c3e90-114">Im Vergleich zu Array Kategorien wird deutlich, dass nur Strukturen mit einer Größe von bis zu 64K beschrieben werden können (die Größe ist für den flachen Teil der Struktur), d. h. es gibt keine Entsprechung von SM-und LG-Arrays.</span><span class="sxs-lookup"><span data-stu-id="c3e90-114">When compared to array categories, it becomes clear that only structures up to 64k in size can be described (the size is for the flat part of the structure), that is there is no equivalent of SM and LG arrays.</span></span>

 

<span data-ttu-id="c3e90-115">**Elemente, die von Strukturen gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="c3e90-115">**Members Common to Structures**</span></span>

-   <span data-ttu-id="c3e90-116">**Richt**</span><span class="sxs-lookup"><span data-stu-id="c3e90-116">**alignment**</span></span>

    <span data-ttu-id="c3e90-117">Die erforderliche Ausrichtung des Puffers vor dem Mars Hallen der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3e90-117">The necessary alignment of the buffer before unmarshaling the structure.</span></span> <span data-ttu-id="c3e90-118">Gültige Werte sind 0, 1, 3 und 7 (die tatsächliche Ausrichtung minus 1).</span><span class="sxs-lookup"><span data-stu-id="c3e90-118">Valid values are 0, 1, 3, and 7 (the actual alignment minus 1).</span></span>

-   <span data-ttu-id="c3e90-119">**Arbeitsspeicher \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="c3e90-119">**memory\_size**</span></span>

    <span data-ttu-id="c3e90-120">Größe der Struktur im Arbeitsspeicher in Bytes. für konforme Strukturen enthält diese Größe nicht die Größe des Arrays.</span><span class="sxs-lookup"><span data-stu-id="c3e90-120">Size of the structure in memory in bytes; for conformant structures this size does not include the array's size.</span></span>

-   <span data-ttu-id="c3e90-121">**\_Beschreibung für Offset zu \_ array \_**</span><span class="sxs-lookup"><span data-stu-id="c3e90-121">**offset\_to\_array\_description**</span></span>

    <span data-ttu-id="c3e90-122">Offset vom aktuellen Format Zeichenfolgen-Zeiger auf die Beschreibung des konformen Arrays, das in einer-Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c3e90-122">Offset from the current format string pointer to the description of the conformant array contained in a structure.</span></span>

-   <span data-ttu-id="c3e90-123">**Element \_ Layout**</span><span class="sxs-lookup"><span data-stu-id="c3e90-123">**member\_layout**</span></span>

    <span data-ttu-id="c3e90-124">Beschreibung der einzelnen Elemente der Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3e90-124">Description of each element of the structure.</span></span> <span data-ttu-id="c3e90-125">Die NDR-Routinen müssen diesen Teil der Format Zeichenfolge eines Typs nur untersuchen, wenn die Endian-Transformation erforderlich ist oder wenn der Typ eine komplexe Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="c3e90-125">The NDR routines only need to examine this portion of a type's format string if endian transformation is needed or if the type is a complex structure.</span></span>

-   <span data-ttu-id="c3e90-126">**Zeiger \_ Layout**</span><span class="sxs-lookup"><span data-stu-id="c3e90-126">**pointer\_layout**</span></span>

    <span data-ttu-id="c3e90-127">Weitere Informationen finden Sie im Abschnitt [Zeiger Layout](pointer-layout-tfs.md) .</span><span class="sxs-lookup"><span data-stu-id="c3e90-127">See the [Pointer Layout](pointer-layout-tfs.md) section.</span></span>

## <a name="simple-structure"></a><span data-ttu-id="c3e90-128">Einfache Struktur</span><span class="sxs-lookup"><span data-stu-id="c3e90-128">Simple Structure</span></span>

<span data-ttu-id="c3e90-129">Eine einfache Struktur enthält nur Basis Typen, fixierte Arrays und andere einfache Strukturen.</span><span class="sxs-lookup"><span data-stu-id="c3e90-129">A simple structure contains only base types, fixed arrays, and other simple structures.</span></span> <span data-ttu-id="c3e90-130">Die Hauptfunktion der einfachen Struktur ist, dass Sie als Ganzes blockiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c3e90-130">The main feature of the simple structure is that it can be block-copied as a whole.</span></span>

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a><span data-ttu-id="c3e90-131">Einfache Struktur mit Zeigern</span><span class="sxs-lookup"><span data-stu-id="c3e90-131">Simple Structure with Pointers</span></span>

<span data-ttu-id="c3e90-132">Eine einfache Struktur mit Zeigern enthält nur Basis Typen, Zeiger, fixierte Arrays, einfache Strukturen und andere einfache Strukturen mit Zeigern.</span><span class="sxs-lookup"><span data-stu-id="c3e90-132">A simple structure with pointers contains only base types, pointers, fixed arrays, simple structures, and other simple structures with pointers.</span></span> <span data-ttu-id="c3e90-133">Da das Layout<> nur bei einer Endianess-Konvertierung besucht werden muss, wird es am Ende der Beschreibung platziert.</span><span class="sxs-lookup"><span data-stu-id="c3e90-133">Because the layout<> will only have to be visited when doing an endianess conversion, it is placed at the end of the description.</span></span>

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a><span data-ttu-id="c3e90-134">Konforme Struktur</span><span class="sxs-lookup"><span data-stu-id="c3e90-134">Conformant Structure</span></span>

<span data-ttu-id="c3e90-135">Eine konforme Struktur enthält nur Basis Typen, fixierte Arrays und einfache Strukturen und muss entweder eine konforme Zeichenfolge oder ein konformes Array enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3e90-135">A conformant structure contains only base types, fixed arrays, and simple structures, and must contain either a conformant string or a conformant array.</span></span> <span data-ttu-id="c3e90-136">Dieses Array könnte sich in einer anderen konformen Struktur oder einer konformen Struktur mit Zeigern befinden, die in diese Struktur eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="c3e90-136">This array could actually be contained in another conformant structure or conformant structure with pointers which is embedded in this structure.</span></span>

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a><span data-ttu-id="c3e90-137">Konforme Struktur mit Zeigern</span><span class="sxs-lookup"><span data-stu-id="c3e90-137">Conformant Structure with Pointers</span></span>

<span data-ttu-id="c3e90-138">Eine konforme Struktur mit Zeigern enthält nur Basis Typen, Zeiger, fixierte Arrays, einfache Strukturen und einfache Strukturen mit Zeigern. eine konforme Struktur muss ein konformes Array enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3e90-138">A conformant structure with pointers contains only base types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant structure must contain a conformant array.</span></span> <span data-ttu-id="c3e90-139">Dieses Array könnte sich in einer anderen konformen Struktur oder einer Übereinstimmung mit in dieser Struktur eingebetteten Zeigern befinden.</span><span class="sxs-lookup"><span data-stu-id="c3e90-139">This array could actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a><span data-ttu-id="c3e90-140">Konforme unterschiedliche Struktur (mit oder ohne Zeiger)</span><span class="sxs-lookup"><span data-stu-id="c3e90-140">Conformant Varying Structure (with or without Pointers)</span></span>

<span data-ttu-id="c3e90-141">Eine konforme, unterschiedliche Struktur enthält nur einfache Typen, Zeiger, fixierte Arrays, einfache Strukturen und einfache Strukturen mit Zeigern. eine konforme, unterschiedliche Struktur muss entweder eine konforme Zeichenfolge oder ein konforme Array enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3e90-141">A conformant varying structure contains only simple types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant varying structure must contain either a conformant string or a conformant-varying array.</span></span> <span data-ttu-id="c3e90-142">Die konforme Zeichenfolge oder das Array kann in einer anderen konformen Struktur oder einer konformen Struktur mit Zeigern enthalten sein, die in diese Struktur eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="c3e90-142">The conformant string or array can actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a><span data-ttu-id="c3e90-143">Harte Struktur</span><span class="sxs-lookup"><span data-stu-id="c3e90-143">Hard Structure</span></span>

<span data-ttu-id="c3e90-144">Die feste Struktur war ein Konzept, das auf die Vermeidung von schweren Strafen im Zusammenhang mit der Verarbeitung komplexer Strukturen abzielt.</span><span class="sxs-lookup"><span data-stu-id="c3e90-144">The hard structure was a concept aimed at eliminating steep penalties related to processing complex structures.</span></span> <span data-ttu-id="c3e90-145">Sie wird von einer Beobachtung abgeleitet, dass eine komplexe Struktur in der Regel nur eine oder zwei Bedingungen hat, die das Kopieren von Blöcken verhindern und somit die Leistung im Vergleich zu einer einfachen Struktur beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="c3e90-145">It is derived from an observation that a complex structure typically has only one or two conditions that prevent block-copying, and therefore spoil its performance compared to a simple structure.</span></span> <span data-ttu-id="c3e90-146">Die Übeltäter sind in der Regel Unions oder enumerationsfelder.</span><span class="sxs-lookup"><span data-stu-id="c3e90-146">The culprits are usually unions or enumeration fields.</span></span>

<span data-ttu-id="c3e90-147">Eine feste Struktur ist eine Struktur, die über eine enum16, einen endleerraum im Arbeitsspeicher oder eine Union als letzten Member verfügt.</span><span class="sxs-lookup"><span data-stu-id="c3e90-147">A hard structure is a structure that has an enum16, end-padding in memory, or a union as the last member.</span></span> <span data-ttu-id="c3e90-148">Diese drei Elemente verhindern, dass die Struktur in eine der vorherigen Struktur Kategorien fällt, bei denen ein geringer Interpretations Aufwand und ein maximales Optimierungspotenzial auftreten, aber nicht in der sehr kostspieligen komplexen Struktur Kategorie erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="c3e90-148">These three elements prevent the structure from falling into one of the previous structure categories, which enjoy small interpretation overhead and maximum optimization potential, but do not force it into the very costly complex structure category.</span></span>

<span data-ttu-id="c3e90-149">Der enum16 darf nicht bewirken, dass sich die Arbeitsspeicher-und Netzwerkgröße der Struktur unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="c3e90-149">The enum16 must not cause the memory and wire sizes of the structure to differ.</span></span> <span data-ttu-id="c3e90-150">Die Struktur darf weder ein konformes Array noch einen Zeiger enthalten (es sei denn, ein Teil der Union); die einzigen zulässigen Member sind Basis Typen, fixierte Arrays und einfache Strukturen.</span><span class="sxs-lookup"><span data-stu-id="c3e90-150">The structure cannot have any conformant array, nor any pointers (unless part of the union); the only other members allowed are base types, fixed arrays, and simple structures.</span></span>

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

<span data-ttu-id="c3e90-151">Das Enumeration \_ Offset<2> Feld gibt den Offset vom Anfang der Struktur im Arbeitsspeicher zu einem enum16 an, wenn es einen enthält. andernfalls ist der Enumeration- \_ Offset<2> Feld – 1.</span><span class="sxs-lookup"><span data-stu-id="c3e90-151">The enum\_offset<2> field provides the offset from the beginning of the structure in memory to an enum16 if it contains one; otherwise the enum\_offset<2> field is –1.</span></span>

<span data-ttu-id="c3e90-152">Im \_ Feld kopiergröße<2> wird die Gesamtzahl der Bytes in der Struktur angezeigt, die in den bzw. aus dem Puffer in den Puffer kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c3e90-152">The copy\_size<2> field provides the total number of bytes in the structure, which may be block-copied into/from the buffer.</span></span> <span data-ttu-id="c3e90-153">Diese Summe umfasst weder eine nachfolgende Union noch einen Endabstand im Speicher.</span><span class="sxs-lookup"><span data-stu-id="c3e90-153">This total does not include any trailing union nor any end-padding in memory.</span></span> <span data-ttu-id="c3e90-154">Dieser Wert ist auch der Betrag, um den der Puffer Zeiger nach der Kopie inkrementiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3e90-154">This value is also the amount the buffer pointer should be incremented following the copy.</span></span>

<span data-ttu-id="c3e90-155">Das Feld für die<der Arbeits \_ \_ Speicher-2> ist die Anzahl der Bytes, die der Speicher Zeiger nach dem Block Kopiervorgang erhöht werden soll, bevor eine nachfolgende Union verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="c3e90-155">The mem\_copy\_incr<2> field is the number of bytes the memory pointer should be incremented following the block-copy before handling any trailing union.</span></span> <span data-ttu-id="c3e90-156">Das Inkrementieren um diesen Betrag (nicht nach Kopier \_ Größe<2> Bytes) ergibt einen korrekten Speicher Zeiger auf jede nachfolgende Union.</span><span class="sxs-lookup"><span data-stu-id="c3e90-156">Incrementing by this amount (not by copy\_size<2> bytes) yields a proper memory pointer to any trailing union.</span></span>

## <a name="complex-structure"></a><span data-ttu-id="c3e90-157">Komplexe Struktur</span><span class="sxs-lookup"><span data-stu-id="c3e90-157">Complex Structure</span></span>

<span data-ttu-id="c3e90-158">Eine komplexe Struktur ist jede Struktur, die ein oder mehrere Felder enthält, die entweder verhindern, dass die Struktur blockiert wird, oder für die während des Marshalling oder Unmarshalling eine zusätzliche Überprüfung durchgeführt werden muss (z. b. gebundene Prüfungen auf eine Enumeration).</span><span class="sxs-lookup"><span data-stu-id="c3e90-158">A complex structure is any structure containing one or more fields that either prevent the structure from being block-copied, or for which additional checking must be performed during marshaling or unmarshaling (for example, bound checks on an enumeration).</span></span> <span data-ttu-id="c3e90-159">Die folgenden NDR-Typen fallen in diese Kategorie:</span><span class="sxs-lookup"><span data-stu-id="c3e90-159">The following NDR types fall in this category:</span></span>

-   <span data-ttu-id="c3e90-160">[einfache Typen](simple-types-tfs.md): ENUM16, \_ \_ INT3264 (nur auf 64-Bit-Plattformen), eine Ganzzahl mit dem \[ [ **Bereich**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="c3e90-160">[simple types](simple-types-tfs.md): ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="c3e90-161">Ausrichtungs Abstände am Ende der Struktur</span><span class="sxs-lookup"><span data-stu-id="c3e90-161">alignment padding at the end of the structure</span></span>
-   <span data-ttu-id="c3e90-162">Schnittstellen Zeiger (Sie verwenden einen eingebetteten komplexen)</span><span class="sxs-lookup"><span data-stu-id="c3e90-162">interface pointers (they go using an embedded complex)</span></span>
-   <span data-ttu-id="c3e90-163">ignorierte Zeiger (die sich auf das \[ [**Ignore**](/windows/desktop/Midl/ignore) \] -Attribut und das FC- \_ ignoriertoken beziehen)</span><span class="sxs-lookup"><span data-stu-id="c3e90-163">ignored pointers (that is related to \[[**ignore**](/windows/desktop/Midl/ignore)\] attribute and FC\_IGNORE token)</span></span>
-   <span data-ttu-id="c3e90-164">komplexe Arrays, unterschiedliche Arrays, Zeichen folgen Arrays</span><span class="sxs-lookup"><span data-stu-id="c3e90-164">complex arrays, varying arrays, string arrays</span></span>
-   <span data-ttu-id="c3e90-165">Mehrdimensionale konforme Arrays mit mindestens einer nicht fixierten Dimension</span><span class="sxs-lookup"><span data-stu-id="c3e90-165">multidimensional conformant arrays with at least one nonfixed dimension</span></span>
-   <span data-ttu-id="c3e90-166">Unions</span><span class="sxs-lookup"><span data-stu-id="c3e90-166">unions</span></span>
-   <span data-ttu-id="c3e90-167">Elemente, die mit "über \[ [**tragen \_ als**](/windows/desktop/Midl/transmit-as)" definiert \] sind, \[ [**darstellen \_ als**](/windows/desktop/Midl/represent-as) \] , \[ [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) \] , \[ [**User \_ Marshal**](/windows/desktop/Midl/user-marshal)\]</span><span class="sxs-lookup"><span data-stu-id="c3e90-167">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**represent\_as**](/windows/desktop/Midl/represent-as)\], \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="c3e90-168">eingebettete komplexe Strukturen</span><span class="sxs-lookup"><span data-stu-id="c3e90-168">embedded complex structures</span></span>
-   <span data-ttu-id="c3e90-169">Auffüllen am Ende der Struktur</span><span class="sxs-lookup"><span data-stu-id="c3e90-169">padding at the end of the structure</span></span>

<span data-ttu-id="c3e90-170">Eine komplexe Struktur hat die folgende Formatbeschreibung:</span><span class="sxs-lookup"><span data-stu-id="c3e90-170">A complex structure has the following format description:</span></span>

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

<span data-ttu-id="c3e90-171">Die Arbeitsspeicher \_ Größe<2> Feld ist die Größe der Struktur im Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c3e90-171">The memory\_size<2> field is the size of the structure in memory, in bytes.</span></span>

<span data-ttu-id="c3e90-172">Wenn die Struktur ein konformes Array enthält, gibt die Offset \_ \_ - \_ zu \_ -konform-Array Beschreibung<2> Feld den Offset der Beschreibung des konformen Arrays an; andernfalls ist Sie 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c3e90-172">If the structure contains a conformant array, the offset\_to\_conformant\_array\_description<2> field provides the offset to the conformant array's description, otherwise it is zero.</span></span>

<span data-ttu-id="c3e90-173">Wenn die Struktur Zeiger enthält, stellt das \_ \_ Layout zum Zeiger \_ Layout<2> Feld den Offset hinter dem Layout der Struktur für das Zeiger Layout bereit. andernfalls ist dieses Feld NULL.</span><span class="sxs-lookup"><span data-stu-id="c3e90-173">If the structure has pointers, the offset\_to\_pointer\_layout<2> field provides the offset past the structure's layout to the pointer layout, otherwise this field is zero.</span></span>

<span data-ttu-id="c3e90-174">Das Zeiger \_ Layout<> Feld einer komplexen Struktur wird etwas anders behandelt als bei anderen Strukturen.</span><span class="sxs-lookup"><span data-stu-id="c3e90-174">The pointer\_layout<> field of a complex structure is handled somewhat differently than for other structures.</span></span> <span data-ttu-id="c3e90-175">Das Zeiger \_ Layout<> -Feld einer komplexen Struktur enthält nur Beschreibungen der tatsächlichen Zeiger Felder in der Struktur selbst.</span><span class="sxs-lookup"><span data-stu-id="c3e90-175">The pointer\_layout<> field of a complex structure only contains descriptions of actual pointer fields in the structure itself.</span></span> <span data-ttu-id="c3e90-176">Alle Zeiger, die in eingebetteten Arrays, Unions oder Strukturen enthalten sind, werden nicht im Feld Zeiger Layout<> der komplexen Struktur beschrieben \_ .</span><span class="sxs-lookup"><span data-stu-id="c3e90-176">Any pointers contained within any embedded arrays, unions, or structures are not described in the complex structure's pointer\_layout<> field.</span></span>

> [!Note]  
> <span data-ttu-id="c3e90-177">Dies steht im Gegensatz zu anderen-Strukturen, die die Beschreibung von Zeigern duplizieren, die in eingebetteten Arrays oder Strukturen in Ihrem eigenen Zeiger \_ Layout<> Feld enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c3e90-177">This is in contrast to other structures, which duplicate the description of any pointers contained in embedded arrays or structures in their own pointer \_layout<> field as well.</span></span>

 

<span data-ttu-id="c3e90-178">Das Format des Zeiger Layouts einer komplexen Struktur ist ebenfalls völlig unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="c3e90-178">The format of a complex structure's pointer layout is also radically different.</span></span> <span data-ttu-id="c3e90-179">Da es nur Beschreibungen der tatsächlichen Zeiger Elemente enthält und eine komplexe Struktur gemarshallt wird und ein Feld gleichzeitig gemarshallt wird, enthält das Zeiger \_ Layout<> Feld einfach die Zeiger Beschreibung aller Zeiger Elemente.</span><span class="sxs-lookup"><span data-stu-id="c3e90-179">Because it only contains descriptions of actual pointer members and because a complex structure is marshaled and unmarshaled one field at a time, the pointer\_layout<> field simply contains the pointer description of all pointer members.</span></span> <span data-ttu-id="c3e90-180">Es gibt keine beginnende FC \_ -PP und keines der üblichen Zeiger \_ Layouts<> Informationen.</span><span class="sxs-lookup"><span data-stu-id="c3e90-180">There is no beginning FC\_PP, and none of the usual pointer\_layout<> information.</span></span>

## <a name="structure-member-layout-description"></a><span data-ttu-id="c3e90-181">Beschreibung des Strukturmember-Layouts</span><span class="sxs-lookup"><span data-stu-id="c3e90-181">Structure Member Layout Description</span></span>

<span data-ttu-id="c3e90-182">Die layoutbeschreibung einer Struktur enthält mindestens eines der folgenden Formatzeichen:</span><span class="sxs-lookup"><span data-stu-id="c3e90-182">A structure's layout description contains one or more of the following format characters:</span></span>

-   <span data-ttu-id="c3e90-183">Eines der Basistyps, wie z. b. FC \_ Char, usw.</span><span class="sxs-lookup"><span data-stu-id="c3e90-183">Any of the base type characters, like FC\_CHAR, and so on</span></span>
-   <span data-ttu-id="c3e90-184">Ausrichtungs Direktiven.</span><span class="sxs-lookup"><span data-stu-id="c3e90-184">Alignment directives.</span></span> <span data-ttu-id="c3e90-185">Es gibt drei Formatzeichen, die die Ausrichtung des Speicher Zeigers angeben: FC \_ ALIGNM2, FC \_ ALIGNM4 und FC \_ ALIGNM8.</span><span class="sxs-lookup"><span data-stu-id="c3e90-185">There are three format characters specifying alignment of the memory pointer: FC\_ALIGNM2, FC\_ALIGNM4, and FC\_ALIGNM8.</span></span>
    > [!Note]  
    > <span data-ttu-id="c3e90-186">Es gibt auch Puffer Ausrichtungs Token, FC \_ ALIGNB2 bis FC \_ ALIGNM8; diese werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3e90-186">There are also buffer alignment tokens, FC\_ALIGNB2 through FC\_ALIGNM8; these are not used.</span></span>

     

-   <span data-ttu-id="c3e90-187">Arbeitsspeicher Auffüll Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c3e90-187">Memory padding.</span></span> <span data-ttu-id="c3e90-188">Diese treten nur am Ende der Beschreibung einer Struktur auf und geben die Anzahl von Byte Auffüll Zeichen im Arbeitsspeicher vor dem konformen Array in der Struktur an: FC \_ structpadn, wobei n für die Anzahl der Byte Auffüll Zeichen steht.</span><span class="sxs-lookup"><span data-stu-id="c3e90-188">These occur only at the end of a structure's description and denote the number of bytes of padding in memory before the conformant array in the structure: FC\_STRUCTPADn, where n is the number of bytes of padding.</span></span>
-   <span data-ttu-id="c3e90-189">Alle eingebetteten nicht-Basistyps (Beachten Sie jedoch, dass im Struktur Layout nie ein konformes Array auftritt).</span><span class="sxs-lookup"><span data-stu-id="c3e90-189">Any embedded nonbase type (note, however, that a conformant array never occurs in the structure layout).</span></span> <span data-ttu-id="c3e90-190">Dies hat eine 4-Byte-Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="c3e90-190">This has a 4-byte description:</span></span>

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    <span data-ttu-id="c3e90-191">, wenn der Offset nicht garantiert 2-Byte-ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="c3e90-191">where the offset is not guaranteed to be 2-byte aligned.</span></span>

    <span data-ttu-id="c3e90-192">\_das Speicher Pad<1> ist ein Abstand, der im Arbeitsspeicher vor dem komplexen Feld benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c3e90-192">memory\_pad<1> is a padding needed in memory before the complex field.</span></span>

    <span data-ttu-id="c3e90-193">Offset \_ zu \_ Beschreibung<2> ist ein relativer typoffset zum eingebetteten Typ.</span><span class="sxs-lookup"><span data-stu-id="c3e90-193">offset\_to\_description<2> is a relative type offset to the embedded type.</span></span>

<span data-ttu-id="c3e90-194">Es kann auch ein FC \_ -Pad vor dem abschließenden FC-Ende vorhanden sein \_ , um sicherzustellen, dass die Format Zeichenfolge an einer 2-Byte-Grenze nach dem FC-Ende ausgerichtet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="c3e90-194">There may also be an FC\_PAD before the terminating FC\_END if needed to ensure that the format string will be aligned at a 2-byte boundary following the FC\_END.</span></span>

 

 