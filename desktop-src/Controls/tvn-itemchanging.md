---
title: TVN_ITEMCHANGING Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass sich Element Attribute ändern. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- Windows-Steuerelemente für TVN_ITEMCHANGING Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517825"
---
# <a name="tvn_itemchanging-notification-code"></a>TVN \_ ItemChanging-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass sich Element Attribute ändern. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmtvitemchange**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) -Struktur, die das geänderte Element beschreibt. Der **uchanged** -Member ist auf den tvif-Status festgelegt \_ .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **false** zurück, um die Änderung zu akzeptieren, oder **true** , um die Änderung zu verhindern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ Itemchangingw** (Unicode) und **TVN \_ itemchanginga** (ANSI)<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TVN \_ ItemChanged](tvn-itemchanged.md)
</dt> </dl>

 

 





