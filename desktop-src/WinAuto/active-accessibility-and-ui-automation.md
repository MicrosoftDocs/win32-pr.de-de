---
title: Active Accessibility und Benutzeroberflächen Automatisierung
description: Microsoft Active Accessibility ist für die Verwendung mit Windows XP und früheren Betriebssystemen konzipiert.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341885"
---
# <a name="active-accessibility-and-ui-automation"></a><span data-ttu-id="95219-103">Active Accessibility und Benutzeroberflächen Automatisierung</span><span class="sxs-lookup"><span data-stu-id="95219-103">Active Accessibility and UI Automation</span></span>

<span data-ttu-id="95219-104">Microsoft Active Accessibility ist für die Verwendung mit Windows XP und früheren Betriebssystemen konzipiert.</span><span class="sxs-lookup"><span data-stu-id="95219-104">Microsoft Active Accessibility is designed for use with Windows XP and earlier operating systems.</span></span> <span data-ttu-id="95219-105">Entwickler von benutzerdefinierten Steuerelementen und zugänglichen Technologie Client Anwendungen für Windows XP und Windows Vista sollten stattdessen die Verwendung von Microsoft [UI Automation](entry-uiauto-win32.md) in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="95219-105">Developers of custom controls and accessible technology client applications for Windows XP and Windows Vista should consider using Microsoft [UI Automation](entry-uiauto-win32.md) instead.</span></span>

<span data-ttu-id="95219-106">Microsoft UI Automation ist ein System mit vollem Funktionsumfang, das präzisere Informationen über die Benutzeroberfläche bereitstellt und dem Benutzer die Interaktion mit Steuerelementen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="95219-106">Microsoft UI Automation is a full-featured system that provides more precise information about the user interface and gives the user more ability to interact with controls.</span></span> <span data-ttu-id="95219-107">Insbesondere bietet Sie eine stark verbesserte Unterstützung für Text.</span><span class="sxs-lookup"><span data-stu-id="95219-107">In particular, it provides greatly enhanced support for text.</span></span>

<span data-ttu-id="95219-108">Ein Satz von Proxy Objekten bietet Unterstützung für die Benutzeroberflächen Automatisierung für standardmäßige Microsoft Win32-und Windows Forms-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="95219-108">A set of proxy objects provides UI Automation support for standard Microsoft Win32 and Windows Forms controls.</span></span> <span data-ttu-id="95219-109">Umfangreichere Unterstützung ist für Steuerelemente verfügbar, die speziell im Hinblick auf die Benutzeroberflächen Automatisierung geschrieben wurden, einschließlich System eigener Windows Presentation Foundation (WPF)-Elemente, die Microsoft Active Accessibility nicht direkt unterstützen.</span><span class="sxs-lookup"><span data-stu-id="95219-109">Richer support is available for controls specifically written with UI Automation in mind, including native Windows Presentation Foundation (WPF) elements, which do not directly support Microsoft Active Accessibility.</span></span> <span data-ttu-id="95219-110">Benutzerdefinierte Steuerelemente, die Benutzeroberflächen Automatisierung unterstützen, können in verwaltetem oder nicht verwaltetem Code geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="95219-110">Custom controls that support UI Automation can be written in either managed or unmanaged code.</span></span>

<span data-ttu-id="95219-111">Microsoft Active Accessibility-Clients haben über eine Überbrückungs Schicht eingeschränkten Zugriff auf Benutzeroberflächen Elemente, die nur die Automatisierung der Benutzeroberfläche unterstützen.</span><span class="sxs-lookup"><span data-stu-id="95219-111">Microsoft Active Accessibility clients have limited access, through a bridging layer, to UI elements that support only UI Automation.</span></span> <span data-ttu-id="95219-112">Weitere Informationen finden Sie unter [Anhang G: Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span><span class="sxs-lookup"><span data-stu-id="95219-112">For more information, see [Appendix G: Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span></span>

<span data-ttu-id="95219-113">Weitere Informationen zu den Ähnlichkeiten und unterschieden zwischen Microsoft Active Accessibility und der Automatisierung der Benutzeroberfläche finden Sie [im Vergleich zu Microsoft Active Accessibility und UI-Automatisierung](microsoft-active-accessibility-and-ui-automation-compared.md).</span><span class="sxs-lookup"><span data-stu-id="95219-113">For more information about the similarities and differences between Microsoft Active Accessibility and UI Automation, see [Microsoft Active Accessibility and UI Automation Compared](microsoft-active-accessibility-and-ui-automation-compared.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95219-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95219-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="95219-115">**Licher**</span><span class="sxs-lookup"><span data-stu-id="95219-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="95219-116">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="95219-116">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="95219-117">Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="95219-117">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




