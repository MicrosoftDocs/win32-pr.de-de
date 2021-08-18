---
title: multipleInstancesPolicyType Simple Type
description: Definiert die Instanzrichtlinienkonstanten für das Element MultipleInstancesPolicy (settingsType).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- simple type multipleInstancesPolicyType Taskplaner
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e8e847e268486e58bc36bd1bcf9f454b2d8af7b7664d0372613c40c818f932f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758509"
---
# <a name="multipleinstancespolicytype-simple-type"></a>multipleInstancesPolicyType Simple Type

Definiert die Instanzrichtlinienkonstanten für das [**Element MultipleInstancesPolicy (settingsType).**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache **MultipleInstancesPolicyType-Typ** definiert die folgenden Werte.



| Wert        | Beschreibung                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| Parallel     | Startet eine neue Instanz, während eine vorhandene Instanz ausgeführt wird.<br/>                           |
| Warteschlange        | Startet eine neue Instanz des Tasks, nachdem alle anderen Instanzen des Tasks abgeschlossen sind.<br/>      |
| IgnoreNew    | Standard. Startet keine neue Instanz, wenn eine vorhandene Instanz des Tasks ausgeführt wird.<br/> |
| StopExisting | Beendet eine vorhandene Instanz des Tasks, bevor die neue Instanz gestartet wird.<br/>                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner schema simple types (Einfache Schematypen)](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





