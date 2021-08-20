---
title: TTN_LINKCLICK Benachrichtigungscode (Commctrl.h)
description: Wird gesendet, wenn auf einen Textlink in einer Sprechblasen-QuickInfo geklickt wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a31b1f942627ee22fb050bbddd0b74ac10dd09a7a8f14018189620f6c8155f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166096"
---
# <a name="ttn_linkclick-notification-code"></a>TTN \_ LINKCLICK-Benachrichtigungscode

Wird gesendet, wenn auf einen Textlink in einer Sprechblasen-QuickInfo geklickt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a>Parameter

Dieser Benachrichtigungscode enthält keine Parameter.

## <a name="return-value"></a>Rückgabewert

Rückgabewert nicht verwendet.

## <a name="remarks"></a>Hinweise

Es folgt ein Beispiel für das Senden dieser Benachrichtigung. Angenommen, ihre QuickInfo für die Sprechblase enthält den folgenden Text: "This is a <A>link".</A> Wenn auf "Link" geklickt wird, sendet das QuickInfo-Steuerelement einen TTN \_ LINKCLICK-Benachrichtigungscode.

> [!Note]  
> Um diesen Benachrichtigungscode verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





