---
title: WM_MENUCOMMAND Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer eine Auswahl aus einem Menü trifft.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND von Meldungs Menüs und anderen Ressourcen
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
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392222"
---
# <a name="wm_menucommand-message"></a>WM- \_ MenuCommand-Meldung

Wird gesendet, wenn der Benutzer eine Auswahl aus einem Menü trifft.


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des ausgewählten Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Menü für das ausgewählte Element.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit der " **WM \_ MenuCommand** "-Meldung erhalten Sie ein Handle für das Menü, sodass Sie auf die Menü Daten in der [**menuinfo**](/windows/win32/api/winuser/ns-winuser-menuinfo) -Struktur zugreifen können. Außerdem erhalten Sie den Index des ausgewählten Elements, das in der Regel von den Anwendungen benötigt wird. Im Gegensatz dazu gibt Ihnen die [**WM- \_ Befehls**](wm-command.md) Meldung den Menü Element Bezeichner.

Die " **WM \_ MenuCommand** "-Meldung wird nur für Menüs gesendet, die mit dem im **dwstyle** -Member der [**menuinfo**](/windows/win32/api/winuser/ns-winuser-menuinfo) -Struktur festgelegten **MNS- \_ notifybypos** -Flag definiert werden.

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

 

 





