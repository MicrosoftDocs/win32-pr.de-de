---
description: Benachrichtigt eine Anwendung, wenn der ausgewählte IME die konvertierte Zeichenfolge aus der Anwendung benötigt. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit den festgelegten Parametern, wie unten gezeigt.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: IMR_DOCUMENTFEED Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215922"
---
# <a name="imr_documentfeed-notification-code"></a>IMR- \_ documentfeed-Benachrichtigungs Code

Benachrichtigt eine Anwendung, wenn der ausgewählte IME die konvertierte Zeichenfolge aus der Anwendung benötigt. Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit den festgelegten Parametern, wie unten gezeigt.


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMR \_ documentfeed fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Zeiger auf einen Puffer, der die [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die aktuelle Zeichen folgen Struktur der erneuten Konvertierung zurück. Wenn *LPARAM* auf **null** festgelegt ist, gibt die Anwendung die erforderliche Größe für den Puffer zum Speichern der Struktur zurück. Der Befehl gibt 0 (null) zurück, wenn er nicht erfolgreich ist.

## <a name="remarks"></a>Bemerkungen

Der IME speichert konvertierte Zeichen folgen für eine höhere Konvertierungs Genauigkeit zwischen. Eine zwischen Speicherungs Einschränkung für den IME besteht darin, dass die konvertierte Zeichenfolge in den folgenden Situationen verloren geht:

-   Die Position der Einfügemarke für die Anwendung wird durch einen Schlüssel verschoben, z. b. eine Cursor Taste.
-   Die Position der Einfügemarke für die Anwendung wird mit der Maus bewegt.
-   Ein neues Dokument wird geöffnet.

Mit dem **IMR \_ documentfeed** -Befehl kann der IME seine zwischengespeicherten Zeichen folgen jederzeit aktualisieren. Die Verwendung dieses Befehls verbessert die Konvertierungs Genauigkeit.

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

[**Reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**WM- \_ IME- \_ Anforderung**](wm-ime-request.md)
</dt> </dl>

 

 




