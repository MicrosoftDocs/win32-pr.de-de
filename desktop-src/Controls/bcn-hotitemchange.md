---
title: BCN_HOTITEMCHANGE Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt den Besitzer des Schaltflächensteuerfelds, dass die Maus in den Clientbereich des Schaltflächen-Steuerelements eintritt oder diesen verlässt. Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungscode in Form einer WM \_ NOTIFY-Nachricht.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- BCN_HOTITEMCHANGE Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6966978dc1d1eee1d84a9e5caa51116ccb96e098d2c196ea143051663abbf4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921370"
---
# <a name="bcn_hotitemchange-notification-code"></a>BCN \_ HOTITEMCHANGE-Benachrichtigungscode

Benachrichtigt den Besitzer des Schaltflächensteuerfelds, dass die Maus in den Clientbereich des Schaltflächen-Steuerelements eintritt oder diesen verlässt. Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungscode in Form einer [**WM \_ NOTIFY-Nachricht.**](wm-notify.md)


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMBCHOTITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diesen Benachrichtigungscode verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





