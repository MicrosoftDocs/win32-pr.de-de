---
title: WM_SIZECLIPBOARD (Winuser.h)
description: Wird von einem Zwischenablage-Viewerfenster an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF OWNERDISPLAY-Format enthält und sich die Größe des Clientbereichs des Zwischenablage-Viewers \_ geändert hat.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- WM_SIZECLIPBOARD der Exchange
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 778caa6538992d927a0451518fcb28b82891773563614ba97c9d9df121fb69f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545319"
---
# <a name="wm_sizeclipboard-message"></a>WM \_ SIZECLIPBOARD-Nachricht

Wird von einem Zwischenablage-Viewerfenster an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im [**CF \_ OWNERDISPLAY-Format**](standard-clipboard-formats.md) enthält und sich die Größe des Clientbereichs des Zwischenablage-Viewers geändert hat.


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Viewerfenster der Zwischenablage.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für ein globales Speicherobjekt, das eine [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) enthält. Die -Struktur gibt die neuen Dimensionen des Clientbereichs des Zwischenablage-Viewers an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Wenn das Viewerfenster der Zwischenablage zerstört oder seine Größe geändert werden soll, wird eine **WM \_ SIZECLIPBOARD-Nachricht** mit einem NULL-Rechteck (0, 0, 0, 0) als neue Größe gesendet. Dadurch kann der Besitzer der Zwischenablage seine Anzeigeressourcen frei geben.

Der Besitzer der Zwischenablage muss die [**GlobalLock-Funktion**](/windows/desktop/api/winbase/nf-winbase-globallock) verwenden, um das Speicherobjekt zu sperren, das [**RECT enthält.**](/previous-versions//dd162897(v=vs.85)) Vor der Rückgabe muss der Besitzer der Zwischenablage das Objekt mithilfe der [**GlobalUnlock-Funktion entsperren.**](/windows/desktop/api/winbase/nf-winbase-globalunlock)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

