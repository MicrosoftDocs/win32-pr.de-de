---
title: ACN_STOP Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Animations Steuer Elements, dass der zugehörige AVI-Clip beendet wurde. Dieser Benachrichtigungs Code wird in Form einer WM- \_ Befehlsnachricht gesendet.
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- Windows-Steuerelemente für ACN_STOP Benachrichtigungs
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cbdb27677439b7f08b489cba9024d44f3ebee6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040315"
---
# <a name="acn_stop-notification-code"></a>ACN- \_ anstoppbenachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Animations Steuer Elements, dass der zugehörige AVI-Clip beendet wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht gesendet.


```C++
ACN_STOP     

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



 

