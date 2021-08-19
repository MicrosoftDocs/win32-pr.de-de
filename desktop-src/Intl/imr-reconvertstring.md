---
description: Benachrichtigt eine Anwendung, wenn ein ausgewählter IME eine Zeichenfolge für die Neukonvertierung benötigt. Die Anwendung empfängt diesen Befehl über die WM \_ IME \_ REQUEST-Nachricht mit Parametereinstellungen, wie unten dargestellt.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: IMR_RECONVERTSTRING Benachrichtigungscode (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dfc2b188a2873af3ec7004ffaac65a3cce0b4257c1428dfe4abfcba9d2b2aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948757"
---
# <a name="imr_reconvertstring-notification-code"></a>IMR \_ RECONVERTSTRING-Benachrichtigungscode

Benachrichtigt eine Anwendung, wenn ein ausgewählter IME eine Zeichenfolge für die Neukonvertierung benötigt. Die Anwendung empfängt diesen Befehl über die [**WM \_ IME \_ REQUEST-Nachricht**](wm-ime-request.md) mit Parametereinstellungen, wie unten dargestellt.


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMR \_ RECONVERTSTRING fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Zeiger auf einen Puffer, der die [**RECONVERTSTRING-Struktur**](/windows/win32/api/imm/ns-imm-reconvertstring) und -Zeichenfolgen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die aktuelle Reconversion-Zeichenfolgenstruktur zurück. Wenn *lParam* auf **NULL festgelegt** ist, gibt die Anwendung die Größe für den Puffer zurück, der für die Struktur erforderlich ist. Der Befehl gibt 0 zurück, wenn er nicht erfolgreich ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethode-Manager](input-method-manager.md)
</dt> <dt>

[Befehle des Eingabemethode-Managers](input-method-manager-commands.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**WM \_ \_ IME-ANFORDERUNG**](wm-ime-request.md)
</dt> </dl>

 

 




