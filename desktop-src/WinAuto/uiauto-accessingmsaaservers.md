---
title: Zugreifen auf Microsoft Active Accessibility Server
description: Die Microsoft Active Accessibility des Benutzeroberflächenautomatisierung Proxys ist eine Softwarekomponente, mit der Microsoft Benutzeroberflächenautomatisierung-Clients mit Microsoft Active Accessibility-Servern interagieren können, die die IAccessible-Schnittstelle nativ implementieren.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Benutzeroberflächenautomatisierung,Zugreifen auf Active Accessibility
- Benutzeroberflächenautomatisierung,Active Accessibility
- Benutzeroberflächenautomatisierung Proxy
- Benutzeroberflächenautomatisierung,Benutzeroberflächenautomatisierung Proxy
- LegacyIAccessible-Steuerelementmuster
- Benutzeroberflächenautomatisierung,LegacyIAccessible-Steuerelementmuster
- Microsoft Active Accessibility
- Active Accessibility
- Clients,Zugreifen auf Active Accessibility Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6f6ccbc29695b7ca5d1413025a50a7bcf4a9cf679dbcd6a0b8f3160ff0b399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030770"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a>Zugreifen auf Microsoft Active Accessibility Server

Der Microsoft Active Accessibility zu Benutzeroberflächenautomatisierung Proxy ist eine Softwarekomponente, mit der Microsoft Benutzeroberflächenautomatisierung-Clients mit Microsoft Active Accessibility-Servern interagieren können, die die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativ implementieren. Der Proxy unterstützt das [LegacyIAccessible-Steuerelementmuster](uiauto-implementinglegacyiaccessible.md) und stellt eine Instanz der [**IUIAutomationLegacyIAccessiblePattern-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) für jeden erkannten Microsoft Active Accessibility bereit. Benutzeroberflächenautomatisierung clients verwenden die methoden, die von **IUIAutomationLegacyIAccessiblePattern** verfügbar gemacht werden, um auf die Microsoft Active Accessibility Eigenschaften und Objekte zu zugreifen, die vom Server unterstützt werden.

Wenn ein Benutzeroberflächenautomatisierung-Element über eine zugrunde liegende Microsoft Active Accessibility-Implementierung verfügt, kann ein Client einen [**IUIAutomationLegacyIAccessiblePattern-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) für das Element abrufen, indem die [**UIA \_ LegacyIAccessiblePatternId-Steuerelementmuster-ID**](uiauto-controlpattern-ids.md) an eine der folgenden [**IUIAutomationElement-Methoden**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) übergeben wird:

-   [**GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [**GetCachedPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [**Getcurrentpattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [**GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

Die [**IUIAutomationLegacyIAccessiblePattern-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) ist nicht für Steuerelemente verfügbar, die auf Benutzeroberflächenautomatisierung.

Die [**IUIAutomationLegacyIAccessiblePattern-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) ermöglicht Benutzeroberflächenautomatisierung Clients den Zugriff auf die zugrunde liegende [**IAccessible-Implementierung**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) eines Microsoft Active Accessibility Elements. Die -Schnittstelle unterstützt jedoch keine Methoden, die veraltet oder redundant mit Benutzeroberflächenautomatisierung sind. **IUIAutomationLegacyIAccessiblePattern** verfügt beispielsweise nicht über eine Methode, die [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) entspricht, da der aktuelle Speicherort eines Benutzeroberflächenelements über die Benutzeroberflächenautomatisierung BoundingRectangle-Eigenschaft verfügbar ist.

Mit [**der IUIAutomationLegacyIAccessiblePattern::GetIAccessible-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) kann ein Client einen [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) aus einem Benutzeroberflächenautomatisierung abrufen. Das Gegenteil ist auch mithilfe der [**Methoden IUIAutomation::ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) und [**IUIAutomation::ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) möglich.

[**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) gibt **NULL** zurück, wenn die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für das Element von einem Proxyobjekt aus OLEACC.dll oder vom Benutzeroberflächenautomatisierung zum Microsoft Active Accessibility Bridge bereitgestellt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Benutzeroberflächenautomatisierung und Active Accessibility](uiauto-msaa.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




