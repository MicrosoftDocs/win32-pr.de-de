---
description: Mit einem bedingten Zugriffs Steuerungs Eintrag (ACE) kann eine Zugriffs Bedingung ausgewertet werden, wenn eine Zugriffs Überprüfung durchgeführt wird. Die Security Deskriptor Definition Language (SDDL) stellt eine Syntax zum Definieren von bedingten ACEs in einem Zeichen folgen Format bereit.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Sicherheits Deskriptor-Definitions Sprache für bedingte ACEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cb6ae0588ae197c84d3b13362721cc3e98b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527014"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a><span data-ttu-id="ad7d2-104">Sicherheits Deskriptor-Definitions Sprache für bedingte ACEs</span><span class="sxs-lookup"><span data-stu-id="ad7d2-104">Security Descriptor Definition Language for Conditional ACEs</span></span>

<span data-ttu-id="ad7d2-105">Mit einem bedingten [*Zugriffs Steuerungs Eintrag*](/windows/desktop/SecGloss/a-gly) (ACE) kann eine Zugriffs Bedingung ausgewertet werden, wenn eine Zugriffs Überprüfung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-105">A conditional [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) allows an access condition to be evaluated when an access check is performed.</span></span> <span data-ttu-id="ad7d2-106">Die Security Deskriptor Definition Language (SDDL) stellt eine Syntax zum Definieren von bedingten ACEs in einem Zeichen folgen Format bereit.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-106">The security descriptor definition language (SDDL) provides syntax for defining conditional ACEs in a string format.</span></span>

<span data-ttu-id="ad7d2-107">Die SDDL für einen bedingten ACE ist das gleiche wie bei jedem ACE, wobei die Syntax für die bedingte Anweisung an das Ende der ACE-Zeichenfolge angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-107">The SDDL for a conditional ACE is the same as for any ACE, with the syntax for the conditional statement appended to the end of the ACE string.</span></span> <span data-ttu-id="ad7d2-108">Weitere Informationen zu SDDL finden Sie unter [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="ad7d2-108">For information about SDDL, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

<span data-ttu-id="ad7d2-109">Das \# Zeichen "" ist in Ressourcen Attributen mit "0" Synonym.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-109">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="ad7d2-110">Beispiel: d:Ai (XA; oici; FA;;; WD; (octetstringtype = = \# 1 \# 2 \# 3 \# \# )) entspricht und wird als d:Ai (XA; oici; FA;;;) interpretiert. WD; (octetstringtype = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="ad7d2-110">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

-   [<span data-ttu-id="ad7d2-111">Format der bedingten ACE-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad7d2-111">Conditional ACE String Format</span></span>](#conditional-ace-string-format)
-   [<span data-ttu-id="ad7d2-112">Bedingte Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="ad7d2-112">Conditional Expressions</span></span>](#conditional-expressions)
-   [<span data-ttu-id="ad7d2-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad7d2-113">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="ad7d2-114">Operatoren</span><span class="sxs-lookup"><span data-stu-id="ad7d2-114">Operators</span></span>](#operators)
-   [<span data-ttu-id="ad7d2-115">Operatorrangfolge</span><span class="sxs-lookup"><span data-stu-id="ad7d2-115">Operator Precedence</span></span>](#operator-precedence)
-   [<span data-ttu-id="ad7d2-116">Unbekannte Werte</span><span class="sxs-lookup"><span data-stu-id="ad7d2-116">Unknown Values</span></span>](#unknown-values)
-   [<span data-ttu-id="ad7d2-117">Auswertung bedingter ACE</span><span class="sxs-lookup"><span data-stu-id="ad7d2-117">Conditional ACE Evaluation</span></span>](#conditional-ace-evaluation)
-   [<span data-ttu-id="ad7d2-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad7d2-118">Examples</span></span>](#examples)
-   [<span data-ttu-id="ad7d2-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad7d2-119">Related topics</span></span>](#related-topics)

## <a name="conditional-ace-string-format"></a><span data-ttu-id="ad7d2-120">Format der bedingten ACE-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad7d2-120">Conditional ACE String Format</span></span>

<span data-ttu-id="ad7d2-121">Jeder ACE in einer [*sicherheitsbeschreibungerzeichenfolge*](/windows/desktop/SecGloss/s-gly) wird in Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-121">Each ACE in a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string is enclosed in parentheses.</span></span> <span data-ttu-id="ad7d2-122">Die Felder des ACE liegen in der folgenden Reihenfolge vor und sind durch Semikolons (;) getrennt.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-122">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

<span data-ttu-id="ad7d2-123">*AceType ***;** _AceFlags_* _;_ *_Rechte_*_;_ *_ObjectGUID_*_;_ *_Erertobjectguid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-123">*AceType\***;**_AceFlags_*_;_*_Rights_*_;_*_ObjectGuid_*_;_*_InheritObjectGuid_*_;_*_AccountSid_*_;(_*_ConditionalExpression_*_)_\*</span></span>

<span data-ttu-id="ad7d2-124">Die Felder werden wie in [ACE](ace-strings.md)-Zeichen folgen beschrieben mit den folgenden Ausnahmen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-124">The fields are as described in [ACE Strings](ace-strings.md), with the following exceptions.</span></span>

-   <span data-ttu-id="ad7d2-125">Das Feld " *AceType* " kann eine der folgenden Zeichen folgen sein.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-125">The *AceType* field can be one of the following strings.</span></span>

    | <span data-ttu-id="ad7d2-126">ACE-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad7d2-126">ACE type string</span></span> | <span data-ttu-id="ad7d2-127">Konstante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="ad7d2-127">Constant in Sddl.h</span></span>                         | <span data-ttu-id="ad7d2-128">AceType-Wert</span><span class="sxs-lookup"><span data-stu-id="ad7d2-128">AceType value</span></span>                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | <span data-ttu-id="ad7d2-129">Geleitet</span><span class="sxs-lookup"><span data-stu-id="ad7d2-129">"XA"</span></span><br/> | <span data-ttu-id="ad7d2-130">SDDL- \_ Rückruf \_ Zugriff \_ zulässig</span><span class="sxs-lookup"><span data-stu-id="ad7d2-130">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span><br/> | <span data-ttu-id="ad7d2-131">Zugriffs zulässiger \_ \_ Rückruf-ACE- \_ \_ Typ</span><span class="sxs-lookup"><span data-stu-id="ad7d2-131">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE</span></span><br/> |
    | <span data-ttu-id="ad7d2-132">XD</span><span class="sxs-lookup"><span data-stu-id="ad7d2-132">"XD"</span></span><br/> | <span data-ttu-id="ad7d2-133">SDDL- \_ Rückruf \_ Zugriff \_ verweigert</span><span class="sxs-lookup"><span data-stu-id="ad7d2-133">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span><br/>  | <span data-ttu-id="ad7d2-134">\_Rückruf- \_ ACE \_ - \_ Typ für Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="ad7d2-134">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE</span></span><br/>  |

    

     

-   <span data-ttu-id="ad7d2-135">Die ACE-Zeichenfolge enthält einen oder mehrere bedingte Ausdrücke, die in Klammern am Ende der Zeichenfolge eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-135">The ACE string includes one or more conditional expressions, enclosed in parentheses at the end of the string.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="ad7d2-136">Bedingte Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="ad7d2-136">Conditional Expressions</span></span>

<span data-ttu-id="ad7d2-137">Ein bedingter Ausdruck kann eines der folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-137">A conditional expression can include any of the following elements.</span></span>



| <span data-ttu-id="ad7d2-138">Ausdruckselement</span><span class="sxs-lookup"><span data-stu-id="ad7d2-138">Expression element</span></span>                                                | <span data-ttu-id="ad7d2-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad7d2-139">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7d2-140">*AttributeName*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-140">*AttributeName*</span></span><br/>                                        | <span data-ttu-id="ad7d2-141">Testet, ob das angegebene Attribut einen Wert ungleich 0 (null) aufweist.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-141">Tests whether the specified attribute has a nonzero value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ad7d2-142"> *attributeName* ist vorhanden</span><span class="sxs-lookup"><span data-stu-id="ad7d2-142">**exists** *AttributeName*</span></span><br/>                             | <span data-ttu-id="ad7d2-143">Testet, ob das angegebene Attribut im Client Kontext vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-143">Tests whether the specified attribute exists in the client context.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ad7d2-144">*AttributeName* - *Operator* *Wert*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-144">*AttributeName* *Operator* *Value*</span></span><br/>                     | <span data-ttu-id="ad7d2-145">Gibt das Ergebnis des angegebenen Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-145">Returns the result of the specified operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ad7d2-146">\* ConditionalExpression \* **\|\|** _ConditionalExpression_</span><span class="sxs-lookup"><span data-stu-id="ad7d2-146">\*ConditionalExpression\***\|\|**_ConditionalExpression_</span></span><br/> | <span data-ttu-id="ad7d2-147">Testet, ob einer der angegebenen bedingten Ausdrücke True ist.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-147">Tests whether either of the specified conditional expressions is true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ad7d2-148">*ConditionalExpression* **&&** *ConditionalExpression*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-148">*ConditionalExpression* **&&** *ConditionalExpression*</span></span><br/> | <span data-ttu-id="ad7d2-149">Testet, ob beide angegebenen bedingten Ausdrücke True sind.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-149">Tests whether both of the specified conditional expressions are true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ad7d2-150">**! (**_ConditionalExpression_*_)_*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-150">**!(**_ConditionalExpression_*_)_*</span></span><br/>                     | <span data-ttu-id="ad7d2-151">Die Umkehrung eines bedingten Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-151">The inverse of a conditional expression.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ad7d2-152">**Member \_ von {**_sidarray_*_}_*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-152">**Member\_of{**_SidArray_*_}_*</span></span><br/>                         | <span data-ttu-id="ad7d2-153">Testet, ob das [**sid \_ -und \_ Attribute-**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) Array des Client Kontexts alle [Sicherheits](security-identifiers.md) -IDs (SIDs) in der durch Trennzeichen getrennten Liste enthält, die von *sidarray* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-153">Tests whether the [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) array of the client context contains all of the [Security Identifiers](security-identifiers.md) (SIDs) in the comma-separated list specified by *SidArray*.</span></span><br/> <span data-ttu-id="ad7d2-154">Für ACEs zulassen muss für eine Client Kontext-sid festgelegt sein, dass das Attribut der **SE- \_ Gruppe \_** als eine Entsprechung betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-154">For Allow ACEs, a client context SID must have the **SE\_GROUP\_ENABLED** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="ad7d2-155">Bei deny-ACEs muss für eine Client Kontext-sid entweder die **SE- \_ Gruppe \_ aktiviert** sein, oder die Gruppe "SE", die für das Attribut " **\_ \_ \_ \_ \_ nur ablehnen" verwendet** werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-155">For Deny ACEs, a client context SID must have either the **SE\_GROUP\_ENABLED** or the **SE\_GROUP\_USE\_FOR\_DENY\_ONLY** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="ad7d2-156">Das *sidarray* -Array kann entweder sid-Zeichen folgen (z. b. "S-1-5-6") oder sid-Aliase (z. b. "BA") enthalten.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-156">The *SidArray* array can contain either SID strings (for example, "S-1-5-6") or SID aliases (for example, "BA"</span></span><br/> |



 

## <a name="attributes"></a><span data-ttu-id="ad7d2-157">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad7d2-157">Attributes</span></span>

<span data-ttu-id="ad7d2-158">Ein Attribut stellt ein Element im Informations Array der [**Authz- \_ Sicherheits \_ Attribute \_**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) im Client Kontext dar.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-158">An attribute represents an element in the [**AUTHZ\_SECURITY\_ATTRIBUTES\_INFORMATION**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) array in the client context.</span></span> <span data-ttu-id="ad7d2-159">Ein Attribut Name kann alle alphanumerischen Zeichen und jedes der Zeichen ":", "/", "." und " \_ " enthalten.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-159">An attribute name can contain any alphanumeric characters and any of the characters ":", "/", ".", and "\_".</span></span>

<span data-ttu-id="ad7d2-160">Bei einem Attribut Wert kann es sich um einen der folgenden Typen handeln:</span><span class="sxs-lookup"><span data-stu-id="ad7d2-160">An attribute value can be any of the following types.</span></span>



| <span data-ttu-id="ad7d2-161">Werttyp</span><span class="sxs-lookup"><span data-stu-id="ad7d2-161">Value type</span></span>         | <span data-ttu-id="ad7d2-162">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad7d2-162">Description</span></span>                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7d2-163">Integer</span><span class="sxs-lookup"><span data-stu-id="ad7d2-163">Integer</span></span><br/> | <span data-ttu-id="ad7d2-164">Eine 64-Bit-Ganzzahl in Dezimal-oder hexadezimal Schreibweise.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-164">A 64-bit integer in either decimal or hexadecimal notation.</span></span><br/>                                                                                                                              |
| <span data-ttu-id="ad7d2-165">String</span><span class="sxs-lookup"><span data-stu-id="ad7d2-165">String</span></span><br/>  | <span data-ttu-id="ad7d2-166">Ein durch Anführungszeichen getrennter Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-166">A string value delimited by quotes.</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="ad7d2-167">SID</span><span class="sxs-lookup"><span data-stu-id="ad7d2-167">SID</span></span><br/>     | <span data-ttu-id="ad7d2-168">Sid (S-1-1-0) oder sid (BA).</span><span class="sxs-lookup"><span data-stu-id="ad7d2-168">SID(S-1-1-0) or SID(BA).</span></span> <span data-ttu-id="ad7d2-169">Muss Mitglied der RHS des Members \_ oder des Geräte \_ Mitglieds von sein \_ .</span><span class="sxs-lookup"><span data-stu-id="ad7d2-169">Has to be on RHS of Member\_of or Device\_Member\_of.</span></span><br/>                                                                                                           |
| <span data-ttu-id="ad7d2-170">BLOB</span><span class="sxs-lookup"><span data-stu-id="ad7d2-170">BLOB</span></span><br/>    | <span data-ttu-id="ad7d2-171">\# gefolgt von hexadezimal Zahlen.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-171">\# followed by hexadecimal numbers.</span></span> <span data-ttu-id="ad7d2-172">Wenn die Länge der Zahlen ungerade ist, wird der in 0 (null) \# übersetzt, um dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-172">If length of the numbers is odd, then the \# is translated to a 0 to make it even.</span></span> <span data-ttu-id="ad7d2-173">Außerdem \# wird ein, das an anderer Stelle im Wert angezeigt wird, in 0 übersetzt.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-173">Also an \# appearing elsewhere in the value is translated to a 0.</span></span><br/> |



 

## <a name="operators"></a><span data-ttu-id="ad7d2-174">Operatoren</span><span class="sxs-lookup"><span data-stu-id="ad7d2-174">Operators</span></span>

<span data-ttu-id="ad7d2-175">Die folgenden Operatoren sind für die Verwendung in bedingten Ausdrücken definiert, um die Werte von Attributen zu testen.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-175">The following operators are defined for use in conditional expressions to test the values of attributes.</span></span> <span data-ttu-id="ad7d2-176">Alle diese Operatoren sind binäre Operatoren und werden in der Form *attributeName* *Operator* *value* verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-176">All of these are binary operators and used in the form *AttributeName* *Operator* *Value*.</span></span>



| <span data-ttu-id="ad7d2-177">Operator</span><span class="sxs-lookup"><span data-stu-id="ad7d2-177">Operator</span></span>            | <span data-ttu-id="ad7d2-178">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad7d2-178">Description</span></span>                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | <span data-ttu-id="ad7d2-179">Konventionelle Definition.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-179">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="ad7d2-180">!=</span><span class="sxs-lookup"><span data-stu-id="ad7d2-180">!=</span></span><br/>       | <span data-ttu-id="ad7d2-181">Konventionelle Definition.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-181">Conventional definition.</span></span><br/>                                                                                      |
| <<br/>     | <span data-ttu-id="ad7d2-182">Konventionelle Definition.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-182">Conventional definition.</span></span><br/>                                                                                      |
| <=<br/>    | <span data-ttu-id="ad7d2-183">Konventionelle Definition.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-183">Conventional definition.</span></span><br/>                                                                                      |
| ><br/>     | <span data-ttu-id="ad7d2-184">Konventionelle Definition.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-184">Conventional definition.</span></span><br/>                                                                                      |
| >=<br/>    | <span data-ttu-id="ad7d2-185">Konventionelle Definition.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-185">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="ad7d2-186">Enthält</span><span class="sxs-lookup"><span data-stu-id="ad7d2-186">Contains</span></span><br/> | <span data-ttu-id="ad7d2-187">**True** , wenn der Wert des angegebenen Attributs eine übergeordnete Menge des angegebenen Werts ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-187">**TRUE** if the value of the specified attribute is a superset of the specified value; otherwise, **FALSE**.</span></span><br/>  |
| <span data-ttu-id="ad7d2-188">Beliebige \_ von</span><span class="sxs-lookup"><span data-stu-id="ad7d2-188">Any\_of</span></span><br/>  | <span data-ttu-id="ad7d2-189">**True** , wenn der angegebene Wert eine supermenge des Werts des angegebenen Attributs ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-189">**TRUE** if the specified value is a superset of the value of the specified attribute; otherwise, **FALSE**.</span></span> <br/> |



 

<span data-ttu-id="ad7d2-190">Außerdem sind die unären Operatoren vorhanden, Member \_ von und Negation (!) werden wie in der Tabelle bedingte Ausdrücke beschrieben definiert.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-190">In addition, the unary operators Exists, Member\_of, and negation (!) are defined as described in the Conditional Expressions table.</span></span>

<span data-ttu-id="ad7d2-191">Dem "enthält"-Operator muss ein Leerraum vorangestellt und gefolgt werden, und dem "Any \_ of"-Operator muss ein Leerzeichen vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-191">The "Contains" operator must be preceded and followed by white space, and the "Any\_of" operator must be preceded by white space.</span></span>

## <a name="operator-precedence"></a><span data-ttu-id="ad7d2-192">Operatorrangfolge</span><span class="sxs-lookup"><span data-stu-id="ad7d2-192">Operator Precedence</span></span>

<span data-ttu-id="ad7d2-193">Die Operatoren werden in der folgenden Rangfolge ausgewertet, wobei Vorgänge mit gleicher Rangfolge von links nach rechts ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-193">The operators are evaluated in the following order of precedence, with operations of equal precedence being evaluated from left to right.</span></span>

1.  <span data-ttu-id="ad7d2-194">Vorhanden, Mitglied \_ von</span><span class="sxs-lookup"><span data-stu-id="ad7d2-194">Exists, Member\_of</span></span>
2.  <span data-ttu-id="ad7d2-195">Enthält, beliebige \_ von</span><span class="sxs-lookup"><span data-stu-id="ad7d2-195">Contains, Any\_of</span></span>
3.  <span data-ttu-id="ad7d2-196">= =,! =, <, <=, >, >=</span><span class="sxs-lookup"><span data-stu-id="ad7d2-196">==, !=, <, <=, >, >=</span></span>
4.  <span data-ttu-id="ad7d2-197">!</span><span class="sxs-lookup"><span data-stu-id="ad7d2-197">!</span></span>
5.  &&
6.  \|\|

<span data-ttu-id="ad7d2-198">Außerdem kann jeder Teil eines bedingten Ausdrucks in Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-198">In addition, any portion of a conditional expression can be enclosed in parenthesis.</span></span> <span data-ttu-id="ad7d2-199">Ausdrücke in Klammern werden zuerst ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-199">Expressions within parentheses are evaluated first.</span></span>

## <a name="unknown-values"></a><span data-ttu-id="ad7d2-200">Unbekannte Werte</span><span class="sxs-lookup"><span data-stu-id="ad7d2-200">Unknown Values</span></span>

<span data-ttu-id="ad7d2-201">Die Ergebnisse der bedingten Ausdrücke geben mitunter den Wert **Unknown** zurück.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-201">The results of conditional expressions sometimes return a value of **Unknown**.</span></span> <span data-ttu-id="ad7d2-202">Beispielsweise geben alle relationalen Vorgänge " **Unknown** " zurück, wenn das angegebene Attribut nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-202">For example, any of the relational operations return **Unknown** when the specified attribute does not exist.</span></span>

<span data-ttu-id="ad7d2-203">In der folgenden Tabelle werden die Ergebnisse für eine logische **and-** Operation zwischen zwei bedingten Ausdrücken, *ConditionalExpression1* und *ConditionalExpression2*, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-203">The following table describes the results for a logical **AND** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="ad7d2-204">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-204">*ConditionalExpression1*</span></span> | <span data-ttu-id="ad7d2-205">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-205">*ConditionalExpression2*</span></span> | <span data-ttu-id="ad7d2-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|----------------------------------------------------------|
| <span data-ttu-id="ad7d2-207">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-207">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-208">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-208">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-209">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-209">**TRUE**</span></span><br/>                                      |
| <span data-ttu-id="ad7d2-210">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-210">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-211">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-211">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-212">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-212">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="ad7d2-213">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-213">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-214">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-214">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-215">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-215">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="ad7d2-216">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-216">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-217">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-217">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-218">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-218">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="ad7d2-219">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-219">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-220">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-220">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-221">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-221">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="ad7d2-222">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-222">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-223">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-223">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-224">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-224">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="ad7d2-225">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-225">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-226">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-226">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-227">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-227">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="ad7d2-228">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-228">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-229">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-229">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-230">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-230">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="ad7d2-231">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-231">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-232">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-232">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-233">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-233">**UNKNOWN**</span></span><br/>                                   |



 

<span data-ttu-id="ad7d2-234">In der folgenden Tabelle werden die Ergebnisse für eine logische **or** -Operation zwischen zwei bedingten Ausdrücken, *ConditionalExpression1* und *ConditionalExpression2*, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-234">The following table describes the results for a logical **OR** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="ad7d2-235">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-235">*ConditionalExpression1*</span></span> | <span data-ttu-id="ad7d2-236">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-236">*ConditionalExpression2*</span></span> | <span data-ttu-id="ad7d2-237">*ConditionalExpression1* \*\*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-237">*ConditionalExpression1* \*\*</span></span>\|\|<span data-ttu-id="ad7d2-238">\*\* *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="ad7d2-238">\*\* *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|------------------------------------------------------------|
| <span data-ttu-id="ad7d2-239">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-239">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-240">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-240">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-241">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-241">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="ad7d2-242">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-242">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-243">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-243">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-244">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-244">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="ad7d2-245">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-245">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-246">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-246">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-247">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-247">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="ad7d2-248">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-248">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-249">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-249">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-250">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-250">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="ad7d2-251">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-251">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-252">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-252">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-253">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-253">**FALSE**</span></span><br/>                                       |
| <span data-ttu-id="ad7d2-254">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-254">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-255">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-255">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-256">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-256">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="ad7d2-257">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-257">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-258">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-258">**TRUE**</span></span><br/>      | <span data-ttu-id="ad7d2-259">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-259">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="ad7d2-260">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-260">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-261">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-261">**FALSE**</span></span><br/>     | <span data-ttu-id="ad7d2-262">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-262">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="ad7d2-263">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-263">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-264">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-264">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ad7d2-265">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7d2-265">**UNKNOWN**</span></span><br/>                                     |



 

<span data-ttu-id="ad7d2-266">Die Negation eines bedingten Ausdrucks mit dem Wert " **Unknown** " ist ebenfalls **unbekannt**.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-266">The negation of a conditional expression with a value of **UNKNOWN** is also **UNKNOWN**.</span></span>

## <a name="conditional-ace-evaluation"></a><span data-ttu-id="ad7d2-267">Auswertung bedingter ACE</span><span class="sxs-lookup"><span data-stu-id="ad7d2-267">Conditional ACE Evaluation</span></span>

<span data-ttu-id="ad7d2-268">In der folgenden Tabelle wird das Ergebnis der Zugriffs Überprüfung eines bedingten ACE in Abhängigkeit von der abschließenden Auswertung des bedingten Ausdrucks beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-268">The following table describes the access check result of a conditional ACE depending on the final evaluation of the conditional expression.</span></span>

| <span data-ttu-id="ad7d2-269">ACE-Typ</span><span class="sxs-lookup"><span data-stu-id="ad7d2-269">ACE type</span></span>         | <span data-ttu-id="ad7d2-270">TRUE</span><span class="sxs-lookup"><span data-stu-id="ad7d2-270">TRUE</span></span>             | <span data-ttu-id="ad7d2-271">false</span><span class="sxs-lookup"><span data-stu-id="ad7d2-271">FALSE</span></span>                 | <span data-ttu-id="ad7d2-272">UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="ad7d2-272">UNKNOWN</span></span>               |
|------------------|------------------|-----------------------|-----------------------|
| <span data-ttu-id="ad7d2-273">Zulassen</span><span class="sxs-lookup"><span data-stu-id="ad7d2-273">Allow</span></span><br/> | <span data-ttu-id="ad7d2-274">Zulassen</span><span class="sxs-lookup"><span data-stu-id="ad7d2-274">Allow</span></span><br/> | <span data-ttu-id="ad7d2-275">ACE ignorieren</span><span class="sxs-lookup"><span data-stu-id="ad7d2-275">Ignore ACE</span></span><br/> | <span data-ttu-id="ad7d2-276">ACE ignorieren</span><span class="sxs-lookup"><span data-stu-id="ad7d2-276">Ignore ACE</span></span><br/> |
| <span data-ttu-id="ad7d2-277">Verweigern</span><span class="sxs-lookup"><span data-stu-id="ad7d2-277">Deny</span></span><br/>  | <span data-ttu-id="ad7d2-278">Verweigern</span><span class="sxs-lookup"><span data-stu-id="ad7d2-278">Deny</span></span><br/>  | <span data-ttu-id="ad7d2-279">ACE ignorieren</span><span class="sxs-lookup"><span data-stu-id="ad7d2-279">Ignore ACE</span></span><br/> | <span data-ttu-id="ad7d2-280">Verweigern</span><span class="sxs-lookup"><span data-stu-id="ad7d2-280">Deny</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="ad7d2-281">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad7d2-281">Examples</span></span>

<span data-ttu-id="ad7d2-282">In den folgenden Beispielen wird veranschaulicht, wie die angegebenen Zugriffsrichtlinien durch einen bedingten ACE dargestellt werden, der mithilfe von SDDL definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-282">The following examples show how the specified access policies are represented by a conditional ACE defined by using SDDL.</span></span>

<dl> <dt>

<span data-ttu-id="ad7d2-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span><span class="sxs-lookup"><span data-stu-id="ad7d2-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="ad7d2-284">Execute für alle zulassen, wenn die beiden folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="ad7d2-284">Allow Execute to Everyone if both of the following conditions are met:</span></span>

-   <span data-ttu-id="ad7d2-285">Titel = pm</span><span class="sxs-lookup"><span data-stu-id="ad7d2-285">Title = PM</span></span>
-   <span data-ttu-id="ad7d2-286">Division = Finanzen oder Division = Verkäufe</span><span class="sxs-lookup"><span data-stu-id="ad7d2-286">Division = Finance or Division = Sales</span></span>

</dd> <dt>

<span data-ttu-id="ad7d2-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="ad7d2-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="ad7d2-288">D: (XA;; FX;;; S-1-1-0; ( @User.Title = = "PM"  &&  ( @User.Division = = "Finance" \| \| @User.Division = = "Sales")))</span><span class="sxs-lookup"><span data-stu-id="ad7d2-288">D:(XA; ;FX;;;S-1-1-0; (@User.Title=="PM" && (@User.Division=="Finance" \|\| @User.Division ==" Sales")))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="ad7d2-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span><span class="sxs-lookup"><span data-stu-id="ad7d2-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="ad7d2-290">Execute Execute, wenn eines der Benutzer-Projekte mit den Datei-Projekten Intersect.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-290">Allow execute if any of the user s projects intersect with the file s projects.</span></span>

</dd> <dt>

<span data-ttu-id="ad7d2-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="ad7d2-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="ad7d2-292">D: (XA;; FX;;; S-1-1-0; ( @User.Project Any \_ von @Resource.Project ))</span><span class="sxs-lookup"><span data-stu-id="ad7d2-292">D:(XA; ;FX;;;S-1-1-0; (@User.Project Any\_of @Resource.Project))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="ad7d2-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span><span class="sxs-lookup"><span data-stu-id="ad7d2-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="ad7d2-294">Lesezugriff zulassen, wenn der Benutzer sich mit einer Smartcard angemeldet hat, ein Sicherungs Operator ist und eine Verbindung von einem Computer mit aktiviertem BitLocker herstellt.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-294">Allow read access if the user has logged in with a smart card, is a backup operator, and is connecting from a machine with Bitlocker enabled.</span></span>

</dd> <dt>

<span data-ttu-id="ad7d2-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="ad7d2-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="ad7d2-296">D: (XA;; Fr;;; S-1-1-0; (Mitglied \_ von {sid (Smartcard- \_ SID), sid (BO)}  && @Device.Bitlocker ))</span><span class="sxs-lookup"><span data-stu-id="ad7d2-296">D:(XA; ;FR;;;S-1-1-0; (Member\_of {SID(Smartcard\_SID), SID(BO)} && @Device.Bitlocker))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="ad7d2-297">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad7d2-297">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ad7d2-298">[\[MS-DYP \] : Beschreibung der Sicherheits Beschreibungssprache](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="ad7d2-298">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

