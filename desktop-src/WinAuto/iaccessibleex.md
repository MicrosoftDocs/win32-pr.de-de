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
# <a name="the-iaccessibleex-interface"></a><span data-ttu-id="dd4e1-103">Die iaccessibleex-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dd4e1-103">The IAccessibleEx Interface</span></span>

<span data-ttu-id="dd4e1-104">Steuerelemente, die nicht über einen Microsoft-Benutzeroberflächenautomatisierungs-Anbieter verfügen, aber [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementieren, können problemlos aktualisiert werden, um einige Funktionen zur Automatisierung der Benutzeroberfläche durch Implementieren der [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle bereitzustellen</span><span class="sxs-lookup"><span data-stu-id="dd4e1-104">Controls that do not have a Microsoft UI Automation provider, but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), can easily be upgraded to provide some UI Automation functionality by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="dd4e1-105">Diese Schnittstelle ermöglicht es dem Steuerelement, Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Muster verfügbar zu machen, ohne dass eine vollständige Implementierung von Schnittstellen für Benutzeroberflächenautomatisierungs-Anbieter wie [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)</span><span class="sxs-lookup"><span data-stu-id="dd4e1-105">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="dd4e1-106">Um **iaccessibleex**, **IRawElementProviderFragment** und alle anderen Benutzeroberflächenautomatisierungs-Schnittstellen zu verwenden, fügen Sie die uiautomation. h-Header Datei in Ihren Quellcode ein.</span><span class="sxs-lookup"><span data-stu-id="dd4e1-106">To use **IAccessibleEx**, **IRawElementProviderFragment**, and all other UI Automation interfaces, include the UIAutomation.h header file in your source code.</span></span>

<span data-ttu-id="dd4e1-107">Angenommen, Sie haben ein benutzerdefiniertes Steuerelement, das über einen Bereichs Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="dd4e1-107">For example, consider a custom control that has a range value.</span></span> <span data-ttu-id="dd4e1-108">Der Microsoft Active Accessibility Server für das Steuerelement definiert die Rolle des Steuer Elements und kann seinen aktuellen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dd4e1-108">The Microsoft Active Accessibility server for the control defines the control's role and is able to return its current value.</span></span> <span data-ttu-id="dd4e1-109">Da in Microsoft Active Accessibility jedoch keine Mindest-und höchst Eigenschaften definiert sind, verfügt der Server nicht über die Möglichkeit, die minimalen und maximalen Werte des Steuer Elements zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="dd4e1-109">However, because Microsoft Active Accessibility does not define minimum and maximum properties, the server lacks the means to return the minimum and maximum values of the control.</span></span> <span data-ttu-id="dd4e1-110">Ein Benutzeroberflächenautomatisierungs-Client kann die Rolle, den aktuellen Wert und andere Eigenschaften von Microsoft Active Accessibility abrufen, da der Benutzeroberflächenautomatisierungs-Kern diese über [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="dd4e1-110">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="dd4e1-111">Ohne Zugriff auf eine [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) -Schnittstelle für das Objekt kann die Benutzeroberflächen Automatisierung jedoch auch nicht die maximalen und minimalen Werte abrufen.</span><span class="sxs-lookup"><span data-stu-id="dd4e1-111">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="dd4e1-112">Der Steuerelement Entwickler könnte einen kompletten Benutzeroberflächenautomatisierungs-Anbieter für das Steuerelement bereitstellen. Dies würde jedoch bedeuten, dass ein Großteil der vorhandenen Funktionen der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung duplizieren würde, z. b. Navigation und allgemeine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd4e1-112">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="dd4e1-113">Stattdessen kann sich der Entwickler weiterhin auf **IAccessible** verlassen, um diese Funktionalität bereitzustellen, und gleichzeitig Unterstützung für Steuerelement spezifische Eigenschaften durch [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dd4e1-113">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dd4e1-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="dd4e1-114">In this section</span></span>

-   [<span data-ttu-id="dd4e1-115">Iaccessibleex-Implementierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="dd4e1-115">IAccessibleEx Implementation Guidelines</span></span>](iaccessibleex-implementation-guidelines.md)
-   [<span data-ttu-id="dd4e1-116">Implementieren von iaccessibleex für Anbieter</span><span class="sxs-lookup"><span data-stu-id="dd4e1-116">Implementing IAccessibleEx for Providers</span></span>](implementing-iaccessibleex-for-providers.md)
-   [<span data-ttu-id="dd4e1-117">Verwenden von iaccessibleex von einem Client</span><span class="sxs-lookup"><span data-stu-id="dd4e1-117">Using IAccessibleEx from a Client</span></span>](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a><span data-ttu-id="dd4e1-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd4e1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd4e1-119">Allgemeine Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="dd4e1-119">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




