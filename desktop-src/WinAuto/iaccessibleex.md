---
title: Die iaccessibleex-Schnittstelle
description: Steuerelemente, die nicht über einen Microsoft-Benutzeroberflächenautomatisierungs-Anbieter verfügen, aber IAccessible implementieren, können problemlos aktualisiert werden, um einige Funktionen zur Automatisierung der Benutzeroberfläche durch Implementieren der iaccessibleex-Schnittstelle bereitzustellen
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100770"
---
# <a name="the-iaccessibleex-interface"></a>Die iaccessibleex-Schnittstelle

Steuerelemente, die nicht über einen Microsoft-Benutzeroberflächenautomatisierungs-Anbieter verfügen, aber [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementieren, können problemlos aktualisiert werden, um einige Funktionen zur Automatisierung der Benutzeroberfläche durch Implementieren der [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle bereitzustellen Diese Schnittstelle ermöglicht es dem Steuerelement, Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Muster verfügbar zu machen, ohne dass eine vollständige Implementierung von Schnittstellen für Benutzeroberflächenautomatisierungs-Anbieter wie [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) Um **iaccessibleex**, **IRawElementProviderFragment** und alle anderen Benutzeroberflächenautomatisierungs-Schnittstellen zu verwenden, fügen Sie die uiautomation. h-Header Datei in Ihren Quellcode ein.

Angenommen, Sie haben ein benutzerdefiniertes Steuerelement, das über einen Bereichs Wert verfügt. Der Microsoft Active Accessibility Server für das Steuerelement definiert die Rolle des Steuer Elements und kann seinen aktuellen Wert zurückgeben. Da in Microsoft Active Accessibility jedoch keine Mindest-und höchst Eigenschaften definiert sind, verfügt der Server nicht über die Möglichkeit, die minimalen und maximalen Werte des Steuer Elements zurückzugeben. Ein Benutzeroberflächenautomatisierungs-Client kann die Rolle, den aktuellen Wert und andere Eigenschaften von Microsoft Active Accessibility abrufen, da der Benutzeroberflächenautomatisierungs-Kern diese über [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)abrufen kann. Ohne Zugriff auf eine [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) -Schnittstelle für das Objekt kann die Benutzeroberflächen Automatisierung jedoch auch nicht die maximalen und minimalen Werte abrufen.

Der Steuerelement Entwickler könnte einen kompletten Benutzeroberflächenautomatisierungs-Anbieter für das Steuerelement bereitstellen. Dies würde jedoch bedeuten, dass ein Großteil der vorhandenen Funktionen der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung duplizieren würde, z. b. Navigation und allgemeine Eigenschaften. Stattdessen kann sich der Entwickler weiterhin auf **IAccessible** verlassen, um diese Funktionalität bereitzustellen, und gleichzeitig Unterstützung für Steuerelement spezifische Eigenschaften durch [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)hinzufügen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Iaccessibleex-Implementierungs Richtlinien](iaccessibleex-implementation-guidelines.md)
-   [Implementieren von iaccessibleex für Anbieter](implementing-iaccessibleex-for-providers.md)
-   [Verwenden von iaccessibleex von einem Client](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Infrastruktur](common-infrastructure.md)
</dt> </dl>

 

 




