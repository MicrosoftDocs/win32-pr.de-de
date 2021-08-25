---
title: Datums- und Uhrzeitauswahl
description: Dieser Abschnitt enthält Informationen zu den API-Elementen, die mit Steuerelementen für die Datums- und Uhrzeitauswahl verwendet werden.
ms.assetid: vs|controls|~\controls\datetime\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b29aa1bf7552b87f18a9ded05b67fc8e47770c01431af4da897f2b9733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929480"
---
# <a name="date-and-time-picker"></a>Datums- und Uhrzeitauswahl

Dieser Abschnitt enthält Informationen zu den API-Elementen, die mit Steuerelementen für die Datums- und Uhrzeitauswahl verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                                                    | Inhalte                                                                                                                                                     |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Steuerelementen für die Datums- und Uhrzeitauswahl](date-and-time-picker-controls.md) | Ein *DTP-Steuerelement* (Datums- und Uhrzeitauswahl) bietet eine einfache und intuitive Schnittstelle zum Austauschen von Datums- und Uhrzeitinformationen mit einem Benutzer.<br/> |
| [Verwenden von Steuerelementen für die Datums- und Uhrzeitauswahl](using-date-and-time-picker.md)    | Dieser Abschnitt enthält Informationen und Beispielcode zum Implementieren von Steuerelementen für die Datums- und Uhrzeitauswahl. <br/>                                                |



 

### <a name="macros"></a>Makros



| Thema                                                                     | Inhalte                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)                 | Schließt das DTP-Steuerelement (Date and Time Picker). Verwenden Sie dieses Makro, oder senden Sie die [**MELDUNG \_ CLOSEMONTHCAL**](dtm-closemonthcal.md) explizit.<br/>                                                                                                                     |
| [**DateTime \_ GetDateTimePickerInfo**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getdatetimepickerinfo) | Ruft Informationen für ein angegebenes DTP-Steuerelement (Date and Time Picker) ab.<br/>                                                                                                                                                                                              |
| [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)                   | Ruft die Größe ab, die zum Anzeigen des Steuerelements ohne Clipping erforderlich ist. Verwenden Sie dieses Makro, oder senden Sie explizit die [**MESSAGEFID \_ GETIDEALSIZE.**](dtm-getidealsize.md)<br/>                                                                                                        |
| [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal)                     | Ruft das Handle für das Untergeordnete Monatskalender-Steuerelement einer Datums- und Uhrzeitauswahl (DTP) ab. Sie können dieses Makro verwenden oder die [**MESSAGE-Nachricht VOM ANT \_ GETMONTHCAL**](dtm-getmonthcal.md) explizit senden. <br/>                                                                               |
| [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor)           | Ruft die Farbe für einen bestimmten Teil des Monatskalenders innerhalb eines DTP-Steuerelements (Date and Time Picker) ab. Sie können dieses Makro verwenden oder die [**MESSAGE-Nachricht VOM ANT \_ GETMCCOLOR**](dtm-getmccolor.md) explizit senden. <br/>                                                           |
| [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)             | Ruft die Schriftart ab, die das untergeordnete Monatskalender-Steuerelement des DTP-Steuerelements (Date and Time Picker) derzeit verwendet. Sie können dieses Makro verwenden oder die [**FEHLERMELDUNG \_ GETMCFONT-Nachricht**](dtm-getmcfont.md) explizit senden. <br/>                                                      |
| [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)           | Ruft den Stil eines angegebenen DTP-Steuerelements ab. Verwenden Sie dieses Makro, oder senden Sie explizit die [**MELDUNG FÜR DIE MELDUNG \_ GETMCSTYLE.**](dtm-getmcstyle.md)<br/>                                                                                                                               |
| [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange)                           | Ruft die aktuellen minimalen und maximalen zulässigen Systemzeiten für ein Datums- und Uhrzeitauswahl-Steuerelement (DTP) ab. Sie können dieses Makro verwenden oder die [**MESSAGE-Nachricht VOM ANT \_ GETRANGE-Objekt**](dtm-getrange.md) explizit senden. <br/>                                                              |
| [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime)                 | Ruft die aktuell ausgewählte Uhrzeit aus einem DTP-Steuerelement (Date and Time Picker) ab und platziert sie in einer [**angegebenen SYSTEMTIME-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) Sie können dieses Makro verwenden oder die [**MESSAGE-Nachricht VOM NACHRICHTENDIENST \_ GETSYSTEMTIME**](dtm-getsystemtime.md) explizit senden. <br/> |
| [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)                         | Legt die Anzeige eines DTP-Steuerelements (Date and Time Picker) basierend auf einer angegebenen Formatzeichenfolge fest. Sie können dieses Makro verwenden oder die [**MELDUNG VOM \_ SETFORMAT**](dtm-setformat.md) explizit senden. <br/>                                                                          |
| [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor)           | Legt die Farbe für einen bestimmten Teil des Monatskalenders innerhalb eines DTP-Steuerelements (Date and Time Picker) fest. Sie können dieses Makro verwenden oder die [**MELDUNG \_ SETMCCOLOR**](dtm-setmccolor.md) explizit senden. <br/>                                                           |
| [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)             | Legt die Schriftart fest, die vom untergeordneten Monatskalender-Steuerelement des DTP-Steuerelements (Datums- und Uhrzeitauswahl) verwendet werden soll. Sie können dieses Makro verwenden oder explizit die [**MELDUNG VOM \_ SETMCFONT senden.**](dtm-setmcfont.md) <br/>                                                                |
| [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)           | Legt das Format für ein angegebenes DTP-Steuerelement fest. Verwenden Sie dieses Makro, oder senden Sie [**die FEHLERMELDUNG \_ SETMCSTYLE-Nachricht**](dtm-setmcstyle.md) explizit.<br/>                                                                                                                              |
| [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange)                           | Legt die minimalen und maximalen zulässigen Systemzeiten für ein Datums- und Uhrzeitauswahl-Steuerelement (DTP) fest. Sie können dieses Makro verwenden oder die [**MELDUNG \_ SETRANGE explizit**](dtm-setrange.md) senden. <br/>                                                                       |
| [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)                 | Legt ein Datums- und Uhrzeitauswahl-Steuerelement (DTP) auf ein bestimmtes Datum und eine bestimmte Uhrzeit fest. Sie können dieses Makro verwenden oder die [**MESSAGE-Nachricht FÜR DIE \_ SETSYSTEMTIME explizit**](dtm-setsystemtime.md) senden. <br/>                                                                                       |



 

### <a name="messages"></a>Meldungen



| Thema                                                           | Inhalte                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_SCHLIEßENMONTHCAL**](dtm-closemonthcal.md)                 | Schließt ein DTP-Steuerelement. Senden Sie diese Nachricht explizit oder mithilfe des [**DateTime \_ CloseMonthCal-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)<br/>                                                                                                                                        |
| [**DG \_ GETDATETIMEPICKERINFO**](dtm-getdatetimepickerinfo.md) | Ruft Informationen zu einem DTP-Steuerelement (Date and Time Picker) ab.<br/>                                                                                                                                                                                                                  |
| [**DG \_ GETIDEALSIZE**](dtm-getidealsize.md)                   | Ruft die Größe ab, die zum Anzeigen des Steuerelements ohne Clipping erforderlich ist. Senden Sie diese Nachricht explizit oder mithilfe des [**DateTime \_ GetIdealSize-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)<br/>                                                                                                  |
| [**DG \_ GETMCCOLOR**](dtm-getmccolor.md)                       | Ruft die Farbe für einen bestimmten Teil des Monatskalenders innerhalb eines DTP-Steuerelements (Date and Time Picker) ab. Sie können diese Nachricht explizit senden oder das [**\_ DateTime-Makro GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) verwenden. <br/>                                              |
| [**WL \_ GETMCFONT**](dtm-getmcfont.md)                         | Ruft die Schriftart ab, die das untergeordnete Monatskalender-Steuerelement des DTP-Steuerelements (Date and Time Picker) derzeit verwendet. Sie können diese Nachricht explizit senden oder das [**\_ DateTime-Makro GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) verwenden. <br/>                                         |
| [**DG \_ GETMCSTYLE**](dtm-getmcstyle.md)                       | Ruft den Stil eines DTP-Steuerelements ab. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ DateTime-Makros GetMonthCalStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)<br/>                                                                                                                       |
| [**DG \_ GETMONTHCAL**](dtm-getmonthcal.md)                     | Ruft das Handle für das Untergeordnete Monatskalender-Steuerelement einer Datums- und Uhrzeitauswahl (DTP) ab. Sie können diese Nachricht explizit senden oder das [**DateTime \_ GetMonthCal-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) verwenden. <br/>                                                                              |
| [**RANGE \_ GETRANGE**](dtm-getrange.md)                           | Ruft die aktuellen minimalen und maximalen zulässigen Systemzeiten für ein Datums- und Uhrzeitauswahl-Steuerelement (DTP) ab. Sie können diese Nachricht explizit senden oder das [**DateTime \_ GetRange-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) verwenden. <br/>                                                              |
| [**DG \_ GETSYSTEMTIME**](dtm-getsystemtime.md)                 | Ruft die aktuell ausgewählte Uhrzeit aus einem DTP-Steuerelement (Date and Time Picker) ab und platziert sie in einer [**angegebenen SYSTEMTIME-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) Sie können diese Nachricht explizit senden oder das [**DateTime \_ GetSystemtime-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) verwenden. <br/> |
| [**DTS \_ SETFORMAT**](dtm-setformat.md)                         | Legt die Anzeige eines DTP-Steuerelements (Date and Time Picker) basierend auf einer angegebenen Formatzeichenfolge fest. Sie können diese Nachricht explizit senden oder das [**DateTime \_ SetFormat-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) verwenden. <br/>                                                                         |
| [**\_MCCOLOR**](dtm-setmccolor.md)                       | Legt die Farbe für einen bestimmten Teil des Monatskalenders innerhalb eines DTP-Steuerelements (Date and Time Picker) fest. Sie können diese Nachricht explizit senden oder das [**\_ DateTime-Makro SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) verwenden. <br/>                                              |
| [**\_TSETMCFONT**](dtm-setmcfont.md)                         | Legt die Schriftart fest, die vom untergeordneten Monatskalender-Steuerelement des DTP-Steuerelements (Datums- und Uhrzeitauswahl) verwendet werden soll. Sie können diese Nachricht explizit senden oder das [**\_ DateTime-Makro SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) verwenden.<br/>                                                    |
| [**\_MCSTYLE**](dtm-setmcstyle.md)                       | Legt den Stil eines DTP-Steuerelements fest. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ DateTime-Makros SetMonthCalStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)<br/>                                                                                                                       |
| [**RANGE \_ SETRANGE**](dtm-setrange.md)                           | Legt die minimalen und maximalen zulässigen Systemzeiten für ein DTP-Steuerelement (Date and Time Picker) fest. Sie können diese Nachricht explizit senden oder das [**DateTime \_ SetRange-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) verwenden. <br/>                                                                      |
| [**MF \_ SETSYSTEMTIME**](dtm-setsystemtime.md)                 | Legt die Uhrzeit in einem DTP-Steuerelement (Date and Time Picker) fest. Sie können diese Nachricht explizit senden oder das [**DateTime \_ SetSystemtime-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) verwenden. <br/>                                                                                                   |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                   | Inhalte                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DTN \_ CLOSEUP](dtn-closeup.md)                         | Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, wenn der Benutzer den Kalender des Dropdownmonats schließt. Der Monatskalender wird geschlossen, wenn der Benutzer ein Datum aus dem Monatskalender ausgibt oder auf den Dropdownpfeil klickt, während der Kalender geöffnet ist. <br/>                                                                                                      |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md)           | Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, wenn eine Änderung auftritt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                                                                                  |
| [\_DTN-DROPDOWNLISTE](dtn-dropdown.md)                       | Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, wenn der Benutzer den Kalender des Dropdownmonats aktiviert. <br/>                                                                                                                                                                                                                                               |
| [\_DTN-FORMAT](dtn-format.md)                           | Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, um anzufordern, dass Text in einem Rückruffeld angezeigt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                                                       |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)                 | Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, um die maximal zulässige Größe der Zeichenfolge abzurufen, die in einem Rückruffeld angezeigt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                           |
| [DTN \_ USERSTRING](dtn-userstring.md)                   | Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, wenn ein Benutzer die Bearbeitung einer Zeichenfolge im -Steuerelement beendet. Dieser Benachrichtigungscode wird nur von DTP-Steuerelementen gesendet, die auf den [**DTS \_ APPCANPARSE-Stil**](date-and-time-picker-control-styles.md) festgelegt sind. Diese Nachricht wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/> |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)                     | Wird von einem DTP-Steuerelement (Date and Time Picker) gesendet, wenn der Benutzer in ein Rückruffeld eingibt. Diese Nachricht wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                                                                             |
| [NM \_ KILLFOCUS (Datum/Uhrzeit)](nm-killfocus-date-time.md) | Benachrichtigt das übergeordnete Fenster eines Datums- und Uhrzeitauswahlsteuerelements, dass das Steuerelement den Eingabefokus verloren hat. [**NM \_ KILLFOCUS (Datum/Uhrzeit)**](nm-killfocus-date-time.md) wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                 |
| [NM \_ SETFOCUS (Datum/Uhrzeit)](nm-setfocus-date-time-.md)  | Benachrichtigt das übergeordnete Fenster eines Datums- und Uhrzeitauswahlsteuerelements, dass das Steuerelement den Eingabefokus erhalten hat. [NM \_ SETFOCUS (Datum/Uhrzeit)](nm-setfocus-date-time-.md) wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                  |



 

### <a name="structures"></a>Strukturen



| Thema                                                  | Inhalte                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATETIMEPICKERINFO**](/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo)       | Enthält Informationen zu einem DTP-Steuerelement. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange)           | Enthält Informationen zu einer Änderung, die in einem DTP-Steuerelement (Datums- und Uhrzeitauswahl) erfolgt ist. Diese Struktur wird mit dem [DTN \_ DATETIMECHANGE-Benachrichtigungscode](dtn-datetimechange.md) verwendet. <br/>                                                                                                                                                                                     |
| [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata)           | Enthält Informationen zu einem Teil der Formatzeichenfolge, der ein Rückruffeld innerhalb eines DTP-Steuerelements (Date and Time Picker) definiert. Sie enthält die Teilzeichenfolge, die das Rückruffeld definiert, und enthält einen Puffer zum Empfangen der Zeichenfolge, die im Rückruffeld angezeigt wird. Diese Struktur wird mit dem [DTN \_ FORMAT-Benachrichtigungscode](dtn-format.md) verwendet. <br/>               |
| [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) | Enthält Informationen zu einem DTP-Steuerelementrückruffeld (Date and Time Picker). Sie enthält eine Teilzeichenfolge (aus der Formatzeichenfolge des Steuerelements), die ein Rückruffeld definiert. Die -Struktur empfängt die maximal zulässige Größe des Texts, der im Rückruffeld angezeigt wird. Diese Struktur wird mit dem [DTN \_ FORMATQUERY-Benachrichtigungscode](dtn-formatquery.md) verwendet. <br/> |
| [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa)           | Enthält Spezifische Informationen zu einem Bearbeitungsvorgang, der in einem DTP-Steuerelement (Date and Time Picker) ausgeführt wurde. Diese Meldung wird mit dem [DTN USERSTRING-Benachrichtigungscode \_ ](dtn-userstring.md) verwendet. <br/>                                                                                                                                                                                |
| [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna)     | Enthält Informationen, die zum Beschreiben und Behandeln eines [DTN \_ WMKEYDOWN-Benachrichtigungscodes](dtn-wmkeydown.md) verwendet werden. <br/>                                                                                                                                                                                                                                                                               |



 

### <a name="constants"></a>Konstanten



| Thema                                                                          | Inhalte                                                                                |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Datums- und Uhrzeitauswahl-Steuerelementstile](date-and-time-picker-control-styles.md) | Die hier aufgeführten Fensterstile sind spezifisch für Steuerelemente der Datums- und Uhrzeitauswahl.<br/> |



 

 

