---
title: BN_HILITE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer eine Schaltfläche auswählt.
ms.assetid: f20ba77e-257c-44ec-a2dd-dbf23cd78d07
keywords:
- Windows-Steuerelemente für BN_HILITE Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_HILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5567837c9883c52d99f0ca68d450f7b3538f233b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949599"
---
# <a name="bn_hilite-notification-code"></a>BN- \_ Hilite-Benachrichtigungs Code

Wird gesendet, wenn der Benutzer eine Schaltfläche auswählt.

> [!Note]  
> Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt. Anwendungen sollten für diese [**Aufgabe \_ den Schrift**](button-styles.md) Schnitt-Stil und die [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur des s verwenden.

 

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
BN_HILITE

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

Handle für die Schaltfläche.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der BN-Hilite-Wert ist identisch mit dem von der Übertragung übertragenen \_ Benachrichtigungs Code [ \_ ](bn-pushed.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

