---
description: Enthält codierte Binärdaten für ein Bild im Journaldokument, sofern vorhanden.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Image-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9dd3b37a39ce45ee0294f46922fbab376523b64
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432582"
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



| attribute  | Typ                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum äußersten linken Punkt im Begrenzungsfeld für das Element. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand vom Ursprung zum obersten Punkt im begrenzungsfeld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |



 

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

 

 



