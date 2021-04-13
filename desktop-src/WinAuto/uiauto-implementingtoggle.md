---
title: Toggle-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ideggleprovider, einschließlich Informationen zu Eigenschaften und Methoden. Das Toggle-Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die eine Reihe von Zuständen durchlaufen und einen Zustand nach dem Festlegen beibehalten können.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- UI-Automatisierung, Implementieren eines Toggle-Steuerelement Musters
- UI-Automatisierung, Toggle-Steuerelement Muster
- UI-Automatisierung, iabggleprovider
- IToggleProvider
- Implementieren von Steuerelement Mustern zum Umschalten der Benutzeroberflächen Automatisierung
- Steuerelement Muster umschalten
- Steuerelement Muster, iesggleprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächen Automatisierung umschalten
- Steuerelement Muster, Umschalten
- Schnittstellen, ideggleprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388122"
---
# <a name="toggle-control-pattern"></a>Toggle-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**ideggleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **Toggle** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die eine Reihe von Zuständen durchlaufen und einen Zustand nach dem Festlegen beibehalten können.

Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **iesggleprovider**](#required-members-for-itoggleprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Toggle** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Steuerelemente, die den Zustand bei Aktivierung nicht beibehalten, z. b. Schaltflächen, Symbolleisten Schaltflächen und Links, müssen stattdessen [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) implementieren.
-   Ein Steuerelement muss seine UMSCHALT Zustände ("[**degglestate**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)") in der folgenden Reihenfolge durchlaufen: " **degglestate \_ on**", " **degglestate \_ Off** " und ", falls unterstützt", " **degglestate" \_ unbestimmt**.
-   Ein-und **ausschalten bietet keine** Set-State-Methode aufgrund von Problemen im Zusammenhang mit der direkten Einstellung eines Kontrollkästchens mit drei Zuständen ohne durchlaufen der entsprechenden " [**degglestate**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) "-Sequenz.
-   Das Optionsfeld-Steuerelement implementiert [**iumggleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)nicht, da es nicht in der Lage ist, seine gültigen Zustände zu durchlaufen.

## <a name="required-members-for-itoggleprovider"></a>Erforderliche Member für **iesggleprovider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ideggleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                          | Memberart | Hinweise |
|-----------------------------------------------------------|-------------|-------|
| [**Ein-/Ausschalten**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | Methode      | Keine  |
| [**Objektstatus**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | Eigenschaft    | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




