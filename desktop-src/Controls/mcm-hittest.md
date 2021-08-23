---
title: MCM_HITTEST Nachricht (Commctrl.h)
description: Bestimmt, welcher Teil eines Monatskalender-Steuerelements sich an einem bestimmten Punkt auf dem Bildschirm befindet. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ HitTest-Makros senden.
ms.assetid: 51e74b07-4ed7-488d-ad5d-116f046577fc
keywords:
- MCM_HITTEST Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 3ab43ae76a2e747ff019a5bafa32870a208851a143ad94dd0679e894366c3592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697190"
---
# <a name="mcm_hittest-message"></a>MCM \_ HITTEST-Nachricht

Bestimmt, welcher Teil eines Monatskalender-Steuerelements sich an einem bestimmten Punkt auf dem Bildschirm befindet. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ HitTest-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**MCHITTESTINFO-Struktur.**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) Beim Senden der Nachricht muss der **cbSize-Member** auf die Größe der **MCHITTESTINFO-Struktur** und **pt** auf den Punkt festgelegt werden, an dem Sie den Treffertest erreichen möchten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Legt Werte in Membern von fest.



| Rückgabecode                                                                                           | Beschreibung                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MCHT \_ CALENDAR**</dt> </dl>         | Der angegebene Punkt befand sich innerhalb des Kalenders.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**MCHT \_ CALENDARBK**</dt> </dl>       | Der angegebene Punkt befand sich im Hintergrund des Kalenders.<br/>                                                                                                                                                                                                              |
| <dl> <dt>**MCHT \_ CALENDARDATE**</dt> </dl>     | Der angegebene Punkt befand sich an einem bestimmten Datum innerhalb des Kalenders. Die [**SYSTEMTIME-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) bei *lParam->st* wird auf das Datum am angegebenen Punkt festgelegt.<br/>                                                                                    |
| <dl> <dt>**MCHT \_ CALENDARDATENEXT**</dt> </dl> | Der angegebene Punkt befand sich über einem Datum des nächsten Monats (teilweise am Ende des aktuell angezeigten Monats angezeigt). Wenn der Benutzer hier klickt, führt der Monatskalender einen Bildlauf bis zum nächsten Monat oder einer Gruppe von Monaten durch.<br/>                                 |
| <dl> <dt>**MCHT \_ CALENDARDATEPREV**</dt> </dl> | Der angegebene Punkt lag über einem Datum aus dem vorigen Monat (teilweise am Ende des aktuell angezeigten Monats angezeigt). Wenn der Benutzer hier klickt, führt der Monatskalender einen Bildlauf bis zum vorherigen Monat oder einer Gruppe von Monaten durch.<br/>                         |
| <dl> <dt>**MCHT \_ CALENDARDAY**</dt> </dl>      | Der angegebene Punkt befand sich über einer Abkürzung für einen Tag ("z.B. Fr"). Die [**SYSTEMTIME-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) bei *lParam->st* wird auf das entsprechende Datum in der obersten Zeile festgelegt.<br/>                                                                      |
| <dl> <dt>**MCHT \_ CALENDARWEEKNUM**</dt> </dl>  | Der angegebene Punkt lag über einer Wochennummer (nur [**IM MCS \_ WEEKNUMBERS-Format).**](month-calendar-control-styles.md) Die [**SYSTEMTIME-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) bei *lParam->st* wird auf das entsprechende Datum in der spalte ganz links festgelegt.<br/> |
| <dl> <dt>**MCHT \_ NEXT**</dt> </dl>             | Der angegebene Punkt befindet sich in einem Bereich, der bewirkt, dass der Monatskalender in seiner Anzeige zum nächsten Monat oder einer Gruppe von Monaten scrollt. Dieses Flag wird verwendet, um andere Treffertestflags zu ändern.<br/>                                                                                   |
| <dl> <dt>**\_MCHT-HEITER**</dt> </dl>          | Der angegebene Punkt befand sich nicht im Monatskalender-Steuerelement oder in einem inaktiven Teil des Steuerelements.<br/>                                                                                                                                                        |
| <dl> <dt>**MCHT \_ PREV**</dt> </dl>             | Der angegebene Punkt befindet sich in einem Bereich, der bewirkt, dass der Monatskalender in seiner Anzeige zum vorherigen Monat oder einer Gruppe von Monaten scrollt. Dieses Flag wird verwendet, um andere Treffertestflags zu ändern.<br/>                                                                               |
| <dl> <dt>**MCHT \_ TITLE**</dt> </dl>            | Der angegebene Punkt lag über dem Titel eines Monats.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**MCHT \_ TITLEBK**</dt> </dl>          | Der angegebene Punkt befand sich über dem Hintergrund des Titels eines Monats.<br/>                                                                                                                                                                                                    |
| <dl> <dt>**MCHT \_ TITLEBTNNEXT**</dt> </dl>     | Der angegebene Punkt befand sich über der Schaltfläche in der oberen rechten Ecke des Steuerelements. Wenn der Benutzer hier klickt, führt der Monatskalender einen Bildlauf bis zum nächsten Monat oder einer Gruppe von Monaten durch. <br/>                                                                           |
| <dl> <dt>**MCHT \_ TITLEBTNPREV**</dt> </dl>     | Der angegebene Punkt befand sich über der Schaltfläche in der oberen linken Ecke des Steuerelements. Wenn der Benutzer hier klickt, führt der Monatskalender einen Bildlauf bis zum vorherigen Monat oder einer Gruppe von Monaten durch. <br/>                                                                        |
| <dl> <dt>**MCHT \_ TITLEMONTH**</dt> </dl>       | Der angegebene Punkt befand sich in der Titelleiste eines Monats über einem Monatsnamen.<br/>                                                                                                                                                                                                 |
| <dl> <dt>**MCHT \_ TITLEYEAR**</dt> </dl>        | Der angegebene Punkt befand sich in der Titelleiste eines Monats über dem Jahreswert.<br/>                                                                                                                                                                                               |
| <dl> <dt>**MCHT \_ TODAYLINK**</dt> </dl>        | Der angegebene Punkt befand sich auf dem Link "today" am unteren Rand des Monatskalender-Steuerelements.<br/> Der **uHit-Member** der [**MCHITTESTINFO-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) bei *lParam* entspricht dem Rückgabewert. <br/>                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

