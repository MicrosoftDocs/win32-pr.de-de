---
title: ActionCollection-Objekt
description: Skriptobjekt, das die von der Aufgabe ausgeführten Aktionen enthält.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- Aktionen Taskplaner , Sammlungsobjekt
- ActionCollection-Objekt Taskplaner
- ActionCollection-Objekt Taskplaner beschrieben
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5356757d232570a31f5c8d05e01b695f130a33e34c1c0e98689b1c74feba40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011720"
---
# <a name="actioncollection-object"></a>ActionCollection-Objekt

Skriptobjekt, das die von der Aufgabe ausgeführten Aktionen enthält.

## <a name="members"></a>Member

Das **ActionCollection-Objekt** weist diese Typen von Membern auf:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **ActionCollection-Objekt** verfügt über diese Methoden.



| Methode                                    | BESCHREIBUNG                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [**Klar**](actioncollection-clear.md)   | Löscht alle Aktionen aus der Auflistung.<br/>      |
| [**Erstellen**](actioncollection-create.md) | Erstellt eine neue Aktion und fügt sie der Auflistung hinzu.<br/> |
| [**Entfernen**](actioncollection-remove.md) | Entfernt eine angegebene Aktion aus der Auflistung.<br/>  |



 

### <a name="properties"></a>Eigenschaften

Das **ActionCollection-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                               | Zugriffstyp           | BESCHREIBUNG                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Kontext**](actioncollection-context.md)<br/> | Lesen/Schreiben<br/> | Ruft den Bezeichner des Prinzipals für die Aufgabe ab oder legt den Bezeichner fest.<br/> |
| [**Anzahl**](actioncollection-count.md)<br/>     | Schreibgeschützt<br/>  | Ruft die Anzahl der Aktionen in der Auflistung ab.<br/>              |
| [**Element**](actioncollection-item.md)<br/>       | Schreibgeschützt<br/>  | Ruft eine angegebene Aktion aus der Auflistung ab.<br/>               |
| [**Xmltext**](actioncollection-xmltext.md)<br/> | Lesen/Schreiben<br/> | Ruft eine XML-formatierte Version der Auflistung ab oder legt diese fest.<br/>   |



 

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML werden die Aktionen einer Aufgabe im [**Actions-Element**](taskschedulerschema-actions-tasktype-element.md) des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Time Trigger Example (Scripting),](time-trigger-example--scripting-.md) [Event Trigger Example (Scripting) ,](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))Daily Trigger Example [(Scripting),](daily-trigger-example--scripting-.md) [Registration Trigger Example (Scripting),](registration-trigger-example--scripting-.md) [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md)oder [Boot Trigger Example (Scripting) (Beispiel für Starttrigger (Skripterstellung)).](boot-trigger-example--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





