---
title: Gruppe "Gruppe"
description: Definiert die Gruppe von Aktionen, die von einer Aufgabe durchgeführt werden können.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- Gruppe "Aktionsgruppe" Taskplaner
- Aktionsgruppen Taskplaner
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af06598c6eca092f474467bea16a7d7b95a9563f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740833"
---
# <a name="actiongroup-group"></a>Gruppe "Gruppe"

Definiert die Gruppe von Aktionen, die von einer Aufgabe durchgeführt werden können.

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                    | type                                                                       | BESCHREIBUNG                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comhandlertype**](taskschedulerschema-comhandlertype-complextype.md)   | Stellt eine Aktion dar, die einen Handler auslöst.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**exectype**](taskschedulerschema-exectype-complextype.md)               | Stellt eine Aktion dar, die einen Befehlszeilen Vorgang ausführt.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md)     | Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showmessagetype**](taskschedulerschema-showmessagetype-complextype.md) | Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.<br/>               |



## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML sind die Elemente, die von dieser Gruppe definiert werden, die untergeordneten Elemente des [**Actions**](taskschedulerschema-actions-tasktype-element.md) -Elements.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





