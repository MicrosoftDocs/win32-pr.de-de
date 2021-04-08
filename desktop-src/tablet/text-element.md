---
description: Enthält Textinformationen aus der Journal Notiz.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Text-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960664"
---
# <a name="text-element"></a>Text-Element

Enthält Textinformationen aus der Journal Notiz.

## <a name="definition"></a>Definition

Bei Verwendung mit [**Inhalt**](content-element--journal-reader.md):

``` syntax
<xs:element name="Text" type="TextType" />
```

Oder bei Verwendung mit [**titleinfo**](titleinfo-element.md) und [**groupnode**](groupnode-element.md):

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Inhalt**](content-element--journal-reader.md)

[**-Gruppenknoten**](groupnode-element.md)

[**Titleinfo**](titleinfo-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute

Es gibt keine Attribute, wenn Sie mit [**titleinfo**](titleinfo-element.md) und [**groupnode**](groupnode-element.md)verwendet werden. Bei Verwendung mit [**Inhalt**](content-element--journal-reader.md)lauten die Attribute wie folgt.



| Attribut  | type                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungs Rahmens für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des umgebenden Felds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementtyp | ComplexType-Element von [**TextType**](texttype-complex-type.md) (mit dem Content-Element) oder **xs: String** (mit [**groupnode**](groupnode-element.md) -und [**titleinfo**](titleinfo-element.md) -Elementen) |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk<br/>                                                                                                                                               |
| Schemaname  | Journal Leser<br/>                                                                                                                                                                           |



 

 

 




