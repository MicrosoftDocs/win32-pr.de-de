---
title: UDM_SETRANGE Meldung (kommstrg. h)
description: Legt die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement fest.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- Windows-Steuerelemente für UDM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040787"
---
# <a name="udm_setrange-message"></a>UDM- \_ Nachricht

Legt die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **kurzes** Element, das die maximale Position für das auf-ab-Steuerelement angibt, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **kurzes** Element, das die minimale Position angibt. Keine der Positionen kann größer als der UD \_ MaxVal-Wert oder kleiner als der UD \_ MinVal-Wert sein. Außerdem darf der Unterschied zwischen den beiden Positionen UD MaxVal nicht überschreiten \_ .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die maximale Position kann kleiner als die minimale Position sein. Durch Klicken auf die Schaltfläche mit dem Pfeil nach oben wird die aktuelle Position näher an die maximale Position verschoben, und durch Klicken auf die nach-unten-Taste wird die minimale Position

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Makelparam**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**UDM-über \_ Tragung**](udm-setrange.md)
</dt> </dl>

 

