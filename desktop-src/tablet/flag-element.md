---
description: Enthält eine Base64-codierte Bitmap eines Flags, das dem Abschnitt einer Journalnotiz zugeordnet ist.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46508f9821379fbedb3291ba45d16dbdd0fb316f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432327"
---
# <a name="flag-element"></a>Flag-Element

Enthält eine Base64-codierte Bitmap eines Flags, das dem Abschnitt einer Journalnotiz zugeordnet ist.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Inhalt**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute



| attribute  | Typ                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum äußersten linken Punkt im Begrenzungsfeld für das Element. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum obersten Punkt im begrenzungsfeld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|-------------------------------------------------------|
| Elementtyp | [**complexType: FlagType**](flagtype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink            |
| Schemaname  | Journalreader                                        |



 

 

 



