---
description: Enthält einen Absatz.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Paragraph-Element (Windows.ui.xaml.documents.h)
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
ms.openlocfilehash: 2f246294c80814ec809c0a1ca035fcb4741c30c5
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432232"
---
# <a name="paragraph-element"></a>Paragraph-Element

Enthält einen Absatz.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Inhalt**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**Linie**](line-element.md)

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="attributes"></a>Attribute



| attribute       | Typ                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**        | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element. | Eine beliebige ganze Zahl.              |
| **Top**         | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**       | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.                                          | Eine nicht negative ganze Zahl. |
| **Height**      | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.                                         | Eine nicht negative ganze Zahl. |
| **BlockNumber** | **xs:nonNegativeInteger** | Erforderlich | Blocknummer.                                                                           | Eine nicht negative ganze Zahl. |
| **LineNumber**  | **xs:nonNegativeInteger** | Erforderlich | Die Zeile, in der der Absatz beginnt.                                                 | Eine nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|-----------------------------------------------------------------|
| Elementtyp | [**complexType: ParagraphType**](paragraphtype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                      |
| Schemaname  | Journalreader                                                  |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Windows.ui.xaml.documents.h</dt> </dl> |



 

 




