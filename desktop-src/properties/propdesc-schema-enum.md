---
description: Dient zum Zuweisen von Enumerationstext zu diskreten Werten.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b615697e669f8d02e0530a1763309cfe74113467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357780"
---
# <a name="enum"></a>enum

Dient zum Zuweisen von Enumerationstext zu diskreten Werten. Eine beliebige Anzahl dieser Elemente kann unter einer [enumeratedlist](./propdesc-schema-enumeratedlist.md)vorhanden sein. Diese werden Programm gesteuert als ipropertyenumtype-Objekte dargestellt, deren [**ipropertyenumtype:: getenumtype**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) -Methode PET \_ diskretevalue zurückgibt.

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
| [enumeratedlist](./propdesc-schema-enumeratedlist.md) | none           |



 

## <a name="attributes"></a>Attribute



| Attribut | BESCHREIBUNG                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| value     | Öffentlich. Erforderlich. Der diskrete Wert (Zeichenfolge oder Zahl), dem der Enumerationstext zugewiesen werden soll.                                                                                                                           |
| text      | Öffentlich. Erforderlich. Der Text, der verwendet wird, um den Enumerationswert anzuzeigen. Die Syntax ermöglicht eine direkte Anzeige Zeichenfolge oder einen indirekten Verweis auf eine Anzeige Zeichenfolge. Verwenden Sie die indirekte Anzeige Zeichenfolge, damit Sie lokalisiert werden kann. |
| Zugriffstasten | **Windows 7 und höher.** Öffentlich. Dies ist optional. Eine Liste von mnetmonischen Werten, die verwendet werden können, um auf die Eigenschaft in Such Abfragen zu verweisen. Die Liste wird durch das \| Zeichen "" getrennt.                                     |



 

 

 
