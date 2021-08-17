---
title: WM_MENUCOMMAND-Nachricht (Winuser.h)
description: Wird gesendet, wenn der Benutzer eine Auswahl aus einem Menü trifft.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND Meldung Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d97f629b5d4b0c245606b36efea9ebcb230c4c9fd14d837e18949880a7e7e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971809"
---
# <a name="wm_menucommand-message"></a>WM \_ MENUCOMMAND-Nachricht

Wird gesendet, wenn der Benutzer eine Auswahl aus einem Menü trifft.


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des ausgewählten Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Menü für das ausgewählte Element.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mit der **WM \_ MENUCOMMAND-Meldung** erhalten Sie ein Handle für das Menü, sodass Sie auf die Menüdaten in der [**MENUINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-menuinfo) zugreifen können. Außerdem erhalten Sie den Index des ausgewählten Elements. Dies ist in der Regel das, was Anwendungen benötigen. Im Gegensatz dazu erhalten Sie in der [**WM \_ COMMAND-Meldung**](wm-command.md) den Menüelementbezeichner.

Die **WM \_ MENUCOMMAND-Nachricht** wird nur für Menüs gesendet, die mit dem **MNS \_ NOTIFYBYPOS-Flag** definiert sind, das im **dwStyle-Member** der [**MENUINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-menuinfo) festgelegt ist.

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

 

 





