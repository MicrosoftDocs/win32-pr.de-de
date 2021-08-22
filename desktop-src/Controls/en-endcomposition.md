---
title: EN_ENDCOMPOSITION Benachrichtigungscode (Richedit.h)
description: Benachrichtigt ein übergeordnetes Fenster des Rich-Edit-Steuerelements, dass der Benutzer neue Daten eingegeben oder die Eingabe von Daten beendet hat, während er IME oder Textdienstframework.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9fe75910ea018cf9d72dd14696067eb0b2bc00dabd4456cca63e41a099a75d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436849"
---
# <a name="en_endcomposition-notification-code"></a>EN \_ ENDCOMPOSITION-Benachrichtigungscode

Benachrichtigt ein übergeordnetes Fenster des Rich-Edit-Steuerelements, dass der Benutzer neue Daten eingegeben oder die Eingabe von Daten beendet hat, während er IME oder [Textdienstframework.](/windows/desktop/TSF/text-services-framework)


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**ENDCOMPOSITIONNOTIFY-Struktur,**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) die Informationen zur Endkompositionsbedingung empfängt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

