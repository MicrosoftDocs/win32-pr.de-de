---
title: BN_UNHILITE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn die Hervorhebung aus einer Schaltfläche entfernt werden soll.
ms.assetid: 9839a55b-9e9c-4c9c-8e92-347007ea27be
keywords:
- Windows-Steuerelemente für BN_UNHILITE Benachrichtigungs
topic_type:
- apiref
api_name:
- BN_UNHILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395901548103a7a678b4873e1fde52e259297ebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949549"
---
# <a name="bn_unhilite-notification-code"></a>Milliarden- \_ unhilite-Benachrichtigungs Code

Wird gesendet, wenn die Hervorhebung aus einer Schaltfläche entfernt werden soll.

> [!Note]  
> Dieser Benachrichtigungs Code wird nur für die Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3,0 bereitgestellt. Anwendungen sollten für diese [**Aufgabe \_ den Schrift**](button-styles.md) Schnitt-Stil und die [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur des s verwenden.

 

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
BN_UNHILITE

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

Der BN- \_ unhilite-Wert ist identisch mit dem [nicht per \_ pushcode verwalteten](bn-unpushed.md) Benachrichtigungs Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

