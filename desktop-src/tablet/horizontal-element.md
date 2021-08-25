---
description: Enthält Formatierungsinformationen für die horizontalen Linien, die für das Stationery in einer Journalnotiz verwendet werden.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Horizontales Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b66e8557d73570ce1a0b7eb7217c02435c51a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482686"
---
# <a name="horizontal-element"></a>Horizontales Element

Enthält Formatierungsinformationen für die horizontalen Linien, die für das Stationery in einer Journalnotiz verwendet werden.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute




| attribute | type | Erforderlich | BESCHREIBUNG | Mögliche Werte | 
|-----------|------|----------|-------------|-----------------|
| <strong>Stil</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType | Erforderlich | Gibt den Typ der zu zeichneten Linie an. | <ul><li>Keine</li><li>Basis</li><li>Strich</li><li>Punkt</li><li>DashDot</li><li>DashDotDot</li><li>Double</li></ul> | 
| <strong>Farbe</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType | Optional | Farbe des Elements. | Ein hexadezimaler RGB-Wert. Entspricht dem folgenden regulären Ausdruck: #[0-9a-zA-Z] {6} . Beispiel: #4a79B5.<br /> | 
| <strong>SpacingBefore</strong> | <strong>xs:nonNegativeInteger</strong> | Optional | Abstand vor dem Element. | Eine nicht negative ganze Zahl. | 
| <strong>SpacingBetween</strong> | <strong>xs:nonNegativeInteger</strong> | Optional | Abstand zwischen diesem Element und umgebenden Elementen. | Eine nicht negative ganze Zahl. | 




 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|-------------------------------------------------------------------|
| Elementtyp | [**complexType: HorizontalType**](horizontaltype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                        |
| Schemaname  | Journalreader                                                    |



 

 

 




