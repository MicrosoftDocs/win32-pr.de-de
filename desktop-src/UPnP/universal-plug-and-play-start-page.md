---
title: UPnP-APIs
description: Das UPnP-Framework ermöglicht das dynamische Netzwerk von intelligenten Geräten, drahtlosen Geräten und PCs.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102503"
---
# <a name="upnp-apis"></a><span data-ttu-id="34c12-104">UPnP-APIs</span><span class="sxs-lookup"><span data-stu-id="34c12-104">UPnP APIs</span></span>

## <a name="purpose"></a><span data-ttu-id="34c12-105">Zweck</span><span class="sxs-lookup"><span data-stu-id="34c12-105">Purpose</span></span>

<span data-ttu-id="34c12-106">Das UPnP-Framework ermöglicht das dynamische Netzwerk von intelligenten Geräten, drahtlosen Geräten und PCs.</span><span class="sxs-lookup"><span data-stu-id="34c12-106">The UPnP  framework enables dynamic networking of intelligent appliances, wireless devices, and PCs.</span></span> <span data-ttu-id="34c12-107">Für das Arbeiten mit UPnP-zertifizierten Geräten gibt es zwei APIs:</span><span class="sxs-lookup"><span data-stu-id="34c12-107">There are two APIs for working with UPnP-certified devices:</span></span>

-   <span data-ttu-id="34c12-108">Die Kontrollpunkt-API, die aus einem Satz von COM-Schnittstellen besteht, die zum Suchen und Steuern von Geräten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34c12-108">The Control Point API, which consists of a set of COM interfaces used to find and control devices.</span></span>
-   <span data-ttu-id="34c12-109">Die Geräte Host-API, die aus einem Satz von COM-Schnittstellen besteht, die zum Implementieren von Geräten verwendet werden, die von einem Computer gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="34c12-109">The Device Host API, which consists of a set of COM interfaces used to implement devices that are hosted by a computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="34c12-110">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="34c12-110">Where applicable</span></span>

<span data-ttu-id="34c12-111">Die Kontrollpunkt-API ermöglicht Entwicklern das Schreiben von Anwendungen, die nach UPnP-zertifizierten Geräten suchen und diese Steuern.</span><span class="sxs-lookup"><span data-stu-id="34c12-111">The Control Point API enables developers to write applications that search for and control UPnP-certified devices.</span></span> <span data-ttu-id="34c12-112">Die Geräte Host-API ermöglicht Entwicklern die Implementierung der Funktionalität von UPnP-zertifizierten Geräten und die Verwendung des Geräte Hosts zum Verwalten der Ermittlungs-, Beschreibungs-, Steuerungs-, Präsentations-und Ereignis Funktionen eines UPnP-zertifizierten Geräts.</span><span class="sxs-lookup"><span data-stu-id="34c12-112">The Device Host API enables developers to implement the functionality of UPnP-certified devices, and use the device host to manage the discovery, description, control, presentation, and eventing functions of a UPnP-certified device.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="34c12-113">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="34c12-113">Developer audience</span></span>

<span data-ttu-id="34c12-114">Entwickler, die die Steuerungspunkt-APIs und die Geräte Host-APIs verwenden, müssen mit der UPnP-Geräte Architektur vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="34c12-114">Developers using the Control Point APIs and Device Host APIs must be familiar with the UPnP device architecture.</span></span> <span data-ttu-id="34c12-115">Weitere Informationen finden Sie in der [UPnP-Implementierungs Dokumentation](https://openconnectivity.org/resources/upnpresources.zip) und im [UPnP-Forum](https://openconnectivity.org/).</span><span class="sxs-lookup"><span data-stu-id="34c12-115">For more information, see the [UPnP Implementation Documentation](https://openconnectivity.org/resources/upnpresources.zip) and the [UPnP Forum](https://openconnectivity.org/).</span></span>

<span data-ttu-id="34c12-116">Entwickler, die die Geräte Host-APIs verwenden, sollten mit den Active Template Library (ATL) und COM-Schnittstellen vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="34c12-116">Developers who are using the Device Host APIs should be familiar with the Active Template Library (ATL) and COM interfaces.</span></span>

<span data-ttu-id="34c12-117">Die Steuerungspunkt-APIs und die Geräte Host-APIs werden von einer Vielzahl von Anwendungen verwendet, von Skripts, die in HTML-Seiten eingebettet sind, in vollständige C++-und Microsoft Visual Basic-Programme.</span><span class="sxs-lookup"><span data-stu-id="34c12-117">The Control Point APIs and Device Host APIs are used by a variety of applications, from scripts embedded in HTML pages to full-fledged C++ and Microsoft Visual Basic programs.</span></span>

<span data-ttu-id="34c12-118">Nur die Kontrollpunkt-API unterstützt Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="34c12-118">Only the Control Point API supports Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="34c12-119">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="34c12-119">Run-time requirements</span></span>

<span data-ttu-id="34c12-120">Die Kontrollpunkt-API wird auf Computern verwendet, auf denen Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional und Windows CE .NET ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34c12-120">The Control Point API is used on computers running Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="34c12-121">Die Geräte Host-API wird auf Computern verwendet, auf denen Windows XP, Windows XP Professional und Windows CE .NET ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34c12-121">The Device Host API is used on computers running Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="34c12-122">Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in der Dokumentation unter "Anforderungen".</span><span class="sxs-lookup"><span data-stu-id="34c12-122">For more specific information about which operating systems support a particular function, refer to "Requirements" in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="34c12-123">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="34c12-123">In this section</span></span>



| <span data-ttu-id="34c12-124">Thema</span><span class="sxs-lookup"><span data-stu-id="34c12-124">Topic</span></span>                                                                                          | <span data-ttu-id="34c12-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34c12-125">Description</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34c12-126">Übersicht über die UPnP-Architektur</span><span class="sxs-lookup"><span data-stu-id="34c12-126">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)<br/>            | <span data-ttu-id="34c12-127">Allgemeine Informationen und Hintergrundinformationen.</span><span class="sxs-lookup"><span data-stu-id="34c12-127">General information and background.</span></span><br/>                                                     |
| [<span data-ttu-id="34c12-128">Übersicht über den Steuerungspunkt</span><span class="sxs-lookup"><span data-stu-id="34c12-128">Control Point Overview</span></span>](control-point-api.md)<br/>                                     | <span data-ttu-id="34c12-129">Allgemeine Informationen zur Steuerungspunkt-API.</span><span class="sxs-lookup"><span data-stu-id="34c12-129">General information about the Control Point API.</span></span><br/>                                        |
| [<span data-ttu-id="34c12-130">Verwenden der Steuerungspunkt-API</span><span class="sxs-lookup"><span data-stu-id="34c12-130">Using the Control Point API</span></span>](using-the-control-point-api-with-upnp-technology.md)<br/> | <span data-ttu-id="34c12-131">Beispielcode, der zeigt, wie Sie Anwendungen entwickeln, mit denen UPnP-zertifizierte Geräte gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="34c12-131">Sample code that shows how to develop applications that control UPnP-certified devices.</span></span><br/> |
| [<span data-ttu-id="34c12-132">API-Referenz für Steuerungspunkt</span><span class="sxs-lookup"><span data-stu-id="34c12-132">Control Point API Reference</span></span>](control-point-api-with-upnp-technology-reference.md)<br/> | <span data-ttu-id="34c12-133">Dokumentation der Schnittstellen, Methoden und Ereignisse von Steuerungspunkt Komponenten.</span><span class="sxs-lookup"><span data-stu-id="34c12-133">Documentation of Control Point component interfaces, methods, and events.</span></span><br/>               |
| [<span data-ttu-id="34c12-134">Übersicht über die Geräte Host-API</span><span class="sxs-lookup"><span data-stu-id="34c12-134">Device Host API Overview</span></span>](device-host-api.md)<br/>                                     | <span data-ttu-id="34c12-135">Allgemeine Informationen zur Geräte Host-API.</span><span class="sxs-lookup"><span data-stu-id="34c12-135">General information about the Device Host API.</span></span><br/>                                          |
| [<span data-ttu-id="34c12-136">Verwenden der Geräte Host-API</span><span class="sxs-lookup"><span data-stu-id="34c12-136">Using the Device Host API</span></span>](using-the-device-host-api-with-upnp-technology.md)<br/>     | <span data-ttu-id="34c12-137">Beispielcode, der zeigt, wie eine Anwendung für UPnP-zertifizierte Geräte entwickelt wird.</span><span class="sxs-lookup"><span data-stu-id="34c12-137">Sample code that shows how to develop an application for UPnP-certified devices.</span></span><br/>        |
| [<span data-ttu-id="34c12-138">Referenz zur Geräte Host-API</span><span class="sxs-lookup"><span data-stu-id="34c12-138">Device Host API Reference</span></span>](device-host-api-with-upnp-technology-reference.md)<br/>     | <span data-ttu-id="34c12-139">Dokumentation zu Geräte Host Komponenten-Schnittstellen, Methoden und Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="34c12-139">Documentation of Device Host component interfaces, methods, and events.</span></span><br/>                 |



 

 

 





