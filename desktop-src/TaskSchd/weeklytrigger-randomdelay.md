---
title: WeeklyTrigger.RandomDelay-Eigenschaft
description: Für die Skripterstellung ruft eine Verzögerungszeit ab, die zufällig zur Startzeit des Triggers hinzugefügt wird, oder legt diese fest. | WeeklyTrigger.RandomDelay-Eigenschaft
ms.assetid: 711b188d-b283-4c99-b43d-644f39a31cdc
keywords:
- RandomDelay-Taskplaner
- RandomDelay-Eigenschaft Taskplaner , WeeklyTrigger-Objekt
- WeeklyTrigger-Objekt Taskplaner , RandomDelay-Eigenschaft
topic_type:
- apiref
api_name:
- WeeklyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc17260b33b4f5ca833ae0f2e322a99205b690ad8d54779ea6471db246cc056b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001778"
---
# <a name="weeklytriggerrandomdelay-property"></a>WeeklyTrigger.RandomDelay-Eigenschaft

Für die Skripterstellung ruft eine Verzögerungszeit ab, die zufällig zur Startzeit des Triggers hinzugefügt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.RandomDelay As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Verzögerungszeit, die zufällig zur Startzeit des Triggers hinzugefügt wird. Das Format für diese Zeichenfolge ist (z. B. `P<days>DT<hours>H<minutes>M<seconds>S` ist P2DT5S eine Verzögerung von 2 Tag, 5 Sekunden).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





