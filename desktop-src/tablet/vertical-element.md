---
description: Enthält die Informationen, die die vertikale Komponente der Linien im Von der Journalnotiz verwendeten Stationery beschreiben. Wird beispielsweise verwendet, wenn die Notiz Gitternetzlinien auf hat.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Vertical-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6f05ab8a2160dbf6b987177957e8285385fe4db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479506"
---
# <a name="vertical-element"></a>Vertical-Element

Enthält die Informationen, die die vertikale Komponente der Linien im Von der Journalnotiz verwendeten Stationery beschreiben. Wird beispielsweise verwendet, wenn die Notiz Gitternetzlinien auf hat.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
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



|  Element     | Wert                                                         |
|--------------|---------------------------------------------------------------|
| Elementtyp | [**complexType: VerticalType**](verticaltype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                    |
| Schemaname  | Journalreader                                                |



 

 

 




