---
title: MCM_GETSELRANGE Meldung (kommstrg. h)
description: Ruft Datumsinformationen ab, die die obere und untere Grenze des Datums Bereichs darstellen, der derzeit vom Benutzer ausgewählt wird. Sie können diese Nachricht explizit oder mit dem monthcal \_ getselrange-Makro senden.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- Windows-Steuerelemente für MCM_GETSELRANGE Meldung
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
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949701"
---
# <a name="mcm_getselrange-message"></a>MCM \_ getselrange-Nachricht

Ruft Datumsinformationen ab, die die obere und untere Grenze des Datums Bereichs darstellen, der derzeit vom Benutzer ausgewählt wird. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getselrange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein zwei-Element-Array von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen, das die unteren und oberen Grenzen der Auswahl des Benutzers empfängt. Die unteren und oberen Grenzwerte werden in *lprgsystimearray* \[ 0 \] bzw. *lprgsystimearray* \[ 1 platziert \] . Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL. **MCM \_ Getselrange** schlägt fehl, wenn es auf ein Monatskalender-Steuerelement angewendet wird, das den [**MCS- \_ MultiSelect**](month-calendar-control-styles.md) -Stil nicht verwendet.

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

 

