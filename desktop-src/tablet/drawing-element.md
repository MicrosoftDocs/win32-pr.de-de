---
description: Enthält Inhalte, die vom Analyzer oder vom Benutzer als Zeichnung klassifiziert wurden.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Drawing-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe516a4ba33e6e597b17ce8365d792f19468c3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350979"
---
# <a name="drawing-element"></a>Drawing-Element

Enthält Inhalte, die vom Analyzer oder vom Benutzer als Zeichnung klassifiziert wurden.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Inhalt**](content-element--journal-reader.md)

[**-Gruppenknoten**](groupnode-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**Scalartransform**](scalartransform-element.md)

[**Canreclassify**](canreclassify-element.md)

[**Inkclass**](inkclass-element.md)

[**Inkobject**](inkobject-element.md)

## <a name="attributes"></a>Attribute



| Attribut  | type                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungs Rahmens für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des umgebenden Felds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|              |                                                             |
|--------------|-------------------------------------------------------------|
| Elementtyp | ComplexType für [**drawingtype**](drawingtype-complex-type.md) |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk                  |
| Schemaname  | Journal Leser                                              |



 

 

 



