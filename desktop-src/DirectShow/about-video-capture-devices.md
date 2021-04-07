---
description: Informationen zu Video Erfassungs Geräten
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Informationen zu Video Erfassungs Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746376"
---
# <a name="about-video-capture-devices"></a><span data-ttu-id="8d066-103">Informationen zu Video Erfassungs Geräten</span><span class="sxs-lookup"><span data-stu-id="8d066-103">About Video Capture Devices</span></span>

<span data-ttu-id="8d066-104">Die meisten neuen Video Erfassungsgeräte verwenden Windows-Treibermodell-Treiber (WDM).</span><span class="sxs-lookup"><span data-stu-id="8d066-104">Most new video capture devices use Windows Driver Model (WDM) drivers.</span></span> <span data-ttu-id="8d066-105">In der WDM-Architektur stellt Microsoft eine Reihe von hardwareunabhängigen Treibern bereit, die als Klassen Treiber bezeichnet werden, und der Hardwarehersteller stellt Hardware spezifische Mini Treiber bereit.</span><span class="sxs-lookup"><span data-stu-id="8d066-105">In the WDM architecture, Microsoft supplies a set of hardware-independent drivers, called class drivers, and the hardware vendor provides hardware-specific minidrivers.</span></span> <span data-ttu-id="8d066-106">Ein Mini Treiber implementiert alle Funktionen, die für das Gerät spezifisch sind. für die meisten Funktionen ruft der Mini Treiber den Microsoft-Klassen Treiber auf.</span><span class="sxs-lookup"><span data-stu-id="8d066-106">A minidriver implements any functions that are specific to the device; for most functions, the minidriver calls the Microsoft class driver.</span></span>

<span data-ttu-id="8d066-107">In einem DirectShow-Filter Diagramm wird jedes WDM-Erfassungsgerät als [WDM-Video Erfassungs](wdm-video-capture-filter.md) Filter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d066-107">In a DirectShow filter graph, any WDM capture device appears as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="8d066-108">Der WDM-Video Erfassungs Filter konfiguriert sich selbst basierend auf den Merkmalen des Treibers.</span><span class="sxs-lookup"><span data-stu-id="8d066-108">The WDM Video Capture filter configures itself based on the characteristics of the driver.</span></span> <span data-ttu-id="8d066-109">Sie wird unter einem vom Treiber bereitgestellten Namen angezeigt – Sie sehen keinen Filter mit dem Namen "WDM-Video Erfassungs Filter" an einer beliebigen Stelle im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="8d066-109">It appears under a name provided by the driver — you will not see a filter called "WDM Video Capture Filter" anywhere in the graph.</span></span>

<span data-ttu-id="8d066-110">Einige ältere Erfassungsgeräte verwenden weiterhin Video für Windows-Treiber (Vfw).</span><span class="sxs-lookup"><span data-stu-id="8d066-110">Some older capture devices still use Video for Windows (VFW) drivers.</span></span> <span data-ttu-id="8d066-111">Obwohl diese Treiber mittlerweile veraltet sind, werden Sie in DirectShow über den [VFW-Erfassungs](vfw-capture-filter.md) Filter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8d066-111">Although these drivers are now obsolete, they are supported in DirectShow through the [VFW Capture](vfw-capture-filter.md) filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d066-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8d066-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d066-113">Informationen zur Video Erfassung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8d066-113">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



