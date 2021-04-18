---
description: Die Ergebnisse einer Abfrage enthalten sowohl die von der Abfrage zurückgegebenen Zeilen als auch einen Rangwert für jede Zeile, wenn die Rang Spalte in der SELECT-Klausel enthalten ist.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: Rank by-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214457"
---
# <a name="rank-by-clause"></a><span data-ttu-id="6cded-103">Rank by-Klausel</span><span class="sxs-lookup"><span data-stu-id="6cded-103">RANK BY Clause</span></span>

<span data-ttu-id="6cded-104">Die Ergebnisse einer Abfrage enthalten sowohl die von der Abfrage zurückgegebenen Zeilen als auch einen Rangwert für jede Zeile, wenn die Rang Spalte in der SELECT-Klausel enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6cded-104">The results from a query include both the rows returned by the query and a rank value for each row if the rank column is included in the SELECT clause.</span></span> <span data-ttu-id="6cded-105">Die Rang Werte werden von der Suchmaschine berechnet und als ganze Zahlen im Bereich von 0 bis 1000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6cded-105">The rank values are calculated by the Search engine and are returned as integers in the range zero to 1000.</span></span> <span data-ttu-id="6cded-106">Damit die Rang Ergebnisse aussagekräftiger werden, kann die Abfrage steuern, wie rohrang Werte in der Rank by-Klausel berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="6cded-106">To make the rank results more meaningful, the query can control how raw rank values are calculated in the RANK BY clause.</span></span>

<span data-ttu-id="6cded-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="6cded-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="6cded-108">Rank by-Klausel</span><span class="sxs-lookup"><span data-stu-id="6cded-108">RANK BY Clause</span></span>](#rank-by-clause)
-   [<span data-ttu-id="6cded-109">Weight-Funktion</span><span class="sxs-lookup"><span data-stu-id="6cded-109">WEIGHT Function</span></span>](#weight-function)
-   [<span data-ttu-id="6cded-110">Umwandlungs Funktion</span><span class="sxs-lookup"><span data-stu-id="6cded-110">COERCION Function</span></span>](#coercion-function)

## <a name="rank-by-clause"></a><span data-ttu-id="6cded-111">Rank by-Klausel</span><span class="sxs-lookup"><span data-stu-id="6cded-111">RANK BY Clause</span></span>

<span data-ttu-id="6cded-112">Die Syntax für die Rank by-Klausel lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6cded-112">The syntax for the RANK BY clause is as follows:</span></span>


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



<span data-ttu-id="6cded-113">Die Rank by-Klausel wird auf die \_ unmittelbar vorhergehende Such Bedingung angewendet. dabei wird ein niedrigerer oder höherer Rang für Zeilen angegeben, die von dieser Such Bedingung zurückgegeben werden, als von einer anderen Such Bedingung zurückgegebene Zeilen.</span><span class="sxs-lookup"><span data-stu-id="6cded-113">The RANK BY clause is applied to the search\_condition immediately preceding it, effectively specifying a lower or higher rank for rows returned by that search condition than rows returned by another search condition.</span></span> <span data-ttu-id="6cded-114">Die Klammern, die die Such Bedingung umgeben, \_ sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6cded-114">The parentheses surrounding the search\_condition are required.</span></span> <span data-ttu-id="6cded-115">Die Klammern, die die Rang Spezifikation umgeben, sind optional.</span><span class="sxs-lookup"><span data-stu-id="6cded-115">The parentheses surrounding the rank specification are optional.</span></span>

<span data-ttu-id="6cded-116">Auf eine einzelne Bedingung können mehr als eine Rang by-Klausel angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6cded-116">More than one RANK BY clause can be applied to a single condition.</span></span> <span data-ttu-id="6cded-117">Sie können zusätzliche Rank by-Klauseln nacheinander mithilfe von Klammern einschließen.</span><span class="sxs-lookup"><span data-stu-id="6cded-117">You can include additional RANK BY clauses one after the other using parentheses.</span></span>

> [!Note]  
> <span data-ttu-id="6cded-118">Volltext-Prädikate geben Rang Werte im Bereich von 0 bis 1000 zurück.</span><span class="sxs-lookup"><span data-stu-id="6cded-118">Full-text predicates return rank values in the range 0 to 1000.</span></span> <span data-ttu-id="6cded-119">Rang Werte für alle Dokumente, die mit einem nicht-voll Text Prädikat übereinstimmen, sind 1000.</span><span class="sxs-lookup"><span data-stu-id="6cded-119">Rank values for all documents matched by a non-full-text predicate are 1000.</span></span> <span data-ttu-id="6cded-120">Bei Änderungen an den Rang Werten sollten diese Informationen berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="6cded-120">Modifications to the rank values should take this information into account.</span></span>

 

<span data-ttu-id="6cded-121">Der Rang \_ Spezifikations Teil der rankby-Klausel identifiziert mindestens eine Funktion, die auf die Rang Werte angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cded-121">The rank\_specification portion of the RANKBY clause identifies one or more functions to apply to the rank values.</span></span> <span data-ttu-id="6cded-122">Die Weight-Funktion wendet einen Multiplikator auf den unformatierten Rangwert für eine zurückgegebene Zeile an.</span><span class="sxs-lookup"><span data-stu-id="6cded-122">The WEIGHT function applies a multiplier to the raw rank value for a returned row.</span></span> <span data-ttu-id="6cded-123">Je kleiner der Multiplikator, desto niedriger ist der resultierende Rangwert.</span><span class="sxs-lookup"><span data-stu-id="6cded-123">The smaller the multiplier, the lower the resulting rank value.</span></span> <span data-ttu-id="6cded-124">Die Umwandlungs Funktion kann verwendet werden, um einen bestimmten Rangwert für eine zurückgegebene Zeile zu multiplizieren, zu addieren oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6cded-124">The COERCION function can be used to multiply, add to, or set a specific rank value for a returned row.</span></span> <span data-ttu-id="6cded-125">Jede Rang Spezifikation kann entweder NULL oder eine Gewichtungsfunktion und NULL oder mehr koerationsfunktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6cded-125">Each rank specification can include either zero or one WEIGHT function and zero or more COERCION functions.</span></span> <span data-ttu-id="6cded-126">Wenn sowohl Gewichtungs-als auch dekoerationsfunktionen in eine Rank by-Klausel eingeschlossen werden, muss die Gewichtungsfunktion zuerst sein.</span><span class="sxs-lookup"><span data-stu-id="6cded-126">If both WEIGHT and COERCION functions are included in a RANK BY clause, the WEIGHT function must be first.</span></span>

## <a name="weight-function"></a><span data-ttu-id="6cded-127">Weight-Funktion</span><span class="sxs-lookup"><span data-stu-id="6cded-127">WEIGHT Function</span></span>

<span data-ttu-id="6cded-128">Die Syntax der Gewichtungsfunktion lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6cded-128">The syntax of the WEIGHT function is:</span></span>


```
WEIGHT ( <weight_multipler> ) 
```



<span data-ttu-id="6cded-129">Der Multiplikator muss ein Dezimalwert zwischen 0,001 und 1,000 sein.</span><span class="sxs-lookup"><span data-stu-id="6cded-129">The multiplier must be a decimal from 0.001 to 1.000.</span></span> <span data-ttu-id="6cded-130">Der vom Such Bedingungs Prädikat zurückgegebene rohrangwert wird mit dem Gewichtungs Multiplikator multipliziert, um einen neuen Rangwert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6cded-130">The raw rank value returned by the search condition predicate is multiplied by the weight multiplier to set a new rank value.</span></span>

<span data-ttu-id="6cded-131">Im folgenden Beispiel gibt die Weight-Funktion Dokumente mit dem Wort "Theresia" im System.Doc-Umschlag. Lastauthor-Feld halber der Rangwert von Dokumenten mit "Theresa" im Feld "System. Author":</span><span class="sxs-lookup"><span data-stu-id="6cded-131">In the following example, the WEIGHT function gives documents with the word "Theresa" in the System.Document.LastAuthor field half the rank value of documents with "Theresa" in the System.Author field:</span></span>


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> <span data-ttu-id="6cded-132">Die Spalten Gewichtungs Features "enthält" und "frei Text Prädikat" unterstützen eine Kurzform mit einem Doppelpunkt zwischen dem Suchbegriff und dem Multiplikator ("Software": 0,25).</span><span class="sxs-lookup"><span data-stu-id="6cded-132">The CONTAINS and FREETEXT predicate column weighting features support a shorthand format using a colon between the search term and the multiplier ("software":0.25).</span></span> <span data-ttu-id="6cded-133">Die Rang-nach-Klausel unterstützt das gekürzte Formular nicht.</span><span class="sxs-lookup"><span data-stu-id="6cded-133">The RANK BY clause does not support the shortened form.</span></span>

 

<span data-ttu-id="6cded-134">Bei der Verwendung von Rang nach Gewichtung gibt es eine Einschränkung: es funktioniert nicht mit Klauseln, die boolesche Bedingungen verwenden; Das folgende Beispiel ist beispielsweise nicht zulässig:</span><span class="sxs-lookup"><span data-stu-id="6cded-134">There is a limitation when using RANK BY WEIGHT: it does not work with CONTAINS clauses that use Boolean conditions; for example, the following example is not permitted:</span></span>


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a><span data-ttu-id="6cded-135">Umwandlungs Funktion</span><span class="sxs-lookup"><span data-stu-id="6cded-135">COERCION Function</span></span>

<span data-ttu-id="6cded-136">Die Rang Umwandlungs Funktion kann verwendet werden, um den zurückgegebenen Rangwert durch Hinzufügen oder Multiplikation oder durch Zuweisen eines bestimmten Werts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6cded-136">The rank coercion function can be used to change the returned rank value by addition or multiplication or by assigning it a specific value.</span></span>

<span data-ttu-id="6cded-137">Die Syntax der erumwandlungs Funktion lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6cded-137">The syntax of the COERCION function is:</span></span>


```
COERCION ( <coercion_operation> , <coercion_value> )
```



<span data-ttu-id="6cded-138">Der koerationswert ist ein ganzzahliger Wert.</span><span class="sxs-lookup"><span data-stu-id="6cded-138">The coercion value is an integer value.</span></span>

<span data-ttu-id="6cded-139">In der folgenden Tabelle werden die verfügbaren Umwandlungs Vorgangs Einstellungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6cded-139">The following table describes the available coercion operation settings.</span></span>



| <span data-ttu-id="6cded-140">Umwandlungs Vorgang</span><span class="sxs-lookup"><span data-stu-id="6cded-140">Coercion operation</span></span> | <span data-ttu-id="6cded-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cded-141">Description</span></span>                                                                                    | <span data-ttu-id="6cded-142">Wertebereich</span><span class="sxs-lookup"><span data-stu-id="6cded-142">Value range</span></span>  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="6cded-143">ABSOLUTE</span><span class="sxs-lookup"><span data-stu-id="6cded-143">ABSOLUTE</span></span>           | <span data-ttu-id="6cded-144">Der zurückgegebene Rangwert ist der Wert, der im koerationswert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6cded-144">The rank value returned is the value specified in the coercion value.</span></span>                          | <span data-ttu-id="6cded-145">0 bis 1000</span><span class="sxs-lookup"><span data-stu-id="6cded-145">0 to 1000</span></span>    |
| <span data-ttu-id="6cded-146">ADD</span><span class="sxs-lookup"><span data-stu-id="6cded-146">ADD</span></span>                | <span data-ttu-id="6cded-147">Der zurückgegebene Rangwert ist die Summe des rohrang Werts und des angegebenen koerationswerts.</span><span class="sxs-lookup"><span data-stu-id="6cded-147">The rank value returned is the sum of the raw rank value and the specified coercion value.</span></span>     | <span data-ttu-id="6cded-148">0,001 bis 1,0</span><span class="sxs-lookup"><span data-stu-id="6cded-148">0.001 to 1.0</span></span> |
| <span data-ttu-id="6cded-149">MULTIPLIZIEREN</span><span class="sxs-lookup"><span data-stu-id="6cded-149">MULTIPLY</span></span>           | <span data-ttu-id="6cded-150">Der zurückgegebene Rangwert ist das Produkt des rohrang Werts und des angegebenen koerationswerts.</span><span class="sxs-lookup"><span data-stu-id="6cded-150">The rank value returned is the product of the raw rank value and the specified coercion value.</span></span> | <span data-ttu-id="6cded-151">0,001 bis 1,0</span><span class="sxs-lookup"><span data-stu-id="6cded-151">0.001 to 1.0</span></span> |



 

 

> [!IMPORTANT]
> <span data-ttu-id="6cded-152">Die Suche kann Rang Werte nur im Bereich von 0 bis 1000 zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6cded-152">Search can return rank values only in the range of 0 to 1000.</span></span>

 

 

<span data-ttu-id="6cded-153">Im folgenden Beispiel wird die Erteilungs Funktion verwendet, um alle Dokumente mit dem Titel "Computer" im Titel auf einen Rang von 1000 festzulegen, während der Rang der Dokumente, die im Titel "Computer" und "Software" enthalten, um ein Quartal reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="6cded-153">The following example uses the COERCION function to set all documents with "computer" in the title to have a rank of 1000, while reducing by one-quarter the rank of documents containing both "computer" and "software" in the title.</span></span>


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



