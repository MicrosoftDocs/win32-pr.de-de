---
title: Die IAccessibleEx-Schnittstelle
description: Steuerelemente, die über keinen Microsoft Benutzeroberflächenautomatisierung-Anbieter verfügen, aber IAccessible implementieren, können problemlos aktualisiert werden, um einige Benutzeroberflächenautomatisierung bereitstellen, indem die IAccessibleEx-Schnittstelle implementiert wird.
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
# <a name="the-iaccessibleex-interface"></a>Die IAccessibleEx-Schnittstelle

Steuerelemente, die keinen Microsoft Benutzeroberflächenautomatisierung-Anbieter haben, aber [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementieren, können problemlos aktualisiert werden, um einige Benutzeroberflächenautomatisierung bereitstellen, indem die [**IAccessibleEx-Schnittstelle implementiert**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) wird. Diese Schnittstelle ermöglicht es dem Steuerelement, Benutzeroberflächenautomatisierung Eigenschaften und Steuerelementmuster verfügbar zu machen, ohne dass eine vollständige Implementierung von Benutzeroberflächenautomatisierung-Anbieterschnittstellen wie [**IRawElementProviderFragment erforderlich ist.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) Um **IAccessibleEx**, **IRawElementProviderFragment** und alle anderen Benutzeroberflächenautomatisierung-Schnittstellen zu verwenden, schließen Sie die Headerdatei UIAutomation.h in Ihren Quellcode ein.

Stellen Sie sich beispielsweise ein benutzerdefiniertes Steuerelement vor, das über einen Bereichswert verfügt. Der Microsoft Active Accessibility für das Steuerelement definiert die Rolle des Steuerelements und kann seinen aktuellen Wert zurückgeben. Da Microsoft Active Accessibility jedoch keine minimalen und maximalen Eigenschaften definiert, verfügt der Server nicht über die Möglichkeit, die minimalen und maximalen Werte des Steuerelements zurück zu geben. Ein Benutzeroberflächenautomatisierung-Client kann die Rolle, den aktuellen Wert und andere Microsoft Active Accessibility-Eigenschaften des Steuerelements abrufen, da der Benutzeroberflächenautomatisierung-Kern diese über [**IAccessible abrufen kann.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Ohne Zugriff auf eine [**IRangeValueProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) für das -Objekt kann Benutzeroberflächenautomatisierung jedoch auch nicht die maximalen und minimalen Werte abrufen.

Der Steuerelemententwickler könnte einen vollständigen Benutzeroberflächenautomatisierung-Anbieter für das Steuerelement zur Verfügung stellen, aber dies würde bedeuten, einen Großen Teil der vorhandenen Funktionalität der [**IAccessible-Implementierung**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) zu duplizieren: z. B. Navigation und allgemeine Eigenschaften. Stattdessen kann sich der Entwickler weiterhin auf **IAccessible** verlassen, um diese Funktionalität zu bieten, während unterstützung für steuerelementspezifische Eigenschaften über [**IRangeValueProvider hinzugefügt wird.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)

## <a name="in-this-section"></a>In diesem Abschnitt

-   [IAccessibleEx-Implementierungsrichtlinien](iaccessibleex-implementation-guidelines.md)
-   [Implementieren von IAccessibleEx für Anbieter](implementing-iaccessibleex-for-providers.md)
-   [Verwenden von IAccessibleEx über einen Client](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Infrastruktur](common-infrastructure.md)
</dt> </dl>

 

 




