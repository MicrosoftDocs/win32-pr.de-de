---
title: MCM_GETCURSEL Meldung (Commctrl.h)
description: Ruft das aktuell ausgewählte Datum ab. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ GetCurSel-Makros senden.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- MCM_GETCURSEL Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40ed6797cd7f40eb68e40a9eac90eb250badd461011e5490c0f4c8473571bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170207"
---
# <a name="mcm_getcursel-message"></a>MCM \_ GETCURSEL-Nachricht

Ruft das aktuell ausgewählte Datum ab. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ GetCurSel-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**SYSTEMTIME-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die die aktuell ausgewählten Datumsinformationen empfängt. Dieser Parameter muss eine gültige Adresse sein und darf nicht **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben. Diese Meldung schlägt immer fehl, wenn sie auf Monatskalendersteuerelemente angewendet wird, die auf den [**MCS \_ MULTISELECT-Stil**](month-calendar-control-styles.md) festgelegt sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uhrzeiten im Monatskalender-Steuerelement](month-calendar-controls.md)
</dt> </dl>

 

