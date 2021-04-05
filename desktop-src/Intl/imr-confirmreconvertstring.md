---
description: Benachrichtigt eine Anwendung, wenn der IME die reconvertstring-Struktur ändern muss. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: IMR_CONFIRMRECONVERTSTRING Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c500a155be14f447bb07ad506e12d5bece66e225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756493"
---
# <a name="imr_confirmreconvertstring-notification-code"></a>IMR \_ confirmreconvertstring-Benachrichtigungs Code

Benachrichtigt eine Anwendung, wenn der IME die [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur ändern muss. Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit den Parametereinstellungen, wie unten gezeigt.


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMR \_ confirmreconvertstring fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Zeiger auf eine [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur aus dem IME. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn die Anwendung die geänderte [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur akzeptiert. Andernfalls gibt der Befehl 0 zurück, und der IME verwendet die ursprüngliche **reconvertstring** -Struktur.

## <a name="remarks"></a>Bemerkungen

Die Anwendung füllt die [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur auf, wenn der [IMR \_ reconvertstring](imr-reconvertstring.md) -Befehl empfangen wird.

Nachdem die Anwendung [IMR \_ reconvertstring](imr-reconvertstring.md)verarbeitet hat, kann der IME die [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur ggf. nicht mehr anpassen. Der IME sendet eine WM \_ IME- \_ Anforderung mit **IMR \_ confirmreconvertstring** , um die Änderungen an der **reconvertstring** -Struktur zu bestätigen. Wenn die Anwendung **true** für **IMR \_ confirmreconvertstring** zurückgibt, generiert der IME eine neue Kompositions Zeichenfolge auf der Grundlage der **reconvertstring** -Struktur für den **IMR \_ confirmreconvertstring** -Befehl. Wenn die Anwendung für **IMR \_ confirmreconvertstring** **false** zurückgibt, generiert der IME eine neue Kompositions Zeichenfolge auf der Grundlage der ursprünglichen **reconvertstring** -Struktur, die von der Anwendung im IMR- \_ Befehl "reconvertstring" angegeben wird.

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

[IMR \_ reconvertstring](imr-reconvertstring.md)
</dt> <dt>

[**Reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**WM- \_ IME- \_ Anforderung**](wm-ime-request.md)
</dt> </dl>

 

 




