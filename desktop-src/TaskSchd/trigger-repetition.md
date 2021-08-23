---
title: Trigger.Wiederholungseigenschaft
description: Für die Skripterstellung ruft einen Wert ab, der angibt, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde, oder legt diesen fest.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Wiederholungseigenschaft Taskplaner
- Wiederholungseigenschaft Taskplaner , Triggerobjekt
- Triggerobjekt Taskplaner , Wiederholungseigenschaft
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e14b8dc23b329d9646647fdcc1c5bcb3166c5bf885886a5308c329e186dc51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002108"
---
# <a name="triggerrepetition-property"></a>Trigger.Wiederholungseigenschaft

Für die Skripterstellung ruft einen Wert ab, der angibt, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**RepetitionPattern-Objekt,**](repetitionpattern.md) das definiert, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe wird das Wiederholungsmuster für einen Trigger im [**Wiederholungselement**](taskschedulerschema-repetition-triggerbasetype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Wiederholungspattern**](repetitionpattern.md)
</dt> </dl>

 

 





