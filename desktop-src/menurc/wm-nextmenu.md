---
title: WM_NEXTMENU Meldung (Winuser. h)
description: Wird an eine Anwendung gesendet, wenn mit der nach-rechts-oder der nach-links-Taste zwischen der Menüleiste und dem Systemmenü gewechselt wird.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957218"
---
# <a name="wm_nextmenu-message"></a>WM- \_ nextmenu-Meldung

Wird an eine Anwendung gesendet, wenn mit der nach-rechts-oder der nach-links-Taste zwischen der Menüleiste und dem Systemmenü gewechselt wird.


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Code für den virtuellen Schlüssel des Schlüssels. Siehe [**virtuelle Schlüssel Codes**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**mdinextmenu**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) -Struktur, die Informationen über das zu aktivierende Menü enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie auf diese Meldung reagieren, kann die Anwendung das Menü angeben, zu dem im **hmenunext** -Member von [**mdinextmenu**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) gewechselt werden soll, und das Fenster, um die Menü Benachrichtigungs Meldungen im **hwndnext** -Member der **mdinextmenu** -Struktur zu empfangen. Beide Elemente müssen festgelegt werden, damit die Änderungen wirksam werden (Sie sind anfänglich **null**).

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

[**Mdinextmenu**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

**Licher**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

