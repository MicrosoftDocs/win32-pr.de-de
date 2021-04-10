---
title: Zugreifen auf Microsoft Active Accessibility-Server
description: Der Microsoft-Active Accessibility für Benutzeroberflächenautomatisierungs-Proxy ist eine Softwarekomponente, mit der Microsoft UI Automation-Clients mit Microsoft-Active Accessibility Servern interagieren können, die die IAccessible-Schnittstelle System intern implementieren.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Benutzeroberflächen Automatisierung, Zugriff auf Active Accessibility
- Benutzeroberflächen Automatisierung, Active Accessibility
- UI-Automatisierungs Proxy
- UI-Automatisierung, Benutzeroberflächenautomatisierungs-Proxy
- Legacyiaccessible-Steuerelement Muster
- Benutzeroberflächenautomatisierungs, legacyibarrierefreiheits-Steuerelement Muster
- Microsoft Active Accessibility
- Active Accessibility
- Clients, zugreifen auf Active Accessibility Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97319028203351cd9f45b39d133fa38727d6861e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036661"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a>Zugreifen auf Microsoft Active Accessibility-Server

Der Microsoft-Active Accessibility für Benutzeroberflächenautomatisierungs-Proxy ist eine Softwarekomponente, mit der Microsoft UI Automation-Clients mit Microsoft-Active Accessibility Servern interagieren können, die die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle System intern implementieren. Der Proxy unterstützt das [legacyibarrierefreie](uiauto-implementinglegacyiaccessible.md) -Steuerelement Muster und stellt eine Instanz der [**iuiautomationlegacyiaccessiblepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) -Schnittstelle für jeden erkannten Microsoft Active Accessibility Server bereit. Benutzeroberflächenautomatisierungs-Clients verwenden die von **iuiautomationlegacyiaccessiblepattern** verfügbar gemachten Methoden, um auf die Eigenschaften und Objekte von Microsoft Active Accessibility zuzugreifen, die vom Server unterstützt werden.

Wenn ein Benutzeroberflächenautomatisierungs-Element eine zugrunde liegende Microsoft Active Accessibility-Implementierung aufweist, kann ein Client einen [**iuiautomationlegacyiaccessiblepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) -Schnittstellen Zeiger für das Element abrufen, indem er die [**UIA \_ legacyiaccessiblepatternid**](uiauto-controlpattern-ids.md) -Steuerelement Muster-ID an eine der folgenden [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Methoden übergibt:

-   [**GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [**Getcachedpatternas**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [**GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [**Getcurrentpatternas**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

Die [**iuiautomationlegacyiaccessiblepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) -Schnittstelle ist für Steuerelemente, die auf der Benutzeroberflächen Automatisierung basieren, nicht verfügbar.

Die [**iuiautomationlegacyiaccessiblepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) -Schnittstelle ermöglicht Benutzeroberflächenautomatisierungs-Clients den Zugriff auf die zugrunde liegende [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung eines Microsoft Active Accessibility-Elements. Die-Schnittstelle unterstützt jedoch keine Methoden, die mit Benutzeroberflächenautomatisierungs-Features veraltet oder redundant sind. **Iuiautomationlegacyiaccessiblepattern** verfügt beispielsweise nicht über eine-Methode, die [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) entspricht, da der aktuelle Speicherort eines UI-Elements über die Eigenschaft "UI Automation boundingrechteck" verfügbar ist.

Die [**iuiautomationlegacyiaccessiblepattern:: getiaccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) -Methode ermöglicht einem Client das Abrufen eines [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeigers von einem Benutzeroberflächenautomatisierungs-Element. Das Gegenteil ist auch möglich, wenn die Methoden [**iuiautomation:: elementfromiaccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) und [**iuiautomation:: elementfromiaccessiblebuildcache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) verwendet werden.

[**Iuiautomationlegacyiaccessiblepattern:: getiaccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) gibt **null** zurück, wenn die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für das Element von einem Proxy Objekt von OLEACC.dll oder von der Benutzeroberflächen Automatisierung an Microsoft Active Accessibility Bridge bereitgestellt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Benutzeroberflächenautomatisierungs-und Active Accessibility](uiauto-msaa.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




