---
title: WinEvents-Infrastruktur
description: Das Microsoft Windows-Betriebssystem enthält eine Funktion mit dem Namen "WinEvents", mit der Prozesse und Anwendungen, die auf dem Windows-Desktop ausgeführt werden, bestimmte Arten von Informationen austauschen können.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "103720015"
---
# <a name="winevents"></a><span data-ttu-id="c9116-103">WinEvents</span><span class="sxs-lookup"><span data-stu-id="c9116-103">WinEvents</span></span>

<span data-ttu-id="c9116-104">Das Microsoft Windows-Betriebssystem enthält eine Funktion mit dem Namen " *WinEvents*", mit der Prozesse und Anwendungen, die auf dem Windows-Desktop ausgeführt werden, bestimmte Arten von Informationen austauschen können.</span><span class="sxs-lookup"><span data-stu-id="c9116-104">The Microsoft Windows operating system includes a feature, called *WinEvents*, that enables processes and applications running on the Windows desktop to exchange certain types of information.</span></span> <span data-ttu-id="c9116-105">Barrierefreiheits Tools, die Microsoft UI Automation und Microsoft Active Accessibility verwenden, gehören zu den Haupt Benutzern der WinEvents.</span><span class="sxs-lookup"><span data-stu-id="c9116-105">Accessibility tools that use Microsoft UI Automation and Microsoft Active Accessibility are among the primary users of the WinEvents.</span></span>

<span data-ttu-id="c9116-106">Im Kontext der Barrierefreiheit verwenden Benutzeroberflächenautomatisierungs-Anbieter und Microsoft Active Accessibility-Server WinEvents, um Clients über Änderungen in der Benutzeroberfläche einer Anwendung zu benachrichtigen, z. b. Wenn ein Benutzeroberflächen Element erstellt oder zerstört wurde oder wenn sich Elementname,-Zustand oder-Wert geändert hat.</span><span class="sxs-lookup"><span data-stu-id="c9116-106">In the context of accessibility, UI Automation providers and Microsoft Active Accessibility servers use WinEvents to notify clients of changes in an application UI, such as when a UI element has been created or destroyed, or when an element name, state, or value has changed.</span></span>

<span data-ttu-id="c9116-107">Dieser Abschnitt enthält Vorschläge, Richtlinien und Beispiele zum unterstützen von Clients bei der Handhabung von WinEvents und zur Unterstützung von Servern, die das entsprechende WinEvent-Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="c9116-107">This section provides suggestions, guidelines, and examples to help clients handle WinEvents and to help servers determine when to trigger the appropriate WinEvent.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c9116-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c9116-108">In this section</span></span>

-   [<span data-ttu-id="c9116-109">Was sind WinEvents?</span><span class="sxs-lookup"><span data-stu-id="c9116-109">What Are WinEvents?</span></span>](what-are-winevents.md)
-   [<span data-ttu-id="c9116-110">Registrieren einer Hook-Funktion</span><span class="sxs-lookup"><span data-stu-id="c9116-110">Registering a Hook Function</span></span>](registering-a-hook-function.md)
-   [<span data-ttu-id="c9116-111">Ereignisse auf System Ebene und Object-Level</span><span class="sxs-lookup"><span data-stu-id="c9116-111">System-Level and Object-Level Events</span></span>](system-level-and-object-level-events.md)
-   [<span data-ttu-id="c9116-112">Kontext-und Out-of-Context-Hook-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c9116-112">In-Context and Out-of-Context Hook Functions</span></span>](in-context-and-out-of-context-hook-functions.md)
-   [<span data-ttu-id="c9116-113">Schutz vor erneuten eintreten in Hook-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c9116-113">Guarding Against Reentrancy in Hook Functions</span></span>](guarding-against-reentrancy-in-hook-functions.md)
-   [<span data-ttu-id="c9116-114">Zuordnung von WinEvent-IDs</span><span class="sxs-lookup"><span data-stu-id="c9116-114">Allocation of WinEvent IDs</span></span>](allocation-of-winevent-ids.md)

<span data-ttu-id="c9116-115">Eine Übersicht über den Ereignis Benachrichtigungs Prozess in Microsoft Active Accessibility finden Sie unter [WinEvents](winevents-overview.md) in der [technischen Übersicht](technical-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c9116-115">For an overview of the event notification process in Microsoft Active Accessibility, see [WinEvents](winevents-overview.md) in the [Technical Overview](technical-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9116-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9116-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9116-117">Allgemeine Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="c9116-117">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




