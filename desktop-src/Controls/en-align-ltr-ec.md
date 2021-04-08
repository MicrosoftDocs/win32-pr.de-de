---
title: EN_ALIGN_LTR_EC Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer die Richtung des Bearbeitungs Steuer Elements in von links nach rechts geändert hat. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM- \_ Befehls Meldung.
ms.assetid: 231f9d00-c5a5-445e-9176-201fe1c14a0e
keywords:
- Windows-Steuerelemente für EN_ALIGN_LTR_EC Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_ALIGN_LTR_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4886c68a024005c4b2fddd71e1480b0a3545bdf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740992"
---
# <a name="en_align_ltr_ec-notification-code"></a>EN \_ Ausrichten des \_ Ltr- \_ EC-Benachrichtigungs Codes

Wird gesendet, wenn der Benutzer die Richtung des Bearbeitungs Steuer Elements in von links nach rechts geändert hat. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
EN_ALIGN_LTR_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungs Steuer Elements. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Bearbeitungs Steuerelement, das den Benachrichtigungs Code sendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn eine bidirektionale Sprache auf dem System installiert ist (z. b. Arabisch oder Hebräisch), können Sie die Bearbeitungs Steuerelement-Richtung mithilfe von STRG + LShift (von links nach rechts) und STRG + rshift (von rechts nach links) ändern.

Umfassende **Bearbeitung:** Dieser Benachrichtigungs Code wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

