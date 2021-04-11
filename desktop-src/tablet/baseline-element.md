---
description: Stellt (x, y)-Informationen für die Start-und Endpunkte der Baseline eines Absatzes im Journal Dokument bereit. Der für diese Werte verwendete Koordinaten Bereich ist HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Baseline-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b64986707eaa1b382d2f88851367b9147c59c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214380"
---
# <a name="baseline-element"></a>Baseline-Element

Stellt (x, y)-Informationen für die Start-und Endpunkte der Baseline eines Absatzes im Journal Dokument bereit. Der für diese Werte verwendete Koordinaten Bereich ist **HIMETRIC**.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Knotenmetriken**](paragraphlinemetrics-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute



| Attribut  | type                      | Erforderlich | BESCHREIBUNG                                                      | Mögliche Werte           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Startx** | **xs:nonNegativeInteger** | Erforderlich | Der X-Wert für den Punkt, der den Anfang der Baseline markiert. | Eine beliebige nicht negative ganze Zahl. |
| **Startty** | **xs:nonNegativeInteger** | Erforderlich | Der Y-Wert für den Punkt, der den Anfang der Baseline markiert. | Eine beliebige nicht negative ganze Zahl. |
| **EndX**   | **xs:nonNegativeInteger** | Erforderlich | Der X-Wert für den Punkt, der das Ende der Baseline markiert.       | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|              |                                                               |
|--------------|---------------------------------------------------------------|
| Elementtyp | ComplexType für [**baselinetype**](baselinetype-complex-type.md) |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk                    |
| Schemaname  | Journal Leser                                                |



 

 

 



