---
title: WM_SIZECLIPBOARD Meldung (Winuser. h)
description: Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF \_ -Besitzer Anzeige Format enthält und der Client Bereich der Zwischenablage-Viewer die Größe geändert hat.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- WM_SIZECLIPBOARD Nachrichten Datenaustausch
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
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741864"
---
# <a name="wm_sizeclipboard-message"></a>WM- \_ sizeclipboard-Meldung

Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF-Besitzer [**\_ Anzeige**](standard-clipboard-formats.md) Format enthält und der Client Bereich der Zwischenablage-Viewer die Größe geändert hat.


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster der Zwischenablage Anzeige.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für ein globales Speicher Objekt, das eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur enthält. Die-Struktur gibt die neuen Dimensionen des Client Bereichs der Zwischenablage Anzeige an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn das Fenster der Zwischenablage Anzeige zerstört oder seine Größe geändert wird, wird eine **WM- \_ sizeclipboard** -Meldung mit einem NULL-Rechteck (0, 0, 0, 0) als neue Größe gesendet. Dadurch wird es dem Besitzer der Zwischenablage ermöglicht, seine Anzeige Ressourcen freizugeben.

Der Besitzer der Zwischenablage muss die [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) -Funktion verwenden, um das Speicher Objekt zu sperren, das [**Rect**](/previous-versions//dd162897(v=vs.85))enthält. Vor der Rückgabe muss der Besitzer der Zwischenablage das Objekt mithilfe der [**globalunlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) -Funktion entsperren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Licher**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

