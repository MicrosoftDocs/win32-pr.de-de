---
title: Grundlagen der Benutzeroberflächenautomatisierung
description: In diesem Abschnitt werden die grundlegenden Konzepte erläutert, auf denen die Benutzeroberflächen Automatisierung basiert.
ms.assetid: 109f113f-9ed0-4a57-b3af-90e831e53c42
keywords:
- Benutzeroberflächen Automatisierung, Microsoft Win32-API
- UI-Automatisierung, Win32-API
- Benutzeroberflächen Automatisierung, Anbieter
- Benutzeroberflächen Automatisierung, Client Anwendungen
- Clients, Microsoft UI Automation für die Microsoft Win32-API
- Clients, UI-Automatisierung für die Microsoft Win32-API
- Win32 API
- Microsoft Win32-API
- UI-Automatisierung für die Microsoft Win32-API
- Microsoft-Benutzeroberflächen Automatisierung für die Win32-API von Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba8147a8dd7f8d03340fad43465c225a174e606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388525"
---
# <a name="ui-automation-fundamentals"></a><span data-ttu-id="202fe-113">Grundlagen der Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="202fe-113">UI Automation Fundamentals</span></span>

<span data-ttu-id="202fe-114">Die Microsoft-Benutzeroberflächen Automatisierung ermöglicht Hilfstechnologieanwendungen und automatisierten Testtools die Interaktion mit den UI-Steuerelementen anderer Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="202fe-114">Microsoft UI Automation enables assistive technology applications and automated testing tools to interact with the UI controls of other applications.</span></span> <span data-ttu-id="202fe-115">In diesem Abschnitt werden die grundlegenden Konzepte erläutert, auf denen die Benutzeroberflächen Automatisierung basiert.</span><span class="sxs-lookup"><span data-stu-id="202fe-115">This section explains the fundamental concepts that UI Automation is based on.</span></span>

<span data-ttu-id="202fe-116">Die API für die Benutzeroberflächen Automatisierung besteht aus zwei Teilen.</span><span class="sxs-lookup"><span data-stu-id="202fe-116">The UI Automation API is in two parts.</span></span> <span data-ttu-id="202fe-117">Ein Teil wird von Benutzeroberflächenautomatisierungs- *Anbieter* Anwendungen verwendet, der andere wird von Benutzeroberflächenautomatisierungs- *Client* Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="202fe-117">One part is used by *UI Automation provider* applications, and the other is used by *UI Automation client* applications.</span></span> <span data-ttu-id="202fe-118">Die Anbieter-API ermöglicht Entwicklern von benutzerdefinierten Microsoft Win32-Steuerelementen und anderen Steuerungs Frameworks, diese Steuerelemente für die Benutzeroberflächen Automatisierung verfügbar zu machen und für Client Anwendungen sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="202fe-118">The provider API enables developers of Microsoft Win32 custom control and other control frameworks to expose those controls to UI Automation and make them visible to client applications.</span></span> <span data-ttu-id="202fe-119">Die Client-API ermöglicht Anwendungen die Interaktion mit Steuerelementen in anderen Anwendungen und das Abrufen von Informationen zu diesen.</span><span class="sxs-lookup"><span data-stu-id="202fe-119">The client API enables applications to interact with controls in other applications and retrieve information about them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="202fe-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="202fe-120">In this section</span></span>

-   [<span data-ttu-id="202fe-121">Übersicht über die Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="202fe-121">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
-   [<span data-ttu-id="202fe-122">Benutzeroberflächenautomatisierungs-und Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="202fe-122">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
-   [<span data-ttu-id="202fe-123">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="202fe-123">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
-   [<span data-ttu-id="202fe-124">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="202fe-124">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
-   [<span data-ttu-id="202fe-125">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="202fe-125">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
-   [<span data-ttu-id="202fe-126">Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="202fe-126">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
-   [<span data-ttu-id="202fe-127">Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="202fe-127">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
-   [<span data-ttu-id="202fe-128">Benutzerdefinierte Eigenschaften, Ereignisse und Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="202fe-128">Custom Properties, Events, and Control Patterns</span></span>](uiauto-custompropertieseventscontrolpatterns.md)
-   [<span data-ttu-id="202fe-129">Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte</span><span class="sxs-lookup"><span data-stu-id="202fe-129">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
-   [<span data-ttu-id="202fe-130">Benutzeroberflächenautomatisierungs-Unterstützung für Drag & Drop</span><span class="sxs-lookup"><span data-stu-id="202fe-130">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
-   [<span data-ttu-id="202fe-131">Sicherheitsüberlegungen für Hilfstechnologien</span><span class="sxs-lookup"><span data-stu-id="202fe-131">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
-   [<span data-ttu-id="202fe-132">Bewährte Methoden für die Verwendung von sicheren Arrays</span><span class="sxs-lookup"><span data-stu-id="202fe-132">Best Practices for Using Safe Arrays</span></span>](uiauto-workingwithsafearrays.md)
-   [<span data-ttu-id="202fe-133">Spezifikation für die Benutzeroberflächenautomatisierung und Zusicherung an die Community</span><span class="sxs-lookup"><span data-stu-id="202fe-133">UI Automation Specification and Community Promise</span></span>](uiauto-specandcommunitypromise.md)

## <a name="related-topics"></a><span data-ttu-id="202fe-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="202fe-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="202fe-135">Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="202fe-135">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




