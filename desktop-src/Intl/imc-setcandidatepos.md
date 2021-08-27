---
description: Weist ein IME-Fenster an, die Position des Kandidatenfensters zu festlegen. Zum Senden dieses Befehls verwendet die Anwendung die WM \_ IME \_ CONTROL-Nachricht mit den unten gezeigten Parametereinstellungen.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: IMC_SETCANDIDATEPOS Befehl (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fbce21cac53eecf3ad5b99cc7dbe5cf5b52304ed25869a5c3f6ae729ac9d016
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107270"
---
# <a name="imc_setcandidatepos-command"></a>IMC \_ SETCANDIDATEPOS-Befehl

Weist ein IME-Fenster an, die Position des Kandidatenfensters zu festlegen. Zum Senden dieses Befehls verwendet die Anwendung die [**WM \_ IME \_ CONTROL-Nachricht**](wm-ime-control.md) mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMC \_ SETCANDIDATEPOS fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Zeiger auf eine [**CANDIDATEFORM-Struktur,**](/windows/win32/api/imm/ns-imm-candidateform) die die x-Koordinate und die y-Koordinate für das Kandidatenfenster enthält. Die Anwendung sollte den **dwIndex-Member** dieser Struktur festlegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 oder andernfalls einen Wert ungleich 0 zurück.

## <a name="remarks"></a>Hinweise

Dieser Befehl ist für Anwendungen vorgesehen, die Kompositionszeichen selbst anzeigen, aber das IME-Fenster verwenden, um Kandidaten anzuzeigen.

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

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**WM \_ \_ IME-STEUERUNG**](wm-ime-control.md)
</dt> </dl>

 

 




