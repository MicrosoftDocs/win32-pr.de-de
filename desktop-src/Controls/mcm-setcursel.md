---
title: MCM_SETCURSEL (Commctrl.h)
description: Legt das aktuell ausgewählte Datum für ein Monatskalender-Steuerelement fest. Wenn das angegebene Datum nicht angezeigt wird, aktualisiert das Steuerelement die Anzeige, um sie anzuzeigen. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ SetCurSel-Makros senden.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- MCM_SETCURSEL message Windows Controls
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63238f11f93e56c18e1897fcdd3cb96977f23fe16bde19123b5c063f99c0ff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061890"
---
# <a name="mcm_setcursel-message"></a>MCM \_ SETCURSEL-Nachricht

Legt das aktuell ausgewählte Datum für ein Monatskalender-Steuerelement fest. Wenn das angegebene Datum nicht angezeigt wird, aktualisiert das Steuerelement die Anzeige, um sie anzuzeigen. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ SetCurSel-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**SYSTEMTIME-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die das Datum enthält, das als aktuelle Auswahl festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück. Diese Meldung wird nicht angezeigt, wenn sie auf ein Monatskalender-Steuerelement angewendet wird, das den [**MCS \_ MULTISELECT-Stil**](month-calendar-control-styles.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zeiten im Monatskalender-Steuerelement](month-calendar-controls.md)
</dt> </dl>

 

