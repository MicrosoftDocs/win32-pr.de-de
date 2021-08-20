---
description: Benachrichtigt eine Anwendung, wenn die Statusfensterposition im Eingabekontext aktualisiert wird. Die Anwendung empfängt diesen Befehl über die WM \_ IME \_ NOTIFY-Nachricht mit Parametereinstellungen wie folgt.
ms.assetid: 15e65aff-67d9-4d1a-a6a7-b921cecb3aec
title: IMN_SETSTATUSWINDOWPOS Benachrichtigungscode (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0c414de9ba8e75a85d6649d747173c73af274c3527cf9f0dc5b7540a3bf8669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810127"
---
# <a name="imn_setstatuswindowpos-notification-code"></a>IMN \_ SETSTATUSWINDOWPOS-Benachrichtigungscode

Benachrichtigt eine Anwendung, wenn die Statusfensterposition im Eingabekontext aktualisiert wird. Die Anwendung empfängt diesen Befehl über die [**WM \_ IME \_ NOTIFY-Nachricht**](wm-ime-notify.md) mit Parametereinstellungen wie folgt.


```C++
IMN_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMN \_ SETSTATUSWINDOWPOS fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl hat keinen Rückgabewert.

## <a name="remarks"></a>Hinweise

Die Anwendung kann mithilfe des [**Befehls IMC \_ GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) Informationen zur Position des Statusfensters abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Befehle des Eingabemethoden-Managers](input-method-manager-commands.md)
</dt> <dt>

[**IMC \_ GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




