---
description: Definiert die Randlinien, die auf der Seite gezeichnet werden.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Margin-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c264c2470d070353d1fd19340a161cf765bc05
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478666"
---
# <a name="margin-element"></a>Margin-Element

Definiert die Randlinien, die auf der Seite gezeichnet werden.

## <a name="definition"></a>Definition

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>Übergeordnete Elemente

Keine

## <a name="child-elements"></a>Untergeordnete Elemente

Nichts..

## <a name="attributes"></a>Attribute




| attribute | type | Erforderlich | BESCHREIBUNG | Mögliche Werte | 
|-----------|------|----------|-------------|-----------------|
| <strong>Stil</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType | Erforderlich | Gibt den Typ der zu zeichnenden Linie an. | <ul><li>Keine</li><li>Basis</li><li>Strich</li><li>Punkt</li><li>DashDot</li><li>DashDotDot</li><li>Double</li></ul> | 
| <strong>Farbe</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType | Optional | Farbe des Elements. | Ein hexadezimaler RGB-Wert. Entspricht dem folgenden regulären Ausdruck: #[0-9a-zA-Z] {6} . Beispiel: #4a79B5.<br /> | 
| <strong>Typ</strong> | <a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType | Optional | Gibt den linken oder rechten Rand an. | <ul><li>Left</li><li>Right</li></ul> | 
| <strong>Abstand</strong> | <strong>xs:nonNegativeInteger</strong> | Optional | Abstand zwischen Seitenrand und Rand. | Eine beliebige nicht negative ganze Zahl. | 




 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|-----------------------------------------------------------|
| Elementtyp | [**complexType: MarginType**](margintype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                |
| Schemaname  | Journalreader                                            |



 

 

 




