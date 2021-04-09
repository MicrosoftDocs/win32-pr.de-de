---
description: Weist das IME-Fenster an, das Statusfenster anzuzeigen. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: IMC_OPENSTATUSWINDOW Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd0b5e19ef6a026459eedb050e9ac9587b5ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862924"
---
# <a name="imc_openstatuswindow-command"></a>Befehl "- \_ openstatus Window" von IMC

Weist das IME-Fenster an, das Statusfenster anzuzeigen. Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf "IMC \_ openstatus Window" fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Dieser Befehl wird ignoriert, wenn sich das Betriebssystem nicht im Modus "IME-Status anzeigen" befindet. Der Benutzer kann den IME-Status Modus anzeigen auf der Taskleiste festlegen oder deaktivieren.

Wenn das Statusfenster bereits angezeigt wird, führt dieser Befehl nichts aus. Obwohl die Anwendung diesen Befehl an das IME-Fenster senden kann, empfängt die Anwendung nicht den entsprechenden [**IMN \_ openstatus Window**](imn-openstatuswindow.md) -Befehl.

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
</dt> <dt>

[**WM \_ IME- \_ Steuerelement**](wm-ime-control.md)
</dt> </dl>

 

 




