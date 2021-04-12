---
title: Aktions Sammlungsobjekt
description: Skript Objekt, das die von der Aufgabe ausgeführten Aktionen enthält.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- Aktionen Taskplaner, Sammlungsobjekt
- Aktions Sammlungsobjekt Taskplaner
- Taskplaner des Aktions Sammlungs Objekts, beschrieben
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
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519143"
---
# <a name="actioncollection-object"></a>Aktions Sammlungsobjekt

Skript Objekt, das die von der Aufgabe ausgeführten Aktionen enthält.

## <a name="members"></a>Member

Das Objekt " **Aktions Sammlung** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das Objekt " **Aktions Sammlung** " verfügt über diese Methoden.



| Methode                                    | BESCHREIBUNG                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [**Klartext**](actioncollection-clear.md)   | Löscht alle Aktionen aus der Auflistung.<br/>      |
| [**Stelle**](actioncollection-create.md) | Erstellt eine neue Aktion und fügt Sie der Auflistung hinzu.<br/> |
| [**Aufgeh**](actioncollection-remove.md) | Entfernt eine angegebene Aktion aus der Auflistung.<br/>  |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **Aktions Sammlung** " verfügt über diese Eigenschaften.



| Eigenschaft                                               | Zugriffstyp           | BESCHREIBUNG                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Kontext**](actioncollection-context.md)<br/> | Lesen/Schreiben<br/> | Ruft den Bezeichner des Prinzipals für den Task ab oder legt ihn fest.<br/> |
| [**Countdown**](actioncollection-count.md)<br/>     | Schreibgeschützt<br/>  | Ruft die Anzahl von Aktionen in der Auflistung ab.<br/>              |
| [**Element**](actioncollection-item.md)<br/>       | Schreibgeschützt<br/>  | Ruft eine angegebene Aktion aus der Auflistung ab.<br/>               |
| [**XmlText**](actioncollection-xmltext.md)<br/> | Lesen/Schreiben<br/> | Ruft eine XML-formatierte Version der Auflistung ab oder legt diese fest.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML werden die Aktionen einer Aufgabe im [**Actions**](taskschedulerschema-actions-tasktype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md), [Ereignis auslöserbeispiel (Skripterstellung)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Beispiel für den täglichen Auslösung [(Skripterstellung)](daily-trigger-example--scripting-.md), Registrierungs- [auslöserbeispiel (Skripterstellung)](registration-trigger-example--scripting-.md), Beispiel für einen wöchentlichen Aufruf [(](weekly-trigger-example--scripting-.md)Skripterstellung), Beispiel für LOGON-Beispiel [(Skript](logon-trigger-example--scripting-.md)Erstellung) oder [Beispiel](boot-trigger-example--scripting-.md)für

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





