---
title: MCM_HITTEST Meldung (kommstrg. h)
description: Bestimmt, welcher Teil eines Monatskalender-Steuer Elements sich an einem angegebenen Punkt auf dem Bildschirm befindet. Sie können diese Nachricht explizit oder mit dem monthcal- \_ HitTest-Makro senden.
ms.assetid: 51e74b07-4ed7-488d-ad5d-116f046577fc
keywords:
- Windows-Steuerelemente für MCM_HITTEST Meldung
topic_type:
- apiref
api_name:
- MCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3670ac8ab663ceda1786f7136a50c4da255a76c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740288"
---
# <a name="mcm_hittest-message"></a>MCM- \_ HitTest-Meldung

Bestimmt, welcher Teil eines Monatskalender-Steuer Elements sich an einem angegebenen Punkt auf dem Bildschirm befindet. Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) -Struktur. Beim Senden der Nachricht muss das **CBSIZE** -Element auf die Größe der **MCHITTESTINFO** -Struktur festgelegt werden, und **PT** muss auf den Punkt festgelegt werden, für den Sie einen Treffer Test durchsetzen möchten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Legt Werte in den Elementen des



| Rückgabecode                                                                                           | Beschreibung                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**mcht- \_ Kalender**</dt> </dl>         | Der angegebene Punkt lag innerhalb des Kalenders.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**mcht \_ calendarbk**</dt> </dl>       | Der angegebene Punkt befand sich im Hintergrund des Kalenders.<br/>                                                                                                                                                                                                              |
| <dl> <dt>**mcht \_ calendardate**</dt> </dl>     | Der angegebene Punkt lag an einem bestimmten Datum innerhalb des Kalenders. Die [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur bei *LPARAM->St* wird auf das Datum am angegebenen Punkt festgelegt.<br/>                                                                                    |
| <dl> <dt>**mcht \_ calendardatenext**</dt> </dl> | Der angegebene Punkt befand sich über einem Datum des nächsten Monats (teilweise am Ende des derzeit angezeigten Monats angezeigt). Wenn der Benutzer darauf klickt, wird der Monatskalender durch einen Bildlauf zum nächsten Monat oder Satz von Monaten angezeigt.<br/>                                 |
| <dl> <dt>**mcht \_ calendardateprev**</dt> </dl> | Der angegebene Punkt befand sich über einem Datum des vorherigen Monats (teilweise am Ende des derzeit angezeigten Monats angezeigt). Wenn der Benutzer auf diese Schaltfläche klickt, wird die Anzeige des Monats Kalenders auf den vorhergehenden Monat oder die Monats Gruppe zurückgesetzt.<br/>                         |
| <dl> <dt>**mcht \_ CalendarDay**</dt> </dl>      | Der angegebene Punkt war über eine Tages Abkürzung (z. b. "Fri"). Die [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur bei *LPARAM->St* wird auf das entsprechende Datum in der obersten Zeile festgelegt.<br/>                                                                      |
| <dl> <dt>**mcht \_ calendarweeknum**</dt> </dl>  | Der angegebene Punkt lag über einer Wochenzahl (nur [**MCS \_ weeknumbers**](month-calendar-control-styles.md) Style). Die [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur bei *LPARAM->St* wird auf das entsprechende Datum in der äußersten linken Spalte festgelegt.<br/> |
| <dl> <dt>**Nächstes mcht \_**</dt> </dl>             | Der angegebene Punkt befindet sich in einem Bereich, der bewirkt, dass der Monatskalender einen Bildlauf zum nächsten Monat oder Satz von Monaten durchführt. Dieses Flag wird verwendet, um andere Treffer testflags zu ändern.<br/>                                                                                   |
| <dl> <dt>**nicht im \_ nirgendwo**</dt> </dl>          | Der angegebene Punkt befand sich nicht im Monatskalender-Steuerelement oder befand sich in einem inaktiven Teil des Steuer Elements.<br/>                                                                                                                                                        |
| <dl> <dt>**mcht- \_ Prev**</dt> </dl>             | Der angegebene Punkt befindet sich in einem Bereich, der bewirkt, dass der Monatskalender einen Bildlauf zum vorherigen Monat oder Satz von Monaten durchführt. Dieses Flag wird verwendet, um andere Treffer testflags zu ändern.<br/>                                                                               |
| <dl> <dt>**mcht- \_ Titel**</dt> </dl>            | Der angegebene Punkt lag über dem Titel eines Monats.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**mcht \_ titlebk**</dt> </dl>          | Der angegebene Punkt befand sich im Hintergrund des Titels eines Monats.<br/>                                                                                                                                                                                                    |
| <dl> <dt>**mcht \_ titlebtnnext**</dt> </dl>     | Der angegebene Punkt befand sich über der Schaltfläche in der oberen rechten Ecke des Steuer Elements. Wenn der Benutzer darauf klickt, wird der Monatskalender durch einen Bildlauf zum nächsten Monat oder Satz von Monaten angezeigt. <br/>                                                                           |
| <dl> <dt>**mcht \_ titlebtnprev**</dt> </dl>     | Der angegebene Punkt befand sich über der Schaltfläche in der oberen linken Ecke des Steuer Elements. Wenn der Benutzer auf diese Schaltfläche klickt, wird die Anzeige des Monats Kalenders auf den vorhergehenden Monat oder die Monats Gruppe zurückgesetzt. <br/>                                                                        |
| <dl> <dt>**mcht- \_ titlemonth**</dt> </dl>       | Der angegebene Punkt befand sich in der Titelleiste eines Monats über einen Monatsnamen.<br/>                                                                                                                                                                                                 |
| <dl> <dt>**mcht \_ titleyear**</dt> </dl>        | Der angegebene Punkt lag in der Titelleiste eines Monats über dem Jahreswert.<br/>                                                                                                                                                                                               |
| <dl> <dt>**mcht- \_ Verbindungs Link**</dt> </dl>        | Der angegebene Punkt befand sich am unteren Rand des Monatskalender-Steuer Elements auf dem Link "heute".<br/> Der **uhit** -Member der [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) -Struktur bei *LPARAM* entspricht dem Rückgabewert. <br/>                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

