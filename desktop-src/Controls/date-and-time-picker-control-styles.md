---
title: Datums- und Uhrzeitauswahl-Steuerelementstile (CommCtrl.h)
description: Die hier aufgeführten Fensterstile sind spezifisch für Steuerelemente der Datums- und Uhrzeitauswahl.
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
ms.openlocfilehash: b6f9740e0de413649b67cc8231d31425d212d2571dbc9a1b703f9f95c35e4981
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085760"
---
# <a name="date-and-time-picker-control-styles"></a>Datums- und Uhrzeitauswahl-Steuerelementstile

Die hier aufgeführten Fensterstile sind spezifisch für Steuerelemente der Datums- und Uhrzeitauswahl.



| Konstante                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DTS_APPCANPARSE"></span><span id="dts_appcanparse"></span><dl> <dt>**DTS \_ APPCANPARSE**</dt> </dl>                                  | Ermöglicht es dem Besitzer, Benutzereingaben zu analysieren und die erforderlichen Maßnahmen zu ergreifen. Sie ermöglicht Es Benutzern, innerhalb des Clientbereichs des Steuerelements zu bearbeiten, wenn sie die F2-Taste drücken. Das Steuerelement sendet [DTN USERSTRING-Benachrichtigungscodes, \_ ](dtn-userstring.md) wenn Benutzer fertig sind.<br/>                                                                                                                                                                                                                                                                    |
| <span id="DTS_LONGDATEFORMAT"></span><span id="dts_longdateformat"></span><dl> <dt>**DTS \_ LONGDATEFORMAT**</dt> </dl>                         | Zeigt das Datum im langen Format an. Die Standardformatzeichenfolge für diesen Stil wird durch LOCALE \_ SLONGDATEFORMAT definiert, das eine Ausgabe wie "Friday, April 19, 1996" erzeugt. Wenn dieser Stil verwendet wird, wird auf der Dropdownschaltfläche kein Symbol angezeigt.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="DTS_RIGHTALIGN"></span><span id="dts_rightalign"></span><dl> <dt>**DTS \_ RIGHTALIGN**</dt> </dl>                                     | Der Dropdownmonatskalender wird mit dem Steuerelement rechtsbündig ausgerichtet und nicht linksbündig ausgerichtet, was der Standard ist. <br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHOWNONE"></span><span id="dts_shownone"></span><dl> <dt>**DTS \_ SHOWNONE**</dt> </dl>                                           | Es ist möglich, dass im Steuerelement derzeit kein Datum ausgewählt ist. Mit diesem Stil zeigt das Steuerelement ein Kontrollkästchen an, das automatisch ausgewählt wird, wenn ein Datum ausgewählt oder eingegeben wird. Wenn das Kontrollkästchen anschließend deaktiviert wird, kann die Anwendung das Datum nicht aus dem Steuerelement abrufen, da das Steuerelement im Wesentlichen über kein Datum verfügt. Der Status des Kontrollkästchens kann mit der [**MELDUNG "MF \_ SETSYSTEMTIME"**](dtm-setsystemtime.md) festgelegt oder mit der [**MELDUNG "MF \_ GETSYSTEMTIME"**](dtm-getsystemtime.md) abgefragt werden.<br/> |
| <span id="DTS_SHORTDATEFORMAT"></span><span id="dts_shortdateformat"></span><dl> <dt>**DTS \_ SHORTDATEFORMAT**</dt> </dl>                      | Zeigt das Datum im Kurzformat an. Die Standardformatzeichenfolge für diesen Stil wird durch LOCALE \_ SSHORTDATE definiert, das eine Ausgabe wie "4/19/96" erzeugt.<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHORTDATECENTURYFORMAT"></span><span id="dts_shortdatecenturyformat"></span><dl> <dt>**DTS \_ SHORTDATECENTURYFORMAT**</dt> </dl> | **Version 5.80.** Ähnlich wie beim **DTS \_ SHORTDATEFORMAT-Stil,** mit dem Unterschied, dass das Jahr ein vierstelliges Feld ist. Die Standardformatzeichenfolge für diesen Stil basiert auf LOCALE \_ SSHORTDATE. Die Ausgabe sieht wie folgt aus: "19.4.1996".<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="DTS_TIMEFORMAT"></span><span id="dts_timeformat"></span><dl> <dt>**DTS \_ TIMEFORMAT**</dt> </dl>                                     | Zeigt die Uhrzeit an. Die Standardformatzeichenfolge für diesen Stil wird durch LOCALE \_ STIMEFORMAT definiert, das eine Ausgabe wie "5:31:42 PM" erzeugt.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="DTS_UPDOWN"></span><span id="dts_updown"></span><dl> <dt>**DTS \_ UPDOWN**</dt> </dl>                                                 | Platziert ein Up-Down-Steuerelement rechts neben dem DTP-Steuerelement, um Datums-/Uhrzeitwerte zu ändern. Dieser Stil kann anstelle des Dropdown-Monatskalenders verwendet werden. Dies ist der Standardstil.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Hinweise

Die DTS \_ XXXFORMAT-Stile, die das Anzeigeformat definieren, können nicht kombiniert werden. Wenn keines der Formatformate geeignet ist, verwenden Sie eine [**** \_ SETFORMAT-Nachricht,**](dtm-setformat.md) um ein benutzerdefiniertes Format zu definieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





