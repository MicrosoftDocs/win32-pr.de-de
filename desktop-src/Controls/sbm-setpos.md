---
title: SBM_SETPOS Meldung (Winuser. h)
description: Die SBM- \_ SetPos-Nachricht wird gesendet, um die Position des Bild Lauf Felds (Thumb) festzulegen, und, falls angefordert, die Schiebe Leiste neu gezeichnet, um die neue Position des Bild Lauf Felds widerzuspiegeln.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- Windows-Steuerelemente für SBM_SETPOS Meldung
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479155"
---
# <a name="sbm_setpos-message"></a>SBM- \_ SetPos-Nachricht

Die **SBM- \_ SetPos** -Nachricht wird gesendet, um die Position des Bild Lauf Felds (Thumb) festzulegen, und, falls angefordert, die Schiebe Leiste neu gezeichnet, um die neue Position des Bild Lauf Felds widerzuspiegeln.

Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **setscrollpos** -Funktion ordnungsgemäß funktioniert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die neue Position des Bild Lauf Felds an. Er muss innerhalb des scrollbereichs liegen. Wenn dieser Parameter außerhalb des scrollbereichs liegt, wird der Wert auf den nächstgelegenen gültigen Wert aufgerundet.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt an, ob die Schiebe Leiste neu gezeichnet werden soll, um die neue Position des Bild Lauf Felds widerzuspiegeln. Wenn dieser Parameter **true** ist, wird die Scrollleiste neu gezeichnet. Wenn der Wert **false** ist, wird die Scrollleiste nicht neu gezeichnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**ComCtl32.dll Version 5,0**: Wenn sich die Position des Bild Lauf Felds geändert hat, ist der Rückgabewert die vorherige Position des Bild Lauf Felds. Andernfalls ist der Wert 0 (null).

**ComCtl32.dll Version 6,0**: die aktuelle Position des Bild Lauf Felds, unabhängig davon, ob es geändert wurde.

## <a name="remarks"></a>Bemerkungen

Wenn das Schiebe leisten-Steuerelement durch einen nachfolgenden Rückruf einer anderen Funktion neu gezeichnet wird, ist das Festlegen des *LPARAM* -Parameters auf **false** nützlich.

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

[**SBM-über \_ Tragung**](sbm-setrange.md)
</dt> <dt>

[**SBM- \_ abzeichnende**](sbm-setrangeredraw.md)
</dt> </dl>

 

