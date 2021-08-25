---
description: Enthält Textinformationen aus der Journalnotiz.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Text-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae4e9fa123f1f43bd92d902158fc3fbc5b1c1de8e074b57aadeb339a0a7b6f15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819939"
---
# <a name="text-element"></a>Text-Element

Enthält Textinformationen aus der Journalnotiz.

## <a name="definition"></a>Definition

Bei Verwendung mit [**Content**](content-element--journal-reader.md):

``` syntax
<xs:element name="Text" type="TextType" />
```

Oder, wenn sie mit [**TitleInfo**](titleinfo-element.md) und [**GroupNode**](groupnode-element.md)verwendet wird:

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Inhalt**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

[**TitleInfo**](titleinfo-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute

Bei Verwendung mit [**TitleInfo**](titleinfo-element.md) und [**GroupNode**](groupnode-element.md)gibt es keine Attribute. Bei Verwendung mit [**Content**](content-element--journal-reader.md)sind die Attribute wie folgt.



| attribute  | type                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum äußersten linken Punkt im Begrenzungsfeld für das Element. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum obersten Punkt im Begrenzungsfeld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|   Element           |   Wert                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementtyp | [**TextType**](texttype-complex-type.md) complexType (mit dem Content-Element) oder **xs:string** (mit [**GroupNode-**](groupnode-element.md) und [**TitleInfo-Elementen)**](titleinfo-element.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink<br/>                                                                                                                                               |
| Schemaname  | Journalreader<br/>                                                                                                                                                                           |



 

 

 




