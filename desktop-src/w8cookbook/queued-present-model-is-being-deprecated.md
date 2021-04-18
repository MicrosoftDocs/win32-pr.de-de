---
title: Ein in der Warteschlange vorhandenes Modell ist veraltet.
description: Ein in der Warteschlange vorhandenes Modell ist veraltet.
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "106338097"
---
# <a name="queued-present-model-is-being-deprecated"></a><span data-ttu-id="2114c-103">Ein in der Warteschlange vorhandenes Modell ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="2114c-103">Queued present model is being deprecated</span></span>

## <a name="platforms"></a><span data-ttu-id="2114c-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="2114c-104">Platforms</span></span>

<span data-ttu-id="2114c-105">**Clients** – nach Windows 8</span><span class="sxs-lookup"><span data-stu-id="2114c-105">**Clients** – After Windows 8</span></span>  
<span data-ttu-id="2114c-106">**Server** – nach Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2114c-106">**Servers** – After Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="2114c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2114c-107">Description</span></span>

<span data-ttu-id="2114c-108">In der Windows-Version nach Windows 8 geben diese APIs E \_ notimpl zurück:</span><span class="sxs-lookup"><span data-stu-id="2114c-108">In the Windows release after Windows 8, these APIs will return E\_NOTIMPL:</span></span>

-   <span data-ttu-id="2114c-109">Dwmsetpresentparameters</span><span class="sxs-lookup"><span data-stu-id="2114c-109">DwmSetPresentParameters</span></span>
-   <span data-ttu-id="2114c-110">Dwmsetdxframeduration</span><span class="sxs-lookup"><span data-stu-id="2114c-110">DwmSetDxFrameDuration</span></span>
-   <span data-ttu-id="2114c-111">Dwmmodifypreviousdxframeduration</span><span class="sxs-lookup"><span data-stu-id="2114c-111">DwmModifyPreviousDxFrameDuration</span></span>

<span data-ttu-id="2114c-112">Außerdem akzeptiert diese API nur den NULL-Wert für den HWND-Parameter:</span><span class="sxs-lookup"><span data-stu-id="2114c-112">In addition, this API will only accept the NULL value for the hwnd parameter:</span></span>

-   <span data-ttu-id="2114c-113">Dwmgetcompositiontiminginfo</span><span class="sxs-lookup"><span data-stu-id="2114c-113">DwmGetCompositionTimingInfo</span></span>

<span data-ttu-id="2114c-114">Die Unterstützung von dwmgetcompositiontiminginfo mit HWND! = NULL wird beendet, und die zugehörige Funktionalität wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="2114c-114">We will stop supporting DwmGetCompositionTimingInfo with hwnd != NULL and remove associated functionality.</span></span> <span data-ttu-id="2114c-115">Wenn ein nicht-NULL-Wert für HWND angegeben wird, gibt diese API E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="2114c-115">If non-NULL value for hwnd is specified, this API will return E\_INVALIDARG.</span></span>

<span data-ttu-id="2114c-116">Außerdem wird die Verwendung der dwmgetcompositiontiminginfo-API davon abgeraten, und es wird empfohlen, dass Entwickler zum DXGI-Flip-Modell und der zugehörigen DX-Statistik-API wechseln.</span><span class="sxs-lookup"><span data-stu-id="2114c-116">We also discourage the use of DwmGetCompositionTimingInfo API and suggest that developers switch to the DXGI flip model and associated DX present statistics API.</span></span>

## <a name="manifestation"></a><span data-ttu-id="2114c-117">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="2114c-117">Manifestation</span></span>

<span data-ttu-id="2114c-118">Anwendungen, die das in der Warteschlange stehende Modell verwenden, funktionieren nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2114c-118">Applications that use the queued present model will not function correctly.</span></span> <span data-ttu-id="2114c-119">Die genaue Manifestation hängt von der jeweiligen Anwendung ab, kann jedoch von einer falschen Präsentationszeit bis hin zu einer unerwarteten Beendigung der Anwendung reichen.</span><span class="sxs-lookup"><span data-stu-id="2114c-119">The exact manifestation depends on the particular application, but can range from incorrect presentation timing to the application exiting unexpectedly).</span></span> <span data-ttu-id="2114c-120">In der Praxis erwarten wir nicht, dass es sich um solche Anwendungen handelt.</span><span class="sxs-lookup"><span data-stu-id="2114c-120">In practice, we do not expect to see many (if any) such applications.</span></span> <span data-ttu-id="2114c-121">Dieses Modell wurde von Vista Media Player verwendet, das nicht unter Windows 8 (und möglicherweise dem alten Zune-Player) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2114c-121">This model was used by Vista media player, which will not be used on Windows 8 (and possibly the old Zune player).</span></span> <span data-ttu-id="2114c-122">Zurzeit sind keine Informationen zu anderen Anwendungen vorhanden, die dieses Modell tatsächlich verwenden.</span><span class="sxs-lookup"><span data-stu-id="2114c-122">At this time we don’t have info about any other applications actually using this model.</span></span>

## <a name="solution"></a><span data-ttu-id="2114c-123">Lösung</span><span class="sxs-lookup"><span data-stu-id="2114c-123">Solution</span></span>

<span data-ttu-id="2114c-124">Entwickler müssen den DXGI-Modus für die Flip-Darstellung anstelle der in der Warteschlange befindlichen Zeit (verfügbar in der DX9-Laufzeit seit Windows 7 und in Version DX10 und DX11-Laufzeiten in Windows 8) verwenden.</span><span class="sxs-lookup"><span data-stu-id="2114c-124">Developers need to use the DXGI flip presentation mode instead of queued present (available in DX9 runtime since Windows 7, and on DX10 and DX11 runtimes in Windows 8).</span></span>

## <a name="tests"></a><span data-ttu-id="2114c-125">Tests</span><span class="sxs-lookup"><span data-stu-id="2114c-125">Tests</span></span>

<span data-ttu-id="2114c-126">Führen Sie allgemeine Tests aus, um sicherzustellen, dass Eingangsbox-Windows-Komponenten und wichtige Produkte weiterhin unter der nächsten Version von Windows funktionieren</span><span class="sxs-lookup"><span data-stu-id="2114c-126">Run general tests to ensure that inbox Windows components and major products continue to work on the next version of Windows.</span></span>

 

 




