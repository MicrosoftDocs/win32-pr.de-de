---
description: 'Gibt an, wie ipropertydescription:: formatfordisplay den Wert der Eigenschaft als Zeichenfolge formatieren soll.'
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: enumeratedlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373059"
---
# <a name="enumeratedlist"></a>enumeratedlist

Gibt an, wie [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll. Außerdem wird beeinflusst, wie die-Eigenschaft gruppiert werden kann oder welche Werte in der Liste angezeigt werden sollen, wenn "editcontrol" ein listblox ist. Dies gilt nur, wenn <displayInfo displayType="Enumerated"> . Es darf nur ein [enumeratedlist]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet. Wenn kein [enumeratedlist]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.

## <a name="syntax"></a>Syntax


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                   | Untergeordnete Elemente                               |
|--------------------------------------------------|----------------------------------------------|
| [Display Info](./propdesc-schema-displayinfo.md) | [enum](./propdesc-schema-enum.md)           |
|                                                  | [enumbereich](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a>Attribute



| Attribut          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DefaultText        | Öffentlich. Dies ist optional. Geben Sie den Standardtext an, der verwendet werden soll, wenn [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) ein Wert zugewiesen wird, der keinem der aufgelisteten Elemente in der Liste zugeordnet ist. Die Syntax ermöglicht eine direkte Anzeige Zeichenfolge oder einen indirekten Verweis auf eine Anzeige Zeichenfolge. Verwenden Sie den Verweis, damit er lokalisiert werden kann.                              |
| usevaluefordefault | Öffentlich. Dies ist optional. Wenn diese Eigenschaft auf "true" festgelegt wird, wird [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) so informiert, dass der Wert unverändert verwendet wird, wenn der Wert keinem der aufgelisteten Elemente in der Liste zugeordnet ist. Für **ipropertydescription:: formatfordisplay** hat die Festlegung auf "true" Vorrang vor dem Festlegen von "DefaultText". Der Standardwert lautet "false". |



 

 

 
