---
title: Korrelations Deskriptoren
description: Ein Korrelations Deskriptor ist eine Format Zeichenfolge, die einen Ausdruck auf Grundlage eines Arguments beschreibt, das sich auf ein anderes Argument bezieht.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858441"
---
# <a name="correlation-descriptors"></a><span data-ttu-id="be9f3-103">Korrelations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="be9f3-103">Correlation Descriptors</span></span>

<span data-ttu-id="be9f3-104">Ein Korrelations Deskriptor ist eine Format Zeichenfolge, die einen Ausdruck auf Grundlage eines Arguments beschreibt, das sich auf ein anderes Argument bezieht.</span><span class="sxs-lookup"><span data-stu-id="be9f3-104">A correlation descriptor is a format string that describes an expression based on one argument related to another argument.</span></span> <span data-ttu-id="be9f3-105">Ein Korrelations Deskriptor ist für die Verarbeitung der Semantik im Zusammenhang mit Attributen wie " \[ **size \_ is ()**" \] , " \[ **length \_ is ()**" \] , " \[ **Switch \_ is ()** " \] und " \[ **IID \_ is ()** \] "</span><span class="sxs-lookup"><span data-stu-id="be9f3-105">A correlation descriptor is needed for handling semantics related to attributes like \[**size\_is()**\], \[**length\_is()**\], \[**switch\_is()**\] and \[**iid\_is()**\].</span></span> <span data-ttu-id="be9f3-106">Korrelations Deskriptoren werden mit Arrays, Größen Zeigern, Unions und Schnittstellen Zeigern verwendet.</span><span class="sxs-lookup"><span data-stu-id="be9f3-106">Correlation descriptors are used with arrays, sized pointers, unions, and interface pointers.</span></span> <span data-ttu-id="be9f3-107">Der Wert des möglichen Ausdrucks kann eine Größe, eine Länge, ein Union-diskriminant oder ein Zeiger auf eine IID sein.</span><span class="sxs-lookup"><span data-stu-id="be9f3-107">The eventual expression value can be a size, a length, a union discriminant, or a pointer to an IID, respectively.</span></span> <span data-ttu-id="be9f3-108">In Form von Format Zeichenfolgen werden Korrelations Deskriptoren mit Arrays, Unions und Schnittstellen Zeigern verwendet.</span><span class="sxs-lookup"><span data-stu-id="be9f3-108">In terms of format strings, correlation descriptors are used with arrays, unions, and interface pointers.</span></span> <span data-ttu-id="be9f3-109">Ein Größen Zeiger wird in Format Zeichenfolgen als Zeiger auf ein Array beschrieben.</span><span class="sxs-lookup"><span data-stu-id="be9f3-109">A sized pointer is described in format strings as a pointer to an array.</span></span>

<span data-ttu-id="be9f3-110">Es gibt zwei Routinen, in denen grundlegende Ausdrucks Berechnungen durchgeführt werden: ndrpcomputeconformance wird für Größen, Switches und IID verwendet, \* während ndrpcomputevarianz für Längen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be9f3-110">There are two routines performing basic expression calculations: NdrpComputeConformance is used for sizes, switches and IID\* while NdrpComputeVariance is used for lengths.</span></span> <span data-ttu-id="be9f3-111">Es gibt auch eine einzige Routine, mit der eine Korrelations Wert Validierung für Denial-of-Angriff-Funktionen durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be9f3-111">There is also a single routine to perform a correlation value validation for denial-of-attack functionality.</span></span>

<span data-ttu-id="be9f3-112">Korrelations Deskriptoren wurden so entworfen, dass nur sehr begrenzte Ausdrücke unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="be9f3-112">Correlation descriptors have been designed to support only very limited expressions.</span></span> <span data-ttu-id="be9f3-113">Für komplizierte Situationen generiert der Compiler eine Ausdrucks Auswertungs Routine, die bei Bedarf von der Engine aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="be9f3-113">For complicated situations, the compiler generates an expression evaluation routine to be called by the engine when needed.</span></span>

<span data-ttu-id="be9f3-114">Ein Korrelations Deskriptor weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="be9f3-114">A correlation descriptor has the following format:</span></span>

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

<span data-ttu-id="be9f3-115">Der Korrelations deskriptorkorrelationstyp \_<1> besteht aus zwei Nibbles: die oberen 4 Bits beschreiben, wo der Ausdruck gefunden werden kann, und die unteren 4 Bits beschreiben den Typ des Ausdrucks Werts.</span><span class="sxs-lookup"><span data-stu-id="be9f3-115">The correlation descriptor correlation\_type<1> consists of two nibbles: the upper 4 bits describe where the expression can be found and the lower 4 bits describe the type of the expression value.</span></span>

<span data-ttu-id="be9f3-116">Der obere Halbbyte kann einen der folgenden fünf Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="be9f3-116">The upper nibble can have one of these five values:</span></span>

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span data-ttu-id="be9f3-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>normale FC- \_ \_ Konformität</span><span class="sxs-lookup"><span data-stu-id="be9f3-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>FC\_NORMAL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="be9f3-118">Eine normale Übereinstimmung, z. b. die, die in einem Feld einer Struktur beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="be9f3-118">A normal case of conformance, such as that described in a field of a structure.</span></span>

</dd> <dt>

<span data-ttu-id="be9f3-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>FC- \_ Zeiger \_ Konformität</span><span class="sxs-lookup"><span data-stu-id="be9f3-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>FC\_POINTER\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="be9f3-120">Für attributierte Zeiger (**size \_ ist ()**, **length \_ ist ()**), die Felder in einer Struktur sind.</span><span class="sxs-lookup"><span data-stu-id="be9f3-120">For attributed pointers (**size\_is()**, **length\_is()**) which are fields in a structure.</span></span> <span data-ttu-id="be9f3-121">Dies wirkt sich darauf aus, wie der Basis Speicher Zeiger festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="be9f3-121">This affects the way the base memory pointer is set.</span></span>

</dd> <dt>

<span data-ttu-id="be9f3-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>FC- \_ Konformität der obersten \_ Ebene \_</span><span class="sxs-lookup"><span data-stu-id="be9f3-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>FC\_TOP\_LEVEL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="be9f3-123">Für die Übereinstimmung auf oberster Ebene, die von einem anderen Parameter beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="be9f3-123">For top-level conformance described by another parameter.</span></span>

</dd> <dt>

<span data-ttu-id="be9f3-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>die \_ \_ \_ multid- \_ Konformität der obersten Ebene von FC</span><span class="sxs-lookup"><span data-stu-id="be9f3-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>FC\_TOP\_LEVEL\_MULTID\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="be9f3-125">Für die Konformität auf oberster Ebene eines mehrdimensionalen Arrays, das von einem anderen Parameter beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="be9f3-125">For top-level conformance of a multidimensional array described by another parameter.</span></span>

> [!Note]  
> <span data-ttu-id="be9f3-126">Arrays und Zeiger mit mehrdimensionaler Größenangabe einen Switch zu [**– Oicf**](/windows/desktop/Midl/-oi).</span><span class="sxs-lookup"><span data-stu-id="be9f3-126">Multidimensional sized arrays and pointers trigger a switch to [**–Oicf**](/windows/desktop/Midl/-oi).</span></span>

 

</dd> <dt>

<span data-ttu-id="be9f3-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>FC \_ - \_ konstantenkonformität</span><span class="sxs-lookup"><span data-stu-id="be9f3-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>FC\_CONSTANT\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="be9f3-128">Für einen konstanten Wert.</span><span class="sxs-lookup"><span data-stu-id="be9f3-128">For a constant value.</span></span> <span data-ttu-id="be9f3-129">Der Compiler berechnet den Wert aus einem konstanten Ausdruck, der vom Benutzer bereitgestellt wird, vorab.</span><span class="sxs-lookup"><span data-stu-id="be9f3-129">The compiler precalculates the value from a constant expression supplied by the user.</span></span> <span data-ttu-id="be9f3-130">Wenn dies der Fall ist, enthalten die nachfolgenden 3 Bytes in der Übereinstimmungs Beschreibung die unteren 3 Bytes, die die Konformitäts Größe beschreiben.</span><span class="sxs-lookup"><span data-stu-id="be9f3-130">When this is the case, the subsequent 3 bytes in the conformance description contain the lower 3 bytes of a long describing the conformance size.</span></span> <span data-ttu-id="be9f3-131">Es ist keine weitere Berechnung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="be9f3-131">No further computation is required.</span></span>

</dd> </dl>

<span data-ttu-id="be9f3-132">Der untere Halbbyte gibt den Typ des Werts an, der aus dem Arbeitsspeicher extrahiert werden muss:</span><span class="sxs-lookup"><span data-stu-id="be9f3-132">The lower nibble gives the type of the value that needs to be extracted from memory:</span></span>

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> <span data-ttu-id="be9f3-133">64-Bit-Ausdrücke werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be9f3-133">64-bit expressions are not supported.</span></span> <span data-ttu-id="be9f3-134">FC \_ Hyper wird nur für **IID \_ is ()** auf 64-Bit-Plattformen verwendet, um den Zeiger Wert für IID zu extrahieren \* .</span><span class="sxs-lookup"><span data-stu-id="be9f3-134">FC\_HYPER is used only for **iid\_is()** on 64-bit platforms to extract the pointer value for IID\*.</span></span>
>
> <span data-ttu-id="be9f3-135">Der Compiler legt den Halbbyte-Typ für die folgenden Fälle auf 0 (null) fest: der oben erwähnte Konstante Ausdruck und die Auswertungs Ausdrucks Routine müssen aufgerufen werden, z. b. wenn die Einhaltung der FC \_ \_ -Konstante und der FC- \_ Rückruf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be9f3-135">The compiler sets the type nibble to zero for the following cases: constant expression mentioned above and when evaluation expression routine needs to be called, for example, when FC\_CONSTANT\_CONFORMANCE and FC\_CALLBACK are used.</span></span>

 

<span data-ttu-id="be9f3-136">Die Größe \_ ist \_ op<1> Feld ermöglicht, dass einer der folgenden Vorgänge auf die Übereinstimmungs Variable angewendet wird:</span><span class="sxs-lookup"><span data-stu-id="be9f3-136">The size\_is\_op<1> field allows for one of the following operations to be applied to the conformance variable:</span></span>

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

<span data-ttu-id="be9f3-137">Die FC- \_ dereferenzierungskonstante wird für die Korrelation als pointee verwendet, z. b. für **\[ size \_ ( \* PL) \]**.</span><span class="sxs-lookup"><span data-stu-id="be9f3-137">The FC\_DEREFERENCE constant is used for correlation being a pointee, like for **\[size\_is(\*pL)\]**.</span></span> <span data-ttu-id="be9f3-138">Arithmetische Operatoren verwenden nur die-Konstante.</span><span class="sxs-lookup"><span data-stu-id="be9f3-138">Arithmetic operators just use the indicated constant.</span></span> <span data-ttu-id="be9f3-139">Die FC- \_ Rückruf Konstante gibt an, dass eine Ausdrucks Auswertungs Routine aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="be9f3-139">The FC\_CALLBACK constant indicates that an expression evaluation routine needs to be called.</span></span>

<span data-ttu-id="be9f3-140">Der Offset<2> Feld ist in der Regel ein relativer Speicher Offset für die Ausdrucks Argument Variable.</span><span class="sxs-lookup"><span data-stu-id="be9f3-140">The offset<2> field is typically a relative memory offset to the expression argument variable.</span></span> <span data-ttu-id="be9f3-141">Es kann auch eine Ausdrucks Auswertung – Routine Index sein.</span><span class="sxs-lookup"><span data-stu-id="be9f3-141">It can also be an expression evaluation–routine index.</span></span> <span data-ttu-id="be9f3-142">Wie bereits zuvor in diesem Dokument erwähnt, ist es für konstante Ausdrücke ein Teil des tatsächlichen, endgültigen Ausdrucks Werts.</span><span class="sxs-lookup"><span data-stu-id="be9f3-142">As mentioned previously in this document, for constant expressions it is a part of actual, final expression value.</span></span>

<span data-ttu-id="be9f3-143">Die Interpretation des Offset<2> Felds als Speicher Offset hängt von der Komplexität des Ausdrucks, dem Speicherort der Ausdrucks Variablen und im Fall eines Arrays ab, ob das Array tatsächlich ein attributierter Zeiger ist.</span><span class="sxs-lookup"><span data-stu-id="be9f3-143">The interpretation of the offset<2> field as memory offset depends on the complexity of the expression, the location of the expression variable, and in the case of an array, whether the array is actually an attributed pointer.</span></span>

<span data-ttu-id="be9f3-144">Wenn das Array ein attributierter Zeiger ist und die Übereinstimmungs Variable ein Feld in einer Struktur ist, enthält das Offset Feld den Offset vom Anfang der Struktur bis zur Übereinstimmungs beschreibenden Felder.</span><span class="sxs-lookup"><span data-stu-id="be9f3-144">If the array is an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the beginning of the structure to the conformance-describing field.</span></span> <span data-ttu-id="be9f3-145">Wenn es sich bei dem Array nicht um einen attributierten Zeiger handelt und die Übereinstimmungs Variable ein Feld in einer Struktur ist, enthält das Offset-Feld den Offset vom Ende des nicht konformen Teils der Struktur bis zu dem Feld, das die Konformität beschreibt.</span><span class="sxs-lookup"><span data-stu-id="be9f3-145">If the array is not an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the end of the nonconformant part of the structure to the conformance-describing field.</span></span> <span data-ttu-id="be9f3-146">In der Regel befindet sich das konforme Array am Ende der Struktur.</span><span class="sxs-lookup"><span data-stu-id="be9f3-146">Typically, the conformant array is at the end of the structure.</span></span>

<span data-ttu-id="be9f3-147">Für die Übereinstimmung auf oberster Ebene enthält das Offset Feld den Offset von der Position des ersten Parameters des Stubs auf dem Stapel bis zu dem Parameter, der die Konformität beschreibt.</span><span class="sxs-lookup"><span data-stu-id="be9f3-147">For top-level conformance, the offset field contains the offset from the stub's first parameter's location on the stack to the parameter that describes the conformance.</span></span> <span data-ttu-id="be9f3-148">Dies wird im **– OS** -Modus nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="be9f3-148">This is not used in **–Os** mode.</span></span> <span data-ttu-id="be9f3-149">Es gibt noch weitere Ausnahmen für die Interpretation des Offset Felds. Diese Ausnahmen werden in der Beschreibung dieser Typen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="be9f3-149">There are other exceptions to the interpretation of the offset field; such exceptions are described in the description of those types.</span></span>

<span data-ttu-id="be9f3-150">Wenn Offset<2> mit dem FC- \_ Rückruf verwendet wird, enthält es einen Index in der Routine Tabelle der Ausdrucks Auswertung, die vom Compiler generiert wird.</span><span class="sxs-lookup"><span data-stu-id="be9f3-150">When offset<2> is used with FC\_CALLBACK, it contains an index in the expression evaluation routine table generated by the compiler.</span></span> <span data-ttu-id="be9f3-151">Die Stub-Nachricht wird an die Evaluierungs Routine übergeben, die dann den Konformitäts Wert berechnet und dem Feld maxCount der Stub-Nachricht zuweist.</span><span class="sxs-lookup"><span data-stu-id="be9f3-151">The stub message is passed to the evaluation routine, which then computes the conformance value and assigns it to the MaxCount field of the stub message.</span></span>

<span data-ttu-id="be9f3-152">Das \_ Feld robuste Flags<2> wurde für Windows 2000 hinzugefügt, um [**/robust**](/windows/desktop/Midl/-robust)zu unterstützen, wie z. b. das Denial-of-Angriff-Feature.</span><span class="sxs-lookup"><span data-stu-id="be9f3-152">The robust\_flags<2> field has been added for Windows 2000 to support [**/robust**](/windows/desktop/Midl/-robust), such as the denial-of-attacks feature.</span></span> <span data-ttu-id="be9f3-153">Die folgenden Flags werden auf dem ersten Byte definiert:</span><span class="sxs-lookup"><span data-stu-id="be9f3-153">The following flags are defined on the first byte:</span></span>

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

<span data-ttu-id="be9f3-154">Das frühe Flag gibt eine frühe und späte Korrelation an.</span><span class="sxs-lookup"><span data-stu-id="be9f3-154">The Early flag indicates early versus late correlation.</span></span> <span data-ttu-id="be9f3-155">Eine frühe Korrelation ist, wenn das Ausdrucks Argument dem beschriebenen Argument vorangestellt ist, z. b. ein size-Argument vor einem großen Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="be9f3-155">An early correlation is when the expression argument precedes the described argument, for example a size argument is before a sized pointer argument.</span></span> <span data-ttu-id="be9f3-156">Eine späte Korrelation ist, wenn das Ausdrucks Argument hinter das verwandte Argument folgt.</span><span class="sxs-lookup"><span data-stu-id="be9f3-156">A late correlation is when the expression argument comes after the related argument.</span></span> <span data-ttu-id="be9f3-157">Die Engine führt sofort eine Validierung der frühen Korrelations Werte durch, die späten Korrelations Werte werden zur Überprüfung gespeichert, nachdem das Marshalling abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="be9f3-157">The engine performs validation of early correlation values right away, the late correlation values are stored for checking after unmarshaling is done.</span></span>

<span data-ttu-id="be9f3-158">Das Split-Flag gibt eine asynchrone Teilung zwischen \[ in \] -und \[ out-Argumenten an \] .</span><span class="sxs-lookup"><span data-stu-id="be9f3-158">The Split flag indicates an async split among \[in\] and \[out\] arguments.</span></span> <span data-ttu-id="be9f3-159">Beispielsweise kann ein size-Argument in sein, \[ \] während der Size-Zeiger \[ nicht mehr angezeigt wird \] .</span><span class="sxs-lookup"><span data-stu-id="be9f3-159">For example, a size argument may be \[in\] while the sized pointer may be \[out\].</span></span> <span data-ttu-id="be9f3-160">Im asynchronen DCOM-Kontext befinden sich diese Argumente in verschiedenen Stapeln, sodass die Engine dies beachten muss.</span><span class="sxs-lookup"><span data-stu-id="be9f3-160">In the DCOM async context, these arguments happen to be on different stacks, so the engine must be aware of this.</span></span>

<span data-ttu-id="be9f3-161">Das isiidis-Flag gibt an, dass die **IID \_ ()** -Korrelation ist.</span><span class="sxs-lookup"><span data-stu-id="be9f3-161">The IsIidIs flag indicates an **iid\_is()** correlation.</span></span> <span data-ttu-id="be9f3-162">Die ndrcomputeconformance-Routine ist so festgelegt, dass Sie einen Zeiger auf IID als Ausdruckswert erhält, aber die Validierungs Routine kann diese Werte nicht vergleichen (Sie sind Zeiger), sodass das Flag angibt, dass die tatsächlichen IIDs verglichen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="be9f3-162">The NdrComputeConformance routine is tricked to obtain a pointer to IID as an expression value, but the validation routine cannot compare such values (they would be pointers) and so the flag indicates that actual IIDs need to be compared.</span></span>

### <a name="variance-description-and-other-array-attributes"></a><span data-ttu-id="be9f3-163">Varianz Beschreibung und andere Array Attribute</span><span class="sxs-lookup"><span data-stu-id="be9f3-163">Variance Description and Other Array Attributes</span></span>

<span data-ttu-id="be9f3-164">Das Feld Format der Varianz Beschreibung ist mit dem Feld für die Übereinstimmungs Beschreibung identisch.</span><span class="sxs-lookup"><span data-stu-id="be9f3-164">The variance description field format is identical to the conformance description field.</span></span> <span data-ttu-id="be9f3-165">Der Unterschied besteht darin, dass ein anderes Stub-Nachrichtenfeld von der NDR-Engine als temporäre Variable verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be9f3-165">The difference is that a different stub message field is used by the NDR engine as a temporary variable.</span></span> <span data-ttu-id="be9f3-166">Im Fall von Varianz Beschreibung ist dies die Länge, die ausgewertet wird, und das entsprechende Feld heißt "actuallength".</span><span class="sxs-lookup"><span data-stu-id="be9f3-166">In the case of variance description, it is the length that is evaluated and the corresponding field is called ActualLength.</span></span>

<span data-ttu-id="be9f3-167">Bei Varianz ist der Start Offset in der Regel 0 (null), und die Engine wird entsprechend optimiert.</span><span class="sxs-lookup"><span data-stu-id="be9f3-167">With variance, the starting offset is typically zero and the engine is tuned accordingly.</span></span> <span data-ttu-id="be9f3-168">Wenn das **erste \_ is ()** -Attribut auf ein unterschiedliches Array angewendet wird, wird ein Rückruf an eine Ausdrucks Auswertungs Routine erzwungen.</span><span class="sxs-lookup"><span data-stu-id="be9f3-168">If the **first\_is()** attribute is applied to a conformant varying array, a callback to an expression evaluation routine is forced.</span></span>

 

 