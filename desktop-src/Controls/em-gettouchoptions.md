---
title: EM_GETTOUCHOPTIONS Nachricht (Richedit.h)
description: Ruft die Touchoptionen ab, die einem Rich-Edit-Steuerelement zugeordnet sind.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- EM_GETTOUCHOPTIONS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4771cd11fd8aaf16925c97a3242918ba8f7b56e4e580a6f3cd70672a134399b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799990"
---
# <a name="em_gettouchoptions-message"></a>EM \_ GETTOUCHOPTIONS-Nachricht

Ruft die Touchoptionen ab, die einem Rich-Edit-Steuerelement zugeordnet sind.


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die abzurufende Toucheingabeoption. Dieses Argument einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                        | Bedeutung                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ SHOWHANDLES**</dt> </dl>          | Ruft ab, ob die Toucheingaben sichtbar sind.<br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ DISABLEHANDLES**</dt> </dl> | Das Abrufen dieses Flags ist nicht implementiert.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert der vom *wParam-Parameter* angegebenen Option zurück. Er ist ungleich 0 (null), wenn *wParam* **RTO \_ SHOWHANDLES** ist und die Touch-Zierer sichtbar sind, andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ SETTOUCHOPTIONS**](em-settouchoptions.md)
</dt> </dl>

 

 





