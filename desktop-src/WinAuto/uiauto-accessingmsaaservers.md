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
# <a name="accessing-microsoft-active-accessibility-servers"></a><span data-ttu-id="e448b-112">Zugreifen auf Microsoft Active Accessibility-Server</span><span class="sxs-lookup"><span data-stu-id="e448b-112">Accessing Microsoft Active Accessibility Servers</span></span>

<span data-ttu-id="e448b-113">Der Microsoft-Active Accessibility für Benutzeroberflächenautomatisierungs-Proxy ist eine Softwarekomponente, mit der Microsoft UI Automation-Clients mit Microsoft-Active Accessibility Servern interagieren können, die die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle System intern implementieren.</span><span class="sxs-lookup"><span data-stu-id="e448b-113">The Microsoft Active Accessibility to UI Automation Proxy is a software component that enables Microsoft UI Automation clients to interact with Microsoft Active Accessibility servers that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface natively.</span></span> <span data-ttu-id="e448b-114">Der Proxy unterstützt das [legacyibarrierefreie](uiauto-implementinglegacyiaccessible.md) -Steuerelement Muster und stellt eine Instanz der [**iuiautomationlegacyiaccessiblepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) -Schnittstelle für jeden erkannten Microsoft Active Accessibility Server bereit.</span><span class="sxs-lookup"><span data-stu-id="e448b-114">The proxy supports the [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) control pattern, and supplies an instance of the [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface for each Microsoft Active Accessibility server detected.</span></span> <span data-ttu-id="e448b-115">Benutzeroberflächenautomatisierungs-Clients verwenden die von **iuiautomationlegacyiaccessiblepattern** verfügbar gemachten Methoden, um auf die Eigenschaften und Objekte von Microsoft Active Accessibility zuzugreifen, die vom Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e448b-115">UI Automation clients use the methods exposed by **IUIAutomationLegacyIAccessiblePattern** to access the Microsoft Active Accessibility properties and objects supported by the server.</span></span>

<span data-ttu-id="e448b-116">Wenn ein Benutzeroberflächenautomatisierungs-Element eine zugrunde liegende Microsoft Active Accessibility-Implementierung aufweist, kann ein Client einen [**iuiautomationlegacyiaccessiblepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) -Schnittstellen Zeiger für das Element abrufen, indem er die [**UIA \_ legacyiaccessiblepatternid**](uiauto-controlpattern-ids.md) -Steuerelement Muster-ID an eine der folgenden [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Methoden übergibt:</span><span class="sxs-lookup"><span data-stu-id="e448b-116">If a UI Automation element has an underlying Microsoft Active Accessibility implementation, a client can obtain an [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface pointer for the element by passing the [**UIA\_LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) control pattern ID to one of the following [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) methods:</span></span>

-   [<span data-ttu-id="e448b-117">**GetCachedPattern**</span><span class="sxs-lookup"><span data-stu-id="e448b-117">**GetCachedPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [<span data-ttu-id="e448b-118">**Getcachedpatternas**</span><span class="sxs-lookup"><span data-stu-id="e448b-118">**GetCachedPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [<span data-ttu-id="e448b-119">**GetCurrentPattern**</span><span class="sxs-lookup"><span data-stu-id="e448b-119">**GetCurrentPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [<span data-ttu-id="e448b-120">**Getcurrentpatternas**</span><span class="sxs-lookup"><span data-stu-id="e448b-120">**GetCurrentPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

<span data-ttu-id="e448b-121">Die [**iuiautomationlegacyiaccessiblepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) -Schnittstelle ist für Steuerelemente, die auf der Benutzeroberflächen Automatisierung basieren, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e448b-121">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface is not available for controls based on UI Automation.</span></span>

<span data-ttu-id="e448b-122">Die [**iuiautomationlegacyiaccessiblepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) -Schnittstelle ermöglicht Benutzeroberflächenautomatisierungs-Clients den Zugriff auf die zugrunde liegende [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung eines Microsoft Active Accessibility-Elements.</span><span class="sxs-lookup"><span data-stu-id="e448b-122">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface enables UI Automation clients to access the underlying [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation of an Microsoft Active Accessibility element.</span></span> <span data-ttu-id="e448b-123">Die-Schnittstelle unterstützt jedoch keine Methoden, die mit Benutzeroberflächenautomatisierungs-Features veraltet oder redundant sind.</span><span class="sxs-lookup"><span data-stu-id="e448b-123">However, the interface does not support methods that are obsolete or redundant with UI Automation features.</span></span> <span data-ttu-id="e448b-124">**Iuiautomationlegacyiaccessiblepattern** verfügt beispielsweise nicht über eine-Methode, die [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) entspricht, da der aktuelle Speicherort eines UI-Elements über die Eigenschaft "UI Automation boundingrechteck" verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e448b-124">For example, **IUIAutomationLegacyIAccessiblePattern** does not have a method that is equivalent to [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because the current location of a UI element is available from the UI Automation BoundingRectangle property.</span></span>

<span data-ttu-id="e448b-125">Die [**iuiautomationlegacyiaccessiblepattern:: getiaccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) -Methode ermöglicht einem Client das Abrufen eines [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeigers von einem Benutzeroberflächenautomatisierungs-Element.</span><span class="sxs-lookup"><span data-stu-id="e448b-125">The [**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) method enables a client to retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer from an UI Automation element.</span></span> <span data-ttu-id="e448b-126">Das Gegenteil ist auch möglich, wenn die Methoden [**iuiautomation:: elementfromiaccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) und [**iuiautomation:: elementfromiaccessiblebuildcache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e448b-126">The reverse is also possible by using the [**IUIAutomation::ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) and [**IUIAutomation::ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) methods.</span></span>

<span data-ttu-id="e448b-127">[**Iuiautomationlegacyiaccessiblepattern:: getiaccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) gibt **null** zurück, wenn die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für das Element von einem Proxy Objekt von OLEACC.dll oder von der Benutzeroberflächen Automatisierung an Microsoft Active Accessibility Bridge bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e448b-127">[**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) returns **NULL** if the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element is provided by a proxy object from OLEACC.dll or from the UI Automation to Microsoft Active Accessibility Bridge.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e448b-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e448b-128">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e448b-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="e448b-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e448b-130">Benutzeroberflächenautomatisierungs-und Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="e448b-130">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
</dt> <dt>

[<span data-ttu-id="e448b-131">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="e448b-131">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




