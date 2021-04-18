---
description: Enthält einen Absatz.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Paragraph-Element (Windows.ui.xaml.doc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: bfe3752541bb54571e9802f557e83dcc7632f845
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365169"
---
# <a name="paragraph-element"></a>Paragraph-Element

Enthält einen Absatz.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Inhalt**](content-element--journal-reader.md)

[**-Gruppenknoten**](groupnode-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**Stimmen**](line-element.md)

[**Knotenmetriken**](paragraphlinemetrics-element.md)

## <a name="attributes"></a>Attribute



| Attribut       | type                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**        | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements. | Eine beliebige ganze Zahl.              |
| **Top**         | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**       | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungs Rahmens für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height**      | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des umgebenden Felds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |
| **BlockNumber** | **xs:nonNegativeInteger** | Erforderlich | Block Nummer.                                                                           | Eine beliebige nicht negative ganze Zahl. |
| **LineNumber**  | **xs:nonNegativeInteger** | Erforderlich | Die Zeile, in der der Absatz beginnt.                                                 | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| Elementtyp | ComplexType- [**Datentyp**](paragraphtype-complex-type.md) |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk                      |
| Schemaname  | Journal Leser                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Windows.ui.xaml.doc. h.</dt> </dl> |



 

 




