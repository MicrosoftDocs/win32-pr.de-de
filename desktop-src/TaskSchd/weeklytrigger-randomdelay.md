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
ms.openlocfilehash: d2b320b0def6f8e9cb0dabff9ff04bdfea3d858e
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734155"
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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





