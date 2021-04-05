---
description: Weist ein IME-Fenster an, die Position des Kompositions Fensters zu erhalten. Um diesen Befehl zu senden, verwendet die Anwendung die WM- \_ IME- \_ Steuerungs Meldung mit den unten gezeigten Parametereinstellungen.
ms.assetid: d2c60974-a602-4a42-8a45-870ee39df001
title: IMC_GETCOMPOSITIONWINDOW Befehl (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32b8f4414311d0727f622a1b552428cd31b0716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752344"
---
# <a name="imc_getcompositionwindow-command"></a>IMC \_ getcompositionwindow-Befehl

Weist ein IME-Fenster an, die Position des Kompositions Fensters zu erhalten. Um diesen Befehl zu senden, verwendet die Anwendung die [**WM- \_ IME- \_ Steuerungs**](wm-ime-control.md) Meldung mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_GETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf "IMC \_ getcompositionwindow" fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Ein Zeiger auf eine [**compositionform**](/windows/win32/api/imm/ns-imm-compositionform) -Struktur, die die Position des Kompositions Fensters enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück oder andernfalls einen Wert ungleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Da der IME die Position eines Kompositions Fensters anpassen kann, verwendet eine Anwendung diesen Befehl, um die tatsächliche Position zu ermitteln, um zu entscheiden, ob das Fenster neu positioniert werden soll. Die abgerufene Position befindet sich in Fenster Koordinaten relativ zu dem Fenster, das den aktuellen Eingabefokus besitzt.

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
</dt> </dl>

 

 




