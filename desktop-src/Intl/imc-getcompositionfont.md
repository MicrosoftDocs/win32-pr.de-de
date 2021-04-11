---
description: Weist ein IME-Fenster an, die logische Schriftart zum Anzeigen von zwischen Zeichen im Kompositionsfenster abzurufen. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: IMC_GETCOMPOSITIONFONT Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214762"
---
# <a name="imc_getcompositionfont-command"></a>IMC \_ getcompositionfont-Befehl

Weist ein IME-Fenster an, die logische Schriftart zum Anzeigen von zwischen Zeichen im Kompositionsfenster abzurufen. Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf "IMC \_ getcompositionfont" fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Ein Zeiger auf eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, die Informationen über die logische Schriftart empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).

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

 

 
