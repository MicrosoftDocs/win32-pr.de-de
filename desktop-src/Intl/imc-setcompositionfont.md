---
description: Weist ein IME-Fenster an, die logische Schriftart anzugeben, die zum Anzeigen von Zwischenzeichen im Kompositionsfenster verwendet werden soll. Zum Senden dieses Befehls verwendet die Anwendung die WM \_ IME \_ CONTROL-Nachricht mit den unten gezeigten Parametereinstellungen.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: IMC_SETCOMPOSITIONFONT Befehl (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ebc9f435371d4ae08b12191419c95fd53c69256064f0e90bb654e75fab922f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949271"
---
# <a name="imc_setcompositionfont-command"></a>IMC \_ SETCOMPOSITIONFONT-Befehl

Weist ein IME-Fenster an, die logische Schriftart anzugeben, die zum Anzeigen von Zwischenzeichen im Kompositionsfenster verwendet werden soll. Zum Senden dieses Befehls verwendet die Anwendung die [**WM \_ IME \_ CONTROL-Nachricht**](wm-ime-control.md) mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMC \_ SETCOMPOSITIONFONT fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Zeiger auf eine [**LOGFONT-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-logfonta) die Informationen zur logischen Schriftart enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 oder andernfalls einen Wert ungleich 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Bei der Verarbeitung dieses Befehls ändert das IME-Fenster die aktuell ausgewählte Schriftart im Eingabekontext.

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

[**WM \_ IME \_ CONTROL**](wm-ime-control.md)
</dt> </dl>

 

 
