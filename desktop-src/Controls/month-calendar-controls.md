---
title: Informationen zu Monatskalender-Steuerelementen
description: Ein Monatskalender-Steuerelement implementiert eine Kalender ähnliche Benutzeroberfläche.
ms.assetid: 81b8f233-272e-4043-92ff-5ff47b0610d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f61b0ffc291473b330469910d1dad0317668e1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102418"
---
# <a name="about-month-calendar-controls"></a>Informationen zu Monatskalender-Steuerelementen

Ein Monatskalender-Steuerelement implementiert eine Kalender ähnliche Benutzeroberfläche. Dadurch erhält der Benutzer eine sehr intuitive und erkennbare Methode zum eingeben oder Auswählen eines Datums. Das-Steuerelement stellt der Anwendung außerdem die Möglichkeit zum Abrufen und Festlegen der Datumsinformationen im-Steuerelement mithilfe vorhandener Datentypen zur Verfügung.

-   [Monatskalender-Steuerelement Features](#month-calendar-control-features)
    -   [Auswählen eines Tags](#selecting-a-day)
    -   [Auswählen eines nicht angrenzenden Monats](#selecting-a-nonadjacent-month)
    -   [Auswählen eines anderen Jahres](#selecting-a-different-year)
-   [Lokalisierung](#localization)
-   [Uhrzeiten im Monatskalender-Steuerelement](#times-in-the-month-calendar-control)

## <a name="month-calendar-control-features"></a>Monatskalender-Steuerelement Features

Der folgende Screenshot zeigt ein Monatskalender-Steuerelement mit einer Größenangabe von zwei Monaten.

![Screenshot eines Dialog Felds mit einem Monatskalender-Steuerelement, das zwei Monate und nebeneinander anzeigt](images/mc-simple.png)

> [!Note]  
> Das Aussehen und Verhalten des Monatskalender-Steuer Elements unterscheidet sich geringfügig unter verschiedenen Versionen der Lauf Zeit Bibliothek. Dieses Thema konzentriert sich auf das-Steuerelement, wie es in Windows Vista mit Version 6 von Comctl32.dll angezeigt wird.

 

Das-Steuerelement in der Abbildung verfügt über die folgenden optionalen Features.

-   Das aktuelle Datum wird in einer separaten Zeile am unteren Rand des Steuer Elements angezeigt. Dies ist das Standardformat.
-   Der "heutige Kreis" (tatsächlich ein Rechteck in dieser Version) wird um den aktuellen Tag und neben der "heute"-Zeile als visueller Hinweis angezeigt. Dies ist das Standardformat.
-   Wochen Nummern werden auf der linken Seite der einzelnen Zeilen angezeigt. Dieser Stil muss angegeben werden.
-   Einige Datumsangaben werden in Fett Schrift angezeigt, entsprechend dem von der Anwendung festgelegten Tageszustand. Beispielsweise können Datumsangaben, die geplante Besprechungen aufweisen, fett angezeigt werden. Dieser Stil muss angegeben werden.

> [!Note]
>
> Datumsangaben vor 1601 werden von Windows nicht unterstützt. Weitere Informationen finden Sie unter [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .
>
> Das Month-Calendar-Steuerelement basiert auf dem gregorianischen Kalender, der in 1753 eingeführt wurde. Es werden keine Datumsangaben berechnet, die mit dem julianischen Kalender übereinstimmen, der vor 1753 verwendet wurde.

 

### <a name="selecting-a-day"></a>Auswählen eines Tags

Wenn ein Benutzer auf die Pfeil Schaltflächen in der oberen linken oder oberen rechten Ecke des Monatskalender-Steuer Elements klickt, aktualisiert das Steuerelement standardmäßig seine Anzeige, um den vorherigen oder nächsten Monat anzuzeigen. Der Benutzer kann dieselbe Aktion auch durchführen, indem er auf die vor dem ersten Monat und nach dem letzten Monat angezeigten partiellen Monate klickt.

Die folgenden Tastaturbefehle können auch verwendet werden, um die Auswahl zu verschieben. Der Kalender scrollt immer nach Bedarf, um den ausgewählten Tag anzuzeigen. (Die [**virtuellen Schlüsselcodes**](/windows/desktop/inputdev/virtual-key-codes) werden in der Tabelle angezeigt.)



|                         |                                                                                                                                                                                                                                          |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pfeil nach links (VK \_ Links)   | Wählen Sie den vorherigen Tag aus.                                                                                                                                                                                                                 |
| Rechter Pfeil (VK \_ rechts) | Wählen Sie den nächsten Tag aus.                                                                                                                                                                                                                     |
| Pfeil nach oben (VK \_ aufwärts)       | Wählen Sie denselben Tag in der vorangegangenen Woche aus.                                                                                                                                                                                                |
| Pfeil nach unten (VK \_ nach unten)   | Wählen Sie in der nächsten Woche denselben Tag aus.                                                                                                                                                                                                    |
| Bild-auf (VK \_ vor)     | Wählen Sie im vorhergehenden Monat denselben Tag aus. (Wenn dieser Monat nicht den Tag hat, wird der nächste Tag ausgewählt. die Auswahl wird z. b. vom 31. März zum 28. Februar oder 29.)                                                      |
| Bild-ab (VK \_ Weiter)    | Wählen Sie im nächsten Monat denselben Tag aus.                                                                                                                                                                                                   |
| Startseite (VK- \_ Startseite)         | Wählen Sie den ersten Tag des aktuellen Monats aus.                                                                                                                                                                                               |
| Ende (VK- \_ Ende)           | Wählen Sie den letzten Tag des aktuellen Monats aus.                                                                                                                                                                                                |
| STRG + Startseite             | Scrollen Sie einen Monat rückwärts, und wählen Sie einen Tag in der äußersten linken Spalte aus.                                                                                                                                                                       |
| STRG + Ende              | Scrollen Sie einen Monat vorwärts, und wählen Sie einen Tag in der Spalte ganz rechts aus.                                                                                                                                                                       |
| STRG + Bild-auf          | Wählen Sie denselben Tag in einem früheren Monat aus. Die Anzahl der Monate, um die die Auswahl verschoben wird, ist die Anzahl der Monate, die im Steuerelement angezeigt werden. Wenn beispielsweise zwei Monate angezeigt werden, wird die Auswahl vom 6. Juni bis zum 6. Mai verschoben.    |
| STRG + Bild-ab        | Wählen Sie denselben Tag in einem früheren Monat aus. Die Anzahl der Monate, um die die Auswahl verschoben wird, ist die Anzahl der Monate, die im Steuerelement angezeigt werden. Wenn beispielsweise zwei Monate angezeigt werden, wechselt die Auswahl vom 6. Juni zum 6. August. |



 

Wenn ein Monatskalender-Steuerelement nicht den [**MCS- \_ notoday**](month-calendar-control-styles.md) -Stil verwendet, kann der Benutzer zum aktuellen Tag zurückkehren, indem er auf den "heute"-Text am unteren Rand des Steuer Elements klickt. Wenn der aktuelle Tag nicht sichtbar ist, aktualisiert das Steuerelement seine Anzeige, um es anzuzeigen.

Eine Anwendung kann die Anzahl von Monaten ändern, um die das Steuerelement seine Anzeige mithilfe der [**MCM- \_ setmonthdelta**](mcm-setmonthdelta.md) -Nachricht oder des entsprechenden Makros ( [**monthcal \_ setmonthdelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta)) aktualisiert. Allerdings ändern die Bild-auf-und Bild-ab-Taste den ausgewählten Monat um 1, unabhängig von der Anzahl der angezeigten Monate oder dem durch **MCM \_ setmonthdelta** festgelegten Wert.

### <a name="selecting-a-nonadjacent-month"></a>Auswählen eines nicht angrenzenden Monats

Wenn ein Benutzer auf den Namen eines angezeigten Monats klickt, werden alle Monate des Jahres aufgelistet (in früheren Versionen ist dies ein Popup Menü). Der Benutzer kann einen Monat in der Liste auswählen. Wenn die Auswahl des Benutzers nicht angezeigt wird, führt das Monatskalender-Steuerelement einen Bildlauf zur Anzeige des ausgewählten Monats aus. Im folgenden Screenshot zeigt ein Monatskalender-Steuerelement die Monate von zwei angrenzenden Jahren.

![Screenshot eines Dialog Felds mit einem Monatskalender-Steuerelement, das alle Monate von 2007 und 2008 anzeigt](images/mc-months.png)

### <a name="selecting-a-different-year"></a>Auswählen eines anderen Jahres

Wenn der Benutzer auf das Jahr klickt, wird eine Gruppe von Jahren aufgelistet, und der Benutzer kann eine andere Gruppe auswählen, wie im folgenden Screenshot zu sehen.

![Screenshot eines Monatskalender-Steuer Elements, das alle Jahre zwischen 1999 und 2020 anzeigt](images/mc-years.png)

## <a name="localization"></a>Lokalisierung

Das Month-Calendar-Steuerelement erhält sein Format und alle Zeichen folgen vom Gebiets Schema \_ Benutzer \_ Standard.

## <a name="times-in-the-month-calendar-control"></a>Uhrzeiten im Monatskalender-Steuerelement

Im Monatskalender-Steuerelement wird die Uhrzeit nicht angezeigt. Die [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die verwendet wird, um das ausgewählte Datum oder das heutige Datum festzulegen und abzurufen, enthält jedoch Zeitfelder. Wenn ein Datum Programm gesteuert festgelegt wird, kopiert das Steuerelement entweder die Zeitfelder, die Sie sind, oder überprüft Sie zuerst. Wenn Sie ungültig sind, speichert die aktuellen Standardzeiten. Im folgenden finden Sie eine Liste der Nachrichten, die ein Datum festlegen, und eine Beschreibung, wie die Zeitfelder behandelt werden.



|                                             |                                                                                                                                                                                                                            |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCM \_ setcurrsel**](mcm-setcursel.md)     | Das-Steuerelement kopiert die Zeitfelder unverändert, ohne Validierung oder Änderung.                                                                                                                                        |
| [**MCM-über \_ Tragung**](mcm-setrange.md)       | Die Zeitfelder der übergebenen Strukturen werden überprüft. Wenn Sie gültig sind, werden die Zeitfelder ohne Änderung kopiert. Wenn Sie ungültig sind, kopiert das Steuerelement die Zeitfelder aus den heutigen Daten.                  |
| [**MCM \_ setselrange**](mcm-setselrange.md) | Die Zeitfelder der übergebenen Strukturen werden überprüft. Wenn Sie gültig sind, werden die Zeitfelder ohne Änderung kopiert. Wenn Sie ungültig sind, behält das Steuerelement die Zeitfelder aus den aktuellen Auswahl Bereichen bei. |
| [**MCM \_ settoday**](mcm-settoday.md)       | Das-Steuerelement kopiert die Zeitfelder unverändert, ohne Validierung oder Änderung.                                                                                                                                        |



 

Wenn ein Datum aus dem-Steuerelement abgerufen wird, werden die Zeitfelder ohne Änderung aus den gespeicherten Zeiten kopiert. Die Handhabung der Zeitfelder durch das Steuerelement wird dem Programmierer als praktische Hilfe bereitgestellt. Das-Steuerelement prüft oder ändert die Zeitfelder nicht als Ergebnis eines Vorgangs, der nicht den oben aufgeführten Vorgängen entspricht.

 

 