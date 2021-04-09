---
title: TVN_ITEMCHANGED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Element Attribute geändert wurden. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- Windows-Steuerelemente für TVN_ITEMCHANGED Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858934"
---
# <a name="tvn_itemchanged-notification-code"></a>TVN \_ ItemChanged-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Element Attribute geändert wurden. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtvitemchange**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) -Struktur, die das geänderte Element beschreibt. Der **uchanged** -Member ist auf den tvif-Status festgelegt \_ .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **false** zurück, um die Änderung zu akzeptieren, oder **true** , um die Änderung zu verhindern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ Itemchangedw** (Unicode) und **TVN \_ itemchangeda** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TVN \_ ItemChanging](tvn-itemchanging.md)
</dt> </dl>

 

 





