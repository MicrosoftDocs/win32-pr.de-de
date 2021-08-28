---
description: Das &lt; &gt; propertyStore-Element gibt einen Satz von Eigenschaften an, die von dieser Bibliothek verwendet werden. Dieses Element ist optional und verfügt über keine Attribute.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: propertyStore-Element (Bibliotheksschema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089e87e6e7bdfa568ffa2e8903f6347cb6dc7b3d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880426"
---
# <a name="propertystore-element-library-schema"></a>propertyStore-Element (Bibliotheksschema)

Das &lt; &gt; propertyStore-Element gibt einen Satz von Eigenschaften an, die von dieser Bibliothek verwendet werden. Dieses Element ist optional und verfügt über keine Attribute.

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

Das &lt; &gt; propertyStore-Element kann ein oder mehrere untergeordnete &lt; &gt; Eigenschaftenelemente enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schema der Bibliotheksbeschreibung](library-schema-entry.md)
</dt> <dt>

[Suchconnectorbeschreibungsschema](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
