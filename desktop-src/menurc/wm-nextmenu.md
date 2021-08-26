---
title: WM_NEXTMENU (Winuser.h)
description: Wird an eine Anwendung gesendet, wenn die NACH-RECHTS- oder NACH-LINKS-TASTE verwendet wird, um zwischen der Menüleiste und dem Systemmenü zu wechseln.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU von Nachrichtenmenüs und anderen Ressourcen
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
ms.openlocfilehash: 635ce19efbcfdfd8451f929affbbe0fe2b2c000bc4912977062f3fba2c54e9c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952080"
---
# <a name="wm_nextmenu-message"></a>WM \_ NEXTMENU-Nachricht

Wird an eine Anwendung gesendet, wenn die NACH-RECHTS- oder NACH-LINKS-TASTE verwendet wird, um zwischen der Menüleiste und dem Systemmenü zu wechseln.


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Virtuelle Schlüsselcode des Schlüssels. Weitere Informationen [**finden Sie unter Codes für virtuelle Schlüssel.**](/windows/desktop/inputdev/virtual-key-codes)

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**MDINEXTMENU-Struktur,**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) die Informationen über das zu aktivierende Menü enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Als Reaktion auf diese Nachricht kann die Anwendung das Menü angeben, zu dem im **hmenuNext-Member** von [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) und im Fenster die Menübenachrichtigungsmeldungen im **hwndNext-Member** der **MDINEXTMENU-Struktur** empfangen werden sollen. Sie müssen beide Member festlegen, damit die Änderungen wirksam werden (sie sind anfänglich **NULL).**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

