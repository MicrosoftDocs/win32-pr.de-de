---
description: Der Filter für die Muster Übereinstimmung benachrichtigt den Treiber, dass Frames mit einem bestimmten Muster an einem bestimmten Offset akzeptiert werden.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Schreiben des patternmatch-Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372992"
---
# <a name="writing-the-patternmatch-filter"></a>Schreiben des patternmatch-Filters

Der Filter für die Muster Übereinstimmung benachrichtigt den Treiber, dass Frames mit einem bestimmten Muster an einem bestimmten Offset akzeptiert werden. Sie können maximal vier ausführliche Muster Übereinstimmungen angeben, die in logischen and-oder or-Anweisungen für die Auswertung Netzwerkmonitor Treibers kombiniert werden können.

Verwenden Sie die folgenden Netzwerkmonitor Strukturen, um Muster Übereinstimmungen zu implementieren:

-   [**Begriff**](expression.md)
-   [**Andexp**](andexp.md)
-   [**Patternmatch**](patternmatch.md)

Um eine- **oder** -Anweisung auszuwerten, kombinieren Sie zwei bis vier Muster mit einer [**andexp**](andexp.md) -Struktur (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3). Um eine-Anweisung und eine-Anweisung auszuwerten, kombinieren Sie eine zu vier **andexp** -Strukturen und eine [**Ausdrucks**](expression.md) Struktur (AndExp1 && AndExp2).

## <a name="pattern-match-definitions"></a>Muster Übereinstimmungs Definitionen

Eine einzelne Muster Übereinstimmung wird durch die [**patternmatch**](patternmatch.md) -Struktur definiert. Eine individuelle Übereinstimmung kann auf zwei Arten ausgeführt werden.

Normalerweise nimmt der Treiber den Offset auf (der auf der Basis von Frame, Offset-Basis in Bezug auf das \_ \_ \_ effektive Protokoll, die Offset-Basis in Bezug auf \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ IPX oder \_ die Offset Basis \_ \_ in Bezug auf die \_ IP-Adresse sein kann) und beginnt mit der Zählung. Der Treiber zählt Offset Bytes von dort und passt dann die gefundenen Daten mit den ersten Längen Bytes in **patterntomatch** an. Wenn Sie identisch sind und die Übereinstimmungs \_ Kennzeichen \_ \_ nicht-Flag nicht festgelegt ist, wird dieses Muster weitergeleitet. Wenn Sie unterschiedlich sind und die Übereinstimmungs Flags für Muster \_ \_ \_ nicht festgelegt wurden, wird das Muster weitergegeben. Andernfalls schlägt dieses Muster fehl.

Oder:

Wenn das angegebene Flag für das Übereinstimmungs Kennzeichen des Musters \_ \_ festgelegt \_ \_ ist und die Basis auf den Wert "Offset" \_ \_ relativ \_ zu \_ IPX oder "Offset" \_ relativ zu IP festgelegt ist \_ \_ \_ , ist der Vergleich komplexer. Zuerst stellt der Treiber sicher, dass das Protokoll für die Offset Basis vorhanden ist, dann überprüft der Treiber, ob der angegebene Port mit dem Port im Frame übereinstimmt. Schließlich stellt der Treiber sicher, dass der **patterntomatch** -Member wie zuvor übereinstimmt, mit der Ausnahme, dass der Offset vom Ende von IP oder IPX abweicht. Beachten Sie Folgendes: Wenn es sich bei der Basis nicht um eine dieser beiden handelt, wird das Flag für den Übereinstimmungs Kennzeichen \_ \_ \_ \_ -Port festgelegt, und das Muster wird wie oben ausgewertet.

Zum Auswerten einer einzelnen Muster Übereinstimmung muss eine [**Ausdrucks**](expression.md) Struktur einen " **andexp** "-Member aufweisen, der eine einzelne Muster Übereinstimmung enthält.

Das Erstellen des Muster Übereinstimmungs Filters umfasst das Erstellen von [**patternmatch**](patternmatch.md) -Strukturen und das logische kombinieren mit den Strukturen [**Expression**](expression.md) und [**andexp**](andexp.md) .

**So schreiben Sie einen patternmatch-Filter**

1.  Füllen Sie in der [**andexp**](andexp.md) -Struktur das Array mit Muster Übereinstimmungen auf.
2.  Füllt die [**Ausdrucks**](expression.md) Struktur mit einem Array von **andexp** -Membern auf.
3.  Die Summe von vier Muster Übereinstimmungen für den Erfassungs Filter darf nicht überschritten werden.
4.  Wählen Sie in der [**patternmatch**](patternmatch.md) -Struktur einen flagtyp aus.
5.  Wählen Sie einen Offset aus.
6.  Enumerieren Sie einen Portwert.
7.  Legen Sie den Offset Wert fest.
8.  Definieren Sie die Muster Länge.
9.  Listet den Pattern-Wert auf.

## <a name="patternmatch-examples"></a>Patternmatch-Beispiele

Dieser Frame stellt einen Standard Offset dar.

![Standard Offset Rahmen](images/offs-pat.png)

Das Code Fragment wird wie folgt implementiert:

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

Dieser Frame stellt einen Port spezifischen Offset (gegen IPX) dar.

![vom Port angegebener Offset Rahmen](images/stan-pat.png)

Der Beispielcode wird wie folgt implementiert:

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



