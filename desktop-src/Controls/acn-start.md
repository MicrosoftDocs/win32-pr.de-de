---
title: ACN_START Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Animations Steuer Elements, dass der zugehörige AVI-Clip mit der Wiedergabe begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM- \_ Befehlsnachricht gesendet.
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- Windows-Steuerelemente für ACN_START Benachrichtigungs
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0354d8b2b41ea8690be47e70cbc577c064e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740520"
---
# <a name="acn_start-notification-code"></a>ACN- \_ Start Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Animations Steuer Elements, dass der zugehörige AVI-Clip mit der Wiedergabe begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht gesendet.


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Animations Steuer Elements. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **HWND** , das das Handle für das Animations Steuerelement angibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

