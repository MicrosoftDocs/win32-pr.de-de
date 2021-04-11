---
title: BN_DBLCLK Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- Windows-Steuerelemente für BN_DBLCLK Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04c6bf52e213056d85d3a6d038bedb83754a27e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040373"
---
# <a name="bn_dblclk-notification-code"></a>Mrd. \_ dblclk-Benachrichtigungs Code

Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt. Dieser Benachrichtigungs Code wird automatisch für die Schaltflächen " [**\_ Benutzer Schaltfläche**](button-styles.md)", " [**SB \_ RadioButton**](button-styles.md)" und " [**b \_**](button-styles.md) Andere Schaltflächen Typen senden \_ nur dann eine Milliarde dblclk, wenn Sie über das Format "Schriftarten [**\_ Benachrichtigen**](button-styles.md) " verfügen

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für die Schaltfläche.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der BN- \_ dblclk-Wert ist identisch mit dem über die [Milliarde \_ doublegeklickt](bn-doubleclicked.md) -Benachrichtigungs Code.

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

[auf BN \_ geklickt](bn-clicked.md)
</dt> <dt>

[BN- \_ Doppelklick](bn-doubleclicked.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

