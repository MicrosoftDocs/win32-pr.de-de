---
title: Benutzeroberflächenautomatisierungs-Client Programmiererhandbuch
description: Dieser Abschnitt enthält Informationen zum Erstellen von Anwendungen, die Microsoft UI Automation für die Interaktion mit der Benutzeroberfläche von anderen Anwendungen und dem Desktop verwenden.
ms.assetid: d3616e1f-7b38-4a3e-ac96-72ec70cc13fc
keywords:
- Erstellen von Benutzeroberflächen Automatisierungs-Client Anwendungen
- Erstellen von Client Anwendungen
- Clients, Erstellen von Benutzeroberflächenautomatisierungs-Anwendungen
- Clients, Benutzeroberflächenautomatisierungs-Anwendungs Erstellung
- Benutzeroberflächen Automatisierung, Erstellen von Client Anwendungen
- Benutzeroberflächen Automatisierung, Erstellung von Client Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f353243c8c194e2d732efd1d68bc2894ca930285
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727720"
---
# <a name="ui-automation-client-programmers-guide"></a><span data-ttu-id="4b314-109">Benutzeroberflächenautomatisierungs-Client Programmiererhandbuch</span><span class="sxs-lookup"><span data-stu-id="4b314-109">UI Automation Client Programmer's Guide</span></span>

<span data-ttu-id="4b314-110">Dieser Abschnitt enthält Informationen zum Erstellen von Anwendungen, die Microsoft UI Automation für die Interaktion mit der Benutzeroberfläche von anderen Anwendungen und dem Desktop verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b314-110">This section contains information about creating applications that use Microsoft UI Automation to interact with the UI of other applications and the desktop.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4b314-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4b314-111">In this section</span></span>

-   [<span data-ttu-id="4b314-112">Übersicht über UI-Automatisierungs Clients</span><span class="sxs-lookup"><span data-stu-id="4b314-112">UI Automation Clients Overview</span></span>](/windows/desktop/WinAuto/uiauto-clientsoverview)
-   [<span data-ttu-id="4b314-113">Erstellen des cuiautomation-Objekts</span><span class="sxs-lookup"><span data-stu-id="4b314-113">Creating the CUIAutomation Object</span></span>](uiauto-creatingcuiautomation.md)
-   [<span data-ttu-id="4b314-114">Abrufen von Benutzeroberflächenautomatisierungs-Elementen</span><span class="sxs-lookup"><span data-stu-id="4b314-114">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
-   [<span data-ttu-id="4b314-115">Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen</span><span class="sxs-lookup"><span data-stu-id="4b314-115">Retrieving Properties from UI Automation Elements</span></span>](uiauto-propertiesforclients.md)
-   [<span data-ttu-id="4b314-116">Zwischenspeichern von Eigenschaften der Benutzeroberflächen Automatisierung und Steuerelement Mustern</span><span class="sxs-lookup"><span data-stu-id="4b314-116">Caching UI Automation Properties and Control Patterns</span></span>](uiauto-cachingforclients.md)
-   [<span data-ttu-id="4b314-117">Abonnieren von Benutzeroberflächenautomatisierungs-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="4b314-117">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
-   [<span data-ttu-id="4b314-118">Arbeiten mit Text basierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="4b314-118">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
-   [<span data-ttu-id="4b314-119">Arbeiten mit virtualisierten Elementen</span><span class="sxs-lookup"><span data-stu-id="4b314-119">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
-   [<span data-ttu-id="4b314-120">Zugreifen auf Microsoft Active Accessibility-Server</span><span class="sxs-lookup"><span data-stu-id="4b314-120">Accessing Microsoft Active Accessibility Servers</span></span>](uiauto-accessingmsaaservers.md)
-   [<span data-ttu-id="4b314-121">Verwenden von Benutzeroberflächenautomatisierung für automatisierte Tests</span><span class="sxs-lookup"><span data-stu-id="4b314-121">Using UI Automation for Automated Testing</span></span>](uiauto-usefortesting.md)
-   [<span data-ttu-id="4b314-122">Grundlegendes zur Bildschirm Skalierung</span><span class="sxs-lookup"><span data-stu-id="4b314-122">Understanding Screen Scaling Issues</span></span>](uiauto-screenscaling.md)
-   [<span data-ttu-id="4b314-123">Grundlegendes zu Threading Problemen</span><span class="sxs-lookup"><span data-stu-id="4b314-123">Understanding Threading Issues</span></span>](uiauto-threading.md)
-   [<span data-ttu-id="4b314-124">Themen zur Vorgehensweise für Benutzeroberflächenautomatisierungs-Clients</span><span class="sxs-lookup"><span data-stu-id="4b314-124">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)

## <a name="related-topics"></a><span data-ttu-id="4b314-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b314-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b314-126">Registrierung mit leichteren Zugriffsberechtigungen</span><span class="sxs-lookup"><span data-stu-id="4b314-126">Registering with Ease of Access</span></span>](/windows/desktop/WinAuto/ease-of-access---assistive-technology-registration)
</dt> <dt>

[<span data-ttu-id="4b314-127">Sicherheitsüberlegungen für Hilfstechnologien</span><span class="sxs-lookup"><span data-stu-id="4b314-127">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
</dt> <dt>

[<span data-ttu-id="4b314-128">Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="4b314-128">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 