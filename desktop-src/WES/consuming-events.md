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
# <a name="consuming-events-windows-event-log"></a>Verarbeiten von Ereignissen (Windows-Ereignisprotokoll)

Ereignisse können von Kanälen oder Protokolldateien genutzt werden. Um Ereignisse zu verarbeiten, können Sie alle Ereignisse verarbeiten, oder Sie können einen XPath-Ausdruck angeben, der die Ereignisse identifiziert, die Sie verwenden möchten. Informationen zum Bestimmen der Elemente und Attribute eines Ereignisses, das Sie im XPath-Ausdruck verwenden können, finden Sie unter [Ereignis Schema](eventschema-schema.md).

Das Windows-Ereignisprotokoll unterstützt eine Teilmenge von XPath 1,0. Ausführliche Informationen zu den Einschränkungen finden Sie unter [Einschränkungen für XPath 1,0](#xpath-10-limitations).

Die folgenden Beispiele zeigen einfache XPath-Ausdrücke.


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



Sie können die XPath-Ausdrücke direkt verwenden, wenn Sie die Funktionen [**evtquery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) oder [**evtsubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) aufrufen, oder Sie können eine strukturierte XML-Abfrage verwenden, die den XPath-Ausdruck enthält. Für einfache Abfragen, die Ereignisse aus einer einzelnen Quelle Abfragen, ist die Verwendung eines XPath-Ausdrucks in Ordnung. Handelt es sich bei dem XPath-Ausdruck um einen Verbund Ausdruck, der mehr als 20 Ausdrücke enthält oder um Ereignisse aus mehreren Quellen abzufragen, müssen Sie eine strukturierte XML-Abfrage verwenden. Ausführliche Informationen zu den Elementen einer strukturierten XML-Abfrage finden Sie unter [Abfrage Schema](queryschema-schema.md).

Eine strukturierte Abfrage identifiziert die Quelle der Ereignisse und einen oder mehrere Selektoren oder Unterdrücker. Ein Selektor enthält einen XPath-Ausdruck, der Ereignisse aus der Quelle auswählt, und ein unter Prüfer enthält einen XPath-Ausdruck, der verhindert, dass Ereignisse ausgewählt werden. Sie können Ereignisse aus mehreren Quellen auswählen. Wenn ein Selektor und unter Prüfer dasselbe Ereignis identifizieren, ist das Ereignis nicht im Ergebnis enthalten.

Das folgende Beispiel zeigt eine strukturierte XML-Abfrage, die einen Satz von Selektoren und Unterdrückern angibt.


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



Das Resultset aus der Abfrage enthält keine Momentaufnahme der Ereignisse zum Zeitpunkt der Abfrage. Stattdessen enthält das Resultset die Ereignisse zum Zeitpunkt der Abfrage und enthält außerdem alle neuen Ereignisse, die bei der Enumeration der Ergebnisse mit den Abfrage Kriterien übereinstimmen.

> [!Note]  
> Die Reihenfolge der Ereignisse wird für Ereignisse beibehalten, die vom gleichen Thread geschrieben werden. Es ist jedoch möglich, dass Ereignisse, die von separaten Threads auf unterschiedlichen Prozessoren eines Computers mit mehreren Prozessoren geschrieben wurden, nicht in der richtigen Reihenfolge angezeigt werden.

 

Ausführliche Informationen zum Verarbeiten von Ereignissen finden Sie in den folgenden Themen:

-   [Abfragen von Ereignissen](querying-for-events.md)
-   [Abonnieren von Ereignissen](subscribing-to-events.md)
-   [Renderingereignisse](rendering-events.md)
-   [Formatieren von Ereignismeldungen](formatting-event-messages.md)
-   [Lesezeichen Ereignisse](bookmarking-events.md)

Die standardmäßigen Endbenutzer Tools zum Verarbeiten von Ereignissen lauten:

-   [Ereignisanzeige](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))
-   Das Windows PowerShell-Cmdlet " [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) "
-   [**WevtUtil**](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a>Einschränkungen für XPath 1,0

Das Windows-Ereignisprotokoll unterstützt eine Teilmenge von XPath 1,0. Die primäre Einschränkung besteht darin, dass nur XML-Elemente, die Ereignisse darstellen, von einem Ereignis Selektor ausgewählt werden können. Eine XPath-Abfrage, die kein Ereignis auswählt, ist ungültig. Alle gültigen Auswahl Pfade beginnen mit \* oder "Event". Alle Standort Pfade arbeiten auf den Ereignis Knoten und bestehen aus einer Reihe von Schritten. Jeder Schritt besteht aus einer Struktur von drei Teilen: der Achse, dem Knoten Test und dem Prädikat. Weitere Informationen zu diesen Teilen und zu XPath 1,0 finden Sie unter [XML Path Language (XPath)](https://www.w3.org/TR/xpath). Das Windows-Ereignisprotokoll fügt die folgenden Einschränkungen für den Ausdruck ein:

-   Achse: nur das untergeordnete (Standard-) und das-Attribut (und seine Kurzwert-Achse) werden unterstützt.
-   Knoten Tests: nur Knoten Namen und NCName-Tests werden unterstützt. Das \* Zeichen "", von dem ein beliebiges Zeichen ausgewählt wird, wird unterstützt.
-   Prädikate: jeder gültige XPath-Ausdruck ist zulässig, wenn die Speicherort Pfade den folgenden Einschränkungen entsprechen:
    -   Standard Operatoren **oder**, **and**, =,! =, <=, <, >=, > und Klammern werden unterstützt.
    -   Das Erstellen eines Zeichen folgen Werts für einen Knoten Namen wird nicht unterstützt.
    -   Die Auswertung in umgekehrter Reihenfolge wird nicht unterstützt.
    -   Knotengruppen werden nicht unterstützt.
    -   Namespace-Gültigkeits Bereiche werden nicht unterstützt.
    -   Namespace-, Verarbeitungs-und Kommentar Knoten werden nicht unterstützt.
    -   Die Kontext Größe wird nicht unterstützt.
    -   Variablen Bindungen werden nicht unterstützt.
    -   Die Positions Funktion und deren Kurzwert-Array Verweis werden unterstützt (nur auf Blattknoten).
    -   Die Band Funktion wird unterstützt. Die-Funktion führt ein bitweises and für zwei ganzzahlige Zahlen Argumente aus. Wenn das Ergebnis der bitweisen and-Funktion ungleich NULL ist, wird die-Funktion als true ausgewertet. Andernfalls wird die-Funktion zu false ausgewertet.
    -   Die timediff-Funktion wird unterstützt. Die-Funktion berechnet den Unterschied zwischen dem zweiten Argument und dem ersten Argument. Eines der Argumente muss eine Literalzahl sein. Die Argumente müssen die FILETIME-Darstellung verwenden. Das Ergebnis ist die Anzahl der Millisekunden zwischen den zwei Uhrzeiten. Das Ergebnis ist positiv, wenn das zweite Argument einen späteren Zeitpunkt darstellt. Andernfalls ist sie negativ. Wenn das zweite Argument nicht angegeben wird, wird die aktuelle Systemzeit verwendet.

 

 
