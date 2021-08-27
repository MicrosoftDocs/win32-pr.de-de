---
title: MCM_GETSELRANGE-Nachricht (Commctrl.h)
description: Ruft Datumsinformationen ab, die die oberen und unteren Grenzwerte des vom Benutzer derzeit ausgewählten Datumsbereichs darstellen. Sie können diese Nachricht explizit oder mithilfe des \_ MonthCal GetSelRange-Makros senden.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- MCM_GETSELRANGE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7c446c98a43714a8cd839704050d2aedd1b7eab83b9199700ba24dd4e2be98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061950"
---
# <a name="mcm_getselrange-message"></a>MCM \_ GETSELRANGE-Nachricht

Ruft Datumsinformationen ab, die die oberen und unteren Grenzwerte des vom Benutzer derzeit ausgewählten Datumsbereichs darstellen. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ GetSelRange-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array mit zwei Elementen von [**SYSTEMTIME-Strukturen,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die die unteren und oberen Grenzen der Auswahl des Benutzers erhalten. Die unteren und oberen Grenzwerte werden in *lprgSysTimeArray* \[ 0 \] bzw. *lprgSysTimeArray* \[ 1 \] platziert. Dieser Parameter muss eine gültige Adresse sein und darf nicht **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben. **MCM \_ GETSELRANGE** schlägt fehl, wenn es auf ein Monatskalender-Steuerelement angewendet wird, das nicht den [**MCS \_ MULTISELECT-Stil**](month-calendar-control-styles.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Uhrzeiten im Monatskalender-Steuerelement](month-calendar-controls.md)
</dt> </dl>

 

