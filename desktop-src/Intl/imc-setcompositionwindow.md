---
description: Weist ein IME-Fenster an, den Stil des Kompositionsfensters festzulegen. Zum Senden dieses Befehls verwendet die Anwendung die WM \_ IME \_ CONTROL-Nachricht mit den unten gezeigten Parametereinstellungen.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: IMC_SETCOMPOSITIONWINDOW Befehl (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bb1fe35ecd530e8173b7ea57f7c6ff414105d09507a11bf4eed29ab0595e604
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107260"
---
# <a name="imc_setcompositionwindow-command"></a>IMC \_ SETCOMPOSITIONWINDOW-Befehl

Weist ein IME-Fenster an, den Stil des Kompositionsfensters festzulegen. Zum Senden dieses Befehls verwendet die Anwendung die [**WM \_ IME \_ CONTROL-Nachricht**](wm-ime-control.md) mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMC \_ SETCOMPOSITIONWINDOW fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Zeiger auf eine [**COMPOSITIONFORM-Struktur,**](/windows/win32/api/imm/ns-imm-compositionform) die die Stilinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 oder andernfalls einen Wert ungleich 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Dieser Befehl legt den Stil im aktuellen Eingabekontext fest, und der Stil wird anschließend auf jedes IME-Fenster angewendet, das diesen Eingabekontext empfängt.

Standardmäßig weist das IME-Fenster den CFS \_ POINT-Stil auf. Bei diesem Stil verwendet das IME-Fenster die aktuelle Caretposition und den Clientbereich des Fensters, wenn ein Kompositionsfenster geöffnet wird.

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

[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[**WM \_ IME \_ CONTROL**](wm-ime-control.md)
</dt> </dl>

 

 




