---
title: RangeValue-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IRangeValueProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das RangeValue-Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die auf einen Wert innerhalb eines Bereichs festgelegt werden können.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des RangeValue-Steuerelement Musters
- UI-Automatisierung, RangeValue-Steuerelement Muster
- Benutzeroberflächenautomatisierung, IRangeValueProvider
- IRangeValueProvider
- Implementieren von RangeValue-Steuerelement Mustern für Benutzeroberflächen
- RangeValue-Steuerelement Muster
- Steuerelement Muster, IRangeValueProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-RangeValue
- Steuerelement Muster, RangeValue
- Schnittstellen, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf426069ad88ad272fd78c521a220ba7ccf72275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339214"
---
# <a name="rangevalue-control-pattern"></a>RangeValue-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **RangeValue** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die auf einen Wert innerhalb eines Bereichs festgelegt werden können.

Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für " **IRangeValueProvider** "](#required-members-for-irangevalueprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **RangeValue** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Steuerelemente lassen eine erneute Kalibrierung der unterstützten Eigenschaften auf Grundlage des Gebietsschemas oder einer Benutzereinstellung zu. Ein Beispiel hierfür ist ein Thermometersteuerelement, das so festgelegt werden kann, dass die Temperatur in Fahrenheit oder Celsius angezeigt wird.
-   Für Steuerelemente, die über mehrdeutige Bereichswerte verfügen, z. B. Statusanzeigen oder Schieberegler, sollten diese Werte normalisiert werden.

## <a name="required-members-for-irangevalueprovider"></a>Erforderliche Member für " **IRangeValueProvider** "

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                              | Memberart | Hinweise |
|---------------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | Eigenschaft    | Keine  |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Eigenschaft    | Keine  |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | Eigenschaft    | Keine  |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Eigenschaft    | Keine  |
| [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Eigenschaft    | Keine  |
| [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Eigenschaft    | Keine  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




