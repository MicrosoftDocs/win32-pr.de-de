---
description: Weist ein IME-Fenster an, den Stil des Kompositions Fensters festzulegen. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: IMC_SETCOMPOSITIONWINDOW Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345142"
---
# <a name="imc_setcompositionwindow-command"></a>IMC \_ setcompositionwindow-Befehl

Weist ein IME-Fenster an, den Stil des Kompositions Fensters festzulegen. Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMC \_ setcompositionwindow fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Zeiger auf eine [**compositionform**](/windows/win32/api/imm/ns-imm-compositionform) -Struktur, die die Stil Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Mit diesem Befehl wird der Stil im aktuellen Eingabe Kontext festgelegt, und anschließend wird der Stil auf jedes IME-Fenster angewendet, das diesen Eingabe Kontext empfängt.

Standardmäßig verfügt das IME-Fenster über die Art des CFS- \_ Punkts. Bei diesem Stil verwendet das IME-Fenster die aktuelle Position der Einfügemarke und den Fenster Client Bereich, wenn ein Kompositionsfenster geöffnet wird.

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

[**Compositionform**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[**WM \_ IME- \_ Steuerelement**](wm-ime-control.md)
</dt> </dl>

 

 




