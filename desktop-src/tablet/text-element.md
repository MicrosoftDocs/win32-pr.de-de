---
description: Enthält Textinformationen aus der Journalnotiz.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Text-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570f613a06f9fe814bfb1acbdbdba040dbc1119f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432318"
---
# <a name="text-element"></a>Text-Element

Enthält Textinformationen aus der Journalnotiz.

## <a name="definition"></a>Definition

Bei Verwendung mit [**Inhalt:**](content-element--journal-reader.md)

``` syntax
<xs:element name="Text" type="TextType" />
```

Oder, wenn sie mit [**TitleInfo und**](titleinfo-element.md) [**GroupNode verwendet wird:**](groupnode-element.md)

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

Es gibt keine Attribute, wenn sie mit [**TitleInfo und**](titleinfo-element.md) [**GroupNode verwendet werden.**](groupnode-element.md) Bei Verwendung mit [**Content**](content-element--journal-reader.md)lauten die Attribute wie folgt.



| attribute  | Typ                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.                                          | Eine nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.                                         | Eine nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|   Element           |   Wert                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementtyp | [**complexType:TextType**](texttype-complex-type.md) (mit dem Content-Element) oder **xs:string** (mit [**GroupNode-**](groupnode-element.md) und [**TitleInfo-Elementen)**](titleinfo-element.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink<br/>                                                                                                                                               |
| Schemaname  | Journalreader<br/>                                                                                                                                                                           |



 

 

 




