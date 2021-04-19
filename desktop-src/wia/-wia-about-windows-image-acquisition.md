---
description: Die Windows-Abbild Erfassungs Schnittstelle (WIA) ist sowohl eine API als auch eine Gerätetreiber Schnittstelle (DDI).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Informationen zur Windows-Abbild Erfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80eed6289f7a30476ea6889c947577ad003b656e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360554"
---
# <a name="about-windows-image-acquisition"></a><span data-ttu-id="77bbf-103">Informationen zur Windows-Abbild Erfassung</span><span class="sxs-lookup"><span data-stu-id="77bbf-103">About Windows Image Acquisition</span></span>

<span data-ttu-id="77bbf-104">Die Windows-Abbild Erfassungs Schnittstelle (WIA) ist sowohl eine API als auch eine Gerätetreiber Schnittstelle (DDI).</span><span class="sxs-lookup"><span data-stu-id="77bbf-104">The Windows Image Acquisition (WIA) interface is both an API and a device driver interface (DDI).</span></span> <span data-ttu-id="77bbf-105">Die WIA-API ist so konzipiert, dass Anwendungen:</span><span class="sxs-lookup"><span data-stu-id="77bbf-105">The WIA API is designed to allow applications to:</span></span>

-   <span data-ttu-id="77bbf-106">Führen Sie in einer robusten und stabilen Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="77bbf-106">Run in a robust and stable environment.</span></span>
-   <span data-ttu-id="77bbf-107">Minimieren von Interoperabilitätsproblemen</span><span class="sxs-lookup"><span data-stu-id="77bbf-107">Minimize interoperability problems.</span></span>
-   <span data-ttu-id="77bbf-108">Listet die verfügbaren Abbild Erwerbs Geräte auf.</span><span class="sxs-lookup"><span data-stu-id="77bbf-108">Enumerate available image acquisition devices.</span></span>
-   <span data-ttu-id="77bbf-109">Gleichzeitiges Erstellen von Verbindungen mit mehreren Geräten.</span><span class="sxs-lookup"><span data-stu-id="77bbf-109">Create connections to multiple devices simultaneously.</span></span>
-   <span data-ttu-id="77bbf-110">Abfragen von Eigenschaften von Geräten in einer standardmäßigen und erweiterbaren Weise.</span><span class="sxs-lookup"><span data-stu-id="77bbf-110">Query properties of devices in a standard and expandable manner.</span></span>
-   <span data-ttu-id="77bbf-111">Beschaffen von Gerätedaten mithilfe von Standard-und Hochleistungs Übertragungsmechanismen</span><span class="sxs-lookup"><span data-stu-id="77bbf-111">Acquire device data using standard and high performance transfer mechanisms.</span></span>
-   <span data-ttu-id="77bbf-112">Behalten Sie Bildeigenschaften über Datenübertragungen hinweg bei.</span><span class="sxs-lookup"><span data-stu-id="77bbf-112">Maintain image properties across data transfers.</span></span>
-   <span data-ttu-id="77bbf-113">Sie werden über eine Vielzahl von Geräte Ereignissen benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="77bbf-113">Be notified of a wide variety of device events.</span></span>

<span data-ttu-id="77bbf-114">Der wiaddi ist so konzipiert, dass die Menge an Code minimiert wird, die ein Hardwarehersteller schreiben muss, und gleichzeitig die Flexibilität, individuelle Lösungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77bbf-114">The WIADDI is designed to minimize the amount of code a hardware vendor must write, while maintaining the flexibility to craft individual solutions.</span></span> <span data-ttu-id="77bbf-115">Dies wird durch Folgendes erreicht:</span><span class="sxs-lookup"><span data-stu-id="77bbf-115">This is accomplished by:</span></span>

-   <span data-ttu-id="77bbf-116">Bereitstellen einer Standard-Geräte Dienst Bibliothek, mit der die meisten Treiber Vorgänge durchführt werden</span><span class="sxs-lookup"><span data-stu-id="77bbf-116">Providing a standard device service library that performs most driver operations.</span></span>
-   <span data-ttu-id="77bbf-117">Herauf Stufen von Kommunikationsstandards für Industriegeräte, sodass ein WIA-Treiber die meisten WIA-Geräte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="77bbf-117">Promoting industry device communications standards so that one WIA driver supports most WIA devices.</span></span> <span data-ttu-id="77bbf-118">Beispielsweise PTP (Picture Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="77bbf-118">For example, Picture Transfer Protocol (PTP).</span></span>
-   <span data-ttu-id="77bbf-119">Zulassen, dass der Gerätetreiber benutzerdefinierte Schnittstellen unterstützt, ohne dass die standardmäßige Geräte Dienst Bibliothek verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="77bbf-119">Allowing the device driver to support custom interfaces, while not requiring that it use the standard device service library.</span></span> <span data-ttu-id="77bbf-120">Allerdings müssen die Treiber weiterhin die standardmäßigen WIA-Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="77bbf-120">However, drivers still need to implement the standard WIA interfaces.</span></span>

<span data-ttu-id="77bbf-121">Dieser Abschnitt enthält eine kurze Übersicht über die WIA-Schnittstelle in den folgenden Bereichen:</span><span class="sxs-lookup"><span data-stu-id="77bbf-121">This section presents a brief overview of the WIA interface in the following areas:</span></span>

-   [<span data-ttu-id="77bbf-122">WIA-Architektur</span><span class="sxs-lookup"><span data-stu-id="77bbf-122">WIA Architecture</span></span>](-wia-wia-architecture.md)
-   [<span data-ttu-id="77bbf-123">STI-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="77bbf-123">STI Compatibility</span></span>](-wia-sti-compatibility.md)
-   [<span data-ttu-id="77bbf-124">TWAIN-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="77bbf-124">TWAIN Compatibility</span></span>](-wia-twain-compatibility.md)
-   [<span data-ttu-id="77bbf-125">WIA-Device Manager</span><span class="sxs-lookup"><span data-stu-id="77bbf-125">WIA Device Manager</span></span>](-wia-wia-device-manager.md)
-   [<span data-ttu-id="77bbf-126">WIA-Mini Treiber-Dienst Bibliothek</span><span class="sxs-lookup"><span data-stu-id="77bbf-126">WIA Minidriver Service Library</span></span>](-wia-wia-minidriver-service-library.md)
-   [<span data-ttu-id="77bbf-127">WIA-Mini Treiber</span><span class="sxs-lookup"><span data-stu-id="77bbf-127">WIA Minidriver</span></span>](-wia-wia-minidriver.md)

 

 



