---
title: LVN_GETINFOTIP Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement mit einer großen Symbol Ansicht gesendet, das über den erweiterten LVS- \_ \_ infotip-Stil verfügt.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- Windows-Steuerelemente für LVN_GETINFOTIP Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519327"
---
# <a name="lvn_getinfotip-notification-code"></a>LVN \_ getinfotip-Benachrichtigungs Code

Wird von einem Listenansicht-Steuerelement mit einer großen Symbol Ansicht gesendet, das über den erweiterten [**LVS- \_ \_ infotip**](extended-list-view-styles.md) -Stil verfügt. Dieser Benachrichtigungs Code wird gesendet, wenn das Listenansicht-Steuerelement zusätzliche Textinformationen anfordert, die in einer QuickInfo angezeigt werden sollen. Sie wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmlvgetinfotip**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Dieser Benachrichtigungs Code wird nur von Listenansicht-Steuerelementen gesendet, die über die erweiterte [**LVS- \_ \_ infotip**](extended-list-view-styles.md) -Art verfügen. Der LVN \_ getinfotip-Benachrichtigungs Code wird nur für Unterelement 0 gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVN \_ Getinfotipw** (Unicode) und **LVN \_ getinfotipa** (ANSI)<br/>             |



 

 





