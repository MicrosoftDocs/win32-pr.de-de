---
description: Enthält codierte Binärdaten für ein Bild im Journal Dokument, falls vorhanden.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Image-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8437495a4c248a8e5bc68a0f7b75a2cf7d761387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360680"
---
# <a name="image-element"></a>Image-Element

Enthält codierte Binärdaten für ein Bild im Journal Dokument, falls vorhanden.

## <a name="definition"></a>Definition

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
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



|              |                                                         |
|--------------|---------------------------------------------------------|
| Elementtyp | ComplexType " [**ImageType**](imagetype-complex-type.md) " |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk              |
| Schemaname  | Journal Leser                                          |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hintergrund**](background-element.md)
</dt> </dl>

 

 



