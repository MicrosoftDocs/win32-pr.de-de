---
title: Weeklyauslöst. randomdelay-Eigenschaft
description: Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest. | Weeklyauslöst. randomdelay-Eigenschaft
ms.assetid: 711b188d-b283-4c99-b43d-644f39a31cdc
keywords:
- Randomdelay-Eigenschaft Taskplaner
- Randomdelay-Eigenschaft Taskplaner, weeklyauslöserobjekt
- Weeklyauslöserobjekt Taskplaner, randomdelay-Eigenschaft
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
ms.openlocfilehash: e3a7d955956c119244a5b92a1ee0d81cd5add9b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365064"
---
# <a name="weeklytriggerrandomdelay-property"></a>Weeklyauslöst. randomdelay-Eigenschaft

Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.RandomDelay As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Verzögerungszeit, die der Startzeit des Auslösers nach dem Zufallsprinzip hinzugefügt wird. Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S (z. b. P2DT5S ist eine Verzögerung von 2 Tagen, 5 Sekunden).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





