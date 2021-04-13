---
title: Aktions Objekt
description: Skript Objekt, das die allgemeinen Eigenschaften bereitstellt, die von allen Aktions Objekten geerbt werden.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Aktions Objekt Taskplaner
- Taskplaner des Aktions Objekts, beschrieben
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
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518239"
---
# <a name="action-object"></a>Aktions Objekt

Skript Objekt, das die allgemeinen Eigenschaften bereitstellt, die von allen Aktions Objekten geerbt werden. Ein Aktions Objekt wird von der [**Action Collection. Create**](actioncollection-create.md) -Methode erstellt.

## <a name="members"></a>Member

Das **Aktions** Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Aktions** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                               | Zugriffstyp           | BESCHREIBUNG                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [**Name**](action-id.md)<br/>     | Lesen/Schreiben<br/> | Ruft den Bezeichner der Aktion ab oder legt ihn fest.<br/> |
| [**type**](action-type.md)<br/> | Schreibgeschützt<br/>  | Ruft den Typ der Aktion ab.<br/>               |



 

## <a name="remarks"></a>Bemerkungen

Informationen zur Zusammenarbeit von Aktionen und Aufgaben finden Sie unter [Aufgaben Aktionen](task-actions.md). Die folgende Tabelle enthält die Skript Objekte, die die Aktionen darstellen, die ausgeführt werden können:



| API                                            | BESCHREIBUNG                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**Comhandleraction**](comhandleraction.md)   | Stellt eine Aktion dar, die einen Handler auslöst.                   |
| [**Execaction**](execaction.md)               | Stellt eine Aktion dar, die einen Befehlszeilen Vorgang ausführt. |
| [**Emailaction**](emailaction.md)             | Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.            |
| [**Showmessageaction**](showmessageaction.md) | Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.               |



 

Beim Lesen oder Schreiben von XML werden die Aktionen einer Aufgabe im [**Actions**](taskschedulerschema-actions-tasktype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md) , [Ereignis auslöserbeispiel (Skripterstellung)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Beispiel für den täglichen Auslösung [(Skripterstellung)](daily-trigger-example--scripting-.md), Registrierungs- [auslöserbeispiel (Skripterstellung)](registration-trigger-example--scripting-.md), Beispiel für einen wöchentlichen Aufruf [(](weekly-trigger-example--scripting-.md)Skripterstellung), Beispiel für LOGON-Beispiel [(Skript](logon-trigger-example--scripting-.md)Erstellung) oder [Beispiel](boot-trigger-example--scripting-.md)für

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skript Objekte Taskplaner](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





