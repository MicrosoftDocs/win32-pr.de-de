---
title: SBM_SETRANGEREDRAW Meldung (Winuser. h)
description: Eine Anwendung sendet die SBM \_ setrangeredraw-Nachricht an ein ScrollBar-Steuerelement, um die minimalen und maximalen Positionswerte festzulegen und das Steuerelement neu zu zeichnen.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- Windows-Steuerelemente für SBM_SETRANGEREDRAW Meldung
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040090"
---
# <a name="sbm_setrangeredraw-message"></a>SBM- \_ Nachricht "abzeichnet"

Eine Anwendung sendet die **SBM \_ setrangeredraw** -Nachricht an ein ScrollBar-Steuerelement, um die minimalen und maximalen Positionswerte festzulegen und das Steuerelement neu zu zeichnen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die minimale Bild Lauf Position an.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die maximale Scrollposition an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**ComCtl32.dll Version 5,0**: Wenn sich die Position des Bild Lauf Felds geändert hat, ist der Rückgabewert die vorherige Position des Bild Lauf Felds. Andernfalls ist der Wert 0 (null).

**ComCtl32.dll Version 6,0**: die aktuelle Position des Bild Lauf Felds, unabhängig davon, ob es geändert wurde.

## <a name="remarks"></a>Bemerkungen

Die standardmäßigen und maximalen Positionswerte sind 0 (null). Der Unterschied zwischen den Werten, die von den *wParam* -und *LPARAM* -Parametern angegeben werden, darf nicht größer sein als MAXLONG.

Wenn die minimalen und maximalen Positionswerte gleich sind, wird das Bild Lauf leisten-Steuerelement ausgeblendet und deaktiviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**SBM- \_ GetPos**](sbm-getpos.md)
</dt> <dt>

[**SBM- \_ GetRange**](sbm-getrange.md)
</dt> <dt>

[**SBM- \_ SetPos**](sbm-setpos.md)
</dt> <dt>

[**SBM-über \_ Tragung**](sbm-setrange.md)
</dt> </dl>

 

 





