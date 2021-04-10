---
title: TriggerCollection-Objekt (Windows. UI. XAML. h)
description: Skript Objekt, das zum Hinzufügen, entfernen und Abrufen der Trigger einer Aufgabe verwendet wird.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- Trigger Taskplaner, triggerauflistungs Objekt
- TriggerCollection-Objekt Taskplaner
- TriggerCollection-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103274"
---
# <a name="triggercollection-object"></a>TriggerCollection-Objekt

Skript Objekt, das zum Hinzufügen, entfernen und Abrufen der Trigger einer Aufgabe verwendet wird.

## <a name="members"></a>Member

Das **TriggerCollection** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **TriggerCollection** -Objekt verfügt über diese Methoden.



| Methode                                     | BESCHREIBUNG                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Klartext**](triggercollection-clear.md)   | Löscht alle Trigger aus der Auflistung.<br/>                                        |
| [**Stelle**](triggercollection-create.md) | Erstellt einen neuen-Auslösers für die Aufgabe.<br/>                                             |
| [**Aufgeh**](triggercollection-remove.md) | Entfernt den angegebenen Trigger aus der Auflistung von Triggern, die vom Task verwendet werden.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **TriggerCollection** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp          | BESCHREIBUNG                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Countdown**](triggercollection-count.md)<br/> | Schreibgeschützt<br/> | Ruft die Anzahl der Trigger in der-Auflistung ab.<br/>  |
| [**Element**](triggercollection-item.md)<br/>   | Schreibgeschützt<br/> | Ruft den angegebenen-Auslösers aus der Auflistung ab.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Trigger für die Aufgabe im [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) -Element des Taskplaner Schemas angegeben.

Informationen zu den einzelnen Auslösertypen finden Sie unter [Auslösertypen](trigger-types.md)

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Windows. UI. XAML. h</dt> </dl> |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Trigger**](trigger.md)
</dt> </dl>

 

 





