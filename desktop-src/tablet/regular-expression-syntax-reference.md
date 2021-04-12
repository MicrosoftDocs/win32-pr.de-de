---
description: Sie können benutzerdefinierte Eingabe Bereiche definieren und zuweisen, indem Sie die Handschrift Syntax für reguläre Ausdrücke verwenden, die von einigen der Handschrift Erkennungsformen von Microsoft interpretiert wird.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Syntax Referenz für reguläre Ausdrücke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218933"
---
# <a name="regular-expression-syntax-reference"></a><span data-ttu-id="08861-103">Syntax Referenz für reguläre Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="08861-103">Regular Expression Syntax Reference</span></span>

<span data-ttu-id="08861-104">Sie können benutzerdefinierte Eingabe Bereiche definieren und zuweisen, indem Sie die Handschrift Syntax für reguläre Ausdrücke verwenden, die von einigen der Handschrift Erkennungsformen von Microsoft interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="08861-104">You can define and assign custom input scopes using the handwriting regular expression syntax that is understood by some of the Microsoft handwriting recognizers.</span></span> <span data-ttu-id="08861-105">Die Syntax ist eine Teilmenge der [sprach Implementierung für reguläre Ausdrücke](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) in der .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="08861-105">The syntax is a subset of the [Regular Expression Language Implementation](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) in the .NET Framework.</span></span>

<span data-ttu-id="08861-106">Es gibt einige Unterschiede bei der Verwendung von Handschrift regulären Ausdrücken und der Art und Weise, wie die anderen Typen von regulären Ausdrücken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08861-106">There are some differences in the way that handwriting regular expressions are used and the way the other types of regular expressions are used.</span></span> <span data-ttu-id="08861-107">Die Handschrift Syntax wird verwendet, um eine exakte Zeichenfolge anzugeben, die mit der Erkennungs-Engine und nicht mit einer Teil Zeichenfolge abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="08861-107">The handwriting syntax is used to specify an exact string that will be matched by the recognition engine and not a sub-string.</span></span> <span data-ttu-id="08861-108">Beispielsweise würde der reguläre Ausdruck s ( \[ a-z \] +) p Übereinstimmungen für "Suppe", "Ende", "inStep" und "esophagus" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="08861-108">For example, the regular expression s(\[a-z\]+)p would return matches for "soup", "stop", "instep", and "esophagus".</span></span> <span data-ttu-id="08861-109">Ein entsprechender Handschrift regulärer Ausdruck, wie z. b. s (! is \_ OneChar) + p, würde z. b. "Suppe" und "beenden", aber nicht "inStep" und "esophagus" entsprechen.</span><span class="sxs-lookup"><span data-stu-id="08861-109">Whereas, an equivalent handwriting regular expression such as s(!IS\_ONECHAR)+p would match "soup" and "stop", but not "instep" and "esophagus".</span></span>

<span data-ttu-id="08861-110">Reguläre Ausdrücke von Handschrift unterstützen keine nicht unterbrechende Leerzeichen in regulären Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="08861-110">Handwriting regular expressions do not support non-breaking spaces within regular expressions.</span></span> <span data-ttu-id="08861-111">Das heißt, Sie können die Entität "nbsp" nicht innerhalb eines regulären Handschrift Ausdrucks verwenden.</span><span class="sxs-lookup"><span data-stu-id="08861-111">That is, you cannot use the "nbsp" entity within a handwriting regular expression.</span></span>

<span data-ttu-id="08861-112">In den folgenden Abschnitten wird die Syntax ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="08861-112">The following sections describe the syntax in more detail.</span></span>

## <a name="valid-operators"></a><span data-ttu-id="08861-113">Gültige Operatoren</span><span class="sxs-lookup"><span data-stu-id="08861-113">Valid Operators</span></span>

<span data-ttu-id="08861-114">Die folgenden Operatoren sind für das Erstellen regulärer Ausdrücke zum Definieren von Eingabe Bereichen für Handschrift Erkennungsformen gültig.</span><span class="sxs-lookup"><span data-stu-id="08861-114">The following operators are valid for creating regular expressions to define input scopes for handwriting recognizers.</span></span>



| <span data-ttu-id="08861-115">Operator</span><span class="sxs-lookup"><span data-stu-id="08861-115">Operator</span></span>      | <span data-ttu-id="08861-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08861-116">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | <span data-ttu-id="08861-117">Der unäre Postfix-Operator, der 0 (null) oder mehr Vorkommen des Operanden bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="08861-117">Postfix unary operator signifying zero or more occurrences of the operand.</span></span><br/> |
| +<br/>  | <span data-ttu-id="08861-118">Der unäre Postfix-Operator, der ein oder mehrere Vorkommen des Operanden bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="08861-118">Postfix unary operator signifying one or more occurrences of the operand.</span></span><br/>  |
| <span data-ttu-id="08861-119">?</span><span class="sxs-lookup"><span data-stu-id="08861-119">?</span></span><br/>  | <span data-ttu-id="08861-120">Der unäre Postfix-Operator gibt NULL oder ein Vorkommen des Operanden an.</span><span class="sxs-lookup"><span data-stu-id="08861-120">Postfix unary operator signifying zero or one occurrence of the operand.</span></span><br/>   |
| \|<br/> | <span data-ttu-id="08861-121">Binärer Infix-Operator, der "or" bedeutet.</span><span class="sxs-lookup"><span data-stu-id="08861-121">Binary infix operator meaning "or".</span></span><br/>                                        |
| <span data-ttu-id="08861-122">()</span><span class="sxs-lookup"><span data-stu-id="08861-122">()</span></span><br/> | <span data-ttu-id="08861-123">Wird zum Gruppieren von Elementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="08861-123">Used to group items.</span></span><br/>                                                       |



 

<span data-ttu-id="08861-124">Die Microsoft-Implementierung von regulären Ausdrücken für Handschrift Erkennungs Tools ermöglicht wiederholte Anwendungen von Postfix-unären Operatoren.</span><span class="sxs-lookup"><span data-stu-id="08861-124">The Microsoft implementation of regular expressions for handwriting recognizers allows repeated applications of postfix unary operators.</span></span> <span data-ttu-id="08861-125">Beispiel: a \* \* = (a \* ) \* = a \* , b?</span><span class="sxs-lookup"><span data-stu-id="08861-125">For example, a\*\* = (a\*)\* = a\*, b??</span></span> <span data-ttu-id="08861-126">= (b?)?</span><span class="sxs-lookup"><span data-stu-id="08861-126">= (b?)?</span></span> <span data-ttu-id="08861-127">= b?</span><span class="sxs-lookup"><span data-stu-id="08861-127">= b?.</span></span> <span data-ttu-id="08861-128">Sie können auch nicht aufeinander folgende Wiederholungen zulassen, z. b \* .: a? \* = ((a \* )?) \* = (a \* ) \* = a \* .</span><span class="sxs-lookup"><span data-stu-id="08861-128">They also allow non-consecutive repetitions, for example: a\*?\* = ((a\*)?)\* = (a\*)\* = a\*.</span></span> <span data-ttu-id="08861-129">Dies unterscheidet sich von .NET Framework regulären Ausdrücken, die nur das zulassen?</span><span class="sxs-lookup"><span data-stu-id="08861-129">This is different from .NET Framework regular expressions, which only allow the ?</span></span> <span data-ttu-id="08861-130">Operator, der wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08861-130">operator to be repeated.</span></span>

<span data-ttu-id="08861-131">Ein weiterer Unterschied von .NET Framework regulären Ausdrücken ist, dass reguläre Handschrift Ausdrücke keinen leeren Ausdruck unterstützen, der mit einem leeren paar Klammern () gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="08861-131">Another difference from .NET Framework regular expressions is that handwriting regular expressions do not support an empty expression designated with an empty pair of parentheses, ().</span></span>

> [!Note]  
> <span data-ttu-id="08861-132">Für reguläre Handschrift Ausdrücke werden nur Zeichen in der 1252-Codepage unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08861-132">Only characters in the 1252 codepage are supported for handwriting regular expressions.</span></span>

 

## <a name="using-input-scopes"></a><span data-ttu-id="08861-133">Verwenden von Eingabe Bereichen</span><span class="sxs-lookup"><span data-stu-id="08861-133">Using Input Scopes</span></span>

<span data-ttu-id="08861-134">Sie können auch den Satz regulärer Eingabe Bereiche verwenden, die als Teil der [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) -Funktion in ihren regulären Ausdrücken definiert sind.</span><span class="sxs-lookup"><span data-stu-id="08861-134">You can also use the set of regular input scopes that are defined as part of the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) function in your regular expressions.</span></span> <span data-ttu-id="08861-135">Der Wert für month (numerisch) lautet z. b \_ . "Date \_ Month".</span><span class="sxs-lookup"><span data-stu-id="08861-135">For example, the value for Month (numerical) is IS\_DATE\_MONTH.</span></span> <span data-ttu-id="08861-136">Die Syntax zum Angeben eines Eingabe Bereichs als Teil eines regulären Ausdrucks besteht darin, dem Enumerationswert des Eingabe Bereichs eine öffnende Klammer und ein Ausrufezeichen (! und eine schließende Klammer) am Ende vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="08861-136">The syntax for specifying an input scope as part of a regular expression is to prepend the input scope enumerated value with an open parenthesis and an exclamation point, (!, and place a closing parenthesis, ), on the end.</span></span> <span data-ttu-id="08861-137">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="08861-137">For example:</span></span>

<span data-ttu-id="08861-138">(! Ist \_ Datum/ \_ Monat)</span><span class="sxs-lookup"><span data-stu-id="08861-138">(!IS\_DATE\_MONTH)</span></span>

<span data-ttu-id="08861-139">Wenn Sie den \_ Standardeingabe Bereich der-Klasse mit einem beliebigen anderen Eingabebereich kombinieren, besteht der Effekt darin, dass die Erkennung entweder jeden einzelnen Ausdruck, der vom Standard Sprachmodell unterstützt wird (z. b. ein Wort aus dem System Wörterbuch oder einem Datum), mit oder ohne Interpunktions Zeichen oder einen beliebigen Wert zurückgeben kann, der dem restlichen regulären Ausdruck entspricht.</span><span class="sxs-lookup"><span data-stu-id="08861-139">If you combine the IS\_DEFAULT input scope by ORing it with any other input scope, the effect is that the recognizer can return either any single expression that the default language model supports (for example, one word from the system dictionary or a date) with or without punctuation, or any value that meets the rest of the regular expression passed in to the recognizer.</span></span>

> [!Note]  
> <span data-ttu-id="08861-140">Die folgenden [**Member von "**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) " in regulären Ausdrücken werden nicht unterstützt: ist " \_ PhraseList", " \_ RegularExpression", " \_ SRGS", "XML" \_ .</span><span class="sxs-lookup"><span data-stu-id="08861-140">The following members of [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) are not supported in regular expressions: IS\_PHRASELIST, IS\_REGULAREXPRESSION, IS\_SRGS, IS\_XML.</span></span>

 

## <a name="unsupported-operators"></a><span data-ttu-id="08861-141">Nicht unterstützte Operatoren</span><span class="sxs-lookup"><span data-stu-id="08861-141">Unsupported Operators</span></span>

<span data-ttu-id="08861-142">Die folgenden Operatoren für reguläre Ausdrücke werden beim Erstellen von regulären Handschrift Ausdrücken nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08861-142">The following regular expression operators are not supported when creating handwriting regular expressions.</span></span>



| <span data-ttu-id="08861-143">Operator</span><span class="sxs-lookup"><span data-stu-id="08861-143">Operator</span></span>                                     | <span data-ttu-id="08861-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08861-144">Description</span></span>                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="08861-145">.</span><span class="sxs-lookup"><span data-stu-id="08861-145">.</span></span><br/>                                 | <span data-ttu-id="08861-146">Zeit Zeichen.</span><span class="sxs-lookup"><span data-stu-id="08861-146">Period character.</span></span><br/>                                        |
| \[\]<br/>                              | <span data-ttu-id="08861-147">Eckige Klammern.</span><span class="sxs-lookup"><span data-stu-id="08861-147">Square brackets.</span></span> <span data-ttu-id="08861-148">Klammer für das Gruppieren von Elementen verwenden.</span><span class="sxs-lookup"><span data-stu-id="08861-148">Use parenthesis for grouping items.</span></span><br/>     |
| {}<br/>                                | <span data-ttu-id="08861-149">Geschweifte Klammern.</span><span class="sxs-lookup"><span data-stu-id="08861-149">Curly brackets.</span></span><br/>                                          |
| <span data-ttu-id="08861-150">(?\# Kommentar) und \# \[ Kommentar\]</span><span class="sxs-lookup"><span data-stu-id="08861-150">(?\# comment) and \#\[ comment \]</span></span><br/> | <span data-ttu-id="08861-151">Kommentare.</span><span class="sxs-lookup"><span data-stu-id="08861-151">Comments.</span></span><br/>                                                |
| $<br/>                                 | <span data-ttu-id="08861-152">Dollar Zeichen.</span><span class="sxs-lookup"><span data-stu-id="08861-152">Dollar sign character.</span></span><br/>                                   |
| ^<br/>                                 | <span data-ttu-id="08861-153">Caretzeichen.</span><span class="sxs-lookup"><span data-stu-id="08861-153">Caret character.</span></span><br/>                                         |
| -<br/>                                 | <span data-ttu-id="08861-154">Bindestrich.</span><span class="sxs-lookup"><span data-stu-id="08861-154">Dash character.</span></span> <span data-ttu-id="08861-155">Muss oder ( \| ) alle Sätze von Elementen kombinieren.</span><span class="sxs-lookup"><span data-stu-id="08861-155">Must OR (\|) together all sets of items.</span></span><br/> |



 

## <a name="escaping-characters"></a><span data-ttu-id="08861-156">Umwandeln von Zeichen mit Escapezeichen</span><span class="sxs-lookup"><span data-stu-id="08861-156">Escaping Characters</span></span>

<span data-ttu-id="08861-157">Gewöhnliche Zeichen, die nicht die in der folgenden Tabelle aufgeführten sind, stimmen mit sich selbst.</span><span class="sxs-lookup"><span data-stu-id="08861-157">Ordinary characters, other than the ones in the following table, match themselves.</span></span> <span data-ttu-id="08861-158">Das heißt, ein "a" in einem regulären Ausdruck gibt an, dass die Eingabe einem "a" entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="08861-158">That is, an "a" in a regular expression specifies that input should match an "a".</span></span>

<span data-ttu-id="08861-159">Ein weiterer bedeutender Unterschied beim Schreiben regulärer Ausdrücke ist, dass Sie nur eine begrenzte Anzahl von Zeichen in einem regulären Ausdruck mit Escapezeichen versehen können.</span><span class="sxs-lookup"><span data-stu-id="08861-159">Another significant difference in writing handwriting regular expressions is that you can only escape a limited set of characters within a regular expression.</span></span> <span data-ttu-id="08861-160">In der folgenden Tabelle werden die zulässigen Zeichen, die mit Escapezeichen versehen werden können, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="08861-160">The following table outlines the allowed set of characters that can be escaped.</span></span> <span data-ttu-id="08861-161">Jeder andere Versuch, ein Zeichen mit Escapezeichen zu versehen, führt zu einem Fehler, der von der Erkennung ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="08861-161">Any other attempt to escape a character will result in an error being thrown by the recognizer.</span></span>



| <span data-ttu-id="08861-162">Zeichen</span><span class="sxs-lookup"><span data-stu-id="08861-162">Character</span></span>       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| <span data-ttu-id="08861-163">\\?</span><span class="sxs-lookup"><span data-stu-id="08861-163">\\?</span></span><br/>  |
| <span data-ttu-id="08861-164">\\(</span><span class="sxs-lookup"><span data-stu-id="08861-164">\\(</span></span><br/>  |
| <span data-ttu-id="08861-165">\\)</span><span class="sxs-lookup"><span data-stu-id="08861-165">\\)</span></span><br/>  |
| \\\|<br/> |
| \\\\<br/> |
| <span data-ttu-id="08861-166">\\!</span><span class="sxs-lookup"><span data-stu-id="08861-166">\\!</span></span><br/>  |
| <span data-ttu-id="08861-167">\\.</span><span class="sxs-lookup"><span data-stu-id="08861-167">\\.</span></span><br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| <span data-ttu-id="08861-168">\\{</span><span class="sxs-lookup"><span data-stu-id="08861-168">\\{</span></span><br/>  |
| <span data-ttu-id="08861-169">\\}</span><span class="sxs-lookup"><span data-stu-id="08861-169">\\}</span></span><br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 