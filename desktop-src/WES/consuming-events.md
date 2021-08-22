---
title: Nutzen von Ereignissen (Windows Ereignisprotokoll)
description: Sie können Ereignisse aus Kanälen oder Protokolldateien nutzen.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f131f0f3b02485c3c838e9180ea1daaebb4121b8846e5a124f36cfdb6bf377f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620380"
---
# <a name="consuming-events-windows-event-log"></a>Nutzen von Ereignissen (Windows Ereignisprotokoll)

Sie können Ereignisse aus Kanälen oder Protokolldateien nutzen. Um Ereignisse zu nutzen, können Sie alle Ereignisse nutzen oder einen XPath-Ausdruck angeben, der die Ereignisse identifiziert, die Sie nutzen möchten. Informationen zum Bestimmen der Elemente und Attribute eines Ereignisses, die Sie in Ihrem XPath-Ausdruck verwenden können, finden Sie unter [Ereignisschema.](eventschema-schema.md)

Windows Das Ereignisprotokoll unterstützt eine Teilmenge von XPath 1.0. Ausführliche Informationen zu den Einschränkungen finden Sie unter [XPath 1.0-Einschränkungen.](#xpath-10-limitations)

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



Sie können die XPath-Ausdrücke direkt verwenden, wenn Sie die [**EvtQuery-**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) oder [**EvtSubscribe-Funktionen**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) aufrufen, oder Sie können eine strukturierte XML-Abfrage verwenden, die den XPath-Ausdruck enthält. Bei einfachen Abfragen, die Ereignisse aus einer einzelnen Quelle abfragen, ist die Verwendung eines XPath-Ausdrucks in Ordnung. Wenn der XPath-Ausdruck ein zusammengesetzter Ausdruck ist, der mehr als 20 Ausdrücke enthält, oder Wenn Sie Ereignisse aus mehreren Quellen abfragen, müssen Sie eine strukturierte XML-Abfrage verwenden. Ausführliche Informationen zu den Elementen einer strukturierten XML-Abfrage finden Sie unter [Abfrageschema.](queryschema-schema.md)

Eine strukturierte Abfrage identifiziert die Quelle der Ereignisse und eine oder mehrere Selektoren oder Unterdrücker. Ein Selektor enthält einen XPath-Ausdruck, der Ereignisse aus der Quelle auswählt, und ein Suppressor enthält einen XPath-Ausdruck, der verhindert, dass Ereignisse ausgewählt werden. Sie können Ereignisse aus mehreren Quellen auswählen. Wenn ein Selektor und ein Suppressor das gleiche Ereignis identifizieren, ist das Ereignis nicht im Ergebnis enthalten.

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



Das Resultset der Abfrage enthält keine Momentaufnahme der Ereignisse zum Zeitpunkt der Abfrage. Stattdessen enthält das Resultset die Ereignisse zum Zeitpunkt der Abfrage und enthält auch alle neuen Ereignisse, die ausgelöst werden, die den Abfragekriterien entsprechen, während Sie die Ergebnisse aufzählen.

> [!Note]  
> Die Reihenfolge der Ereignisse wird für Ereignisse beibehalten, die vom gleichen Thread geschrieben werden. Es ist jedoch möglich, dass Ereignisse, die von separaten Threads auf verschiedenen Prozessoren eines Computers mit mehreren Prozessoren geschrieben werden, nicht in der reihenfolgengeordneten Reihenfolge angezeigt werden.

 

Ausführliche Informationen zum Nutzen von Ereignissen finden Sie in den folgenden Themen:

-   [Abfragen von Ereignissen](querying-for-events.md)
-   [Abonnieren von Ereignissen](subscribing-to-events.md)
-   [Renderingereignisse](rendering-events.md)
-   [Formatieren von Ereignismeldungen](formatting-event-messages.md)
-   [Lesezeichenereignisse](bookmarking-events.md)

Die standard-Endbenutzertools für die Nutzung von -Ereignis sind:

-   [Ereignisanzeige](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))
-   Das Windows PowerShell [Get-WinEvent-Cmdlet](/previous-versions//dd367894(v=technet.10))
-   [**WevtUtil**](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a>XPath 1.0-Einschränkungen

Windows Das Ereignisprotokoll unterstützt eine Teilmenge von XPath 1.0. Die primäre Einschränkung besteht darin, dass nur XML-Elemente, die Ereignisse darstellen, von einem Ereignisselektor ausgewählt werden können. Eine XPath-Abfrage, die kein Ereignis auswählt, ist ungültig. Alle gültigen Selektorpfade beginnen mit \* oder "Event". Alle Speicherortpfade werden auf den Ereignisknoten ausgeführt und bestehen aus einer Reihe von Schritten. Jeder Schritt besteht aus drei Teilen: Achse, Knotentest und Prädikat. Weitere Informationen zu diesen Teilen und zu XPath 1.0 finden Sie unter [XML Path Language (XPath)](https://www.w3.org/TR/xpath). Windows Das Ereignisprotokoll weist die folgenden Einschränkungen für den Ausdruck auf:

-   Achse: Es werden nur die untergeordnete Achse (Standard) und das Attribut (und die kurzformige @-Achse) unterstützt.
-   Knotentests: Es werden nur Knotennamen und NCName-Tests unterstützt. Das \* Zeichen "", das ein beliebiges Zeichen auswählt, wird unterstützt.
-   Prädikate: Jeder gültige XPath-Ausdruck ist akzeptabel, wenn die Speicherortpfade den folgenden Einschränkungen entsprechen:
    -   Die Standardoperatoren **OR**, **AND**, =, !=, <=, <, >=, > und Klammern werden unterstützt.
    -   Das Generieren eines Zeichenfolgenwerts für einen Knotennamen wird nicht unterstützt.
    -   Die Auswertung in umgekehrter Reihenfolge wird nicht unterstützt.
    -   Knotensätze werden nicht unterstützt.
    -   Namespace-Bereichsinformationen werden nicht unterstützt.
    -   Namespace-, Verarbeitungs- und Kommentarknoten werden nicht unterstützt.
    -   Die Kontextgröße wird nicht unterstützt.
    -   Variablenbindungen werden nicht unterstützt.
    -   Die Position-Funktion und ihr Kurzformarrayverweis werden unterstützt (nur auf Blattknoten).
    -   Die Band-Funktion wird unterstützt. Die -Funktion führt ein bitweises AND für zwei ganzzahlige Zahlenargumente aus. Wenn das Ergebnis des bitweisen AND ungleich 0 (null) ist, wird die Funktion als TRUE ausgewertet. andernfalls wird die Funktion als FALSE ausgewertet.
    -   Die timediff-Funktion wird unterstützt. Die Funktion berechnet den Unterschied zwischen dem zweiten argument und dem ersten Argument. Eines der Argumente muss eine Literalzahl sein. Die Argumente müssen die FILETIME-Darstellung verwenden. Das Ergebnis ist die Anzahl von Millisekunden zwischen den beiden Zeiten. Das Ergebnis ist positiv, wenn das zweite Argument einen späteren Zeitpunkt darstellt. andernfalls ist sie negativ. Wenn das zweite Argument nicht angegeben wird, wird die aktuelle Systemzeit verwendet.

 

 
