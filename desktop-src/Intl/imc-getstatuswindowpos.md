---
description: Weist ein IME-Fenster an, die Position des Statusfensters abzurufen. Zum Senden dieses Befehls verwendet die Anwendung die WM \_ IME \_ CONTROL-Nachricht mit den unten gezeigten Parametereinstellungen.
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: IMC_GETSTATUSWINDOWPOS Befehl (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfb542ef95a7825e4809e0fa2ce9175493bffeffbbaa36926a91299746026d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068080"
---
# <a name="imc_getstatuswindowpos-command"></a>IMC \_ GETSTATUSWINDOWPOS-Befehl

Weist ein IME-Fenster an, die Position des Statusfensters abzurufen. Zum Senden dieses Befehls verwendet die Anwendung die [**WM \_ IME \_ CONTROL-Nachricht**](wm-ime-control.md) mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie diese Einstellung auf IMC \_ GETSTATUSWINDOWPOS fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) zurück, die die x-Koordinate und die y-Koordinate der Statusfensterposition in Bildschirmkoordinaten relativ zur oberen linken Ecke des Bildschirms enthält.

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
</dt> <dt>

[**WM \_ IME \_ CONTROL**](wm-ime-control.md)
</dt> </dl>

 

 
