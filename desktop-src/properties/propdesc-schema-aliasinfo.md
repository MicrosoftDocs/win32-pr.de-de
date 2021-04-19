---
description: Gibt einen Sortierungs Alias oder eine Liste von Sortier Aliasen an, indem ein Element angegeben wird, das eine Sortier Eigenschaft oder eine Liste von Sortier Eigenschaften enthält.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372970"
---
# <a name="aliasinfo"></a>aliasInfo

Gibt einen Sortierungs Alias oder eine Liste von Sortier Aliasen an, indem ein Element angegeben wird, das eine Sortier Eigenschaft oder eine Liste von Sortier Eigenschaften enthält. Es darf nur ein [AliasInfo]() -Element für jedes [propertydescription](./propdesc-schema-propertydescription.md) -Element vorhanden sein. Bei Eigenschaften, bei denen cangroupby = true festgelegt ist, kann es beim aliasInfo/@additionalSortByAliases Ändern der Sortierreihenfolge in einer Ansicht, die nach der-Eigenschaft gruppiert ist, zu unerwartetem Verhalten kommen, es sei denn, es wird eine sekundäre Sortier Eigenschaft angegeben (= prop: example) Insbesondere wird die Reihenfolge der Gruppen geändert, aber die Reihenfolge der Elemente in den Gruppen ist nicht.

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
| [propertydescription](./propdesc-schema-propertydescription.md) | Keine           |



 

## <a name="attributes"></a>Attribute



| Attribut               | BESCHREIBUNG                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sortbyalias             | Öffentlich. Dies ist optional. Der kanonische Name der Eigenschaft, die zum Sortieren nach verwendet werden soll. Diese Zeichenfolge ist vom Typ "Canonical-Type".                                            |
| additionalsortbyaliases | Öffentlich. Dies ist optional. Eine durch Semikolons getrennte Liste der zusätzlichen Eigenschaften, die beim Sortieren verwendet werden sollen. Die Eigenschaften werden auf die Sortierreihenfolge in der von Ihnen angegebenen Reihenfolge angewendet. |



 

 

 
