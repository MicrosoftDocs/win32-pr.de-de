---
title: RBN_CHEVRONPUSHED Benachrichtigungscode (Commctrl.h)
description: Wird von einem Rebar-Steuerelement gesendet, wenn ein Chevron gepusht wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- RBN_CHEVRONPUSHED Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f5f8d52558251524e9d978c52ae703565a9641febdd53190925cfb8b127160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985320"
---
# <a name="rbn_chevronpushed-notification-code"></a>\_RBN-CHEVRONPUSHED-Benachrichtigungscode

Wird von einem Rebar-Steuerelement gesendet, wenn ein Chevron gepusht wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf die [**NMREBARCHEVRON-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) des Bands.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Wenn eine Anwendung diesen Benachrichtigungscode empfängt, ist sie für die Anzeige eines Popupmenüs mit Elementen für jedes ausgeblendete Tool verantwortlich. Verwenden Sie den **rc-Member** der [**NMREBARCHEVRON-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) um die richtige Position für das Popupmenü zu finden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





