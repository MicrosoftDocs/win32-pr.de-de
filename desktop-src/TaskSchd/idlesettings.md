---
title: IdleSettings-Objekt
description: Skriptobjekt, das angibt, wie der Taskplaner Aufgaben ausführt, wenn sich der Computer in einem Leerlaufzustand befindet.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- IdleSettings-Objekt Taskplaner
- IdleSettings-Objekt Taskplaner beschrieben
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7597f2232d95d6ddd5f8001be8cf88178ccf5dacd3694c2a8e179d371e54c898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659600"
---
# <a name="idlesettings-object"></a>IdleSettings-Objekt

Ein Skriptobjekt, das angibt, wie der Taskplaner Aufgaben ausführt, wenn sich der Computer in einer Leerlaufbedingung befindet. Informationen zu Leerlaufbedingungen finden Sie unter [Leerlaufbedingungen für Aufgaben.](task-idle-conditions.md)

## <a name="members"></a>Member

Das **IdleSettings-Objekt** verfügt über diese Typen von Membern:

- [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **IdleSettings-Objekt** verfügt über diese Eigenschaften.

> [!NOTE]
> Die Einstellungen *IdleDuration* und *WaitTimeout* sind veraltet. Sie sind weiterhin in der Taskplaner Benutzeroberfläche vorhanden, und ihre Schnittstellenmethoden geben möglicherweise weiterhin gültige Werte zurück, werden jedoch nicht mehr verwendet.

| Eigenschaft                                                       | Zugriffstyp           | Beschreibung                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](idlesettings-restartonidle.md)<br/> | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, ob der Task neu gestartet wird, wenn der Computer mehrfach in eine Leerlaufbedingung übergeht, oder legt diesen fest.<br/>            |
| [**StopOnIdleEnd**](idlesettings-stoponidleend.md)<br/> | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe beendet, wenn die Leerlaufbedingung beendet wird, bevor der Task abgeschlossen wird, oder legt diesen fest.<br/> |
| **Veraltet:** [ **IdleDuration**](idlesettings-idleduration.md)<br/>   | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird, oder legt diesen fest.<br/>                            |
| **Veraltet:** [ **WaitTimeout**](idlesettings-waittimeout.md)<br/>     | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, wie lange der Taskplaner auf das Auftreten einer Leerlaufbedingung wartet, oder legt diesen fest.<br/>                             |

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**IdleSettings-Element**](taskschedulerschema-idlesettings-settingstype-element.md) des Taskplaner Schemas angegeben.

Wenn eine Aufgabe durch einen Leerlauftrigger ausgelöst wird, wird die [**IdleSettings.WaitTimeout-Eigenschaft**](idlesettings-waittimeout.md) ignoriert.

> [!NOTE]
> *IdleSettings.IdleDuration* und *IdleSettings.WaitTimeout* sind veraltet.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[Taskplaner-Objekte](task-scheduler-objects.md)

[Aufgabenplanung](task-scheduler-start-page.md)
