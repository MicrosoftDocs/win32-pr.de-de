---
description: Ruft die Schriftart ab, mit der das Steuerelement derzeit seinen Text zeichnet.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: WM_GETFONT-Nachricht (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d3dbd4a34557459fa0f31f6e2a96eba9d0cab36d54cf2bddaa353343a18b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200471"
---
# <a name="wm_getfont-message"></a>WM \_ GETFONT-Nachricht

Ruft die Schriftart ab, mit der das Steuerelement derzeit seinen Text zeichnet.


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HFONT**

Der Rückgabewert ist ein Handle für die vom Steuerelement verwendete Schriftart oder **NULL,** wenn das Steuerelement die Systemschriftart verwendet.

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

[**WM \_ SETFONT**](wm-setfont.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 




