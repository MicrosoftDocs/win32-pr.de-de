---
description: Weist das IME-Fenster an, das Statusfenster auszublenden. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: e3da5962-a652-409e-b0ec-eb93671049b4
title: IMC_CLOSESTATUSWINDOW Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207f04d53f269318f87ed11038cbd6817d5e607e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869263"
---
# <a name="imc_closestatuswindow-command"></a>IMC \_ closestatus Window-Befehl

Weist das IME-Fenster an, das Statusfenster auszublenden. Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_CLOSESTATUSWINDOW
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf "IMC \_ closestatus Window" fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Wenn das Fenster IME-Status bereits ausgeblendet ist, führt dieser Befehl nichts aus. Obwohl eine Anwendung diesen Befehl an das IME-Fenster senden kann, erhält die Anwendung nicht den entsprechenden [IMN \_ closestatus Window](imn-closestatuswindow.md) -Befehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Befehle](input-method-manager-commands.md)
</dt> </dl>

 

 




