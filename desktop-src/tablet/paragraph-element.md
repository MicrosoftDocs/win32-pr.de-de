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
ms.openlocfilehash: 877bede54ef714a011903424b1f323f004264affefedbcfae0ab44f2dcf58816
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843400"
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



| attribute       | Typ                      | Erforderlich | Beschreibung                                                                             | Mögliche Werte           |
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



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Windows.ui.xaml.documents.h</dt> </dl> |



 

 




