---
title: Monatskalender-Steuerelementstile (CommCtrl.h)
description: Die folgenden Stilkonstanten werden beim Erstellen von Monatskalender-Steuerelementen verwendet.
ms.assetid: 8d9b2239-fd13-4579-81a2-0385fd318e83
topic_type:
- apiref
api_name:
- MCS_DAYSTATE
- MCS_MULTISELECT
- MCS_WEEKNUMBERS
- MCS_NOTODAYCIRCLE
- MCS_NOTODAY
- MCS_NOTRAILINGDATES
- MCS_SHORTDAYSOFWEEK
- MCS_NOSELCHANGEONNAV
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d236526792d4b965f58dc6c188add6a257845bcb8450e84f4b691849acb493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061850"
---
# <a name="month-calendar-control-styles"></a>Monatskalender-Steuerelementstile

Die folgenden Stilkonstanten werden beim Erstellen von Monatskalender-Steuerelementen verwendet.



| Konstante                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <dt>**MCS \_ DAYSTATE**</dt> </dl>                         | [Version 4.70.](common-control-versions.md) Der Monatskalender sendet [MCN \_ GETDAYSTATE-Benachrichtigungen,](mcn-getdaystate.md) um Informationen dazu anzufordern, welche Tage fett angezeigt werden sollen.<br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <dt>**MCS \_ MULTISELECT**</dt> </dl>                | [Version 4.70.](common-control-versions.md) Mit dem Monatskalender kann der Benutzer einen Datumsbereich innerhalb des Steuerelements auswählen. Standardmäßig beträgt der maximale Bereich eine Woche. Sie können den maximalen Bereich ändern, der mithilfe der [**MCM \_ SETMAXSELCOUNT-Nachricht**](mcm-setmaxselcount.md) ausgewählt werden kann. <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <dt>**MCS \_ WEEKNUMBERS**</dt> </dl>                | [Version 4.70.](common-control-versions.md) Das Monatskalender-Steuerelement zeigt Wochennummern (1-52) links von jeder Zeile von Tagen an. Woche 1 ist als die erste Woche definiert, die mindestens vier Tage enthält. <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <dt>**MCS \_ NOTCIRCLE**</dt> </dl>          | [Version 4.70.](common-control-versions.md) Das Monatskalender-Steuerelement umkreist nicht das Datum "heute". <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <dt>**MCS \_ NOT DANN**</dt> </dl>                            | [Version 4.70.](common-control-versions.md) Das Monatskalender-Steuerelement zeigt das Datum "heute" am unteren Rand des Steuerelements nicht an. <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <dt>**MCS \_ NOTRAILINGDATES**</dt> </dl>    | **Windows Vista.** Datumsangaben aus den vorherigen und nächsten Monaten werden im Kalender des aktuellen Monats nicht angezeigt.<br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <dt>**MCS \_ SHORTDAYSOFWEEK**</dt> </dl>    | **Windows Vista.** Kurze Tagesnamen werden im Header angezeigt.<br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <dt>**MCS \_ NOSELCHANGEONNAV**</dt> </dl> | **Windows Vista.** Die Auswahl wird nicht geändert, wenn der Benutzer im Kalender zum nächsten oder vorherigen Navigiert. Dadurch kann der Benutzer einen Bereich auswählen, der größer als sichtbar ist.<br/>                                                                                                                                  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





