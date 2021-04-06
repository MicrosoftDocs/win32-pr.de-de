---
title: BN_DOUBLECLICKED Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- Windows-Steuerelemente für BN_DOUBLECLICKED Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018df4387b026d68e3f4e9a6c259fb19efd4a0f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858758"
---
# <a name="bn_doubleclicked-notification-code"></a>Milliarde- \_ Benachrichtigungs Code mit doppelten Klicks

Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt. Dieser Benachrichtigungs Code wird automatisch für die Schaltflächen " [**\_ Benutzer Schaltfläche**](button-styles.md)", " [**SB \_ RadioButton**](button-styles.md)" und " [**b \_**](button-styles.md) Bei anderen Schaltflächen Typen \_ wird nur der Typ "bn doublegeklickt" gesendet, wenn Sie über die Art der [**\_**](button-styles.md) "

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
BN_DOUBLECLICKED

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

Der Wert für "bn doublegeklickt" ist mit dem Datenbankadministrator- \_ Benachrichtigungs Code [ \_ ](bn-dblclk.md) identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

