---
description: Neu für Windows 7. Identifiziert eine Eigenschaft, die mit der in der Eigenschaftenbeschreibungsdatei definierten Eigenschaft verknüpft ist.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285c0f8b0731ba790cd57105f907cd4df85b6faa41c3f649588aca7ef457418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938680"
---
# <a name="relatedproperty"></a>relatedProperty

Neu für Windows 7. Identifiziert eine Eigenschaft, die mit der in der Eigenschaftenbeschreibungsdatei definierten Eigenschaft verknüpft ist. Es können beliebig viele [relatedProperty-Elemente]() innerhalb einer [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) vorhanden sein.

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
| [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) | Keine           |



 

## <a name="attributes"></a>Attribute



| attribute        | BESCHREIBUNG                                                        |
|------------------|--------------------------------------------------------------------|
| relationshipName | Öffentlich. Erforderlich. Der kanonische Name der Eigenschaftenbeziehung. |
| propertyName     | Öffentlich. Erforderlich. Der kanonische Name der verknüpften Eigenschaft.      |



 

## <a name="remarks"></a>Hinweise

Mit diesem Element können Sie eine Eigenschaft einer anderen zuordnen. Beispielsweise können Sie den Text Ihrer benutzerdefinierten Eigenschaft Fabrikam.StorageCapacity System.Capacity zuordnen:


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
