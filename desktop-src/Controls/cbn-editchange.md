---
title: CBN_EDITCHANGE Benachrichtigungscode (Winuser.h)
description: Wird gesendet, nachdem der Benutzer eine Aktion ausgeführt hat, die möglicherweise den Text im Bearbeitungssteuerelement eines Kombinationsfelds geändert hat.
ms.assetid: 2c5de5cd-24d3-4198-906e-b520369e0f61
keywords:
- CBN_EDITCHANGE Benachrichtigungscode Windows-Steuerelemente
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
ms.openlocfilehash: 0897c8e2de2417d304a1b8737a7358322a42073ec87442d75c21e954fa6ac805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054120"
---
# <a name="cbn_editchange-notification-code"></a>CBN \_ EDITCHANGE-Benachrichtigungscode

Wird gesendet, nachdem der Benutzer eine Aktion ausgeführt hat, die möglicherweise den Text im Bearbeitungssteuerelement eines Kombinationsfelds geändert hat. Im Gegensatz zum [CBN EDITUPDATE-Benachrichtigungscode \_ ](cbn-editupdate.md) wird dieser Benachrichtigungscode gesendet, nachdem das System den Bildschirm aktualisiert hat. Das übergeordnete Fenster des Kombinationsfelds empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
CBN_EDITCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelementbezeichner des Kombinationsfelds. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Kombinationsfeld.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn das Kombinationsfeld den [**\_ CBS-DROPDOWNLIST-Stil**](combo-box-styles.md) auflistet, wird dieser Benachrichtigungscode nicht gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[CBN \_ EDITUPDATE](cbn-editupdate.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

