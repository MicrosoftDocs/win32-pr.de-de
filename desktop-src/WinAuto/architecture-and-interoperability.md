---
title: Architektur und Interoperabilität
description: In diesem Thema wird die Architektur von Microsoft Active Accessibility und der Microsoft-Benutzeroberflächen Automatisierung sowie die Komponenten beschrieben, die die Interoperabilität zwischen Anwendungen auf der Grundlage der beiden unterschiedlichen Technologien ermöglichen.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "104101186"
---
# <a name="architecture-and-interoperability"></a><span data-ttu-id="9b2d4-103">Architektur und Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9b2d4-103">Architecture and Interoperability</span></span>

<span data-ttu-id="9b2d4-104">In diesem Thema wird die Architektur von Microsoft Active Accessibility und der Microsoft-Benutzeroberflächen Automatisierung sowie die Komponenten beschrieben, die die Interoperabilität zwischen Anwendungen auf der Grundlage der beiden unterschiedlichen Technologien ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-104">This topic briefly describes the architecture of Microsoft Active Accessibility and Microsoft UI Automation, and the components that allow interoperability between applications based on the two different technologies.</span></span>

<span data-ttu-id="9b2d4-105">Weitere Informationen zur Interoperabilität von Microsoft Active Accessibility und zur Benutzeroberflächen Automatisierung finden Sie unter [Common Infrastructure (allgemeine Infrastruktur](common-infrastructure.md)).</span><span class="sxs-lookup"><span data-stu-id="9b2d4-105">For more information about Microsoft Active Accessibility and UI Automation interoperability, see [Common Infrastructure](common-infrastructure.md).</span></span>

<span data-ttu-id="9b2d4-106">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="9b2d4-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9b2d4-107">Microsoft Active Accessibility-Architektur</span><span class="sxs-lookup"><span data-stu-id="9b2d4-107">Microsoft Active Accessibility Architecture</span></span>](#microsoft-active-accessibility-architecture)
-   [<span data-ttu-id="9b2d4-108">Architektur der Benutzeroberflächen Automatisierung</span><span class="sxs-lookup"><span data-stu-id="9b2d4-108">UI Automation Architecture</span></span>](#ui-automation-architecture)
-   [<span data-ttu-id="9b2d4-109">Interoperabilität von Microsoft Active Accessibility und UI-Automatisierung</span><span class="sxs-lookup"><span data-stu-id="9b2d4-109">Microsoft Active Accessibility and UI Automation Interoperability</span></span>](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [<span data-ttu-id="9b2d4-110">Die iaccessibleex-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9b2d4-110">The IAccessibleEx Interface</span></span>](#the-iaccessibleex-interface)
-   [<span data-ttu-id="9b2d4-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b2d4-111">Related topics</span></span>](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a><span data-ttu-id="9b2d4-112">Microsoft Active Accessibility-Architektur</span><span class="sxs-lookup"><span data-stu-id="9b2d4-112">Microsoft Active Accessibility Architecture</span></span>

<span data-ttu-id="9b2d4-113">Microsoft Active Accessibility stellt grundlegende Informationen zu Steuerelementen, wie z. b. den Steuerelement Namen, den Speicherort auf dem Bildschirm und die Art der Steuerung, sowie Zustandsinformationen wie Sichtbarkeit und aktivierten/deaktivierten</span><span class="sxs-lookup"><span data-stu-id="9b2d4-113">Microsoft Active Accessibility exposes basic information about controls such as control name, location on screen, and type of control, as well as state information such as visibility and enabled/disabled status.</span></span> <span data-ttu-id="9b2d4-114">Die Benutzeroberfläche wird als Hierarchie barrierefreier Objekte dargestellt. Änderungen und Aktionen werden als WinEvents dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-114">The UI is represented as a hierarchy of accessible objects; changes and actions are represented as WinEvents.</span></span>

<span data-ttu-id="9b2d4-115">Microsoft Active Accessibility besteht aus den folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="9b2d4-115">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="9b2d4-116">Barrierefreies Objekt – ein logisches UI-Element (z. b. eine Schaltfläche), das durch eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Component Object Model (com)-Schnittstelle und einen untergeordneten ganzzahligen Bezeichner (childID) dargestellt</span><span class="sxs-lookup"><span data-stu-id="9b2d4-116">Accessible object—A logical UI element (such as a button) that is represented by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Component Object Model (COM) interface and an integer child identifier (ChildID).</span></span>
-   <span data-ttu-id="9b2d4-117">WinEvents – ein Ereignis System, mit dem Server Clients benachrichtigen können, wenn ein Barrierefreies Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-117">WinEvents—An event system that enables servers to notify clients when an accessible object changes.</span></span> <span data-ttu-id="9b2d4-118">Weitere Informationen finden Sie unter [WinEvents](winevents-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="9b2d4-118">For more information, see [WinEvents](winevents-infrastructure.md).</span></span>
-   <span data-ttu-id="9b2d4-119">OLEACC.dll – die Laufzeit, Dynamic Link Library, die die Microsoft Active Accessibility-API und das Barrierefreiheits System Framework bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-119">OLEACC.dll—The run-time, dynamic-link library that provides the Microsoft Active Accessibility API and the accessibility system framework.</span></span> <span data-ttu-id="9b2d4-120">Oleacc implementiert Proxy Objekte, die standardmäßige Barrierefreiheits Informationen für Standardbenutzer Oberflächen Elemente bereitstellen, einschließlich Benutzer Steuerelemente, Benutzermenüs und allgemeine Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-120">OLEACC implements proxy objects that provide default accessibility information for standard UI elements, including USER controls, USER menus, and common controls.</span></span>

<span data-ttu-id="9b2d4-121">Bei Microsoft Active Accessibility unterstützt die Systemkomponente des Barrierefreiheits-Frameworks (oleacc) die Kommunikation zwischen Hilfstechnologien (Barrierefreiheits Tools) und Anwendungen, wie in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-121">For Microsoft Active Accessibility, the system component of the accessibility framework (OLEACC) helps the communication between assistive technologies (accessibility tools) and applications, as the following illustration shows.</span></span>

![Abbildung, die zeigt, wie Barrierefreiheits Tools mit Anwendungen interagieren](images/msaaarch.gif)

<span data-ttu-id="9b2d4-123">Die Anwendungen (Microsoft Active Accessibility-Server) stellen Informationen zur Benutzeroberflächen-Barrierefreiheit für Tools (Microsoft Active Accessibility-Clients) bereit, die im Namen von Benutzern mit der Benutzeroberfläche interagieren.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-123">The applications (Microsoft Active Accessibility servers) provide UI accessibility information to tools (Microsoft Active Accessibility clients), which interact with the UI on behalf of users.</span></span> <span data-ttu-id="9b2d4-124">Die Code Grenze ist sowohl eine programmgesteuerte als auch eine Prozess Grenze.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-124">The code boundary is both a programmatic and a process boundary.</span></span>

## <a name="ui-automation-architecture"></a><span data-ttu-id="9b2d4-125">Architektur der Benutzeroberflächen Automatisierung</span><span class="sxs-lookup"><span data-stu-id="9b2d4-125">UI Automation Architecture</span></span>

<span data-ttu-id="9b2d4-126">Bei der Automatisierung der Benutzeroberfläche wird die Benutzeroberflächenautomatisierungs-Kernkomponente (UIAutomationCore.dll) sowohl in die Tools für die Barrierefreiheit als auch in die Anwendungsprozesse geladen.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-126">With UI Automation, the UI Automation core component (UIAutomationCore.dll) is loaded into both the accessibility tools' and applications' processes.</span></span> <span data-ttu-id="9b2d4-127">Die Kernkomponente verwaltet die prozessübergreifende Kommunikation, bietet Dienste höherer Ebene, wie z. b. das Suchen nach Elementen nach Eigenschafts Werten, und ermöglicht das Massen abrufen oder Zwischenspeichern von Eigenschaften, was eine bessere Leistung als die Implementierung von Microsoft Active Accessibility bietet.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-127">The core component manages cross-process communication, provides higher level services such as searching for elements by property values, and enables bulk fetching or caching of properties, which provides better performance than the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="9b2d4-128">Die Benutzeroberflächen Automatisierung umfasst Proxy Objekte, die Benutzeroberflächen Informationen über Standardbenutzer Oberflächen Elemente wie Benutzer Steuerelemente, Benutzermenüs und allgemeine Steuerelemente bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-128">UI Automation includes proxy objects that provide UI information about standard UI elements such as USER controls, USER menus, and common controls.</span></span> <span data-ttu-id="9b2d4-129">Außerdem sind Proxys enthalten, mit denen Benutzeroberflächenautomatisierungs-Clients Benutzeroberflächen Informationen von Microsoft Active Accessibility-Servern erhalten.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-129">It also includes proxies that enable UI Automation clients to get UI information from Microsoft Active Accessibility servers.</span></span>

<span data-ttu-id="9b2d4-130">Die folgende Abbildung zeigt die Beziehungen zwischen den verschiedenen Benutzeroberflächenautomatisierungs-Komponenten, die in Barrierefreiheits Tools (Clients) und in Anwendungen (Anbietern) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-130">The following illustration shows the relationships among the various UI Automation compontents used in accessibility tools (clients) and in applications (providers).</span></span>

![Abbildung, die zeigt, wie Komponenten von Barrierefreiheits Tools mit Anwendungen in Anwendungen interagieren](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a><span data-ttu-id="9b2d4-132">Interoperabilität von Microsoft Active Accessibility und UI-Automatisierung</span><span class="sxs-lookup"><span data-stu-id="9b2d4-132">Microsoft Active Accessibility and UI Automation Interoperability</span></span>

<span data-ttu-id="9b2d4-133">Mithilfe der Benutzeroberflächen Automatisierung an Microsoft Active Accessibility Bridge können Microsoft Active Accessibility-Clients auf Benutzeroberflächenautomatisierungs-Anbieter zugreifen, indem Sie das Objektmodell für die Benutzeroberflächen Automatisierung in ein Microsoft Active Accessibility-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="9b2d4-133">The UI Automation to Microsoft Active Accessibility Bridge enables Microsoft Active Accessibility clients to access UI Automation providers by converting the UI Automation object model to a Microsoft Active Accessibility object model.</span></span> <span data-ttu-id="9b2d4-134">In der folgenden Abbildung wird die Rolle der Benutzeroberflächen Automatisierung-zu-Microsoft-Active Accessibility Bridge gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-134">The following illustration shows the role of the UI Automation-to-Microsoft Active Accessibility Bridge.</span></span>

![Darstellung der Funktionsweise der Benutzeroberflächen Automatisierung mit Barrierefreiheits Tools und-Anwendungen](images/uiatomsaabridge.gif)

<span data-ttu-id="9b2d4-136">Entsprechend übersetzt der Microsoft Active Accessibility-to-UI-Automatisierungs Proxy Microsoft Active Accessibility-basierte Server Objekt Modelle für Benutzeroberflächenautomatisierungs-Clients.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-136">Similarly, the Microsoft Active Accessibility-to-UI Automation Proxy translates Microsoft Active Accessibility-based server object models for UI Automation clients.</span></span> <span data-ttu-id="9b2d4-137">In der folgenden Abbildung wird die Rolle des Microsoft Active Accessibility-to-UI-Automatisierungs Proxys gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-137">The following illustration shows the role of the Microsoft Active Accessibility-to-UI Automation Proxy.</span></span>

![Abbildung der Funktionsweise des Benutzeroberflächenautomatisierungs-Proxys mit Tools und Anwendungen](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a><span data-ttu-id="9b2d4-139">Die iaccessibleex-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9b2d4-139">The IAccessibleEx Interface</span></span>

<span data-ttu-id="9b2d4-140">Mit der [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle können vorhandene Anwendungen oder Benutzeroberflächen Bibliotheken Ihr Microsoft Active Accessibility-Objektmodell erweitern, um die Benutzeroberflächen Automatisierung zu unterstützen, ohne die Implementierung von Grund auf neu schreiben</span><span class="sxs-lookup"><span data-stu-id="9b2d4-140">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface enables existing applications or UI libraries to extend their Microsoft Active Accessibility object model to support UI Automation without rewriting the implementation from scratch.</span></span> <span data-ttu-id="9b2d4-141">Mit **iaccessibleex** können Sie nur die zusätzlichen Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Muster implementieren, die erforderlich sind, um die Benutzeroberfläche und ihre Funktionalität vollständig zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-141">With **IAccessibleEx**, you can implement only the additional UI Automation properties and control patterns needed to fully describe the UI and its functionality.</span></span>

<span data-ttu-id="9b2d4-142">Da der Microsoft Active Accessibility-to-UI-Automatisierungs Proxy die Objekt Modelle von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)-fähigen Microsoft Active Accessibility Servern als Benutzeroberflächenautomatisierungs-Objekt Modelle übersetzt, müssen Benutzeroberflächenautomatisierungs-Clients keine zusätzlichen Aufgaben erledigen.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-142">Because the Microsoft Active Accessibility-to-UI Automation Proxy translates the object models of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)-enabled Microsoft Active Accessibility servers as UI Automation object models, UI Automation clients do not need to do any extra work.</span></span> <span data-ttu-id="9b2d4-143">Mit der **iaccessibleex** -Schnittstelle können auch Prozess interne Microsoft Active Accessibility-Clients für die direkte Interaktion mit Benutzeroberflächenautomatisierungs-Anbietern aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="9b2d4-143">The **IAccessibleEx** interface can also enable in-process Microsoft Active Accessibility clients to interact directly with UI Automation providers.</span></span>

<span data-ttu-id="9b2d4-144">Weitere Informationen finden Sie [unter iaccessibleex Interface](iaccessibleex.md).</span><span class="sxs-lookup"><span data-stu-id="9b2d4-144">For more information, see [The IAccessibleEx Interface](iaccessibleex.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b2d4-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b2d4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b2d4-146">Übersicht über die Windows Automation-API</span><span class="sxs-lookup"><span data-stu-id="9b2d4-146">Windows Automation API Overview</span></span>](windows-automation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="9b2d4-147">Die iaccessibleex-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9b2d4-147">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> <dt>

[<span data-ttu-id="9b2d4-148">Sicherheitsüberlegungen für Hilfstechnologien</span><span class="sxs-lookup"><span data-stu-id="9b2d4-148">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
</dt> </dl>

 

 




