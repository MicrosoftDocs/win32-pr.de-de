---
description: Eine lose gekoppelte Internet Explorer (LCIE) verbessert die Zuverlässigkeit des Browsers, indem seine Komponenten getrennt und die Abhängigkeiten gelockert werden.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Architektur (Cookbook zur Anwendungsqualität von Windows 7 und Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd27246b7b19765288a280bd467de86d2fe50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760081"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="3b224-103">Architektur (Cookbook zur Anwendungsqualität von Windows 7 und Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="3b224-103">Architecture (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="3b224-104">Eine *lose gekoppelte Internet Explorer* (LCIE) verbessert die Zuverlässigkeit des Browsers, indem seine Komponenten getrennt und die Abhängigkeiten gelockert werden.</span><span class="sxs-lookup"><span data-stu-id="3b224-104">*Loosely-coupled Internet Explorer* (LCIE) improves the browser’s reliability by separating its components and loosening their interdependence.</span></span>

<span data-ttu-id="3b224-105">Insbesondere versucht LCIE, den Windows Internet Explorer-Frame und seine Registerkarten in separaten Prozessen zu isolieren.</span><span class="sxs-lookup"><span data-stu-id="3b224-105">In particular, LCIE tries to isolate the Windows Internet Explorer frame and its tabs into separate processes.</span></span> <span data-ttu-id="3b224-106">In Windows Internet Explorer 8 verbessert diese Isolation die Leistung und Skalierbarkeit.</span><span class="sxs-lookup"><span data-stu-id="3b224-106">In Windows Internet Explorer 8, this isolation improves performance and scalability.</span></span> <span data-ttu-id="3b224-107">Diese Architektur Änderung kann sich auf die Kompatibilität von Erweiterungen und Add-ons auswirken, einschließlich ActiveX-Steuerelementen, Browserhilfsobjekte (BHOs) und UI-Komponenten, die mit älteren Programmiertechniken erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3b224-107">This architectural change might affect the compatibility of extensions and add-ons, including ActiveX Controls, Browser Helper Objects (BHOs), and UI toolbar components that are built by using older programming techniques.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b224-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b224-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b224-109">Entwerfen von Updates, die sich auf die Kompatibilität zwischen Browsern auswirken</span><span class="sxs-lookup"><span data-stu-id="3b224-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



