---
description: Stellt (x, y)-Informationen für die Start- und Endpunkte der Baseline eines Absatzes im Journaldokument zur Verfügung. Der für diese Werte verwendete Koordinatenraum ist HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Baseline-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bc64f332608b4bd0281ae2a7f29db96101e9d2e
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436565"
---
# <a name="baseline-element"></a>Baseline-Element

Stellt (x, y)-Informationen für die Start- und Endpunkte der Baseline eines Absatzes im Journaldokument zur Verfügung. Der für diese Werte verwendete Koordinatenraum ist **HIMETRIC.**

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute



| attribute  | type                      | Erforderlich | BESCHREIBUNG                                                      | Mögliche Werte           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Startx** | **xs:nonNegativeInteger** | Erforderlich | Der X-Wert für den Punkt, der den Anfang der Baseline markiert. | Eine nicht negative ganze Zahl. |
| **StartY** | **xs:nonNegativeInteger** | Erforderlich | Der Y-Wert für den Punkt, der den Anfang der Baseline markiert. | Eine nicht negative ganze Zahl. |
| **EndX**   | **xs:nonNegativeInteger** | Erforderlich | Der X-Wert für den Punkt, der das Ende der Baseline markiert.       | Eine nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|                  | Wert                                                         |
|------------------|---------------------------------------------------------------|
| **Elementtyp** | [**complexType: BaselineType**](baselinetype-complex-type.md) |
| **Namespace**    | urn:schemas-microsoft-com:tabletpc:richink                    |
| **Schemaname**  | Journalreader                                                |



 

 

 



