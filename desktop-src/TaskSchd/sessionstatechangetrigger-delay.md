---
title: Sessionstatechangeauslöst. Delay (Eigenschaft)
description: Ruft bei der Skripterstellung einen Wert ab, der angibt, wie lange eine Verzögerung stattfindet, bevor eine Aufgabe gestartet wird, nachdem eine Terminal Server-Sitzungs Zustandsänderung erkannt wurde, oder legt diesen Wert fest.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Verzögerte Eigenschaften Taskplaner
- Delay-Eigenschaft Taskplaner, sessionstatechange-Objekt
- Sessionstatechange-Objekt Taskplaner, Delay-Eigenschaft
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103190"
---
# <a name="sessionstatechangetriggerdelay-property"></a>Sessionstatechangeauslöst. Delay (Eigenschaft)

Ruft bei der Skripterstellung einen Wert ab, der angibt, wie lange eine Verzögerung stattfindet, bevor eine Aufgabe gestartet wird, nachdem eine Terminal Server-Sitzungs Zustandsänderung erkannt wurde, oder legt diesen Wert fest. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z

## <a name="syntax"></a>Syntax


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Verzögerung, die durchgeführt wird, bevor ein Task gestartet wird, nachdem eine Terminal Server-Sitzungs Zustandsänderung erkannt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





