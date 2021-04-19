---
title: Windows-Codierungs Konventionen
description: Wenn Sie mit der Windows-Programmierung noch nicht vertraut sind, kann es zu einer displanung kommen, wenn ein Windows-Programm angezeigt wird.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341925"
---
# <a name="windows-coding-conventions"></a><span data-ttu-id="031c9-103">Windows-Codierungs Konventionen</span><span class="sxs-lookup"><span data-stu-id="031c9-103">Windows Coding Conventions</span></span>

<span data-ttu-id="031c9-104">Wenn Sie mit der Windows-Programmierung noch nicht vertraut sind, kann es zu einer displanung kommen, wenn ein Windows-Programm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="031c9-104">If you are new to Windows programming, it can be disconcerting when you first see a Windows program.</span></span> <span data-ttu-id="031c9-105">Der Code wird mit seltsamen Typdefinitionen wie **DWORD \_ ptr** und **lprect** gefüllt, und Variablen haben Namen wie *HWND* und *Pwsz* (als ungarische Notation bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="031c9-105">The code is filled with strange type definitions like **DWORD\_PTR** and **LPRECT**, and variables have names like *hWnd* and *pwsz* (called Hungarian notation).</span></span> <span data-ttu-id="031c9-106">Es lohnt sich, einige der Windows-Codierungs Konventionen kennenzulernen.</span><span class="sxs-lookup"><span data-stu-id="031c9-106">It's worth taking a moment to learn some of the Windows coding conventions.</span></span>

<span data-ttu-id="031c9-107">Die meisten Windows-APIs bestehen aus Funktionen oder Component Object Model (com)-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="031c9-107">The vast majority of Windows APIs consist of either functions or Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="031c9-108">Nur wenige Windows-APIs werden als C++-Klassen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="031c9-108">Very few Windows APIs are provided as C++ classes.</span></span> <span data-ttu-id="031c9-109">(Eine wichtige Ausnahme ist GDI+, eine der 2D-Grafik-APIs.)</span><span class="sxs-lookup"><span data-stu-id="031c9-109">(A notable exception is GDI+, one of the 2-D graphics APIs.)</span></span>

## <a name="typedefs"></a><span data-ttu-id="031c9-110">TypeDefs</span><span class="sxs-lookup"><span data-stu-id="031c9-110">Typedefs</span></span>

<span data-ttu-id="031c9-111">Die Windows-Header enthalten zahlreiche Typedefs.</span><span class="sxs-lookup"><span data-stu-id="031c9-111">The Windows headers contain a lot of typedefs.</span></span> <span data-ttu-id="031c9-112">Viele davon sind in der Header Datei WINDEF. h definiert.</span><span class="sxs-lookup"><span data-stu-id="031c9-112">Many of these are defined in the header file WinDef.h.</span></span> <span data-ttu-id="031c9-113">Im folgenden finden Sie einige, auf die Sie häufig stoßen werden.</span><span class="sxs-lookup"><span data-stu-id="031c9-113">Here are some that you will encounter often.</span></span>

### <a name="integer-types"></a><span data-ttu-id="031c9-114">Ganzzahltypen</span><span class="sxs-lookup"><span data-stu-id="031c9-114">Integer types</span></span>



| <span data-ttu-id="031c9-115">Datentyp</span><span class="sxs-lookup"><span data-stu-id="031c9-115">Data type</span></span>     | <span data-ttu-id="031c9-116">Size</span><span class="sxs-lookup"><span data-stu-id="031c9-116">Size</span></span>    | <span data-ttu-id="031c9-117">Ebenes?</span><span class="sxs-lookup"><span data-stu-id="031c9-117">Signed?</span></span>  |
|---------------|---------|----------|
| <span data-ttu-id="031c9-118">**BYTE**</span><span class="sxs-lookup"><span data-stu-id="031c9-118">**BYTE**</span></span>      | <span data-ttu-id="031c9-119">8 Bit</span><span class="sxs-lookup"><span data-stu-id="031c9-119">8 bits</span></span>  | <span data-ttu-id="031c9-120">Ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="031c9-120">Unsigned</span></span> |
| <span data-ttu-id="031c9-121">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="031c9-121">**DWORD**</span></span>     | <span data-ttu-id="031c9-122">32 Bit</span><span class="sxs-lookup"><span data-stu-id="031c9-122">32 bits</span></span> | <span data-ttu-id="031c9-123">Ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="031c9-123">Unsigned</span></span> |
| <span data-ttu-id="031c9-124">**INT32**</span><span class="sxs-lookup"><span data-stu-id="031c9-124">**INT32**</span></span>     | <span data-ttu-id="031c9-125">32 Bit</span><span class="sxs-lookup"><span data-stu-id="031c9-125">32 bits</span></span> | <span data-ttu-id="031c9-126">Signiert</span><span class="sxs-lookup"><span data-stu-id="031c9-126">Signed</span></span>   |
| <span data-ttu-id="031c9-127">**INT64**</span><span class="sxs-lookup"><span data-stu-id="031c9-127">**INT64**</span></span>     | <span data-ttu-id="031c9-128">64 Bit</span><span class="sxs-lookup"><span data-stu-id="031c9-128">64 bits</span></span> | <span data-ttu-id="031c9-129">Signiert</span><span class="sxs-lookup"><span data-stu-id="031c9-129">Signed</span></span>   |
| <span data-ttu-id="031c9-130">**LONG**</span><span class="sxs-lookup"><span data-stu-id="031c9-130">**LONG**</span></span>      | <span data-ttu-id="031c9-131">32 Bit</span><span class="sxs-lookup"><span data-stu-id="031c9-131">32 bits</span></span> | <span data-ttu-id="031c9-132">Signiert</span><span class="sxs-lookup"><span data-stu-id="031c9-132">Signed</span></span>   |
| <span data-ttu-id="031c9-133">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="031c9-133">**LONGLONG**</span></span>  | <span data-ttu-id="031c9-134">64 Bit</span><span class="sxs-lookup"><span data-stu-id="031c9-134">64 bits</span></span> | <span data-ttu-id="031c9-135">Signiert</span><span class="sxs-lookup"><span data-stu-id="031c9-135">Signed</span></span>   |
| <span data-ttu-id="031c9-136">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="031c9-136">**UINT32**</span></span>    | <span data-ttu-id="031c9-137">32 Bit</span><span class="sxs-lookup"><span data-stu-id="031c9-137">32 bits</span></span> | <span data-ttu-id="031c9-138">Ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="031c9-138">Unsigned</span></span> |
| <span data-ttu-id="031c9-139">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="031c9-139">**UINT64**</span></span>    | <span data-ttu-id="031c9-140">64 Bit</span><span class="sxs-lookup"><span data-stu-id="031c9-140">64 bits</span></span> | <span data-ttu-id="031c9-141">Ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="031c9-141">Unsigned</span></span> |
| <span data-ttu-id="031c9-142">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="031c9-142">**ULONG**</span></span>     | <span data-ttu-id="031c9-143">32 Bit</span><span class="sxs-lookup"><span data-stu-id="031c9-143">32 bits</span></span> | <span data-ttu-id="031c9-144">Ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="031c9-144">Unsigned</span></span> |
| <span data-ttu-id="031c9-145">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="031c9-145">**ULONGLONG**</span></span> | <span data-ttu-id="031c9-146">64 Bit</span><span class="sxs-lookup"><span data-stu-id="031c9-146">64 bits</span></span> | <span data-ttu-id="031c9-147">Ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="031c9-147">Unsigned</span></span> |
| <span data-ttu-id="031c9-148">**WORD**</span><span class="sxs-lookup"><span data-stu-id="031c9-148">**WORD**</span></span>      | <span data-ttu-id="031c9-149">16 Bit</span><span class="sxs-lookup"><span data-stu-id="031c9-149">16 bits</span></span> | <span data-ttu-id="031c9-150">Ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="031c9-150">Unsigned</span></span> |



 

<span data-ttu-id="031c9-151">Wie Sie sehen können, gibt es eine gewisse Redundanz in diesen Typedefs.</span><span class="sxs-lookup"><span data-stu-id="031c9-151">As you can see, there is a certain amount of redundancy in these typedefs.</span></span> <span data-ttu-id="031c9-152">Einige dieser Überschneidungen sind lediglich auf den Verlauf der Windows-APIs zurückzuführen.</span><span class="sxs-lookup"><span data-stu-id="031c9-152">Some of this overlap is simply due to the history of the Windows APIs.</span></span> <span data-ttu-id="031c9-153">Die hier aufgeführten Typen haben eine fester Größe, und die Größen sind in 32-Bit-und 64-Anwendungen identisch.</span><span class="sxs-lookup"><span data-stu-id="031c9-153">The types listed here have fixed size, and the sizes are the same in both 32-bit and 64-applications.</span></span> <span data-ttu-id="031c9-154">Beispielsweise ist der **DWORD** -Typ immer 32 Bits breit.</span><span class="sxs-lookup"><span data-stu-id="031c9-154">For example, the **DWORD** type is always 32 bits wide.</span></span>

### <a name="boolean-type"></a><span data-ttu-id="031c9-155">Boolescher Typ</span><span class="sxs-lookup"><span data-stu-id="031c9-155">Boolean Type</span></span>

<span data-ttu-id="031c9-156">**Bool** ist eine typedef für einen ganzzahligen Wert, der in einem booleschen Kontext verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="031c9-156">**BOOL** is a typedef for an integer value that is used in a Boolean context.</span></span> <span data-ttu-id="031c9-157">Die Header Datei WINDEF. h definiert auch zwei Werte für die Verwendung mit **bool**.</span><span class="sxs-lookup"><span data-stu-id="031c9-157">The header file WinDef.h also defines two values for use with **BOOL**.</span></span>


```C++
#define FALSE    0 
#define TRUE     1
```



<span data-ttu-id="031c9-158">Trotz dieser Definition von **true** können die meisten Funktionen, die einen **booleschen** Typ zurückgeben, einen Wert ungleich 0 (null) zurückgeben, um die boolesche Wahrheit anzugeben.</span><span class="sxs-lookup"><span data-stu-id="031c9-158">Despite this definition of **TRUE**, however, most functions that return a **BOOL** type can return any non-zero value to indicate Boolean truth.</span></span> <span data-ttu-id="031c9-159">Daher sollten Sie immer Folgendes schreiben:</span><span class="sxs-lookup"><span data-stu-id="031c9-159">Therefore, you should always write this:</span></span>


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



<span data-ttu-id="031c9-160">und nicht:</span><span class="sxs-lookup"><span data-stu-id="031c9-160">and not this:</span></span>


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



<span data-ttu-id="031c9-161">Beachten Sie, dass **bool** ein ganzzahliger Typ ist und nicht mit dem C++ **bool** -Typ austauschbar ist.</span><span class="sxs-lookup"><span data-stu-id="031c9-161">Be aware that **BOOL** is an integer type and is not interchangeable with the C++ **bool** type.</span></span>

### <a name="pointer-types"></a><span data-ttu-id="031c9-162">Zeiger Typen</span><span class="sxs-lookup"><span data-stu-id="031c9-162">Pointer Types</span></span>

<span data-ttu-id="031c9-163">Windows definiert viele Datentypen des Formular *Zeigers auf X*.</span><span class="sxs-lookup"><span data-stu-id="031c9-163">Windows defines many data types of the form *pointer-to-X*.</span></span> <span data-ttu-id="031c9-164">Diese haben in der Regel das Präfix *P-* oder *LP-* in den Namen.</span><span class="sxs-lookup"><span data-stu-id="031c9-164">These usually have the prefix *P-* or *LP-* in the name.</span></span> <span data-ttu-id="031c9-165">Beispielsweise ist **lprect** ein Zeiger auf ein [**Rect**](/previous-versions//dd162897(v=vs.85)), wobei **Rect** eine Struktur ist, die ein Rechteck beschreibt.</span><span class="sxs-lookup"><span data-stu-id="031c9-165">For example, **LPRECT** is a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)), where **RECT** is a structure that describes a rectangle.</span></span> <span data-ttu-id="031c9-166">Die folgenden Variablen Deklarationen sind gleichwertig.</span><span class="sxs-lookup"><span data-stu-id="031c9-166">The following variable declarations are equivalent.</span></span>


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



<span data-ttu-id="031c9-167">In der Vergangenheit steht *P* für "Zeiger" und " *LP* " für "Long-Zeiger".</span><span class="sxs-lookup"><span data-stu-id="031c9-167">Historically, *P* stands for "pointer" and *LP* stands for "long pointer".</span></span> <span data-ttu-id="031c9-168">Lange Zeiger (auch als " *weite Zeiger*" bezeichnet) sind eine Holdover von 16-Bit-Fenstern, wenn Sie benötigt werden, um Speicherbereiche außerhalb des aktuellen Segments zu beheben.</span><span class="sxs-lookup"><span data-stu-id="031c9-168">Long pointers (also called *far pointers*) are a holdover from 16-bit Windows, when they were needed to address memory ranges outside the current segment.</span></span> <span data-ttu-id="031c9-169">Das *LP* -Präfix wurde beibehalten, um das Portieren von 16-Bit-Code auf 32-Bit-Windows zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="031c9-169">The *LP* prefix was preserved to make it easier to port 16-bit code to 32-bit Windows.</span></span> <span data-ttu-id="031c9-170">Heute gibt es keinen Unterschied – ein Zeiger ist ein Zeiger.</span><span class="sxs-lookup"><span data-stu-id="031c9-170">Today there is no distinction — a pointer is a pointer.</span></span>

### <a name="pointer-precision-types"></a><span data-ttu-id="031c9-171">Zeiger Genauigkeits Typen</span><span class="sxs-lookup"><span data-stu-id="031c9-171">Pointer Precision Types</span></span>

<span data-ttu-id="031c9-172">Die folgenden Datentypen sind immer die Größe eines Zeigers – d. h. 32 Bits Wide in 32-Bit-Anwendungen und 64 Bits Wide in 64-Bit-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="031c9-172">The following data types are always the size of a pointer—that is, 32 bits wide in 32-bit applications, and 64 bits wide in 64-bit applications.</span></span> <span data-ttu-id="031c9-173">Die Größe wird zur Kompilierzeit bestimmt.</span><span class="sxs-lookup"><span data-stu-id="031c9-173">The size is determined at compile time.</span></span> <span data-ttu-id="031c9-174">Wenn eine 32-Bit-Anwendung auf 64-Bit-Windows ausgeführt wird, sind diese Datentypen weiterhin 4 Bytes breit.</span><span class="sxs-lookup"><span data-stu-id="031c9-174">When a 32-bit application runs on 64-bit Windows, these data types are still 4 bytes wide.</span></span> <span data-ttu-id="031c9-175">(Eine 64-Bit-Anwendung kann nicht auf 32-Bit-Fenstern ausgeführt werden, sodass keine umgekehrte Situation auftritt.)</span><span class="sxs-lookup"><span data-stu-id="031c9-175">(A 64-bit application cannot run on 32-bit Windows, so the reverse situation does not occur.)</span></span>

-   <span data-ttu-id="031c9-176">**DWORD \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="031c9-176">**DWORD\_PTR**</span></span>
-   <span data-ttu-id="031c9-177">**INT \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="031c9-177">**INT\_PTR**</span></span>
-   <span data-ttu-id="031c9-178">**Long- \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="031c9-178">**LONG\_PTR**</span></span>
-   <span data-ttu-id="031c9-179">**ULONG \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="031c9-179">**ULONG\_PTR**</span></span>
-   <span data-ttu-id="031c9-180">**uint \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="031c9-180">**UINT\_PTR**</span></span>

<span data-ttu-id="031c9-181">Diese Typen werden in Situationen verwendet, in denen eine Ganzzahl in einen-Zeiger umgewandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="031c9-181">These types are used in situations where an integer might be cast to a pointer.</span></span> <span data-ttu-id="031c9-182">Sie werden auch verwendet, um Variablen für Zeigerarithmetik zu definieren und Schleifen Zähler zu definieren, die den gesamten Bereich von Bytes in Speicher Puffern durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="031c9-182">They are also used to define variables for pointer arithmetic and to define loop counters that iterate over the full range of bytes in memory buffers.</span></span> <span data-ttu-id="031c9-183">Im Allgemeinen werden Sie an Stellen angezeigt, an denen ein vorhandener 32-Bit-Wert auf 64 Bits auf 64-Bit-Fenstern erweitert wurde.</span><span class="sxs-lookup"><span data-stu-id="031c9-183">More generally, they appear in places where an existing 32-bit value was expanded to 64 bits on 64-bit Windows.</span></span>

## <a name="hungarian-notation"></a><span data-ttu-id="031c9-184">Ungarische Notation</span><span class="sxs-lookup"><span data-stu-id="031c9-184">Hungarian Notation</span></span>

<span data-ttu-id="031c9-185">In der *ungarischen Schreib* Weise werden den Namen von Variablen Präfixe hinzugefügt, um zusätzliche Informationen zur Variablen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="031c9-185">*Hungarian notation* is the practice of adding prefixes to the names of variables, to give additional information about the variable.</span></span> <span data-ttu-id="031c9-186">(Der Erfinder der Notation, Charles Simonyi, war Ungarisch und daher sein Name).</span><span class="sxs-lookup"><span data-stu-id="031c9-186">(The notation's inventor, Charles Simonyi, was Hungarian, hence its name).</span></span>

<span data-ttu-id="031c9-187">In der ursprünglichen Form gibt die ungarische Notation *semantische* Informationen zu einer Variablen an und gibt Ihnen die beabsichtigte Verwendung.</span><span class="sxs-lookup"><span data-stu-id="031c9-187">In its original form, Hungarian notation gives *semantic* information about a variable, telling you the intended use.</span></span> <span data-ttu-id="031c9-188">Beispiels *Weise bedeutet dies* , dass ein Index, *CB* , eine Größe in Byte ("count of bytes") und die Zeilen-und Spalten Nummern von *RW* und *Col* bedeuten.</span><span class="sxs-lookup"><span data-stu-id="031c9-188">For example, *i* means an index, *cb* means a size in bytes ("count of bytes"), and *rw* and *col* mean row and column numbers.</span></span> <span data-ttu-id="031c9-189">Diese Präfixe sind so konzipiert, dass die versehentliche Verwendung einer Variablen im falschen Kontext vermieden wird.</span><span class="sxs-lookup"><span data-stu-id="031c9-189">These prefixes are designed to avoid the accidental use of a variable in the wrong context.</span></span> <span data-ttu-id="031c9-190">Wenn Sie z. b. den Ausdruck gesehen haben `rwPosition +  cbTable` , wissen Sie, dass eine Zeilennummer zu einer Größe hinzugefügt wird, was fast sicherlich ein Fehler im Code ist.</span><span class="sxs-lookup"><span data-stu-id="031c9-190">For example, if you saw the expression `rwPosition +  cbTable`, you would know that a row number is being added to a size, which is almost certainly a bug in the code</span></span>

<span data-ttu-id="031c9-191">Eine allgemeinere Form der ungarischen Notation verwendet Präfixe, um *Typinformationen* anzugeben – beispielsweise *DW* für **DWORD** und *w* für **Word**.</span><span class="sxs-lookup"><span data-stu-id="031c9-191">A more common form of Hungarian notation uses prefixes to give *type* information—for example, *dw* for **DWORD** and *w* for **WORD**.</span></span>

<span data-ttu-id="031c9-192">Wenn Sie im Web nach "ungarischer Notation" suchen, finden Sie viele Meinungen darüber, ob die ungarische Notation gut oder schlecht ist.</span><span class="sxs-lookup"><span data-stu-id="031c9-192">If you search the Web for "Hungarian notation," you will find a lot of opinions about whether Hungarian notation is good or bad.</span></span> <span data-ttu-id="031c9-193">Einige Programmierer haben eine sehr hohe Abneigung gegen die ungarische Notation.</span><span class="sxs-lookup"><span data-stu-id="031c9-193">Some programmers have an intense dislike for Hungarian notation.</span></span> <span data-ttu-id="031c9-194">Andere finden es hilfreich.</span><span class="sxs-lookup"><span data-stu-id="031c9-194">Others find it helpful.</span></span> <span data-ttu-id="031c9-195">Unabhängig davon verwenden viele der Codebeispiele auf MSDN die ungarische Notation, aber Sie müssen nicht die Präfixe beachten, um den Code zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="031c9-195">Regardless, many of the code examples on MSDN use Hungarian notation, but you don't need to memorize the prefixes to understand the code.</span></span>

## <a name="next"></a><span data-ttu-id="031c9-196">Nächste</span><span class="sxs-lookup"><span data-stu-id="031c9-196">Next</span></span>

[<span data-ttu-id="031c9-197">Arbeiten mit Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="031c9-197">Working with Strings</span></span>](working-with-strings.md)

 

 