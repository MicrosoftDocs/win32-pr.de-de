---
title: Informationen zu Steuerelementen für die Datums- und Uhrzeitauswahl
description: Ein DTP-Steuerelement (Datums- und Uhrzeitauswahl) bietet eine einfache und intuitive Schnittstelle, über die Sie Datums- und Uhrzeitinformationen mit einem Benutzer austauschen können.
ms.assetid: 6749c3ae-2c52-4183-ac4e-68ca7ebf1e13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182381c40b636683255e95ba0680a1245ef0adf3
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424220"
---
# <a name="about-date-and-time-picker-controls"></a>Informationen zu Steuerelementen für die Datums- und Uhrzeitauswahl

Ein *DTP-Steuerelement* (Datums- und Uhrzeitauswahl) bietet eine einfache und intuitive Schnittstelle, über die Sie Datums- und Uhrzeitinformationen mit einem Benutzer austauschen können. Mit einem DTP-Steuerelement können Sie den Benutzer beispielsweise auffordern, ein Datum ein- und dann die Auswahl einfach abzurufen.

Die folgenden Themen werden erörtert:

-   [Datums- und Uhrzeitauswahl Benutzeroberfläche](#date-and-time-picker-user-interface)
-   [Datums- und Uhrzeitauswahl-Steuerelementstile und -formate](#date-and-time-picker-control-styles-and-formats)
    -   [Voreingestellte Formate](#preset-formats)
    -   [Benutzerdefinierte Formate](#custom-formats)
    -   [Formatzeichenfolgen](#format-strings)
    -   [Rückruffelder](#callback-fields)
-   [Benachrichtigungsmeldungen zur Datums- und Uhrzeitauswahl](#date-and-time-picker-control-notification-messages)
-   [Verwandte Themen](#related-topics)

> [!Note]
> Windows unterstützt keine Datumsangaben vor 1601. Weitere Informationen finden Sie in der [**FILETIME-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
>
> Das Steuerelement basiert auf dem gregorianischen Kalender, der 1753 eingeführt wurde. Es werden keine Datumsangaben berechnet, die mit dem Kalender "Chef" konsistent sind.

## <a name="date-and-time-picker-user-interface"></a>Datums- und Uhrzeitauswahl Benutzeroberfläche

Der Clientbereich eines DTP-Steuerelements (Datums- und Uhrzeitauswahl) zeigt Datums- oder Uhrzeitinformationen oder beides an und fungiert als Schnittstelle, über die Benutzer die Informationen ändern. Das Datum kann in einem Kalender oder mithilfe eines Auf-Ab-Steuerelements ausgewählt werden. Die Uhrzeit kann geändert werden, indem Sie Felder eingeben, die durch die Formatzeichenfolgen des [Steuerelements definiert sind.](#format-strings) Optional zeigt das Steuerelement ein Kontrollkästchen an. Wenn es aktiviert ist, kann der Wert im -Steuerelement abgerufen werden. Andernfalls gilt das Steuerelement als nicht initialisiert.

Die folgende Abbildung zeigt ein Fenster, das drei Datumsauswahl-Steuerelemente enthält. Das erste Datumsauswahl-Steuerelement wurde mit dem [**DTS \_ SHOWNONE-Stil**](date-and-time-picker-control-styles.md) erstellt, das zweite mit dem [**DTS \_ UPDOWN-Stil**](date-and-time-picker-control-styles.md) und das dritte steuerelement ohne spezielle Stile. Im dritten Steuerelement hat der Benutzer auf den Pfeil nach unten geklickt, um den Kalender anzuzeigen.

![Screenshot eines Fensters, das drei Stile von Datumsauswahl-Steuerelementen veranschaulicht](images/dtpdatepick.png)

Die folgende Abbildung zeigt ein Fenster mit drei Steuerelementen, die die Uhrzeit enthalten.

Das erste Steuerelement wurde mit dem [**FORMAT DTS \_ TIMEFORMAT**](date-and-time-picker-control-styles.md) erstellt und zeigt die Zeit in der Standardzeit an, die aus vier Feldern besteht. Der Benutzer kann einen gültigen Wert in eines dieser Felder eingeben oder das Feld auswählen und den Wert mithilfe des Nach-unten-Steuerelements oder der Pfeiltasten ändern.

Das zweite Steuerelement zeigt einen benutzerdefinierten Formatsatz mithilfe von [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)an. Wie beim ersten Steuerelement kann der Benutzer die Zeitfelder ändern, indem er oder die Pfeiltasten eingibt. Der Wochentag kann durch Auswählen eines Datums im Kalender geändert werden, das geöffnet wird, wenn der Benutzer auf den Pfeil nach unten klickt.

Das dritte Steuerelement zeigt, wie beliebiger Text zum Steuerelement hinzugefügt werden kann. Der Benutzer kann eine Stunde (von 1 bis 24) auswählen, indem er eingibt, die Pfeiltasten verwendet oder das Steuerelement nach oben verwendet.

![Screenshot eines Fensters mit drei Steuerelementen, die die Zeit enthalten](images/dtpdatetimepick.png)

Das DTP-Steuerelement aktualisiert automatisch interne Informationen basierend auf der Eingabe des Benutzers. Das Steuerelement erkennt Folgendes als gültige Eingabe.



| Eingabekategorie | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pfeiltasten     | Das Steuerelement akzeptiert Pfeiltasten, um durch die Felder im Steuerelement zu navigieren und Werte zu ändern. Der Benutzer kann die Taste oder drücken, um das Steuerelement zu durchlaufen. Wenn der Benutzer versucht, das letzte Feld in einer bestimmten Richtung zu durchlaufen, wird der Tastaturfokus auf das Feld auf der gegenüberliegenden Seite des Steuerelements "umbrochen". Die Schlüssel und ändern werte im aktuellen Feld inkrementell. |
| Ende und Startseite   | Das Steuerelement akzeptiert die virtuellen Schlüssel VK END und VK HOME, um den Wert innerhalb des aktuellen Felds in die oberen bzw. unteren \_ \_ Grenzwerte zu ändern.                                                                                                                                                                                                                          |
| Funktionstasten  | Der Schlüssel aktiviert den Bearbeitungsmodus. Die Taste bewirkt, dass das Steuerelement ein Dropdown-Monatskalender-Steuerelement an angezeigt (durch Drücken von wird dies auch gemacht).                                                                                                                                                                                                                                          |
| Zahlen        | Das -Steuerelement akzeptiert numerische Eingaben in Segmenten mit zwei Zeichen. Wenn der vom Benutzer eingegebene Wert ungültig ist (z. B. das Festlegen des Monats auf 14), lehnt das Steuerelement ihn ab und setzt die Anzeige auf den vorherigen Wert zurück.                                                                                                                                                                |
| Plus und Minus | Das Steuerelement akzeptiert die virtuellen VK-Schlüssel ADD und VK SUBTRACT von der numerischen Tastatur, um den Wert im aktuellen Feld zu erhöhen \_ \_ und zu dekrementieren.                                                                                                                                                                                                                             |



 

DTP-Steuerelemente, die nicht den [**DTS \_ UPDOWN-Stil**](date-and-time-picker-control-styles.md) verwenden, zeigen eine Pfeilschaltfläche an. Wenn der Benutzer auf diese Schaltfläche klickt, fällt ein Monatskalender-Steuerelement aus. Der Benutzer kann ein bestimmtes Datum auswählen, indem er auf einen Bereich des Kalenders klickt.

## <a name="date-and-time-picker-control-styles-and-formats"></a>Datums- und Uhrzeitauswahl-Steuerelementstile und -formate

DTP-Steuerelemente (Datums- und [](date-and-time-picker-control-styles.md) Uhrzeitauswahl) verfügen über mehrere Datums- und Uhrzeitauswahl-Steuerelementstile, die die Darstellung und das Verhalten eines Steuerelements bestimmen. Geben Sie den Stil beim Erstellen des Steuerelements mit dem *dwStyle-Parameter* von [**CreateWindowEx an.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Verwenden Sie [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) und [**SetWindowLong,**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)um den Fensterstil nach dem Erstellen des Steuerelements abzurufen oder zu ändern.

### <a name="preset-formats"></a>Voreingestellte Formate

Es gibt drei voreingestellte Formate zum Anzeigen des Datums und eines für die Anzeige der Uhrzeit. Legen Sie diese Formate fest, indem Sie einen der folgenden Fensterstile auswählen.



|   Format                                                                                                    |   BESCHREIBUNG                                                         |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**DTS \_ LONGDATEFORMAT**](date-and-time-picker-control-styles.md)                 | Die Anzeige sieht wie folgt aus: "Friday, April 19, 1996".      |
| [**DTS \_ SHORTDATEFORMAT**](date-and-time-picker-control-styles.md)               | Die Anzeige sieht wie folgt aus: "19.04.96".                     |
| [**DTS \_ SHORTDATECENTURYFORMAT**](date-and-time-picker-control-styles.md) | **Version 5.80.** Die Anzeige sieht wie folgt aus: "19.4.1996". |
| [**DTS \_ TIMEFORMAT**](date-and-time-picker-control-styles.md)                         | Die Anzeige sieht wie folgt aus: "17:31:42 Uhr".                  |



 

### <a name="custom-formats"></a>Benutzerdefinierte Formate

Ein DTP-Steuerelement verwendet eine Formatzeichenfolge, um zu bestimmen, wie Informationsfelder angezeigt werden. Wenn die voreingestellten Formate nicht ausreichen, können Sie ein benutzerdefiniertes Format erstellen, indem Sie Eine eigene Formatzeichenfolge definieren. Benutzerdefinierte Formate bieten mehr Flexibilität für eine Anwendung. Sie ermöglichen es Ihnen, die Reihenfolge anzugeben, in der das Steuerelement Informationsfelder anzeigt. Sie können Texttext sowie Rückruffelder zum Anfordern von Informationen vom Benutzer einschließen. Nachdem die Zeichenfolge erstellt wurde, weisen Sie sie dem DTP-Steuerelement mit einer [**FTP \_ SETFORMAT-Meldung**](dtm-setformat.md) zu.

### <a name="format-strings"></a>Formatzeichenfolgen

Eine DTP-Formatzeichenfolge besteht aus einer Reihe von Elementen, die eine bestimmte Information darstellen und das Anzeigeformat definieren. Die Elemente werden in der Reihenfolge angezeigt, in der sie in der Formatzeichenfolge angezeigt werden.

Datums- und Uhrzeitformatelemente werden durch das tatsächliche Datum und die tatsächliche Uhrzeit ersetzt. Sie werden durch die folgenden Zeichengruppen definiert.



| Element | BESCHREIBUNG                                                                       |
|---------|-----------------------------------------------------------------------------------|
| "d"     | Der ein- oder zweistellige Tag.                                                        |
| "dd"    | Der zweistellige Tag. Einstelligen Tageswerten wird eine Null vorangehende.                |
| "ddd"   | Die Drei-Zeichen-Abkürzung für Wochentage.                                         |
| "dddd"  | Der vollständige Wochentagsname.                                                            |
| "h"     | Die ein- oder zweistellige Stunde im 12-Stunden-Format.                                     |
| "hh"    | Die zweistellige Stunde im 12-Stunden-Format. Einstelligen Werten wird eine Null vorangehende. |
| "H"     | Die ein- oder zweistellige Stunde im 24-Stunden-Format.                                     |
| "HH"    | Die zweistellige Stunde im 24-Stunden-Format. Einstelligen Werten wird eine Null vorangehende. |
| "m"     | Die ein- oder zweistellige Minute.                                                     |
| "mm"    | Die zweistellige Minute. Einstelligen Werten wird eine Null vorangehende.                 |
| "M"     | Die ein- oder zweistellige Monatszahl.                                               |
| "MM"    | Die zweistellige Monatszahl. Einstelligen Werten wird eine Null vorangehende.           |
| "MMM"   | Die Drei-Zeichen-Monatsabkürzung.                                           |
| "MMMM"  | Der vollständige Monatsname.                                                              |
| "t"     | Die Abkürzung am/PM mit einem Buchstaben (d. h. AM wird als "A" angezeigt).              |
| "tt"    | Die zweibuchstabige Am/PM-Abkürzung (d.h. AM wird als "AM" angezeigt).             |
| "yy"    | Die letzten beiden Ziffern des Jahres (d. b. 1996 werden als "96" angezeigt).       |
| "yyyy"  | Das gesamte Jahr (d.b. 1996 wird als "1996" angezeigt).                       |



 

Um die Informationen lesbarer zu machen, können Sie text text zur Formatzeichenfolge hinzufügen, indem Sie sie in einfache Anführungszeichen einschließen. Leerzeichen und Satzzeichen müssen nicht in Anführungszeichen stehen.

> [!Note]  
> Nicht formatierte Zeichen, die nicht durch einfache Anführungszeichen getrennt sind, führen zu einer unvorhersehbaren Anzeige durch das DTP-Steuerelement.

Um z. B. das aktuelle Datum im Format "'Today is: 04:22:31 Tuesday Mar 23, 1996' anzuzeigen, lautet die Formatzeichenfolge "'Today is: 'hh':'m':es dddd MMM dd', 'yyyy". Verwenden Sie zwei aufeinander folgende einfache Anführungszeichen, um ein einfaches Anführungszeichen in ihren Text aufzunehmen. Beispielsweise erzeugt "'Don't forget' MMM dd',' yyyy" eine Ausgabe, die wie folgt aussieht: Do not forget Mar 23, 1996. Es ist nicht erforderlich, Anführungszeichen mit dem Komma zu verwenden, sodass "'Don't forget' MMM dd, yyyy" ebenfalls gültig ist und die gleiche Ausgabe erzeugt.

### <a name="callback-fields"></a>Rückruffelder

Zusätzlich zu den [Standardformatzeichenfolgen](#format-strings) und Textkörpern können Sie bestimmte Teile der Anzeige auch als [Rückruffelder](#callback-fields)definieren. Diese Felder können verwendet werden, um den Benutzer nach Informationen abzufragen. Um ein Rückruffeld zu deklarieren, fügen Sie ein oder mehrere "X"-Zeichen (ASCII-Code 88) an einer beliebigen Stelle in die Formatzeichenfolge ein. Sie können Rückruffelder mit einer eindeutigen Identität erstellen, indem Sie das Zeichen "X" wiederholen. Daher enthält die Formatzeichenfolge "XX dddd MMM dd", "yyyy XXX" zwei eindeutige Rückruffelder, "XX" und "XXX". Wie andere DTP-Steuerelementfelder werden Rückruffelder in der Reihenfolge von links nach rechts angezeigt, basierend auf ihrer Position in der Formatzeichenfolge.

Wenn das DTP-Steuerelement die Formatzeichenfolge analysiert und auf ein Rückruffeld trifft, sendet es [DTN \_ FORMAT-](dtn-format.md) und [DTN \_ FORMATQUERY-Benachrichtigungscodes.](dtn-formatquery.md) Das Formatzeichenfolgenelement, das dem Rückruffeld entspricht, ist in den Benachrichtigungen enthalten, damit die empfangende Anwendung bestimmen kann, welches Rückruffeld abgefragt wird. Der Besitzer des Steuerelements muss auf diese Benachrichtigungen reagieren, um sicherzustellen, dass die benutzerdefinierten Informationen ordnungsgemäß angezeigt werden.

## <a name="date-and-time-picker-control-notification-messages"></a>Benachrichtigungsmeldungen zur Datums- und Uhrzeitauswahl

Ein DTP-Steuerelement (Datums- und Uhrzeitauswahl) sendet Benachrichtigungscodes, wenn es Benutzereingaben empfängt oder verarbeitet und auf Rückruffelder reagiert. Das übergeordnete Element des Steuerelements empfängt diese Benachrichtigungscodes in Form von [**WM \_ NOTIFY-Nachrichten.**](wm-notify.md)

Die folgenden Benachrichtigungscodes werden mit DTP-Steuerelementen verwendet.



| Benachrichtigungscode                             | BESCHREIBUNG                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DTN \_ CLOSEUP](dtn-closeup.md)               | Gibt an, dass der Dropdown-Monatskalender entfernt werden soll.                                                                                                                                               |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) | Signalisiert eine Änderung innerhalb des DTP-Steuerelements.                                                                                                                                                                          |
| [\_DTN-DROPDOWNliste](dtn-dropdown.md)             | Gibt an, dass der Dropdown-Monatskalender angezeigt wird.                                                                                                                                             |
| [\_DTN-FORMAT](dtn-format.md)                 | Fordert Text an, der in einem Teil der Formatzeichenfolge angezeigt werden soll, der als Rückruffeld beschrieben wird.                                                                                                                         |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)       | Fordert Informationen zur maximal zulässigen Größe des Texts an, der in einem Rückruffeld angezeigt werden soll.                                                                                                            |
| [DTN \_ USERSTRING](dtn-userstring.md)         | Signalisiert das Ende des Bearbeitungsvorgang eines Benutzers innerhalb des Steuerelements. Diese Benachrichtigung wird nur von DTP-Steuerelementen gesendet, die den [**DTS \_ APPCANPARSE-Stil**](date-and-time-picker-control-styles.md) verwenden. |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)           | Signalisiert, dass der Benutzer eine Taste in einem Rückruffeld des DTP-Steuerelements gedrückt hat.                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementreferenz zur Datums- und Uhrzeitauswahl](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 