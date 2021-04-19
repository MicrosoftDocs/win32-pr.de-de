---
description: Die Erweiterte Abfrage Syntax (AQS) ist die Standard Abfrage Syntax, die von Windows Search verwendet wird, um den Index abzufragen und Suchparameter zu verfeinern und einzuschränken.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Programm gesteuertes verwenden der erweiterten Abfrage Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8fa69a5a5ccaa37b84a10abd367e5a29656455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345673"
---
# <a name="using-advanced-query-syntax-programmatically"></a><span data-ttu-id="ac2b1-103">Programm gesteuertes verwenden der erweiterten Abfrage Syntax</span><span class="sxs-lookup"><span data-stu-id="ac2b1-103">Using Advanced Query Syntax Programmatically</span></span>

<span data-ttu-id="ac2b1-104">Die Erweiterte Abfrage Syntax (AQS) ist die Standard Abfrage Syntax, die von Windows Search verwendet wird, um den Index abzufragen und Suchparameter zu verfeinern und einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-104">Advanced Query Syntax (AQS) is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="ac2b1-105">AQS wird von Entwicklern verwendet, um Abfragen Programm gesteuert zu erstellen (und von Benutzern, um Ihre Suchparameter einzuschränken).</span><span class="sxs-lookup"><span data-stu-id="ac2b1-105">AQS is employed by developers to build queries programmatically (and by users to narrow their search parameters).</span></span> <span data-ttu-id="ac2b1-106">Kanonische AQS wurde in Windows 7 eingeführt und muss in Windows 7 und höher zum programmgesteuerten Generieren von AQS-Abfragen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-106">Canonical AQS was introduced in Windows 7 and must be used in Windows 7 and later to programmatically generate AQS queries.</span></span>

<span data-ttu-id="ac2b1-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="ac2b1-108">Informationen zur erweiterten Abfrage Syntax</span><span class="sxs-lookup"><span data-stu-id="ac2b1-108">About Advanced Query Syntax</span></span>](#about-advanced-query-syntax)
    -   [<span data-ttu-id="ac2b1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac2b1-109">Examples</span></span>](#examples)
    -   [<span data-ttu-id="ac2b1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac2b1-110">Properties</span></span>](#properties)
-   [<span data-ttu-id="ac2b1-111">Schlüsselwort Verwendung in lokalen Sprachen</span><span class="sxs-lookup"><span data-stu-id="ac2b1-111">Keyword Use in Local Languages</span></span>](#keyword-use-in-local-languages)
-   [<span data-ttu-id="ac2b1-112">Kanonische Erweiterte Abfrage Syntax in Windows 7</span><span class="sxs-lookup"><span data-stu-id="ac2b1-112">Canonical Advanced Query Syntax in Windows 7</span></span>](#canonical-advanced-query-syntax-in-windows-7)
    -   [<span data-ttu-id="ac2b1-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac2b1-113">Examples</span></span>](#examples)
    -   [<span data-ttu-id="ac2b1-114">Abfrage Operatoren</span><span class="sxs-lookup"><span data-stu-id="ac2b1-114">Query Operators</span></span>](#query-operators)
    -   [<span data-ttu-id="ac2b1-115">Abfrage Werte</span><span class="sxs-lookup"><span data-stu-id="ac2b1-115">Query Values</span></span>](#query-values)
-   [<span data-ttu-id="ac2b1-116">Bereichs Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="ac2b1-116">Scope Restrictions</span></span>](#scope-restrictions)
-   [<span data-ttu-id="ac2b1-117">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ac2b1-117">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="ac2b1-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ac2b1-118">Related topics</span></span>](#related-topics)

## <a name="about-advanced-query-syntax"></a><span data-ttu-id="ac2b1-119">Informationen zur erweiterten Abfrage Syntax</span><span class="sxs-lookup"><span data-stu-id="ac2b1-119">About Advanced Query Syntax</span></span>

<span data-ttu-id="ac2b1-120">Eine Abfrage besteht aus grundlegenden Abfragen, die mit and, or und Not verbunden sind, wie in der folgenden Beispiel Syntax gezeigt:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-120">A query consists of basic queries connected with AND, OR, and NOT, as shown in the following example syntax:</span></span>

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> <span data-ttu-id="ac2b1-121">Bei AQS wird die Groß-/Kleinschreibung nicht beachtet, mit Ausnahme von and, or, und Not, das in Großbuchstaben vorliegen muss.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-121">AQS is not case sensitive, with the exception of AND, OR, and NOT, which must be in all uppercase.</span></span>

 

<span data-ttu-id="ac2b1-122">Wenn eine Abfrage zwei oder mehr Verwendungen von and oder or aufweist, werden Sie von links nach rechts gebunden, unabhängig davon, ob es sich um and oder or handelt.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-122">If a query has two or more uses of AND or OR, they will bind from left to right, regardless of whether it is AND or OR.</span></span> <span data-ttu-id="ac2b1-123">Das heißt, die Abfrage "Apple und Birnen oder Plum" wird so interpretiert, als ob Sie als "(Apple, Birne) oder Plum" geschrieben wäre, und die Abfrage "Apple", "PEAR" und "Plum" wird so interpretiert, als ob Sie als "(Apple oder Birne) und Plum" geschrieben wäre.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-123">That is, the query, "apple AND pear OR plum" will be interpreted as if it were written as "(apple AND pear) OR plum", and the query, "apple OR pear AND plum", will be interpreted as if it were written as "(apple OR pear) AND plum".</span></span> <span data-ttu-id="ac2b1-124">Wenn ein Dokument das Wort Plum, aber weder Apple noch Birnen enthält, gibt die erste Abfrage es zurück, die zweite Abfrage jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-124">So if a document contains the word plum but neither apple, nor pear, the first query will return it but the second query will not.</span></span> <span data-ttu-id="ac2b1-125">Daher wird empfohlen, dass Sie für jede Abfrage, die and und or kombiniert, explizite Klammern verwenden, um Fehler oder Fehlinterpretationen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-125">Hence, we recommend that you use explicit parentheses for any query that mixes AND and OR to avoid mistakes or misinterpretations.</span></span>

<span data-ttu-id="ac2b1-126">Eine grundlegende Abfrage sucht nach Elementen, die eine Einschränkung für eine Eigenschaft erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-126">A basic query searches for items that satisfy a restriction over a property.</span></span> <span data-ttu-id="ac2b1-127">Der einzige erforderliche Teil einer grundlegenden Abfrage ist der Einschränkungs-oder Suchwert.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-127">The only required portion of a basic query is the restriction or search value.</span></span> <span data-ttu-id="ac2b1-128">Wenn Sie keine Eigenschaft angeben, durchsucht Windows Search alle Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-128">If you do not specify a property, Windows Search searches all properties.</span></span> <span data-ttu-id="ac2b1-129"><restr> stellt die Such Einschränkung dar.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-129"><restr> represents the search restriction.</span></span>

<span data-ttu-id="ac2b1-130">Die folgenden Formulare für eine einfache Abfrage sind gültig:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-130">The following forms for a basic query are valid:</span></span>

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

<span data-ttu-id="ac2b1-131">Eine Eigenschaft wird durch ein Schlüsselwort wie "Author" oder "size" oder durch einen kanonischen Eigenschaftsnamen wie " [System. DateModified](../properties/props-system-datemodified.md)" angegeben.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-131">A property is designated by a keyword such as author or size, or by a canonical property name such as [System.DateModified](../properties/props-system-datemodified.md).</span></span> <span data-ttu-id="ac2b1-132">Gültige Formulare für eine Eigenschaft sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-132">Valid forms for a property are as follows:</span></span>

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

<span data-ttu-id="ac2b1-133">Ein Operator gibt einen Vorgang an, z. b. < oder =.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-133">An operator indicates an operation such as < or =.</span></span> <span data-ttu-id="ac2b1-134">Eine Liste gültiger Operatoren finden Sie im Abschnitt Abfrage Operatoren weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-134">For a list of valid operators, see the Query Operators section later in this topic.</span></span>

<span data-ttu-id="ac2b1-135">Eine grundlegende Einschränkung ist eine einfache Einschränkung für eine Eigenschaft, die ohne Klammern geschrieben werden kann:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-135">A basic restriction is a simple restriction on a property that can be written without parentheses:</span></span>

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

<span data-ttu-id="ac2b1-136">Eine Einschränkung ist ein Suchwert, z. b. ein Zahlenwert oder ein Zeichen folgen Wert, optional mit einem-Operator.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-136">A restriction is a search value such as a number value or string value, optionally with an operator.</span></span> <span data-ttu-id="ac2b1-137">Gültige Formulare für eine Einschränkung lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-137">Valid forms for a restriction are as follows:</span></span>

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

<span data-ttu-id="ac2b1-138">Wenn Sie keinen Operator angeben, wählt Windows Search den am besten geeigneten Operator für die Abfrage aus:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-138">If you do not specify an operator, Windows Search chooses the most appropriate operator for your query:</span></span>

-   <span data-ttu-id="ac2b1-139">Für eine Zeichen folgen Eigenschaft wird der COP \_ Word- \_ Operator StartWith $< angenommen.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-139">For a string property, the COP\_WORD\_STARTSWITH $< operator is assumed.</span></span>
-   <span data-ttu-id="ac2b1-140">Für alle anderen Eigenschaften wird der COP \_ EQUAL =-Operator angenommen.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-140">For all other properties, the COP\_EQUAL = operator is assumed.</span></span>

<span data-ttu-id="ac2b1-141">Für die programmgesteuerte Verwendung von AQS wird empfohlen, dass Sie immer über einen expliziten Operator verfügen.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-141">For the programmatic use of AQS, we recommend that you always have an explicit operator.</span></span> <span data-ttu-id="ac2b1-142">Das gültige Formular für die Suche nach einem einfachen Wert oder Wertebereich lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-142">The valid form for searching a simple value or value range is as follows:</span></span>

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

<span data-ttu-id="ac2b1-143">Ein einfacher Wert kann aus einem der folgenden Typen bestehen:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-143">A simple value can consist of any of the following types:</span></span>

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a><span data-ttu-id="ac2b1-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac2b1-144">Examples</span></span>

<span data-ttu-id="ac2b1-145">Eine Abfrage, die nach einem Dokument mit der von Theresa oder Lee erstellten Phase "Letztes Quartal" sucht und im Ordner "MyDocs" gespeichert wurde, kombiniert drei grundlegende Abfragen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-145">A query that searches for a document containing the phase "last quarter," authored by Theresa or Lee, and that was saved to the folder MyDocs, combines three basic queries as follows:</span></span>

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

<span data-ttu-id="ac2b1-146">Die drei grundlegenden Abfragen lauten:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-146">The three basic queries are:</span></span>

-   <span data-ttu-id="ac2b1-147">"Letztes Quartal"</span><span class="sxs-lookup"><span data-stu-id="ac2b1-147">"last quarter"</span></span>
-   <span data-ttu-id="ac2b1-148">Autor: (Theresa oder Lee)</span><span class="sxs-lookup"><span data-stu-id="ac2b1-148">author:(theresa OR lee)</span></span>
-   <span data-ttu-id="ac2b1-149">Ordner: MyDocs</span><span class="sxs-lookup"><span data-stu-id="ac2b1-149">folder:MyDocs</span></span>

<span data-ttu-id="ac2b1-150">Eine einfache Abfrage, die kanonische Syntax verwendet, lautet:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-150">A basic query that uses canonical syntax is:</span></span>

``` syntax
System.Size:>1kb
```

### <a name="properties"></a><span data-ttu-id="ac2b1-151">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac2b1-151">Properties</span></span>

<span data-ttu-id="ac2b1-152">Auf Eigenschaften wird durch ein Schlüsselwort verwiesen, das in Windows 7 und höher als kanonischer Eigenschaftsname dienen kann.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-152">Properties are referred to by a keyword, which can be a canonical property name in Windows 7 and later.</span></span> <span data-ttu-id="ac2b1-153">AQS in der Windows-Benutzeroberfläche kann die Bezeichnung anstelle des kanonischen Eigenschaften namens verwenden, z. b. "Author" anstelle von " [System. Author](../properties/props-system-author.md)".</span><span class="sxs-lookup"><span data-stu-id="ac2b1-153">AQS in the Windows UI can use the label instead of the canonical property name, such as author instead of [System.Author](../properties/props-system-author.md).</span></span> <span data-ttu-id="ac2b1-154">In Windows Vista und früheren Versionen war es möglich, englische Bezeichnungen unabhängig von der Benutzeroberflächen Sprache zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-154">In Windows Vista and earlier it was possible to use English labels regardless of the UI language.</span></span> <span data-ttu-id="ac2b1-155">In Windows 7 und höher erkennt Windows Search Schlüsselwörter nur in der aktuellen Standardsprache der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-155">In Windows 7 and later, Windows Search recognizes keywords in the current default UI language only.</span></span>

### <a name="support-for-custom-properties"></a><span data-ttu-id="ac2b1-156">Unterstützung für benutzerdefinierte Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac2b1-156">Support for Custom Properties</span></span>

<span data-ttu-id="ac2b1-157">In Windows Vista und früheren Versionen waren benutzerdefinierte Eigenschaften in AQS nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-157">In Windows Vista and earlier, custom properties were not available in AQS.</span></span> <span data-ttu-id="ac2b1-158">In Windows 7 und höher funktioniert AQS mit benutzerdefinierten Eigenschaften, die im-Eigenschaften System registriert sind.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-158">In Windows 7 and later, AQS works with custom properties that are registered with the property system.</span></span> <span data-ttu-id="ac2b1-159">Weitere Informationen zum Erstellen von benutzerdefinierten Eigenschaften finden Sie unter Eigenschaften [System](../properties/building-property-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="ac2b1-159">For more information on creating custom properties, see [Property System](../properties/building-property-handlers.md).</span></span>

### <a name="datetime-properties-in-windows-8"></a><span data-ttu-id="ac2b1-160">DateTime-Eigenschaften in Windows 8</span><span class="sxs-lookup"><span data-stu-id="ac2b1-160">DateTime properties in Windows 8</span></span>

<span data-ttu-id="ac2b1-161">Ab Windows 8 unterstützen DateTime-Eigenschaften (z. b [. System. DateModified](../properties/props-system-datemodified.md)) das in [ISO-8601](https://www.w3.org/TR/NOTE-datetime)angegebene kanonische Datums-und Uhrzeit Format, optional einschließlich der UTC-Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-161">As of Windows 8, DateTime properties (like [System.DateModified](../properties/props-system-datemodified.md)) support the canonical date and time format specified by [ISO-8601](https://www.w3.org/TR/NOTE-datetime), optionally including the UTC time zone.</span></span>

-   <span data-ttu-id="ac2b1-162">**Windows 8 und früher, Datum/Uhrzeit ohne UTC-Zeitzone:** *yyyy* - *mm* - *ddThh*:*mm*:*SS*</span><span class="sxs-lookup"><span data-stu-id="ac2b1-162">**Windows 8 and earlier, date-time without UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ss*</span></span>

    <span data-ttu-id="ac2b1-163">Dieses Format gibt eine lokale Uhrzeit an, unabhängig vom Benutzer-oder System Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-163">This format specifies a local time, regardless of the user or system locale.</span></span>

-   <span data-ttu-id="ac2b1-164">**Windows 8, Datum und Uhrzeit mit UTC-Zeitzone:** *yyyy* - *mm* - *ddThh*:*mm*:*sstzd*</span><span class="sxs-lookup"><span data-stu-id="ac2b1-164">**Windows 8, date-time with UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ssTZD*</span></span>

    <span data-ttu-id="ac2b1-165">Dieses Format gibt eine Uhrzeit in der angegebenen UTC-Zeitzone an.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-165">This format specifies a time at the specified UTC time zone.</span></span>

## <a name="keyword-use-in-local-languages"></a><span data-ttu-id="ac2b1-166">Schlüsselwort Verwendung in lokalen Sprachen</span><span class="sxs-lookup"><span data-stu-id="ac2b1-166">Keyword Use in Local Languages</span></span>

<span data-ttu-id="ac2b1-167">In Windows 7 und höher funktionieren mnetmonische Schlüsselwörter nur in der Systemsprache, wie z. b. deutschen Schlüsselwörtern nur auf einem deutschen Betriebssystem und englischen Schlüsselwörtern nur in einem englischen Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-167">In Windows 7 and later, mnemonic keywords work in the system language only, such as German keywords only on a German operating system, and English keywords only on an English operating system.</span></span> <span data-ttu-id="ac2b1-168">[System. Author](../properties/props-system-author.md) ist ein kanonisches Schlüsselwort, und der mnetmonische Wert für die System. Author-Eigenschaft ist beispielsweise Author.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-168">[System.Author](../properties/props-system-author.md) is a canonical keyword, and the mnemonic value for the System.Author property is Author, for example.</span></span> <span data-ttu-id="ac2b1-169">Durch die Einführung von kanonischen Schlüsselwörtern wird die Tatsache kompensiert, dass englische mmaische Schlüsselwörter nicht mehr universell auf allen Betriebssystemen erkannt werden, und zwar unabhängig von der Sprache, wie es in Windows Vista und früheren Versionen der Fall war.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-169">The introduction of canonical keywords compensates for the fact that English mnemonic keywords are no longer universally recognized on all operating systems regardless of language, as was the case in Windows Vista and earlier.</span></span>

> [!Note]  
> <span data-ttu-id="ac2b1-170">In Windows 7 und höher erkennt Windows Search Schlüsselwörter nur in der aktuellen Standardsprache und nicht in englischer Sprache, es sei denn, English ist die aktuelle Standardsprache.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-170">In Windows 7 and later, Windows Search recognizes keywords in the current default language only, and not in English unless English is the current default.</span></span> <span data-ttu-id="ac2b1-171">Es wird empfohlen, dass Entwickler immer eine kanonische Syntax verwenden, damit Ihre Anwendung keine Sprachprobleme mit Schlüsselwörtern hat.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-171">We recommend that developers always use canonical syntax so that their application won't have language problems with keywords.</span></span>

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a><span data-ttu-id="ac2b1-172">Kanonische Erweiterte Abfrage Syntax in Windows 7</span><span class="sxs-lookup"><span data-stu-id="ac2b1-172">Canonical Advanced Query Syntax in Windows 7</span></span>

<span data-ttu-id="ac2b1-173">Die kanonische Syntax wurde für Schlüsselwörter in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-173">Canonical syntax was introduced for keywords in Windows 7.</span></span> <span data-ttu-id="ac2b1-174">Ein Beispiel für eine Abfrage mit einer kanonischen-Eigenschaft ist `System.Message.FromAddress:=me@microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="ac2b1-174">An example of a query with a canonical property is `System.Message.FromAddress:=me@microsoft.com`.</span></span> <span data-ttu-id="ac2b1-175">Beim Codieren von Abfragen in Anwendungen, die unter Windows 7 und höher ausgeführt werden, müssen Sie kanonische Syntax verwenden, um AQS-Abfragen Programm gesteuert zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-175">When coding queries in applications running on Windows 7 and later, you must use canonical syntax to programmatically generate AQS queries.</span></span> <span data-ttu-id="ac2b1-176">Wenn Sie keine kanonische Syntax verwenden und die Anwendung in einer Gebiets Schema-oder Benutzeroberflächen Sprache bereitgestellt wird, die sich von der Sprache im Anwendungscode unterscheidet, werden die Abfragen nicht ordnungsgemäß interpretiert.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-176">If you do not use canonical syntax and your application is deployed in a locale or UI language different from the language in the application code, your queries will not be interpreted correctly.</span></span>

<span data-ttu-id="ac2b1-177">Die Konventionen für die kanonische Schlüsselwort Syntax lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-177">The conventions for canonical keyword syntax are as follows:</span></span>

-   <span data-ttu-id="ac2b1-178">Die kanonische Syntax für eine Eigenschaft ist Ihr kanonischer Name, z `System.Photo.LightSource` . b..</span><span class="sxs-lookup"><span data-stu-id="ac2b1-178">The canonical syntax for a property is its canonical name, such as `System.Photo.LightSource`.</span></span> <span data-ttu-id="ac2b1-179">Kanonische Namen beachten die Groß-/Kleinschreibung nicht.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-179">Canonical names are not case sensitive.</span></span>
-   <span data-ttu-id="ac2b1-180">Die kanonische Syntax für die booleschen Operatoren besteht aus den Schlüsselwörtern and, or und Not in Großbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-180">The canonical syntax for the Boolean operators consists of the keywords AND, OR, and NOT, in all uppercase.</span></span>
-   <span data-ttu-id="ac2b1-181">Die Operatoren <, >, = usw., werden nicht lokalisiert und sind daher auch Teil der kanonischen Syntax.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-181">The operators <, >, =, and so forth, are not localized and are thus also part of the canonical syntax.</span></span>
-   <span data-ttu-id="ac2b1-182">Wenn eine Eigenschaft `P` Werte oder Bereiche mit dem Namen N ₁ bis NK aufzählt, ist die kanonische Syntax für den *I* Th-Wert oder-Bereich der kanonische Name für P, gefolgt vom Zeichen gefolgt von \# n <sub>I</sub>, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-182">If a property `P` has enumerated values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for P, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   <span data-ttu-id="ac2b1-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` usw.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA`, and so forth.</span></span>
-   <span data-ttu-id="ac2b1-184">Für einen definierten Semantik Typ t mit Werten oder Bereichen mit dem Namen N ₁ bis NK ist die kanonische Syntax für den *I* Th-Wert oder-Bereich der kanonische Name für t, gefolgt vom Zeichen gefolgt von \# n <sub>I</sub>, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-184">For a defined semantic type T with values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for T, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   <span data-ttu-id="ac2b1-185">Bei Literalwerten wie Wörtern oder Ausdrücken ist die kanonische Syntax die gleiche wie die reguläre Syntax.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-185">For literal values such as words or phrases, the canonical syntax is the same as the regular syntax.</span></span> <span data-ttu-id="ac2b1-186">Beispiele für Abfragen mit Literalwerten in kanonischer Syntax:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-186">Examples of queries with literal values in canonical syntax are:</span></span>
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> <span data-ttu-id="ac2b1-187">Es gibt keine kanonische Syntax für Zahlen in Windows 7 und höher.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-187">There is no canonical syntax for numbers in Windows 7 and later.</span></span> <span data-ttu-id="ac2b1-188">Da Gleit Komma Formate sich zwischen den Gebiets Schemata unterscheiden, wird die Verwendung einer kanonischen Abfrage, die eine Gleit Komma Konstante einschließt, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-188">Because floating point formats vary among locales, the use of a canonical query that involves a floating point constant is not supported.</span></span> <span data-ttu-id="ac2b1-189">Ganzzahlige Konstanten hingegen können nur mit Ziffern (keine Trennzeichen für Tausende) geschrieben werden und können in kanonischen Abfragen in Windows 7 und höher sicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-189">Integer constants, in contrast, can be written using only digits (no separators for thousands) and can be safely used in canonical queries in Windows 7 and later.</span></span>

 

### <a name="examples"></a><span data-ttu-id="ac2b1-190">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac2b1-190">Examples</span></span>

<span data-ttu-id="ac2b1-191">In der folgenden Tabelle sind einige Beispiele für kanonische Eigenschaften und die Syntax für deren Verwendung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-191">The following table shows some examples of canonical properties and the syntax for using them.</span></span>



| <span data-ttu-id="ac2b1-192">Typ der kanonischen Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ac2b1-192">Type of canonical property</span></span> | <span data-ttu-id="ac2b1-193">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ac2b1-193">Example</span></span>                                                                                     | <span data-ttu-id="ac2b1-194">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac2b1-194">Syntax</span></span>                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2b1-195">Zeichenfolgenwert</span><span class="sxs-lookup"><span data-stu-id="ac2b1-195">String value</span></span>               | [<span data-ttu-id="ac2b1-196">System.Author</span><span class="sxs-lookup"><span data-stu-id="ac2b1-196">System.Author</span></span>](../properties/props-system-author.md)<br/>    | <span data-ttu-id="ac2b1-197">Der Zeichen folgen Wert wird in der Author-Eigenschaft nach gesucht:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-197">The string value is searched for in the author property:</span></span> <br/>`System.Author:Jacobs`                                                                                                                                                              |
| <span data-ttu-id="ac2b1-198">Enumerationsbereich</span><span class="sxs-lookup"><span data-stu-id="ac2b1-198">Enumeration range</span></span>          | [<span data-ttu-id="ac2b1-199">System. Priority</span><span class="sxs-lookup"><span data-stu-id="ac2b1-199">System.Priority</span></span>](../properties/props-system-priority.md)             | <span data-ttu-id="ac2b1-200">Die Priority-Eigenschaft kann einen numerischen Wertebereich aufweisen:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-200">The priority property can have a numerical value range:</span></span><br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| <span data-ttu-id="ac2b1-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="ac2b1-201">Boolean</span></span>                    | [<span data-ttu-id="ac2b1-202">System. IsDeleted</span><span class="sxs-lookup"><span data-stu-id="ac2b1-202">System.IsDeleted</span></span>](../properties/props-system-isdeleted.md)<br/> | <span data-ttu-id="ac2b1-203">Boolesche Werte können mit jeder booleschen Eigenschaft verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-203">Boolean values can be used with any Boolean property:</span></span><br/><span data-ttu-id="ac2b1-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True` und `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span><span class="sxs-lookup"><span data-stu-id="ac2b1-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True`, and `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span></span>                                                             |
| <span data-ttu-id="ac2b1-205">Numerisch</span><span class="sxs-lookup"><span data-stu-id="ac2b1-205">Numerical</span></span>                  | [<span data-ttu-id="ac2b1-206">System. Size</span><span class="sxs-lookup"><span data-stu-id="ac2b1-206">System.Size</span></span>](../properties/props-system-size.md)<br/>      | <span data-ttu-id="ac2b1-207">Es ist nicht möglich, eine kanonische Abfrage, die eine Gleit Komma Konstante umfasst, sicher zu schreiben, da Gleit Komma Formate sich zwischen den Gebiets Schemata unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-207">It is not possible to write safely a canonical query that involves a floating point constant, because floating point formats vary among locales.</span></span> <span data-ttu-id="ac2b1-208">Ganze Zahlen müssen ohne Trennzeichen für Tausende geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-208">Integers must be written with no separators for thousands.</span></span> <span data-ttu-id="ac2b1-209">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-209">For example:</span></span><br/>`System.Size:<12345` |



 

<span data-ttu-id="ac2b1-210">Weitere Informationen über kanonische Eigenschaften und das Eigenschaften System finden Sie unter [Systemeigenschaften](../properties/props.md).</span><span class="sxs-lookup"><span data-stu-id="ac2b1-210">For more information about canonical properties and the property system generally, see [System Properties](../properties/props.md).</span></span> <span data-ttu-id="ac2b1-211">Alternativ dazu können Sie auch die öffentlichen Header Dateien lesen.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-211">Alternatively, refer to the public header files.</span></span>

### <a name="query-operators"></a><span data-ttu-id="ac2b1-212">Abfrageoperatoren</span><span class="sxs-lookup"><span data-stu-id="ac2b1-212">Query Operators</span></span>

<span data-ttu-id="ac2b1-213">Wenn eine Eigenschaft, p, mehrere Werte für ein Element aufweist, gibt eine AQS-Abfrage für p: <restr> das Element zurück, wenn <restr> für mindestens einen der Werte **true** ist.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-213">If a property, p, has multiple values for some item, an AQS query for p:<restr> returns the item if <restr> is **true** for at least one of the values.</span></span> <span data-ttu-id="ac2b1-214">( <restr> stellt eine Einschränkung dar.)</span><span class="sxs-lookup"><span data-stu-id="ac2b1-214">(<restr> represents a restriction.)</span></span>

<span data-ttu-id="ac2b1-215">Die in der folgenden Tabelle aufgeführte Syntax besteht aus einem Operator, einem Operator Symbol, einem Beispiel und einer Beispiel Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-215">The syntax listed in the following table consists of an operator, operator symbol, example and example description.</span></span> <span data-ttu-id="ac2b1-216">Der Operator und das Symbol können in jeder beliebigen Sprache verwendet und in beliebige Abfragen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-216">The operator and symbol can be used in any language and included in any query.</span></span> <span data-ttu-id="ac2b1-217">Verwenden Sie nicht die entsprechenden Cop- \_ oder Cop- \_ Anwendungs \_ spezifischen Operatoren.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-217">Do not use the COP\_IMPLICIT or COP\_APPLICATION\_SPECIFIC operators.</span></span> <span data-ttu-id="ac2b1-218">Einige der Operatoren verfügen über austauschbare Symbole.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-218">Some of the operators have interchangeable symbols.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ac2b1-219">Operator</span><span class="sxs-lookup"><span data-stu-id="ac2b1-219">Operator</span></span></th>
<th><span data-ttu-id="ac2b1-220">Symbol</span><span class="sxs-lookup"><span data-stu-id="ac2b1-220">Symbol</span></span></th>
<th><span data-ttu-id="ac2b1-221">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ac2b1-221">Example</span></span></th>
<th><span data-ttu-id="ac2b1-222">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac2b1-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ac2b1-223">COP_EQUAL</span><span class="sxs-lookup"><span data-stu-id="ac2b1-223">COP_EQUAL</span></span></td>
<td>=<br/></td>
<td><span data-ttu-id="ac2b1-224">System. File Extension: = &quot; . txt&quot;</span><span class="sxs-lookup"><span data-stu-id="ac2b1-224">System.FileExtension:=&quot;.txt&quot;</span></span><br/></td>
<td><span data-ttu-id="ac2b1-225">Der Wert ist "String &quot; <em>. txt</em>" &quot; .</span><span class="sxs-lookup"><span data-stu-id="ac2b1-225">The value is the string &quot;<em>.txt</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac2b1-226">COP_NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="ac2b1-226">COP_NOTEQUAL</span></span></td>
<td><span data-ttu-id="ac2b1-227">≠</span><span class="sxs-lookup"><span data-stu-id="ac2b1-227">≠</span></span><br/> -<br/> &lt;&gt;<br/> <span data-ttu-id="ac2b1-228">NICHT</span><span class="sxs-lookup"><span data-stu-id="ac2b1-228">NOT</span></span><br/> - -<br/></td>
<td><span data-ttu-id="ac2b1-229">System. Kind: ≠-Bild</span><span class="sxs-lookup"><span data-stu-id="ac2b1-229">System.Kind:≠picture</span></span><br/> <span data-ttu-id="ac2b1-230">System. Photo. DateTaken:-[] ¹</span><span class="sxs-lookup"><span data-stu-id="ac2b1-230">System.Photo.DateTaken:-[]¹</span></span><br/> <span data-ttu-id="ac2b1-231">System. Kind: &lt; &gt; Bild</span><span class="sxs-lookup"><span data-stu-id="ac2b1-231">System.Kind:&lt;&gt;picture</span></span><br/> <span data-ttu-id="ac2b1-232">System. Kind: nicht Bild</span><span class="sxs-lookup"><span data-stu-id="ac2b1-232">System.Kind:NOT picture</span></span><br/> <span data-ttu-id="ac2b1-233">System. Kind:--Bild</span><span class="sxs-lookup"><span data-stu-id="ac2b1-233">System.Kind:- -picture</span></span><br/></td>
<td><span data-ttu-id="ac2b1-234">Die <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> -Eigenschaft ist kein Bild.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-234">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span><br/> <span data-ttu-id="ac2b1-235">Die <a href="/windows/desktop/properties/props-system-photo-datetaken">System. Photo. DateTaken</a> -Eigenschaft weist einen Wert auf.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-235">The <a href="/windows/desktop/properties/props-system-photo-datetaken">System.Photo.DateTaken</a> property has a value.</span></span><br/> <span data-ttu-id="ac2b1-236">Die <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> -Eigenschaft ist kein Bild.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-236">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="ac2b1-237">Die <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> -Eigenschaft ist kein Bild.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-237">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="ac2b1-238">Doppelte not-Operatoren, die auf dieselbe Eigenschaft angewendet werden, werden nicht abgebrochen. Daher ist System. Kind:--Picture Äquivalent zu System. Kind:-Picture und System. Kind: Not Picture.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-238">Double NOT operators applied to the same property do not cancel out. Hence, System.Kind:- -picture is equivalent to System.Kind:-picture and System.Kind:NOT picture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac2b1-239">COP_LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="ac2b1-239">COP_LESSTHAN</span></span></td>
<td>&lt;<br/></td>
<td><span data-ttu-id="ac2b1-240">System. size: &lt; 1 KB</span><span class="sxs-lookup"><span data-stu-id="ac2b1-240">System.Size:&lt;1kb</span></span><br/></td>
<td><span data-ttu-id="ac2b1-241">Dieser Wert ist kleiner als <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-241">This value is less than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac2b1-242">COP_GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="ac2b1-242">COP_GREATERTHAN</span></span></td>
<td>&gt;<br/></td>
<td><span data-ttu-id="ac2b1-243">System. itemdate: &gt; System. structuredquerytype. DateTime # heute</span><span class="sxs-lookup"><span data-stu-id="ac2b1-243">System.ItemDate:&gt;System.StructuredQueryType.DateTime#Today</span></span><br/></td>
<td><span data-ttu-id="ac2b1-244">Dieser Wert ist größer als <em>heute</em>.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-244">This value is greater than <em>today</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac2b1-245">COP_LESSTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="ac2b1-245">COP_LESSTHANOREQUAL</span></span></td>
<td>&lt;=<br/> <span data-ttu-id="ac2b1-246">≤</span><span class="sxs-lookup"><span data-stu-id="ac2b1-246">≤</span></span><br/></td>
<td><span data-ttu-id="ac2b1-247">System. size: &lt; = 1 KB</span><span class="sxs-lookup"><span data-stu-id="ac2b1-247">System.Size:&lt;=1kb</span></span><br/></td>
<td><span data-ttu-id="ac2b1-248">Dieser Wert ist kleiner oder gleich <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-248">This value is less than or equal to <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac2b1-249">COP_GREATERTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="ac2b1-249">COP_GREATERTHANOREQUAL</span></span></td>
<td>&gt;=<br/> <span data-ttu-id="ac2b1-250">≥</span><span class="sxs-lookup"><span data-stu-id="ac2b1-250">≥</span></span><br/></td>
<td><span data-ttu-id="ac2b1-251">System. size: &gt; = 1 KB</span><span class="sxs-lookup"><span data-stu-id="ac2b1-251">System.Size:&gt;=1kb</span></span><br/></td>
<td><span data-ttu-id="ac2b1-252">Dieser Wert ist gleich oder größer als <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-252">This value is equal to or greater than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac2b1-253">COP_VALUE_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="ac2b1-253">COP_VALUE_STARTSWITH</span></span></td>
<td>~&lt;<br/></td>
<td><span data-ttu-id="ac2b1-254">System. filename: ~ &lt; &quot; C++ Primer&quot;</span><span class="sxs-lookup"><span data-stu-id="ac2b1-254">System.FileName:~&lt;&quot;C++ Primer&quot;</span></span><br/></td>
<td><span data-ttu-id="ac2b1-255">Sucht nach Elementen, bei denen der Dateiname mit den Zeichen &quot; <em>C++ "Primer</em>" beginnt &quot; .</span><span class="sxs-lookup"><span data-stu-id="ac2b1-255">Finds items where the file name begins with the characters &quot;<em>C++ Primer</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac2b1-256">COP_VALUE_ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="ac2b1-256">COP_VALUE_ENDSWITH</span></span></td>
<td>~&gt;<br/></td>
<td><span data-ttu-id="ac2b1-257">System. Photo. CameraModel: ~ &gt; Non</span><span class="sxs-lookup"><span data-stu-id="ac2b1-257">System.Photo.CameraModel:~&gt;non</span></span><br/></td>
<td><span data-ttu-id="ac2b1-258">Sucht nach Elementen, bei denen der Eigenschafts Wert mit den Zeichen <em>nicht</em>endet.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-258">Finds items where the property value ends with the characters <em>non</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac2b1-259">COP_VALUE_CONTAINS</span><span class="sxs-lookup"><span data-stu-id="ac2b1-259">COP_VALUE_CONTAINS</span></span></td>
<td>~=<br/> ~~<br/></td>
<td><span data-ttu-id="ac2b1-260">System. Subject. ~ = Round</span><span class="sxs-lookup"><span data-stu-id="ac2b1-260">System.Subject.~=round</span></span> <br/> <span data-ttu-id="ac2b1-261">System. search. autosummary: ~ ~ Round</span><span class="sxs-lookup"><span data-stu-id="ac2b1-261">System.Search.Autosummary:~~round</span></span><br/></td>
<td><span data-ttu-id="ac2b1-262">Sucht eine Meldung, die diese Zeichenfolge im Betreff hat, und entspricht &quot; z. b. g-<em>runden</em> Regeln &quot; .</span><span class="sxs-lookup"><span data-stu-id="ac2b1-262">Finds a message that has this string in the subject, and will match &quot;g<em>round</em> rules&quot; for example.</span></span><br/> <span data-ttu-id="ac2b1-263">Sucht alle Elemente mit einer autosummary, die die Zeichen <em>Runde</em>enthält.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-263">Finds all items with an Autosummary that contains the characters <em>round</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac2b1-264">COP_VALUE_NOTCONTAINS</span><span class="sxs-lookup"><span data-stu-id="ac2b1-264">COP_VALUE_NOTCONTAINS</span></span></td>
<td><span data-ttu-id="ac2b1-265">~!</span><span class="sxs-lookup"><span data-stu-id="ac2b1-265">~!</span></span><br/></td>
<td><span data-ttu-id="ac2b1-266">System. Author: ~! &quot; Sanjay&quot;</span><span class="sxs-lookup"><span data-stu-id="ac2b1-266">System.Author:~!&quot;sanjay&quot;</span></span><br/></td>
<td><span data-ttu-id="ac2b1-267">Sucht Autoren, die nicht über die Zeichenfolge &quot; <em>Sanjay</em> verfügen &quot; .</span><span class="sxs-lookup"><span data-stu-id="ac2b1-267">Finds authors that do not have the character sequence&quot;<em>sanjay</em>&quot; in them.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac2b1-268">COP_DOSWILDCARDS</span><span class="sxs-lookup"><span data-stu-id="ac2b1-268">COP_DOSWILDCARDS</span></span></td>
<td>~ <br/></td>
<td><span data-ttu-id="ac2b1-269">System. filename: ~ &quot; MIC? osoft W \* d&quot;</span><span class="sxs-lookup"><span data-stu-id="ac2b1-269">System.FileName:~&quot;Mic?osoft W\*d&quot;</span></span><br/></td>
<td><span data-ttu-id="ac2b1-270">Sucht nach Dateien, bei denen der Dateiname mit <em>MIC</em>beginnt, gefolgt von einem Zeichen, gefolgt von <em>osoft w</em>, gefolgt von allen Zeichen, die mit <em>d</em>enden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-270">Finds files where the file name starts with <em>Mic</em>, followed by some character, followed by <em>osoft w</em>, followed by any characters ending with <em>d</em>.</span></span> <br/> <span data-ttu-id="ac2b1-271">Mit dem Zeichen „?“</span><span class="sxs-lookup"><span data-stu-id="ac2b1-271">The ?</span></span> <span data-ttu-id="ac2b1-272">und \* Zeichen werden nicht buchstäblich interpretiert und funktionieren wie Platzhalter Zeichen im DOS-Stil:</span><span class="sxs-lookup"><span data-stu-id="ac2b1-272">and \* characters are not interpreted literally, and work like DOS-style wildcard characters:</span></span><br/>
<ul>
<li><span data-ttu-id="ac2b1-273">?</span><span class="sxs-lookup"><span data-stu-id="ac2b1-273">?</span></span> <span data-ttu-id="ac2b1-274">entspricht einem beliebigen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-274">matches one arbitrary character.</span></span></li>
<li><span data-ttu-id="ac2b1-275">\* entspricht 0 (null) oder mehr beliebigen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-275">\* matches zero or more arbitrary characters.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac2b1-276">COP_WORD_EQUAL</span><span class="sxs-lookup"><span data-stu-id="ac2b1-276">COP_WORD_EQUAL</span></span></td>
<td>$=<br/> $$<br/></td>
<td><span data-ttu-id="ac2b1-277">System. StructuredQuery. Virtual. from: $ = &quot; Sanjay Jacobs&quot;</span><span class="sxs-lookup"><span data-stu-id="ac2b1-277">System.StructuredQuery.Virtual.From:$=&quot;Sanjay Jacobs&quot;</span></span><br/></td>
<td><span data-ttu-id="ac2b1-278">Für Windows 7 und höher.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-278">For Windows 7 and later.</span></span> <span data-ttu-id="ac2b1-279">Sucht den Ausdruck &quot; <em>Sanjay Jacobs</em> &quot; in allen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-279">Finds the phrase &quot;<em>Sanjay Jacobs</em>&quot; in all From properties.</span></span> <span data-ttu-id="ac2b1-280">Auf das Wort <em>Sanjay</em> muss das Wort <em>Jacobs</em>folgen.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-280">The word <em>Sanjay</em> must be followed by the word <em>Jacobs</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac2b1-281">COP_WORD_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="ac2b1-281">COP_WORD_STARTSWITH</span></span></td>
<td>$<<br/></td>
<td><span data-ttu-id="ac2b1-282">System. Author: $</span><span class="sxs-lookup"><span data-stu-id="ac2b1-282">System.Author:$</span></span><&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td><span data-ttu-id="ac2b1-283">Für Windows 7 und höher.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-283">For Windows 7 and later.</span></span> <span data-ttu-id="ac2b1-284">Sucht nach jedem Element, bei dem der Autor ein Wort enthält, das mit den Zeichen &quot; <em>San</em>beginnt &quot; .</span><span class="sxs-lookup"><span data-stu-id="ac2b1-284">Finds any item where Author contains a word starting with the characters &quot;<em>San</em>&quot;.</span></span><br/> <span data-ttu-id="ac2b1-285">Findet eine beliebige Datei, in der der Dateiname ein Wort enthält, das mit <em>Micro</em>beginnt, gefolgt von einem Wort, das mit <em>exe</em>beginnt.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-285">Finds any file in which the file name contains a word starting with <em>micro</em>, followed by a word starting with <em>exe</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ac2b1-286">¹ leere eckige Klammern ( \[ \] ) kennzeichnen "kein Wert".</span><span class="sxs-lookup"><span data-stu-id="ac2b1-286">¹ Empty square brackets (\[\]) denote "no value".</span></span>

<span data-ttu-id="ac2b1-287">Für Zeichen folgen Eigenschaften ist der Standard Vorgang entweder Cop \_ Word \_ beginnt \_ mit oder Cop \_ Word \_ gleich.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-287">For string properties the default operation is either COP\_WORD\_STARTS\_WITH or COP\_WORD\_EQUAL.</span></span>

### <a name="query-values"></a><span data-ttu-id="ac2b1-288">Abfrage Werte</span><span class="sxs-lookup"><span data-stu-id="ac2b1-288">Query Values</span></span>

<span data-ttu-id="ac2b1-289">In der folgenden Tabelle sind nützliche Beispiele für die Einschränkung von Abfrage Werten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-289">Useful examples of how query values can be restricted are listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ac2b1-290">Wert/Symbol</span><span class="sxs-lookup"><span data-stu-id="ac2b1-290">Value/symbol</span></span></th>
<th><span data-ttu-id="ac2b1-291">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac2b1-291">Examples</span></span></th>
<th><span data-ttu-id="ac2b1-292">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac2b1-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ac2b1-293">String</span><span class="sxs-lookup"><span data-stu-id="ac2b1-293">String</span></span></td>
<td><span data-ttu-id="ac2b1-294">auto</span><span class="sxs-lookup"><span data-stu-id="ac2b1-294">auto</span></span><br/></td>
<td><span data-ttu-id="ac2b1-295">Eine beliebige Sequenz von Zeichen, nach denen gesucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-295">Any sequence of characters that can be searched for.</span></span> <span data-ttu-id="ac2b1-296">Die Zeichenfolge darf keine Leerzeichen oder Zeichenkombinationen enthalten, die Teil der Syntax sind.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-296">The string must not contain whitespace or character combinations that are part of the syntax.</span></span> <span data-ttu-id="ac2b1-297">Dieses Beispiel sucht nach einem Wort, das mit " <em>Auto</em>" beginnt.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-297">This example searches for a word beginning with <em>auto</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac2b1-298">Zeichenfolge in Zeichen &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="ac2b1-298">Quoted string &quot;&quot;</span></span></td>
<td><span data-ttu-id="ac2b1-299">&quot;Schlussfolgerungen: gültiges &quot; &quot; &quot; &quot; blaues &quot; &quot; Team&quot;</span><span class="sxs-lookup"><span data-stu-id="ac2b1-299">&quot;Conclusions: valid&quot; &quot;The &quot;&quot;blue&quot;&quot; team&quot;</span></span><br/></td>
<td><span data-ttu-id="ac2b1-300">Eine beliebige Sequenz von Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-300">Any sequence of characters.</span></span> <span data-ttu-id="ac2b1-301">Die Zeichenfolge wird nicht als Teil der Syntax interpretiert.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-301">The string is not interpreted as part of the syntax.</span></span><br/> <span data-ttu-id="ac2b1-302">Anführungszeichen können in eine Abfrage eingeschlossen werden, wenn Sie verdoppelt werden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-302">Quotation marks can be included in a query if they are doubled.</span></span> <span data-ttu-id="ac2b1-303">Dieses Beispiel sucht nach <em>dem &quot; blauen &quot; Team</em>.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-303">This example searches for <em>The &quot;blue&quot; team</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac2b1-304">Integer</span><span class="sxs-lookup"><span data-stu-id="ac2b1-304">Integer</span></span></td>
<td><span data-ttu-id="ac2b1-305">5678</span><span class="sxs-lookup"><span data-stu-id="ac2b1-305">5678</span></span><br/></td>
<td><span data-ttu-id="ac2b1-306">Verwenden Sie nur Ziffern für ganze Zahlen.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-306">Use only digits for integers.</span></span> <span data-ttu-id="ac2b1-307">Verwenden Sie keine Trennzeichen für Tausender.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-307">Do not use any separators for thousands.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac2b1-308">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="ac2b1-308">Floating point number</span></span></td>
<td><span data-ttu-id="ac2b1-309">5678,1234</span><span class="sxs-lookup"><span data-stu-id="ac2b1-309">5678.1234</span></span><br/></td>
<td><span data-ttu-id="ac2b1-310">Da Gleit Komma Formate sich zwischen den Gebiets Schemata unterscheiden, kann eine kanonische Abfrage keine Gleit Komma Konstante verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-310">Because floating point formats vary among locales, a canonical query cannot use a floating point constant.</span></span> <span data-ttu-id="ac2b1-311">Die Verwendung von kanonischer Syntax mit Gleit Komma Zahlen ist nicht Lokalisierungs sicher.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-311">The use of canonical syntax with floating point numbers is not localization safe.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac2b1-312">Boolescher Wert <strong>true</strong> / <strong>false</strong></span><span class="sxs-lookup"><span data-stu-id="ac2b1-312">Boolean <strong>true</strong>/<strong>false</strong></span></span></td>
<td><span data-ttu-id="ac2b1-313">System. isread: = System. structuredquerytype. Boolean # true</span><span class="sxs-lookup"><span data-stu-id="ac2b1-313">System.IsRead:=System.StructuredQueryType.Boolean#True</span></span><br/> <span data-ttu-id="ac2b1-314">System. isverschlüsselte:-System. structuredquerytype. Boolean # false</span><span class="sxs-lookup"><span data-stu-id="ac2b1-314">System.IsEncrypted:-System.StructuredQueryType.Boolean#False</span></span><br/></td>
<td><span data-ttu-id="ac2b1-315">Der <strong>echte</strong> boolesche Wert.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-315">The <strong>TRUE</strong> Boolean value.</span></span><br/> <span data-ttu-id="ac2b1-316">Der boolesche Wert <strong>false</strong> .</span><span class="sxs-lookup"><span data-stu-id="ac2b1-316">The <strong>FALSE</strong> Boolean value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac2b1-317">[]</span><span class="sxs-lookup"><span data-stu-id="ac2b1-317">[]</span></span></td>
<td><span data-ttu-id="ac2b1-318">System. Keywords: = []</span><span class="sxs-lookup"><span data-stu-id="ac2b1-318">System.Keywords:=[]</span></span><br/></td>
<td><span data-ttu-id="ac2b1-319">Leere eckige Klammern kennzeichnen, dass kein Wert vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-319">Empty square brackets denote that there is no value.</span></span> <span data-ttu-id="ac2b1-320">In diesem Beispiel werden alle Elemente gesucht, die nicht markiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-320">This example finds all items that have not been tagged.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac2b1-321">Absolute Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="ac2b1-321">Absolute dates</span></span></td>
<td><span data-ttu-id="ac2b1-322">System. itemdate: 1/26/2010</span><span class="sxs-lookup"><span data-stu-id="ac2b1-322">System.ItemDate:1/26/2010</span></span><br/> <span data-ttu-id="ac2b1-323">Systemdatemodified 10/15/2002 19:00</span><span class="sxs-lookup"><span data-stu-id="ac2b1-323">SystemDateModified 10/15/2002 19:00</span></span><br/></td>
<td><span data-ttu-id="ac2b1-324">Sucht nach Elementen mit dem Datum 26. Januar 2010.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-324">Finds items with a date of 26 January 2010.</span></span><br/> <span data-ttu-id="ac2b1-325">Ermittelt Elemente, die am 15. Oktober 2002 zwischen den Stunden 19:00:00 und 19:00:59 geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-325">Finds items that were modified on 15 October 2002 between the hours 19:00:00 and 19:00:59.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ac2b1-326">Da Datumsformate (z. b. Gleit Komma Formate) zwischen Gebiets Schemata variieren, wird die Verwendung von kanonischer Syntax mit absoluten Datumsangaben nicht unterstützt und ist nicht Lokalisierungs sicher.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-326">Because date formats (like floating point formats) vary among locales, the use of canonical syntax with absolute dates is not supported and is not localization safe.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac2b1-327">Relative Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="ac2b1-327">Relative dates</span></span></td>
<td><span data-ttu-id="ac2b1-328">System. itemdate: System. structuredquerytype. DateTime # heute</span><span class="sxs-lookup"><span data-stu-id="ac2b1-328">System.ItemDate:System.StructuredQueryType.DateTime#Today</span></span><br/> <span data-ttu-id="ac2b1-329">System. dateerworbener Name: System. structuredquerytype. DateTime # nextmonth</span><span class="sxs-lookup"><span data-stu-id="ac2b1-329">System.DateAcquired:System.StructuredQueryType.DateTime#NextMonth</span></span><br/> <span data-ttu-id="ac2b1-330">System. Message. DateReceived: System. structuredquerytype. DateTime # lastYear</span><span class="sxs-lookup"><span data-stu-id="ac2b1-330">System.Message.DateReceived:System.StructuredQueryType.DateTime#LastYear</span></span><br/></td>
<td><span data-ttu-id="ac2b1-331">Sucht nach Elementen mit dem heutigen Datum.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-331">Finds items with today's date.</span></span><br/> <span data-ttu-id="ac2b1-332">Findet Elemente mit einem Datum im nächsten Monat.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-332">Finds items with a date in the next month.</span></span><br/> <span data-ttu-id="ac2b1-333">Findet Elemente mit einem Datum im letzten Jahr.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-333">Finds items with a date in the last year.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ac2b1-334">Neben der Suche nach bestimmten Datums-und Datumsbereichen werden von AQS relative Datumswerte (z. b. <em>heute</em>, <em>Morgen</em>, <em>nextweek</em>, <em>nextmonth</em>) und Day (z. b. <em>Dienstag</em> oder Montag) erkannt <em>. Mittwoch</em>) und Monat (<em>Februar</em>).</span><span class="sxs-lookup"><span data-stu-id="ac2b1-334">In addition to searching on specific dates and date ranges, AQS recognizes relative date values (like <em>today</em>, <em>tomorrow</em>, <em>nextweek</em>, <em>nextmonth</em>), and day (like <em>Tuesday</em> or <em>Monday..Wednesday</em>), and month (<em>February</em>).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac2b1-335">..</span><span class="sxs-lookup"><span data-stu-id="ac2b1-335">..</span></span></td>
<td><span data-ttu-id="ac2b1-336">System. itemdate: 11/05/04.. 11/10/04 System. size: 5 KB. 10 KB</span><span class="sxs-lookup"><span data-stu-id="ac2b1-336">System.ItemDate:11/05/04..11/10/04 System.Size:5kb..10kb</span></span><br/></td>
<td><span data-ttu-id="ac2b1-337">Doppelte Zeiträume geben einen Wertebereich an.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-337">Double periods indicate a value range.</span></span> <span data-ttu-id="ac2b1-338">Sucht nach Elementen, deren Datum zwischen 11/05/04 und 11/10/04 (einschließlich) liegt.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-338">Finds items with a date between 11/05/04 and 11/10/04, inclusive.</span></span><br/> <span data-ttu-id="ac2b1-339">Sucht nach Elementen zwischen 5 und 10 KB.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-339">Finds items between 5 and 10kb in size.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a><span data-ttu-id="ac2b1-340">Bereichs Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="ac2b1-340">Scope Restrictions</span></span>

<span data-ttu-id="ac2b1-341">Benutzer können den Suchbereich auf bestimmte Ordner Speicherorte oder Datenspeicher beschränken.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-341">Users can limit the scope of their searches to specific folder locations or data stores.</span></span> <span data-ttu-id="ac2b1-342">Wenn Sie z. b. mehrere e-Mail-Konten verwenden und eine Abfrage entweder auf Microsoft Outlook oder Microsoft Outlook Express beschränken möchten, können Sie `System.Search.Store:mapi` oder verwenden `System.Search.Store:oe` .</span><span class="sxs-lookup"><span data-stu-id="ac2b1-342">For example, if you use several email accounts and you want to limit a query to either Microsoft Outlook or Microsoft Outlook Express, you can use `System.Search.Store:mapi` or `System.Search.Store:oe` respectively.</span></span> <span data-ttu-id="ac2b1-343">In der folgenden Tabelle finden Sie einige Beispiele für die Einschränkung einer Suche nach Datenspeicher.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-343">The following table shows some examples of how to restrict a search by data store.</span></span>



| <span data-ttu-id="ac2b1-344">Einschränken der Suche nach Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="ac2b1-344">Restrict search by data store</span></span>  | <span data-ttu-id="ac2b1-345">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="ac2b1-345">Keyword</span></span> | <span data-ttu-id="ac2b1-346">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ac2b1-346">Example</span></span>                                     |
|--------------------------------|---------|---------------------------------------------|
| <span data-ttu-id="ac2b1-347">Dateien</span><span class="sxs-lookup"><span data-stu-id="ac2b1-347">Files</span></span>                          | <span data-ttu-id="ac2b1-348">file</span><span class="sxs-lookup"><span data-stu-id="ac2b1-348">file</span></span>    | <span data-ttu-id="ac2b1-349">System. search. Store: Datei</span><span class="sxs-lookup"><span data-stu-id="ac2b1-349">System.Search.Store:file</span></span>                    |
| <span data-ttu-id="ac2b1-350">Outlook</span><span class="sxs-lookup"><span data-stu-id="ac2b1-350">Outlook</span></span>                        | <span data-ttu-id="ac2b1-351">MAPI</span><span class="sxs-lookup"><span data-stu-id="ac2b1-351">mapi</span></span>    | <span data-ttu-id="ac2b1-352">System. search. Store: MAPI</span><span class="sxs-lookup"><span data-stu-id="ac2b1-352">System.Search.Store:mapi</span></span>                    |
| <span data-ttu-id="ac2b1-353">Outlook Express</span><span class="sxs-lookup"><span data-stu-id="ac2b1-353">Outlook Express</span></span>                | <span data-ttu-id="ac2b1-354">oe</span><span class="sxs-lookup"><span data-stu-id="ac2b1-354">oe</span></span>      | <span data-ttu-id="ac2b1-355">System. search. Store: OE</span><span class="sxs-lookup"><span data-stu-id="ac2b1-355">System.Search.Store:oe</span></span>                      |
| <span data-ttu-id="ac2b1-356">Offlinedateien</span><span class="sxs-lookup"><span data-stu-id="ac2b1-356">Offline files</span></span>                  | <span data-ttu-id="ac2b1-357">CSC</span><span class="sxs-lookup"><span data-stu-id="ac2b1-357">csc</span></span>     | <span data-ttu-id="ac2b1-358">System. search. Store: CSC</span><span class="sxs-lookup"><span data-stu-id="ac2b1-358">System.Search.Store:csc</span></span>                     |
| <span data-ttu-id="ac2b1-359">Bestimmter Ordner auf lokalem Laufwerk</span><span class="sxs-lookup"><span data-stu-id="ac2b1-359">Specific folder on local drive</span></span> | <span data-ttu-id="ac2b1-360">folder</span><span class="sxs-lookup"><span data-stu-id="ac2b1-360">folder</span></span>  | <span data-ttu-id="ac2b1-361">System. itemfoldernamedisplay: C: " \\ MyFolder"</span><span class="sxs-lookup"><span data-stu-id="ac2b1-361">System.ItemFolderNameDisplay:C:"\\MyFolder"</span></span> |



 

## <a name="additional-resources"></a><span data-ttu-id="ac2b1-362">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ac2b1-362">Additional Resources</span></span>

-   <span data-ttu-id="ac2b1-363">In Windows 7 und höher kann eine Kontextmenü Option basierend darauf verfügbar sein, ob eine AQS-Bedingung erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-363">In Windows 7 and later, a shortcut menu option can be available based on whether an AQS condition is met.</span></span> <span data-ttu-id="ac2b1-364">Weitere Informationen finden Sie unter "erzielen von dynamischen Verhalten bei statischen Verben mithilfe der erweiterten Abfrage Syntax" unter [Erstellen von Kontextmenü Handlern](../shell/context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="ac2b1-364">For more information, see "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" in [Creating Context Menu Handlers](../shell/context-menu-handlers.md).</span></span>
-   <span data-ttu-id="ac2b1-365">AQS-Abfragen können auf bestimmte Typen von Dateien beschränkt werden, die als Dateitypen bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ac2b1-365">AQS queries can be limited to specific types of files, which are known as file kinds.</span></span> <span data-ttu-id="ac2b1-366">Weitere Informationen finden Sie unter [Dateitypen und Zuordnungen](../shell/fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="ac2b1-366">For more information, see [File Types and Associations](../shell/fa-intro.md).</span></span> <span data-ttu-id="ac2b1-367">Informationen zur Eigenschafts Referenz Dokumentation finden Sie unter [System. Kind](../properties/props-system-kind.md)und [System. kindtext](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="ac2b1-367">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac2b1-368">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ac2b1-368">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac2b1-369">Programm gesteuertes Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="ac2b1-369">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="ac2b1-370">Verwenden von SQL-und AQS-Ansätzen zum Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="ac2b1-370">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="ac2b1-371">Abfragen des Indexes mit isearchqueryhelper</span><span class="sxs-lookup"><span data-stu-id="ac2b1-371">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="ac2b1-372">Abfragen des Indexes mit dem Search-MS-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ac2b1-372">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="ac2b1-373">Abfragen des Indexes mit der SQL-Syntax von Windows Search</span><span class="sxs-lookup"><span data-stu-id="ac2b1-373">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 
