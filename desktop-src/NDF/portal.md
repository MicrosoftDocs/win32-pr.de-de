---
title: Netzwerk Diagnose-Framework
description: Das Network Diagnostics Framework (ndf) bietet Komponenten-und Anwendungsentwicklern die Möglichkeit, die Netzwerkproblem Behandlung für Benutzer zu vereinfachen.
ms.assetid: 61dfb66b-4bc6-43a9-ad61-698f5cd67f4a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0342ee4cb285f0a0f1c76c74b3bdc5b412b07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036669"
---
# <a name="network-diagnostics-framework"></a><span data-ttu-id="33282-103">Netzwerk Diagnose-Framework</span><span class="sxs-lookup"><span data-stu-id="33282-103">Network Diagnostics Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="33282-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="33282-104">Purpose</span></span>

<span data-ttu-id="33282-105">Das Network Diagnostics Framework (ndf) bietet Komponenten-und Anwendungsentwicklern die Möglichkeit, die Netzwerkproblem Behandlung für Benutzer zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="33282-105">The Network Diagnostics Framework (NDF) provides a way for component and application developers to simplify network troubleshooting for users.</span></span> <span data-ttu-id="33282-106">Benutzer können mithilfe eines einzelnen Tools zur Problembehandlung versuchen, ein Netzwerkproblem zu diagnostizieren und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="33282-106">Users can attempt to diagnose and repair a network problem using a single troubleshooting tool.</span></span>

<span data-ttu-id="33282-107">Microsoft stellt NDF-Hilfsklassen bereit, von denen einige erweiterbar sind, damit Entwickler Problem Behandlungseinheiten erstellen können, die als Hilfsklassen Erweiterungen bezeichnet werden, um detailliertere Diagnosen speziell für bestimmte Software-oder Hardwarekomponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="33282-107">Microsoft provides NDF helper classes, some of which are extensible so that developers can create troubleshooting units called helper class extensions to provide more detailed diagnoses specific to particular software or hardware components.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="33282-108">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="33282-108">Where applicable</span></span>

<span data-ttu-id="33282-109">NDF kann von jeder beliebigen Hersteller Software verwendet werden, die von der Netzwerk Konnektivität abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="33282-109">NDF can be used by any vendor's software which relies on network connectivity.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="33282-110">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="33282-110">Developer audience</span></span>

<span data-ttu-id="33282-111">Die NDF-API ist für C/C++-Entwickler konzipiert.</span><span class="sxs-lookup"><span data-stu-id="33282-111">The NDF API is designed for C/C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="33282-112">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="33282-112">Run-time requirements</span></span>

<span data-ttu-id="33282-113">NDF ist für Computer verfügbar, auf denen Windows Vista, Windows Server 2008 oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33282-113">NDF is available for computers running Windows Vista, Windows Server 2008, or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="33282-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="33282-114">In this section</span></span>



| <span data-ttu-id="33282-115">Thema</span><span class="sxs-lookup"><span data-stu-id="33282-115">Topic</span></span>                                                                       | <span data-ttu-id="33282-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33282-116">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33282-117">Informationen zu NDF</span><span class="sxs-lookup"><span data-stu-id="33282-117">About NDF</span></span>](about-ndf.md)<br/>                                       | <span data-ttu-id="33282-118">Bietet eine allgemeine Zusammenfassung der NDF-Technologie.</span><span class="sxs-lookup"><span data-stu-id="33282-118">Provides a general summary of the NDF technology.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="33282-119">Verwenden von NDF</span><span class="sxs-lookup"><span data-stu-id="33282-119">Using NDF</span></span>](using-ndf.md)<br/>                                       | <span data-ttu-id="33282-120">Bietet Informationen und Beispiele für die Verwendung von NDF-Funktionen sowie Informationen zum Erweitern dieser Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="33282-120">Provides information and examples on using NDF functionality, as well as how to extend this functionality.</span></span><br/>                                                                                    |
| [<span data-ttu-id="33282-121">NDF-Referenz</span><span class="sxs-lookup"><span data-stu-id="33282-121">NDF Reference</span></span>](ndf-reference.md)<br/>                               | <span data-ttu-id="33282-122">Bietet Informationen über Enumerationen, Funktionen, Schnittstellen und Strukturen, die die Verwendung von NDF unterstützen, sowie Informationen zu den von Microsoft bereitgestellten Extensible Helper-Klassen.</span><span class="sxs-lookup"><span data-stu-id="33282-122">Provides information about enumerations, functions, interfaces, and structures that support the use of NDF, as well as information about the extensible helper classes provided by Microsoft.</span></span><br/> |
| [<span data-ttu-id="33282-123">Netzwerk Ablauf Verfolgung in Windows 7</span><span class="sxs-lookup"><span data-stu-id="33282-123">Network Tracing in Windows 7</span></span>](network-tracing-in-windows-7.md)<br/> | <span data-ttu-id="33282-124">Erläutert die Netzwerk Ablauf Verfolgung und Tools, die zur Problembehandlung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33282-124">Discusses network tracing and tools to use for troubleshooting.</span></span><br/>                                                                                                                               |



 

 

 





