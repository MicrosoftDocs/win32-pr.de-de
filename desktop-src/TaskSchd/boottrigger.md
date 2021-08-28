---
title: BootTrigger-Objekt
description: Skriptobjekt, das einen Trigger darstellt, der eine Aufgabe startet, wenn das System gestartet wird.
ms.assetid: 9d5a7cf6-2e1d-44ae-bb45-66424770d61b
keywords:
- Starttrigger Taskplaner , Objekt
- BootTrigger-Objekt Taskplaner
- BootTrigger-Objekt Taskplaner beschrieben
topic_type:
- apiref
api_name:
- BootTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ede15265a0ff492ddb062687c1ca45af77c32fd6319821b1c214b82dce002a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860170"
---
# <a name="boottrigger-object"></a>BootTrigger-Objekt

Skriptobjekt, das einen Trigger darstellt, der eine Aufgabe startet, wenn das System gestartet wird.

## <a name="members"></a>Member

Das **BootTrigger-Objekt** weist diese Typen von Membern auf:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **BootTrigger-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | Beschreibung                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](boottrigger-delay.md)<br/>                       |                       | Ruft einen Wert ab, der die Zeitspanne zwischen dem Start des Systems und dem Start des Tasks angibt, oder legt diesen fest.<br/>                                                           |
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft einen booleschen Wert ab, der angibt, ob der Trigger aktiviert ist, oder legt diesen fest.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft das Datum und die Uhrzeit der Deaktivierung des Triggers ab oder legt diese fest. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft die maximale Zeit ab, die der vom Trigger gestartete Task ausführen darf, oder legt diese fest.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft den Bezeichner für den Trigger ab oder legt den Bezeichner fest.<br/>                                                                               |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft ab oder legt fest, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft das Datum und die Uhrzeit der Aktivierung des Triggers ab oder legt diese fest.<br/>                                                              |
| [**Typ**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft den Typ des Triggers ab.<br/>                                                                                              |



 

## <a name="remarks"></a>Hinweise

Der Taskplaner Dienst wird gestartet, wenn das Betriebssystem gestartet wird, und Starttriggertasks werden so festgelegt, dass sie beim Starten des Taskplaner Diensts gestartet werden.

Nur ein Mitglied der Gruppe Administratoren kann eine Aufgabe mit einem Starttrigger erstellen.

Beim Erstellen eines eigenen XML-Elements für eine Aufgabe wird ein Starttrigger mithilfe des [**BootTrigger-Elements**](taskschedulerschema-boottrigger-triggergroup-element.md) des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Starttriggerbeispiel (Skripterstellung).](boot-trigger-example--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[**Triggercollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





