---
title: IAccessibleEx-Schnittstelle
description: Steuerelemente, die nicht über einen Microsoft Benutzeroberflächenautomatisierung-Anbieter verfügen, aber IAccessible implementieren, können problemlos aktualisiert werden, um einige Benutzeroberflächenautomatisierung Funktionen bereitzustellen, indem die IAccessibleEx-Schnittstelle implementiert wird.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170e6160a05350fa459090b2f51dbedd618ebdb81512a7e9730b50f8533ef95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566011"
---
# <a name="the-iaccessibleex-interface"></a>IAccessibleEx-Schnittstelle

Steuerelemente, die nicht über einen Microsoft Benutzeroberflächenautomatisierung-Anbieter verfügen, aber [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementieren, können problemlos aktualisiert werden, um einige Benutzeroberflächenautomatisierung Funktionalität bereitzustellen, indem die [**IAccessibleEx-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementiert wird. Diese Schnittstelle ermöglicht es dem Steuerelement, Benutzeroberflächenautomatisierung Eigenschaften und Steuerelementmuster verfügbar zu machen, ohne dass eine vollständige Implementierung Benutzeroberflächenautomatisierung Anbieterschnittstellen wie [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)erforderlich ist. Um **IAccessibleEx,** **IRawElementProviderFragment** und alle anderen Benutzeroberflächenautomatisierung Schnittstellen zu verwenden, schließen Sie die Headerdatei UIAutomation.h in Ihren Quellcode ein.

Betrachten Sie beispielsweise ein benutzerdefiniertes Steuerelement, das über einen Bereichswert verfügt. Der Microsoft Active Accessibility-Server für das Steuerelement definiert die Rolle des Steuerelements und kann seinen aktuellen Wert zurückgeben. Da Microsoft Active Accessibility jedoch keine minimalen und maximalen Eigenschaften definiert, verfügt der Server nicht über die Möglichkeit, die Minimal- und Höchstwerte des Steuerelements zurückzugeben. Ein Benutzeroberflächenautomatisierung Client kann die Rolle, den aktuellen Wert und andere Microsoft Active Accessibility Eigenschaften des Steuerelements abrufen, da der Benutzeroberflächenautomatisierung Core diese über [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)abrufen kann. Ohne Zugriff auf eine [**IRangeValueProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) für das Objekt kann Benutzeroberflächenautomatisierung jedoch auch die Maximalen und Mindestwerte nicht abrufen.

Der Steuerelemententwickler könnte einen vollständigen Benutzeroberflächenautomatisierung Anbieter für das Steuerelement bereitstellen. Dies würde jedoch bedeuten, einen Großteil der vorhandenen Funktionalität der [**IAccessible-Implementierung**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) zu duplizieren, z. B. Navigation und allgemeine Eigenschaften. Stattdessen kann sich der Entwickler weiterhin auf **IAccessible** verlassen, um diese Funktionalität zur Verfügung zu stellen, während er unterstützung für steuerelementspezifische Eigenschaften über [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)hinzufügt.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [IAccessibleEx-Implementierungsrichtlinien](iaccessibleex-implementation-guidelines.md)
-   [Implementieren von IAccessibleEx für Anbieter](implementing-iaccessibleex-for-providers.md)
-   [Verwenden von IAccessibleEx über einen Client](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Infrastruktur](common-infrastructure.md)
</dt> </dl>

 

 




