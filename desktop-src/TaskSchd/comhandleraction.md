---
title: Comhandleraction-Objekt
description: Skript Objekt, das eine Aktion darstellt, die einen Handler auslöst.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- COM-handleraktion Taskplaner, Objekt
- Comhandleraction-Objekt Taskplaner
- Comhandleraction-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d7e8371deda260c407682181fd31e29886b777
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475045"
---
# <a name="comhandleraction-object"></a>Comhandleraction-Objekt

Skript Objekt, das eine Aktion darstellt, die einen Handler auslöst.

## <a name="members"></a>Member

Das **comhandleraction** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **comhandleraction** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                               | Zugriffstyp           | BESCHREIBUNG                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**ClassID**](comhandleraction-classid.md)<br/> | Lesen/Schreiben<br/> | Ruft den Bezeichner der Handlerklasse ab oder legt ihn fest.<br/>                                              |
| [**Daten**](comhandleraction-data.md)<br/>       | Lesen/Schreiben<br/> | Ruft zusätzliche Daten ab, die dem Handler zugeordnet sind, oder legt diese fest.<br/>                              |
| [**Name**](action-id.md)<br/>                     | Lesen/Schreiben<br/> | Wird vom [**Action**](action.md) -Objekt geerbt. Ruft den Bezeichner der Aktion ab oder legt ihn fest.<br/> |
| [**type**](action-type.md)<br/>                 | Schreibgeschützt<br/>  | Wird vom [**Action**](action.md) -Objekt geerbt. Ruft den Typ der Aktion ab.<br/>               |



 

## <a name="remarks"></a>Bemerkungen

COM-Handler müssen die [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) -Schnittstelle für das Taskplaner implementieren, um den Handler zu starten und anzuhalten. Der com-Handler verwendet wiederum die Methoden des [**taskhandlerstatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) -Objekts, um den Status zurück an den Taskplaner zu übermitteln.

Beim Lesen oder Schreiben von XML wird eine com-handleraktion im [**comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Taskhandlerstatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[Taskplaner Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





