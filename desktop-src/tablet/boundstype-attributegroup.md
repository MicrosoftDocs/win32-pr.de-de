---
description: Definiert eine Attributgruppe, die von einer Vielzahl von Elementen in einer Journal-XML-Datei verwendet wird. Sie enthält Attribute, die verwendet werden, um die Begrenzungen (links, oben, Höhe und Breite) eines Elements im Dokument zu definieren.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: BoundsType-Attributgruppe
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c51fcb9bc0041bbc030f2c67e434a964212562
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436507"
---
# <a name="boundstype-attribute-group"></a>BoundsType-Attributgruppe

Definiert eine Attributgruppe, die von einer Vielzahl von Elementen in einer Journal-XML-Datei verwendet wird. Sie enthält Attribute, die verwendet werden, um die Begrenzungen (links, oben, Höhe und Breite) eines Elements im Dokument zu definieren.

## <a name="definition"></a>Definition

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute



| attribute  | type                      | Erforderlich | BESCHREIBUNG                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element.<br/> | Eine beliebige ganze Zahl.<br/>              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.<br/>  | Eine beliebige ganze Zahl.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.<br/>                                          | Eine nicht negative ganze Zahl.<br/> |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.<br/>                                         | Eine nicht negative ganze Zahl.<br/> |



 

## <a name="type-information"></a>Typinformationen



|                 | Wert                                      |
|-----------------|--------------------------------------------|
| **Namespace**   | urn:schemas-microsoft-com:tabletpc:richink |
| **Schemaname** | Journalreader                             |



 

## <a name="remarks"></a>Hinweise

**Left** und **Top** können negativ sein, da der Ursprung durch die Ränder und nicht durch die Seite definiert wird.

 

 




