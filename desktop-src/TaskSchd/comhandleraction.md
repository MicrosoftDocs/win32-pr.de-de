---
title: ComHandlerAction-Objekt
description: Skripterstellungsobjekt, das eine Aktion darstellt, die einen Handler ausspricht.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- COM-Handleraktion Taskplaner , Objekt
- ComHandlerAction-Taskplaner
- ComHandlerAction-Objekt Taskplaner , beschrieben
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
ms.openlocfilehash: 7dd803d67d292df22e651e4393880038835c862e0e81dde19e0d0a7e15fccd32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659680"
---
# <a name="comhandleraction-object"></a>ComHandlerAction-Objekt

Skripterstellungsobjekt, das eine Aktion darstellt, die einen Handler ausspricht.

## <a name="members"></a>Member

Das **ComHandlerAction-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **ComHandlerAction-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                               | Zugriffstyp           | Beschreibung                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Classid**](comhandleraction-classid.md)<br/> | Lesen/Schreiben<br/> | Ruft den Bezeichner der Handlerklasse ab oder legt den Bezeichner fest.<br/>                                              |
| [**Daten**](comhandleraction-data.md)<br/>       | Lesen/Schreiben<br/> | Ruft zusätzliche Daten ab, die dem Handler zugeordnet sind, oder legt diese fest.<br/>                              |
| [**Id**](action-id.md)<br/>                     | Lesen/Schreiben<br/> | Geerbt vom [**Action-Objekt.**](action.md) Ruft den Bezeichner der Aktion ab oder legt den Bezeichner fest.<br/> |
| [**Typ**](action-type.md)<br/>                 | Schreibgeschützt<br/>  | Geerbt vom [**Action-Objekt.**](action.md) Ruft den Typ der Aktion ab.<br/>               |



 

## <a name="remarks"></a>Hinweise

COM-Handler müssen die [**ITaskHandler-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) implementieren, damit Taskplaner handler starten und beenden kann. Im Gegenzug verwendet der COM-Handler die Methoden des [**TaskHandlerStatus-Objekts,**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) um den Status an die Taskplaner.

Beim Lesen oder Schreiben von XML wird eine COM-Handleraktion im [**ComHandler-Element**](taskschedulerschema-comhandler-actiongroup-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[Taskplaner Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





