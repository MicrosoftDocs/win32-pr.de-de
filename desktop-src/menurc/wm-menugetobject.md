---
title: WM_MENUGETOBJECT-Nachricht (Winuser.h)
description: Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Mauszeiger in ein Menüelement eintritt oder sich von der Mitte des Elements nach oben oder unten des Elements bewegt.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT Meldung Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a9ac39a453a007e4ad81f0369dc1d78f268f3496ffb4aa9b371a2d3f5ca0baa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119354470"
---
# <a name="wm_menugetobject-message"></a>WM \_ MENUGETOBJECT-Meldung

Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Mauszeiger in ein Menüelement eintritt oder sich von der Mitte des Elements nach oben oder unten des Elements bewegt.


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**MENUGETOBJECTINFO-Struktur.**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung sollte einen der folgenden Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                | BESCHREIBUNG                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNGO \_ NOERROR**</dt> <dt>0x00000001</dt> </dl>     | Im **pvObj-Member** von [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) wurde ein Schnittstellenzeiger zurückgegeben.<br/> |
| <dl> <dt>**MNGO \_ NOINTERFACE**</dt> <dt>0x00000000</dt> </dl> | Die -Schnittstelle wird nicht unterstützt.<br/>                                                                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Menüs](menus.md)
</dt> </dl>

 

 





