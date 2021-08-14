---
title: actionGroup Group
description: Definiert die Gruppe von Aktionen, die eine Aufgabe ausführen kann.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- actionGroup-Taskplaner
- actionGroup Taskplaner
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcfd37187373e8bebdcc6b2af22323fd5475a6893791158b83b16c278752e420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357177"
---
# <a name="actiongroup-group"></a>actionGroup Group

Definiert die Gruppe von Aktionen, die eine Aufgabe ausführen kann.

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
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | Stellt eine Aktion dar, die einen Handler ausspricht.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | Stellt eine Aktion dar, die einen Befehlszeilenvorgang ausgeführt.<br/> |
| [**Sendemail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Stellt eine Aktion dar, die eine E-Mail sendet.<br/>            |
| [**Showmessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Stellt eine Aktion dar, die ein Meldungsfeld zeigt.<br/>               |



## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML sind die von dieser Gruppe definierten Elemente die untergeordneten Elemente des [**Actions-Elements.**](taskschedulerschema-actions-tasktype-element.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





