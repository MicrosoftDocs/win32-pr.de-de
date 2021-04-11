---
title: TVN_ITEMEXPANDED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements erweitert oder reduziert wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- Windows-Steuerelemente für TVN_ITEMEXPANDED Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105945"
---
# <a name="tvn_itemexpanded-notification-code"></a>TVN \_ itemexpanded-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements erweitert oder reduziert wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur. Der **itemnew** -Member ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die gültige Informationen über das übergeordnete Element in den Elementen " **Hitem**", " **State**" und " **LPARAM** " enthält. Der **Aktionsmember** gibt an, ob die Liste erweitert oder reduziert wurde. Eine Liste möglicher Werte finden Sie in der Beschreibung der [**TVM \_ Expand**](tvm-expand.md) Message.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ Itemexpandedw** (Unicode) und **TVN \_ itemexpandeda** (ANSI)<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TVN \_ itemexpanding](tvn-itemexpanding.md)
</dt> </dl>

 

 





