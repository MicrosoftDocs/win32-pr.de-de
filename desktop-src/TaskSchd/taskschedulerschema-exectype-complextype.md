---
title: execType Complex Type
description: Definiert die untergeordneten Elemente und Sequenzierungsinformationen des Exec -Elements (actionGroup).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- execType complex type Taskplaner
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e0726930f902ec0458f42fff9cdce39026cf63ddab92982bc30da33ca671712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796630"
---
# <a name="exectype-complex-type"></a>execType Complex Type

Definiert die untergeordneten Elemente und Sequenzierungsinformationen des [**Exec -Elements (actionGroup).**](taskschedulerschema-exec-actiongroup-element.md)

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | type                                                        | Beschreibung                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Argumente**](taskschedulerschema-arguments-exectype-element.md)               | **string**                                                  | Gibt die Argumente an, die dem Befehlszeilenvorgang zugeordnet sind. <br/>                              |
| [**Befehl**](taskschedulerschema-command-exectype-element.md)                   | [**Pathtype**](taskschedulerschema-pathtype-simpletype.md) | Gibt die ausführbare Datei oder das Dokument an, die bzw. das ausgeführt werden soll.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | [**Pathtype**](taskschedulerschema-pathtype-simpletype.md) | Gibt das Verzeichnis an, in dem die ausführbare Datei oder die von der ausführbaren Datei verwendeten Dateien vorhanden sind.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[komplexe Schematypen Taskplaner](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





