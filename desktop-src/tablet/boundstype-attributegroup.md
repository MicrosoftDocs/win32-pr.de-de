---
description: Definiert eine Attribut Gruppe, die von einer Vielzahl von Elementen in einer Journal-XML-Datei verwendet wird. Sie enthält Attribute, mit denen die Begrenzungen (Links, oben, Höhe und Breite) eines Elements im Dokument definiert werden.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Boundstype-Attribut Gruppe
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749105"
---
# <a name="boundstype-attribute-group"></a>Boundstype-Attribut Gruppe

Definiert eine Attribut Gruppe, die von einer Vielzahl von Elementen in einer Journal-XML-Datei verwendet wird. Sie enthält Attribute, mit denen die Begrenzungen (Links, oben, Höhe und Breite) eines Elements im Dokument definiert werden.

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



| Attribut  | type                      | Erforderlich | BESCHREIBUNG                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements.<br/> | Eine beliebige ganze Zahl.<br/>              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.<br/>  | Eine beliebige ganze Zahl.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungs Rahmens für das Element.<br/>                                          | Eine beliebige nicht negative ganze Zahl.<br/> |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des umgebenden Felds für das Element.<br/>                                         | Eine beliebige nicht negative ganze Zahl.<br/> |



 

## <a name="type-information"></a>Typinformationen



|             |                                            |
|-------------|--------------------------------------------|
| Namespace   | urn: Schemas-Microsoft-com: TabletPC: RichInk |
| Schemaname | Journal Leser                             |



 

## <a name="remarks"></a>Bemerkungen

" **Left** " und " **Top** " können negativ sein, da der Ursprung durch die Ränder definiert wird, nicht die Seite.

 

 




