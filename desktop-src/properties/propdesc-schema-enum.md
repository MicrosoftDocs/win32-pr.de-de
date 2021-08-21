---
description: Wird verwendet, um aufzählten Text diskreten Werten zu zuweisen.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1336a690fe7ac1e19a8606912a4f7d538d3842ab6a490d17b89f90f64bbfbc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970979"
---
# <a name="enum"></a>enum

Wird verwendet, um aufzählten Text diskreten Werten zu zuweisen. Eine beliebige Anzahl dieser Elemente kann unter einem [enumeratedList-Element vorhanden sein.](./propdesc-schema-enumeratedlist.md) Programmgesteuert werden diese als IPropertyEnumType-Objekte dargestellt, deren [**IPropertyEnumType::GetEnumType-Methode**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) PET \_ DISCRETEVALUE zurückgibt.

## <a name="syntax"></a>Syntax


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                         | Untergeordnete Elemente |
|--------------------------------------------------------|----------------|
| [enumeratedList](./propdesc-schema-enumeratedlist.md) | Keine           |



 

## <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| value     | Öffentlich. Erforderlich. Der diskrete Wert (Zeichenfolge oder Zahl), dem enumerierter Text zugewiesen werden soll.                                                                                                                           |
| text      | Öffentlich. Erforderlich. Der Text, der zum Anzeigen des aufzählten Werts verwendet wird. Die Syntax ermöglicht eine direkte Anzeigezeichenfolge oder einen indirekten Anzeigezeichenfolgenverweis. verwenden Sie die indirekte Anzeigezeichenfolge, damit sie lokalisiert werden kann. |
| Zugriffstasten | **Windows 7 und höher.** Öffentlich. Optional. Eine Liste von mnemonischen Werten, die verwendet werden können, um in Suchabfragen auf die -Eigenschaft zu verweisen. Die Liste ist durch das Zeichen " \| " getrennt.                                     |



 

 

 
