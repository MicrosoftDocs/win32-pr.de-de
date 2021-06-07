---
description: Enthält Inhalt, der vom Analysegerät oder vom Benutzer als Zeichnung klassifiziert wurde.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Drawing-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87c0a3d8879fb5f3146c46c9c88d83a6e658d8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432512"
---
# <a name="drawing-element"></a>Drawing-Element

Enthält Inhalt, der vom Analysegerät oder vom Benutzer als Zeichnung klassifiziert wurde.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Inhalt**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**ScalarTransform**](scalartransform-element.md)

[**CanReClassify**](canreclassify-element.md)

[**InkClass**](inkclass-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Attribute



| attribute  | Typ                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.                                          | Eine nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.                                         | Eine nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|-------------------------------------------------------------|
| Elementtyp | [**complexType: DrawingType**](drawingtype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Schemaname  | Journalreader                                              |



 

 

 



