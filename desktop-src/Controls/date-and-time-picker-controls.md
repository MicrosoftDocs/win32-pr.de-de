---
title: Informationen zu Steuerelementen für Datums-und Zeitauswahl
description: Ein DTP-Steuerelement (Datums-und Zeitauswahl) stellt eine einfache und intuitive Oberfläche bereit, mit der Datums-und Uhrzeit Informationen an einen Benutzer ausgetauscht werden können.
ms.assetid: 6749c3ae-2c52-4183-ac4e-68ca7ebf1e13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04604c01a73aa8f2ebb8542061412372faee5282
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039724"
---
# <a name="about-date-and-time-picker-controls"></a>Informationen zu Steuerelementen für Datums-und Zeitauswahl

Ein *DTP-Steuerelement (Datums-und Zeitauswahl)* stellt eine einfache und intuitive Oberfläche bereit, mit der Datums-und Uhrzeit Informationen an einen Benutzer ausgetauscht werden können. Beispielsweise können Sie mit einem DTP-Steuerelement den Benutzer zur Eingabe eines Datums auffordern und dann die Auswahl problemlos abrufen.

Die folgenden Themen werden erörtert:

-   [Benutzeroberfläche für Datums-und Zeitauswahl](#date-and-time-picker-user-interface)
-   [Steuerelement Stile und-Formate für Datums-und Zeitauswahl](#date-and-time-picker-control-styles-and-formats)
    -   [Voreinstellungs Formate](#preset-formats)
    -   [Benutzerdefinierte Formate](#custom-formats)
    -   [Formatzeichenfolgen](#format-strings)
    -   [Rückruf Felder](#callback-fields)
-   [Benachrichtigungs Meldungen zur Steuerung von Datums-und Zeitauswahl](#date-and-time-picker-control-notification-messages)
-   [Zugehörige Themen](#related-topics)

> [!Note]
> Datumsangaben vor 1601 werden von Windows nicht unterstützt. Weitere Informationen finden Sie in der [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur.
>
> Das-Steuerelement basiert auf dem gregorianischen Kalender, der in 1753 eingeführt wurde. Es werden keine Datumsangaben berechnet, die mit dem julianischen Kalender konsistent sind.

## <a name="date-and-time-picker-user-interface"></a>Benutzeroberfläche für Datums-und Zeitauswahl

Im Client Bereich eines DTP-Steuer Elements (Datums-und Zeitauswahl) werden Datums-oder Uhrzeit Informationen oder beides angezeigt, und die Benutzer können die Informationen ändern. Das Datum kann aus einem Kalender oder mithilfe eines auf-ab-Steuer Elements ausgewählt werden. die Zeit kann geändert werden, indem Felder eingegeben werden, die von den [Format](#format-strings)Zeichenfolgen des-Steuer Elements definiert werden. Optional zeigt das-Steuerelement ein Kontrollkästchen an. Wenn diese Option aktiviert ist, kann der Wert im Steuerelement abgerufen werden. Andernfalls wird das Steuerelement als nicht initialisiert betrachtet.

Die folgende Abbildung zeigt ein Fenster, das drei Steuerelemente für die Datumsauswahl enthält. Das erste Steuerelement für die Datumsauswahl wurde mit dem [**DTS- \_ Format "shownone**](date-and-time-picker-control-styles.md) " erstellt, das zweite mit dem [**DTS- \_ UpDown**](date-and-time-picker-control-styles.md) -Stil und das dritte ohne besondere Stile. Im dritten Steuerelement hat der Benutzer auf den Pfeil nach unten geklickt, um den Kalender anzuzeigen.

![Screenshot eines Fensters, das drei Stile von Steuerelementen für die Datumsauswahl veranschaulicht](images/dtpdatepick.png)

Die folgende Abbildung zeigt ein Fenster mit drei Steuerelementen, die die Uhrzeit enthalten.

Das erste Steuerelement wurde mit dem [**DTS- \_ Zeitformat**](date-and-time-picker-control-styles.md) Stil erstellt und zeigt die Zeit in der Standardzeit an, die aus vier Feldern besteht. Der Benutzer kann einen gültigen Wert in eines dieser Felder eingeben oder das Feld auswählen und den Wert mit dem auf-ab-Steuerelement oder den Pfeiltasten ändern.

Das zweite Steuerelement zeigt einen benutzerdefinierten Format Satz mithilfe von [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)an. Wie beim ersten Steuerelement kann der Benutzer die Zeitfelder durch Eingabe von oder mithilfe von Pfeiltasten ändern. Der Wochentag kann geändert werden, indem Sie ein Datum aus dem Kalender auswählen, das geöffnet wird, wenn der Benutzer auf den Pfeil nach unten klickt.

Das dritte Steuerelement zeigt, wie dem Steuerelement beliebiger Text hinzugefügt werden kann. Der Benutzer kann eine Stunde (zwischen 1 und 24) auswählen, indem er mit den Pfeiltasten oder mit dem auf-ab-Steuerelement die EINGABETASTE drücken.

![Screenshot eines Fensters, in dem drei Steuerelemente angezeigt werden, die die Uhrzeit enthalten](images/dtpdatetimepick.png)

Das DTP-Steuerelement aktualisiert interne Informationen automatisch basierend auf der Eingabe des Benutzers. Das-Steuerelement erkennt Folgendes als gültige Eingabe.



| Eingabe Kategorie | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pfeiltasten     | Das-Steuerelement akzeptiert Pfeiltasten, um durch die Felder im Steuerelement zu navigieren und Werte zu ändern. Der Benutzer kann die-Taste oder die-Taste drücken, um durch das-Steuerelement zu navigieren, wenn der Benutzer versucht, das letzte Feld in einer bestimmten Richtung zu bewegen, der Tastaturfokus "umschließt" in das Feld auf der gegenüberliegenden Seite des-Steuer Elements. Die Schlüssel und ändern Werte im aktuellen Feld inkrementell. |
| Ende und Startseite   | Das-Steuerelement akzeptiert die \_ virtuellen Schlüssel VK End und VK \_ Home, um den Wert im aktuellen Feld in seine obere bzw. untere Begrenzung zu ändern.                                                                                                                                                                                                                          |
| Funktionstasten  | Mit dem Schlüssel wird der Bearbeitungsmodus aktiviert. Der Schlüssel bewirkt, dass das Steuerelement ein Dropdown-Monatskalender-Steuerelement anzeigt (durch das Drücken wird dies ebenfalls).                                                                                                                                                                                                                                          |
| Zahlen        | Das-Steuerelement akzeptiert numerische Eingaben in zwei Zeichen Segmenten. Wenn der vom Benutzer eingegebene Wert ungültig ist (z. b. das Festlegen des Monats auf 14), lehnt das Steuerelement ihn ab und setzt die Anzeige auf den vorherigen Wert zurück.                                                                                                                                                                |
| Plus und minus | Das-Steuerelement akzeptiert die \_ virtuellen Schlüssel VK Add und VK \_ Subtract von der numerischen Tastatur, um den Wert im aktuellen Feld zu erhöhen und zu verringern.                                                                                                                                                                                                                             |



 

Bei DTP-Steuerelementen, bei denen der [**DTS- \_ UpDown**](date-and-time-picker-control-styles.md) -Stil nicht verwendet wird, wird die Schaltfläche Wenn der Benutzer auf diese Schaltfläche klickt, sinkt ein Monatskalender-Steuerelement. Der Benutzer kann ein bestimmtes Datum durch Klicken auf einen Bereich des Kalenders auswählen.

## <a name="date-and-time-picker-control-styles-and-formats"></a>Steuerelement Stile und-Formate für Datums-und Zeitauswahl

Die Steuerelemente für Datums-und Zeitauswahl (DTP) verfügen über mehrere Steuerelemente für [Datums-und Zeit](date-and-time-picker-control-styles.md) Auswahl, die die Darstellung und das Verhalten eines Steuer Elements bestimmen Geben Sie den Stil an, wenn Sie das Steuerelement mit dem *dwstyle* -Parameter von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" erstellen. Um den Fenster Stil nach dem Erstellen des Steuer Elements abzurufen oder zu ändern, verwenden Sie " [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) " und " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)".

### <a name="preset-formats"></a>Voreinstellungs Formate

Zum Anzeigen des Datums und eines zum Anzeigen der Zeit sind drei Voreinstellungs Formate verfügbar. Legen Sie diese Formate fest, indem Sie eines der folgenden Fenster Stile auswählen.



|                                                                                                       |                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**DTS \_ longdateformat**](date-and-time-picker-control-styles.md)                 | Die Anzeige sieht wie folgt aus: "Friday, 19. April 1996".      |
| [**DTS- \_ shortdateformat**](date-and-time-picker-control-styles.md)               | Die Anzeige sieht wie folgt aus: "4/19/96".                     |
| [**DTS \_ shortdatecenturyformat**](date-and-time-picker-control-styles.md) | **Version 5,80**. Die Anzeige sieht wie folgt aus: "4/19/1996". |
| [**DTS- \_ Zeitformat**](date-and-time-picker-control-styles.md)                         | Die Anzeige sieht wie folgt aus: "5:31:42 pm".                  |



 

### <a name="custom-formats"></a>Benutzerdefinierte Formate

Ein DTP-Steuerelement verwendet eine Format Zeichenfolge, um zu bestimmen, wie Felder mit Informationen angezeigt werden. Wenn die voreingestellten Formate nicht ausreichen, können Sie ein benutzerdefiniertes Format erstellen, indem Sie eine eigene Format Zeichenfolge definieren. Benutzerdefinierte Formate bieten größere Flexibilität für eine Anwendung. Sie ermöglichen es Ihnen, die Reihenfolge anzugeben, in der das Steuerelement Informationsfelder anzeigt. Sie können Textkörper und Rückruf Felder einschließen, um Informationen vom Benutzer anzufordern. Nachdem die Zeichenfolge erstellt wurde, weisen Sie Sie dem DTP-Steuerelement mit einer [**DTM- \_ SetFormat**](dtm-setformat.md) -Nachricht zu.

### <a name="format-strings"></a>Formatzeichenfolgen

Eine DTP-Format Zeichenfolge besteht aus einer Reihe von Elementen, die ein bestimmtes Informationselement darstellen und das Anzeige Format definieren. Die Elemente werden in der Reihenfolge angezeigt, in der Sie in der Format Zeichenfolge angezeigt werden.

Datums-und Uhrzeit Format Elemente werden durch das tatsächliche Datum und die Uhrzeit ersetzt. Sie werden durch die folgenden Zeichen Gruppen definiert.



| Element | BESCHREIBUNG                                                                       |
|---------|-----------------------------------------------------------------------------------|
| "d"     | Der ein-oder zweistellige Tag.                                                        |
| "dd"    | Die zweistellige Tages Angabe. Einstellige Tageswerte werden mit 0 (null) vorangestellt.                |
| "ddd"   | Die aus drei Zeichen bestehende wochentagsabkürzung.                                         |
| "dddd"  | Der vollständige Name des Wochentags.                                                            |
| "h"     | Die einstellige oder zweistellige Stunden Angabe im 12-Stunden-Format.                                     |
| "hh"    | Die zweistellige Stunden Angabe im 12-Stunden-Format. Einstellige Werte werden eine Null vorangestellt. |
| "H"     | Die einstellige oder zweistellige Stunden Angabe im 24-Stunden-Format.                                     |
| "HH"    | Die zweistellige Stunden Angabe im 24-Stunden-Format. Einstellige Werte werden eine Null vorangestellt. |
| "m"     | Die einstellige oder zweistellige Minute.                                                     |
| "mm"    | Die zweistellige Minute. Einstellige Werte werden eine Null vorangestellt.                 |
| "M"     | Die einstellige oder zweistellige Monatszahl.                                               |
| "MM"    | Die zweistellige Monatszahl. Einstellige Werte werden eine Null vorangestellt.           |
| "MMM"   | Die aus drei Zeichen bestehende Monats Abkürzung.                                           |
| "MMMM"  | Der vollständige Monats Name.                                                              |
| "t"     | Die einbuchstabige am/pm-Abkürzung (d. h., wird als "A" angezeigt).              |
| "tt"    | Die zwei buchstabige am/pm-Abkürzung (d. h., wird als "am" angezeigt).             |
| "yy"    | Die letzten zwei Ziffern des Jahres (d. h. 1996 werden als "96" angezeigt).       |
| "yyyy"  | Das vollständige Jahr (d. h. 1996 wird als "1996" angezeigt).                       |



 

Um die Informationen lesbarer zu machen, können Sie der Format Zeichenfolge Text Text hinzufügen, indem Sie ihn in einfache Anführungszeichen einschließen. Leerzeichen und Interpunktions Zeichen müssen nicht in Anführungszeichen eingeschlossen werden.

> [!Note]  
> Nicht formatierende Zeichen, die nicht durch einfache Anführungszeichen voneinander getrennt sind, führen zu unvorhersehbaren Anzeigemöglichkeiten des DTP-Steuer Elements.

Wenn Sie z. b. das aktuelle Datum mit dem Format "" heute anzeigen möchten, ist dies: 04:22:31 Dienstag, 23, 1996 ", die Format Zeichenfolge lautet" "heute:" hh ": 'm": es dddd Mmm dd "," yyyy ". Wenn Sie ein einzelnes Anführungszeichen in ihren TextText einschließen möchten, verwenden Sie zwei aufeinander folgende einfache Anführungszeichen. Wenn Sie z. b. "" nicht vergessen "MMM DD", "yyyy", wird eine Ausgabe erzeugt, die wie folgt aussieht: Don 't Forget Mar 23, 1996. Es ist nicht erforderlich, Anführungszeichen mit dem Komma zu verwenden, daher ist "" nicht vergessen "MMM DD, yyyy" ist ebenfalls gültig und erzeugt dieselbe Ausgabe.

### <a name="callback-fields"></a>Rückruf Felder

Zusätzlich zu den Standard [Format](#format-strings) Zeichenfolgen und TextText können Sie auch bestimmte Teile der Anzeige als [Rückruf Felder](#callback-fields)definieren. Diese Felder können verwendet werden, um den Benutzer nach Informationen abzufragen. Zum Deklarieren eines Rückruf Felds fügen Sie ein oder mehrere "X"-Zeichen (ASCII-Code 88) an beliebiger Stelle in der Format Zeichenfolge ein. Sie können Rückruf Felder erstellen, die eine eindeutige Identität aufweisen, indem Sie das "X"-Zeichen wiederholen. Daher enthält die Format Zeichenfolge "XX dddd Mmm dd", "yyy xxx" zwei eindeutige Rückruf Felder: "XX" und "xxx". Wie andere DTP-Steuerungs Felder werden Rückruf Felder in der Reihenfolge von links nach rechts angezeigt, die auf ihrer Position in der Format Zeichenfolge basiert.

Wenn das DTP-Steuerelement die Format Zeichenfolge analysiert und ein Rückruf Feld erkennt, sendet es das [Dtn- \_ Format](dtn-format.md) und [Dtn \_ formatQuery](dtn-formatquery.md) -Benachrichtigungs Codes. Das FormatString-Element, das dem Rückruf Feld entspricht, ist in den Benachrichtigungen enthalten, damit die empfangende Anwendung bestimmen kann, welches Rückruf Feld abgefragt wird. Der Besitzer des Steuer Elements muss auf diese Benachrichtigungen reagieren, um sicherzustellen, dass die benutzerdefinierten Informationen ordnungsgemäß angezeigt werden.

## <a name="date-and-time-picker-control-notification-messages"></a>Benachrichtigungs Meldungen zur Steuerung von Datums-und Zeitauswahl

Ein DTP-Steuerelement (Datums-und Zeitauswahl) sendet Benachrichtigungs Codes, wenn es Benutzereingaben oder-Prozesse empfängt und auf Rückruf Felder reagiert. Das übergeordnete Element des-Steuer Elements empfängt diese Benachrichtigungs Codes in Form von WM-Benachrichtigungs Meldungen. [**\_**](wm-notify.md)

Die folgenden Benachrichtigungs Codes werden bei DTP-Steuerelementen verwendet.



| Benachrichtigungs Code                             | BESCHREIBUNG                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DTN- \_ Schließung](dtn-closeup.md)               | Gibt an, dass der Dropdown-Monatskalender entfernt werden soll.                                                                                                                                               |
| [DTN \_ datetimechange](dtn-datetimechange.md) | Signalisiert eine Änderung im DTP-Steuerelement.                                                                                                                                                                          |
| [DTN- \_ Dropdown](dtn-dropdown.md)             | Gibt an, dass der Dropdown-Monatskalender angezeigt wird.                                                                                                                                             |
| [DTN- \_ Format](dtn-format.md)                 | Fordert Text auf, der in einem Teil der Format Zeichenfolge angezeigt wird, die als Rückruf Feld beschrieben wird.                                                                                                                         |
| [DTN \_ formatQuery](dtn-formatquery.md)       | Fordert Informationen über die maximal zulässige Größe des Texts an, der in einem Rückruf Feld angezeigt werden soll.                                                                                                            |
| [DTN \_ UserString](dtn-userstring.md)         | Signalisiert das Ende des Bearbeitungsvorgangs eines Benutzers im-Steuerelement. Diese Benachrichtigung wird nur von DTP-Steuerelementen gesendet, die den [**DTS \_ appcananalyse**](date-and-time-picker-control-styles.md) -Stil verwenden. |
| [DTN \_ wmKeyDown](dtn-wmkeydown.md)           | Signalisiert, dass der Benutzer eine Taste in einem Rückruf Feld des DTP-Steuer Elements gedrückt hat.                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Verweis für Datums-und Zeitauswahl](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 