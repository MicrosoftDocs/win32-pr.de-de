---
title: WM_CAPTURECHANGED Meldung (Winuser. h)
description: Wird an das Fenster gesendet, das die Maus Aufzeichnung verliert.
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- Tastatur-und Maus Eingaben für WM_CAPTURECHANGED Nachricht
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103406"
---
# <a name="wm_capturechanged-message"></a>WM \_ capturechanged-Meldung

Wird an das Fenster gesendet, das die Maus Aufzeichnung verliert.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Fenster, das die Maus Aufzeichnung erhält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Ein Fenster empfängt diese Meldung auch dann, wenn es [**releasecapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) selbst aufruft. Eine Anwendung sollte nicht versuchen, die Maus Aufzeichnung als Reaktion auf diese Meldung festzulegen.

Wenn diese Meldung empfangen wird, sollte sich ein Fenster bei Bedarf selbst neu zeichnen, um den neuen Zustand der Maus Aufzeichnung widerzuspiegeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Releasecapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

**Licher**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> </dl>

 

