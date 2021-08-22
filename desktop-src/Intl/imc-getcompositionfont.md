---
description: Weist ein IME-Fenster an, die logische Schriftart abzurufen, die zum Anzeigen von Zwischenzeichen im Kompositionsfenster verwendet wird. Zum Senden dieses Befehls verwendet die Anwendung die WM \_ IME \_ CONTROL-Nachricht mit den unten gezeigten Parametereinstellungen.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: IMC_GETCOMPOSITIONFONT Befehl (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ebf26592f2fd000f864685bd79d71b189fc24d695941691fe2e01d48132d00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068100"
---
# <a name="imc_getcompositionfont-command"></a>IMC \_ GETCOMPOSITIONFONT-Befehl

Weist ein IME-Fenster an, die logische Schriftart abzurufen, die zum Anzeigen von Zwischenzeichen im Kompositionsfenster verwendet wird. Zum Senden dieses Befehls verwendet die Anwendung die [**WM \_ IME \_ CONTROL-Nachricht**](wm-ime-control.md) mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMC \_ GETCOMPOSITIONFONT fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Zeiger auf eine LOGFONT-Struktur, die Informationen über die logische Schriftart [**empfängt.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 oder andernfalls einen Wert ungleich 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Befehle des Eingabemethoden-Managers](input-method-manager-commands.md)
</dt> </dl>

 

 
