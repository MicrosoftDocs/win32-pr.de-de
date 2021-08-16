---
description: Wird gesendet, wenn eine Anwendung den aktivierten Zustand eines Fensters ändert.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: WM_ENABLE Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e01477de7cf1b9052bba752929210a1bc7553445f81f971aec67d7b510653a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200481"
---
# <a name="wm_enable-message"></a>WM \_ ENABLE-Meldung

Wird gesendet, wenn eine Anwendung den aktivierten Zustand eines Fensters ändert. Sie wird an das Fenster gesendet, dessen aktivierter Zustand sich ändert. Diese Meldung wird gesendet, bevor die [**EnableWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-enablewindow) zurückgegeben wird, aber nachdem sich der aktivierte Zustand [**(WS DISABLED-Formatbit) \_**](window-styles.md) des Fensters geändert hat.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob das Fenster aktiviert oder deaktiviert wurde. Dieser Parameter ist **TRUE,** wenn das Fenster aktiviert wurde, oder **FALSE,** wenn das Fenster deaktiviert wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
