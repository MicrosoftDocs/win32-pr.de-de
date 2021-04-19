---
title: Dailyauslöst. randomdelay (Eigenschaft)
description: Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest. | Dailyauslöst. randomdelay (Eigenschaft)
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- Randomdelay-Eigenschaft Taskplaner
- Randomdelay-Eigenschaft Taskplaner, dailyauslöserobjekt
- Dailyauslöserobjekt Taskplaner, randomdelay-Eigenschaft
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd24fc5bd97a51cc0276e0fdfe800c0a9baa022a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355766"
---
# <a name="dailytriggerrandomdelay-property"></a>Dailyauslöst. randomdelay (Eigenschaft)

Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
DailyTrigger.RandomDelay As String
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dailylöst**](dailytrigger.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





