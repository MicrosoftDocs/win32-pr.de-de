---
title: PGN_CALCSIZE Benachrichtigungscode (Commctrl.h)
description: Wird von einem Pagersteuerelement gesendet, um die bildlauffähigen Dimensionen des enthaltenen Fensters abzurufen.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- PGN_CALCSIZE Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c2f6da5153457a871918afea60ac1251496454831a09426f16579ac47342406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078874"
---
# <a name="pgn_calcsize-notification-code"></a>PGN \_ CALCSIZE-Benachrichtigungscode

Wird von einem Pagersteuerelement gesendet, um die bildlauffähigen Dimensionen des enthaltenen Fensters abzurufen. Diese Dimensionen werden vom Pagersteuerelement verwendet, um die bildlauffähige Größe des enthaltenen Fensters zu bestimmen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMPGCALCSIZE-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) die Informationen zum Benachrichtigungscode enthält und empfängt. Das **dwFlag-Element** dieser Struktur gibt an, welche Dimension berechnet wird. Abhängig vom Wert von **dwFlag** sollten Sie die gewünschte Dimension im **iWidth-** oder **iHeight-Element** dieser Struktur platzieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





