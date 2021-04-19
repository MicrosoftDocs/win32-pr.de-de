---
description: Das Filter Diagramm und dessen Komponenten
ms.assetid: 3747bfcd-1e4a-404c-a493-26d3c20bab21
title: Das Filter Diagramm und dessen Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473fb3dfe327eb43bb2065417c7be80f7537d06a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356962"
---
# <a name="the-filter-graph-and-its-components"></a><span data-ttu-id="7ef54-103">Das Filter Diagramm und dessen Komponenten</span><span class="sxs-lookup"><span data-stu-id="7ef54-103">The Filter Graph and Its Components</span></span>

<span data-ttu-id="7ef54-104">In diesem Artikel werden die Hauptkomponenten von DirectShow beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7ef54-104">This article describes the major components of DirectShow.</span></span> <span data-ttu-id="7ef54-105">Es ist eine Einführung für Anwendungsentwickler und Entwickler, die benutzerdefinierte DirectShow-Filter schreiben.</span><span class="sxs-lookup"><span data-stu-id="7ef54-105">It is intended as an introduction for application developers and for developers writing custom DirectShow filters.</span></span> <span data-ttu-id="7ef54-106">Anwendungsentwickler können normalerweise viele der Details von DirectShow auf niedriger Ebene ignorieren.</span><span class="sxs-lookup"><span data-stu-id="7ef54-106">Application developers can usually ignore many of the low-level details of DirectShow.</span></span> <span data-ttu-id="7ef54-107">Es ist jedoch immer noch ratsam, diesen Abschnitt zu lesen, um ein allgemeines Verständnis der DirectShow-Architektur zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7ef54-107">However, it is still a good idea to read this section, to have a general understanding of the DirectShow architecture.</span></span>

<span data-ttu-id="7ef54-108">Dieser Artikel enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="7ef54-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="7ef54-109">Informationen zu DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="7ef54-109">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="7ef54-110">Informationen zum Filter Graph-Manager</span><span class="sxs-lookup"><span data-stu-id="7ef54-110">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)
-   [<span data-ttu-id="7ef54-111">Informationen zu Medientypen</span><span class="sxs-lookup"><span data-stu-id="7ef54-111">About Media Types</span></span>](about-media-types.md)
-   [<span data-ttu-id="7ef54-112">Informationen zu Medien Beispielen und-Zuweisungen</span><span class="sxs-lookup"><span data-stu-id="7ef54-112">About Media Samples and Allocators</span></span>](about-media-samples-and-allocators.md)
-   [<span data-ttu-id="7ef54-113">Einbeziehung von Hardware Geräten in das Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="7ef54-113">How Hardware Devices Participate in the Filter Graph</span></span>](how-hardware-devices-participate-in-the-filter-graph.md)

 

 



