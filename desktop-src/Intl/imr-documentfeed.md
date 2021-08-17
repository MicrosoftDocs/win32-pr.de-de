---
description: Benachrichtigt eine Anwendung, wenn der ausgewählte IME die konvertierte Zeichenfolge aus der Anwendung benötigt. Die Anwendung empfängt diesen Befehl über die WM \_ IME \_ REQUEST-Nachricht mit parametern, die wie unten gezeigt festgelegt sind.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: IMR_DOCUMENTFEED Benachrichtigungscode (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbef4c83d35fa02e2c879d76b9520df6d01588c07cb725b13e66888e9dd27722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948777"
---
# <a name="imr_documentfeed-notification-code"></a>IMR \_ DOCUMENTFEED-Benachrichtigungscode

Benachrichtigt eine Anwendung, wenn der ausgewählte IME die konvertierte Zeichenfolge aus der Anwendung benötigt. Die Anwendung empfängt diesen Befehl über die [**WM \_ IME \_ REQUEST-Nachricht**](wm-ime-request.md) mit parametern, die wie unten gezeigt festgelegt sind.


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMR \_ DOCUMENTFEED fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Zeiger auf einen Puffer, der die [**RECONVERTSTRING-Struktur enthalten**](/windows/win32/api/imm/ns-imm-reconvertstring) soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die aktuelle Reconversion-Zeichenfolgenstruktur zurück. Wenn *lParam* auf **NULL festgelegt ist,** gibt die Anwendung die erforderliche Größe zurück, damit der Puffer die Struktur enthalten kann. Der Befehl gibt 0 zurück, wenn er nicht erfolgreich ist.

## <a name="remarks"></a>Hinweise

Der IME speichert konvertierte Zeichenfolgen zwischen, um eine höhere Konvertierungsgenauigkeit zu verwenden. Eine Einschränkung beim Zwischenspeichern des IME ist, dass die konvertierte Zeichenfolge unter den folgenden Umständen verloren geht:

-   Die Position des Caretcursors für die Anwendung wird durch einen Schlüssel verschoben, z. B. durch eine Cursortaste.
-   Die Position des Caretzeigers für die Anwendung wird mit der Maus verschoben.
-   Ein neues Dokument wird geöffnet.

Mit dem **BEFEHL IMR \_ DOCUMENTFEED** kann der IME seine zwischengespeicherten Zeichenfolgen jederzeit aktualisieren. Die Verwendung dieses Befehls verbessert die Konvertierungsgenauigkeit.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eingabemethode-Manager](input-method-manager.md)
</dt> <dt>

[Befehle des Eingabemethode-Managers](input-method-manager-commands.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**WM \_ \_ IME-ANFORDERUNG**](wm-ime-request.md)
</dt> </dl>

 

 




