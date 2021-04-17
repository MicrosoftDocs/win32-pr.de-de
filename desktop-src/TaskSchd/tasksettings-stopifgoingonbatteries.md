---
title: Tasksettings. stopifgoingonakkus (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab oder legt diesen fest, der angibt, dass der Task angehalten wird, wenn der Computer auf dem Gerät ausgeführt wird.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Stopifgoingonakkus-Eigenschaft Taskplaner
- Stopifgoingonakkus-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, stopifgoingonakkus (Eigenschaft)
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aced436d653b6bbc02b4b36edea9046e3ac62392
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478354"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a>Tasksettings. stopifgoingonakkus (Eigenschaft)

Ruft bei der Skripterstellung einen booleschen Wert ab oder legt diesen fest, der angibt, dass der Task angehalten wird, wenn der Computer auf dem Gerät ausgeführt wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Ein boolescher Wert, der angibt, dass der Task angehalten wird, wenn der Computer in den Akku Betrieb geht. Wenn der Wert true ist, gibt die Eigenschaft an, dass der Task beendet wird, wenn der Computer auf die Batterie geht. Wenn der Wert false ist, gibt die Eigenschaft an, dass die Aufgabe nicht angehalten wird, wenn der Computer auf die Batterie geht. Der Standardwert ist True. Weitere Informationen finden Sie unter "Hinweise".

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**stopifgoingonakkus**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





