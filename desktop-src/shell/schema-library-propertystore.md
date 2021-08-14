---
description: Das <propertyStore> -Element gibt einen Satz von einer oder mehreren Eigenschaften an, die von dieser Bibliothek verwendet werden. Dieses Element ist optional und weist keine Attribute auf.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: propertyStore-Element (Bibliotheksschema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ff30972a358916e715ff1b374a555c6db24ee6d512d114bcf47f57ac8a1954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452975"
---
# <a name="propertystore-element-library-schema"></a>propertyStore-Element (Bibliotheksschema)

Das <propertyStore> -Element gibt einen Satz von einer oder mehreren Eigenschaften an, die von dieser Bibliothek verwendet werden. Dieses Element ist optional und weist keine Attribute auf.

## <a name="syntax"></a>Syntax

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                               | Untergeordnete Elemente                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [libraryDescription-Element (Bibliotheksschema)](schema-librarydescription.md) | [property-Element (Bibliotheksschema)](schema-library-property.md) |



 

## <a name="remarks"></a>Hinweise

Das <propertyStore> -Element kann über mindestens ein <property> untergeordnetes Element verfügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bibliotheksbeschreibungsschema](library-schema-entry.md)
</dt> <dt>

[Suchconnectorbeschreibungsschema](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
