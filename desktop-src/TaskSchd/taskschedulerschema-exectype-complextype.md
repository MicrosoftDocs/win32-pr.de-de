---
title: komplexer exectype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen des exec (aktiongroup)-Elements.
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- komplexer exectype-Typ Taskplaner
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f6186c15e8bbe059abaa6cc33580fca45286cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475651"
---
# <a name="exectype-complex-type"></a>komplexer exectype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen des [**exec (aktiongroup)**](taskschedulerschema-exec-actiongroup-element.md) -Elements.

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



| Element                                                                           | type                                                        | BESCHREIBUNG                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Argumente**](taskschedulerschema-arguments-exectype-element.md)               | **string**                                                  | Gibt die Argumente an, die dem Befehlszeilen Vorgang zugeordnet sind. <br/>                              |
| [**Get-Help**](taskschedulerschema-command-exectype-element.md)                   | [**PathType**](taskschedulerschema-pathtype-simpletype.md) | Gibt die ausführbare Datei oder das Dokument an, das ausgeführt werden soll.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | [**PathType**](taskschedulerschema-pathtype-simpletype.md) | Gibt das Verzeichnis an, in dem die ausführbare Datei oder die von der ausführbaren Datei verwendeten Dateien vorhanden sind.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komplexe Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





