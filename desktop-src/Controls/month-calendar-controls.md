---
title: Informationen zu Monatskalender-Steuerelementen
description: Ein Monatskalender-Steuerelement implementiert eine kalenderähnliche Benutzeroberfläche.
ms.assetid: 81b8f233-272e-4043-92ff-5ff47b0610d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f21fba66f9fb71ad45f8853578821ad5f83da00e
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423750"
---
# <a name="about-month-calendar-controls"></a>Informationen zu Monatskalender-Steuerelementen

Ein Monatskalender-Steuerelement implementiert eine kalenderähnliche Benutzeroberfläche. Dies bietet dem Benutzer eine sehr intuitive und erkennbare Methode zum Eingeben oder Auswählen eines Datums. Das -Steuerelement bietet der Anwendung auch die Möglichkeit, die Datumsinformationen im Steuerelement mithilfe vorhandener Datentypen abzurufen und festzulegen.

-   [Funktionen des Monatskalender-Steuerelements](#month-calendar-control-features)
    -   [Auswählen eines Tages](#selecting-a-day)
    -   [Auswählen eines Nicht-Abstiegsmonats](#selecting-a-nonadjacent-month)
    -   [Auswählen eines anderen Jahres](#selecting-a-different-year)
-   [Lokalisierung](#localization)
-   [Uhrzeiten im Monatskalender-Steuerelement](#times-in-the-month-calendar-control)

## <a name="month-calendar-control-features"></a>Funktionen des Monatskalender-Steuerelements

Der folgende Screenshot zeigt ein Monatskalender-Steuerelement, das so dimensioniert wurde, dass es zwei Monate anzeigt.

![Screenshot eines Dialogfelds mit einem Monatskalender-Steuerelement, das zwei Monate nebeneinander anzeigt](images/mc-simple.png)

> [!Note]  
> Darstellung und Verhalten des Monatskalender-Steuerelements unterscheiden sich geringfügig unter verschiedenen Versionen der Laufzeitbibliothek. Dieses Thema konzentriert sich auf das Steuerelement, wie es in Windows Vista mit Version 6 von Comctl32.dll angezeigt wird.

 

Das Steuerelement in der Abbildung verfügt über die folgenden optionalen Features.

-   Das aktuelle Datum wird in einer separaten Zeile am unteren Rand des Steuerelements angezeigt. Dies ist das Standardformat.
-   Der "heutige Kreis" (eigentlich ein Rechteck in dieser Version) wird um den aktuellen Tag und neben der Zeile "Heute" als visueller Hinweis angezeigt. Dies ist das Standardformat.
-   Wochenzahlen werden links von jeder Zeile mit Tagen angezeigt. Dieses Format muss angegeben werden.
-   Einige Datumsangaben werden entsprechend dem von der Anwendung festgelegten Tageszustand fett angezeigt. Beispielsweise können Datumsangaben mit geplanten Besprechungen fett angezeigt werden. Dieses Format muss angegeben werden.

> [!Note]
>
> Windows unterstützt keine Datumsangaben vor 1601. Weitere Informationen finden Sie unter [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
>
> Das Monatskalender-Steuerelement basiert auf dem gregorianischen Kalender, der 1753 eingeführt wurde. Es werden keine Datumsangaben berechnet, die mit dem Vor 1753 in Gebrauch war.

 

### <a name="selecting-a-day"></a>Auswählen eines Tages

Wenn ein Benutzer auf die Pfeilschaltflächen in der oberen linken oder oberen rechten Ecke des Monatskalender-Steuerelements klickt, aktualisiert das Steuerelement standardmäßig seine Anzeige, um den vorherigen oder nächsten Monat anzuzeigen. Der Benutzer kann die gleiche Aktion auch ausführen, indem er auf die Teilmonate klickt, die vor dem ersten monat und nach dem letzten Monat angezeigt werden.

Die folgenden Tastaturbefehle können auch verwendet werden, um die Auswahl zu verschieben. Der Kalender scrollt immer nach Bedarf, um den ausgewählten Tag anzuzeigen. (Die [**Codes für virtuelle Schlüssel**](/windows/desktop/inputdev/virtual-key-codes) werden in der Tabelle angezeigt.)



|    Befehl      |    BESCHREIBUNG                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nach-LINKS-TASTE (VK \_ LEFT)   | Wählen Sie den vorherigen Tag aus.                                                                                                                                                                                                                 |
| Pfeil nach rechts (VK \_ NACH-RECHTS) | Wählen Sie den nächsten Tag aus.                                                                                                                                                                                                                     |
| NACH-OBEN-TASTE (VK \_ NACH OBEN)       | Wählen Sie den gleichen Tag in der vorherigen Woche aus.                                                                                                                                                                                                |
| Pfeil nach unten (VK \_ NACH-UNTEN)   | Wählen Sie den gleichen Tag in der nächsten Woche aus.                                                                                                                                                                                                    |
| PAGE UP (VK \_ PRIOR)     | Wählen Sie den gleichen Tag im vorherigen Monat aus. (Wenn dieser Monat nicht über den Tag verfügt, wird der nächstgelegene Tag ausgewählt. Die Auswahl wird beispielsweise vom 31. März bis zum 28. oder 29. Februar verschoben.)                                                      |
| PAGE DOWN (VK \_ NEXT)    | Wählen Sie den gleichen Tag im nächsten Monat aus.                                                                                                                                                                                                   |
| HOME (VK \_ HOME)         | Wählen Sie den ersten Tag des aktuellen Monats aus.                                                                                                                                                                                               |
| END (VK \_ END)           | Wählen Sie den letzten Tag des aktuellen Monats aus.                                                                                                                                                                                                |
| STRG +HOME             | Scrollen Sie einen Monat rückwärts, und wählen Sie in der Spalte ganz links einen Tag aus.                                                                                                                                                                       |
| STRG+ENDE              | Scrollen Sie einen Monat nach vorn, und wählen Sie einen Tag in der spalte ganz rechts aus.                                                                                                                                                                       |
| STRG +PAGE UP          | Wählen Sie den gleichen Tag in einem früheren Monat aus. Die Anzahl der Monate, um die sich die Auswahl verschiebt, ist die Anzahl der Monate, die im Steuerelement angezeigt werden. Wenn beispielsweise zwei Monate angezeigt werden, wird die Auswahl vom 6. Juni in den 6. Mai verschoben.    |
| STRG +SEITE NACH UNTEN        | Wählen Sie den gleichen Tag in einem früheren Monat aus. Die Anzahl der Monate, um die sich die Auswahl verschiebt, ist die Anzahl der Monate, die im Steuerelement angezeigt werden. Wenn beispielsweise zwei Monate angezeigt werden, würde die Auswahl vom 6. Juni auf den 6. August wechseln. |



 

Wenn für ein Monatskalender-Steuerelement nicht das [**\_ MCS-Format NOT WIE**](month-calendar-control-styles.md) VERWENDET wird, kann der Benutzer zum aktuellen Tag zurückkehren, indem er am unteren Rand des Steuerelements auf den Text "Today" klickt. Wenn der aktuelle Tag nicht sichtbar ist, aktualisiert das Steuerelement seine Anzeige, um es anzuzeigen.

Eine Anwendung kann die Anzahl der Monate ändern, um die das Steuerelement seine Anzeige aktualisiert, indem die [**MCM \_ SETMONTHDELTA-Meldung**](mcm-setmonthdelta.md) oder das entsprechende Makro [**MonthCal \_ SetMonthDelta verwendet wird.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) Die Tasten PAGE UP und PAGE DOWN ändern den ausgewählten Monat jedoch um 1, unabhängig von der Anzahl der angezeigten Monate oder dem von **MCM \_ SETMONTHDELTA festgelegten Wert.**

### <a name="selecting-a-nonadjacent-month"></a>Auswählen eines Nicht-Folgemonats

Wenn ein Benutzer auf den Namen eines angezeigten Monats klickt, werden alle Monate im Jahr aufgeführt (in früheren Versionen ist dies ein Popupmenü). Der Benutzer kann einen Monat in der Liste auswählen. Wenn die Auswahl des Benutzers nicht sichtbar ist, scrollt das Monatskalender-Steuerelement in seiner Anzeige, um den ausgewählten Monat anzuzeigen. Im folgenden Screenshot zeigt ein Monatskalender-Steuerelement die Monate von zwei angrenzenden Jahren an.

![Screenshot eines Dialogfelds mit einem Monatskalender-Steuerelement, das alle Monate 2007 und 2008 zeigt](images/mc-months.png)

### <a name="selecting-a-different-year"></a>Auswählen eines anderen Jahres

Wenn der Benutzer auf das Jahr klickt, wird eine Gruppe von Jahren aufgeführt, und der Benutzer kann eine andere auswählen, wie im folgenden Screenshot gezeigt.

![Screenshot eines Monatskalender-Steuerelements mit allen Jahren von 1999 bis 2020](images/mc-years.png)

## <a name="localization"></a>Lokalisierung

Das Monatskalender-Steuerelement ruft sein Format und alle Zeichenfolgen aus LOCALE \_ USER \_ DEFAULT ab.

## <a name="times-in-the-month-calendar-control"></a>Zeiten im Monatskalender-Steuerelement

Das Monatskalender-Steuerelement zeigt die Uhrzeit nicht an. Die [**SYSTEMTIME-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die zum Festlegen und Abrufen des ausgewählten Datums oder des heutigen Datums verwendet wird, enthält jedoch Zeitfelder. Wenn ein Datum programmgesteuert festgelegt wird, kopiert das Steuerelement entweder die Zeitfelder, wie sie sind, oder überprüft sie zuerst und speichert dann, wenn sie ungültig sind, die aktuellen Standardzeiten. Es folgt eine Liste der Meldungen, die ein Datum festlegen, und eine Beschreibung, wie die Zeitfelder behandelt werden.



|  `Message`         |  BESCHREIBUNG            |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCM \_ SETCURSEL**](mcm-setcursel.md)     | Das Steuerelement kopiert die Zeitfelder ohne Überprüfung oder Änderung in deren Beschriftung.                                                                                                                                        |
| [**MCM \_ SETRANGE**](mcm-setrange.md)       | Die Zeitfelder der übergebenen Strukturen werden überprüft. Wenn sie gültig sind, werden die Zeitfelder ohne Änderungen kopiert. Wenn sie ungültig sind, kopiert das Steuerelement die Zeitfelder aus den heutigen Daten.                  |
| [**MCM \_ SETSELRANGE**](mcm-setselrange.md) | Die Zeitfelder der übergebenen Strukturen werden überprüft. Wenn sie gültig sind, werden die Zeitfelder ohne Änderungen kopiert. Wenn sie ungültig sind, behält das Steuerelement die Zeitfelder aus den aktuellen Auswahlbereichen bei. |
| [**MCM \_ SETTODAY**](mcm-settoday.md)       | Das Steuerelement kopiert die Zeitfelder ohne Überprüfung oder Änderung in deren Beschriftung.                                                                                                                                        |



 

Wenn ein Datum aus dem -Steuerelement abgerufen wird, werden die Zeitfelder ohne Änderungen aus den gespeicherten Zeiten kopiert. Die Verarbeitung der Zeitfelder durch das -Steuerelement wird dem Programmierer zur Vereinfachung bereitgestellt. Das Steuerelement untersucht oder ändert die Zeitfelder nicht als Ergebnis eines anderen Vorgangs als den oben aufgeführten.

 

 