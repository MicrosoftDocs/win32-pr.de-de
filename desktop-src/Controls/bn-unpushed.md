---
title: BN_UNPUSHED Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der pushzustand einer Schaltfläche auf nicht per Push übertragen festgelegt ist.
ms.assetid: 1ae7311d-f067-41fe-a117-e0c70d239e9d
keywords:
- Windows-Steuerelemente für BN_UNPUSHED Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_UNPUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eb8c16d8860274c070c31910254311a897c0f1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103127"
---
# <a name="bn_unpushed-notification-code"></a>BN- \_ Benachrichtigungs Code ohne pushübertragung

Wird gesendet, wenn der pushzustand einer Schaltfläche auf nicht per Push übertragen festgelegt ist.

> [!Note]  
> Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt. Anwendungen sollten für diese [**Aufgabe \_ den Schrift**](button-styles.md) Schnitt-Stil und die [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur des s verwenden.

 

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
BN_UNPUSHED

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

Der Wert von ' BN ' \_ ist mit dem [Milliarden- \_ unhilite](bn-unhilite.md) -Benachrichtigungs Code identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[BN per \_ pushübertragung](bn-pushed.md)
</dt> </dl>

 

