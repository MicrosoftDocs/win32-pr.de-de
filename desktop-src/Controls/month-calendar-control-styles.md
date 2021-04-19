---
title: Monatskalender-Steuerelement Stile (kommctrl. h)
description: Die folgenden Stil Konstanten werden verwendet, wenn Sie Monatskalender-Steuerelemente erstellen.
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
ms.openlocfilehash: 45ccef4a3cc8e16851c0676b8b0dce8c53cfdd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360401"
---
# <a name="month-calendar-control-styles"></a>Monatskalender-Steuerelement Stile

Die folgenden Stil Konstanten werden verwendet, wenn Sie Monatskalender-Steuerelemente erstellen.



| Konstante                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <dt>**MCS \_ daystate**</dt> </dl>                         | [Version 4,70](common-control-versions.md). Der Monatskalender sendet [MCN \_ getdaystate](mcn-getdaystate.md) -Benachrichtigungen, um Informationen darüber anzufordern, welche Tage fett angezeigt werden sollen.<br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <dt>**MCS- \_ Mehrfachauswahl**</dt> </dl>                | [Version 4,70](common-control-versions.md). Der Monatskalender ermöglicht dem Benutzer die Auswahl eines Datums Bereichs innerhalb des-Steuer Elements. Standardmäßig beträgt der maximale Bereich eine Woche. Sie können den maximalen Bereich, der ausgewählt werden kann, mithilfe der [**MCM \_ setmaxselcount**](mcm-setmaxselcount.md) -Nachricht ändern. <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <dt>**MCS- \_ Wochen Nummern**</dt> </dl>                | [Version 4,70](common-control-versions.md). Das Monatskalender-Steuerelement zeigt die Wochen Nummern (1-52) links neben den Zeilen der Tage an. Woche 1 wird als erste Woche definiert, die mindestens vier Tage umfasst. <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <dt>**MCS \_ noumdaycircle**</dt> </dl>          | [Version 4,70](common-control-versions.md). Das Month Calendar-Steuerelement Zirkel nicht das heutige Datum. <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <dt>**MCS \_ notoday**</dt> </dl>                            | [Version 4,70](common-control-versions.md). Im Monatskalender-Steuerelement wird nicht das heutige Datum am unteren Rand des Steuer Elements angezeigt. <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <dt>**MCS \_ notrailingdates**</dt> </dl>    | **Windows Vista.** Datumsangaben aus dem vorherigen und den nächsten Monaten werden im Kalender des aktuellen Monats nicht angezeigt.<br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <dt>**MCS \_ shortdaysofweek**</dt> </dl>    | **Windows Vista.** Kurztagnamen werden in der Kopfzeile angezeigt.<br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <dt>**MCS \_ noselchangeonnav**</dt> </dl> | **Windows Vista.** Die Auswahl wird nicht geändert, wenn der Benutzer im Kalender auf "Next" oder "Previous" navigiert. Dadurch kann der Benutzer einen Bereich auswählen, der größer als sichtbar ist.<br/>                                                                                                                                  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





