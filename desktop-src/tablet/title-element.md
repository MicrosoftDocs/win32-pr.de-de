---
description: Enthält Titelinformationen zur Journalnotiz.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Title-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05661be8566cf4136194af4e08d8f9774d3413dc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473136"
---
# <a name="title-element"></a>Title-Element

Enthält Titelinformationen zur Journalnotiz.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Briefpapier**](stationery-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**TitleArea**](titlearea-element.md)

## <a name="attributes"></a>Attribute




| attribute | type | Erforderlich | BESCHREIBUNG | Mögliche Werte | 
|-----------|------|----------|-------------|-----------------|
| <strong>Stil</strong> | <strong>xs:string</strong> | Erforderlich | Gibt den Typ des Rahmens um den Titel der Notiz an. | <ul><li>Keine</li><li>SolidSquare</li><li>OutlineSquare</li><li>SolidRoundRect</li><li>OutlineRoundRect</li><li>SolidRoundRectDottedBaseline</li></ul> | 
| <strong>DateStyle</strong> | <strong>xs:string</strong> | Erforderlich | Definiert, ob der Titel ein Datum enthält oder nicht. | <ul><li>Keine</li><li>Short</li></ul> | 
| <strong>Farbe</strong> | <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a> | Optional | Gibt die Hintergrundfarbe an. | Weitere Informationen finden Sie unter <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>. | 




 

## <a name="element-information"></a>Elementinformationen



| Element      | Wert                                                   |
|--------------|---------------------------------------------------------|
| Elementtyp | [**complexType: TitleType**](titletype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink              |
| Schemaname  | Journalreader                                          |



 

 

 



