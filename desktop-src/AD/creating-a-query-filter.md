---
title: Erstellen eines Abfrage Filters
description: Ein Abfrage Filter weist Active Directory Domain Services an, Daten in einer LDAP-Abfrage Syntax zu suchen. Alle angegebenen Datenzugriffs Technologien, die im Thema auswählen der Suchtechnologie aufgeführt sind, unterstützen die LDAP-Abfrage Syntax.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, Erstellen eines Abfrage Filters
- Abfrage Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855203"
---
# <a name="creating-a-query-filter"></a><span data-ttu-id="a516d-106">Erstellen eines Abfrage Filters</span><span class="sxs-lookup"><span data-stu-id="a516d-106">Creating a Query Filter</span></span>

<span data-ttu-id="a516d-107">Ein Abfrage Filter weist Active Directory Domain Services an, Daten in einer LDAP-Abfrage Syntax zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a516d-107">A query filter instructs Active Directory Domain Services to find data in an LDAP query syntax.</span></span> <span data-ttu-id="a516d-108">Alle angegebenen Datenzugriffs Technologien, die im Thema [Auswählen der Suchtechnologie](choosing-the-search-technology.md) aufgeführt sind, unterstützen die LDAP-Abfrage Syntax.</span><span class="sxs-lookup"><span data-stu-id="a516d-108">All the specified data access technologies listed in the [Choosing the Search Technology](choosing-the-search-technology.md) topic support LDAP query syntax.</span></span>

<span data-ttu-id="a516d-109">Die LDAP-Abfrage Syntax lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a516d-109">The LDAP query syntax is as follows:</span></span>


```C++
<expression><expression>...
```



<span data-ttu-id="a516d-110">Ein Filter kann einen oder mehrere Ausdrücke enthalten.</span><span class="sxs-lookup"><span data-stu-id="a516d-110">A filter can contain one, or more, expressions.</span></span> <span data-ttu-id="a516d-111">Ein Ausdruck weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="a516d-111">An expression has the following form:</span></span>


```C++
(<logicaloperator><comparison><comparison...>)
```



<span data-ttu-id="a516d-112">dabei &lt; ist "logischeroperator &gt; " einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="a516d-112">where "&lt;logicaloperator&gt;" is one of the following.</span></span>



| <span data-ttu-id="a516d-113">Operator</span><span class="sxs-lookup"><span data-stu-id="a516d-113">Operator</span></span>        | <span data-ttu-id="a516d-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a516d-114">Description</span></span>                |
|-----------------|----------------------------|
| <span data-ttu-id="a516d-115">"\|"</span><span class="sxs-lookup"><span data-stu-id="a516d-115">"\|"</span></span><br/> | <span data-ttu-id="a516d-116">Logisches **or**</span><span class="sxs-lookup"><span data-stu-id="a516d-116">Logical **OR**</span></span><br/>  |
| <span data-ttu-id="a516d-117">"&"</span><span class="sxs-lookup"><span data-stu-id="a516d-117">"&"</span></span><br/>  | <span data-ttu-id="a516d-118">Logisches **and**</span><span class="sxs-lookup"><span data-stu-id="a516d-118">Logical **AND**</span></span><br/> |
| <span data-ttu-id="a516d-119">"!"</span><span class="sxs-lookup"><span data-stu-id="a516d-119">"!"</span></span><br/>  | <span data-ttu-id="a516d-120">Logisches **Not**</span><span class="sxs-lookup"><span data-stu-id="a516d-120">Logical **NOT**</span></span><br/> |



 

<span data-ttu-id="a516d-121">und " &lt; Vergleich &gt; " ist Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a516d-121">and "&lt;comparison&gt;" is the following:</span></span>


```C++
(<attribute><operator><value>)
```



<span data-ttu-id="a516d-122">Dabei ist " &lt; Attribute &gt; " der **ldapDisplayName** des auszuwertenden Attributs &lt; . "Value &gt; " ist der Wert, mit dem verglichen werden soll, und " &lt; Operator &gt; " ist einer der folgenden Vergleichs Operatoren.</span><span class="sxs-lookup"><span data-stu-id="a516d-122">where "&lt;attribute&gt;" is the **lDAPDisplayName** of the attribute to evaluate, "&lt;value&gt;" is the value to compare against, and "&lt;operator&gt;" is one of the following comparison operators.</span></span>



| <span data-ttu-id="a516d-123">Operator</span><span class="sxs-lookup"><span data-stu-id="a516d-123">Operator</span></span>           | <span data-ttu-id="a516d-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a516d-124">Description</span></span>                         |
|--------------------|-------------------------------------|
| <span data-ttu-id="a516d-125">"="</span><span class="sxs-lookup"><span data-stu-id="a516d-125">"="</span></span><br/>     | <span data-ttu-id="a516d-126">Equals</span><span class="sxs-lookup"><span data-stu-id="a516d-126">Equals</span></span><br/>                   |
| <span data-ttu-id="a516d-127">"~="</span><span class="sxs-lookup"><span data-stu-id="a516d-127">"~="</span></span><br/>    | <span data-ttu-id="a516d-128">Ungefähr Gleichheits</span><span class="sxs-lookup"><span data-stu-id="a516d-128">Approximately equals</span></span><br/>     |
| <span data-ttu-id="a516d-129">"<="</span><span class="sxs-lookup"><span data-stu-id="a516d-129">"<="</span></span><br/> | <span data-ttu-id="a516d-130">Kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="a516d-130">Less than or equal to</span></span><br/>    |
| <span data-ttu-id="a516d-131">">="</span><span class="sxs-lookup"><span data-stu-id="a516d-131">">="</span></span><br/> | <span data-ttu-id="a516d-132">Größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="a516d-132">Greater than or equal to</span></span><br/> |



 

<span data-ttu-id="a516d-133">Außerdem kann der Wert "Value" abhängig von der Attribut Syntax das Platzhalter &lt; &gt; Symbol (" \* ") enthalten.</span><span class="sxs-lookup"><span data-stu-id="a516d-133">In addition, depending on the attribute syntax, the "&lt;value&gt;" may contain the wildcard symbol ("\*").</span></span> <span data-ttu-id="a516d-134">Ein " &lt; Wert &gt; ", der nur einen Platzhalter enthält, prüft, ob ein Wert in " &lt; Attribute &gt; " vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a516d-134">A "&lt;value&gt;" that contains only a wildcard will check for the existence of any value in "&lt;attribute&gt;".</span></span> <span data-ttu-id="a516d-135">Wenn kein Wert für "Attribute" festgelegt ist &lt; &gt; , schlägt der Test fehl.</span><span class="sxs-lookup"><span data-stu-id="a516d-135">If no value is set for "&lt;attribute&gt;", the test will fail.</span></span>

<span data-ttu-id="a516d-136">Wenn eines der folgenden Sonderzeichen als Literale im Abfrage Filter angezeigt werden muss, müssen Sie durch die aufgeführte Escapesequenz ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a516d-136">If any of the following special characters must appear in the query filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="a516d-137">ASCII-Zeichen</span><span class="sxs-lookup"><span data-stu-id="a516d-137">ASCII character</span></span>    | <span data-ttu-id="a516d-138">Escapesequenzersatz</span><span class="sxs-lookup"><span data-stu-id="a516d-138">Escape sequence substitute</span></span> |
|--------------------|----------------------------|
| \*<br/>      | <span data-ttu-id="a516d-139">" \\ 2A"</span><span class="sxs-lookup"><span data-stu-id="a516d-139">"\\2a"</span></span><br/>          |
| <span data-ttu-id="a516d-140">(</span><span class="sxs-lookup"><span data-stu-id="a516d-140">(</span></span><br/>       | <span data-ttu-id="a516d-141">" \\ 28"</span><span class="sxs-lookup"><span data-stu-id="a516d-141">"\\28"</span></span><br/>          |
| <span data-ttu-id="a516d-142">)</span><span class="sxs-lookup"><span data-stu-id="a516d-142">)</span></span><br/>       | <span data-ttu-id="a516d-143">" \\ 29"</span><span class="sxs-lookup"><span data-stu-id="a516d-143">"\\29"</span></span><br/>          |
| \\<br/>      | <span data-ttu-id="a516d-144">" \\ 5C"</span><span class="sxs-lookup"><span data-stu-id="a516d-144">"\\5c"</span></span><br/>          |
| <span data-ttu-id="a516d-145">**NUL**</span><span class="sxs-lookup"><span data-stu-id="a516d-145">**NUL**</span></span><br/> | <span data-ttu-id="a516d-146">" \\ 00"</span><span class="sxs-lookup"><span data-stu-id="a516d-146">"\\00"</span></span><br/>          |



 

<span data-ttu-id="a516d-147">Darüber hinaus können beliebige Binärdaten mithilfe der Escapesequenzsyntax dargestellt werden, indem jedes Byte der Binärdaten mit dem umgekehrten Schrägstrich und zwei hexadezimalen Ziffern codiert wird.</span><span class="sxs-lookup"><span data-stu-id="a516d-147">In addition, arbitrary binary data may be represented using the escape sequence syntax by encoding each byte of binary data with the backslash followed by two hexadecimal digits.</span></span> <span data-ttu-id="a516d-148">Beispielsweise wird der vier-Byte-Wert 0x00000004 \\ \\ \\ \\ in einer Filter Zeichenfolge als "00 00 00 04" codiert.</span><span class="sxs-lookup"><span data-stu-id="a516d-148">For example, the four-byte value 0x00000004 is encoded as "\\00\\00\\00\\04" in a filter string.</span></span>

## <a name="examples"></a><span data-ttu-id="a516d-149">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a516d-149">Examples</span></span>

<span data-ttu-id="a516d-150">Mit der folgenden Abfrage Zeichenfolge wird nach allen Objekten des Typs "Computer" gesucht.</span><span class="sxs-lookup"><span data-stu-id="a516d-150">The following query string will search for all objects of type "computer".</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="a516d-151">Die folgende Abfrage Zeichenfolge sucht nach allen Objekten des Typs "Computer" mit einem Namen, der mit "Desktop" beginnt.</span><span class="sxs-lookup"><span data-stu-id="a516d-151">The following query string will search for all objects of type "computer" with a name that begins with "desktop".</span></span>


```C++
(&(objectCategory=computer)(name=desktop*))
```



<span data-ttu-id="a516d-152">Die folgende Abfrage Zeichenfolge sucht nach allen Objekten des Typs "Computer" mit einem Namen, der mit "Desktop" beginnt, oder mit einem Namen, der mit "Notebook" beginnt.</span><span class="sxs-lookup"><span data-stu-id="a516d-152">The following query string will search for all objects of type "computer" with a name that begins with "desktop" or a name that begins with "notebook".</span></span>


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



<span data-ttu-id="a516d-153">Mit der folgenden Abfrage Zeichenfolge wird nach allen Objekten des Typs "User" gesucht, die eine privat Telefonnummer haben.</span><span class="sxs-lookup"><span data-stu-id="a516d-153">The following query string will search for all objects of type "user" that have a home phone number.</span></span>


```C++
(&(objectCategory=user)(homePhone=*))
```



<span data-ttu-id="a516d-154">Weitere Informationen zu Abfrage Filter Zeichenfolgen und Verwendungs Beispielen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="a516d-154">For more information about query filter strings, and usage examples, see:</span></span>

-   [<span data-ttu-id="a516d-155">Suchen nach Objekten nach Klasse</span><span class="sxs-lookup"><span data-stu-id="a516d-155">Finding Objects by Class</span></span>](finding-objects-by-class.md)
-   [<span data-ttu-id="a516d-156">Suchen nach Objekten nach Namen</span><span class="sxs-lookup"><span data-stu-id="a516d-156">Finding Objects by Name</span></span>](finding-objects-by-name.md)
-   [<span data-ttu-id="a516d-157">Suchen nach einer Liste der abzufragende Attribute</span><span class="sxs-lookup"><span data-stu-id="a516d-157">Finding a List of Attributes To Query</span></span>](finding-a-list-of-attributes-to-query.md)
-   [<span data-ttu-id="a516d-158">Überprüfen der Abfrage Filter Syntax</span><span class="sxs-lookup"><span data-stu-id="a516d-158">Checking the Query Filter Syntax</span></span>](checking-the-query-filter-syntax.md)
-   [<span data-ttu-id="a516d-159">Angeben von Vergleichswerten</span><span class="sxs-lookup"><span data-stu-id="a516d-159">How to Specify Comparison Values</span></span>](how-to-specify-comparison-values.md)

 

 





