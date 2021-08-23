---
title: TriggerCollection-Objekt (Windows.ui.xaml.h)
description: Skripterstellungsobjekt, das zum Hinzufügen, Entfernen aus und Abrufen der Trigger einer Aufgabe verwendet wird.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- triggers Taskplaner , trigger collection object
- TriggerCollection-Taskplaner
- TriggerCollection-Taskplaner , beschrieben
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
ms.openlocfilehash: c7fd103918bc3898e56a3041221c9c70c9ede9aea5df4843cd984f2502279014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001938"
---
# <a name="triggercollection-object"></a>TriggerCollection-Objekt

Skripterstellungsobjekt, das zum Hinzufügen, Entfernen aus und Abrufen der Trigger einer Aufgabe verwendet wird.

## <a name="members"></a>Member

Das **TriggerCollection-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **TriggerCollection-Objekt** verfügt über diese Methoden.



| Methode                                     | Beschreibung                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Klar**](triggercollection-clear.md)   | Entfernt alle Trigger aus der Auflistung.<br/>                                        |
| [**Erstellen**](triggercollection-create.md) | Erstellt einen neuen Trigger für die Aufgabe.<br/>                                             |
| [**Entfernen**](triggercollection-remove.md) | Entfernt den angegebenen Trigger aus der Auflistung von Triggern, die vom Task verwendet werden.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **TriggerCollection-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp          | Beschreibung                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Anzahl**](triggercollection-count.md)<br/> | Schreibgeschützt<br/> | Ruft die Anzahl der Trigger in der Auflistung ab.<br/>  |
| [**Element**](triggercollection-item.md)<br/>   | Schreibgeschützt<br/> | Ruft den angegebenen Trigger aus der Auflistung ab.<br/> |



 

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Trigger für die Aufgabe im [**Triggers-Element**](taskschedulerschema-triggers-tasktype-element.md) des Taskplaner angegeben.

Informationen zu den einzelnen Triggertypen finden Sie unter [Triggertypen.](trigger-types.md)

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Time Trigger Example (Scripting) .](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Windows.ui.xaml.h</dt> </dl> |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Trigger**](trigger.md)
</dt> </dl>

 

 





