---
title: MCM_SETDAYSTATE Meldung (kommstrg. h)
description: Legt die Tages Zustände für alle Monate fest, die gegenwärtig innerhalb eines Monatskalender-Steuer Elements sichtbar sind. Sie können diese Nachricht explizit oder mit dem monthcal \_ SetDayState-Makro senden.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- Windows-Steuerelemente für MCM_SETDAYSTATE Meldung
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478957"
---
# <a name="mcm_setdaystate-message"></a>MCM \_ SetDayState-Meldung

Legt die Tages Zustände für alle Monate fest, die gegenwärtig innerhalb eines Monatskalender-Steuer Elements sichtbar sind. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert, der angibt, wie viele Elemente im Array sind, auf das *LPARAM* zeigt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array von [**MONTHDAYSTATE**](monthdaystate.md) -Werten, die definieren, wie das Monatskalender-Steuerelement jeden Tag in der Anzeige zeichnen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann die Tages Zustandsinformationen explizit festlegen, indem diese Nachricht gesendet wird. der Zustand wird jedoch nicht beibehalten, wenn ein anderer Teil des Kalenders in der Ansicht angezeigt wird. Die Tages Zustandsinformationen werden in der Regel als Reaktion auf den [MCN \_ getdaystate](mcn-getdaystate.md) -Benachrichtigungs Code festgelegt, der immer dann gesendet wird, wenn das Steuerelement aktualisiert werden muss.

Das Array bei *LPARAM* muss so viele Elemente enthalten wie der Wert, der vom folgenden Makro zurückgegeben wird:

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

Beachten Sie, dass das Array bei *LPARAM* die [**MONTHDAYSTATE**](monthdaystate.md) -Werte enthalten muss, die mit allen Monaten übereinstimmen, die sich derzeit in der Anzeige des Steuer Elements in chronologischer Reihenfolge befinden. Dies schließt die zwei Monate ein, die möglicherweise vor dem ersten Monat und nach dem letzten Monat teilweise angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Monatskalender-Steuerelementen](using-month-calendar-controls.md)
</dt> </dl>

 

 





