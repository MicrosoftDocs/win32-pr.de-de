---
description: Weist ein IME-Fenster an, die Position des Kandidatenfensters abzurufen. Zum Senden dieses Befehls verwendet die Anwendung die WM \_ IME \_ CONTROL-Nachricht mit den unten gezeigten Parametereinstellungen.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: IMC_GETCANDIDATEPOS Befehl (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e155a08c9d95fa2ac9f865d80b18d51120d19b28489bcad418eb4323dda39c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107320"
---
# <a name="imc_getcandidatepos-command"></a>IMC \_ GETCANDIDATEPOS-Befehl

Weist ein IME-Fenster an, die Position des Kandidatenfensters abzurufen. Zum Senden dieses Befehls verwendet die Anwendung die [**WM \_ IME \_ CONTROL-Nachricht**](wm-ime-control.md) mit den unten gezeigten Parametereinstellungen.


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie diese Einstellung auf IMC \_ GETCANDIDATEPOS fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Zeiger auf eine [**CANDIDATEFORM-Struktur,**](/windows/win32/api/imm/ns-imm-candidateform) die die Position des Kandidatenfensters enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 oder andernfalls einen Wert ungleich 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Da die IME die Position eines Kandidatenfensters anpassen kann, verwendet eine Anwendung diesen Befehl, um die tatsächliche Position abzurufen, um zu entscheiden, ob das Fenster neu positioniert werden soll. Die abgerufene Position befindet sich in Fensterkoordinaten relativ zum Fenster mit dem aktuellen Eingabefokus.

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

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 




