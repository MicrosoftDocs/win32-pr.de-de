---
description: Definiert eine Gruppe, die einen Satz gruppierter Inhalte in einer Journal Notiz enthält.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Gruppe "contentgroup"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbbc13a3dee796646b6d61ac9ba0bde50880f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042622"
---
# <a name="contentgroup-group"></a>Gruppe "contentgroup"

Definiert eine Gruppe, die einen Satz gruppierter Inhalte in einer Journal Notiz enthält.

## <a name="definition"></a>Definition

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Untergeordnete Elemente

[**-Gruppenknoten**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Zeichnung**](drawing-element.md)

[**Text**](text-element.md)

[**Image**](docimage-element.md)

[**Flag**](flag-element.md)

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



 

 

 




