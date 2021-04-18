---
title: Steuerelement Stile für Datums-und Zeitauswahl (kommctrl. h)
description: Die hier aufgeführten Fenster Stile sind spezifisch für Steuerelemente für Datums-und Zeitauswahl.
ms.assetid: d3b95521-75ef-4cca-b801-94c6f749aa47
topic_type:
- apiref
api_name:
- DTS_APPCANPARSE
- DTS_LONGDATEFORMAT
- DTS_RIGHTALIGN
- DTS_SHOWNONE
- DTS_SHORTDATEFORMAT
- DTS_SHORTDATECENTURYFORMAT
- DTS_TIMEFORMAT
- DTS_UPDOWN
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d24e7543e4e843fc70e0ccacdab670e18e46cf3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364671"
---
# <a name="date-and-time-picker-control-styles"></a>Steuerelement Stile für Datums-und Zeitauswahl

Die hier aufgeführten Fenster Stile sind spezifisch für Steuerelemente für Datums-und Zeitauswahl.



| Konstante                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DTS_APPCANPARSE"></span><span id="dts_appcanparse"></span><dl> <dt>**DTS \_ appcananalyse**</dt> </dl>                                  | Ermöglicht dem Besitzer, Benutzereingaben zu analysieren und erforderliche Maßnahmen zu ergreifen. Dadurch können Benutzer im Client Bereich des Steuer Elements bearbeiten, wenn Sie die F2-Taste drücken. Das-Steuerelement sendet [Dtn \_ UserString](dtn-userstring.md) -Benachrichtigungs Codes, wenn Benutzer abgeschlossen sind.<br/>                                                                                                                                                                                                                                                                    |
| <span id="DTS_LONGDATEFORMAT"></span><span id="dts_longdateformat"></span><dl> <dt>**DTS \_ longdateformat**</dt> </dl>                         | Zeigt das Datum im langen Format an. Die Standardformat Zeichenfolge für diesen Stil wird durch das locale \_ slongdateformat definiert, das eine Ausgabe wie "Friday, 19. April 1996" erzeugt. Wenn dieser Stil verwendet wird, wird auf der Dropdown-Schaltfläche kein Symbol angezeigt.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="DTS_RIGHTALIGN"></span><span id="dts_rightalign"></span><dl> <dt>**DTS- \_ RightAlign**</dt> </dl>                                     | Der Dropdown-Monatskalender wird rechtsbündig mit dem Steuerelement ausgerichtet, anstatt linksbündig ausgerichtet zu sein. Dies ist die Standardeinstellung. <br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHOWNONE"></span><span id="dts_shownone"></span><dl> <dt>**DTS- \_ Show None**</dt> </dl>                                           | Es ist möglich, dass im-Steuerelement momentan kein Datum ausgewählt ist. Bei diesem Stil zeigt das Steuerelement ein Kontrollkästchen an, das automatisch ausgewählt wird, wenn ein Datum ausgewählt oder eingegeben wird. Wenn das Kontrollkästchen anschließend deaktiviert wird, kann die Anwendung das Datum nicht aus dem Steuerelement abrufen, da das Steuerelement im Grunde kein Datum hat. Der Status des Kontrollkästchens kann mit der [**DTM- \_ SetSystemTime**](dtm-setsystemtime.md) -Nachricht festgelegt oder mit der [**DTM \_ GetSystemTime**](dtm-getsystemtime.md) -Nachricht abgefragt werden.<br/> |
| <span id="DTS_SHORTDATEFORMAT"></span><span id="dts_shortdateformat"></span><dl> <dt>**DTS- \_ shortdateformat**</dt> </dl>                      | Zeigt das Datum in Kurzform an. Die Standardformat Zeichenfolge für diesen Stil wird durch das locale \_ sshortdate definiert, das eine Ausgabe wie "4/19/96" erzeugt.<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHORTDATECENTURYFORMAT"></span><span id="dts_shortdatecenturyformat"></span><dl> <dt>**DTS \_ shortdatecenturyformat**</dt> </dl> | **Version 5,80.** Vergleichbar mit dem **DTS \_ shortdateformat** -Stil, mit dem Unterschied, dass year ein vierstelliges Feld ist. Die Standardformat Zeichenfolge für diesen Stil basiert auf dem \_ Gebiets Schema sshortdate. Die Ausgabe sieht wie folgt aus: "4/19/1996".<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="DTS_TIMEFORMAT"></span><span id="dts_timeformat"></span><dl> <dt>**DTS- \_ Zeitformat**</dt> </dl>                                     | Zeigt die Uhrzeit an. Die Standardformat Zeichenfolge für diesen Stil wird durch locale \_ stimeformat definiert, das eine Ausgabe wie "5:31:42 pm" erzeugt.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="DTS_UPDOWN"></span><span id="dts_updown"></span><dl> <dt>**DTS- \_ UpDown**</dt> </dl>                                                 | Platziert ein auf-ab-Steuerelement auf der rechten Seite des DTP-Steuer Elements, um Datums-/Uhrzeitwerte zu ändern. Dieser Stil kann anstelle des Dropdown-Monats Kalenders verwendet werden. Dies ist der Standardstil.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Bemerkungen

Die DTS- \_ xxxformat-Stile, die das Anzeige Format definieren, können nicht kombiniert werden. Wenn keines der Format Stile geeignet ist, verwenden Sie eine [**DTM- \_ SetFormat**](dtm-setformat.md) -Meldung, um ein benutzerdefiniertes Format zu definieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





