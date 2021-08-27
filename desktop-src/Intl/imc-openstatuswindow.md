---
description: Weist das IME-Fenster an, das Statusfenster anzuzeigen. Zum Senden dieses Befehls verwendet die Anwendung die WM \_ IME \_ CONTROL-Nachricht mit den unten gezeigten Parametereinstellungen.
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: IMC_OPENSTATUSWINDOW (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 263640a3f104c9abf72a7eb5b33bce6ff3813ca40645c18b179b9b31a95fdda9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107290"
---
# <a name="imc_openstatuswindow-command"></a>IMC \_ OPENSTATUSWINDOW-Befehl

Weist das IME-Fenster an, das Statusfenster anzuzeigen. Zum Senden dieses Befehls verwendet die Anwendung die [**WM \_ IME \_ CONTROL-Nachricht**](wm-ime-control.md) mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMC \_ OPENSTATUSWINDOW fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 oder andernfalls einen Wert ungleich 0 zurück.

## <a name="remarks"></a>Hinweise

Dieser Befehl wird ignoriert, wenn sich das Betriebssystem nicht im ImE-Statusmodus anzeigen befindet. Der Benutzer kann den IME-Statusmodus anzeigen über die Taskleiste festlegen oder löschen.

Wenn das Statusfenster bereits angezeigt wird, führt dieser Befehl nichts aus. Obwohl die Anwendung diesen Befehl an das IME-Fenster senden kann, erhält die Anwendung nicht den entsprechenden [**IMN \_ OPENSTATUSWINDOW-Befehl.**](imn-openstatuswindow.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethode-Manager](input-method-manager.md)
</dt> <dt>

[Befehle des Eingabemethode-Managers](input-method-manager-commands.md)
</dt> <dt>

[**WM \_ \_ IME-STEUERUNG**](wm-ime-control.md)
</dt> </dl>

 

 




