---
title: RangeValue-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IRangeValueProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das RangeValue-Steuerelementmuster wird verwendet, um Steuerelemente zu unterstützen, die auf einen Wert innerhalb eines Bereichs festgelegt werden können.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des RangeValue-Steuerelementmusters
- Benutzeroberflächenautomatisierung,RangeValue-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IRangeValueProvider
- IRangeValueProvider
- Implementieren Benutzeroberflächenautomatisierung RangeValue-Steuerelementmustern
- RangeValue-Steuerelementmuster
- Steuerelementmuster, IRangeValueProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung RangeValue
- Steuerelementmuster, RangeValue
- interfaces,IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae87ca25fd1ada2f57ce77412fb589875792541fd2b5d31d6eb0aa86192dee36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114861"
---
# <a name="rangevalue-control-pattern"></a>RangeValue-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung [**von IRangeValueProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)einschließlich Informationen zu Eigenschaften und Methoden. Das **RangeValue-Steuerelementmuster** wird verwendet, um Steuerelemente zu unterstützen, die auf einen Wert innerhalb eines Bereichs festgelegt werden können.

Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IRangeValueProvider**](#required-members-for-irangevalueprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim **Implementieren des RangeValue-Steuerelementmusters** die folgenden Richtlinien und Konventionen:

-   Steuerelemente lassen eine erneute Kalibrierung der unterstützten Eigenschaften auf Grundlage des Gebietsschemas oder einer Benutzereinstellung zu. Ein Beispiel hierfür ist ein Thermometersteuerelement, das so festgelegt werden kann, dass die Temperatur in Fahrenheit oder Celsius angezeigt wird.
-   Für Steuerelemente, die über mehrdeutige Bereichswerte verfügen, z. B. Statusanzeigen oder Schieberegler, sollten diese Werte normalisiert werden.

## <a name="required-members-for-irangevalueprovider"></a>Erforderliche Member für **IRangeValueProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IRangeValueProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) erforderlich.



| Erforderliche Member                                              | Memberart | Hinweise |
|---------------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | Eigenschaft    | Keine  |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Eigenschaft    | Keine  |
| [**Largechange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | Eigenschaft    | Keine  |
| [**Smallchange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Eigenschaft    | Keine  |
| [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Eigenschaft    | Keine  |
| [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Eigenschaft    | Keine  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




