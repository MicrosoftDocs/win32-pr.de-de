---
title: Idlesettings-Objekt
description: Skript Objekt, das angibt, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Idlesettings-Objekt Taskplaner
- Idlesettings-Objekt Taskplaner, beschrieben
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
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391766"
---
# <a name="idlesettings-object"></a>Idlesettings-Objekt

Ein Skript Objekt, das angibt, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet. Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).

## <a name="members"></a>Member

Das **idlesettings** -Objekt verfügt über folgende Typen von Membern:

- [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **idlesettings** -Objekt verfügt über diese Eigenschaften.

> [!NOTE]
> Die Einstellungen *idleduration* und *WaitTimeout* sind veraltet. Sie sind weiterhin in der Taskplaner-Benutzeroberfläche vorhanden, und ihre Schnittstellen Methoden geben möglicherweise weiterhin gültige Werte zurück, aber Sie werden nicht mehr verwendet.

| Eigenschaft                                                       | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Neustartondle**](idlesettings-restartonidle.md)<br/> | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt, oder legt diesen fest.<br/>            |
| [**Stoponidleend**](idlesettings-stoponidleend.md)<br/> | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe beendet, wenn die Leerlauf Bedingung endet, bevor die Aufgabe abgeschlossen wird, oder legt diesen fest.<br/> |
| **Veraltet**: [ **idleduration**](idlesettings-idleduration.md)<br/>   | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird, oder legt ihn fest.<br/>                            |
| **Veraltet**: [ **WaitTimeout**](idlesettings-waittimeout.md)<br/>     | Lesen/Schreiben<br/> | Ruft einen Wert ab oder legt einen Wert fest, der die Zeitspanne angibt, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet.<br/>                             |

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**idlesettings**](taskschedulerschema-idlesettings-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.

Wenn eine Aufgabe durch einen Leerlauf Trigger ausgelöst wird, wird die [**idlesettings. WaitTimeout**](idlesettings-waittimeout.md) -Eigenschaft ignoriert.

> [!NOTE]
> *Idlesettings. idleduration* und *idlesettings. WaitTimeout* sind veraltet.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[Taskplaner Objekte](task-scheduler-objects.md)

[Aufgabenplanung](task-scheduler-start-page.md)
