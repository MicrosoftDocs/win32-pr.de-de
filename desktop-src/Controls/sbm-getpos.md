---
title: SBM_GETPOS Meldung (Winuser. h)
description: Die SBM- \_ GetPos-Nachricht wird gesendet, um die aktuelle Position des Bild Lauf Felds eines ScrollBar-Steuer Elements abzurufen.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- Windows-Steuerelemente für SBM_GETPOS Meldung
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956881"
---
# <a name="sbm_getpos-message"></a>SBM- \_ GetPos-Nachricht

Die **SBM- \_ GetPos** -Nachricht wird gesendet, um die aktuelle Position des Bild Lauf Felds eines ScrollBar-Steuer Elements abzurufen. Die aktuelle Position ist ein relativer Wert, der vom aktuellen scrollbereich abhängig ist. Wenn der scrollbereich z. b. zwischen 0 und 100 liegt und sich das Bild Lauf Feld in der Mitte des Balkens befindet, ist die aktuelle Position 50.

Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**getscrollpos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **getscrollpos** -Funktion ordnungsgemäß funktioniert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die aktuelle Position des Bild Lauf Felds auf der Bild Lauf Leiste.

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

[**SBM- \_ GetRange**](sbm-getrange.md)
</dt> <dt>

[**SBM- \_ SetPos**](sbm-setpos.md)
</dt> <dt>

[**SBM-über \_ Tragung**](sbm-setrange.md)
</dt> <dt>

[**SBM- \_ abzeichnende**](sbm-setrangeredraw.md)
</dt> </dl>

 

