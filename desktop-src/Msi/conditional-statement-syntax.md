---
description: In diesem Abschnitt wird die Syntax von bedingten Anweisungen beschrieben, die von der msievaluatecondition-Funktion und den Aktions Sequenz Tabellen verwendet werden. Weitere Informationen finden Sie unter Beispiele für bedingte Anweisungs Syntax.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Syntax der bedingten Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0548a71756faff654bfe2b49e14c0581a6248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864408"
---
# <a name="conditional-statement-syntax"></a><span data-ttu-id="59a76-104">Syntax der bedingten Anweisung</span><span class="sxs-lookup"><span data-stu-id="59a76-104">Conditional Statement Syntax</span></span>

<span data-ttu-id="59a76-105">In diesem Abschnitt wird die Syntax von bedingten Anweisungen beschrieben, die von der [**msievaluatecondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) -Funktion und den Aktions [Sequenz Tabellen](using-a-sequence-table.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59a76-105">This section describes the syntax of conditional statements used by the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function and the action [sequence tables](using-a-sequence-table.md).</span></span> <span data-ttu-id="59a76-106">Weitere Informationen finden Sie unter [Beispiele für bedingte Anweisungs Syntax](examples-of-conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="59a76-106">For more information, see, [Examples of Conditional Statement Syntax](examples-of-conditional-statement-syntax.md).</span></span>

## <a name="summary-of-conditional-statement-syntax"></a><span data-ttu-id="59a76-107">Zusammenfassung der Syntax der bedingten Anweisung</span><span class="sxs-lookup"><span data-stu-id="59a76-107">Summary of Conditional Statement Syntax</span></span>

<span data-ttu-id="59a76-108">In dieser Tabelle und in der folgenden Liste wird die Syntax zusammengefasst, die in bedingten Ausdrücken verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="59a76-108">This table and the following list summarize the syntax to use in conditional expressions.</span></span>



| <span data-ttu-id="59a76-109">Element</span><span class="sxs-lookup"><span data-stu-id="59a76-109">Item</span></span>                | <span data-ttu-id="59a76-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="59a76-110">Syntax</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59a76-111">value</span><span class="sxs-lookup"><span data-stu-id="59a76-111">value</span></span>               | <span data-ttu-id="59a76-112">Symbol \| Literale \| Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="59a76-112">symbol \| literal \| integer</span></span>                                                                                    |
| <span data-ttu-id="59a76-113">Vergleichs Operator</span><span class="sxs-lookup"><span data-stu-id="59a76-113">comparison-operator</span></span> | < \| > \| <= \| >= \| = \| <>                                                                 |
| <span data-ttu-id="59a76-114">Begriff</span><span class="sxs-lookup"><span data-stu-id="59a76-114">term</span></span>                | <span data-ttu-id="59a76-115">Wert \| Vergleichswert-Operator Wert \| (Ausdruck)\|</span><span class="sxs-lookup"><span data-stu-id="59a76-115">value \| value comparison-operator value \| ( expression )\|</span></span>                                                    |
| <span data-ttu-id="59a76-116">Boolescher Faktor</span><span class="sxs-lookup"><span data-stu-id="59a76-116">Boolean-factor</span></span>      | <span data-ttu-id="59a76-117">Begriff " \| **nicht** Begriff"</span><span class="sxs-lookup"><span data-stu-id="59a76-117">term \| **NOT** term</span></span>                                                                                            |
| <span data-ttu-id="59a76-118">Boolescher Ausdruck</span><span class="sxs-lookup"><span data-stu-id="59a76-118">Boolean-term</span></span>        | <span data-ttu-id="59a76-119">Boolescher Faktor \| **und** Begriff "boolescher Faktor"</span><span class="sxs-lookup"><span data-stu-id="59a76-119">Boolean-factor \| Boolean-factor **AND** term</span></span>                                                                   |
| <span data-ttu-id="59a76-120">expression</span><span class="sxs-lookup"><span data-stu-id="59a76-120">expression</span></span>          | <span data-ttu-id="59a76-121">Boolescher Ausdruck ( \| boolescher Ausdruck **oder** Ausdruck)</span><span class="sxs-lookup"><span data-stu-id="59a76-121">Boolean-term \| Boolean-term **OR** expression</span></span>                                                                  |
| <span data-ttu-id="59a76-122">Symbol</span><span class="sxs-lookup"><span data-stu-id="59a76-122">symbol</span></span>              | <span data-ttu-id="59a76-123">Eigenschaft " \| % Environment-Variable \| $Component-Action \| ? Component-State \| &Feature-Action \| ! Feature-State"</span><span class="sxs-lookup"><span data-stu-id="59a76-123">property \| %environment-variable \| $component-action \| ?component-state \| &feature-action \| !feature-state</span></span> |



 

-   <span data-ttu-id="59a76-124">Bei Symbol Namen und Werten wird Groß-/Kleinschreibung beachtet</span><span class="sxs-lookup"><span data-stu-id="59a76-124">Symbol names and values are case sensitive.</span></span>
-   <span data-ttu-id="59a76-125">Bei Umgebungsvariablen Namen wird Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="59a76-125">Environment variable names are not case sensitive.</span></span>
-   <span data-ttu-id="59a76-126">LiteralText muss in Anführungszeichen ("Text") eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="59a76-126">Literal text must be enclosed between quotation marks ("text").</span></span>
    > [!Note]  
    > <span data-ttu-id="59a76-127">LiteralText mit Anführungszeichen kann nicht in Bedingungs Anweisungen verwendet werden, da es kein Escapezeichen für Anführungszeichen innerhalb von Literaltext gibt.</span><span class="sxs-lookup"><span data-stu-id="59a76-127">Literal text containing quotation marks cannot be used in conditional statements because there is no escape character for quotation marks inside literal text.</span></span> <span data-ttu-id="59a76-128">Um einen Vergleich mit Literaltext mit Anführungszeichen durchzuführen, sollte der Literaltext in eine Eigenschaft eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="59a76-128">To do a comparison against literal text containing quotation marks, the literal text should be put in a property.</span></span> <span data-ttu-id="59a76-129">Um z. b. zu überprüfen, ob die ServerName-Eigenschaft keine Anführungszeichen enthält, definieren Sie eine Eigenschaft mit dem Namen Anführungszeichen in der [Eigenschaften Tabelle](property-table.md) mit dem Wert "", und ändern Sie die Bedingung in Not Servername><Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="59a76-129">For example, to verify that the SERVERNAME property does not contain any quotation marks, define a property called QUOTES in the [Property table](property-table.md) with a value of " and change the condition to NOT SERVERNAME><QUOTES.</span></span>

     

-   <span data-ttu-id="59a76-130">Nicht vorhandene Eigenschaftswerte werden als leere Zeichen folgen behandelt.</span><span class="sxs-lookup"><span data-stu-id="59a76-130">Nonexistent property values are treated as empty strings.</span></span>
-   <span data-ttu-id="59a76-131">Numerische Gleit Komma Werte werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="59a76-131">Floating point numeric values are not supported.</span></span>
-   <span data-ttu-id="59a76-132">Operatoren und Rangfolge sind identisch mit denen in den Sprachen "Basic" und "SQL".</span><span class="sxs-lookup"><span data-stu-id="59a76-132">Operators and precedence are the same as in the BASIC and SQL languages.</span></span>
-   <span data-ttu-id="59a76-133">Arithmetische Operatoren werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="59a76-133">Arithmetic operators are not supported.</span></span>
-   <span data-ttu-id="59a76-134">Klammern können zum Überschreiben der Operator Rangfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59a76-134">Parentheses can be used to override operator precedence.</span></span>
-   <span data-ttu-id="59a76-135">Bei Operatoren wird die Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="59a76-135">Operators are not case sensitive.</span></span>
-   <span data-ttu-id="59a76-136">Bei Zeichen folgen vergleichen führt eine Tilde, die dem Operator vorangestellt ist, einen Vergleich durch, bei dem die Groß-/Kleinschreibung nicht beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="59a76-136">For string comparisons, a tilde "~" prefixed to the operator performs a comparison that is not case sensitive.</span></span>
-   <span data-ttu-id="59a76-137">Der Vergleich einer Ganzzahl mit einer Zeichenfolge oder einem Eigenschafts Wert, der nicht in eine ganze Zahl konvertiert werden kann, ist immer **msievaluateconditionfalse**, mit Ausnahme des Vergleichs Operators "<>", der " **msievaluateconditiontrue**" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="59a76-137">Comparison of an integer with a string or property value that cannot be converted to an integer is always **msiEvaluateConditionFalse**, except for the comparison operator "<>", which returns **msiEvaluateConditionTrue**.</span></span>

## <a name="access-prefixes"></a><span data-ttu-id="59a76-138">Zugriffs Präfixe</span><span class="sxs-lookup"><span data-stu-id="59a76-138">Access Prefixes</span></span>

<span data-ttu-id="59a76-139">In der folgenden Tabelle sind die Präfixe aufgeführt, die für den Zugriff auf verschiedene System-und Installerinformationen zur Verwendung in bedingten Ausdrücken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59a76-139">The following table shows the prefixes to use to access various system and installer information for use in conditional expressions.</span></span>



| <span data-ttu-id="59a76-140">Symboltyp</span><span class="sxs-lookup"><span data-stu-id="59a76-140">Symbol type</span></span>          | <span data-ttu-id="59a76-141">Präfix</span><span class="sxs-lookup"><span data-stu-id="59a76-141">Prefix</span></span> | <span data-ttu-id="59a76-142">Wert</span><span class="sxs-lookup"><span data-stu-id="59a76-142">Value</span></span>                                                     |
|----------------------|--------|-----------------------------------------------------------|
| <span data-ttu-id="59a76-143">Installereigenschaft</span><span class="sxs-lookup"><span data-stu-id="59a76-143">Installer property</span></span>   | <span data-ttu-id="59a76-144">(none)</span><span class="sxs-lookup"><span data-stu-id="59a76-144">(none)</span></span> | <span data-ttu-id="59a76-145">Der Wert der Eigenschaften Tabelle ([Property](property-table.md)).</span><span class="sxs-lookup"><span data-stu-id="59a76-145">Value of property ([Property](property-table.md)) table.</span></span> |
| <span data-ttu-id="59a76-146">Umgebungsvariable</span><span class="sxs-lookup"><span data-stu-id="59a76-146">Environment variable</span></span> | %      | <span data-ttu-id="59a76-147">Wert der Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="59a76-147">Value of environment variable.</span></span>                            |
| <span data-ttu-id="59a76-148">Komponenten Tabellenschlüssel</span><span class="sxs-lookup"><span data-stu-id="59a76-148">Component table key</span></span>  | $      | <span data-ttu-id="59a76-149">Der Aktionszustand der Komponente.</span><span class="sxs-lookup"><span data-stu-id="59a76-149">Action state of the component.</span></span>                            |
| <span data-ttu-id="59a76-150">Komponenten Tabellenschlüssel</span><span class="sxs-lookup"><span data-stu-id="59a76-150">Component table key</span></span>  | <span data-ttu-id="59a76-151">?</span><span class="sxs-lookup"><span data-stu-id="59a76-151">?</span></span>      | <span data-ttu-id="59a76-152">Installierter Status der Komponente.</span><span class="sxs-lookup"><span data-stu-id="59a76-152">Installed state of the component.</span></span>                         |
| <span data-ttu-id="59a76-153">Funktionstabellen Schlüssel</span><span class="sxs-lookup"><span data-stu-id="59a76-153">Feature table key</span></span>    | &      | <span data-ttu-id="59a76-154">Der Aktionszustand des Features.</span><span class="sxs-lookup"><span data-stu-id="59a76-154">Action state of the feature.</span></span>                              |
| <span data-ttu-id="59a76-155">Funktionstabellen Schlüssel</span><span class="sxs-lookup"><span data-stu-id="59a76-155">Feature table key</span></span>    | <span data-ttu-id="59a76-156">!</span><span class="sxs-lookup"><span data-stu-id="59a76-156">!</span></span>      | <span data-ttu-id="59a76-157">Installierter Status des Features.</span><span class="sxs-lookup"><span data-stu-id="59a76-157">Installed state of the feature.</span></span>                           |



 

## <a name="logical-operators"></a><span data-ttu-id="59a76-158">Logische Operatoren</span><span class="sxs-lookup"><span data-stu-id="59a76-158">Logical Operators</span></span>

<span data-ttu-id="59a76-159">In der folgenden Tabelle werden die logischen Operatoren in bedingten Ausdrücken in der Reihenfolge, in der die Rangfolge hoch zu niedrig ist, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="59a76-159">The following table shows the logical operators in conditional expressions, in order of high-to-low precedence.</span></span>



| <span data-ttu-id="59a76-160">Operator</span><span class="sxs-lookup"><span data-stu-id="59a76-160">Operator</span></span> | <span data-ttu-id="59a76-161">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="59a76-161">Meaning</span></span>                                                 |
|----------|---------------------------------------------------------|
| <span data-ttu-id="59a76-162">Not</span><span class="sxs-lookup"><span data-stu-id="59a76-162">Not</span></span>      | <span data-ttu-id="59a76-163">Unärer Präfix Operator; kehrt den Status des folgenden Begriffs um.</span><span class="sxs-lookup"><span data-stu-id="59a76-163">Prefix unary operator; inverts state of following term.</span></span> |
| <span data-ttu-id="59a76-164">Und</span><span class="sxs-lookup"><span data-stu-id="59a76-164">And</span></span>      | <span data-ttu-id="59a76-165">True, wenn beide Begriffe true sind.</span><span class="sxs-lookup"><span data-stu-id="59a76-165">TRUE if both terms are TRUE.</span></span>                            |
| <span data-ttu-id="59a76-166">oder</span><span class="sxs-lookup"><span data-stu-id="59a76-166">Or</span></span>       | <span data-ttu-id="59a76-167">True, wenn eine oder beide Begriffe den Wert true haben.</span><span class="sxs-lookup"><span data-stu-id="59a76-167">TRUE if either or both terms are TRUE.</span></span>                  |
| <span data-ttu-id="59a76-168">Xor</span><span class="sxs-lookup"><span data-stu-id="59a76-168">Xor</span></span>      | <span data-ttu-id="59a76-169">True, wenn beide Bedingungen nicht erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="59a76-169">TRUE if either but not both terms are TRUE.</span></span>             |
| <span data-ttu-id="59a76-170">Eqv</span><span class="sxs-lookup"><span data-stu-id="59a76-170">Eqv</span></span>      | <span data-ttu-id="59a76-171">True, wenn beide Begriffe true sind oder beide Begriffe false sind.</span><span class="sxs-lookup"><span data-stu-id="59a76-171">TRUE if both terms are TRUE or both terms are FALSE.</span></span>    |
| <span data-ttu-id="59a76-172">IMP</span><span class="sxs-lookup"><span data-stu-id="59a76-172">Imp</span></span>      | <span data-ttu-id="59a76-173">True, wenn der linke Begriff false ist oder der Rechte Begriff true ist.</span><span class="sxs-lookup"><span data-stu-id="59a76-173">TRUE if left term is FALSE or right term is TRUE.</span></span>       |



 

## <a name="comparative-operators"></a><span data-ttu-id="59a76-174">Vergleichs Operatoren</span><span class="sxs-lookup"><span data-stu-id="59a76-174">Comparative Operators</span></span>

<span data-ttu-id="59a76-175">Die folgende Tabelle zeigt die Vergleichs Operatoren, die in bedingten Ausdrücken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59a76-175">The following table shows the comparison operators used in conditional expressions.</span></span> <span data-ttu-id="59a76-176">Diese Vergleichs Operatoren können nur zwischen zwei Werten auftreten.</span><span class="sxs-lookup"><span data-stu-id="59a76-176">These comparison operators can only occur between two values.</span></span>



| <span data-ttu-id="59a76-177">Operator</span><span class="sxs-lookup"><span data-stu-id="59a76-177">Operator</span></span> | <span data-ttu-id="59a76-178">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="59a76-178">Meaning</span></span>                                                     |
|----------|-------------------------------------------------------------|
| =        | <span data-ttu-id="59a76-179">TRUE, wenn der linke Wert gleich dem richtigen Wert ist.</span><span class="sxs-lookup"><span data-stu-id="59a76-179">TRUE if left value is equal to right value.</span></span>                 |
| <> | <span data-ttu-id="59a76-180">TRUE, wenn der linke Wert nicht gleich dem richtigen Wert ist.</span><span class="sxs-lookup"><span data-stu-id="59a76-180">TRUE if left value is not equal to right value.</span></span>             |
| >     | <span data-ttu-id="59a76-181">TRUE, wenn der linke Wert größer als der Rechte Wert ist.</span><span class="sxs-lookup"><span data-stu-id="59a76-181">TRUE if left value is greater than right value.</span></span>             |
| >=    | <span data-ttu-id="59a76-182">TRUE, wenn der linke Wert größer oder gleich dem rechten Wert ist.</span><span class="sxs-lookup"><span data-stu-id="59a76-182">TRUE if left value is greater than or equal to right value.</span></span> |
| <     | <span data-ttu-id="59a76-183">TRUE, wenn der linke Wert kleiner als der Rechte Wert ist.</span><span class="sxs-lookup"><span data-stu-id="59a76-183">TRUE if left value is less than right value.</span></span>                |
| <=    | <span data-ttu-id="59a76-184">TRUE, wenn der linke Wert kleiner oder gleich dem rechten Wert ist.</span><span class="sxs-lookup"><span data-stu-id="59a76-184">TRUE if left value is less than or equal to right value.</span></span>    |



 

## <a name="substring-operators"></a><span data-ttu-id="59a76-185">Substring-Operatoren</span><span class="sxs-lookup"><span data-stu-id="59a76-185">Substring Operators</span></span>

<span data-ttu-id="59a76-186">In der folgenden Tabelle sind die Teil Zeichenfolge-Operatoren aufgeführt, die in bedingten Ausdrücken verwendet werden</span><span class="sxs-lookup"><span data-stu-id="59a76-186">The following table shows the substring operators used in conditional expressions.</span></span> <span data-ttu-id="59a76-187">Substring-Operatoren können zwischen zwei Zeichen folgen Werten auftreten.</span><span class="sxs-lookup"><span data-stu-id="59a76-187">Substring operators can occur between two string values.</span></span>



| <span data-ttu-id="59a76-188">Operator</span><span class="sxs-lookup"><span data-stu-id="59a76-188">Operator</span></span> | <span data-ttu-id="59a76-189">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="59a76-189">Meaning</span></span>                                           |
|----------|---------------------------------------------------|
| >< | <span data-ttu-id="59a76-190">TRUE, wenn die linke Zeichenfolge die Rechte Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="59a76-190">TRUE if left string contains the right string.</span></span>    |
| << | <span data-ttu-id="59a76-191">TRUE, wenn die linke Zeichenfolge mit der rechten Zeichenfolge beginnt.</span><span class="sxs-lookup"><span data-stu-id="59a76-191">TRUE if left string starts with the right string.</span></span> |
| >> | <span data-ttu-id="59a76-192">TRUE, wenn die linke Zeichenfolge mit der rechten Zeichenfolge endet.</span><span class="sxs-lookup"><span data-stu-id="59a76-192">TRUE if left string ends with the right string.</span></span>   |



 

## <a name="bitwise-numeric-operators"></a><span data-ttu-id="59a76-193">Bitweise numerische Operatoren</span><span class="sxs-lookup"><span data-stu-id="59a76-193">Bitwise Numeric Operators</span></span>

<span data-ttu-id="59a76-194">In der folgenden Tabelle werden die bitweisen numerischen Operatoren in bedingten Ausdrücken angezeigt.</span><span class="sxs-lookup"><span data-stu-id="59a76-194">The following table shows the bitwise numeric operators in conditional expressions.</span></span> <span data-ttu-id="59a76-195">Diese Operatoren können zwischen zwei ganzzahligen Werten auftreten.</span><span class="sxs-lookup"><span data-stu-id="59a76-195">These operators can occur between two integer values.</span></span>



| <span data-ttu-id="59a76-196">Operator</span><span class="sxs-lookup"><span data-stu-id="59a76-196">Operator</span></span> | <span data-ttu-id="59a76-197">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="59a76-197">Meaning</span></span>                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | <span data-ttu-id="59a76-198">Bitweises and, true, wenn die linke und die Rechte Ganzzahl allgemeine Bits aufweisen.</span><span class="sxs-lookup"><span data-stu-id="59a76-198">Bitwise AND, TRUE if the left and right integers have any bits in common.</span></span>    |
| << | <span data-ttu-id="59a76-199">True, wenn die hohen 16 Bits der linken Ganzzahl gleich der rechten ganzen Zahl sind.</span><span class="sxs-lookup"><span data-stu-id="59a76-199">True if the high 16-bits of the left integer are equal to the right integer.</span></span> |
| >> | <span data-ttu-id="59a76-200">True, wenn die unteren 16 Bits der linken Ganzzahl gleich der rechten ganzen Zahl sind.</span><span class="sxs-lookup"><span data-stu-id="59a76-200">True if the low 16-bits of the left integer are equal to the right integer.</span></span>  |



 

## <a name="feature-and-component-state-values"></a><span data-ttu-id="59a76-201">Funktions-und Komponenten Zustands Werte</span><span class="sxs-lookup"><span data-stu-id="59a76-201">Feature and Component State Values</span></span>

<span data-ttu-id="59a76-202">In der folgenden Tabelle wird gezeigt, wo die Verwendung der Symbol-und Komponenten Operator Symbole gültig ist.</span><span class="sxs-lookup"><span data-stu-id="59a76-202">The following table shows where it is valid to use the feature and component operator symbols.</span></span>



| <span data-ttu-id="59a76-203">KOM <state></span><span class="sxs-lookup"><span data-stu-id="59a76-203">Operator <state></span></span> | <span data-ttu-id="59a76-204">Wenn diese Syntax gültig ist</span><span class="sxs-lookup"><span data-stu-id="59a76-204">Where this syntax is valid</span></span>                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59a76-205">$Component Aktion</span><span class="sxs-lookup"><span data-stu-id="59a76-205">$component-action</span></span>      | <span data-ttu-id="59a76-206">In der [Bedingungs Tabelle und](condition-table.md) in den [Sequenz](using-a-sequence-table.md) Tabellen nach der [costfinalize](costfinalize-action.md) -Aktion.</span><span class="sxs-lookup"><span data-stu-id="59a76-206">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="59a76-207">&Feature-Aktion</span><span class="sxs-lookup"><span data-stu-id="59a76-207">&feature-action</span></span>        | <span data-ttu-id="59a76-208">In der [Bedingungs Tabelle und](condition-table.md) in den [Sequenz](using-a-sequence-table.md) Tabellen nach der [costfinalize](costfinalize-action.md) -Aktion.</span><span class="sxs-lookup"><span data-stu-id="59a76-208">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="59a76-209">! Feature-State</span><span class="sxs-lookup"><span data-stu-id="59a76-209">!feature-state</span></span>         | <span data-ttu-id="59a76-210">In der [Bedingungs Tabelle und](condition-table.md) in den [Sequenz](using-a-sequence-table.md) Tabellen nach der [costfinalize](costfinalize-action.md) -Aktion.</span><span class="sxs-lookup"><span data-stu-id="59a76-210">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="59a76-211">? Component-State</span><span class="sxs-lookup"><span data-stu-id="59a76-211">?component-state</span></span>       | <span data-ttu-id="59a76-212">In der [Bedingungs Tabelle und](condition-table.md) in den [Sequenz](using-a-sequence-table.md) Tabellen nach der [costfinalize](costfinalize-action.md) -Aktion.</span><span class="sxs-lookup"><span data-stu-id="59a76-212">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |



 

<span data-ttu-id="59a76-213">In der folgenden Tabelle werden die Funktions-und Komponenten Zustands Werte aufgeführt, die in bedingten Ausdrücken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59a76-213">The following table shows the feature and component state values used in conditional expressions.</span></span> <span data-ttu-id="59a76-214">Diese Zustände werden erst festgelegt, wenn [**msisetinstalllevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) entweder direkt oder durch die [costfinalize](costfinalize-action.md) -Aktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="59a76-214">These states are not set until [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) is called, either directly or by the [CostFinalize](costfinalize-action.md) action.</span></span>



| <span data-ttu-id="59a76-215">State</span><span class="sxs-lookup"><span data-stu-id="59a76-215">State</span></span>                    | <span data-ttu-id="59a76-216">Wert</span><span class="sxs-lookup"><span data-stu-id="59a76-216">Value</span></span> | <span data-ttu-id="59a76-217">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="59a76-217">Meaning</span></span>                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| <span data-ttu-id="59a76-218">InstallState \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="59a76-218">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="59a76-219">-1</span><span class="sxs-lookup"><span data-stu-id="59a76-219">-1</span></span>    | <span data-ttu-id="59a76-220">Es ist keine Aktion für das Feature oder die Komponente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="59a76-220">No action to be taken on the feature or component.</span></span>              |
| <span data-ttu-id="59a76-221">InstallState \_ angekündigt</span><span class="sxs-lookup"><span data-stu-id="59a76-221">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="59a76-222">1</span><span class="sxs-lookup"><span data-stu-id="59a76-222">1</span></span>     | <span data-ttu-id="59a76-223">Angekündigte Funktion.</span><span class="sxs-lookup"><span data-stu-id="59a76-223">Advertised feature.</span></span> <span data-ttu-id="59a76-224">Dieser Status ist für Komponenten nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59a76-224">This state is not available for components.</span></span> |
| <span data-ttu-id="59a76-225">InstallState \_ fehlt.</span><span class="sxs-lookup"><span data-stu-id="59a76-225">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="59a76-226">2</span><span class="sxs-lookup"><span data-stu-id="59a76-226">2</span></span>     | <span data-ttu-id="59a76-227">Die Funktion oder Komponente ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="59a76-227">Feature or component is not present.</span></span>                            |
| <span data-ttu-id="59a76-228">InstallState \_ lokal</span><span class="sxs-lookup"><span data-stu-id="59a76-228">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="59a76-229">3</span><span class="sxs-lookup"><span data-stu-id="59a76-229">3</span></span>     | <span data-ttu-id="59a76-230">Feature oder Komponente auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="59a76-230">Feature or component on the local computer.</span></span>                     |
| <span data-ttu-id="59a76-231">InstallState- \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="59a76-231">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="59a76-232">4</span><span class="sxs-lookup"><span data-stu-id="59a76-232">4</span></span>     | <span data-ttu-id="59a76-233">Funktion oder Komponente, die von der Quelle ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59a76-233">Feature or component run from the source.</span></span>                       |



 

<span data-ttu-id="59a76-234">Beispielsweise wird der bedingte Ausdruck "&myfeature = 3" nur dann zu "true" ausgewertet, wenn die Funktion "myfeature" von Ihrem aktuellen Zustand in den Zustand "", der auf dem lokalen Computer installiert ist, "InstallState local" geändert wird \_ .</span><span class="sxs-lookup"><span data-stu-id="59a76-234">For example, the conditional expression "&MyFeature=3" evaluates to True only if MyFeature is changing from its current state to the state of being installed on the local computer, INSTALLSTATE\_LOCAL.</span></span>

<span data-ttu-id="59a76-235">Beachten Sie, dass Sie nicht auf die Bedingung $Component 1 = 3 angewiesen sind, um zu überprüfen, ob Component1 lokal auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="59a76-235">Note that you should not depend upon the condition $Component1=3 to check whether Component1 is locally installed on the computer.</span></span> <span data-ttu-id="59a76-236">Dies kann fehlschlagen, wenn Component1 von mehr als einem Produkt installiert wird.</span><span class="sxs-lookup"><span data-stu-id="59a76-236">This can fail if Component1 is installed by more than one product.</span></span> <span data-ttu-id="59a76-237">Nachdem Component1 lokal von product1 installiert wurde, wertet das Installationsprogramm während der Installation von product2 die Bedingung $Component 1 = 3 als false aus.</span><span class="sxs-lookup"><span data-stu-id="59a76-237">After Component1 has been installed locally by Product1, the installer evaluates the condition $Component1=3 as False during the installation of Product2.</span></span> <span data-ttu-id="59a76-238">Dies liegt daran, dass das Installationsprogramm die Version der Komponente mithilfe des Schlüssel Pfads der Komponente bestimmt und die Komponente für die Installation markiert, wenn deren Version größer oder gleich der installierten Komponente ist.</span><span class="sxs-lookup"><span data-stu-id="59a76-238">This is because the installer determines the version of the component using the component's key path and marks the component for installation if its version is greater than or equal to the installed component.</span></span>

<span data-ttu-id="59a76-239">Beachten Sie, dass das Installationsprogramm keine direkten Vergleiche des Datentyps [Version](version.md) in Bedingungs Anweisungen durchführt.</span><span class="sxs-lookup"><span data-stu-id="59a76-239">Note that the installer will not do direct comparisons of the [Version](version.md) data type in conditional statements.</span></span> <span data-ttu-id="59a76-240">Beispielsweise können Sie keine Vergleichs Operatoren verwenden, um Versionen wie "01,10" und "1,010" in einer Bedingungs Anweisung zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="59a76-240">For example, you cannot use comparative operators to compare versions such as "01.10" and "1.010" in a conditional statement.</span></span> <span data-ttu-id="59a76-241">Verwenden Sie stattdessen eine gültige Methode für die Suche nach einer Version, z. b. in [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), und legen Sie dann eine Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="59a76-241">Instead use a valid method to search for a version, such as described in [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), and then set a property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59a76-242">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59a76-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59a76-243">Verwenden von Eigenschaften in Bedingungs Anweisungen</span><span class="sxs-lookup"><span data-stu-id="59a76-243">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



