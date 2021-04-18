---
title: Tasksettings. allowdemandstart (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task entweder mit dem Befehl ausführen oder mit dem Kontextmenü gestartet werden kann, oder legt diesen fest.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Allowdemandstart-Eigenschaft Taskplaner
- Allowdemandstart-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, allowdemandstart-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391628"
---
# <a name="tasksettingsallowdemandstart-property"></a>Tasksettings. allowdemandstart (Eigenschaft)

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task entweder mit dem Befehl ausführen oder mit dem Kontextmenü gestartet werden kann, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass der Task mithilfe des Befehls ausführen oder des Kontextmenüs ausgeführt werden kann. Wenn der Wert false ist, kann der Task nicht mit dem Befehl ausführen oder dem Kontextmenü ausgeführt werden. Der Standardwert ist True.

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft auf true festgelegt ist, kann der Task unabhängig von gestartet werden, wenn ein Trigger den Task startet.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [allowstartondemand](taskschedulerschema-allowstartondemand-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





