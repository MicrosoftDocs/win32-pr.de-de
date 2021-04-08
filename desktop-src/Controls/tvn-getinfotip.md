---
title: TVN_GETINFOTIP Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Strukturansicht-Steuerelement gesendet, das über den infotip-Stil des Fernsehsystems verfügt \_ . Dieser Benachrichtigungs Code wird gesendet, wenn das Steuerelement zusätzliche Textinformationen anfordert, die in einer QuickInfo angezeigt werden sollen. Der Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- Windows-Steuerelemente für TVN_GETINFOTIP Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742256"
---
# <a name="tvn_getinfotip-notification-code"></a>TVN \_ getinfotip-Benachrichtigungs Code

Wird von einem Strukturansicht-Steuerelement gesendet, das über den [**\_ infotip**](tree-view-control-window-styles.md) -Stil des Fernsehsystems verfügt. Dieser Benachrichtigungs Code wird gesendet, wenn das Steuerelement zusätzliche Textinformationen anfordert, die in einer QuickInfo angezeigt werden sollen. Der Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtvgetinfotip**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Das-Steuerelement ignoriert den Rückgabewert für diesen Benachrichtigungs Code.

## <a name="remarks"></a>Bemerkungen

Dieser Benachrichtigungs Code wird nur von Strukturansicht-Steuerelementen gesendet, die über den [**\_ infotip**](tree-view-control-window-styles.md) -Stil "TV" verfügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ Getinfotipw** (Unicode) und **TVN \_ getinfotipa** (ANSI)<br/>             |



 

 





