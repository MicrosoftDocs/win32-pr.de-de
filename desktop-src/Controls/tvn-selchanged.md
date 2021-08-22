---
title: TVN_SELCHANGED Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements, dass sich die Auswahl von einem Element in ein anderes geändert hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7708d797edebc8c2c0bf43b910aec4dc0a1d6ece1a8a535fdcac57e6b15d6e04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957779"
---
# <a name="tvn_selchanged-notification-code"></a>TVN \_ SELCHANGED-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements, dass sich die Auswahl von einem Element in ein anderes geändert hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTREEVIEW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Die **Elemente itemOld** und **itemNew** der **NMTREEVIEW-Struktur** sind [**TVITEM-Strukturen,**](/windows/win32/api/commctrl/ns-commctrl-tvitema) die Informationen über das zuvor ausgewählte Element und das neu ausgewählte Element enthalten. Nur die Elemente **mask**, **hItem,** **state** und **lParam** dieser Strukturen sind gültig. Die **stateMask-Member** der **TVITEM-Strukturen,** die von **itemOld** und **itemNew** angegeben werden, sind bei der Eingabe nicht definiert. Der **Aktionsmember** der **NMTREEVIEW-Struktur** gibt den Aktionstyp an, der die Änderung der Auswahl verursacht hat. Es kann sich um einen der folgenden Werte handeln:



| Anforderung | Wert |
|-----------------|-------------------|
| TVC \_ BYKEYBOARD | Durch eine Tastatureingabe.   |
| TVC \_ BYMOUSE    | Mit einem Mausklick. |
| TVC \_ UNKNOWN    | Unbekannt          |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ SELCHANGEDW** (Unicode) und **TVN \_ SELCHANGEDA** (ANSI)<br/>             |



 

 





