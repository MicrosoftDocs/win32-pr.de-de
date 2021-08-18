---
description: Definiert eine Attributgruppe, die von einer Vielzahl von Elementen in einer Journal-XML-Datei verwendet wird. Sie enthält Attribute, die verwendet werden, um die Begrenzungen (links, oben, Höhe und Breite) eines Elements im Dokument zu definieren.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: BoundsType-Attributgruppe
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba91269660875e55b92797609969ebee38d221016914d9473cd5eddd245cfc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967769"
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



| attribute  | type                      | Erforderlich | Beschreibung                                                                                        | PossibleValues                       |
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

 

 




