---
description: Das- <propertyStore> Element gibt einen Satz von einer oder mehreren Eigenschaften an, die von dieser Bibliothek verwendet werden. Dieses Element ist optional und besitzt keine Attribute.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: PropertyStore-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980320"
---
# <a name="propertystore-element-library-schema"></a>PropertyStore-Element (Bibliotheks Schema)

Das- <propertyStore> Element gibt einen Satz von einer oder mehreren Eigenschaften an, die von dieser Bibliothek verwendet werden. Dieses Element ist optional und besitzt keine Attribute.

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
| [librarydescription-Element (Bibliotheks Schema)](schema-librarydescription.md) | [Property-Element (Bibliotheks Schema)](schema-library-property.md) |



 

## <a name="remarks"></a>Bemerkungen

Das- <propertyStore> Element kann ein oder mehrere untergeordnete- <property> Elemente aufweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bibliotheks Beschreibungs Schema](library-schema-entry.md)
</dt> <dt>

[Suchdienst-Beschreibungs Schema](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
