---
title: Verarbeiten von Ereignissen (Windows-Ereignisprotokoll)
description: Ereignisse können von Kanälen oder Protokolldateien genutzt werden.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb3fb1b36a0cd4ecf836a8893bc1abc14e46451
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341765"
---
# <a name="consuming-events-windows-event-log"></a><span data-ttu-id="3ed0d-103">Verarbeiten von Ereignissen (Windows-Ereignisprotokoll)</span><span class="sxs-lookup"><span data-stu-id="3ed0d-103">Consuming Events (Windows Event Log)</span></span>

<span data-ttu-id="3ed0d-104">Ereignisse können von Kanälen oder Protokolldateien genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-104">You can consume events from channels or from log files.</span></span> <span data-ttu-id="3ed0d-105">Um Ereignisse zu verarbeiten, können Sie alle Ereignisse verarbeiten, oder Sie können einen XPath-Ausdruck angeben, der die Ereignisse identifiziert, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-105">To consume events, you can consume all events or you can specify an XPath expression that identifies the events that you want to consume.</span></span> <span data-ttu-id="3ed0d-106">Informationen zum Bestimmen der Elemente und Attribute eines Ereignisses, das Sie im XPath-Ausdruck verwenden können, finden Sie unter [Ereignis Schema](eventschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="3ed0d-106">To determine the elements and attributes of an event that you can use in your XPath expression, see [Event Schema](eventschema-schema.md).</span></span>

<span data-ttu-id="3ed0d-107">Das Windows-Ereignisprotokoll unterstützt eine Teilmenge von XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-107">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="3ed0d-108">Ausführliche Informationen zu den Einschränkungen finden Sie unter [Einschränkungen für XPath 1,0](#xpath-10-limitations).</span><span class="sxs-lookup"><span data-stu-id="3ed0d-108">For details on the limitations, see [XPath 1.0 limitations](#xpath-10-limitations).</span></span>

<span data-ttu-id="3ed0d-109">Die folgenden Beispiele zeigen einfache XPath-Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-109">The following examples show simple XPath expressions.</span></span>


```XML
// The following query selects all events from the channel or log file
XPath Query: *

// The following query selects all the LowOnMemory events from the channel or log file
XPath Query: *[UserData/LowOnMemory]

// The following query selects all events with a severity level of 1 (Critical) from the channel or log file
XPath Query: *[System/Level=1]

// The following query shows a compound expression that selects all events from the channel or log file
// where the printer's name is MyPrinter and severity level is 1.
XPath Query: *[UserData/*/PrinterName="MyPrinter" and System/Level=1]

// The following query selects all events from the channel or log file where the severity level is
// less than or equal to 3 and the event occurred in the last 24 hour period.
XPath Query: *[System[(Level <= 3) and TimeCreated[timediff(@SystemTime) <= 86400000]]]
```



<span data-ttu-id="3ed0d-110">Sie können die XPath-Ausdrücke direkt verwenden, wenn Sie die Funktionen [**evtquery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) oder [**evtsubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) aufrufen, oder Sie können eine strukturierte XML-Abfrage verwenden, die den XPath-Ausdruck enthält.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-110">You can use the XPath expressions directly when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions or you can use a structured XML query that contains the XPath expression.</span></span> <span data-ttu-id="3ed0d-111">Für einfache Abfragen, die Ereignisse aus einer einzelnen Quelle Abfragen, ist die Verwendung eines XPath-Ausdrucks in Ordnung.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-111">For simple queries that query events from a single source, using an XPath expression is fine.</span></span> <span data-ttu-id="3ed0d-112">Handelt es sich bei dem XPath-Ausdruck um einen Verbund Ausdruck, der mehr als 20 Ausdrücke enthält oder um Ereignisse aus mehreren Quellen abzufragen, müssen Sie eine strukturierte XML-Abfrage verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-112">If the XPath expression is a compound expression that contains more than 20 expressions or you are querying for events from multiple sources, then you must use a structured XML query.</span></span> <span data-ttu-id="3ed0d-113">Ausführliche Informationen zu den Elementen einer strukturierten XML-Abfrage finden Sie unter [Abfrage Schema](queryschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="3ed0d-113">For details on the elements of a structured XML query, see [Query Schema](queryschema-schema.md).</span></span>

<span data-ttu-id="3ed0d-114">Eine strukturierte Abfrage identifiziert die Quelle der Ereignisse und einen oder mehrere Selektoren oder Unterdrücker.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-114">A structured query identifies the source of the events and one or more selectors or suppressors.</span></span> <span data-ttu-id="3ed0d-115">Ein Selektor enthält einen XPath-Ausdruck, der Ereignisse aus der Quelle auswählt, und ein unter Prüfer enthält einen XPath-Ausdruck, der verhindert, dass Ereignisse ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-115">A selector contains an XPath expressions that selects events from the source and a suppressor contains an XPath expression that prevents events from being selected.</span></span> <span data-ttu-id="3ed0d-116">Sie können Ereignisse aus mehreren Quellen auswählen.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-116">You can select events from more than one source.</span></span> <span data-ttu-id="3ed0d-117">Wenn ein Selektor und unter Prüfer dasselbe Ereignis identifizieren, ist das Ereignis nicht im Ergebnis enthalten.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-117">If a selector and suppressor identify the same event, the event is not included in the result.</span></span>

<span data-ttu-id="3ed0d-118">Das folgende Beispiel zeigt eine strukturierte XML-Abfrage, die einen Satz von Selektoren und Unterdrückern angibt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-118">The following shows a structured XML query that specifies a set of selectors and suppressors.</span></span>


```XML
<QueryList>
  <Query Id="0">
    <Select Path="Application">
        *[System[(Level <= 3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
  </Query>
</QueryList>
```



<span data-ttu-id="3ed0d-119">Das Resultset aus der Abfrage enthält keine Momentaufnahme der Ereignisse zum Zeitpunkt der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-119">The result set from the query does not contain a snapshot of the events at the time of the query.</span></span> <span data-ttu-id="3ed0d-120">Stattdessen enthält das Resultset die Ereignisse zum Zeitpunkt der Abfrage und enthält außerdem alle neuen Ereignisse, die bei der Enumeration der Ergebnisse mit den Abfrage Kriterien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-120">Instead, the result set includes the events at the time of the query and will also contain all new events that are raised that match the query criteria while you are enumerating the results.</span></span>

> [!Note]  
> <span data-ttu-id="3ed0d-121">Die Reihenfolge der Ereignisse wird für Ereignisse beibehalten, die vom gleichen Thread geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-121">The order of the events is preserved for events that are written by the same thread.</span></span> <span data-ttu-id="3ed0d-122">Es ist jedoch möglich, dass Ereignisse, die von separaten Threads auf unterschiedlichen Prozessoren eines Computers mit mehreren Prozessoren geschrieben wurden, nicht in der richtigen Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-122">However, it is possible for events written by separate threads on different processors of a multiple processor computer to appear out of order.</span></span>

 

<span data-ttu-id="3ed0d-123">Ausführliche Informationen zum Verarbeiten von Ereignissen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="3ed0d-123">For details on consuming events, see the following topics:</span></span>

-   [<span data-ttu-id="3ed0d-124">Abfragen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="3ed0d-124">Querying for Events</span></span>](querying-for-events.md)
-   [<span data-ttu-id="3ed0d-125">Abonnieren von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="3ed0d-125">Subscribing to Events</span></span>](subscribing-to-events.md)
-   [<span data-ttu-id="3ed0d-126">Renderingereignisse</span><span class="sxs-lookup"><span data-stu-id="3ed0d-126">Rendering Events</span></span>](rendering-events.md)
-   [<span data-ttu-id="3ed0d-127">Formatieren von Ereignismeldungen</span><span class="sxs-lookup"><span data-stu-id="3ed0d-127">Formatting Event Messages</span></span>](formatting-event-messages.md)
-   [<span data-ttu-id="3ed0d-128">Lesezeichen Ereignisse</span><span class="sxs-lookup"><span data-stu-id="3ed0d-128">Bookmarking Events</span></span>](bookmarking-events.md)

<span data-ttu-id="3ed0d-129">Die standardmäßigen Endbenutzer Tools zum Verarbeiten von Ereignissen lauten:</span><span class="sxs-lookup"><span data-stu-id="3ed0d-129">The standard end user tools for consuming event are:</span></span>

-   <span data-ttu-id="3ed0d-130">[Ereignisanzeige](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="3ed0d-130">[Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span></span>
-   <span data-ttu-id="3ed0d-131">Das Windows PowerShell-Cmdlet " [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) "</span><span class="sxs-lookup"><span data-stu-id="3ed0d-131">The Windows PowerShell [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) cmdlet</span></span>
-   [<span data-ttu-id="3ed0d-132">**WevtUtil**</span><span class="sxs-lookup"><span data-stu-id="3ed0d-132">**WevtUtil**</span></span>](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a><span data-ttu-id="3ed0d-133">Einschränkungen für XPath 1,0</span><span class="sxs-lookup"><span data-stu-id="3ed0d-133">XPath 1.0 limitations</span></span>

<span data-ttu-id="3ed0d-134">Das Windows-Ereignisprotokoll unterstützt eine Teilmenge von XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-134">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="3ed0d-135">Die primäre Einschränkung besteht darin, dass nur XML-Elemente, die Ereignisse darstellen, von einem Ereignis Selektor ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-135">The primary restriction is that only XML elements that represent events can be selected by an event selector.</span></span> <span data-ttu-id="3ed0d-136">Eine XPath-Abfrage, die kein Ereignis auswählt, ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-136">An XPath query that does not select an event is not valid.</span></span> <span data-ttu-id="3ed0d-137">Alle gültigen Auswahl Pfade beginnen mit \* oder "Event".</span><span class="sxs-lookup"><span data-stu-id="3ed0d-137">All valid selector paths start with \* or "Event".</span></span> <span data-ttu-id="3ed0d-138">Alle Standort Pfade arbeiten auf den Ereignis Knoten und bestehen aus einer Reihe von Schritten.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-138">All location paths operate on the event nodes and are composed of a series of steps.</span></span> <span data-ttu-id="3ed0d-139">Jeder Schritt besteht aus einer Struktur von drei Teilen: der Achse, dem Knoten Test und dem Prädikat.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-139">Each step is a structure of three parts: the axis, node test, and predicate.</span></span> <span data-ttu-id="3ed0d-140">Weitere Informationen zu diesen Teilen und zu XPath 1,0 finden Sie unter [XML Path Language (XPath)](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="3ed0d-140">For more information about these parts and about XPath 1.0, see [XML Path Language (XPath)](https://www.w3.org/TR/xpath).</span></span> <span data-ttu-id="3ed0d-141">Das Windows-Ereignisprotokoll fügt die folgenden Einschränkungen für den Ausdruck ein:</span><span class="sxs-lookup"><span data-stu-id="3ed0d-141">Windows Event Log places the following restrictions on the expression:</span></span>

-   <span data-ttu-id="3ed0d-142">Achse: nur das untergeordnete (Standard-) und das-Attribut (und seine Kurzwert-Achse) werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-142">Axis: Only the Child (default) and Attribute (and its shorthand "@") axis are supported.</span></span>
-   <span data-ttu-id="3ed0d-143">Knoten Tests: nur Knoten Namen und NCName-Tests werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-143">Node Tests: Only node names and NCName tests are supported.</span></span> <span data-ttu-id="3ed0d-144">Das \* Zeichen "", von dem ein beliebiges Zeichen ausgewählt wird, wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-144">The "\*" character, which selects any character, is supported.</span></span>
-   <span data-ttu-id="3ed0d-145">Prädikate: jeder gültige XPath-Ausdruck ist zulässig, wenn die Speicherort Pfade den folgenden Einschränkungen entsprechen:</span><span class="sxs-lookup"><span data-stu-id="3ed0d-145">Predicates: Any valid XPath expression is acceptable if the location paths conform to the following restrictions:</span></span>
    -   <span data-ttu-id="3ed0d-146">Standard Operatoren **oder**, **and**, =,! =, <=, <, >=, > und Klammern werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-146">Standard operators **OR**, **AND**, =, !=, <=, <, >=, >, and parentheses are supported.</span></span>
    -   <span data-ttu-id="3ed0d-147">Das Erstellen eines Zeichen folgen Werts für einen Knoten Namen wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-147">Generating a string value for a node name is not supported.</span></span>
    -   <span data-ttu-id="3ed0d-148">Die Auswertung in umgekehrter Reihenfolge wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-148">Evaluation in reverse order is not supported.</span></span>
    -   <span data-ttu-id="3ed0d-149">Knotengruppen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-149">Node sets are not supported.</span></span>
    -   <span data-ttu-id="3ed0d-150">Namespace-Gültigkeits Bereiche werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-150">Namespace scoping is not supported.</span></span>
    -   <span data-ttu-id="3ed0d-151">Namespace-, Verarbeitungs-und Kommentar Knoten werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-151">Namespace, processing, and comment nodes are not supported.</span></span>
    -   <span data-ttu-id="3ed0d-152">Die Kontext Größe wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-152">Context size is not supported.</span></span>
    -   <span data-ttu-id="3ed0d-153">Variablen Bindungen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-153">Variable bindings are not supported.</span></span>
    -   <span data-ttu-id="3ed0d-154">Die Positions Funktion und deren Kurzwert-Array Verweis werden unterstützt (nur auf Blattknoten).</span><span class="sxs-lookup"><span data-stu-id="3ed0d-154">The position function, and its shorthand array reference, is supported (on leaf nodes only).</span></span>
    -   <span data-ttu-id="3ed0d-155">Die Band Funktion wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-155">The Band function is supported.</span></span> <span data-ttu-id="3ed0d-156">Die-Funktion führt ein bitweises and für zwei ganzzahlige Zahlen Argumente aus.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-156">The function performs a bitwise AND for two integer number arguments.</span></span> <span data-ttu-id="3ed0d-157">Wenn das Ergebnis der bitweisen and-Funktion ungleich NULL ist, wird die-Funktion als true ausgewertet. Andernfalls wird die-Funktion zu false ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-157">If the result of the bitwise AND is nonzero, the function evaluates to true; otherwise, the function evaluates to false.</span></span>
    -   <span data-ttu-id="3ed0d-158">Die timediff-Funktion wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-158">The timediff function is supported.</span></span> <span data-ttu-id="3ed0d-159">Die-Funktion berechnet den Unterschied zwischen dem zweiten Argument und dem ersten Argument.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-159">The function computes the difference between the second argument and the first argument.</span></span> <span data-ttu-id="3ed0d-160">Eines der Argumente muss eine Literalzahl sein.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-160">One of the arguments must be a literal number.</span></span> <span data-ttu-id="3ed0d-161">Die Argumente müssen die FILETIME-Darstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-161">The arguments must use FILETIME representation.</span></span> <span data-ttu-id="3ed0d-162">Das Ergebnis ist die Anzahl der Millisekunden zwischen den zwei Uhrzeiten.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-162">The result is the number of milliseconds between the two times.</span></span> <span data-ttu-id="3ed0d-163">Das Ergebnis ist positiv, wenn das zweite Argument einen späteren Zeitpunkt darstellt. Andernfalls ist sie negativ.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-163">The result is positive if the second argument represents a later time; otherwise, it is negative.</span></span> <span data-ttu-id="3ed0d-164">Wenn das zweite Argument nicht angegeben wird, wird die aktuelle Systemzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ed0d-164">When the second argument is not provided, the current system time is used.</span></span>

 

 
