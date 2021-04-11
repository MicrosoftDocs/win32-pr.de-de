---
description: Weist ein IME-Fenster an, die Position des Status Fensters festzulegen. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den Parametereinstellungen wie unten gezeigt.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: IMC_SETSTATUSWINDOWPOS Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041805"
---
# <a name="imc_setstatuswindowpos-command"></a>Befehl "der \_ Befehl"

Weist ein IME-Fenster an, die Position des Status Fensters festzulegen. Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den Parametereinstellungen wie unten gezeigt.


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf "IMC \_ SetStatus-WINDOWPOS" fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Zeiger auf eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur, die die x-Koordinate und die y-Koordinate der Position des Status Fensters enthält. Die Koordinaten befinden sich in Bildschirm Koordinaten relativ zur oberen linken Ecke der Anzeige.

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
</dt> <dt>

[**WM \_ IME- \_ Steuerelement**](wm-ime-control.md)
</dt> </dl>

 

 
