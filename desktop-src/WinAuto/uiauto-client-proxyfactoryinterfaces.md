---
title: Proxyfactory-Schnittstellen für Clients
description: In diesem Abschnitt werden die proxyfactory-Schnittstellen für nicht verwaltete Benutzeroberflächenautomatisierungs-Client Anwendungen beschrieben
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc1827ab36a221dcd7f27e5b2a05de91931b0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037458"
---
# <a name="proxy-factory-interfaces-for-clients"></a><span data-ttu-id="177f4-103">Proxyfactory-Schnittstellen für Clients</span><span class="sxs-lookup"><span data-stu-id="177f4-103">Proxy Factory Interfaces for Clients</span></span>

<span data-ttu-id="177f4-104">In diesem Abschnitt werden die proxyfactory-Schnittstellen für nicht verwaltete Benutzeroberflächenautomatisierungs-Client Anwendungen beschrieben</span><span class="sxs-lookup"><span data-stu-id="177f4-104">This section describes the proxy factory interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="177f4-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="177f4-105">In this section</span></span>



| <span data-ttu-id="177f4-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="177f4-106">Interface</span></span>                                                                                      | <span data-ttu-id="177f4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="177f4-107">Description</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="177f4-108">**Iuiautomationproxyfactory**</span><span class="sxs-lookup"><span data-stu-id="177f4-108">**IUIAutomationProxyFactory**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | <span data-ttu-id="177f4-109">Macht Eigenschaften und Methoden eines Objekts verfügbar, das einen Microsoft-Benutzeroberflächenautomatisierungs-Anbieter für Benutzeroberflächen Elemente erstellt, die keine native Unterstützung für die Benutzeroberflächen Automatisierung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="177f4-109">Exposes properties and methods of an object that creates a Microsoft UI Automation provider for UI elements that do not have native support for UI Automation.</span></span> <span data-ttu-id="177f4-110">Diese Schnittstelle wird von Proxys implementiert.</span><span class="sxs-lookup"><span data-stu-id="177f4-110">This interface is implemented by proxies.</span></span><br/>                                                                          |
| [<span data-ttu-id="177f4-111">**Iuiautomationproxyfactoriyentry**</span><span class="sxs-lookup"><span data-stu-id="177f4-111">**IUIAutomationProxyFactoryEntry**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | <span data-ttu-id="177f4-112">Stellt eine proxyfactory in der von der Benutzeroberflächen Automatisierung verwalteten Tabelle dar und macht Eigenschaften und Methoden verfügbar, die von Client Anwendungen für die Interaktion mit [**iuiautomationproxyfactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) -Objekten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="177f4-112">Represents a proxy factory in the table maintained by UI Automation, and exposes properties and methods that can be used by client applications to interact with [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) objects.</span></span><br/>                                   |
| [<span data-ttu-id="177f4-113">**Iuiautomationproxyfactoriymapping**</span><span class="sxs-lookup"><span data-stu-id="177f4-113">**IUIAutomationProxyFactoryMapping**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | <span data-ttu-id="177f4-114">Macht Eigenschaften und Methoden für eine Tabelle von proxyfactorys verfügbar.</span><span class="sxs-lookup"><span data-stu-id="177f4-114">Exposes properties and methods for a table of proxy factories.</span></span> <span data-ttu-id="177f4-115">Jeder Tabelleneintrag wird durch eine [**iuiautomationproxyfactor yentry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="177f4-115">Each table entry is represented by an [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) interface.</span></span> <span data-ttu-id="177f4-116">Die Einträge werden in der Reihenfolge angezeigt, in der das System versucht, die Proxys zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="177f4-116">The entries are in the order in which the system will attempt to use the proxies.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="177f4-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="177f4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="177f4-118">UI-Automatisierungs Clients</span><span class="sxs-lookup"><span data-stu-id="177f4-118">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





