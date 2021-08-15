---
description: Benachrichtigt eine Appbar, dass der Benutzer im Kontextmenü der Taskleiste den Befehl Cascade, Tile Horizontally oder Tile Vertically ausgewählt hat.
title: ABN_WINDOWARRANGE Meldung (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 27c679b7ccdb5eb92ebe87676cd136c71adcda862472f6f300056511001a683a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225021"
---
# <a name="abn_windowarrange-message"></a>ABN \_ WINDOWARRANGE-Meldung

Benachrichtigt eine Appbar, dass der Benutzer im Kontextmenü der Taskleiste den Befehl Cascade, Tile Horizontally oder Tile Vertically ausgewählt hat.


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fBeginning* 
</dt> <dd>

Ein Flag, das angibt, ob der Kaskadierungs- oder Kachelvorgang beginnt. Dieser Parameter ist **TRUE,** wenn der Vorgang beginnt und die Fenster noch nicht verschoben wurden. Der Wert ist **FALSE,** wenn der Vorgang abgeschlossen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Das System sendet diese Benachrichtigungsnachricht zweimal, wobei *lParam* auf **TRUE** und dann *lParam* auf FALSE festgelegt **ist.** Die erste Benachrichtigung wird gesendet, bevor die Fenster kaskadiert oder gekachelt werden, und die zweite wird nach dem Kaskadieren oder Kachelvorgang gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




