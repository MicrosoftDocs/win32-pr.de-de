---
title: MCM_SETCURSEL Meldung (kommstrg. h)
description: Legt das aktuell ausgewählte Datum für ein Monatskalender-Steuerelement fest. Wenn das angegebene Datum nicht in der Ansicht enthalten ist, aktualisiert das Steuerelement die Anzeige, um es anzuzeigen. Sie können diese Nachricht explizit oder mit dem monthcal \_ setcurrsel-Makro senden.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- Windows-Steuerelemente für MCM_SETCURSEL Meldung
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
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346336"
---
# <a name="mcm_setcursel-message"></a>MCM- \_ setcurrsel-Meldung

Legt das aktuell ausgewählte Datum für ein Monatskalender-Steuerelement fest. Wenn das angegebene Datum nicht in der Ansicht enthalten ist, aktualisiert das Steuerelement die Anzeige, um es anzuzeigen. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ setcurrsel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die das Datum enthält, das als aktuelle Auswahl festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL. Diese Nachricht schlägt fehl, wenn Sie auf ein Monatskalender-Steuerelement angewendet wird, das das [**MCS- \_ MultiSelect**](month-calendar-control-styles.md) -Format verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uhrzeiten im Monatskalender-Steuerelement](month-calendar-controls.md)
</dt> </dl>

 

