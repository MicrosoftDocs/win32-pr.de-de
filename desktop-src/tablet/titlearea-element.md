---
description: Enthält Speicherort- und Begrenzungsinformationen für den Notiztitel, sofern vorhanden.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: TitleArea-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d563e8d7f6fc0107bc3302d3f8d94d29dfbfb8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432192"
---
# <a name="titlearea-element"></a>TitleArea-Element

Enthält Speicherort- und Begrenzungsinformationen für den Notiztitel, sofern vorhanden.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Titel**](title-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute



| attribute  | Typ                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum äußersten linken Punkt im begrenzungsfeld für das Element. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum obersten Punkt im Begrenzungsfeld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|   Element    | Wert                                                           |
|--------------|-----------------------------------------------------------------|
| Elementtyp | [**complexType: TitleAreaType**](titleareatype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                      |
| Schemaname  | Journalreader                                                  |



 

 

 



