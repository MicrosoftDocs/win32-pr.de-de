---
title: " if-, elif-, else-und endif-Direktiven"
description: Präprozessordirektiven, die die Kompilierung von Teilen einer Quelldatei steuern.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- if-, elif-, else-und endif-Direktive HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32206232c726f19febf77c3f3270882894a6747
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101659"
---
# <a name="if-elif-else-and-endif-directives"></a><span data-ttu-id="a01d7-104">\#If \# -, elif \# -, else-und \# EndIf-Direktiven</span><span class="sxs-lookup"><span data-stu-id="a01d7-104">\#if, \#elif, \#else, and \#endif Directives</span></span>

<span data-ttu-id="a01d7-105">Präprozessordirektiven, die die Kompilierung von Teilen einer Quelldatei steuern.</span><span class="sxs-lookup"><span data-stu-id="a01d7-105">Preprocessor directives that control compilation of portions of a source file.</span></span>



| <span data-ttu-id="a01d7-106">\#Wenn *ifcondition* ...</span><span class="sxs-lookup"><span data-stu-id="a01d7-106">\#if *ifCondition* ...</span></span>         |
|--------------------------------|
| <span data-ttu-id="a01d7-107">\[\#Elif *elif Condition* ...\]</span><span class="sxs-lookup"><span data-stu-id="a01d7-107">\[\#elif *elifCondition* ...\]</span></span> |
| <span data-ttu-id="a01d7-108">\[\#else...\]</span><span class="sxs-lookup"><span data-stu-id="a01d7-108">\[\#else ...\]</span></span>                 |
| <span data-ttu-id="a01d7-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="a01d7-109">\#endif</span></span>                        |



 

## <a name="parameters"></a><span data-ttu-id="a01d7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a01d7-110">Parameters</span></span>



| <span data-ttu-id="a01d7-111">Element</span><span class="sxs-lookup"><span data-stu-id="a01d7-111">Item</span></span>                                                                                                                                                                                                 | <span data-ttu-id="a01d7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a01d7-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a01d7-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifcondition*</span><span class="sxs-lookup"><span data-stu-id="a01d7-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span></span><br/>                                                                                   | <span data-ttu-id="a01d7-114">Die auszuwertende primäre Bedingung.</span><span class="sxs-lookup"><span data-stu-id="a01d7-114">Primary condition to evaluate.</span></span> <span data-ttu-id="a01d7-115">Wenn dieser Parameter zu einem Wert ungleich 0 (null) ausgewertet wird, wird der gesamte Text zwischen dieser \# if-Direktive und der nächsten Instanz der \# elif-, \# else-oder \# endif-Direktive in der Übersetzungseinheit beibehalten. andernfalls wird der nachfolgende Quellcode nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a01d7-115">If this parameter evaluates to a nonzero value, all text between this \#if directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="a01d7-116">Mit der Bedingung kann der Präprozessoroperator definiert werden, um zu bestimmen, ob eine bestimmte präprozessorkonstante oder ein bestimmtes Makro definiert ist. Diese Verwendung entspricht der Verwendung der [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) -Direktive.</span><span class="sxs-lookup"><span data-stu-id="a01d7-116">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="a01d7-117">Weitere Informationen zu den Werten des Parameters " *ifcondition* " finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="a01d7-117">See the Remarks section for restrictions on the value of the *ifCondition* parameter.</span></span> <br/>                                                                                        |
| <span data-ttu-id="a01d7-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elif Condition* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="a01d7-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[optional\]</span></span> <br/> | <span data-ttu-id="a01d7-119">Andere auszuwertende Bedingung.</span><span class="sxs-lookup"><span data-stu-id="a01d7-119">Other condition to evaluate.</span></span> <span data-ttu-id="a01d7-120">Wenn der *ifcondition* -Parameter und alle vorherigen \# elif-Direktiven NULL ergeben und dieser Parameter zu einem Wert ungleich 0 (null) ausgewertet wird, wird der gesamte Text zwischen dieser \# elif-Direktive und der nächsten Instanz der \# elif-, \# else-oder \# endif-Direktive in der Übersetzungseinheit beibehalten. andernfalls wird der nachfolgende Quellcode nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a01d7-120">If the *ifCondition* parameter and all previous \#elif directives evaluate to zero, and this parameter evaluates to a nonzero value, all text between this \#elif directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="a01d7-121">Mit der Bedingung kann der Präprozessoroperator definiert werden, um zu bestimmen, ob eine bestimmte präprozessorkonstante oder ein bestimmtes Makro definiert ist. Diese Verwendung entspricht der Verwendung der [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) -Direktive.</span><span class="sxs-lookup"><span data-stu-id="a01d7-121">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="a01d7-122">Im Abschnitt "Hinweise" finden Sie Einschränkungen für den Wert des *elilarcondition* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="a01d7-122">See the Remarks section for restrictions on the value of the *elifCondition* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="a01d7-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a01d7-123">Remarks</span></span>

<span data-ttu-id="a01d7-124">Jede \# if-Direktive in einer Quelldatei muss mit einer abschließenden \# endif-Direktive übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a01d7-124">Each \#if directive in a source file must be matched by a closing \#endif directive.</span></span> <span data-ttu-id="a01d7-125">Eine beliebige Anzahl von \# elif-Direktiven kann zwischen der \# if-und der \# endif-Direktive auftreten, aber \# es ist höchstens eine Else-Direktive zulässig.</span><span class="sxs-lookup"><span data-stu-id="a01d7-125">Any number of \#elif directives can appear between the \#if and \#endif directives, but at most one \#else directive is allowed.</span></span> <span data-ttu-id="a01d7-126">Die \# else-Direktive muss, falls vorhanden, die letzte Direktive vor \# EndIf sein.</span><span class="sxs-lookup"><span data-stu-id="a01d7-126">The \#else directive, if present, must be the last directive before \#endif.</span></span> <span data-ttu-id="a01d7-127">Bedingte Kompilierungs Direktiven, die in include-Dateien enthalten sind, müssen die gleichen Bedingungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="a01d7-127">Conditional-compilation directives contained in include files must satisfy the same conditions.</span></span>

<span data-ttu-id="a01d7-128">Die \# if-, \# elif \# -, else-und \# EndIf-Direktiven können in den Textteilen anderer \# if-Direktiven geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="a01d7-128">The \#if, \#elif, \#else, and \#endif directives can nest in the text portions of other \#if directives.</span></span> <span data-ttu-id="a01d7-129">Jede geschsted \# else-, \# elif-oder \# endif-Direktive gehört der nächstgelegenen vorangehenden \# if-Direktive an.</span><span class="sxs-lookup"><span data-stu-id="a01d7-129">Each nested \#else, \#elif, or \#endif directive belongs to the closest preceding \#if directive.</span></span>

<span data-ttu-id="a01d7-130">Wenn keine Bedingungen zu einem Wert ungleich 0 (null) ausgewertet werden, wählt der Präprozessor den TextBlock nach der \# else-Direktive aus.</span><span class="sxs-lookup"><span data-stu-id="a01d7-130">If no conditions evaluate to a nonzero value, the preprocessor selects the text block after the \#else directive.</span></span> <span data-ttu-id="a01d7-131">Wenn die \# else-Klausel ausgelassen wird und keine Bedingungen zu einem Wert ungleich 0 (null) ausgewertet werden, wird kein TextBlock ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a01d7-131">If the \#else clause is omitted and no conditions evaluate to a nonzero value, no text block is selected.</span></span>

<span data-ttu-id="a01d7-132">Die Parameter " *ifcondition* " und " *elimode Condition* " erfüllen viele der folgenden Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="a01d7-132">The *ifCondition* and *elifCondition* parameters much meet the following requirements:</span></span>

-   <span data-ttu-id="a01d7-133">Ausdrücke für die bedingte Kompilierung werden als [**signierte lange**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) Werte behandelt, und diese Ausdrücke werden mit denselben Regeln wie Ausdrücke in C++ ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="a01d7-133">Conditional compilation expressions are treated as [**signed long**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) values, and these expressions are evaluated using the same rules as expressions in C++.</span></span>
-   <span data-ttu-id="a01d7-134">Ausdrücke müssen einen ganzzahligen Typ aufweisen und können nur ganzzahlige Konstanten und Zeichenkonstanten und den defined -Operator umfassen.</span><span class="sxs-lookup"><span data-stu-id="a01d7-134">Expressions must have integral type and can include only integer constants, character constants, and the defined operator.</span></span>
-   <span data-ttu-id="a01d7-135">Ausdrücke können nicht **sizeof** oder einen Typumwandlungs Operator verwenden.</span><span class="sxs-lookup"><span data-stu-id="a01d7-135">Expressions cannot use **sizeof** or a type-cast operator.</span></span>
-   <span data-ttu-id="a01d7-136">Die Zielumgebung ist möglicherweise nicht in der Lage, alle Bereiche von ganzen Zahlen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="a01d7-136">The target environment may not be able to represent all ranges of integers.</span></span>
-   <span data-ttu-id="a01d7-137">Die Übersetzung stellt den Typ " [**int**](/windows/desktop/WinProg/windows-data-types) " mit dem Typ " **Long**" und " [**Ganzzahl ohne Vorzeichen int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) " gleich " **Ganzzahl ohne Vorzeichen long**" dar.</span><span class="sxs-lookup"><span data-stu-id="a01d7-137">The translation represents type [**int**](/windows/desktop/WinProg/windows-data-types) the same as type **long**, and [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) the same as **unsigned long**.</span></span>
-   <span data-ttu-id="a01d7-138">Das Konvertierungsprogramm kann Zeichenkonstanten in einen Satz von Codewerten übersetzen, die sich vom Satz für die Zielumgebung unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a01d7-138">The translator can translate character constants to a set of code values different from the set for the target environment.</span></span> <span data-ttu-id="a01d7-139">Um die Eigenschaften der Zielumgebung zu bestimmen, überprüfen Sie die Werte der Makros von LIMITS.H in einer für die Zielumgebung erstellten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a01d7-139">To determine the properties of the target environment, check values of macros from LIMITS.H in an application built for the target environment.</span></span>
-   <span data-ttu-id="a01d7-140">Der Ausdruck darf keine Umgebungsabfragen durchführen und muss von Implementierungsdetails auf dem Zielcomputer isoliert bleiben.</span><span class="sxs-lookup"><span data-stu-id="a01d7-140">The expression must not perform any environmental inquiries and must remain insulated from implementation details on the target computer.</span></span>

## <a name="examples"></a><span data-ttu-id="a01d7-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a01d7-141">Examples</span></span>

<span data-ttu-id="a01d7-142">Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie Präprozessordirektiven für die bedingte Kompilierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a01d7-142">This section contains examples that demonstrate how to use conditional compilation preprocessor directives.</span></span>

### <a name="use-of-the-defined-operator"></a><span data-ttu-id="a01d7-143">Verwendung des definierten Operators</span><span class="sxs-lookup"><span data-stu-id="a01d7-143">Use of the defined operator</span></span>

<span data-ttu-id="a01d7-144">Das folgende Beispiel zeigt die Verwendung des definierten-Operators.</span><span class="sxs-lookup"><span data-stu-id="a01d7-144">The following example shows the use of the defined operator.</span></span> <span data-ttu-id="a01d7-145">Wenn das bezeichnerguthaben definiert ist, wird der-Befehl der **Credit** -Funktion kompiliert.</span><span class="sxs-lookup"><span data-stu-id="a01d7-145">If the identifier CREDIT is defined, the call to the **credit** function is compiled.</span></span> <span data-ttu-id="a01d7-146">Wenn der bezeichnerkennung definiert ist, wird der aufrufswert der **debitfunktion** kompiliert.</span><span class="sxs-lookup"><span data-stu-id="a01d7-146">If the identifier DEBIT is defined, the call to the **debit** function is compiled.</span></span> <span data-ttu-id="a01d7-147">Wenn kein Bezeichner definiert ist, wird der-Befehl der **Printerror** -Funktion kompiliert.</span><span class="sxs-lookup"><span data-stu-id="a01d7-147">If neither identifier is defined, the call to the **printerror** function is compiled.</span></span> <span data-ttu-id="a01d7-148">Beachten Sie, dass "Guthaben" und "Guthaben" unterschiedliche Bezeichner in C und C++ sind, da sich ihre Fälle unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a01d7-148">Note that "CREDIT" and "credit" are distinct identifiers in C and C++ because their cases are different.</span></span>


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a><span data-ttu-id="a01d7-149">Verwendung von nsted \# if-Direktiven</span><span class="sxs-lookup"><span data-stu-id="a01d7-149">Use of nested \#if directives</span></span>

<span data-ttu-id="a01d7-150">Das folgende Beispiel zeigt, wie if-Direktiven geschachtelt \# werden.</span><span class="sxs-lookup"><span data-stu-id="a01d7-150">The following example shows how to nest \#if directives.</span></span> <span data-ttu-id="a01d7-151">In diesem Beispiel wird davon ausgegangen, dass bereits eine symbolische Konstante mit dem Namen "DLEVEL" definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a01d7-151">This example assumes that a symbolic constant named DLEVEL has been previously defined.</span></span> <span data-ttu-id="a01d7-152">Die \# elif-und \# else-Direktiven werden verwendet, um eine von vier Optionen basierend auf dem Wert von DLEVEL zu treffen.</span><span class="sxs-lookup"><span data-stu-id="a01d7-152">The \#elif and \#else directives are used to make one of four choices, based on the value of DLEVEL.</span></span> <span data-ttu-id="a01d7-153">Der Konstante Stapel ist abhängig von der Definition von DLEVEL auf 0, 100 oder 200 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a01d7-153">The constant STACK is set to 0, 100, or 200, depending on the definition of DLEVEL.</span></span> <span data-ttu-id="a01d7-154">Wenn DLEVEL größer als 5 ist, wird der Stapel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a01d7-154">If DLEVEL is greater than 5, then STACK is not defined.</span></span>


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a><span data-ttu-id="a01d7-155">Verwenden zum Einschließen von Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a01d7-155">Use for including header files</span></span>

<span data-ttu-id="a01d7-156">Eine übliche Verwendung für die bedingte Kompilierung besteht darin, mehrere Inklusionen derselben Headerdatei zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="a01d7-156">A common use for conditional compilation is to prevent multiple inclusions of the same header file.</span></span> <span data-ttu-id="a01d7-157">In C++, in denen Klassen häufig in Header Dateien definiert werden, können Konstrukte für die bedingte Kompilierung verwendet werden, um mehrere Definitionen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="a01d7-157">In C++, where classes are often defined in header files, conditional compilation constructs can be used to prevent multiple definitions.</span></span> <span data-ttu-id="a01d7-158">Im folgenden Beispiel wird bestimmt, ob das symbolische Konstante Beispiel \_ H definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a01d7-158">The following example determines whether the symbolic constant EXAMPLE\_H is defined.</span></span> <span data-ttu-id="a01d7-159">Wenn dies der Fall ist, wurde die Datei bereits eingeschlossen und muss nicht erneut verarbeitet werden. Wenn dies nicht der Wert ist, wird das Konstante Beispiel \_ H definiert, um das Beispiel anzuzeigen. H wurde bereits verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a01d7-159">If so, the file has already been included and does not need to be reprocessed; if not, the constant EXAMPLE\_H is defined to indicate that EXAMPLE.H has already been processed.</span></span>


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a><span data-ttu-id="a01d7-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a01d7-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a01d7-161">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a01d7-161">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

