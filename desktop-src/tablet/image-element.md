---
description: Enthält codierte Binärdaten für ein Bild im Journaldokument, sofern vorhanden.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Image-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55b1cfd62dd6c2f58c2c1da26f0a9564b8c070f5c57fdccc870fa8b52b3f37c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939834"
---
# <a name="image-element"></a>Image-Element

Enthält codierte Binärdaten für ein Bild im Journaldokument, sofern vorhanden.

## <a name="definition"></a>Definition

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Inhalt**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute



| attribute  | type                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.                                          | Eine nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.                                         | Eine nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|---------------------------------------------------------|
| Elementtyp | [**complexType: ImageType**](imagetype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink              |
| Schemaname  | Journalreader                                          |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hintergrund**](background-element.md)
</dt> </dl>

 

 



