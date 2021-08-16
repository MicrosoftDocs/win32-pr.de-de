---
description: Gibt einen Sortieralias oder eine Liste von Sortieraliasen an, indem ein Element angegeben wird, das eine Sortiereigenschaft oder eine Liste von Sortiereigenschaften enthält.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 087323df682a2f74164c530f18a9c4da8405930304186288a3d84635bb06ab55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970969"
---
# <a name="aliasinfo"></a>aliasInfo

Gibt einen Sortieralias oder eine Liste von Sortieraliasen an, indem ein Element angegeben wird, das eine Sortiereigenschaft oder eine Liste von Sortiereigenschaften enthält. Es sollte nur ein [aliasInfo-Element]() für jedes [propertyDescription-Element](./propdesc-schema-propertydescription.md) vorhanden sein. Für Eigenschaften, die canGroupBy=true festlegen, kann es vorkommen, dass der Benutzer unerwartetes Verhalten aufweist, aliasInfo/@additionalSortByAliases wenn die Sortierreihenfolge in einer Sicht geändert wird, die nach der -Eigenschaft gruppiert ist, sofern keine sekundäre Sortiereigenschaft angegeben ist ( =prop:example). Insbesondere ändert sich die Reihenfolge der Gruppen, die Reihenfolge der Elemente innerhalb der Gruppen jedoch nicht.

## <a name="syntax"></a>Syntax


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                   | Untergeordnete Elemente |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | Keine           |



 

## <a name="attributes"></a>Attribute



| attribute               | BESCHREIBUNG                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sortByAlias             | Öffentlich. Optional. Der kanonische Name der Eigenschaft, nach der sortiert werden soll. Diese Zeichenfolge ist vom Typ kanonischer Typ.                                            |
| additionalSortByAliases | Öffentlich. Optional. Eine durch Semikolons getrennte Liste zusätzlicher Eigenschaften, die beim Sortieren verwendet werden sollen. Die Eigenschaften werden auf die Sortierung in der Reihenfolge angewendet, in der sie angegeben werden. |



 

 

 
