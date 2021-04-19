---
description: Wird einmal an ein Fenster gesendet, nachdem es in die modale Verschiebungs-oder Anpassungs Schleife gelangt ist.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: WM_ENTERSIZEMOVE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368876"
---
# <a name="wm_entersizemove-message"></a>WM- \_ entersizemove-Meldung

Wird einmal an ein Fenster gesendet, nachdem es in die modale Verschiebungs-oder Anpassungs Schleife gelangt ist. Das Fenster wechselt in die modale Verschiebungs-oder Anpassungs Schleife, wenn der Benutzer auf die Titelleiste des Fensters oder den Größen Anpassungsrahmen klickt, oder wenn das Fenster die " [**WM \_ syscommand**](../menurc/wm-syscommand.md) "-Meldung an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt und der *wParam* -Parameter der Nachricht den Wert **SC \_ Move** oder **SC \_ size** angibt. Der Vorgang ist fertiggestellt, wenn [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) zurückgegeben wird.

Das System sendet die WM-Nachricht " **\_ entersizemove** " unabhängig davon, ob das Ziehen von vollständigen Fenstern aktiviert ist.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_ENTERSIZEMOVE                0x0231
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM- \_ exitsizemove**](wm-exitsizemove.md)
</dt> <dt>

[**WM ( \_ syscommand)**](../menurc/wm-syscommand.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
