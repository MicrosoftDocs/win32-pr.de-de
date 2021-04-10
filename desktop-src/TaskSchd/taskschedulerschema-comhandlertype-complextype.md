---
title: komplexer comhandlertype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das comhandlerelement.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- komplexer comhandlertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040396"
---
# <a name="comhandlertype-complex-type"></a>komplexer comhandlertype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**comhandlerelement**](taskschedulerschema-comhandler-actiongroup-element.md) .

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | type                                                         | BESCHREIBUNG                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidtype**](taskschedulerschema-guidtype-simpletype.md)  | Gibt den Bezeichner der Handlerklasse an.<br/>          |
| [**Daten**](taskschedulerschema-data-comhandlertype-element.md)       | [**Datentyp**](taskschedulerschema-datatype-complextype.md) | Gibt zusätzliche Daten an, die dem Handler zugeordnet sind. <br/> |



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

 

 





