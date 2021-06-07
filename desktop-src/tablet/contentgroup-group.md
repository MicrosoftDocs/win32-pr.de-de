---
description: Definiert eine Gruppe, die einen Satz gruppierter Inhalte in einer Journalnotiz enthält.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: ContentGroup-Gruppe
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432612"
---
# <a name="contentgroup-group"></a>ContentGroup-Gruppe

Definiert eine Gruppe, die einen Satz gruppierter Inhalte in einer Journalnotiz enthält.

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

[**GroupNode**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Zeichnung**](drawing-element.md)

[**Text**](text-element.md)

[**Image**](docimage-element.md)

[**Flag**](flag-element.md)

## <a name="attributes"></a>Attribute



| attribute  | Typ                      | Erforderlich | BESCHREIBUNG                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum äußersten linken Punkt im begrenzungsfeld für das Element.<br/> | Eine beliebige ganze Zahl.<br/>              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum obersten Punkt im Begrenzungsfeld für das Element.<br/>  | Eine beliebige ganze Zahl.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.<br/>                                          | Eine beliebige nicht negative ganze Zahl.<br/> |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.<br/>                                         | Eine beliebige nicht negative ganze Zahl.<br/> |



 

## <a name="type-information"></a>Typinformationen



|  Element     | Wert                                                     |
|-------------|--------------------------------------------|
| Namespace   | urn:schemas-microsoft-com:tabletpc:richink |
| Schemaname | Journalreader                             |



 

 

 




