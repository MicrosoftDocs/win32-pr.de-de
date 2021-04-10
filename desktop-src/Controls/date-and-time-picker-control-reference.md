---
title: Datums-und Zeitauswahl
description: Dieser Abschnitt enthält Informationen zu den API-Elementen, die mit Datums-und Zeitauswahl Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\datetime\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4e91b325b798ff465d8048cac2f0a9a72e5774
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858513"
---
# <a name="date-and-time-picker"></a>Datums-und Zeitauswahl

Dieser Abschnitt enthält Informationen zu den API-Elementen, die mit Datums-und Zeitauswahl Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                                                    | Inhalte                                                                                                                                                     |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Steuerelementen für Datums-und Zeitauswahl](date-and-time-picker-controls.md) | Ein *DTP-Steuerelement (Datums-und Zeitauswahl)* stellt eine einfache und intuitive Oberfläche bereit, mit der Datums-und Uhrzeit Informationen an einen Benutzer ausgetauscht werden können.<br/> |
| [Verwenden von Steuerelementen für Datums-und Zeitauswahl](using-date-and-time-picker.md)    | Dieser Abschnitt enthält Informationen und Beispielcode für die Implementierung von Steuerelementen für Datums-und Zeitauswahl. <br/>                                                |



 

### <a name="macros"></a>Makros



| Thema                                                                     | Inhalte                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DateTime \_ closemonthcal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)                 | Schließt das Steuerelement für die Datums-und Zeitauswahl (DTP). Verwenden Sie dieses Makro, oder senden Sie die [**DTM- \_ closemonthcal**](dtm-closemonthcal.md) -Nachricht explizit.<br/>                                                                                                                     |
| [**DateTime \_ getdatetimepickerinfo**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getdatetimepickerinfo) | Ruft Informationen für ein bestimmtes DTP-Steuerelement (Datums-und Zeitauswahl) ab.<br/>                                                                                                                                                                                              |
| [**DateTime- \_ getidealsize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)                   | Ruft die Größe ab, die zum Anzeigen des Steuer Elements ohne Clipping benötigt wird. Verwenden Sie dieses Makro, oder senden Sie die [**DTM- \_ getidealsize**](dtm-getidealsize.md) -Nachricht explizit.<br/>                                                                                                        |
| [**DateTime- \_ getmonthcal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal)                     | Ruft das Handle für das Kalender Steuerelement (DTP) des untergeordneten Monats eines Datums und einer Uhrzeit Auswahl ab. Sie können dieses Makro verwenden oder die [**DTM- \_ getmonthcal**](dtm-getmonthcal.md) -Nachricht explizit senden. <br/>                                                                               |
| [**DateTime \_ getmonthcalcolor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor)           | Ruft die Farbe für einen angegebenen Teil des Monats Kalenders innerhalb eines DTP-Steuer Elements ab. Sie können dieses Makro verwenden oder die [**DTM- \_ getmccolor**](dtm-getmccolor.md) -Nachricht explizit senden. <br/>                                                           |
| [**DateTime \_ getmonthcalfont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)             | Ruft die Schriftart ab, die das untergeordnete Monatskalender-Steuerelement des Datums-und Zeitauswahl Steuer Elements gegenwärtig verwendet. Sie können dieses Makro verwenden oder die [**DTM- \_ getmcfont**](dtm-getmcfont.md) -Nachricht explizit senden. <br/>                                                      |
| [**DateTime \_ getmonthcalstyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)           | Ruft den Stil eines angegebenen DTP-Steuer Elements ab. Verwenden Sie dieses Makro, oder senden Sie die [**DTM- \_ getmcstyle**](dtm-getmcstyle.md) -Nachricht explizit.<br/>                                                                                                                               |
| [**DateTime- \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange)                           | Ruft die aktuellen minimal-und maximal zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) ab. Sie können dieses Makro verwenden oder die DTM- [**\_ GetRange**](dtm-getrange.md) -Nachricht explizit senden. <br/>                                                              |
| [**DateTime- \_ GetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime)                 | Ruft den aktuell ausgewählten Zeitpunkt von einem DTP-Steuerelement (Date and Time Picker) ab und platziert ihn in einer angegebenen [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur. Sie können dieses Makro verwenden oder die DTM- [**\_ GetSystemTime**](dtm-getsystemtime.md) -Nachricht explizit senden. <br/> |
| [**DateTime- \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)                         | Legt die Anzeige eines DTP-Steuer Elements auf der Grundlage einer angegebenen Format Zeichenfolge fest. Sie können dieses Makro verwenden oder die [**DTM- \_ SetFormat**](dtm-setformat.md) -Nachricht explizit senden. <br/>                                                                          |
| [**DateTime- \_ setmonthcalcolor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor)           | Legt die Farbe für einen bestimmten Teil des Monats Kalenders innerhalb eines DTP-Steuer Elements fest. Sie können dieses Makro verwenden oder die [**DTM- \_ ltmccolor**](dtm-setmccolor.md) -Nachricht explizit senden. <br/>                                                           |
| [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)             | Legt die Schriftart fest, die vom untergeordneten Monatskalender-Steuerelement des Steuer Elements für die Datums-und Uhrzeit Auswahl verwendet werden soll. Sie können dieses Makro verwenden oder explizit die [**DTM- \_**](dtm-setmcfont.md) Nachricht "Absenden" senden. <br/>                                                                |
| [**DateTime- \_ setmonthcalstyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)           | Legt den Stil für ein angegebenes DTP-Steuerelement fest. Verwenden Sie dieses Makro, oder senden Sie die [**DTM- \_ ltmcstyle**](dtm-setmcstyle.md) -Nachricht explizit.<br/>                                                                                                                              |
| [**DateTime- \_ Sekunden**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange)                           | Legt die minimalen und maximalen zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) fest. Sie können dieses Makro verwenden oder die [**DTM- \_ ltrange**](dtm-setrange.md) -Nachricht explizit senden. <br/>                                                                       |
| [**DateTime- \_ SetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)                 | Legt das Steuerelement für Datums-und Zeitauswahl (DTP) auf ein bestimmtes Datum und eine bestimmte Uhrzeit fest. Sie können dieses Makro verwenden oder die [**DTM- \_ SetSystemTime**](dtm-setsystemtime.md) -Nachricht explizit senden. <br/>                                                                                       |



 

### <a name="messages"></a>Meldungen



| Thema                                                           | Inhalte                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DTM \_ closemonthcal**](dtm-closemonthcal.md)                 | Schließt ein DTP-Steuerelement. Senden Sie diese Nachricht explizit oder mithilfe des " [**DateTime \_ closemonthcal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) "-Makros.<br/>                                                                                                                                        |
| [**DTM \_ getdatetimepickerinfo**](dtm-getdatetimepickerinfo.md) | Ruft Informationen zu einem DTP-Steuerelement (Datums-und Zeitauswahl) ab.<br/>                                                                                                                                                                                                                  |
| [**DTM- \_ getidealsize**](dtm-getidealsize.md)                   | Ruft die Größe ab, die zum Anzeigen des Steuer Elements ohne Clipping benötigt wird. Senden Sie diese Nachricht explizit oder mithilfe des " [**DateTime \_ getidealsize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) "-Makros.<br/>                                                                                                  |
| [**DTM \_ getmccolor**](dtm-getmccolor.md)                       | Ruft die Farbe für einen angegebenen Teil des Monats Kalenders innerhalb eines DTP-Steuer Elements ab. Sie können diese Nachricht explizit senden oder das " [**DateTime \_ getmonthcalcolor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) "-Makro verwenden. <br/>                                              |
| [**DTM \_ getmcfont**](dtm-getmcfont.md)                         | Ruft die Schriftart ab, die das untergeordnete Monatskalender-Steuerelement des Datums-und Zeitauswahl Steuer Elements gegenwärtig verwendet. Sie können diese Nachricht explizit senden oder das " [**DateTime \_ getmonthcalfont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) "-Makro verwenden. <br/>                                         |
| [**DTM \_ getmcstyle**](dtm-getmcstyle.md)                       | Ruft den Stil eines DTP-Steuer Elements ab. Senden Sie diese Nachricht explizit oder mithilfe des [**DateTime- \_ getmonthcalstyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) -Makros.<br/>                                                                                                                       |
| [**DTM \_ getmonthcal**](dtm-getmonthcal.md)                     | Ruft das Handle für das Kalender Steuerelement (DTP) des untergeordneten Monats eines Datums und einer Uhrzeit Auswahl ab. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ getmonthcal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) -Makro verwenden. <br/>                                                                              |
| [**DTM- \_ GetRange**](dtm-getrange.md)                           | Ruft die aktuellen minimal-und maximal zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) ab. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) -Makro verwenden. <br/>                                                              |
| [**DTM \_ GetSystemTime**](dtm-getsystemtime.md)                 | Ruft den aktuell ausgewählten Zeitpunkt von einem DTP-Steuerelement (Date and Time Picker) ab und platziert ihn in einer angegebenen [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ GetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) -Makro verwenden. <br/> |
| [**DTM- \_ SetFormat**](dtm-setformat.md)                         | Legt die Anzeige eines DTP-Steuer Elements auf der Grundlage einer angegebenen Format Zeichenfolge fest. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) -Makro verwenden. <br/>                                                                         |
| [**DTM-Abbild \_ Farbe**](dtm-setmccolor.md)                       | Legt die Farbe für einen bestimmten Teil des Monats Kalenders innerhalb eines DTP-Steuer Elements fest. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ setmonthcalcolor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) -Makro verwenden. <br/>                                              |
| [**DTM- \_ Abschrift**](dtm-setmcfont.md)                         | Legt die Schriftart fest, die vom untergeordneten Monatskalender-Steuerelement des Steuer Elements für die Datums-und Uhrzeit Auswahl verwendet werden soll. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) -Makro verwenden.<br/>                                                    |
| [**DTM \_ -Format**](dtm-setmcstyle.md)                       | Legt den Stil eines DTP-Steuer Elements fest. Senden Sie diese Nachricht explizit oder mithilfe des [**DateTime- \_ setmonthcalstyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) -Makros.<br/>                                                                                                                       |
| [**DTM-über \_ Tragung**](dtm-setrange.md)                           | Legt die minimalen und maximalen zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) fest. Sie können diese Nachricht explizit senden oder das " [**DateTime \_**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) "-Makro verwenden. <br/>                                                                      |
| [**DTM- \_ SetSystemTime**](dtm-setsystemtime.md)                 | Legt die Zeit in einem DTP-Steuerelement (Datums-und Zeitauswahl) fest. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ SetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) -Makro verwenden. <br/>                                                                                                   |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                   | Inhalte                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DTN- \_ Schließung](dtn-closeup.md)                         | Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer den Dropdown-Monatskalender schließt. Der Monatskalender wird geschlossen, wenn der Benutzer ein Datum aus dem Monatskalender auswählt oder auf den Dropdown Pfeil klickt, während der Kalender geöffnet ist. <br/>                                                                                                      |
| [DTN \_ datetimechange](dtn-datetimechange.md)           | Wird von einem Steuerelement für die Datums-und Zeitauswahl (DTP) gesendet, wenn eine Änderung auftritt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                                                                                  |
| [DTN- \_ Dropdown](dtn-dropdown.md)                       | Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer den Dropdown-Monatskalender aktiviert. <br/>                                                                                                                                                                                                                                               |
| [DTN- \_ Format](dtn-format.md)                           | Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) zum Anfordern von Text gesendet, der in einem Rückruf Feld angezeigt werden soll. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                                                       |
| [DTN \_ formatQuery](dtn-formatquery.md)                 | Wird von einem DTP-Steuerelement gesendet, um die maximal zulässige Größe der Zeichenfolge abzurufen, die in einem Rückruf Feld angezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                           |
| [DTN \_ UserString](dtn-userstring.md)                   | Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn ein Benutzer das Bearbeiten einer Zeichenfolge im-Steuerelement beendet. Dieser Benachrichtigungs Code wird nur von DTP-Steuerelementen gesendet, die auf den [**DTS \_ appcananalyse**](date-and-time-picker-control-styles.md) -Stil festgelegt sind. Diese Meldung wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/> |
| [DTN \_ wmKeyDown](dtn-wmkeydown.md)                     | Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer ein Rückruf Feld eingibt. Diese Meldung wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                                                                             |
| [NM- \_ killfokus (Datum/Uhrzeit)](nm-killfocus-date-time.md) | Benachrichtigt das übergeordnete Fenster eines Steuer Elements für Datum und Uhrzeit, dass das Steuerelement den Eingabefokus verloren hat. [**Nm \_ Killfocus (Datum/Uhrzeit)**](nm-killfocus-date-time.md) wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                 |
| [NM \_ SetFocus (Datum/Uhrzeit)](nm-setfocus-date-time-.md)  | Benachrichtigt das übergeordnete Fenster eines Steuer Elements für Datum und Uhrzeit, dass das Steuerelement den Eingabefokus erhalten hat. [Nm \_ SetFocus (Datum/Uhrzeit)](nm-setfocus-date-time-.md) wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                  |



 

### <a name="structures"></a>Strukturen



| Thema                                                  | Inhalte                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Datetimepickerinfo**](/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo)       | Enthält Informationen zu einem DTP-Steuerelement. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**Nmdatetimechange**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange)           | Enthält Informationen zu einer Änderung, die in einem Steuerelement für Datums-und Zeitauswahl (DTP) vorgenommen wurde. Diese Struktur wird mit dem [Dtn \_ datetimechange](dtn-datetimechange.md) -Benachrichtigungs Code verwendet. <br/>                                                                                                                                                                                     |
| [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata)           | Enthält Informationen zu einem Teil der Format Zeichenfolge, der ein Rückruf Feld innerhalb eines DTP-Steuer Elements (Datums-und Zeitauswahl) definiert. Sie enthält die Teil Zeichenfolge, die das Rückruf Feld definiert und einen Puffer enthält, um die Zeichenfolge zu empfangen, die im Rückruf Feld angezeigt wird. Diese Struktur wird im [Dtn- \_ Format](dtn-format.md) -Benachrichtigungs Code verwendet. <br/>               |
| [**Nmdatetimeformatquery**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) | Enthält Informationen über das Rückruf Feld für die Auswahl von Datums-und Zeitauswahl (DTP). Sie enthält eine Teil Zeichenfolge (entnommen aus der Format Zeichenfolge des Steuer Elements), die ein Rückruf Feld definiert. Die-Struktur empfängt die maximal zulässige Größe des Texts, der im Rückruf Feld angezeigt wird. Diese Struktur wird mit dem [Dtn \_ formatQuery](dtn-formatquery.md) -Benachrichtigungs Code verwendet. <br/> |
| [**Nmdatetimestring**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa)           | Enthält Informationen zu einem Bearbeitungsvorgang, der in einem Steuerelement für Datums-und Zeitauswahl (DTP) stattfindet. Diese Meldung wird mit dem [ \_ benutzerdefinierten Benutzer Zeichenfolgen](dtn-userstring.md) -Benachrichtigungs Code verwendet. <br/>                                                                                                                                                                                |
| [**Nmdatetimewmkeydown**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna)     | Enthält Informationen, die zum beschreiben und behandeln eines [Dtn- \_ wmKeyDown](dtn-wmkeydown.md) -Benachrichtigungs Codes verwendet werden. <br/>                                                                                                                                                                                                                                                                               |



 

### <a name="constants"></a>Konstanten



| Thema                                                                          | Inhalte                                                                                |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Steuerelement Stile für Datums-und Zeitauswahl](date-and-time-picker-control-styles.md) | Die hier aufgeführten Fenster Stile sind spezifisch für Steuerelemente für Datums-und Zeitauswahl.<br/> |



 

 

