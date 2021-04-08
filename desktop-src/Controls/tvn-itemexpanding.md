---
title: TVN_ITEMEXPANDING Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements gerade erweitert oder reduziert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- Windows-Steuerelemente für TVN_ITEMEXPANDING Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957091"
---
# <a name="tvn_itemexpanding-notification-code"></a>TVN \_ itemexpandingbenachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements gerade erweitert oder reduziert wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur. Der **itemnew** -Member ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die gültige Informationen über das übergeordnete Element in den Elementen " **Hitem**", " **State**" und " **LPARAM** " enthält. Der **Aktionsmember** gibt an, ob die Liste erweitert oder reduziert werden soll. Eine Liste möglicher Werte finden Sie in der Beschreibung der [**TVM \_ Expand**](tvm-expand.md) Message.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um zu verhindern, dass die Liste erweitert oder reduziert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ Itemexpandingw** (Unicode) und **TVN \_ itemexpandinga** (ANSI)<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TVN \_ itemexpanded](tvn-itemexpanded.md)
</dt> </dl>

 

 





