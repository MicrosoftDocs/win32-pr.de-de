---
description: Weist ein IME-Fenster an, die logische Schriftart anzugeben, die zum Anzeigen von zwischen Zeichen im Kompositionsfenster verwendet werden soll. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: IMC_SETCOMPOSITIONFONT Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb84c9e05ab19206064988a71b0ffc39b21a44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862923"
---
# <a name="imc_setcompositionfont-command"></a>Befehl "IMC \_ setcompositionfont"

Weist ein IME-Fenster an, die logische Schriftart anzugeben, die zum Anzeigen von zwischen Zeichen im Kompositionsfenster verwendet werden soll. Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMC \_ setcompositionfont fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Zeiger auf eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, die Informationen über die logische Schriftart enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Beim Verarbeiten dieses Befehls ändert das IME-Fenster die aktuell ausgewählte Schriftart im Eingabe Kontext.

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

 

 
