---
title: STN_DBLCLK Benachrichtigungs Code (Winuser. h)
description: Der STN \_ dblclk-Benachrichtigungs Code wird gesendet, wenn der Benutzer auf ein statisches Steuerelement mit dem SS-Benachrichtigungs Stil doppelklickt \_ . Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- Windows-Steuerelemente für STN_DBLCLK Benachrichtigungs
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 853ed5142de99dc85b729b4c4ea208273d4ace1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040309"
---
# <a name="stn_dblclk-notification-code"></a>STN \_ dblclk-Benachrichtigungs Code

Der STN \_ dblclk-Benachrichtigungs Code wird gesendet, wenn der Benutzer auf ein statisches Steuerelement mit dem [**SS \_**](static-control-styles.md) -Benachrichtigungs Stil doppelklickt. Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
STN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des statischen Steuer Elements. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das statische Steuerelement.

</dd> </dl>

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

[\_angeklickte STN](stn-clicked.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Statische Steuerelemente](static-controls.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

