---
title: Aktionsobjekt
description: Skriptobjekt, das die allgemeinen Eigenschaften bereitstellt, die von allen Aktionsobjekten geerbt werden.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Aktionsobjekt Taskplaner
- Aktionsobjekt Taskplaner beschrieben
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b9f41521f1af8b4601faafce9674277b172ad4cde3f364fc2ab7a84cfcc0df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739040"
---
# <a name="action-object"></a>Aktionsobjekt

Skriptobjekt, das die allgemeinen Eigenschaften bereitstellt, die von allen Aktionsobjekten geerbt werden. Ein Aktionsobjekt wird von der [**ActionCollection.Create-Methode**](actioncollection-create.md) erstellt.

## <a name="members"></a>Member

Das **Action-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Action-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                               | Zugriffstyp           | Beschreibung                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [**Id**](action-id.md)<br/>     | Lesen/Schreiben<br/> | Ruft den Bezeichner der Aktion ab oder legt den Bezeichner fest.<br/> |
| [**type**](action-type.md)<br/> | Schreibgeschützt<br/>  | Ruft den Typ der Aktion ab.<br/>               |



 

## <a name="remarks"></a>Hinweise

Informationen dazu, wie Aktionen und Aufgaben zusammenarbeiten, finden Sie unter [Aufgabenaktionen.](task-actions.md) Die folgende Tabelle enthält die Skriptobjekte, die die Aktionen darstellen, die ausgeführt werden können:



| API                                            | Beschreibung                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**ComHandlerAction**](comhandleraction.md)   | Stellt eine Aktion dar, die einen Handler ausgelöst.                   |
| [**ExecAction**](execaction.md)               | Stellt eine Aktion dar, die einen Befehlszeilenvorgang ausführt. |
| [**EmailAction**](emailaction.md)             | Stellt eine Aktion dar, die eine E-Mail sendet.            |
| [**ShowMessageAction**](showmessageaction.md) | Stellt eine Aktion dar, die ein Meldungsfeld anzeigt.               |



 

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Scripting Objects](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





