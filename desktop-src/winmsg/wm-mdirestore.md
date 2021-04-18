---
description: Eine Anwendung sendet die WM- \_ mdirestore-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster von maximierter oder minimierter Größe wiederherzustellen.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: WM_MDIRESTORE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354464"
---
# <a name="wm_mdirestore-message"></a>WM- \_ mumgeleitet-Speicher Nachricht

Eine Anwendung sendet die **WM- \_ mdirestore** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster von maximierter oder minimierter Größe wiederherzustellen.


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das untergeordnete MDI-Fenster, das wieder hergestellt werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **null**

Der Rückgabewert ist immer 0 (null).

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

[**WM- \_ mdimaximierung**](wm-mdimaximize.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




