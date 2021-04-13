---
title: WM_MENURBUTTONUP Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer die Rechte Maustaste loslässt, während sich der Cursor auf einem Menü Element befindet.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341348"
---
# <a name="wm_menurbuttonup-message"></a>WM- \_ menurbuttonup-Meldung

Wird gesendet, wenn der Benutzer die Rechte Maustaste loslässt, während sich der Cursor auf einem Menü Element befindet.


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Menü Elements, auf dem die Rechte Maustaste losgelassen wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Menü, das das Element enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit der " **WM \_ menurbuttonup** "-Meldung können Anwendungen ein Kontext abhängiger Menü bereitstellen, das auch als Kontextmenü für das Menü Element bezeichnet wird, das in dieser Meldung angegeben ist. Wenn Sie ein Kontextmenü für ein Menü Element anzeigen möchten, können Sie die [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) -Funktion mit **TPM \_ recurse** aufrufen.

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

 

 





