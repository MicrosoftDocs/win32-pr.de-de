---
title: CBN_EDITCHANGE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, nachdem der Benutzer eine Aktion ausgeführt hat, die möglicherweise den Text im Bearbeitungs Steuerelement-Teil eines Kombinations Felds geändert hat.
ms.assetid: 2c5de5cd-24d3-4198-906e-b520369e0f61
keywords:
- Windows-Steuerelemente für CBN_EDITCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_EDITCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a661d647d0879b93675563777d77bba2dfe8c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346536"
---
# <a name="cbn_editchange-notification-code"></a>CBN- \_ EditChange-Benachrichtigungs Code

Wird gesendet, nachdem der Benutzer eine Aktion ausgeführt hat, die möglicherweise den Text im Bearbeitungs Steuerelement-Teil eines Kombinations Felds geändert hat. Im Gegensatz zum [CBN- \_ editupdate](cbn-editupdate.md) -Benachrichtigungs Code wird dieser Benachrichtigungs Code gesendet, nachdem das System den Bildschirm aktualisiert hat. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
CBN_EDITCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Kombinations Feld.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das Kombinations Feld den " [**CBS \_ DropDownList**](combo-box-styles.md) "-Stil hat, wird dieser Benachrichtigungs Code nicht gesendet.

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

[CBN- \_ editupdate](cbn-editupdate.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

