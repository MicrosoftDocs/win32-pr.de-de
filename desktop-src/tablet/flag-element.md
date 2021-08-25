---
description: Enthält eine Base64-codierte Bitmap eines Flags, das dem Abschnitt einer Journalnotiz zugeordnet ist.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df40874178ba998ae9c864036b7befbf85179680de92cb68595f394e370e4404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774080"
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



| attribute  | Typ                      | Erforderlich | Beschreibung                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum äußersten linken Punkt im Begrenzungsfeld für das Element. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum obersten Punkt im Begrenzungsfeld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|-------------------------------------------------------|
| Elementtyp | [**complexType: FlagType**](flagtype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink            |
| Schemaname  | Journalreader                                        |



 

 

 



