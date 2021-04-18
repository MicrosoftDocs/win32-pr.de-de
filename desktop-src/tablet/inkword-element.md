---
description: Enthält Informationen über ein bestimmtes frei Hand Wort in der Journal Notiz, einschließlich Position, Alternativen und der eigentlichen frei Hand Daten.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: InkWord-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358526"
---
# <a name="inkword-element"></a>InkWord-Element

Enthält Informationen über ein bestimmtes frei Hand Wort in der Journal Notiz, einschließlich Position, Alternativen und der eigentlichen frei Hand Daten.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**-Gruppenknoten**](groupnode-element.md)

[**Stimmen**](line-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**Scalartransform**](scalartransform-element.md)

[**Alternative ist**](alternatelist-element.md)

[**Canreclassify**](canreclassify-element.md)

[**Confidence**](confidence-element.md)

[**Inkobject**](inkobject-element.md)

## <a name="attributes"></a>Attribute



| Attribut  | type                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungs Rahmens für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des umgebenden Felds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |



 

> [!WARNING]
> Die interne Koordinaten Zuordnung des frei Hand Worts ist eine englische metrikeinheit, und ein Multiplikator von 2,54 muss von Ihrer Anwendung verwendet werden, um die Width-und Height-Werte in die von den Tablet PC Platform-APIs verwendeten HIMETRIC-Einheiten zu konvertieren.

 

## <a name="element-information"></a>Elementinformationen



|              |                                                             |
|--------------|-------------------------------------------------------------|
| Elementtyp | ComplexType " [**inkwordtype**](inkwordtype-complex-type.md) " |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk                  |
| Schemaname  | Journal Leser                                              |



 

 

 



