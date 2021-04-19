---
description: Enthält einen Satz von Elementen&\# 8212; Absatz, InkWord, Zeichnung, Text, Bild oder Flag&\# 8212;, die in der Journal Notiz gruppiert sind.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Groupnode-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346960"
---
# <a name="groupnode-element"></a>Groupnode-Element

Enthält eine Reihe von Elementen –[**Absatz**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Zeichnung**](drawing-element.md), [**Text**](text-element.md), [**Bild**](image-element.md)oder [**Flag**](flag-element.md)–, die in der Journal Notiz gruppiert sind.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Inhalt**](content-element--journal-reader.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Zeichnung**](drawing-element.md)

[**Text**](text-element.md)

[**Image**](docimage-element.md)

[**Flag**](flag-element.md)

## <a name="attributes"></a>Attribute



| Attribut  | type                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungs Rahmens für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des umgebenden Felds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| Elementtyp | ComplexType " [**groupnodetype**](groupnodetype-complex-type.md) " |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk                      |
| Schemaname  | Journal Leser                                                  |



 

 

 



