---
description: Enthält eine Base64-codierte Bitmap eines Flags, das einem Abschnitt eines Journal Hinweises zugeordnet ist.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6eda9aeb29c07c0de05eadffb8ba8d60f81954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345742"
---
# <a name="flag-element"></a>Flag-Element

Enthält eine Base64-codierte Bitmap eines Flags, das einem Abschnitt eines Journal Hinweises zugeordnet ist.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Inhalt**](content-element--journal-reader.md)

[**-Gruppenknoten**](groupnode-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute



| Attribut  | type                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungs Rahmens für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des umgebenden Felds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|              |                                                       |
|--------------|-------------------------------------------------------|
| Elementtyp | ComplexType " [**FlagType**](flagtype-complex-type.md) " |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk            |
| Schemaname  | Journal Leser                                        |



 

 

 



