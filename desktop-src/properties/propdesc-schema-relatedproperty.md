---
description: Neu in Windows 7. Bezeichnet eine Eigenschaft, die mit der in der Eigenschafts Beschreibungsdatei definierten Eigenschaft verknüpft ist.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344799"
---
# <a name="relatedproperty"></a>relatedProperty

Neu in Windows 7. Bezeichnet eine Eigenschaft, die mit der in der Eigenschafts Beschreibungsdatei definierten Eigenschaft verknüpft ist. Es können beliebig viele [relatedproperty]() -Elemente innerhalb von [relatedpropertyinfo](./propdesc-schema-relatedpropertyinfo.md) vorhanden sein.

## <a name="syntax"></a>Syntax


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                   | Untergeordnete Elemente |
|------------------------------------------------------------------|----------------|
| [relatedpropertyinfo](./propdesc-schema-relatedpropertyinfo.md) | Keine           |



 

## <a name="attributes"></a>Attribute



| Attribut        | BESCHREIBUNG                                                        |
|------------------|--------------------------------------------------------------------|
| relationshipName | Öffentlich. Erforderlich. Der kanonische Name der Eigenschafts Beziehung. |
| propertyName     | Öffentlich. Erforderlich. Der kanonische Name der verwandten Eigenschaft.      |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element ermöglicht es Ihnen, eine Eigenschaft einem anderen zuzuordnen. Beispielsweise können Sie den Text der benutzerdefinierten Eigenschaft fabrikam. storagecapacity zu System. Capacity zuordnen:


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
