---
title: WM_MENUGETOBJECT Meldung (Winuser. h)
description: Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Maus Cursor in ein Menü Element oder von der Mitte des Elements zum oberen oder unteren Rand des Elements bewegt wird.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT von Meldungs Menüs und anderen Ressourcen
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
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519204"
---
# <a name="wm_menugetobject-message"></a>WM \_ menugetobject-Meldung

Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Maus Cursor in ein Menü Element oder von der Mitte des Elements zum oberen oder unteren Rand des Elements bewegt wird.


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

Ein Zeiger auf eine [**menugetobjectinfo**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung muss einen der folgenden Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                | BESCHREIBUNG                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Mngo \_ NoError**</dt> <dt>0x00000001</dt> </dl>     | Ein Schnittstellen Zeiger wurde im **pvobj** -Member von [**menugetobjectinfo**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) zurückgegeben.<br/> |
| <dl> <dt>**Mngo \_ Nointerface**</dt> <dt>0x00000000</dt> </dl> | Die-Schnittstelle wird nicht unterstützt.<br/>                                                                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Menüs](menus.md)
</dt> </dl>

 

 





