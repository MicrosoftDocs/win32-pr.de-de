---
title: PBM_SETRANGE Meldung (kommstrg. h)
description: Legt den minimalen und maximalen Wert für eine Statusanzeige fest und zeichnet den Balken neu, um den neuen Bereich widerzuspiegeln.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- Windows-Steuerelemente für PBM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859072"
---
# <a name="pbm_setrange-message"></a>PBM- \_ Nachricht

Legt den minimalen und maximalen Wert für eine Statusanzeige fest und zeichnet den Balken neu, um den neuen Bereich widerzuspiegeln.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den minimalen Bereichs Wert an, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den maximalen Bereichs Wert an. Der minimale Bereichs Wert darf nicht negativ sein. Standardmäßig ist der Minimalwert 0 (null). Der maximale Bereichs Wert muss größer als der minimale Bereichs Wert sein. Der maximale Bereichs Wert ist standardmäßig 100.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherigen Bereichs Werte zurück, wenn erfolgreich, andernfalls 0 (null). Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den vorherigen Minimalwert an, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den vorherigen maximalen Wert an.

## <a name="remarks"></a>Bemerkungen

Wenn Sie die Bereichs Werte nicht festlegen, legt das System den Minimalwert auf 0 und den maximalen Wert auf 100 fest. Da diese Nachricht den Bereich als 16-Bit-Ganzzahl ohne Vorzeichen drückt, kann Sie von 0 bis 65.535 erweitert werden. Der Minimalwert im Bereich kann zwischen 0 und 65.535 liegen. Ebenso kann der Höchstwert zwischen 0 und 65.535 liegen.

Um einen größeren Bereich festzulegen, nennen Sie [**PBM \_ SETRANGE32**](pbm-setrange32.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**PBM- \_ GetRange**](pbm-getrange.md)
</dt> <dt>

[**PBM \_ SETRANGE32**](pbm-setrange32.md)
</dt> </dl>

 

