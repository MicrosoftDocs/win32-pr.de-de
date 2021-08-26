---
title: NM_DBLCLK Benachrichtigungscode (Registerkarte) (Commctrl.h)
description: Benachrichtigt ein übergeordnetes Fenster eines Registerkartensteuerelements, dass der Benutzer auf die linke Maustaste im Steuerelement doppelklickt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: fd99f195-ceac-47e8-b584-d814b055fa21
keywords:
- NM_DBLCLK -Benachrichtigungscode (Registerkarte) Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c100b266ea0e409b9d48846e81d1a5bf9a07de0c6473800b4f2251942bc94b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919690"
---
# <a name="nm_dblclk-tab-notification-code"></a>NM \_ DBLCLK -Benachrichtigungscode (Registerkarte)

Benachrichtigt ein übergeordnetes Fenster eines Registerkartensteuerelements, dass der Benutzer auf die linke Maustaste im Steuerelement doppelklickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie einen Wert ungleich 0 (null) zurück, um die Standardverarbeitung nicht zuzulassen, oder 0 (null), um die Standardverarbeitung zuzulassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





