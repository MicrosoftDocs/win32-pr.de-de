---
title: TBN_INITCUSTOMIZE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Anpassung gestartet wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- Windows-Steuerelemente für TBN_INITCUSTOMIZE Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338319"
---
# <a name="tbn_initcustomize-notification-code"></a>TBN \_ initcustomize-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Anpassung gestartet wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf die [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur der Symbolleiste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt tbnrf \_ hidehelp zurück, um die Schaltfläche Hilfe zu unterdrücken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





