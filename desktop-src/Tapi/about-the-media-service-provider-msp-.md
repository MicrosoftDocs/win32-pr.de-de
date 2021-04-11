---
description: Ein TAPI 3-Medien Dienstanbieter (MSP) ermöglicht einer Anwendung eine beträchtliche Kontrolle über die Medien für einen bestimmten Transportmechanismus.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: Informationen zum Media Service Provider (MSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef4d19a2f01c047d5fc2afd4a0323d7908fcac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132153"
---
# <a name="about-the-media-service-provider-msp"></a><span data-ttu-id="66493-103">Informationen zum Media Service Provider (MSP)</span><span class="sxs-lookup"><span data-stu-id="66493-103">About the Media Service Provider (MSP)</span></span>

<span data-ttu-id="66493-104">Ein TAPI 3-Medien Dienstanbieter (MSP) ermöglicht einer Anwendung eine beträchtliche Kontrolle über die Medien für einen bestimmten Transportmechanismus.</span><span class="sxs-lookup"><span data-stu-id="66493-104">A TAPI 3 media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="66493-105">Ein MSP ist immer mit einem Telefoniedienstanbieter (TSP) gekoppelt.</span><span class="sxs-lookup"><span data-stu-id="66493-105">An MSP always exists paired with a Telephony Service Provider (TSP).</span></span> <span data-ttu-id="66493-106">Ebenso wie ein TSP eine Abstraktionsschicht für die aufrufssteuerung ist, steuert der MSP Medien, ohne dass gerätespezifische Codierungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="66493-106">Just as a TSP is an abstraction layer for call control, the MSP controls media without need for device-specific coding.</span></span> <span data-ttu-id="66493-107">Ein Beispiel für die MSP/TSP-Kommunikation finden Sie unter [Übersicht über den TAPI-Dienstanbieter](./tapi-service-provider-overview.md).</span><span class="sxs-lookup"><span data-stu-id="66493-107">For an example of MSP/TSP communication, see [TAPI Service Provider Overview](./tapi-service-provider-overview.md).</span></span>

<span data-ttu-id="66493-108">Ein MSP ermöglicht die Mediensteuerung durch die Verwendung von speziellen Terminal-, Datenstrom-und substreamschnittstellen, die von TAPI definiert werden.</span><span class="sxs-lookup"><span data-stu-id="66493-108">An MSP enables media control through the use of special terminal, stream, and substream interfaces defined by TAPI.</span></span> <span data-ttu-id="66493-109">Das Diagramm in [Informationen über die Aufrufe und mediensteuer Elemente](about-call-and-media-controls.md) veranschaulicht, wie diese Schnittstellen für eine TAPI 3-Anwendung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="66493-109">The diagram in [About Call and Media Controls](about-call-and-media-controls.md) illustrates how these interfaces appear to a TAPI 3 application.</span></span>

<span data-ttu-id="66493-110">Außerdem kann ein MSP private [anbieterspezifische Schnittstellen](provider-specific-interfaces.md)implementieren, die TAPI auf den Standardobjekten aggregiert, die für eine Anwendung verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="66493-110">In addition, an MSP may implement private [provider-specific interfaces](provider-specific-interfaces.md), which TAPI will aggregate onto the standard objects exposed to an application.</span></span> <span data-ttu-id="66493-111">Beispielsweise implementiert das Microsoft ipconf msp, das mit Microsoft Windows 2000 installiert wird, die [**itteilnehmer**](itparticipant.md) -Schnittstelle, die Steuerelemente für einzelne Mitglieder einer Konferenz bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="66493-111">For example, the Microsoft IPConf MSP, which is installed with Microsoft Windows 2000, implements the [**ITParticipant**](itparticipant.md) interface, which provides controls for individual members of a conference.</span></span>

<span data-ttu-id="66493-112">Im folgenden Thema werden die MSPs kurz beschrieben, die möglicherweise mit einem Microsoft-Betriebssystem installiert werden.</span><span class="sxs-lookup"><span data-stu-id="66493-112">The following topic briefly describes the MSPs that may be installed with a Microsoft operating system.</span></span> <span data-ttu-id="66493-113">Ausführliche Informationen zur Konfiguration und Verwendung finden Sie im Ressourcenkit für die Zielplattform.</span><span class="sxs-lookup"><span data-stu-id="66493-113">For details on configuration and usage, see the resource kit for the target platform.</span></span>

<span data-ttu-id="66493-114">Zusätzliche Medien Dienstanbieter von Drittanbietern können für bestimmte Protokolle oder für physische Geräte geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="66493-114">Additional third-party media service providers can be written for particular protocols or for physical devices.</span></span> <span data-ttu-id="66493-115">Die [Media Service Provider Interface (MSPi)](media-service-provider-interface-mspi-.md) beschreibt die Schnittstellen, die implementiert werden müssen, damit ein MSP mit den Komponenten von Microsoft Telefonie interagieren kann.</span><span class="sxs-lookup"><span data-stu-id="66493-115">The [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md) describes the interfaces that must be implemented to allow an MSP to interact with the components of Microsoft Telephony.</span></span>

 

 
