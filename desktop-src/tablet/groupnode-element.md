---
description: Enthält eine Reihe von Elementen&\# 8212; Paragraph, InkWord, Drawing, Text, Image oder Flag&\# 8212;, die in der Journalnotiz gruppiert sind.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: GroupNode-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc4d39a592b5b6328bd31ff37761cfd3f0138c0
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432571"
---
# <a name="groupnode-element"></a>GroupNode-Element

Enthält eine Reihe von Elementen –[**Absatz**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Zeichnung**](drawing-element.md), [**Text**](text-element.md), [**Bild**](image-element.md)oder [**Flag**](flag-element.md)– die in der Journalnotiz zusammen bzw. niert sind.

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



| attribute  | Typ                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.                                          | Eine nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.                                         | Eine nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|-----------------------------------------------------------------|
| Elementtyp | [**complexType: GroupNodeType**](groupnodetype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                      |
| Schemaname  | Journalreader                                                  |



 

 

 



